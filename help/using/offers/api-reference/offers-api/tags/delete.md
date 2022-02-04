---
title: 刪除標籤
description: 標籤使您能夠更好地組織和整理您的優惠。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 5%

---

# 刪除標籤 {#delete-tag}

有時可能需要刪除(DELETE)標籤。 只能刪除您在租戶容器中建立的標籤。 這是通過對執行DELETE請求 [!DNL Offer Library] 使用要刪除的標籤的$id的API。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的終結點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 標籤所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 要更新的標籤的實例ID。 | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的響應返回HTTP狀態202（無內容）和空白正文。

您可以通過嘗試對標籤進行查找(GET)請求來確認刪除。 您需要在請求中包含「接受」標頭，但應接收HTTP狀態404（未找到），因為已從容器中刪除了標籤。
