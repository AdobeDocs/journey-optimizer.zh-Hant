---
title: 更新擴充功能位置
description: Exd位置包含與限制及排名方法相關聯的集合，用以決定優惠方案。
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 6%

---

# 更新擴充功能位置 {#update-exd-placement}

您可以透過向優惠資料庫API發出PUT請求來修改或更新位置。

如需JSON PUT的詳細資訊，包括可用的作業，請參閱JSON PUT官方檔案。

**Accept和Content-Type標頭**

下表顯示請求標頭中包含Content-Type欄位的有效值：

| 參數 | 說明 |
| --------- | ----------- |
| Content-Type | `application/json` |

**API格式**

```http
PUT /{ENDPOINT_PATH}/exd-placements/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要更新之實體的ID。 | `placement1234` |

**要求**

```shell
curl --location --request PUT 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19aca09b0a456e57' \
--H 'Content-Type: application/json' \
--H 'x-gw-ims-org-id: {IMS_ORG}' \
--H 'x-sandbox-name: {SANDBOX_NAME}' \
--H 'x-api-key: {API_KEY}' \
--H 'Authorization: Bearer {ACCESS_TOKEN}' \
--X '{
  "id":"dps:exd-placement:19aca09b0a456e57",
  "description": "Keyboard application",
  "status":"archived"
}'
```

| 參數 | 說明 |
| --------- | ----------- |
| `value` | 您想要用來更新引數的新值。 |
| `path` | 要更新之引數的路徑。 |
| `op` | 用於定義更新連線所需動作的操作呼叫。 作業包括： `add`、`replace`、`remove`、`copy`和`test`。 |

**回應**

成功的回應會傳回擴充功能位置的更新詳細資料，包括ID。

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
