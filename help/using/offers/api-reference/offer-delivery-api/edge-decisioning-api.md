---
title: 使用邊緣決策API提供服務
description: Adobe Experience PlatformWeb SDK允許您檢索和呈現您使用API或服務庫建立的個性化服務。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: d18a0cb38bf5a3014a87f1dc5f1c3a3c21982b09
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 2%

---


# 使用邊緣決策API提供服務 {#edge-decisioning-api}

## 入門和先決條件 {#edge-overview-and-prerequisites}

的 [Adobe Experience PlatformWeb SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) 是客戶端JavaScript庫，它允許Adobe Experience Cloud客戶通過Experience Platform邊緣網路與Experience Cloud中的各種服務進行交互。

Experience PlatformWeb SDK支援在Adobe查詢個性化解決方案，包括決策管理，允許您檢索和呈現您使用API或服務庫建立的個性化服務。 有關更詳細的說明，請參閱 [建立聘用](../../get-started/starting-offer-decisioning.md)。

有兩種方法可與 [平台Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview)。 一種方法是面向開發者，需要瞭解網站和寫程式。 另一種方法是使用Adobe Experience Platform用戶介面來設定提供，它只需在HTML頁的標題中引用一個小指令碼即可。

請參閱上 [offer decisioning](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) 有關如何使用平台Web SDK提供個性化服務的詳細資訊。

>[!NOTE]
>
>Adobe Experience PlatformWeb SDK中的決策管理目前可以提前訪問選定用戶。 此功能並非所有IMS組織都可用。

## Adobe Experience Platform Web SDK {#aep-web-sdk}

平台Web SDK取代了以下SDK:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

SDK沒有將這些庫合併，而是從頭開始的新實現。 要使用它，必須首先執行以下步驟：

1. 確保您的組織具有使用SDK的適當權限，並且您已正確配置了權限。

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [配置資料流](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) 在您在Adobe Experience Cloud的帳戶中的「資料收集」頁籤中。

1. 安裝SDK。 有多種方法可以執行此操作， [安裝SDK頁](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en)。 本頁將繼續介紹每種不同的實現方法。

要使用SDK，必須有 [架構](../../../start/get-started-schemas.md) 和 [資料流](../../../start/get-started-datasets.md) 定義。

<!-- ****TODO - Configure schema**** -->

要個性化服務，必須單獨配置個性化/配置檔案。

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

要配置SDK進行Offer decisioning，請執行以下兩步之一：

## 選項1 — 使用啟動安裝標籤擴展和實施

對於編碼體驗可能較少的人，此選項更方便用戶。

1. [建立標籤屬性](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [添加嵌入代碼](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. 從「Datastream」下拉清單中選擇配置，使用您建立的Datastream安裝和配置平台Web SDK擴展。 請參閱 [擴展](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en)。

   ![Adobe Experience Platform Web SDK](../../assets/installed-catalog-web-sdk.png)

   ![配置擴展](../../assets/configure-sdk-extension.png)

1. 建立必要 [資料元素](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en)。 至少，必須建立平台Web SDK標識映射和平台Web SDK XDM對象資料元素。

   ![身分對應](../../assets/sdk-identity-map.png)

   ![XDM 物件](../../assets/xdm-object.png)

1. 建立 [規則](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   添加平台Web SDK發送事件操作，並將相關decisionScope添加到該操作的配置中

   ![呈現優惠](../../assets/rule-render-offer.png)

   ![請求優惠](../../assets/rule-request-offer.png)

1. [建立和發佈](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) 包含您配置的所有相關規則、資料元素和擴展的庫。

## 選項2 — 使用預構建的獨立版本手動實施

以下是使用預構建的Web SDK獨立安裝使用Offer decisioning所需的步驟。 本指南假定這是您首次實施SDK，因此所有步驟可能都不適用於您。 本指南還假定了一些發展經驗。

在選項2中包括以下JavaScript代碼段：上預構建的獨立版本 [此頁](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) 的 `<head>` 的子菜單。

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

您需要Adobe帳戶內的兩個ID來設定SDK配置 — edgeConfigId和orgId。 edgeConfigId與Datastream ID相同，您應在先決條件中配置該ID。

要查找edgeConfigID/datastream ID，請轉到「資料收集」並選擇「資料流」。 要查找組織ID，請轉到您的個人資料。

按照本頁上的說明在JavaScript中配置SDK。 您將始終在配置函式中使用edgeConfigId和orgId。 文檔還介紹了配置中存在哪些可選參數。 您的最終配置可能會是這樣的：

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

安裝調試程式Chrome擴展以用於調試。 可在以下位置找到： <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

接下來，在調試器中登錄帳戶。 然後，轉到「日誌」(Logs)，確保已連接到正確的工作區。 現在，從您的優惠中複製base64編碼的決策範圍版本。

編輯網站時，請包括包含配置和 `sendEvent` 函式將決策範圍發送到Adobe。

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

有關如何處理響應的示例，請參見以下內容：

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

您可以使用調試器驗證是否已成功連接到邊緣網路。

>[!NOTE]
>
>如果未在日誌中看到與邊緣的連接，則可能需要禁用廣告攔截程式。

請參閱您如何建立優惠和使用的格式。 根據決策中滿足的條件，將向您返回一份要約，其中包含您在Adobe Experience Platform內建立要約時指定的資訊。

在此示例中，要返回的JSON為：

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

處理響應對象並分析所需資料。 因為您可以在一個 `sendEvent` 電話，你的反應可能有點不同。

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

在此示例中，處理和使用網頁中特定於服務的詳細資訊所需的路徑是： `result['decisions'][0]['items'][0]['data']['content']`

設定JS變數：

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

移動體驗邊緣工作流當前不支援某些服務約束，例如封頂。 「上限設定」欄位值指定可在所有用戶間顯示優惠的次數。 有關詳細資訊，請參閱 [向優惠添加約束](../../offer-library/add-constraints.md#capping)。
