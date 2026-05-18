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
TQID: https://experienceleague.adobe.com/3SJmNX6JrEY07R4pePNPzdokJrK7Ye6e9gV5i1LlDJA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 138
ht-degree: 23%

---

# 刪除後備產品建議 {#delete-fallback-offer}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../../../../experience-decisioning/gs-experience-decisioning.md)


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
