---
title: 刪除標籤
description: 標籤可讓您更妥善地組織和排序優惠方案。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 5%

---

# 刪除標籤

有時可能需要移除(DELETE)標籤。 只能刪除您在租用戶容器中建立的標籤。 若要這麼做，請對 [!DNL Offer Library] API使用您要刪除之標籤的$id。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 標籤所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新之標籤的例項ID。 | `d48fd160-13dc-11eb-bc55-c11be7252432` |

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

成功的回應會傳回HTTP狀態202（無內容）和空白內文。

您可以嘗試對標籤進行查詢(GET)以確認刪除。 您需要在請求中加入Accept標題，但應會收到HTTP狀態404（找不到），因為標籤已從容器中移除。
