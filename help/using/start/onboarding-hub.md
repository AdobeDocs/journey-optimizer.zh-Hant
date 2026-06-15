---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer入門中心
description: Adobe Journey Optimizer的組織入門中心將逐步指示、實際使用案例和視訊內容彙整在一起，讓新使用者可以快速上手並提供他們的第一個客戶體驗。
feature: Get Started
topic: Content Management
role: User
level: Beginner
hide: true
keywords: journey optimizer，入門，入門中心，使用案例，影片，教學課程，開始，升級，第一個歷程
source-git-commit: 727d99f93d3fc19848f00ab423ec320a092b357c
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 12%

---

# Journey Optimizer入門中心 {#onboarding-hub}

>[!BEGINSHADEBOX]

**在此頁面上：** Adobe Journey Optimizer快速上線 — 觀看簡短介紹、依照逐步指示出貨您的第一個體驗、瀏覽真實世界的使用案例，並深入瞭解精選影片內容。

>[!ENDSHADEBOX]

第一次使用[!DNL Adobe Journey Optimizer]？ 此中心彙集各種資源，協助您從零開始使用第一個即時客戶體驗 — 提供常見目標的逐步指示、顯示可行功能的真實使用案例，以及精選影片內容（教學課程、逐步解說和實作練習）。

>[!TIP]
>
>不確定哪些功能符合您的目標？ 從目標開始[尋找適合您目標](ajo-use-case-guide.md)指南的Journey Optimizer功能，然後回到這裡取得逐步指示。

## 從這裡開始：觀看和學習 {#start-here}

如果您有10分鐘，請從此方向影片開始。 它會逐步解說介面，並依角色強調主要功能。

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

然後，利用這些學習資源建立實作信心：

* [Journey Optimizer教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — 每個角色的逐步影片和引導式逐步說明。
* [專家組織的影片播放清單](https://experienceleague.adobe.com/en/playlists?solution=Journey+Optimizer){target="_blank"} — 依序觀看的短片集。
* [訓練沙箱](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/configure-a-training-sandbox/introduction-and-prerequisites){target="_blank"} — 安全的環境，其中包含要在中練習的範例資料。
* [實作挑戰](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/challenges/introduction-and-prerequisites){target="_blank"} — 運用引導式練習所學的知識。

## 建立您的第一個體驗 {#build-first}

以下每個步驟都是以結果為導向的簡短步驟集：您將建置什麼、要建置什麼，以及如何建置。 挑選符合您第一個專案的目標，並依照連結前往詳細檔案。

### 歡迎新客戶 {#build-welcome}

**您將建置：**&#x200B;自動歡迎系列，歡迎每位新訂閱者並推播非作用中訂閱者。
**最適合的客戶：**&#x200B;行銷人員· **功能：**&#x200B;事件觸發的歷程

1. 確認您的[統一設定檔和對象](../audience/get-started-profiles.md)正在接收註冊事件。
2. [建立您的第一個歷程](../building-journeys/journey-gs.md)，並將註冊事件當做專案。
3. 新增歡迎[電子郵件](../email/get-started-email.md)，然後為尚未參與的設定檔新增等待步驟和後續的[推播通知](../push/get-started-push.md)。
4. [使用個人檔案屬性（例如名字和指定的興趣）個人化內容](../personalization/personalize.md)。

➡️ [以歷程開始](../building-journeys/journey-gs.md)

### 復原放棄的購物車 {#build-cart}

**您將建置：**&#x200B;即時復原流程，提醒客戶留下的專案。
**最適合的客戶：**&#x200B;行銷人員· **功能：**&#x200B;事件觸發的歷程

1. 確定放棄購物車事件已送達Journey Optimizer （如有需要，請與您的[資料團隊](../data/gs-data.md)合作）。
2. [建置由放棄事件觸發的歷程](../building-journeys/journey-gs.md)。
3. 傳送個人化提醒電子郵件；如果24小時內沒有點按，則分支到[推播](../push/get-started-push.md)後續追蹤。
4. [使用放棄的專案和忠誠度狀態個人化](../personalization/personalize.md)。

➡️ [以歷程開始](../building-journeys/journey-gs.md)

### 傳送異動訊息 {#build-transactional}

**您將建置：**&#x200B;由外部系統觸發的隨選訂單、送貨或約會確認。
**最佳對象：**&#x200B;行銷人員和開發人員· **功能：** API觸發的行銷活動

1. 檢閱[API觸發的行銷活動](../campaigns/api-triggered-campaigns.md)如何運作，以及它們預期的裝載。
2. 設計訊息範本，並[使用交易詳細資料進行個人化](../personalization/personalize.md)。
3. 請您的開發人員從您的訂單或履行系統呼叫行銷活動端點。

➡️ [使用API觸發的行銷活動](../campaigns/api-triggered-campaigns.md)

### 使用A/B測試啟動行銷活動 {#build-campaign}

**您將建置：**&#x200B;排定的促銷活動，會自動挑選表現最佳的內容。
**最佳對象：**&#x200B;行銷人員· **功能：**&#x200B;排程行銷活動+內容實驗

1. [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)並定義您的對象。
2. 使用[AI內容產生](../content-management/gs-generative.md)來草稿主旨行並複製變化。
3. 設定[內容實驗](../content-management/experiment-accelerator-gs.md)以測試範例上的變體，然後將獲勝者傳送給其餘者。

➡️ [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)

### 根據客戶個人化優惠方案 {#build-offers}

**您將建置：**&#x200B;顯示給每位客戶之單一最佳優惠的決定。
**最適合行銷人員：** · **功能：**&#x200B;決策

1. [開始使用Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)，並建立您的優惠方案和適用性規則。
2. 將決定新增至[歷程](../building-journeys/journey-gs.md)或行銷活動訊息。
3. [AI功能](ai-features.md)中的圖層，可自動排名和最佳化優惠。

➡️ [開始使用Offer Decisioning](../offers/get-started/starting-offer-decisioning.md)

## 依目標的使用案例 {#use-cases}

上述範例涵蓋最常見的起點，但Journey Optimizer支援更多情境 — 從主動式中斷通知和客戶重新參與到即時位置感知訊息。 每個案例都結合了一或多個共同運作的功能。

若要尋找&#x200B;*您*&#x200B;目標的確切功能，請在[尋找適合您目標](ajo-use-case-guide.md)的Journey Optimizer功能，使用完整、目標組織的索引。 如需端對端的有效範例，請參閱[歷程使用案例庫](../building-journeys/jo-use-cases.md)。

## 視訊程式庫 {#videos}

依主題瀏覽已組織的視訊內容。 每個索引標籤都會連結至Experience League上的相關教學課程和播放清單。

>[!BEGINTABS]

>[!TAB 開始使用]

* [Journey Optimizer簡介](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/introduction){target="_blank"} — 核心概念與產品導覽。
* [Journey Optimizer教學課程總覽](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — 引導式影片的完整目錄。

>[!TAB 歷程與行銷活動]

* [建立歷程簡介](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"} — 建立您的第一個事件觸發歷程。
* [使用Journey Agent建置歷程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/journeys/journey-agent-overview){target="_blank"} — 從自然語言提示建立歷程。

>[!TAB Personalization和AI]

* [用於產生內容的AI小幫手](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/content-management/ai-assistant/ai-assistant-for-content-generation-overview){target="_blank"} — 產生復本、影像和變化。
* [使用決策功能個人化Web優惠方案](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/use-decisioning-to-personalize-web-offers/introduction){target="_blank"} — 根據客戶量身打造優惠方案。

>[!TAB 報告與最佳化]

* [使用即時報告監視和分析您的歷程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/report-and-monitor/monitor-and-analyze-your-journey-with-live-reports){target="_blank"} — 即時追蹤效能。
* [建立電子郵件行銷活動的內容實驗](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/experimentation/content-experiments-for-emails){target="_blank"} — 測試並最佳化內容。

>[!ENDTABS]

## 依角色列出的入門檢查清單 {#checklist}

上線涉及多個角色。 選擇您的角色以檢視重點開始的路徑：

* **管理員** — 設定沙箱、許可權和通道。 [管理員入門](path/administrator.md)
* **資料工程師** — 模型結構描述和擷取資料。 [資料工程師入門](path/data-engineer.md)
* **開發人員** — 整合SDK並觸發事件。 [開發人員入門](path/developer.md)
* **行銷人員** — 建立歷程、內容和對象。 [行銷人員快速入門](path/marketer.md)

如需這些角色如何搭配運作的完整概觀，請參閱[角色和責任](quick-start.md)。

## 相關資源 {#related-resources}

* [為您的目標尋找正確的Journey Optimizer功能](ajo-use-case-guide.md) — 每個功能的目標優先決定指南。
* [歷程使用案例庫](../building-journeys/jo-use-cases.md) — 實用的範例和實作模式。
* [重要術語](terminology.md) — 釐清每項功能背後的概念。
* [AI與智慧型功能](ai-features.md) — 探索AI小幫手、傳送時間最佳化及內容產生。
* [開始使用資料管理](../data/gs-data.md) — 如何擷取、統一及啟用資料。
