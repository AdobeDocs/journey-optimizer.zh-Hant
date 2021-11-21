---
title: 刪除決策規則
description: 決策規則是新增至個人化優惠方案的限制，並套用至設定檔以判斷資格。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 5%

---

# 刪除決定規則

有時可能需要移除(DELETE)決策規則。 只能刪除您在租用戶容器中建立的決策規則。 若要這麼做，請對 [!DNL Offer Library] 使用您要刪除之決策規則之例項ID的API。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 決策規則所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新的決策規則的例項ID。 | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態202（無內容）和空白內文。

您可以嘗試對決策規則進行查閱(GET)請求，以確認刪除。 您需要在請求中加入Accept標題，但應會收到HTTP狀態404（找不到），因為已從容器中移除決策規則。
