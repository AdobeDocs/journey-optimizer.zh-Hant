---
title: 列出決定專案
description: 決定專案是行銷優惠方案，您可以建立並組織成集合和目錄。
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: ac618861-276f-4f9c-95d3-7df0b5132be9
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 13%

---

# 列出決定專案 {#list-decision-items}

Journey Optimizer 可讓您建立行銷產品建議 (稱為決定項目)，您可以將其建立並組織到集中式目錄和集合中。這些屬性由標準和自訂屬性組成，旨在精確符合您的需求。 此外，它們納入設定檔限制，可讓您定義決策專案可顯示給誰。

您可以透過對優惠資料庫API執行單一GET請求來檢視所有決定專案的清單。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-items?{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 篩選結果的選用查詢引數。 | `limit=2` |

## 使用查詢引數 {#using-query-parameters}

您可以在列出資源時，使用查詢引數來頁面和篩選結果。

### 分頁 {#paging}

分頁最常見的查詢引數包括：

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `property` | 選用的屬性篩選器： <ul><li>屬性會依AND作業分組。</li><li>引數可以重複如下：屬性={PROPERTY_EXPR}[&amp;屬性={PROPERTY_EXPR2}...]或屬性={PROPERTY_EXPR1}[，{PROPERTY_EXPR2}...]</li><li>屬性運算式的格式為`[!]field[op]value`，在`op`中有`[==,!=,<=,>=,<,>,~]`，支援規則運算式。</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 依特定屬性排序結果。 在名稱前新增 — (orderby=-name)將會以降序順序(Z-A)依名稱排序專案。 路徑運算式採用點分隔路徑的形式。 此引數可以重複執行，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`，`-name` |
| `limit` | 限制傳回的實體數。 | `limit=5` |

**要求**

```shell
curl -X GET '<https://platform.adobe.io/data/core/dps/offer-items?limit=2>' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**回應**

成功的回應會傳回您有權存取的優惠方案專案清單。 `_<imsOrg>`節點可容納自訂決策專案屬性。

```json
{
    "results": [
        {
            "created": "2024-06-10T16:00:34.014Z",
            "modified": "2024-07-09T22:59:21.507Z",
            "etag": 1,
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerItem5678",
            "_experience": {
                "decisioning": {
                    "offeritem": {
                        "fCapConstraintsLastIndex": 0,
                        "lifecycleStatus": "draft"
                    },
                    "decisionitem": {
                        "itemCalendarConstraints": {
                            "endDate": "2030-12-31T08:00:00.000Z",
                            "startDate": "2024-06-10T04:00:00.000Z"
                        },
                        "itemCatalogID": "itemCatalong1234",
                        "itemConstraints": {
                            "eligibilityRule": "rule1234",
                            "profileConstraintType": "eligibilityRule"
                        },
                        "itemDescription": "Offer item description",
                        "itemID": "offerItem5678",
                        "itemLabels": [],
                        "itemName": "Offer Item One",
                        "itemPriority": 1,
                        "itemTags": []
                    }
                }
            },
            "_<imsOrg>": {
                "some_field": "some value"
            }
        },
        {
            "created": "2024-06-04T17:51:52.849Z",
            "modified": "2024-06-28T18:29:27.951Z",
            "etag": 5,
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerItem1234",
            "_experience": {
                "decisioning": {
                    "offeritem": {
                        "frequencyCappingConstraints": [],
                        "fCapConstraintsLastIndex": 0,
                        "lifecycleStatus": "approved"
                    },
                    "decisionitem": {
                        "itemCalendarConstraints": {
                            "endDate": "2030-12-31T08:00:00.000Z",
                            "startDate": "2024-06-01T07:00:00.000Z"
                        },
                        "itemCatalogID": "itemCatalong1234",
                        "itemConstraints": {
                            "profileConstraintType": "none"
                        },
                        "itemDescription": "Offer item description",
                        "itemID": "offerItem1234",
                        "itemLabels": [],
                        "itemName": "Offer Item Two",
                        "itemPriority": 2,
                        "itemTags": []
                    }
                }
            },
            "YOUR_CUSTOM_ATTRIBUTES": {
                "some_field": "some value",
                "some_boolean_field": true
            }
        }
    ],
    "count": 2,
    "total": 844,
    "_links": {
        "self": {
            "href": "/offer-items?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-items?orderby=-modified&limit=2&start=2024-06-28T03:44:15.630Z",
            "type": "application/json"
        }
    }
}
```
