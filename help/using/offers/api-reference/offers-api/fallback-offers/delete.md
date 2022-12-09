---
title: 刪除回退優惠方案
description: 如果客戶不符合其他優惠方案的資格，系統會將備援優惠方案傳送給他們
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# 刪除回退優惠方案 {#delete-fallback-offer}

有時可能需要移除（刪除）備援優惠方案。 您在租用戶容器中建立的後援優惠方案只能刪除。 若要這麼做，請對 [!DNL Offer Library] API，使用您要刪除之備援優惠方案的$id。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 後援優惠方案所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 備援優惠方案的例項ID。 | `b3966680-13ec-11eb-9c20-8323709cfc65` |

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

成功的回應會傳回HTTP狀態202（無內容）和空白內文。

您可以嘗試對備援優惠方案查詢(GET)請求，以確認刪除。 您需要在請求中加入Accept標題，但應會收到HTTP狀態404（找不到），因為後援優惠方案已從容器中移除。
