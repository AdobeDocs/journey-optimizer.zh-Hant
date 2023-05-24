---
title: 刪除遞補優惠
description: 如果客戶不符合其他優惠條件，則會向他們發送備用優惠
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 8%

---

# 刪除遞補優惠 {#delete-fallback-offer}

有時可能需要刪除(DELETE)備用報價。 只能刪除您在租戶容器中建立的回退優惠。 這是通過對執行DELETE請求 [!DNL Offer Library] 使用您要刪除的備用優惠的$id的API。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的終結點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 回退優惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 回退要約的實例ID。 | `b3966680-13ec-11eb-9c20-8323709cfc65` |

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

成功的響應返回HTTP狀態202（無內容）和空白正文。

您可以通過嘗試對備用優惠進行查找(GET)請求來確認刪除。 您需要在請求中包含「接受」標頭，但應接收HTTP狀態404（未找到），因為已從容器中刪除回退優惠。
