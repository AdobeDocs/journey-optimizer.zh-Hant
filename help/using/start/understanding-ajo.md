---
solution: Journey Optimizer
product: journey optimizer
title: 瞭解Journey Optimizer
description: 瞭解Adobe Journey Optimizer如何與Adobe Experience Platform搭配運作，提供個人化的客戶體驗
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 4ae9e908d259dbd266417242cf9e65d693227061
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 3%

---

# 瞭解Journey Optimizer {#understanding-ajo}

Adobe Journey Optimizer和Adobe Experience Platform共同啟用大規模資料導向個人化。 此頁面說明這些系統如何運作，以及其主要功能區域如何結合，以提供卓越的客戶體驗。 [瞭解主要功能](get-started.md) | [探索重要術語](terminology.md)

## Journey Optimizer如何運作 {#how-it-works}

Adobe Journey Optimizer是以持續流程運作，收集、分析和套用資料以建立個人化的客戶歷程。

![](assets/ajo-aep-architecture-diagram.png)

### Adobe Experience Platform： Foundation {#aep-foundation}

Adobe Experience Platform作為骨幹，讓品牌得以集中客戶資料，並針對個人化體驗加以啟用：

* **資料平台** — 用於收集、管理和建構客戶資料的中央樞紐，以確保跨系統的一致性。 [瞭解結構描述和資料集](../data/get-started-schemas.md)
* **資料擷取（來源）** — 使用預先建立的聯結器從CRM平台、網站、行動應用程式和雲端儲存空間匯入資料。 [探索資料來源](../data/get-started-sources.md)
* **即時客戶設定檔** — 合併來自多個來源的資料（電子郵件互動、店內購買、網頁行為），以建立統一的設定檔。 [瞭解設定檔](../audience/get-started-profiles.md)
* **治理層** — 在遵守法規的同時，管理資料存取、隱私權法規遵循和安全性。 [檢視隱私權檔案](../privacy/get-started-privacy.md)

### Adobe Journey Optimizer：協調引擎 {#ajo-orchestration}

Adobe Journey Optimizer套用Adobe Experience Platform的資料和深入分析，提供智慧型、個人化的客戶體驗：

* **客戶瞭解** — 即時客戶設定檔可針對目標訊息啟用細分受眾。 [建立客群](../audience/about-audiences.md)
* **內容與選件** — 建立、管理及個人化內容的工具；為每個人選取最佳選件的即時邏輯。 [設計內容](../content-management/get-started-content.md) | [管理優惠方案](../offers/get-started/starting-offer-decisioning.md)
* **歷程與行銷活動管理** — 自動化互動順序（歷程）或排程單次鎖定目標的訊息（行銷活動）。 [建置歷程](../building-journeys/journey-gs.md) | [建立行銷活動](../campaigns/get-started-with-campaigns.md)
* **傳遞（連線）** — 透過電子郵件、簡訊、推播通知和直接郵件等通道傳遞訊息；將資料匯出至外部系統。 [設定管道](../configuration/get-started-configuration.md)
* **測量與分析** — 透過報告追蹤客戶參與度和行銷活動績效，以持續改進。 [檢視報告](../reports/campaign-global-report.md)

### 持續最佳化週期 {#optimization-cycle}

此生態系統以持續最佳化週期運作。 資料可促進客戶瞭解，進而提供個人化內容和決策的資訊。 這些任務會被協調為歷程、跨管道傳送、測量成效，並隨著時間而精簡。

![](../assets/do-not-localize/get-started-flow.png)

## 主要功能區域 {#functional-areas}

Journey Optimizer包含七個重要功能區域，可順暢地搭配運作：

| 功能區域 | 目的 | 重要活動 |
|-----------------|---------|----------------|
| **資料管理** | 組織客戶資料 | 定義結構描述、建立資料集，從各種系統匯入資料。 [了解更多](../data/get-started-schemas.md) |
| **客戶管理** | 瞭解您的客戶 | 建立統一的設定檔、解析身分、建立對象。 [了解更多](../audience/get-started-profiles.md) |
| **內容管理** | 建立個人化訊息 | 設計電子郵件、管理資產、建立範本和片段、個人化內容。 [進一步了解](../content-management/get-started-content.md) |
| **決定管理** | 即時選取最佳優惠方案 | 管理優惠資料庫、定義規則、套用限制、建立排名邏輯。 [了解更多](../offers/get-started/starting-offer-decisioning.md) |
| **歷程管理** | 設計自動化的客戶體驗 | 使用視覺化設計工具建立歷程、設定觸發器、新增條件和等待步驟。 [了解更多](../building-journeys/journey-gs.md) |
| **連線** | 連線資料來源和管道 | 設定來源聯結器、設定通道、連線至外部平台。 [了解更多](../configuration/get-started-configuration.md) |
| **管理與隱私** | 控制項設定與法規遵循 | 管理使用者、設定沙箱、設定頻道、處理隱私權請求。 [了解更多](../administration/permissions.md) |

### 這些區域如何共同運作 {#working-together}

這些功能區域會以連續的週期運作：

1. **資料擷取** — 資料流入Adobe Experience Platform，由資料管理建構
2. **客戶瞭解** — 即時客戶設定檔可統一資料；客戶管理會建立對象
3. **內容與優惠策略** — 內容管理建立訊息；決定管理定義優惠邏輯
4. **協調流程** - Journey Management會使用客戶資料、內容和決定，對應跨管道的互動
5. **傳遞** — 連線可促進透過通道傳遞訊息，或與外部系統共用資料
6. **測量** — 效能資料摘要深入分析以調整對象、內容、決定和歷程
7. **治理** — 管理和隱私權控制可確保整個過程中的合規性

## 架構詳細資料 {#architecture-details}

若為技術團隊，這裡有詳細的架構圖，說明Journey Optimizer如何與Adobe Experience Platform整合。 [瀏覽介面](user-interface.md)以實際探索這些元件。

![Adobe Journey Optimizer架構](assets/ajo-architecture.png)

Experience Platform上原生建置了四個應用程式：Adobe Real-Time Customer Data Platform、Journey Optimizer、Customer Journey Analytics和Adobe Mix Modeler。 Journey Optimizer可順暢地與這些應用程式搭配運作，但也可以獨立運作。 [檢閱護欄和限制](guardrails.md)以瞭解實作考量事項。

### 整合點 {#integration-points}

Journey Optimizer會在多個層級與Adobe Experience Platform整合：

* **資料層** — 共用相同的即時客戶設定檔、身分圖表和資料集
* **服務層** — 運用Adobe Experience Platform的控管、隱私權和查詢服務
* **應用程式層** — 在Adobe Experience Platform之上提供歷程協調、決定管理和內容管理

深入瞭解[Adobe Journey Optimizer Blueprint](https://experienceleague.adobe.com/zh-hant/docs/blueprints-learn/architecture/customer-journeys/journey-optimizer/journey-optimizer-overview){target="_blank"}。

## 隱私權與安全性 {#privacy-security}

Adobe Experience Cloud的隱私權及安全性實務適用於Adobe Journey Optimizer。 這些措施可確保遵守GDPR等隱私權法規，讓您在維持客戶信任的同時，提供個人化體驗。 [進一步瞭解Journey Optimizer的隱私權](../privacy/get-started-privacy.md)
