---
title: 刪除集合
description: 系列是選件的子集，根據行銷人員定義的預先定義條件，例如選件類別。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 7%

---

# 刪除集合

有時可能需要移除(DELETE)系列。 只能刪除您在租用戶容器中建立的系列。 若要這麼做，請使用您要刪除之系列的$id，對[!DNL Offer Library] API執行DELETE要求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 系列所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新之系列的例項ID。 | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態202（無內容）和空白的內文。

您可以嘗試對系列進行查閱(GET)請求，以確認刪除。 您需要在請求中加入「接受」標題，但應會收到HTTP狀態404（找不到），因為系列已從容器中移除。
