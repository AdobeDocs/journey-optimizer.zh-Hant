---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 刪除版位
description: 版位是用來展示優惠方案的容器。
feature: Decision Management, API
badge: label="舊版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 20%

---

# 刪除位置 {#delete-placement}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！[了解更多](../../../../experience-decisioning/gs-experience-decisioning.md)


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
