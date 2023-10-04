---
title: 列出個人化優惠
description: 個人化優惠是根據適用性規則和限制的可自訂行銷訊息。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 45d51918-1106-4b6b-b383-8ab4d9a4f7af
source-git-commit: f5372ee271851ffb5aa1f5ff281282c8c474dc2a
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 7%

---


# 列出個人化優惠 {#list-personalized-offers}

個人化優惠是根據適用性規則和限制的可自訂行銷訊息。

您可以透過對以下執行單一GET請求，檢視所有個人化優惠的清單： [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/offers?offer-type=personalized&{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 篩選結果的選用查詢引數。 | `limit=2` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers?offer-type=personalized&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## 使用查詢引數 {#using-query-parameters}

您可以在列出資源時，使用查詢引數來頁面和篩選結果。

### 分頁 {#paging}

分頁最常見的查詢引數包括：

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `property` | 選用的屬性篩選器： <ul><li>屬性會依AND作業分組。</li><li>引數可以重複執行，如下所示：property={PROPERTY_EXPR}[屬性(&amp;P)={PROPERTY_EXPR2}...] 或屬性={PROPERTY_EXPR1}[，{PROPERTY_EXPR2}...]</li><li>屬性運算式的格式為 `[!]field[op]value`，使用 `op` 在 `[==,!=,<=,>=,<,>,~]`，支援規則運算式。</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 依特定屬性排序結果。 在名稱前新增 — (orderby=-name)將會以降序順序(Z-A)依名稱排序專案。 路徑運算式採用點分隔路徑的形式。 此引數可重複執行，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 限制傳回的版位數。 | `limit=5` |

**回應**

成功的回應會傳回現有的個人化優惠方案清單，以及您有權存取的優惠方案。

```json
{
    "results": [
        {
            "created": "2023-05-15T14:35:16.781+00:00",
            "modified": "2023-05-15T14:38:26.691+00:00",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.15"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "personalizedOffer1234",
            "name": "Test personalized offer with frequency constraint",
            "status": "draft",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "placement": "offerPlacement1234",
                    "components": [
                        {
                            "type": "html",
                            "format": "text/html",
                            "language": [
                                "en-us"
                            ],
                            "content": "Hello You qualify for our Discount of 60%"
                        }
                    ]
                }
            ],
            "selectionConstraint": {
                "startDate": "2022-07-27T05:00:00.000+00:00",
                "endDate": "2023-07-29T05:00:00.000+00:00",
                "profileConstraintType": "none"
            },
            "rank": {
                "priority": 0
            },
            "cappingConstraint": {},
            "frequencyCappingConstraints": [
                {
                    "enabled": false,
                    "limit": 1,
                    "startDate": "2023-05-15T14:25:49.622+00:00",
                    "endDate": "2023-05-25T14:25:49.622+00:00",
                    "scope": "global",
                    "entity": "offer",
                    "repeat": {
                        "enabled": false,
                        "unit": "month",
                        "unitCount": 1
                    }
                }
            ]
        }
    ],
    "count": 1,
    "total": 1,
    "_links": {
        "self": {
            "href": "/offers?offer-type=personalized&href={SELF_HREF}",
            "type": "application/json"
        }
    }
}
```
