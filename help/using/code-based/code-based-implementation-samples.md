---
title: 程式碼型實施範例
description: 本頁顯示Journey Optimizer程式碼型功能實作方法的範例
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 3%

---

# 程式碼型實作方法範例 {#implementation-samples}

程式碼型體驗支援任何型別的客戶實施。 您可以在此頁面找到每種實作方法的範例：

* [用戶端](#client-side-implementation)
* [伺服器端](#server-side-implementation)
* [混合式](#hybrid-implementation)

>[!IMPORTANT]
>
>追隨 [此連結](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} 以尋找不同個人化和實驗使用案例的實作範例。 請檢視並執行這些報表，以更加瞭解所需的實作步驟，以及端對端個人化流程的運作方式。

## 使用者端實施 {#client-side-implementation}

如果您是使用者端實作，則可以使用其中一個AEP使用者端SDK：AEP Web SDK或AEP Mobile SDK。 以下步驟說明在範例Web SDK實作中，透過程式碼型體驗行銷活動擷取Edge上發佈的內容並顯示個人化內容的程式。

### 運作方式

1. [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant){target="_blank"} 會包含在頁面上。

1. 您需要使用 `sendEvent` 命令並指定表面URI，以擷取個人化內容。

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. 實作程式碼應手動套用程式碼型體驗專案(使用 [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"} 方法)，以根據決定更新DOM。

1. 對於程式碼型體驗行銷活動，必須手動傳送顯示事件以指出內容已顯示時間。 這可透過以下方式完成 `sendEvent` 命令。

```javascript
function sendDisplayEvent(decision) {
  const { id, scope, scopeDetails = {} } = decision;

  alloy("sendEvent", {

    xdm: {
      eventType: "decisioning.propositionDisplay",
      _experience: {
        decisioning: {
          propositions: [
            {
              id: id,
              scope: scope,
              scopeDetails: scopeDetails,
            },
          ],
        },
      },
    },
  });
}
```

1. 對於程式碼型體驗行銷活動，必須手動傳送互動事件，以指出使用者何時已與內容互動。 這可透過以下方式完成 `sendEvent` 命令。

```javascript
function sendInteractEvent(label, proposition) {
  const { id, scope, scopeDetails = {} } = proposition;

  alloy("sendEvent", {
    
    xdm: {
      eventType: "decisioning.propositionInteract",
      _experience: {
        decisioning: {
          propositions: [
            {
              id: id,
              scope: scope,
              scopeDetails: scopeDetails,
            },
          ],
          propositionEventType: {
            interact: 1
          },
          propositionAction: {
            label: label
          },
        },
      },
    },
  });
}
```

### 重要觀察

**Cookie**

Cookie可用來儲存使用者身分和叢集資訊。 使用使用者端實作時，Web SDK會在請求生命週期期間自動處理這些Cookie的儲存和傳送。

| Cookie | 用途 | 儲存者 | 傳送者 |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | 包含使用者身分詳細資訊 | Web SDK | Web SDK |
| kndctr_AdobeOrg_cluster | 指出應使用哪個體驗邊緣叢集來履行請求 | Web SDK | Web SDK |

**請求刊登**

需要向Adobe Experience Platform API提出請求才能取得主張並傳送顯示通知。 使用使用者端實作時，Web SDK會在使用者介面 `sendEvent` 命令時才會使用。

| 請求 | 製作者 |
| ---------------------------------------------- | ----------------------------------- |
| 互動要求以取得主張 | 使用sendEvent命令的Web SDK |
| interact傳送顯示通知的請求 | 使用sendEvent命令的Web SDK |

**流程圖**

![](assets/code-based-client-side-implementation.png)

## 伺服器端實作 {#server-side-implementation}

如果您有伺服器端實作，則可以使用其中一個AEP Edge Network API。 下列步驟說明在範例網頁的Edge Network API實作中，擷取程式碼型體驗促銷活動在Edge上發佈之內容的程式，並顯示個人化內容。

### 運作方式

1. 系統會要求網頁，以及瀏覽器先前儲存的所有Cookie （前置詞為） `kndctr_` 中包含。
1. 當從應用程式伺服器要求頁面時，會將事件傳送至 [互動式資料收集端點](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html) 以擷取個人化內容。 此範例應用程式使用一些協助程式方法來簡化建立及傳送請求至API的程式(請參閱 [aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"})。 但要求只是 `POST` 裝載中包含事件和查詢。 先前步驟的Cookie （如果可用）會包含在中的請求中 `meta>state>entries` 陣列。

   ```javascript
   fetch(
     "https://edge.adobedc.net/ee/v2/interact?dataStreamId=abc&requestId=123",
     {
       headers: {
         accept: "*/*",
         "accept-language": "en-US,en;q=0.9",
         "cache-control": "no-cache",
         "content-type": "text/plain; charset=UTF-8",
         pragma: "no-cache",
         "sec-fetch-dest": "empty",
         "sec-fetch-mode": "cors",
         "sec-fetch-site": "cross-site",
         "sec-gpc": "1",
         "Referrer-Policy": "strict-origin-when-cross-origin",
         Referer: "https://localhost/",
       },
       body: JSON.stringify({
         event: {
           xdm: {
             eventType: "decisioning.propositionFetch",
             web: {
               webPageDetails: {
                 URL: "https://localhost/",
               },
               webReferrer: {
                 URL: "",
               },
             },
             identityMap: {
               FPID: [
                 {
                   id: "xyz",
                   authenticatedState: "ambiguous",
                   primary: true,
                 },
               ],
             },
             timestamp: "2022-06-23T22:21:00.878Z",
           },
           data: {},
         },
         query: {
           identity: {
             fetch: ["ECID"],
           },
           personalization: {
             schemas: [
               "https://ns.adobe.com/personalization/default-content-item",
               "https://ns.adobe.com/personalization/html-content-item",
               "https://ns.adobe.com/personalization/json-content-item",
               "https://ns.adobe.com/personalization/redirect-item",
               "https://ns.adobe.com/personalization/dom-action",
             ],
             surfaces: ["web://localhost/","web://localhost/#sample-json-content"],
           },
         },
         meta: {
           state: {
             domain: "localhost",
             cookiesEnabled: true,
             entries: [
               {
                 key: "kndctr_XXX_AdobeOrg_identity",
                 value: "abc123",
               },
               {
                 key: "kndctr_XXX_AdobeOrg_cluster",
                 value: "or2",
               },
             ],
           },
         },
       }),
       method: "POST",
     }
   ).then((res) => res.json());
   ```

1. 會從回應中讀取程式碼型體驗促銷活動中的JSON體驗，並在產生HTML回應時使用。
1. 對於程式碼型體驗行銷活動，必須在實施中手動傳送顯示事件，以指出行銷活動內容已顯示的時間。 在此範例中，通知會在請求生命週期期間在伺服器端傳送。

   ```javascript
   function sendDisplayEvent(aepEdgeClient, req, propositions, cookieEntries) {
     const address = getAddress(req);
   
     aepEdgeClient.interact(
       {
         event: {
           xdm: {
             web: {
               webPageDetails: { URL: address },
               webReferrer: { URL: "" },
             },
             timestamp: new Date().toISOString(),
             eventType: "decisioning.propositionDisplay",
             _experience: {
               decisioning: {
                 propositions: propositions.map((proposition) => {
                   const { id, scope, scopeDetails } = proposition;
   
                   return {
                     id,
                     scope,
                     scopeDetails,
                   };
                 }),
               },
             },
           },
         },
         query: { identity: { fetch: ["ECID"] } },
         meta: {
           state: {
             domain: "",
             cookiesEnabled: true,
             entries: [...cookieEntries],
           },
         },
       },
       {
         Referer: address,
       }
     );
   }
   ```

1. 傳回HTML回應時，應用程式伺服器會在回應上設定身分和叢集Cookie。

### 重要觀察

**Cookie**

Cookie可用來儲存使用者身分和叢集資訊。 使用伺服器端實作時，應用程式伺服器必須在請求生命週期期間處理這些Cookie的儲存和傳送。

| Cookie | 用途 | 儲存者 | 傳送者 |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | 包含使用者身分詳細資訊 | 應用程式伺服器 | 應用程式伺服器 |
| kndctr_AdobeOrg_cluster | 指出應使用哪個體驗邊緣叢集來履行請求 | 應用程式伺服器 | 應用程式伺服器 |

**請求刊登**

需要向Adobe Experience Platform API提出請求才能取得主張並傳送顯示通知。 使用使用者端實作時，Web SDK會在使用者介面 `sendEvent` 命令時才會使用。

| 請求 | 製作者 |
| ---------------------------------------------- | ------------------------------------------------------------ |
| 互動要求以取得主張 | 應用程式伺服器呼叫Adobe Experience Platform API |
| interact傳送顯示通知的請求 | 應用程式伺服器呼叫Adobe Experience Platform API |

**流程圖**

![](assets/code-based-server-side-implementation.png)

## 混合實施 {#hybrid-implementation}

如果您採用混合式實作，請參閱下列連結。

* Adobe技術部落格： [Adobe Experience Platform Web SDK中的混合個人化](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* SDK檔案： [使用Web SDK和Edge Network Server API的混合個人化](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html){target="_blank"}
