---
title: 刪除版位
description: 版位是用來展示優惠方案的容器。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 7%

---

# 刪除位置 {#delete-placement}

有時可能必須移除(DELETE)位置。 使用您要刪除之位置的ID對[!DNL Offer Library] API執行DELETE要求，即可完成此作業。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/placements/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要更新之位置的例項ID。 | `offerPlacement1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試向位置查詢(GET)請求來確認刪除，應該會收到HTTP狀態404 （找不到），因為位置已移除。
