---
title: 刪除決定規則
description: 決定規則是新增至個人化優惠的限制，並套用至設定檔以判斷適用性。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 7%

---

# 刪除決定規則 {#delete-decision-rule}

有時可能必須移除(DELETE)決定規則。 這可透過向以下對象執行DELETE請求來完成 [!DNL Offer Library] API使用 `id` 要刪除的決定規則的。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要刪除之實體的ID。 | `offerRule1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以透過嘗試對決定規則進行查詢(GET)請求來確認刪除，並且應該會收到HTTP狀態404 （找不到），因為決定規則已移除。
