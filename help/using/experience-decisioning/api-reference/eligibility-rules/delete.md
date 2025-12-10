---
title: 刪除適用性規則
description: 適用性規則可讓您根據要定位的內容（例如設定檔屬性和對象）定義合格的候選人。
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 19baf888-23b7-46de-9d3c-9a0fa8ab2297
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# 刪除適用性規則 {#delete-eligibility-rule}

有時可能必須移除(DELETE)適用性規則。 若要這麼做，請使用您要刪除的適用性規則ID，對優惠資料庫API執行DELETE請求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/eligibility-rules/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要刪除之實體的ID。 | `rule1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試對規則發出查詢(GET)請求以確認刪除。 您應該會收到HTTP狀態404 （找不到），因為規則已移除。
