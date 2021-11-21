---
title: 建立集合
description: 集合是根據行銷人員定義的預先定義條件（例如優惠方案的類別）而提供的優惠方案子集。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 683f8b86-8545-46d0-a4a8-25c5b3c7b9c3
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---

# 建立集合

集合是根據行銷人員定義的預先定義條件（例如優惠方案的類別）而提供的優惠方案子集。

您可以向 [!DNL Offer Library] API，同時提供容器ID。

## 接受和內容類型標題

下表顯示了 *內容類型* 和 *接受* 請求標題中的欄位：

| 標題名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**要求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Offer Collection 1",
        "xdm:filterType": "anyTags",
        "xdm:ids": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**回應**

成功的回應會傳回新建立集合的相關資訊，包括其唯一例項ID和位置 `@id`. 您可以在後續步驟中使用例項ID來更新或刪除您的集合。 您可以使用您的唯一集合 `@id` 以建立決策。

```json
{
    "instanceId": "0bf31c20-13f1-11eb-a752-e58fd7dc4cb3",
    "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2020-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
