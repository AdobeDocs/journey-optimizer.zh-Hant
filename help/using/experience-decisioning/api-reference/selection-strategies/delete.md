---
title: 刪除選取策略
description: 選取策略包含與限制關聯的集合，以及決定優惠的排名方法。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 774f3773-bc39-46c4-b32c-143abbd45696
source-git-commit: 7bfbb88c2817d18b7897a7fe1657ebf11be6eb58
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# 刪除選取策略 {#delete-selection-strategy}

有時可能必須移除(DELETE)選擇策略。 若要這麼做，請使用您要刪除的選擇策略ID，對選件程式庫API執行DELETE要求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要刪除之實體的ID。 | `selectionStrategy1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試對選擇策略發出查詢(GET)請求以確認刪除。 您應該會收到HTTP狀態404 （找不到），因為選取策略已移除。
