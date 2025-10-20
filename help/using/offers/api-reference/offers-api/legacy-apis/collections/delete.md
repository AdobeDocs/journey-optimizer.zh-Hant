---
title: 刪除集合
description: 集合是優惠方案的子集，根據行銷人員定義的預先定義條件，例如優惠方案類別。
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 351d1f44-f3dc-49f9-bc3d-c775dad3cad4
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 7%

---

# 刪除集合 {#delete-collection}

有時可能必須移除(DELETE)集合。 只能刪除您在租使用者容器中建立的集合。 使用您要刪除之集合的$id，對[!DNL Offer Library] API執行DELETE要求來達成此目的。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新之集合的執行個體ID。 | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

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

成功的回應會傳回HTTP狀態202 （無內容）和空白內文。

您可以嘗試向集合中發出查詢(GET)請求，以確認刪除。 您需要在請求中包含Accept標頭，但應該會收到HTTP狀態404 （找不到），因為集合已從容器中移除。
