---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 刪除後備產品建議
description: 如果客戶不符合其他優惠方案的資格，系統會傳送遞補優惠方案給客戶
feature: Decision Management, API
badge: label="舊版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 22%

---


# 刪除後備產品建議 {#delete-fallback-offer}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！[了解更多](../../../../experience-decisioning/gs-experience-decisioning.md)


有時可能必須移除(DELETE)遞補優惠。 使用您要刪除之遞補優惠的ID，對[!DNL Offer Library] API執行DELETE要求來達成此目的。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要刪除之實體的ID。 | `fallbackOffer1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以透過嘗試對優惠進行查詢(GET)請求來確認刪除，並且應該會收到HTTP狀態404 （找不到），因為遞補優惠已移除。
