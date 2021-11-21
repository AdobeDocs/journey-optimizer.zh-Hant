---
title: 清單位置
description: 版位是用來展示優惠方案的容器。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 36030ffe-eb7a-4487-914d-84ccb0a6bf6e
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 11%

---

# 清單位置

版位是用來展示優惠方案的容器。 版位有助於確保正確的優惠方案內容顯示在訊息中的正確位置。 將內容新增至優惠方案時，系統會要求您選取可顯示該內容的版位。

您可以對 [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 版位所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | 定義與版位相關聯的結構。 | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `{QUERY_PARAMS}` | 可選的查詢參數，以依據篩選結果。 | `limit=2` |

## 使用查詢參數

列出資源時，您可以使用查詢參數來頁面並篩選結果。

### 分頁

分頁最常見的查詢參數包括：

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `q` | 要在所選欄位中搜尋的選用查詢字串。 查詢字串應為小寫，並可以用雙引號包住，以防止其被標籤並逸出特殊字元。 字元 `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` 有特殊意義，且在出現在查詢字串時應以反斜線逸出。 | 網站JSON |
| `qop` | 將AND或OR運算子套用至q查詢字串參數中的值。 | `AND` / `OR` |
| `field` | 要限制搜索的欄位的可選清單。 此參數可重複，如下所示：field=field1[,field=field2,...] 和（路徑表達式採用點分隔路徑的形式，如_instance.xdm:name） | `_instance.xdm:name` |
| `orderBy` | 按特定屬性排序結果。 新增 `-` 前標題(`orderby=-title`)會以降序(Z-A)依標題排序項目。 | `-repo:createdDate` |
| `limit` | 限制傳回的版位數。 | `limit=5` |

**要求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2' \
  -H 'Accept: *,application/json' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回位於您可存取之容器中的位置清單。

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2020-10-21T19:48:51.843067Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "0feb6a80-0f32-11eb-8110-e17787c335b5",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-10-15T22:02:05.480449Z",
                "repo:lastModifiedDate": "2020-10-15T22:13:00.278175Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "New placement name",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "Updated placement description",
                    "@id": "xcore:offer-placement:12466ef35fc5baa0"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                }
            },
            {
                "instanceId": "269192b0-f8f2-11ea-8723-916b9fbadc53",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-09-17T14:29:10.107121Z",
                "repo:lastModifiedDate": "2020-09-17T14:29:10.107121Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:name": "demo placement",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "@id": "xcore:offer-placement:1221fac4e7340521"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 17,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=269192b0-f8f2-11ea-8723-916b9fbadc53&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
