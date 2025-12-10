---
title: 建立exd位置
description: 擴充策略包含與限制及排名方法相關聯的集合，用以決定優惠方案。
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---

# 建立exd位置 {#create-exd-placement}

您可以透過向優惠資料庫API發出POST請求來建立擴充版位。

**Accept和Content-Type標頭**

下表顯示請求標頭中包含Content-Type欄位的有效值：

| 參數 | 說明 |
| --------- | ----------- |
| Content-Type | `application/json` |

**API格式**

```http
POST /{ENDPOINT_PATH}/exd-placements
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |

**要求**

```shell
curl --location 'https://platform-stage.adobe.io/data/core/dps/exd-placements' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}' \
--data '{
  "name": "Test Exd Placement1 Pants",
  "channel": "https://ns.adobe.com/xdm/channel-types/email",
  "tags":["3d75b849-b344-402b-9d9e-5d750bd46884"],
  "channelConfiguration":"530b76f9-dcd6-4fd5-8c52-38e29b04a60a",
  "description": "compressing alarm",
  "status":"active"
}'
```

**回應**

成功的回應會傳回新建立的擴充功能位置的詳細資料，包括ID。 您可在後續步驟中使用ID來更新或刪除您的擴充功能位置。

```json
{
    "id": "dps:exd-placement:19cb038eca47bead",
    "sandboxId": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "etag": 2,
    "createdDate": "2024-11-18T18:48:56.298Z",
    "lastModifiedDate": "2024-11-18T18:57:27.457Z",
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedByClientId": "CJMTestClientACP"
}
```
