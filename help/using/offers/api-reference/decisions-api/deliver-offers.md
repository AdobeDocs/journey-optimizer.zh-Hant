---
title: 傳遞優惠
description: 決策管理是服務和UI計畫的集合，可讓行銷人員使用商業邏輯和決策規則，跨通道和應用程式建立和提供使用者個人化的優惠體驗。
translation-type: tm+mt
source-git-commit: b527186d0722492f5f509f1ae0a5315b9a9f771e
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 3%

---

# 使用決策API提供優惠

借助決策管理，您可以使用業務邏輯和決策規則，跨通道和應用程式建立和提供最終用戶個性化的優惠體驗。 選件是行銷訊息，其中可能包含與其關聯的規則，以指定誰有資格檢視選件。

您可以透過向[!DNL Decisions] API提出POST要求來建立和傳送選件。

本教學課程需要對API（尤其是與「決策管理」相關的API）有良好的認識。 如需詳細資訊，請參閱[決策管理API開發人員指南](../getting-started.md)。 本教學課程還要求您有唯一的位置ID和決策ID值可用。 如果您尚未取得這些值，請參閱建立位置](../offers-api/placements/create.md)和[建立決策](../activities-api/activities/create.md)的教學課程。[

![](../../../assets/do-not-localize/how-to-video.png) [在影片中探索此功能](#video)

## 接受和內容類型標題

下表顯示請求標題中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;欄位的有效值：

| 標題名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**API格式**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的端點路徑。 | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**要求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0'
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
  -d '{
        "xdm:propositionRequests": [
            {
              "xdm:placementId": "xcore:offer-placement:ffed0456",
              "xdm:activityId": "xcore:offer-activity:ffed0123",
              "xdm:itemCount": 2
            },
            {
              "xdm:placementId": "xcore:offer-placement:ffed0012",
              "xdm:activityId": "xcore:offer-activity:fffc0789"
            }
        ],
        "xdm:profiles": [
            {
              "xdm:identityMap": {
                "SWCUSTID": [
                {
                    "xdm:id": "123@abc.com"
                }
                ]
            },
            "xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"
            }
        ],
        "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
        },
        "xdm:mergePolicy": {
            "xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"
        },
        "xdm:responseFormat": {
            "xdm:includeContent": true,
            "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
            }
        }
      }'
```

| 屬性 | 說明 | 範例 |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | 此對象包含位置和決策標識符。 |
| `xdm:propositionRequests.xdm:placementId` | 唯一位置識別碼。 | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | 唯一的決策識別碼。 | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | 要傳回的選件數。 最大數目為30。 | `"xdm:itemCount": 2` |
| `xdm:profiles` | 此對象保存有關請求決策的配置檔案的資訊。 若是API要求，則會包含一個描述檔。 |
| `xdm:profiles.xdm:identityMap` | 此物件會根據身分的命名空間整合程式碼，保留一組一般使用者身分識別。 該標識映射可以承載每個命名空間的多個標識。 有關名稱空間的詳細資訊，請參閱[Identity namespace overview](https://docs.adobe.com/content/help/zh-Hant/experience-platform/identity/namespaces.html)。 | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | 由用戶端產生的ID，可用來唯一識別描述檔決策請求。 此ID會回覆在回應中，不會影響決定的結果。 | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | 此對象是重複資料消除規則的控制結構。 它由一系列標幟組成，這些標幟指出是否可以在特定維度中提出相同的選項。 設為true的標幟表示允許重複項目，且不應跨標幟所指示的類別移除。 設為false的標幟表示決策引擎不應在整個維度上提出相同的主張，而應為其中一個子決策選擇下一個最佳選項。 |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | 如果設為true，則可能會指派相同的選項給多個決策。 | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | 如果設為true，可能會指派相同的選項給多個位置。 | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | 標識用於管理配置檔案訪問服務返回資料的合併策略。 如果請求中未指定，決策管理不會傳遞任何描述檔存取服務，否則會傳遞呼叫者提供的ID。 | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | 一組標籤，用於格式化響應內容。 |
| `xdm:responseFormat.xdm:includeContent` | 布爾值，如果設定為`true`，則包括響應的內容。 | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | 用來指定要傳回哪些額外中繼資料的物件。 如果未包含此屬性，則預設情況下會返回`xdm:id`和`repo:etag`。 | `name` |
| `xdm:responseFormat.xdm:activity` | 此標幟可識別為`xdm:activity`傳回的特定中繼資料資訊。 | `name` |
| `xdm:responseFormat.xdm:option` | 此標幟可識別為`xdm:option`傳回的特定中繼資料資訊。 | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | 此標幟可識別為`xdm:placement`傳回的特定中繼資料資訊。 | `name`, `channel`, `componentType` |

**回應**

成功的回應會傳回您的提案，包括其唯一`xdm:propositionId`的資訊。

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "xcore:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "xcore:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "xcore:fallback:ccc0222",
        "repo:etag": 5,
        "@type": "https://ns.adobe.com/experience/decisioning/content-component-imagelink",
        "dc:format": "image/png",
        "xdm:deliveryURL": "https://cdn.adobe.com/content/1445323-1134331.png",
        "xdm:content": "https://www.adobe.com/index2.html"
      }
    }
  ],
  "ode:createDate": 1566497582038
}
```

| 屬性 | 說明 | 範例 |
| -------- | ----------- | ------- |
| `xdm:propositionId` | 與XDM DecisionEvent相關聯的命題實體的唯一標識符。 | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | 此對象包含單一決策命題。 可傳回多個選項供決策使用。 如果找不到任何選項，則會傳回決定的備援選件。 單一決策命題總是包含`options`屬性或`fallback`屬性。 如果存在，`options`屬性不能為空。 |
| `xdm:propositions.xdm:activity` | 此物件包含決策的唯一識別碼。 | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | 此物件包含選件位置的唯一識別碼。 | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | 此物件包含單一選項，包括其唯一識別碼。 如果存在，則此對象不能為空。 | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | 定義元件的類型。 `@type` 當做客戶的處理合約。組合體驗時，撰寫器會尋找具有特定類型的元件。 | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | 回應內容的格式。 | 回應內容可以是：`text`、`html block`或`image link` |
| `xdm:score` | 根據與選項或決策相關聯的排名函式而計算的選項的分數。 如果在排名期間有排名函式參與決定選件的分數，API會傳回此欄位。 | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | 此物件包含單一備援選件，包括其唯一識別碼。 | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | 資源的物理或數位表現。 通常，格式應包括資源的媒體類型。 該格式可用於確定顯示或操作資源所需的軟體、硬體或其它設備。 建議從受控辭彙中選擇一個值，例如[定義電腦媒體格式的](http://www.iana.org/assignments/media-types/)網際網路媒體類型清單。 | `"dc:format": "image/png"` 或 `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | 從內容傳送網路或服務端點讀取資產的選用URL。 此URL用於從使用者代理公開存取資產。 | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | 建立決策響應消息的時間。 這是劃時代的。 | `"ode:createDate": 1566497582038` |

## 教學課程影片{#video}

以下視頻旨在支援您對「決策管理」元件的瞭解。

>[!NOTE]
>
>此視訊適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 然而，它提供了在Journey Optimizer背景下使用選件的一般指導。

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## 後續步驟

依照本API指南，您已使用[!DNL Decisions] API建立並傳送選件。 如需詳細資訊，請參閱[決策管理概觀](../../../offers/get-started/starting-offer-decisioning.md)。
