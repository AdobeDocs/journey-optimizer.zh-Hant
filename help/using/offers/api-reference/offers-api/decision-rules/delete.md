---
title: 刪除決策規則
description: 決策規則是添加到個性化優惠中的約束，並應用到配置檔案以確定資格。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 5%

---

# 刪除決定規則 {#delete-decision-rule}

有時可能需要刪除(DELETE)決策規則。 只能刪除您在租戶容器中建立的決策規則。 這是通過對執行DELETE請求 [!DNL Offer Library] API使用要刪除的決策規則的實例ID。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的終結點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 決策規則所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 要更新的決策規則的實例ID。 | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

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

成功的響應返回HTTP狀態202（無內容）和空白正文。

您可以通過嘗試查找(GET)決策規則來確認刪除。 您需要在請求中包括「接受」標頭，但應接收HTTP狀態404（未找到），因為已從容器中刪除了決策規則。
