---
title: 列舉決定
description: 決策包含通知選件選擇的邏輯。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 123ed057-e15f-4110-9fc6-df0e9cb5b038
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 4%

---

# 列舉決定

決策（先前稱為優惠方案活動）包含通知選件選擇的邏輯。

您可以對執行單一GET請求，以檢視容器內所有決策的清單 [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ACTIVITIES}&{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ACTIVITIES}` | 定義與決策相關聯的架構。 | `https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5` |
| `{QUERY_PARAMS}` | 可選的查詢參數，以依據篩選結果。 | `limit=2` |

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

## 使用查詢參數

列出資源時，您可以使用查詢參數來頁面並篩選結果。

### 分頁

分頁最常見的查詢參數包括：

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `q` | 要在所選欄位中搜尋的選用查詢字串。 查詢字串應為小寫，並可以用雙引號包住，以防止其被標籤並逸出特殊字元。 字元 `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` 有特殊意義，且在出現在查詢字串時應以反斜線逸出。 | `default` |
| `qop` | 將AND或OR運算子套用至q查詢字串參數中的值。 | `AND` / `OR` |
| `field` | 要限制搜索的欄位的可選清單。 此參數可重複，如下所示：field=field1[,field=field2,...] 和（路徑表達式採用點分隔路徑的形式，如_instance.xdm:name） | `_instance.xdm:name` |
| `orderBy` | 按特定屬性排序結果。 新增 `-` 前標題(`orderby=-title`)會以降序(Z-A)依標題排序項目。 | `-repo:createdDate` |
| `limit` | 限制傳回的決定數。 | `limit=5` |

**回應**

成功的回應會傳回您有權存取的容器內所存在的決策清單。

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5",
    "requestTime": "2020-10-21T22:38:32.838180Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "286f6f80-026b-11eb-9439-ad36e372cbf1",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 5,
                "repo:createdDate": "2020-09-29T15:48:02.808677Z",
                "repo:lastModifiedDate": "2020-10-15T15:49:26.673560Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef",
                    "xdm:name": "A2: Cross Channel Activity",
                    "xdm:endDate": "2020-10-09T07:00:00.000Z",
                    "xdm:startDate": "2020-09-29T07:00:00.000Z",
                    "xdm:status": "live",
                    "xdm:criteria": [
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122204529514a2c0"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                            }
                        },
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122201b2150d98c2"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:1222058c3f0d98de"
                            }
                        }
                    ],
                    "@id": "xcore:offer-activity:12317fe6aeec9330"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5#286f6f80-026b-11eb-9439-ad36e372cbf1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/286f6f80-026b-11eb-9439-ad36e372cbf1",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            },
            {
                "instanceId": "4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-14T22:12:10.300775Z",
                "repo:lastModifiedDate": "2020-10-14T22:12:10.300775Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef",
                    "xdm:name": "LBAR",
                    "xdm:endDate": "2021-02-28T08:00:00.000Z",
                    "xdm:startDate": "2020-10-14T07:00:00.000Z",
                    "xdm:status": "live",
                    "xdm:criteria": [
                        {
                            "xdm:placements": [
                                "xcore:offer-placement:122204529514a2c0"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                            }
                        }
                    ],
                    "@id": "xcore:offer-activity:124527ab00b2ebbc"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5#4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 7,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=4e0206d0-0e6a-11eb-884a-c1a1104e3d7d&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
