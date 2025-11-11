---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 刪除集合限定詞
description: 集合限定詞可讓您更妥善地組織和排序優惠方案。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# 刪除集合限定詞 {#delete-tag}

有時可能必須移除(DELETE)集合限定詞（先前稱為「標籤」）。 若要這麼做，請使用您要刪除的集合辨識符號的ID，對選件程式庫API執行DELETE要求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要刪除之實體的ID。 | `tag1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試對集合限定詞進行查詢(GET)請求，以確認刪除。 您應該會收到HTTP狀態404 （找不到），因為集合限定詞已移除。