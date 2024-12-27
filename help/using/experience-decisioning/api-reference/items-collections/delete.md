---
title: 刪除專案集合
description: 瞭解如何將您的群組決定分類為集合。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7290c857-cbc7-4197-ae13-430adcf1649b
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---

# 刪除專案集合 {#delete-decision-item}

有時可能必須移除(DELETE)專案集合。 若要這麼做，請使用您要刪除的專案集合ID，對優惠資料庫API執行DELETE要求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/item-collections/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要刪除之實體的ID。 | `itemCollections1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試對專案集合進行查詢(GET)來確認刪除。 您應該會收到HTTP狀態404 （找不到），因為專案集合已移除。
