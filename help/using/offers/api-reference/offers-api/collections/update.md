---
title: 更新集合
description: 集合是優惠方案的子集，根據行銷人員定義的預先定義條件，例如優惠方案類別。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7d766f0a-4fcb-434a-bbfd-e18ade71ae56
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 7%

---

# 更新集合 {#update-collection}

您可以透過向以下網站發出PATCH請求，修改或更新集合： [!DNL Offer Library] API

如需JSON修補程式的詳細資訊，包括可用的作業，請參閱官方檔案 [JSON修補程式檔案](https://jsonpatch.com/).

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示包含 *Content-Type* 請求標頭中的欄位：

| 頁首名稱 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/offer-collections/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要更新之實體的ID。 | `offerCollection1234` |

**要求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated offer collection"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated offer collection description"
    }
]'
```

| 參數 | 說明 |
| --------- | ----------- |
| `op` | 用於定義更新連線所需動作的操作呼叫。 操作包括： `add`， `replace`， `remove`， `copy` 和 `test`. |
| `path` | 要更新之引數的路徑。 |
| `value` | 您想要用來更新引數的新值。 |

**回應**

成功的回應會傳回集合的更新詳細資料，包括其唯一集合 `id`.

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
