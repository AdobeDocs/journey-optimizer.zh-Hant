---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 查詢集合
description: 集合是優惠方案的子集，根據行銷人員定義的預先定義條件，例如優惠方案類別。
feature: Decision Management, API, Collections
badge: label="舊版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 723daab2-5590-4c44-acb6-93a77f2e7877
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 18%

---

# 查詢集合 {#look-up-collection}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！[了解更多](../../../../experience-decisioning/gs-experience-decisioning.md)


集合是優惠方案的子集，根據行銷人員定義的預先定義條件，例如優惠方案類別。

您可以透過向[!DNL Offer Library] API發出GET請求來查詢特定集合，API在請求路徑中包含集合`id`。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-collections/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要查閱之實體的ID。 | `offerCollection1234` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回集合的詳細資料，包括有關唯一集合`id`的資訊。

```json
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
}
```
