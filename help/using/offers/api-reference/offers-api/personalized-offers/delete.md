---
title: 刪除個人化優惠方案
description: 個人化優惠方案是根據適用性規則和限制而自訂的行銷訊息。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 6%

---

# 刪除個人化優惠

有時可能需要移除(DELETE)個人化優惠方案。 系統只會刪除您在租用戶容器中建立的個人化優惠方案。 若要這麼做，請對 [!DNL Offer Library] 使用您要刪除之個人化優惠方案的$id的API。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 個人化優惠方案所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0f4bc230-13df-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態202（無內容）和空白內文。

您可以嘗試對個人化優惠方案進行查詢(GET)，以確認刪除。 您需要在請求中加入「接受」標題，但應會收到HTTP狀態404（找不到），因為個人化選件已從容器中移除。
