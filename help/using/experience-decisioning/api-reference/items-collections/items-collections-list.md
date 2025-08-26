---
title: 清單專案集合
description: 集合可讓您根據自己的偏好設定來分類和分組決策專案。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: cc9f0d7a-6166-4736-8cb7-1989816708ad
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 10%

---

# 清單專案集合 {#list-decision-items}

集合（也稱為專案集合）可讓您根據偏好設定將決策專案分類及分組。 這些類別是透過制定利用決定項目屬性的規則所建立的。

您可以透過對優惠資料庫API執行單一GET請求，以檢視所有專案集合的清單。

**API格式**

```http
GET /{ENDPOINT_PATH}/item-collections?{QUERY_PARAMS}
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
curl -X GET 'https://platform.adobe.io/data/core/dps/item-collections?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回您有權存取的專案集合清單。

```json
{
    "results": [
        {
            "created": "2024-01-31T18:28:52.888Z",
            "modified": "2024-06-28T19:44:13.112Z",
            "etag": 7,
            "schemas": [
                "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "itemCollection1234",
            "name": "Item collection One",
            "description": "Item collection",
            "constraints": [
                {
                    "itemCatalogId": "itemCatalog1234",
                    "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
                }
            ],
            "tags": []
        },
        {
            "created": "2024-06-10T16:02:57.878Z",
            "modified": "2024-06-10T16:02:57.878Z",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/decisioning/item-collection;version=1.2"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "itemCollection5678",
            "name": "Item collection One",
            "description": "Item collection",
            "constraints": [
                {
                    "itemCatalogId": "itemCatalog1234",
                    "uiModel": "{\"operator\":\"greater than\",\"value\":{\"left\":\"_<imsOrg>.some_integer\",\"right\":100}}"
                }
            ],
            "tags": []
        }
    ],
    "count": 2,
    "total": 166,
    "_links": {
        "self": {
            "href": "/item-collections?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/item-collections?orderby=-modified&limit=2&start=2024-06-04T23:37:33.980Z",
            "type": "application/json"
        }
    }
}
```
