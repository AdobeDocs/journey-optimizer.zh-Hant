---
title: 刪除個性化服務
description: 個性化服務是基於資格規則和約束的可定製營銷資訊。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 6%

---

# 刪除個人化優惠 {#delete-personalized-offer}

有時可能需要刪除(DELETE)個性化優惠。 只能刪除您在租戶容器中建立的個性化優惠。 這是通過對執行DELETE請求 [!DNL Offer Library] 使用您要刪除的個性化優惠的$id的API。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的終結點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 個性化優惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

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

成功的響應返回HTTP狀態202（無內容）和空白正文。

您可以通過嘗試對個性化優惠進行查找(GET)請求來確認刪除。 您需要在請求中包含「接受」標頭，但應收到HTTP狀態404（未找到），因為已從容器中刪除個性化服務。
