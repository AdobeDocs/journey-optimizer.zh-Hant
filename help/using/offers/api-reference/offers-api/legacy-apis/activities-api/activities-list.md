---
title: 列舉決定
description: 決定包含通知優惠選擇的邏輯。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: e9bd7602-8945-4768-8a56-dc13ade32a0b
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 5%

---

# 列舉決定 {#list-decisions}

決定包含通知優惠選擇的邏輯。

您可以透過對[!DNL Offer Library] API執行單一GET請求，來檢視容器中所有決定的清單。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ACTIVITIES}&{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ACTIVITIES}` | 定義與決定相關聯的結構描述。 | `https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5` |
| `{QUERY_PARAMS}` | 篩選結果的選用查詢引數。 | `limit=2` |

**要求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `q` | 在選取的欄位中搜尋的可選查詢字串。 查詢字串應為小寫，並可由雙引號包圍，以防止加以代碼化及逸出特殊字元。 字元`+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /`具有特殊意義，在查詢字串中出現時應該以反斜線逸出。 | `default` |
| `qop` | 將AND或OR運運算元套用至q查詢字串引數中的值。 | `AND` / `OR` |
| `field` | 要限制搜尋的選用欄位清單。 此引數可重複使用，如下所示： field=field1[，field=field2，...]和（路徑運算式採用點分隔路徑的形式，例如_instance.xdm:name） | `_instance.xdm:name` |
| `orderBy` | 依特定屬性排序結果。 在標題(`-`)前新增`orderby=-title`將會依標題以遞減順序(Z-A)排序專案。 | `-repo:createdDate` |
| `limit` | 限制傳回的決策數。 | `limit=5` |

**回應**

成功的回應會傳回存在於您可存取之容器中的決定清單。

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
