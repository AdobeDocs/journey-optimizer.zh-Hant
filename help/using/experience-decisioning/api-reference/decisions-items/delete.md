---
title: 刪除決定專案
description: 決定專案是行銷優惠方案，您可以建立並組織成集合和目錄。
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/OkPIse7NFATcyTdTT0pzNhjPMenbrvigSG2lSRatb-M
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 112
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

您可以嘗試向決定專案查詢(GET)以確認刪除。 您應該會收到HTTP狀態404 （找不到），因為決定專案已移除。
