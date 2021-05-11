---
title: 列出個人化優惠方案
description: 個人化優惠是根據資格規則和限制而自訂的行銷訊息。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 4%

---

# 尋找個人化優惠

個人化優惠是根據資格規則和限制而自訂的行銷訊息。

您可以向[!DNL Offer Library] API提出GET要求，其中包含個人化選件`@id`或請求路徑中個人化選件的名稱，以查找特定的個人化選件。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PERSONALIZED_OFFER}&{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 個人化選件所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_PERSONALIZED_OFFER}` | 定義與個人化選件相關的架構。 | `https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5` |
| `id` | 用於匹配實體`@id`屬性的字串。 字串完全相符。 參數&quot;id&quot;和&quot;name&quot;不能一起使用。 | `xcore:personalized-offer:124cc332095cfa74` |
| `name` | 用於匹配實體xdm:name屬性的字串。 字串與大寫完全相符，但可使用萬用字元。 參數`id`和`name`不能一起使用 | `Discount offer` |

**要求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回位置的詳細資訊，包括您的容器ID、例項ID和獨特的個人化選件`@id`的相關資訊。

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5",
    "requestTime": "2020-10-21T20:59:16.238585Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-20T20:01:02.927874Z",
                "repo:lastModifiedDate": "2020-10-20T20:01:02.927874Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Discount offer",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "dc:language": [
                                        "en"
                                    ],
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json"
                                }
                            ],
                            "xdm:placement": "xcore:offer-placement:12428d436d87dc84"
                        }
                    ],
                    "xdm:rank": {
                        "xdm:priority": 1
                    },
                    "xdm:selectionConstraint": {
                        "xdm:startDate": "2020-10-01T16:00:00Z",
                        "xdm:endDate": "2021-12-13T16:00:00Z",
                        "xdm:eligibilityRule": "xcore:eligibility-rule:124cb4511da781fc"
                    },
                    "xdm:status": "draft",
                    "xdm:cappingConstraint": {
                        "xdm:globalCap": 150
                    },
                    "xdm:tags": [
                        "xcore:tag:1246d138ec8cca1f"
                    ],
                    "@id": "xcore:personalized-offer:124cc332095cfa74"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5#fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "@type": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
