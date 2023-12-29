---
title: 刪除決定
description: 決定包含通知優惠選擇的邏輯。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 36a87d98-fd61-416e-83a1-e267a7b4d455
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 5%

---

# 刪除決定 {#delete-decision}

有時可能必須移除(DELETE)決定。 您只能在租使用者容器中建立的決定才會被刪除。 這可透過向以下對象執行DELETE請求來完成 [!DNL Offer Library] API使用您要刪除之遞補優惠的$id。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 決定的執行個體ID。 | `f88c9be0-1245-11eb-8622-b77b60702882` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態202 （無內容）和空白內文。

您可以嘗試向決定查詢(GET)以確認刪除。 您需要在請求中包含Accept標頭，但應該會收到HTTP狀態404 （找不到），因為決定已從容器中移除。
