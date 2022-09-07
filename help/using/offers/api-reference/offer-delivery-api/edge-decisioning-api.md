---
title: 使用Edge Decisioning API提供優惠方案
description: Adobe Experience Platform Web SDK可讓您使用API或選件資料庫建立的擷取及呈現個人化選件。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 2%

---

# 使用Edge Decisioning API提供優惠方案 {#edge-decisioning-api}

## 快速入門與必要條件 {#edge-overview-and-prerequisites}

此 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) 是用戶端JavaScript程式庫，可讓Adobe Experience Cloud客戶透過Experience Platform邊緣網路與Experience Cloud中的各種服務互動。

Experience PlatformWeb SDK支援在Adobe（包括決策管理）查詢個人化解決方案，讓您能夠擷取及呈現您使用API或選件資料庫建立的個人化選件。 如需更多詳細指示，請參閱 [建立優惠方案](../../get-started/starting-offer-decisioning.md).

有兩種方式可透過 [平台Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). 一種是面向開發人員，需要了解網站和程式設計。 另一種方式是使用Adobe Experience Platform使用者介面來設定選件，該選件只需要在HTML頁面的標題中參考小型指令碼。

請參閱 [決策管理](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) 如需如何使用Platform Web SDK提供個人化優惠方案的詳細資訊。

>[!NOTE]
>
>Adobe Experience Platform Web SDK中的「決策管理」僅適用於一組組織（有限可用性）。 如果您想要運用此功能，請連絡您的Adobe客戶主管。

## Adobe Experience Platform Web SDK {#aep-web-sdk}

Platform Web SDK取代了下列SDK:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

SDK並未結合這些程式庫，而是從頭開始的新實作。 若要使用，您必須先依照下列步驟操作：

1. 請確定貴組織擁有使用SDK的適當權限，且您已正確設定權限。

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [設定您的資料流](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) 在Adobe Experience Cloud中您帳戶的「資料收集」標籤中。

1. 安裝SDK。 執行此作業有多種方法，相關說明請參閱 [安裝SDK頁面](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). 本頁面會繼續提供各種不同的實施方法。

若要使用SDK，您必須有 [綱要](../../../start/get-started-schemas.md) 和 [資料流](../../../start/get-started-datasets.md) 已定義。

<!-- ****TODO - Configure schema**** -->

若要個人化優惠方案，您必須個別設定您的個人化/設定檔。

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

若要設定SDK以進行決策管理，請遵循下列兩個步驟之一：

## 選項1 — 使用Launch安裝Tag擴充功能與實作

對於編碼體驗可能較少的人，此選項較方便使用。

1. [建立標籤屬性](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [新增內嵌程式碼](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. 從「Datastream」下拉式清單中選取設定，使用您建立的Datastream安裝並設定Platform Web SDK擴充功能。 請參閱 [擴充功能](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![Adobe Experience Platform Web SDK](../../assets/installed-catalog-web-sdk.png)

   ![設定擴充功能](../../assets/configure-sdk-extension.png)

1. 建立必要 [資料元素](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en). 您至少必須建立Platform Web SDK身分對應和Platform Web SDK XDM物件資料元素。

   ![身分對應](../../assets/sdk-identity-map.png)

   ![XDM 物件](../../assets/xdm-object.png)

1. 建立 [規則](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   新增Platform Web SDK傳送事件動作，並將相關decisionScopes新增至該動作的設定

   ![轉譯選件](../../assets/rule-render-offer.png)

   ![要求選件](../../assets/rule-request-offer.png)

1. [建立和發佈](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) 包含您已設定之所有相關規則、資料元素和擴充功能的程式庫。

## 選項2 — 使用預先建立的獨立版本手動實作

以下是使用預先建置的Web SDK獨立安裝來進行決策管理所需的步驟。 本指南假設這是您首次實作SDK，因此所有步驟可能皆不適用。 本指南也假設有一些開發經驗。

從選項2加入下列JavaScript程式碼片段：上預先建置的獨立版本 [本頁](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) 在 `<head>` HTML頁面的區段。

```
javascript
    <script>
        !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
        []).push(o),n[o]=function(){var u=arguments;return new Promise(
        function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
        (window,["alloy"]);
    </script>
    <script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.js" async></script>
```

您需要Adobe帳戶內的兩個ID來設定SDK設定：您的edgeConfigId和您的orgId。 edgeConfigId與您的資料流ID相同，您應在「必要條件」中設定。

若要尋找您的edgeConfigID/datastream ID，請前往「資料收集」並選取您的「資料流」。 若要尋找您的orgId，請前往您的個人資料。

依照本頁的指示，在JavaScript中配置SDK。 您一律會在設定函式中使用edgeConfigId和orgId。 本檔案也說明您的設定有哪些選用參數。 您的最終設定可能會如下所示：

```
javascript
    alloy("configure", {
        "edgeConfigId": "12345678-0ABC-DEF-GHIJ-KLMNOPQRSTUV",                            
        "orgId":"ABCDEFGHIJKLMNOPQRSTUVW@AdobeOrg",
        "debugEnabled": true,
        "edgeDomain": "edge.adobedc.net",
        "clickCollectionEnabled": true,
        "idMigrationEnabled": true,
        "thirdPartyCookiesEnabled": true,
        "defaultConsent":"in"  
    });
```

安裝Debugger Chrome擴充功能以用於除錯。 您可在以下位置找到： <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

接下來，在偵錯工具中登入您的帳戶。 接著，前往「記錄檔」，確認您已連線至正確的工作區。 現在，從選件中複製決策範圍的base64編碼版本。

編輯網站時，請加入指令碼及設定，並 `sendEvent` 函式，將決策範圍傳送至Adobe。

**範例**:

```
javascript
    alloy("sendEvent", {
        "decisionScopes": 
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    });
```

如需如何處理回應的範例，請參閱下列內容：

```
javascript
    alloy("sendEvent", {
        "decisionScopes":
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    }).then(function(result) {
        Object.entries(result).forEach(([key, value]) => {
            console.log(key, value);
        });
    });
```

您可以使用偵錯工具來確認您已成功連線至邊緣網路。

>[!NOTE]
>
>如果您在記錄中看不到與邊緣的連線，則可能需要停用廣告封鎖程式。

請參閱建立選件的方式，以及使用的格式。 系統會根據決策中符合的條件，傳回選件給您，其中包含您在Adobe Experience Platform中建立選件時指定的資訊。

在此範例中，要傳回的JSON為：

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

處理回應物件並剖析您需要的資料。 因為您可以一次發送多個決策範圍 `sendEvent` 呼叫，您的回應看起來可能會稍有不同。

```
json
    {
        "id": "abrxgl843d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"ABC Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
]
}
```

```
json
{
    "propositions": 
    [
    {
        "renderAttempted": false,
        "id": "e15ecb09-993e-4b66-93d8-0a4c77e3d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"Claire Hubacek Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
    ]
}
```

在此範例中，處理和使用網頁中選件特定詳細資料所需的路徑為： `result['decisions'][0]['items'][0]['data']['content']`

若要設定JS變數：

```
javascript
const offer = JSON.parse(result['decisions'][0]['items'][0]['data']['content']);

let offerURL = offer['link'];
let offerDescription = offer['description'];
let offerImageURL = offer['image'];

document.getElementById("offerDescription").innerHTML = offerDescription;
document.getElementById('offerImage').src = offerImageURL;
```

## 限制

行動體驗邊緣工作流程目前不支援某些選件限制，例如限定上限。 「限定」欄位值會指定可向所有使用者呈現選件的次數。 如需詳細資訊，請參閱 [新增限制至選件](../../offer-library/add-constraints.md#capping).
