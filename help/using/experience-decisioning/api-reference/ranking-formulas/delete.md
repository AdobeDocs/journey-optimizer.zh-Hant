---
title: 刪除排名公式
description: 排名公式可讓您定義用於排名專案的評分函式。
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4ea50481-b1b9-4e0c-ad4e-c4139891bfdf
source-git-commit: 6378c4a8cb911088c685166b9c1b29a1773d47b7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---

# 刪除排名公式 {#delete-selection-strategy}

有時可能必須移除(DELETE)排名公式。 若要這麼做，請使用您要刪除之排名公式的ID，對優惠資料庫API執行DELETE要求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 要刪除之實體的ID。 | `rankingFormula1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試對排名公式發出查詢(GET)請求以確認刪除。 您應該會收到HTTP狀態404 （找不到），因為已移除排名公式。
