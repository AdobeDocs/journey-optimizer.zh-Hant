---
title: 刪除決定
description: 決定包含通知優惠選擇的邏輯。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%

---

# 刪除決定 {#delete-decision}

有時可能必須移除(DELETE)決定。 這可透過向以下對象執行DELETE請求來完成 [!DNL Offer Library] API使用 `id` 要刪除的決定的預設值。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要刪除之實體的ID。 | `offerDecision1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試向決定查詢(GET)以確認刪除。 您應該會收到HTTP狀態404 （找不到），因為決定已移除。
