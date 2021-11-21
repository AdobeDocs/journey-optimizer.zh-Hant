---
title: 刪除集合
description: 集合是根據行銷人員定義的預先定義條件（例如優惠方案的類別）而提供的優惠方案子集。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 7%

---

# 刪除集合

有時可能需要移除(DELETE)集合。 只能刪除您在租用戶容器中建立的集合。 若要這麼做，請對 [!DNL Offer Library] API，使用您要刪除之集合的$id。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新之集合的例項ID。 | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態202（無內容）和空白內文。

您可以嘗試對集合進行查詢(GET)，以確認刪除。 您需要在請求中加入Accept標題，但應會收到HTTP狀態404（找不到），因為集合已從容器中移除。
