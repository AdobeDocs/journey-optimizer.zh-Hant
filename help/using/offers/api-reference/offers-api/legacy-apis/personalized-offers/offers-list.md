---
title: 列出個人化優惠
description: 個人化優惠是根據適用性規則和限制的可自訂行銷訊息。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 50f4119f-c730-4883-867e-eac83793dced
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 5%

---

# 列出個人化優惠 {#list-personalized-offers}

個人化優惠是根據適用性規則和限制的可自訂行銷訊息。

您可以對[!DNL Offer Library] API執行單一GET要求，以檢視容器中所有個人化優惠方案的清單。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PERSONALIZED_OFFER}&{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 個人化優惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_PERSONALIZED_OFFER}` | 定義與個人化優惠相關聯的結構描述。 | `https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5` |
| `{QUERY_PARAMS}` | 篩選結果的選用查詢引數。 | `limit=1` |

**要求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
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
| `q` | 在選取的欄位中搜尋的可選查詢字串。 查詢字串應為小寫，並可由雙引號包圍，以防止加以代碼化及逸出特殊字元。 字元`+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /`具有特殊意義，在查詢字串中出現時應該以反斜線逸出。 | `discounted offers` |
| `qop` | 將AND或OR運運算元套用至q查詢字串引數中的值。 | `AND` / `OR` |
| `field` | 要限制搜尋的選用欄位清單。 此引數可重複使用，如下所示： field=field1[、field=field2，...]和（路徑運算式採用點分隔路徑的形式，例如_instance.xdm：name） | `_instance.xdm:name` |
| `orderBy` | 依特定屬性排序結果。 在標題(`orderby=-title`)前新增`-`將會依標題以遞減順序(Z-A)排序專案。 | `-repo:createdDate` |
| `limit` | 限制傳回的個人化優惠方案數量。 | `limit=5` |

**回應**

成功的回應會傳回個人化優惠方案清單，這些優惠方案會顯示在您可存取的容器中。

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5",
    "requestTime": "2023-10-22T20:36:50.408105Z",
    "_embedded": {
    "results": [
        {
                "instanceId": "2cdb4d10-149e-11eb-b1a9-a779d2fe8690",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2023-10-22T19:38:35.489354Z",
                "repo:lastModifiedDate": "2023-10-22T19:45:43.839088Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "Checking Advanced",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "dc:format": "image/png",
                                    "repo:id": "urn:aaid:sc:US:7db21be9-89ee-472a-b2c9-91f7a39ada51",
                                    "repo:resolveURL": "https://platform-cs-va6.adobe.io/content/storage/id/urn:aaid:sc:US:7db21be9-89ee-472a-b2c9-91f7a39ada51/:rendition;size=300",
                                    "repo:name": "mobile-check-deposit.png",
                                    "dc:language": [
                                        "en-us"
                                    ],
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-imagelink",
                                    "xdm:deliveryURL": ""
                                }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/offline",
                            "xdm:placement": "xcore:offer-placement:124f4e33724bb15f"
                        },
                {
                            "xdm:components": [
                        {
                                    "dc:format": "text/html",
                                    "repo:name": "my content",
                                    "dc:language": [
                                "en-us"
                            ],
                                    "xdm:content": "{\n\"foo\": \"bar\"\n}",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-html"
                        }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
                }
            ],
                    "xdm:rank": {
                        "xdm:priority": 10
                    },
                    "xdm:characteristics": {
                        "PROD": "checking",
                        "offer_code": "CHECK200",
                        "region": "NA"
            },
                    "xdm:selectionConstraint": {
                        "xdm:startDate": "2023-10-22T07:00:00.000Z",
                        "xdm:endDate": "2023-12-31T08:00:00.000Z",
                        "xdm:eligibilityRule": "xcore:eligibility-rule:124f4f57259caba5"
            },
                    "xdm:status": "draft",
                    "xdm:cappingConstraint": {
                        "xdm:globalCap": 1000
                    },
                    "xdm:tags": [
                        "xcore:tag:124f4e5c8a00cd92",
                        "xcore:tag:1229cf47455177b1"
                    ],
                    "@id": "xcore:personalized-offer:124f513c290bb16e"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5#2cdb4d10-149e-11eb-b1a9-a779d2fe8690",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/2cdb4d10-149e-11eb-b1a9-a779d2fe8690",
                        "@type": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
        }
    ],
        "total": 15,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&orderby=-repo:createdDate&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=1603395515489%2C2cdb4d10-149e-11eb-b1a9-a779d2fe8690&schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&orderby=-repo%3AcreatedDate%2CinstanceId&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
