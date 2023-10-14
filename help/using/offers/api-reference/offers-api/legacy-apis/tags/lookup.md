---
title: 查詢集合限定詞
description: 集合限定詞可讓您更妥善地組織和排序優惠方案。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f31e6a17-c99a-4db9-a301-426a1f0bcc92
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---

# 查詢集合限定詞 {#look-up-tag}

您可以透過向以下網址發出GET要求，查詢特定的集合限定詞（先前稱為「標籤」）： [!DNL Offer Library] 包含集合限定詞的API `id` 在請求路徑中。

**API格式**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要查閱之實體的ID。 | `tag1234` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回收集限定詞的詳細資料，包括有關唯一收集限定詞的資訊 `id`.

```json
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
}
```
