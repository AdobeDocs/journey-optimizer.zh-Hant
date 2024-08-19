---
title: 刪除專案集合
description: 集合可讓您根據自己的偏好設定來分類和分組決策專案。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: dc47e2835379fbb2afb768beea6e4a1596f70ee9
workflow-type: tm+mt
source-wordcount: '120'
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
