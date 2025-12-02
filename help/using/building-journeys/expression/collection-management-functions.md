---
solution: Journey Optimizer
product: journey optimizer
title: 集合管理功能
description: 瞭解集合管理函式中的資料型別
feature: Journeys
role: Developer
level: Experienced
keywords: 查詢，集合，函式，裝載，歷程
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
version: Journey Orchestration
source-git-commit: e7693ba84d8806cf4b0dc10e8fdd18f2511e37ea
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 3%

---

# 集合管理功能 {#collection-management-functions}


## 關於查詢收集函式

運算式語言也會引入一組函式來查詢集合。 這些函式將於下文說明。

在下列範例中，我們使用名為「LobbyBeacon」的事件，其中包含推播通知權杖的集合。 本頁面的範例使用事件裝載結構，如下所示：

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

>[!NOTE]
>
>在下列範例中，此裝載是使用`@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens}`參考的，其中「LobbyBeacon」是事件名稱，而路徑的其餘部分則對應至上述結構。

## all(`<condition>`)函式

**[!UICONTROL all]**&#x200B;函式使用布林運算式啟用指定集合上篩選的定義。

```json
<listExpression>.all(<condition>)
```

**概念範例：**&#x200B;在所有應用程式使用者中，您可以使用IOS 13 (布林運算式「用於IOS 13」==應用程式)來取得這些使用者。 此函式的結果是篩選的清單，其中包含符合布林值運算式的專案（例如：應用程式使用者1、應用程式使用者34、應用程式使用者432）。

在資料Source條件活動中，您可以檢查&#x200B;**[!UICONTROL all]**&#x200B;函式的結果是否為Null。 您也可以將此&#x200B;**[!UICONTROL 所有]**&#x200B;函式與其他函式（例如&#x200B;**[!UICONTROL count]**）結合。 如需詳細資訊，請參閱[資料Source條件活動](../condition-activity.md#data_source_condition)。

**使用LobbyBeacon裝載的程式碼範例：**

以下範例會使用顯示在此頁面頂端的事件裝載。


>[!CAUTION]
>
>不支援在歷程運算式/條件中使用體驗事件。 如果您的使用案例需要使用體驗事件，請考慮替代方法。 [了解更多](../exp-event-lookup.md)

### 範例 1

我們要檢查使用者是否已安裝特定版本的應用程式。 對此，我們會取得與行動應用程式（1.0版）相關的所有推播通知權杖。接著，我們會使用&#x200B;**[!UICONTROL count]**&#x200B;函式執行條件，以檢查傳回的權杖清單是否至少包含一個元素。

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

結果為true。

### 範例 2

在此處，我們使用&#x200B;**[!UICONTROL count]**&#x200B;函式來檢查集合中是否有推播通知權杖。

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


結果為true。


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

運算式的結果是&#x200B;**3**。


>[!NOTE]
>
>* 當&#x200B;**all()**&#x200B;函式中的篩選條件為空白時，篩選器會傳回清單中的所有元素。 **但是，若要計算集合的元素數目，不需要all函式。**
>
>* `currentEventField`僅適用於操控事件集合、`currentDataPackField`適用於操控資料來源集合，以及`currentActionField`適用於操控自訂動作回應集合。
>
>  處理具有`all`、`first`和`last`的集合時，我們會逐一在集合的每個元素上回圈。 `currentEventField`、`currentDataPackField`和`currentActionField`對應到正在回圈的元素。


## 第一個(`<condition>`)和最後一個(`<condition>`)函式

**[!UICONTROL first]**&#x200B;和&#x200B;**[!UICONTROL last]**&#x200B;函式也會在集合上啟用篩選的定義，同時傳回符合篩選的清單的第一個/最後一個元素。

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### 範例 1

此運算式會傳回與版本為1.0的行動應用程式關聯的第一個推播通知權杖。


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

結果為`token_1`。

### 範例 2

此運算式會傳回與版本為1.0的行動應用程式相關聯的最後一個推播通知權杖。


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

結果為`token_2`。

## at(`<index>`)函式

**[!UICONTROL at]**函式可讓您根據索引來參照集合中的特定專案。
索引0是集合的第一個索引。

_`<listExpression>`.at(`<index>`)_

### 範例

此運算式會傳回清單的第二個推播通知權杖。


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

結果為`token_2`。