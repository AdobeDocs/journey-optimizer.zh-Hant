---
title: 刪除決定專案
description: 決定專案是行銷優惠方案，您可以建立並組織成集合和目錄。
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 4%

---

# 刪除決定專案 {#delete-decision-item}

若要移除決定專案，請使用您要刪除之決定專案的ID對優惠資料庫API執行DELETE要求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要刪除之實體的ID。 | `offerItem1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試向決定專案提出查詢(GET)請求以確認刪除。 您應該會收到HTTP狀態404 （找不到），因為決定專案已移除。
