---
solution: Journey Optimizer
product: journey optimizer
title: 使用Journey Optimizer API
description: Journey Optimizer提供RESTful API，可讓您以程式設計方式執行應用程式中的關鍵作業。 瞭解如何存取及使用它們。
feature: Integrations, Data Ingestion
role: Developer
level: Intermediate
exl-id: 4c897c52-6eb2-4d6e-aaa9-9bd83608b2b6
source-git-commit: cbfebeaaa3ef6e55d48457012fd94bd74afc91de
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 4%

---

# 使用[!DNL Journey Optimizer] API {#apis-gs}

## 快速存取 {#quick-access}

>[!IMPORTANT]
>
>**開始使用Journey Optimizer API：**
>
>* **[瀏覽完整的API參考](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}** — 存取所有Journey Optimizer API並直接進行測試
>* **[設定驗證](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}** — 收集必要的認證，以開始使用API
>* **[決定管理API](../offers/api-reference/getting-started.md)** — 以程式設計方式管理優惠和決定
>* **[Experience Decisioning API](../experience-decisioning/api-reference/deliver.md)** — 使用程式碼型體驗提供個人化的決定專案

## 概觀 {#overview}

Adobe Journey Optimizer API可讓您跨任何應用程式、裝置或頻道，提供個人化、連線且及時的客戶體驗，進而有效管理端對端客戶歷程。 客戶歷程是指從第一次接觸直至客戶離開，客戶與品牌互動的整個過程。 從認知階段開始，客戶在這個階段瞭解品牌並開始參與。 然後，客戶將進一步與品牌互動、造訪線上和實體網站、進行購買、傳送訊息或發佈評論。

Adobe Journey Optimizer是以原生方式建置在Adobe Experience Platform上，並結合統一的即時客戶設定檔、API優先開放框架、集中式Offer Decisioning、人工智慧(AI)和機器學習(ML)，以進行個人化和最佳化。 透過與Journey Optimizer API整合，品牌可聰明地決定下一個最佳互動，並在整個客戶歷程中提供規模、速度和彈性。

## Authentication {#authentication}

在使用Journey Optimizer API之前，您必須設定驗證以存取API端點。

請依照[驗證指南](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}收集所有Journey Optimizer API的必要驗證認證。

## API檔案 {#api-documentation}

完整的Adobe Journey Optimizer API檔案包含所有可用端點、請求/回應格式及互動式測試功能的詳細資訊。

存取[Adobe Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}並瀏覽&#x200B;**API參考**&#x200B;功能表以探索所有可用的API。

## 決定管理API {#decision-management-apis}

Journey Optimizer為決定管理提供專用的API，可讓您以程式設計方式管理優惠、決定和刊登版位。

請參閱[決定管理API開發人員指南](../offers/api-reference/getting-started.md)，以開始使用Offer Decisioning API。

## Experience Decisioning API {#experience-decisioning-apis}

Journey Optimizer也提供Experience Decisioning API，透過程式碼式體驗提供個人化決策專案。 Experience Decisioning提供簡化的個人化方法，包含決定專案、適用規則和選擇策略。

**可用的API作業：**

* **決定專案** — 建立、讀取、更新和刪除決定專案
* **選擇策略** — 定義如何選擇和排名決定專案
* **適用性規則** — 設定專案適用性的條件
* **專案集合** — 將決定專案組織到集合中
* **排名公式** — 設定自訂排名邏輯
* **位置** — 定義決策專案出現的位置

進一步瞭解[Experience Decisioning API參考](../experience-decisioning/api-reference/deliver.md)，並探索如何[使用程式碼式體驗來提供選件](../experience-decisioning/api-reference/deliver.md)。
