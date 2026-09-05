---
title: 在網頁SDK中設定收件匣支援
description: 瞭解如何透過Adobe Experience Platform Web SDK，使用內容卡和收件匣行銷活動在Adobe Journey Optimizer中建立永續性訊息收件匣。
feature: Content Cards
topic: Content Management
role: Developer
level: Experienced
source-git-commit: 1ee6fd3ed3523635ea7dbe46dbae0e2403246818
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 1%

---

# 在 Web SDK 中設定收件匣支援 {#inbox-configuration-sdk}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;設定並執行結合內容卡行銷活動和收件匣行銷活動與Adobe Experience Platform Web SDK的範例，以便在您的網站上傳遞永續性通知收件匣。

>[!ENDSHADEBOX]

訊息收件匣是持續性通知收件匣，由定位相同表面的兩個Adobe Journey Optimizer行銷活動驅動：

* **內容卡行銷活動**，可將個別通知專案傳送至收件匣。
* **收件匣行銷活動**，可提供標題、空白狀態副本和版面配置等設定。


## 設定 Adobe Journey Optimizer {#ajo-setup}

在實作Web SDK之前，請先在Journey Optimizer中設定將內容傳送至收件匣的資料流、管道和行銷活動。

1. 設定以&#x200B;**Adobe Experience Platform**&#x200B;設定為服務的&#x200B;**資料流**，並啟用&#x200B;**Journey Optimizer**&#x200B;並選取&#x200B;**事件資料集**。

1. 建立共用相同表面的兩個管道設定：一個&#x200B;**內容卡**&#x200B;管道和一個&#x200B;**收件匣**&#x200B;管道。 [瞭解如何設定內容卡頻道](../content-card/content-card-configuration.md)和[瞭解如何設定收件匣頻道](inbox-configuration.md)。

   將兩個管道的頁面&#x200B;**上的**&#x200B;頁面URL **和**&#x200B;位置設定為您在先決條件中定義的表面。 此位置必須符合您在網頁SDK程式碼中查詢的介面。

1. [建立內容卡行銷活動](../content-card/create-content-card.md)，此行銷活動將內容卡頻道用於其內容卡設定。

   對於應該根據網頁上的使用者動作傳遞的訊息，請在相關動作上啟用&#x200B;**其他傳遞規則**，並設定事件和值條件，以決定訊息何時出現。 對收件匣應收到的每種通知型別重複此步驟。

1. [建立使用收件匣通道的收件匣行銷活動](inbox-create.md)。 此行銷活動會傳送設定收件匣殼層本身的中繼資料。

   比對收件匣行銷活動的對象和排程設定與內容卡行銷活動，讓兩者對相同使用者同時有效。

1. 啟用兩個行銷活動。

## 實作Web SDK {#web-sdk-implementation}

收件匣需仰賴兩個Web SDK命令：

* `subscribeRulesetItems`註冊每次在符合顯示變更資格的主張時執行的回呼。

* `sendEvent`會擷取這些主張。 您可以稍後傳送其他事件，以更新哪些訊息符合顯示資格。

1. 定義內容卡和收件匣結構，以及符合您AJO頻道設定的表面：

   ```javascript
   const CONTENT_CARD_SCHEMA = "https://ns.adobe.com/personalization/message/content-card";
   const INBOX_SCHEMA        = "https://ns.adobe.com/personalization/message/inbox";
   const SURFACE             = "web://your-site.example/#message-inbox";
   ```

1. 使用您的資料流設定網頁SDK：

   ```javascript
   alloy("configure", {
     datastreamId: "YOUR_DATASTREAM_ID",
     orgId: "YOUR_ORG_ID@AdobeOrg",
     defaultConsent: "in", // May not be usable in your implementation, but should be used for testing
     personalizationStorageEnabled: true,
   })
   ```

1. 訂閱表面和結構描述的規則集專案，並提供回撥以在內容卡片主張變更時處理這些主張：

   ```javascript
   alloy("subscribeRulesetItems", {
     surfaces: [SURFACE],
     schemas: [CONTENT_CARD_SCHEMA, INBOX_SCHEMA],
     callback: (result, collectEvent) => {
       const { propositions = [] } = result;
       const notifications = propositions
         .filter((p) => p.items?.[0]?.schema === CONTENT_CARD_SCHEMA)
         .map((proposition) => {
           const content = proposition.items[0]?.data?.content ?? {};
           return {
             id: proposition.scopeDetails.activity.id,
             title: content.title?.content ?? content.title ?? "",
             description: content.body?.content ?? content.body ?? "",
             proposition,
           };
         });
       renderNotifications(notifications, collectEvent);
     },
   });
   ```

1. 當使用者與您的應用程式互動時，傳送事件以更新應顯示的內容卡片主張：

   ```javascript
   alloy("sendEvent", {
     renderDecisions: true,
     personalization: { surfaces: [SURFACE] },
   });
   ```

1. 使用`subscribeRulesetItems`回呼提供的`collectEvent`函式，將互動回報給AJO。 這可讓行銷活動報表保持準確：

   ```javascript
   // When a notification is displayed in the detail view:
   collectEvent("display", [notification.proposition]);
   
   // When a user clicks or interacts with a notification:
   collectEvent("interact", [notification.proposition]);
   
   // When a user dismisses a notification without reading it:
   collectEvent("dismiss", [notification.proposition]);
   
   // When a user deletes a notification:
   collectEvent("interact", [notification.proposition]);
   collectEvent("delete",   [notification.proposition]);
   ```

1. 對於具有其他傳遞規則（例如`action = deposit-funds`）的卡片，請使用相符的`decisionContext`呼叫`evaluateRulesets`以觸發它們，因為它們不會單獨出現在`sendEvent`上：

   ```javascript
   alloy("evaluateRulesets", {
     renderDecisions: true,
     personalization: {
       decisionContext: { action: "deposit-funds" },
     },
   });
   ```

   `subscribeRulesetItems`回撥會再次執行，且任何新合格的卡片會連同現有卡片一併包含。

1. 安裝相依性並啟動範例伺服器：

   ```bash
   npm install
   npm start
   ```

1. 在瀏覽器中開啟`https://localhost`。

1. 在測試之前，更新`src/app/page.js`中的`datastreamId`、`orgId`和`SURFACE`常數，以指向您的AJO環境。

{{$include /help/_includes/do-not-localize/inbox/ai-augmented-inbox-configuration-sdk.md}}
