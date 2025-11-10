---
title: 刪除決定規則
description: 決定規則是新增至個人化優惠的限制，並套用至設定檔以判斷適用性。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7c02041c-b022-4027-b932-294b207add80
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 5%

---

# 刪除決定規則 {#delete-decision-rule}

有時可能必須移除(DELETE)決定規則。 只能刪除您在租使用者容器中建立的決定規則。 若要這麼做，請使用您要刪除的決定規則的執行個體識別碼，對[!DNL Offer Library] API執行DELETE要求。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 決策規則所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新的決定規則的例項ID。 | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**要求**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態202 （無內容）和空白內文。

您可以嘗試向決定規則查詢以確認刪除(GET)。 您需要在請求中包含Accept標頭，但應該會收到HTTP狀態404 （找不到），因為決定規則已從容器中移除。
