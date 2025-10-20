---
title: 刪除集合
description: 集合是優惠方案的子集，根據行銷人員定義的預先定義條件，例如優惠方案類別。
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 9%

---

# 刪除集合 {#delete-collection}

有時可能必須移除(DELETE)集合。 若要這麼做，請使用您要刪除之集合的[!DNL Offer Library]，對`id` API執行DELETE要求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要刪除之實體的ID。 | `offerCollection1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-collections/offerCollection1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' 
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試向集合中發出查詢(GET)請求，以確認刪除。 您應該會收到HTTP狀態404 （找不到），因為集合已移除。
