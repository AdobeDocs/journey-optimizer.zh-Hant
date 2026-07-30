---
solution: Journey Optimizer
product: journey optimizer
title: 集合管理功能
description: 瞭解集合管理函式中的資料型別
feature: Journeys
hide: true
role: Developer
level: Experienced
keywords: 查詢，集合，函式，裝載，歷程
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1222
ht-degree: 1%

---

# 集合管理功能

運算式語言也會引入一組函式來查詢集合。

這些函式將於下文說明。 在下列範例中，讓我們使用包含集合的事件裝載：

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

**函式「all(`<condition>`)」**

**[!UICONTROL all]**&#x200B;函式使用布林運算式啟用指定集合上篩選的定義。

```json
<listExpression>.all(<condition>)
```

例如，在所有應用程式使用者中，您可以透過IOS 13 （布林運算式「IOS 13==使用的應用程式」）取得使用者。 此函式的結果是篩選的清單，其中包含符合布林值運算式的專案（例如：應用程式使用者1、應用程式使用者34、應用程式使用者432）。

在資料Source條件活動中，您可以檢查&#x200B;**[!UICONTROL all]**&#x200B;函式的結果是否為Null。 您也可以將此&#x200B;**[!UICONTROL 所有]**&#x200B;函式與其他函式（例如&#x200B;**[!UICONTROL count]**）結合。 如需詳細資訊，請參閱[資料Source條件活動](../conditions.md#data_source_condition)。


## 範例

>[!CAUTION]
>
>支援在歷程運算式/條件中使用體驗事件，但不建議使用。 如果您的使用案例需要使用體驗事件，請考慮替代方法，例如[計算屬性](../../audience/computed-attributes.md)，或使用事件建立區段並將該區段合併到[`inAudience`運算式](../../building-journeys/functions/functioninaudience.md)中。

**範例 1:**

我們要檢查使用者是否已安裝特定版本的應用程式。 對此，我們會取得與行動應用程式（1.0版）相關的所有推播通知權杖。 接著，我們會使用&#x200B;**[!UICONTROL count]**&#x200B;函式執行條件，以檢查傳回的權杖清單是否至少包含一個元素。

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

結果為true。

**範例 2:**

在此處，我們使用&#x200B;**[!UICONTROL count]**&#x200B;函式來檢查集合中是否有推播通知權杖。

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```

結果將會是true。

<!--
Alternatively, you can check if there is no token in the collection:

   ```json
   count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) == 0
   ```

The result will be false.

Here we use the count function in a condition to count the number of push notification tokens in the event.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token})`

The result is true.

Note that when the condition in the **all()** function is empty, the filter will return all the elements in the list. Hence, the expression above is equivalent to:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.application.name})`

In both cases, the result of the expression is **3**.

A query of experience events recorded on the Adobe Experience Platform may or may not include the current event that triggered the current Journey. This will depend on the relative processing time with which [!DNL Journey Orchestration] sees an event and started evaluating conditions, versus the time it takes for that event to be ingested into the Adobe Experience Platform. For example, when using the .all() syntax to query experience events from the Adobe Experience Platform, we recommend enforcing the exclusion of the current event (by requiring an
earlier timestamp) in order to only consider prior events.
-->

>[!NOTE]
>
>當&#x200B;**all()**&#x200B;函式中的篩選條件為空白時，篩選器會傳回清單中的所有元素。 **但是，若要計算集合的元素數目，不需要all函式。**


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

運算式的結果是&#x200B;**3**。

**範例 3:**

在此處，我們會檢查個人在過去24小時內是否未收到任何通訊。 我們會根據集合的兩個元素，使用兩個運算式，來篩選從ExperiencePlatform資料來源擷取的體驗事件集合。 特別是，會比較事件的時間戳記與&#x200B;**[!UICONTROL nowWithDelta]**&#x200B;函式傳回的dateTime。

```json
count(#{ExperiencePlatform.MarltonExperience.experienceevent.all(
   currentDataPackField.directMarketing.sends.value > 0 and
   currentDataPackField.timestamp > nowWithDelta(-1, "days")).timestamp}) == 0
```

如果沒有體驗事件符合兩個條件，則結果為true。

**範例 4:**

在此處，我們想檢查個人在過去7天內是否至少啟動過一次應用程式，以便觸發推播通知，邀請他們啟動教學課程。

```json
count(
 #{ExperiencePlatform.AnalyticsData.experienceevent.all(
 nowWithDelta(-7,"days") <= currentDataPackField.timestamp
 and currentDataPackField.application.firstLaunches.value > 0
)._id}) > 0
```

<!--
**"All + Count" example 4:** here we use the count function in a boolean expression to see if there is push notification tokens in the collection.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) > 0`

The result will be:

`true`

Alternatively, you can check if there is NO token in the collection:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) =0`

The result will be:

`false`
-->

>[!NOTE]
>
>**[!UICONTROL currentEventField]**&#x200B;僅可在操控事件集合時使用，**[!UICONTROL currentDataPackField]**&#x200B;在操控資料來源集合時使用，以及&#x200B;**[!UICONTROL currentActionField]**&#x200B;在操控自訂動作回應集合時使用。
>
>處理具有&#x200B;**[!UICONTROL all]**、**[!UICONTROL first]**&#x200B;和&#x200B;**[!UICONTROL last]**&#x200B;的集合時，我們會逐一在集合的每個元素上回圈。 **[!UICONTROL currentEventField]**、**currentDataPackField**&#x200B;和&#x200B;**[!UICONTROL currentActionField]**&#x200B;對應到正在回圈的元素。

**函式「first(`<condition>`)」和「last(`<condition>`)」**

**[!UICONTROL first]**&#x200B;和&#x200B;**[!UICONTROL last]**&#x200B;函式也會在集合上啟用篩選的定義，同時傳回符合篩選的清單的第一個/最後一個元素。

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

**範例 1:**

此運算式會傳回與版本為1.0的行動應用程式關聯的第一個推播通知權杖。

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token
```

結果為「token_1」。

**範例 2:**

此運算式會傳回與版本為1.0的行動應用程式相關聯的最後一個推播通知權杖。

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

結果為「token_2」。

>[!NOTE]
>
>體驗事件會以反向時間順序的集合形式從Adobe Experience Platform擷取，因此：
>
>* **[!UICONTROL first]**&#x200B;函式將傳回最近的事件
>* **[!UICONTROL last]**&#x200B;函式將傳回最舊的函式。

**範例 3:**

我們會檢查第一個（最新）DMA ID為非零值的Adobe Analytics事件是否具有等於602的值。

```json
#{ExperiencePlatform.AnalyticsProd_EvarsProps.experienceevent.first(
currentDataPackField.placeContext.geo.dmaID > 0).placeContext.geo.dmaID} == 602
```

**函式&quot;at(`<index>`)&quot;**

**[!UICONTROL at]**&#x200B;函式可讓您根據索引來參照集合中的特定專案。
索引0是集合的第一個索引。

_`<listExpression>`.at(`<index>`)_

**範例：**

此運算式會傳回清單的第二個推播通知權杖。

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

結果為「token_2」。

**其他範例**

此運算式會根據SKU值傳回產品名稱。 這些產品的清單會包含在事件清單中，其條件為事件ID。

```json
#{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.all(currentDataPackField._aepgdcdevenablement2.purchase_event.receipt_nbr == "10-337-4016"). 
_aepgdcdevenablement2.purchase_event.productListItems.all(currentDataPackField.SKU == "AB17 1234 1775 19DT B4DR 8HDK 762").name}
```

此運算式會擷取商務事件的產品清單中最後一個產品的名稱，其中事件型別為「productListAdds」，且總價大於或等於150。

```json
 #{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.last(
currentDataPackField.eventType == "commerce.productListAdds").productListItems.last(currentDataPackField.priceTotal >= 150).name}
```

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面說明歷程運算式語言中可用的集合管理函式`all()`、`first()`、`last()`和`at()`，並提供使用推播通知權杖裝載和體驗事件資料的範例。

**意圖：**

* 使用帶有`all(<condition>)`的布林條件來篩選集合，以擷取相符元素
* 使用與`all()`結合的`count()`函式計算集合中的專案
* 使用`first()`或`last()`擷取篩選集合的第一個或最後一個元素
* 使用`at(<index>)`建立索引來存取集合中的特定元素
* 結合巢狀集合查詢，以依SKU或依事件型別和價格臨界值查詢產品名稱

**字彙表：**

* **all(condition)**：篩選清單並傳回符合指定布林運算式&#x200B;*（產品特定）*&#x200B;之專案的集合函式
* **first(condition)**：傳回符合條件&#x200B;*（產品特定）*&#x200B;之第一個（體驗事件的最近）元素的集合函式
* **last(condition)**：傳回符合條件&#x200B;*（產品特定）*&#x200B;之最後（體驗事件的最舊）專案的集合函式
* **at(index)**：傳回位於特定從零開始的索引&#x200B;*（產品特定）*&#x200B;之專案的集合函式
* **currentEventField**：重複處理`all()`、`first()`或`last()`內的事件集合時，可以使用回圈變數&#x200B;*（產品特定）*
* **currentDataPackField**：重複處理資料來源集合&#x200B;*（產品特定）時可以使用回圈變數*
* **currentActionField**：重複處理自訂動作回應集合&#x200B;*（產品特定）時可以使用回圈變數*

**護欄：**

* 支援在歷程運算式/條件中使用體驗事件，但不建議使用；請考慮將計算屬性或受眾區段作為替代方案
* `currentEventField`僅適用於事件集合；`currentDataPackField`適用於資料來源集合；`currentActionField`適用於自訂動作回應集合
* `all`函式不一定要用來計算集合的元素 — `count()`可以直接套用至集合欄位
* 體驗事件會以反向時間順序擷取： `first()`會傳回最近的事件，`last()`會傳回最舊的事件

**術語：**

* 正式名稱：集合管理函式 — 縮寫：無 — 變體：集合函式，查詢集合函式
* 同義字： &quot;all()&quot; = &quot;filter function&quot;； &quot;first()&quot; = &quot;most recent element function&quot; （適用於體驗事件）
* 請勿混淆： `first()` （最近體驗事件）≠插入順序的第一個專案

**常見問題集：**

* **問：當條件為空時，`all()`會傳回什麼？**  — 它會傳回清單中的所有元素，相當於沒有篩選。
* **問：如何計算集合中推播通知權杖的數量？**  — 直接在權杖欄位路徑上使用`count()`，不需要`all()`，例如`count(@event{...pushNotificationTokens.token})`。
* **問：如何取得集合的第二個元素？**  — 使用`at(1)`，因為索引0是第一個元素。
* **問：為什麼`first()`會傳回最近的體驗事件？**  — 體驗事件是從Adobe Experience Platform中擷取，並依照反向時間順序，因此`first()`會挑選排名最前的（最新）專案。
* **問：如何檢查使用者在過去24小時內是否未收到任何通訊？**  — 篩選以`nowWithDelta(-1, "days")`作為時間戳記下限的體驗事件集合，並使用`count(...) == 0`。

+++
