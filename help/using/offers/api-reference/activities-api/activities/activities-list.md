---
title: 列舉決定
description: 決定包含通知優惠選擇的邏輯。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 123ed057-e15f-4110-9fc6-df0e9cb5b038
source-git-commit: 0d2a5d566a9bc328ebe8ec0f88bb6a7127f6624d
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 6%

---

# 列舉決定 {#list-decisions}

決定包含通知優惠選擇的邏輯。

您可以透過對以下執行單一GET請求來檢視所有決策的清單： [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-decisions?{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 篩選結果的選用查詢引數。 | `limit=2` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-decisions?limit=2' \
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

| 引數說明 | 範例 |
|------------|-----------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| `property` | 選用的屬性篩選器： |
 — 屬性會依AND作業分組。
 — 引數可重複執行，如下所示： `property=<property-expr>[&property=<property-expr2>...]` 或 `property=<property-expr1>[,<property-expr2>...]`
 — 屬性運算式的格式為 `[!]field[op]value`，作業位於 `[==,!=,<=,>=,<,>,~]`，支援規則運算式 | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` | | `orderBy`  |依特定屬性排序結果。 新增 `-` 在名稱之前(orderby=-name)會依名稱以遞減順序(Z-A)排序專案。 路徑運算式採用點分隔路徑的形式。 此引數可重複執行，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`，`-name`                    | | `limit`    |限制傳回的實體數。 | `limit=5`                                |


**回應**

成功的回應會傳回您有權存取的決定清單。

```json
{
    "results": [
        {
            "created": "2022-07-05T09:02:02.835+00:00",
            "modified": "2022-08-16T21:40:58.573+00:00",
            "etag": 12,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision1234",
            "name": "Test Decision One",
            "status": "live",
            "startDate": "2022-05-18T00:09:57.706+00:00",
            "endDate": "2032-08-13T21:40:58.235+00:00",
            "fallback": "fallbackOffer1234",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234",
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 0,
                        "order": {
                            "orderEvaluationType": "ranking-strategy",
                            "rankingStrategy": "123456789123"
                        }
                    },
                    "profileConstraint": {
                        "profileConstraintType": "none"
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }
            ]
        },
        {
            "created": "2022-09-05T14:12:13.773+00:00",
            "modified": "2022-09-05T14:12:13.773+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision5678",
            "name": "Test Decision Two",
            "status": "live",
            "startDate": "2022-08-31T21:00:00.000+00:00",
            "endDate": "2023-02-03T22:00:00.000+00:00",
            "fallback": "fallbackOffer5678",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234"
                    ],
                    "rank": {
                        "priority": 2
                    },
                    "optionSelection": {
                        "filter": "offerCollection5678"
                    }
                },
                {
                    "placements": [
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 1
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }          
            ]
        }
    ],
    "count": 2,
    "total": 21,
    "_links": {
        "self": {
            "href": "/offer-decisions?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-decisions?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
