---
title: 清單集合
description: 集合是優惠方案的子集，根據行銷人員定義的預先定義條件，例如優惠方案類別。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f27ffbe0-a61a-428a-bc37-db6b56e38a83
source-git-commit: 500b76aaaed604a73f2d8430a181763a9f35565f
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 6%

---

# 清單集合 {#list-collections}

集合是優惠方案的子集，根據行銷人員定義的預先定義條件，例如優惠方案類別。

您可以透過對執行單一GET請求來檢視所有收藏集的清單 [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-collections?{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | 篩選結果的選用查詢引數。 | `limit=2` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-collections?limit=2' \
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
| `property` | 選用的屬性篩選器： <br> <ul>  — 屬性會依AND作業分組。 <br><br>  — 引數可以重複執行，如下所示：property=<property-expr>[屬性(&amp;P)=<property-expr2>...] 或屬性=<property-expr1>[&amp;<property-expr2>...] <br><br>  — 屬性運算式的格式為 [！]欄位[op]值，含運算式 [==！=，&lt;=，>=，&lt;，>，~]，支援規則運算式 | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 依特定屬性排序結果。 在名稱前新增 — (orderby=-name)將會以降序順序(Z-A)依名稱排序專案。 路徑運算式採用點分隔路徑的形式。 此引數可重複執行，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 限制傳回的實體數。 | `limit=5` |

**回應**

成功的回應會傳回存在於您可存取之容器中的集合清單。

```json
{
        "results": [
        {
            "created": "2022-09-16T18:59:23.063+00:00",
            "modified": "2022-09-16T18:59:23.063+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerCollection1234",
            "name": "Test Collection with tags",
            "filterType": "any-tags",
            "ids": [
                "tag1234"
            ],
            "labels": [
                "core/C5",
                "custom/myLabel"
            ]
        },
        {
            "created": "2023-05-15T12:50:49.887+00:00",
            "modified": "2023-05-15T12:50:49.887+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.4"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerCollection5678",
            "name": "Test Collection with offers",
            "filterType": "offers",
            "ids": [
                "personalizedOffer1234",
                "personalizedOffer5678"
            ]
        }
    ],
    "count": 2,
    "total": 9,
    "_links": {
        "self": {
            "href": "/offer-collections?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-collections?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
