---
title: 刪除個人化優惠方案
description: 個人化優惠是根據適用性規則和限制的可自訂行銷訊息。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---

# 刪除個人化優惠 {#delete-personalized-offer}

有時可能必須移除(DELETE)個人化優惠方案。 這可透過向以下對象執行DELETE請求來完成 [!DNL Offer Library] API使用您要刪除之個人化優惠的ID。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要刪除之實體的ID。 | `personalizedOffer1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以透過嘗試對個人化優惠進行查詢(GET)請求來確認刪除，並且應該會收到HTTP狀態404 （找不到），因為個人化優惠已移除。
