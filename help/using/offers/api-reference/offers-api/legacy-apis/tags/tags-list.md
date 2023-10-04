---
title: 列出集合限定詞
description: 集合限定詞可讓您更妥善地組織和排序優惠方案。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 6156689d9e5d7abedcd612389c5e332c695601f0
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 6%

---


# 列出集合限定詞 {#list-tags}

集合限定詞（先前稱為「標籤」）可讓您更妥善地整理及排序選件。 例如，您可以使用「黑色星期五」集合限定詞來標示「黑色星期五」優惠方案。 然後，您可以使用優惠資料庫中的搜尋功能，輕鬆找到所有具有該集合限定詞的優惠方案。

集合限定詞也可用於將優惠分組為集合。 如需詳細資訊，請參閱以下教學課程： [建立集合](../../../../offer-library/creating-collections.md).

您可以透過對以下專案執行單一GET請求，來檢視所有集合限定詞的清單： [!DNL Offer Library] API。

**API格式**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
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
| `property` | 選用的屬性篩選器： <ul><li>屬性會依AND作業分組。</li><li>引數可以重複執行，如下所示：property={PROPERTY_EXPR}[屬性(&amp;P)={PROPERTY_EXPR2}...] 或屬性={PROPERTY_EXPR1}[，{PROPERTY_EXPR2}...]</li><li>屬性運算式的格式為 `[!]field[op]value`，使用 `op` 在 `[==,!=,<=,>=,<,>,~]`，支援規則運算式。</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | 依特定屬性排序結果。 在名稱前新增 — (orderby=-name)將會以降序順序(Z-A)依名稱排序專案。 路徑運算式採用點分隔路徑的形式。 此引數可重複執行，如下所示： `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | 限制傳回的實體數。 | `limit=5` |

**回應**

成功的回應會傳回出現的集合限定詞清單。

```json
{
    "results": [
        {
            "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
