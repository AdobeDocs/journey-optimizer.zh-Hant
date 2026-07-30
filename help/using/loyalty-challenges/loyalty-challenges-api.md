---
solution: Journey Optimizer
product: journey optimizer
title: 忠誠度挑戰API
description: 瞭解如何使用忠誠度挑戰REST API以程式設計方式管理挑戰，並查詢Adobe Journey Optimizer中的設定檔參與狀態。
feature: Journeys
topic: Content Management
role: Developer
level: Intermediate
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 3756e104086c83bbca88b2fe770a40a8e9f39ef3
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 8%

---


# 忠誠度挑戰API {#loyalty-challenges-api}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用忠誠度挑戰REST API，以程式設計方式建立和管理挑戰，以及查詢和更新個別設定檔的挑戰參與狀態。

>[!ENDSHADEBOX]

## 快速存取 {#quick-access}

兩種REST API可用於解決忠誠度挑戰：

* **[忠誠度挑戰中繼資料API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}** — 以程式設計方式建立、擷取、更新、發佈、封存和重複挑戰。
* **[忠誠度挑戰狀態API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}** — 查詢並更新個別設定檔的挑戰參與狀態。

## 忠誠度挑戰中繼資料API {#metadata-api}

忠誠度挑戰中繼資料API可讓您在Journey Optimizer UI之外管理挑戰的整個生命週期。 使用它來自動化挑戰操作，或將忠誠度計畫管理整合到您自己的工具和工作流程中。 舉例來說，您可以建立、發佈和封存挑戰，以篩選和排序功能擷取所有挑戰，或複製現有挑戰，包括其歷程中繼資料和行銷活動。

➡️ [忠誠度挑戰中繼資料API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

## 忠誠度挑戰狀態API {#state-api}

忠誠度挑戰狀態API可讓您在設定檔層級與挑戰參與記錄互動。 使用它來查詢設定檔的目前參與狀態、進度和任務完成 — 例如，擷取設定檔的所有挑戰參與記錄、檢查挑戰內的特定任務狀態，或從一個或多個挑戰中撤銷設定檔。

➡️ [忠誠度挑戰狀態API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges-state){target="_blank"}

## Authentication {#authentication}

所有忠誠度挑戰API呼叫都需要以下標題：

| 標頭 | 說明 |
|---|---|
| `Authorization` | IMS存取權杖中的持有人權杖 |
| `x-gw-ims-org-id` | 您的IMS組織ID |
| `x-api-key` | 您的使用者端ID （API金鑰） |
| `x-sandbox-name` | 要定位的沙箱名稱 |

依照[驗證教學課程](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}擷取這些認證。
