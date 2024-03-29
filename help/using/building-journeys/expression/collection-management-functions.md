---
solution: Journey Optimizer
product: journey optimizer
title: 收集管理函式
description: 瞭解集合管理函式中的資料型別
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 查詢，集合，函式，裝載，歷程
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
source-git-commit: b58d6bbcf2311be3f841f7eef0c0bf10692f1704
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 3%

---

# 收集管理函式 {#collection-management-functions}

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

**函式&quot;all(`<condition>`)」**

此 **[!UICONTROL 全部]** 函式可讓您使用布林運算式在指定集合上定義篩選器。

```json
<listExpression>.all(<condition>)
```

例如，在所有應用程式使用者中，您可以透過IOS 13 (布林運算式「IOS 13==使用的應用程式」)取得使用者。 此函式的結果是篩選的清單，其中包含符合布林值運算式的專案（例如：應用程式使用者1、應用程式使用者34、應用程式使用者432）。

在資料來源條件活動中，您可以檢查結果是否為 **[!UICONTROL 全部]** 函式是否為空值。 您也可以合併此專案 **[!UICONTROL 全部]** 函式與其他函式，例如 **[!UICONTROL count]**. 如需詳細資訊，請參閱 [資料來源條件活動](../condition-activity.md#data_source_condition).

**範例 1:**

我們要檢查使用者是否已安裝特定版本的應用程式。 對此，我們會取得與行動應用程式（1.0版）相關的所有推播通知權杖。接著，我們使用 **[!UICONTROL count]** 函式，以檢查傳回的Token清單是否包含至少一個元素。

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

結果為true。

**範例 2:**

在此處，我們使用 **[!UICONTROL count]** 函式來檢查集合中是否有推播通知權杖。

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```

結果將會是true。

<!--Alternatively, you can check if there is no token in the collection:

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
earlier timestamp) in order to only consider prior events.-->

>[!NOTE]
>
>當中的篩選條件 **all()** 函式空白，則篩選條件會傳回清單中的所有元素。 **不過，若要計算集合的元素數，不需要all函式。**


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

運算式的結果為 **3**.

**範例 3:**

在此處，我們會檢查個人在過去24小時內是否未收到任何通訊。 我們會根據集合的兩個元素，使用兩個運算式，來篩選從ExperiencePlatform資料來源擷取的體驗事件集合。 尤其是，事件的時間戳記會與傳回的dateTime比較， **[!UICONTROL nowWithΔ]** 函式。

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

<!--**"All + Count" example 4:** here we use the count function in a boolean expression to see if there is push notification tokens in the collection.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) > 0`

The result will be:

`true`

Alternatively, you can check if there is NO token in the collection:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) =0`

The result will be:

`false`-->

>[!NOTE]
>
>**[!UICONTROL currentEventField]** 僅適用於操控事件集合， **[!UICONTROL currentDataPackField]** 操控資料來源集合和 **[!UICONTROL currentActionField]** 操控自訂動作回應集合時。
>
>處理集合時使用 **[!UICONTROL 全部]**， **[!UICONTROL 第一]** 和 **[!UICONTROL 上次]**，我們會逐一在集合的每個元素上回圈。 **[!UICONTROL currentEventField]**， **currentDataPackField** 和 **[!UICONTROL currentActionField]** 與正在循環的元素相對應。

**函式「first(`<condition>`)」和「last(`<condition>`)」**

此 **[!UICONTROL 第一]** 和 **[!UICONTROL 上次]** 函式也會在集合上啟用篩選的定義，同時傳回符合篩選的清單的第一個/最後一個元素。

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
>* **[!UICONTROL 第一]** 函式將傳回最近的事件
>* **[!UICONTROL 上次]** 函式會傳回最舊的一個。

**範例 3:**

我們會檢查第一個（最新）DMA ID為非零值的Adobe Analytics事件是否具有等於602的值。

```json
#{ExperiencePlatform.AnalyticsProd_EvarsProps.experienceevent.first(
currentDataPackField.placeContext.geo.dmaID > 0).placeContext.geo.dmaID} == 602
```

**函式&quot;at(`<index>`)」**

此 **[!UICONTROL 在]** 函式可讓您根據索引來參照集合中的特定元素。
索引0是集合的第一個索引。

_`<listExpression>`.at(`<index>`)_

**範例：**

此運算式會傳回清單的第二個推播通知權杖。

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

結果為「token_2」。

**其他範例**

```json
#{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent. all(currentDataPackField._aepgdcdevenablement2.purchase_event.receipt_nbr == "10-337-4016"). 
_aepgdcdevenablement2.purchase_event.productListItems. all(currentDataPackField.SKU == "AB17 1234 1775 19DT B4DR 8HDK 762").name}
```

```json
 #{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.last(
currentDataPackField.eventType == "commerce.productListAdds").productListItems.last(currentDataPackField.priceTotal >= 150).name}
```
