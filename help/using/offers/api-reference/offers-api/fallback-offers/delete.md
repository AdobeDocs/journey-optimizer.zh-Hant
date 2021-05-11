---
title: 刪除遞補優惠
description: 如果客戶不符合其他優惠的資格，則會傳送回退優惠給他們
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 8%

---

# 刪除遞補優惠

有時可能需要移除(DELETE)備援選件。 只能刪除您在租用戶容器中建立的備援選件。 若要這麼做，請使用您要刪除之備援選件的$id，對[!DNL Offer Library] API執行DELETE要求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 備援選件所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 備援選件的例項ID。 | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態202（無內容）和空白的內文。

您可以嘗試對備援選件進行查閱(GET)請求，以確認刪除。 您需要在請求中加入「接受」標題，但應收到HTTP狀態404（找不到），因為備援選件已從容器中移除。
