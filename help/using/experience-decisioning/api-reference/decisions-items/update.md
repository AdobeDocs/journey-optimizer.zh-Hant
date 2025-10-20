---
title: 更新決定專案
description: 決定專案是行銷優惠方案，您可以建立並組織成集合和目錄。
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: b924b7d0-bbed-409e-8173-0685fc41d7de
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 5%

---

# 更新決定專案 {#update-decision-items}

您可以透過向優惠資料庫API發出PATCH請求來修改或更新決策專案。

如需JSON修補程式的詳細資訊，包括可用的作業，請參閱官方[JSON修補程式檔案](https://jsonpatch.com/)。

**API格式**

```http
PATCH /{ENDPOINT_PATH}/offer-items/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要更新之實體的ID。 | `offerItem1234` |

**要求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}' \
-d '[
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemName",
        "value": "Updated offer item"
    },
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemDescription",
        "value": "Updated offer item description"
    }
]'
```

| 參數 | 說明 |
| --------- | ----------- |
| `value` | 您想要用來更新引數的新值。 |
| `path` | 要更新之引數的路徑。 |
| `op` | 要執行的作業型別。 作業包括： `add`、`replace`、`remove`、`copy`和`test`。 |

**回應**

成功的回應會傳回更新專案的詳細資料，包括ID。 您可在後續步驟中使用ID來更新或刪除您的決定專案。

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
