---
title: 清單決定規則
description: 決策規則是新增至個人化優惠的限制，並套用至個人檔案以判斷資格。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 5%

---

# 清單決定規則

決策規則是新增至個人化優惠的限制，並套用至個人檔案以判斷資格。 您可以對[!DNL Offer Library] API執行單一GET請求，以檢視容器內現有決策規則的清單。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ELIGIBILITY_RULE}&{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 決策規則所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ELIGIBILITY_RULE}` | 定義與決策規則關聯的方案。 | `https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3` |
| `{QUERY_PARAMS}` | 可選查詢參數，以篩選結果。 | `limit=1` |

## 使用查詢參數

列出資源時，您可以使用查詢參數來頁面和篩選結果。

### 分頁

最常用於分頁的查詢參數包括：

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `q` | 可選的查詢字串，可在選取的欄位中搜尋。 查詢字串應為小寫，可以用雙引號括住，以防止其被標籤化並逸出特殊字元。 字元`+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /`有特殊意義，當出現在查詢字串中時，應以反斜線逸出。 | `default` |
| `qop` | 將AND或OR運算子套用至q查詢字串參數中的值。 | `AND` / `OR` |
| `field` | 將搜索限制為的欄位的可選清單。 此參數可重複，如下所示：field=field1[,field=field2,...]和（路徑表達式採用點分隔路徑的形式，如_instance.xdm:name） | `_instance.xdm:name` |
| `orderBy` | 依特定屬性排序結果。 在標題(`orderby=-title`)之前新增`-`，將依標題以遞減順序(Z-A)排序項目。 | `-repo:createdDate` |
| `limit` | 限制傳回的決策規則數。 | `limit=5` |

**要求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回您有權存取的容器內所顯示之決策規則清單。

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3",
    "requestTime": "2020-10-22T04:14:12.676802Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "36693c30-0377-11eb-9dd8-d781cc064407",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 3,
                "repo:createdDate": "2020-09-30T23:46:51.379003Z",
                "repo:lastModifiedDate": "2020-10-02T05:06:36.780806Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "Qualified for mortgage products",
                    "offerui:segmentModel": {
                        "name": "Qualified for mortgage products",
                        "canHaveFolder": true,
                        "isMissingAnsibleModel": false,
                        "description": "",
                        "deprecated": {
                            "reason": "",
                            "status": false
                        },
                        "schema": {
                            "name": "_xdm.context.profile",
                            "id": "some id"
                        },
                        "schemaName": "",
                        "expression": {
                            "xEventAttributesContainer": {
                                "itemType": "eventTypeCardContainer",
                                "logicalOperator": "then",
                                "exclude": false,
                                "items": []
                            },
                            "logicalOperator": "and",
                            "isValid": true,
                            "profileAttributesContainer": {
                                "itemType": "segmentContainer",
                                "logicalOperator": "and",
                                "exclude": false,
                                "items": [
                                    {
                                        "component": {
                                            "__entity__": true,
                                            "id": "profile._xcoree2etesting.productCategory",
                                            "type": "n"
                                        },
                                        "isPlaceholder": false,
                                        "comparisonType": "equals",
                                        "value": [
                                            "mortgage"
                                        ]
                                    }
                                ]
                            }
                        },
                        "mergePolicyId": "3558157a-19cb-40b4-ba13-a5f5ce31b011",
                        "namespace": "ups"
                    },
                    "xdm:condition": {
                        "xdm:format": "pql/text",
                        "xdm:type": "PQL",
                        "xdm:value": "_xcoree2etesting.productCategory.equals(\"mortgage\", false)"
                    },
                    "xdm:definedOn": {},
                    "xdm:description": "",
                    "@id": "xcore:eligibility-rule:12333714edbf49e6"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3#36693c30-0377-11eb-9dd8-d781cc064407",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/36693c30-0377-11eb-9dd8-d781cc064407",
                        "@type": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 8,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=36693c30-0377-11eb-9dd8-d781cc064407&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
