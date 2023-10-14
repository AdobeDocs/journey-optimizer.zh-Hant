---
title: 刪除版位
description: 版位是用來展示優惠方案的容器。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 944efb12-6745-4bb2-be52-293e23925350
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 5%

---

# 刪除位置 {#delete-placement}

有時可能需要移除(DELETE)位置。 只能刪除您在租使用者容器中建立的版位。 這可透過向以下對象執行DELETE請求來完成 [!DNL Offer Library] 使用您要刪除位置例項ID的API。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 位置所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新之位置的例項ID。 | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態202 （無內容）和空白內文。

您可以嘗試對位置進行查詢(GET)請求以確認刪除。 您需要在請求中加入Accept標頭，但應該會收到HTTP狀態404 （找不到），因為位置已從容器中移除。
