---
title: 提供優惠
description: 決策管理是服務和用戶介面程式的集合，使營銷人員能夠使用業務邏輯和決策規則跨渠道和應用程式建立和提供最終用戶個性化的服務體驗。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
source-git-commit: 2088b5ba2ec77e56644683e118e734acfe6707fc
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 2%

---

# 使用決策API提供服務 {#deliver-offers-using-decisions-api}

使用決策管理，您可以使用業務邏輯和決策規則跨渠道和應用程式建立和提供最終用戶個性化的服務體驗。 聘用是一條市場營銷消息，可能具有與其關聯的規則，指定誰有資格查看聘用。

您可以通過向Oracle Server發出POST請求來建立和交付優惠 [!DNL Decisions] API。

本教程要求對API（特別是與決策管理相關的API）進行有效的理解。 有關詳細資訊，請參見 [決策管理API開發人員指南](../getting-started.md)。 本教程還要求您具有唯一的放置ID和決策ID值。 如果尚未獲取這些值，請參閱 [建立放置](../offers-api/placements/create.md) 和 [建立決策](../activities-api/activities/create.md)。

➡️  [在影片中探索此功能](#video)

## 接受和內容類型標題 {#accept-and-content-type-headers}

下表顯示了組成 *內容類型* 和 *接受* 請求標題中的欄位：

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
| `{ENDPOINT_PATH}` | 儲存庫API的終結點路徑。 | `https://platform.adobe.io/data/core/ode/` |
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
| `xdm:propositionRequests` | 此對象包含放置和決策標識符。 |
| `xdm:propositionRequests.xdm:placementId` | 唯一的放置標識符。 | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | 唯一決策標識符。 | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | 要返回的優惠數量。 最大數為30。 | `"xdm:itemCount": 2` |
| `xdm:profiles` | 此對象包含有關請求決策的配置檔案的資訊。 對於API請求，此請求將包含一個配置檔案。 |
| `xdm:profiles.xdm:identityMap` | 此對象基於標識的命名空間整合代碼保存一組最終用戶標識。 標識映射可以攜帶每個命名空間的多個標識。 有關命名空間的詳細資訊，請參見 [此頁](../../../start/get-started-identity.md)。 | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | 客戶端生成的ID，可用於唯一標識配置檔案決策請求。 此ID在響應中回復，不影響決定的結果。 | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | 此對象是重複資料消除規則的控制結構。 它由一系列標誌組成，這些標誌指示是否可以在某個維上建議同一選項。 設定為true的標誌表示允許重複，並且不應跨標誌所指示的類別刪除。 設定為false的標誌表示決策引擎不應在整個維中提出相同的命題，而應為子決策之一選擇下一個最佳選項。 |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | 如果設定為true，則可能會為多個決策分配相同的選項。 | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | 如果設定為true，則可能會為多個放置分配相同的選項。 | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | 標識用於管理配置檔案訪問服務返回的資料的合併策略。 如果未在請求中指定，則Decision Management將不會傳遞任何配置檔案訪問服務，否則它將傳遞調用方提供的ID。 | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | 一組標誌，用於格式化響應內容。 |
| `xdm:responseFormat.xdm:includeContent` | 布爾值，如果設定為 `true`，包括響應的內容。 | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | 用於指定返回哪些附加元資料的對象。 如果此屬性未包括，則 `xdm:id` 和 `repo:etag` 預設情況下返回。 | `name` |
| `xdm:responseFormat.xdm:activity` | 此標誌標識為返回的特定元資料資訊 `xdm:activity`。 | `name` |
| `xdm:responseFormat.xdm:option` | 此標誌標識為返回的特定元資料資訊 `xdm:option`。 | `name`、`characteristics` |
| `xdm:responseFormat.xdm:placement` | 此標誌標識為返回的特定元資料資訊 `xdm:placement`。 | `name`、`channel`、`componentType` |

**回應**

成功的響應將返回有關您的建議的資訊，包括其獨特性 `xdm:propositionId`。

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
| `xdm:propositionId` | 與XDM DecisionEvent關聯的命題實體的唯一標識符。 | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | 此對象包含單一的決策命題。 可以返回多個選項以用於決策。 如果找不到任何選項，則返回該決定的回退要約。 單個決策主張始終包括 `options` 屬性或 `fallback` 屬性。 當出現時， `options` 屬性不能為空。 |
| `xdm:propositions.xdm:activity` | 此對象包含決策的唯一標識符。 | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | 此對象包含聘用位置的唯一標識符。 | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | 此對象包含一個選項，包括其唯一標識符。 如果存在，則此對象不能為空。 | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | 定義元件的類型。 `@type` 充當客戶端的處理合同。 在組合體驗時，作曲家將查找具有特定類型的元件。 | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | 響應內容的格式。 | 響應內容可以是： `text`。 `html block`或 `image link` |
| `xdm:score` | 作為與選項或決策關聯的排名函式的結果計算的選項的得分。 如果在評級期間確定優惠的得分時涉及評級函式，則API將返回此欄位。 | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | 此對象包含單個回退優惠，包括其唯一標識符。 | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | 資源的物理或數字表示。 通常，格式應包括資源的媒體類型。 該格式可用於確定顯示或操作資源所需的軟體、硬體或其它設備。 建議從受控辭彙(例如， [Internet媒體類型](http://www.iana.org/assignments/media-types/) 定義電腦媒體格式。 | `"dc:format": "image/png"` 或 `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | 用於從內容傳遞網路或服務終結點讀取資產的可選URL。 此URL用於從用戶代理公開訪問資產。 | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | 建立決策響應消息的時間。 這被表示為劃時代。 | `"ode:createDate": 1566497582038` |

## 教程視頻 {#video}

以下視頻旨在支援您對「決策管理」元件的瞭解。

>[!NOTE]
>
>此視頻適用於在Adobe Experience Platform上構建的Offer decisioning應用程式服務。 然而，它為在Journey Optimizer背景下使用要約提供了一般性指導。

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## 後續步驟 {#next-steps}

按照本API指南，您已使用 [!DNL Decisions] API。 有關詳細資訊，請參見 [決策管理概述](../../../offers/get-started/starting-offer-decisioning.md)。
