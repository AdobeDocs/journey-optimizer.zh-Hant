---
title: 刪除遞補優惠
description: 如果客戶不符合其他優惠方案的資格，系統會傳送遞補優惠方案給客戶
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5e97a1fd-7542-4c9a-8234-21c1fa419671
source-git-commit: d312410ce2a91d3084d99e3caceb53ce4ada87b8
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 8%

---

# 刪除遞補優惠 {#delete-fallback-offer}

有時可能必須移除(DELETE)遞補優惠。 您只能在租使用者容器中建立的遞補優惠方案，才會被刪除。 這可透過向以下對象執行DELETE請求來完成 [!DNL Offer Library] API使用您要刪除之遞補優惠的$id。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 遞補優惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 遞補優惠的例項ID。 | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態202 （無內容）和空白內文。

您可以嘗試對遞補優惠進行查詢(GET)以確認刪除。 您需要在請求中包含Accept標頭，但應該會收到HTTP狀態404 （找不到），因為已經從容器中移除遞補優惠。
