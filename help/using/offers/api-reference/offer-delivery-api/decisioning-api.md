---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 傳遞優惠方案
description: 決定管理是服務和UI程式的集合，可讓行銷人員使用商業邏輯和決定規則，跨頻道和應用程式建立和提供一般使用者個人化優惠體驗。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 2%

---

# 使用Decisioning API傳遞優惠方案 {#decisioning-api}

使用決定管理，您可以使用商業邏輯和決定規則，跨頻道和應用程式建立並提供使用者個人化的優惠體驗。 優惠方案是行銷訊息，其中可能包含與其關聯的規則，以指定誰有資格檢視優惠方案。

您可以對[!DNL Decisioning] API發出POST要求，以建立並傳遞優惠方案。

本教學課程需要實際瞭解API，特別是有關決定管理。 如需詳細資訊，請參閱[決定管理API開發人員指南](../getting-started.md)。 本教學課程還要求您有唯一的位置ID和決定ID值可用。 如果您尚未取得這些值，請參閱[建立位置](../offers-api/placements/create.md)和[建立決定](../activities-api/activities/create.md)的教學課程。

## 必要的標頭 {#required-headers}

下表顯示請求標頭中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;欄位的有效值：

| 標題名稱 | 價值 |
| ----------- | ----- |
| 接受 | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |
| Authorization | `Bearer {ACCESS_TOKEN}` |
| x-gw-ims-org-id | `{IMS_ORG}` |
| x-sandbox-name | `{SANDBOX_NAME}` |
| x-api-key | `{API_KEY}` |

* 包含裝載(POST、PUT、PATCH)的所有請求都需要內容型別標頭


>[!NOTE]
>
>不會針對個別沙箱強制執行許可權檢查。 只要呼叫者提供有效的Token，傳送API就會通過。

## API要求 {#request}

### API格式

```https
POST /{ENDPOINT_PATH}/decisions
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/ods` |

### 請求

```shell
curl -X POST 'https://platform.adobe.io/data/core/ods/decisions' \
-H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
-H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}....' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'x-request-id: e9ac8d7e-3e77-4b38-8726-555ef1737b32-example' \
-d '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:15ded04b1786ea27",
            "xdm:placementId": "dps:offer-placement:15d9bc01d35e1238"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "example@adobe.com",
                        "primary": true
                    }
                ]
            }
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
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
| `xdm:propositionRequests` | 此物件包含位置與決定識別碼。 |  |
| `xdm:propositionRequests.xdm:placementId` | 唯一位置識別碼。 | `"xdm:placementId": "dps:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | 唯一決定識別碼。 | `"xdm:activityId": "dps:offer-activity:ffed0123"` |
| `xdm:itemCount` | 要傳回的優惠方案數量。 最大數目為30。 | `"xdm:itemCount": 2` |
| `xdm:profiles` | 此物件包含請求決策的設定檔的相關資訊。 針對API請求，這將包含一個設定檔。 |  |
| `xdm:profiles.xdm:identityMap` | 此物件會根據身分的名稱空間整合程式碼，保留一組一般使用者身分。 身分對應可攜帶每個名稱空間一個以上的身分。 如需名稱空間的詳細資訊，請參閱[此頁面](../../../audience/get-started-identity.md)。 | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | 使用者端產生的ID，可用來唯一識別設定檔決定請求。 此ID會回應回饋，不會影響決策的結果。 | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | 此物件是去重複化規則的控制項結構。 它包含一系列標幟，標幟指出是否可以在特定維度中建議相同的選項。 若標幟設為true，表示允許重複專案，且標幟指示的類別中不應移除重複專案。 設為false的標幟表示決定引擎不應跨維度提出相同主張，而是為其中一個子決定挑選下一個最佳選項。 |  |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | 若設為true，系統可能會將相同選項指派給多個決策。 | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | 若設為true，系統可能會將相同選項指派給多個版位。 | `"xdm:acrossPlacements": true` |
| `xdm:enrichedAudience` | 如果您正在定位CSV對象，請新增此引數並將其設為「true」 | `"xdm:enrichedAudience": true` |
| `xdm:mergePolicy.xdm:id` | 識別用來控管設定檔存取服務傳回資料的合併原則。 如果未在請求中指定，決策管理將不會傳遞任何設定檔存取服務，否則將會傳遞呼叫者提供的ID。 | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | 設定回應內容格式的一組標幟。 |  |
| `xdm:responseFormat.xdm:includeContent` | 布林值，如果設為`true`，會包含回應的內容。 | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | 用來指定傳回其他中繼資料的物件。 如果未包含此屬性，則預設會傳回`xdm:id`和`repo:etag`。 | `name` |
| `xdm:responseFormat.xdm:activity` | 此旗標會識別`xdm:activity`傳回的特定中繼資料資訊。 | `name` |
| `xdm:responseFormat.xdm:option` | 此旗標會識別`xdm:option`傳回的特定中繼資料資訊。 | `name`、`characteristics` |
| `xdm:responseFormat.xdm:placement` | 此旗標會識別`xdm:placement`傳回的特定中繼資料資訊。 | `name`、`channel`、`componentType` |

### 回應

成功的回應會傳回您主張的資訊，包括其唯一的`xdm:propositionId`。

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "dps:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "dps:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "dps:fallback:ccc0222",
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
| `xdm:propositionId` | 與XDM DecisionEvent相關聯之主張實體的唯一識別碼。 | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | 此物件包含單一決定主張。 可針對決定傳回多個選項。 如果找不到選項，則會傳回決定的遞補優惠。 單一決定主張一律包含`options`屬性或`fallback`屬性。 當出現時，`options`屬性不能是空的。 |  |
| `xdm:propositions.xdm:activity` | 此物件包含決定的唯一識別碼。 | `"xdm:id": "dps:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | 此物件包含優惠方案位置的唯一識別碼。 | `"xdm:id": "dps:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | 此物件包含單一選項，包括其唯一識別碼。 如果存在，此物件不得為空白。 | `xdm:id": "dps:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | 定義元件的型別。 `@type`充當使用者端的處理合約。 組裝體驗時，撰寫器會尋找具有特定型別的元件。 | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | 回應內容的格式。 | 回應內容可以是： `text`、`html block`或`image link` |
| `xdm:score` | 選項的得分，計算方式為與選項或決定相關聯的排名函式。 如果排名功能涉及在排名期間決定優惠方案的分數，API會傳回此欄位。 | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | 此物件包含單一遞補優惠，包括其唯一識別碼。 | `"xdm:id": "dps:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | 資源的實體或數位表現形式。 通常，格式應包括資源的媒體型別。 格式可用於決定顯示或操作資源所需的軟體、硬體或其他裝置。 建議從受控制的辭彙中選取值，例如，定義電腦媒體格式的[網際網路媒體型別](https://www.iana.org/assignments/media-types/)清單。 | `"dc:format": "image/png"`或`"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | 用於從內容傳遞網路或服務端點讀取資產的選用URL。 此URL可用來從使用者代理程式公開存取資產。 | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | 決定回應訊息的建立時間。 以紀元時間表示。 | `"ode:createDate": 1566497582038` |

**回應代碼**

下表列出回應中可傳回的所有程式碼：

| 程式碼 | 說明 |
|  ---  |  ---  |
| 200 | 成功。 已針對特定活動做出決定 |
| 400 | 無效的請求引數。 由於語法錯誤，伺服器無法理解該請求。 |
| 403 | 已禁止，許可權不足。 |
| 422 | 無法處理的實體。 要求語法正確，但由於語意錯誤而無法處理。 |
| 429 | 太多請求。 使用者在指定時間內已傳送過多請求。 |
| 500 | 內部伺服器錯誤。 伺服器發生非預期的情況，導致它無法完成要求。 |
| 503 | 由於伺服器超載，服務無法使用。 伺服器目前無法處理要求，因為暫時超載。 |

<!-- ## Tutorial video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12) -->

## 後續步驟 {#next-steps}

依照此API指南，您已使用[!DNL Decisions] API建立和傳遞優惠方案。 如需詳細資訊，請參閱決策管理[的](../../../offers/get-started/starting-offer-decisioning.md)概觀。
