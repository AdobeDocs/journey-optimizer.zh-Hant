---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用歷程
description: 開始使用歷程 — 瞭解歷程型別、工作流程、功能，以及在 [!DNL Adobe Journey Optimizer]中建立個人化客戶體驗的最佳實務
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 歷程、探索、開始、單一、讀取對象、對象資格、商業事件、即時、已排程、批次、事件觸發、工作流程、協調流程、個人化、多管道
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '1439'
ht-degree: 93%

---


# 開始使用歷程{#jo-general-principle}

[!DNL Adobe Journey Optimizer]可讓您建立個人化的多步驟客戶歷程，並即時因應您對象的行為和需求。 使用直覺式拖放版面，您就可以跨多管道，協調訊息和動作，運用內容資料和客群目標定位，發揮最大效果。

本指南提供清晰路徑圖，可協助您瞭解歷程基礎知識，為使用案例選擇正確的歷程類別，還可自信地設計歷程，提供有意義、即時客戶體驗。

## 什麼是歷程？

**歷程**&#x200B;是種自動化多步驟客戶體驗，可針對客戶行為、業務事件，或是排程的行銷活動，跨管道協調個人化互動。

使用 [!DNL Journey Optimizer] 來：

* 使用儲存在事件或資料來源中的情境資料，建立&#x200B;**即時協調**&#x200B;使用案例。 
* 設計&#x200B;**多步驟進階情境**，以動態方式，回應客戶行為與企業事件
* 大規模橫跨電子郵件、推播、簡訊、應用程式內、網頁等內容，提供&#x200B;**1:1個人化體驗**

![具有調色盤、畫布和屬性面板的歷程設計工具介面](assets/journey38.png)

➡️ **準備好開始建立了嗎？在 5 分鐘** [建立歷程](journey-gs.md)。

### 歷程與行銷活動：使用時機 {#journeys-vs-campaigns-intro}

[!DNL Adobe Journey Optimizer]提供三種觸及客戶的方法： **歷程** （1:1即時協調）、**行銷活動** （簡單批次或API觸發的傳遞）和&#x200B;**協調的行銷活動** （具有多實體資料的批次畫布工作流程）。

**快速決策：**

* 使用&#x200B;**歷程**，打造多步驟、行為導向體驗，讓每位客戶都可按照自己的步調前進
* 使用&#x200B;**動作/API 行銷活動**，可將簡單、排程或觸發的訊息傳遞給客群
* 針對需要多實體細分、精確預先傳送計數的複雜批次工作流程，使用&#x200B;**協調的行銷活動**

<!-- waiting for DOCAC-13912
➡️ **[View detailed comparison: Journeys vs Campaigns](../start/journeys-vs-campaigns.md)** - Includes decision guide, use cases, and feature availability-->

## 選擇歷程類別 {#journey-types}

[!DNL Adobe Journey Optimizer]支援四種歷程型別，每種都針對不同的進入機制和業務案例而設計：

* **單一歷程**：即時、事件觸發體驗（訂單確認、歡迎電子郵件）
* **閱讀對象歷程**：已排程批次通訊至對象區段 (電子報、促銷行銷活動)
* **客群資格鑑定歷程**：對客群會籍變更的即時回應 (VIP 升級、重新參與)
* **商業事件歷程**：影響許多客戶的業務狀況（詳細目錄警報、限時特賣）

<!-- waiting for DOCAC-13912 
➡️ **[Journey types and selection guide](journey-types-selection.md)** - Detailed comparison, decision tree, and feature compatibility matrix -->

## 使用歷程設計工具，完成建置 {#journey-designer}

**[歷程設計工具](using-the-journey-designer.md)**&#x200B;是您用來建立客戶體驗的視覺版面。 使用直觀拖放介面，您無需撰寫程式碼，即可協調歷程的各步驟。

![具有調色盤、版面和屬性面板的歷程設計工具介面](assets/journey38.png)

### 您可以在設計工具中執行哪些動作：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hant)

**定義進入點**

選擇客戶輸入的方式：透過事件、客群細分群體，或客群資格篩選。

[深入了解進入管理](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hant)

**傳送訊息**

針對電子郵件、推播、簡訊/多媒體簡訊、應用程式內、網頁等使用內建頻道動作，全都收錄在 Journey Optimizer 中設計。

[可在歷程中傳送訊息](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hant)

**新增邏輯和條件**

根據輪廓屬性、客群會籍，或是即時事件，分支歷程。

[使用條件](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hant)

**善用資料**

使用來自事件、[!DNL Adobe Experience Platform]或協力廠商API服務的內容資料。

[使用資料來源](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hant)

**連線外部系統**

建立自訂動作，以便整合入協力廠商系統，可用來傳送訊息，或是觸發工作流程。

[設定自訂動作](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hant)

**新增協調流程活動**

使用等待時間、跳轉、輪廓更新和客群管理，即可建立複雜的流程。

[深入探索所有活動](about-journey-activities.md)
:::

::::

➡️ **實作教學課程學習：** [觀看歷程設計工具影片](#video)，或可[探索端到端使用案例](jo-use-cases.md)

## 歷程建立工作流程 {#workflow}

建立成功歷程會遵循清晰、可重複流程。 以下是逐步工作流程：

**1. 計劃**→**2。 設計**→**3。 測試**→**4。 發佈**→**5。 監視** → **6。 最佳化**

### &#x200B;1. 計劃歷程 {#plan}

開啟設計工具之前，請先釐清目標：

* **目標是什麼？**（例如：加入新客戶，重新和非使用中的使用者互動）
* **客群有誰？** （特定區段、事件導向個人）
* **適合哪個歷程類型？**（請參閱上述[歷程類型](#journey-types)）
* **您將會使用哪些管道？**（電子郵件、推播、簡訊等）

### &#x200B;2. 請在版面中完成設計 {#design}

使用歷程設計工具，建置流量：

* **設定項目條件** - 定義輪廓如何輸入 (事件、客群、資格篩選)
* **新增協調流程邏輯** — 包含等待時間、條件和決策點
* **設定訊息** — 設計通訊，或可善用現有的範本
* **設定動作** — 設定要執行的內建或自訂動作
* **定義退出推薦準則** — 指定設定檔完成歷程的時機和方式

[瞭解如何使用歷程設計工具→](using-the-journey-designer.md)

### &#x200B;3. 上線前測試 {#test}

永遠在客戶體驗問題之前，先測試歷程，才能找出問題：

* 使用&#x200B;**測試模式**，以便使用測試設定檔，模擬歷程
* 使用&#x200B;**試運行**&#x200B;來預覽歷程執行，卻不會影響到真實資料，或是傳送訊息
* 驗證所有條件、訊息和操作是否如預期運作。
* 檢查時間、資料流程和個人化

[測試歷程→](testing-the-journey.md) | [了解試運行→](journey-dry-run.md)

### &#x200B;4. 發佈歷程 {#publish}

一旦完成測試後，發佈即可讓歷程上線：

* 審閱最終設定和屬性
* 發佈即可為真實客戶啟用
* 備註：可以暫停即時歷程，卻無法編輯（您必須建立新版本）

[發佈您的歷程 →](publish-journey.md)

### &#x200B;5. 監視效能 {#monitor}

追蹤歷程在現實世界的表現：

* 檢視歷程報告與分析
* 監視輸入、完成和錯誤率
* 設定嚴重問題的警報

[監視和報告 →](report-journey.md) | [設定警報→](../reports/alerts.md)

### &#x200B;6. 最佳化並反覆處理 {#optimize}

使用洞察來改善：

* 分析參與量度和轉換率
* 測試傳送時間最佳化
* 建立尚待改進的最新歷程版本
* 使用 AI 驅動的推薦

[最佳化您的歷程→](optimize.md) | [傳送時間最佳化→](send-time-optimization.md)

➡️ **準備好開始了嗎？** [立即建立第一個歷程→](journey-gs.md)

## 現實世界的使用案例 {#use-cases}

透過實際案例，了解如何套用歷程概念，解決常見行銷挑戰：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hant)

**歡迎新的訂閱者**

當客戶訂閱您的服務時，就會觸發迎賓歷程，鼓勵對方完成入門步驟。

[檢視使用案例 →](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=zh-Hant)

**傳送時間最佳化**

當每位客戶最有可能參與時，會使用 AI 來傳送電子郵件，將開啟率和點擊率最大化。

[檢視使用案例 →](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hant)

**加快交付速度**

逐步增加訊息量，以便改善寄件者的信譽，避開傳遞能力問題。

[檢視使用案例 →](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hant)

**依據工作日鎖定目標**

根據客戶進入您歷程的當週日期傳送不同內容，以提高關聯性。

[檢視使用案例 →](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hant)

**多管道行銷活動**

在單一歷程中跨電子郵件、推播、簡訊和網頁管道協調順暢的體驗。

[檢視使用案例 →](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hant)

**所有使用案例**

探索包含逐步實施的完整歷程使用案例庫。

[瀏覽所有→](jo-use-cases.md) | [使用案例庫→](../../rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## 探索歷程功能 {#capabilities}

當您更熟悉建立歷程時，請探索這些強大的功能以建立複雜的客戶體驗：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hant)

**進階運算式**

使用運算式編輯器針對資料操控和複雜邏輯建立動態條件和個人化。

[了解運算式](../../rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=zh-Hant)

**時區管理**

使用自動時區調整和最佳傳送時間來處理全球客群。

[管理時區](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hant)

**測試模式與試運行**

在上線之前，使用測試輪廓驗證歷程，並預覽執行而不影響真實資料。

[使用試運行](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hant)

**複製到沙箱**

跨沙箱複製歷程以簡化測試和部署工作流程。

[複製歷程](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hant)

**標籤和整理**

使用標籤來分類和篩選歷程，以更好地進行大規模管理。

[使用標籤整理](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hant)

**輸送量控制**

限制訊息輸送量，以管理傳送信譽並避免系統過載。

[控制輸送量](limit-throughput.md)
:::

::::

[檢視所有歷程功能 →](../../rp_landing_pages/manage-journey-landing-page.md)

## 觀看以學習 {#video}

取得歷程元件的視覺簡介，並瞭解在畫布中建立歷程的基本知識：

>[!VIDEO](https://video.tv.adobe.com/v/3430349?captions=chi_hant&quality=12)

➡️ **想要更多影片？** [探索歷程影片教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## 常見問題 {#common-questions}

+++ 歷程與行銷活動之間有何差異？

[!DNL Adobe Journey Optimizer]提供三種方法：

* **歷程**：1:1 即時協調流程，每個輪廓都以自己的步調在步驟中行進。最適合具有條件邏輯 (例如上線、購物車放棄) 的行為導向多步驟體驗。

* **行銷活動 (動作和 API 觸發)**：將簡單的訊息傳送給客群，依排程或透過 API 觸發程序同時執行所有輪廓。最適合促銷活動、電子報、交易型訊息。

* **協調的行銷活動**：使用關聯式資料 (輪廓+產品/商店/預訂) 進行具有複雜細分的多步驟批次工作流程。所有輪廓連同確切的預先傳送計數一起處理。最適合季節性促銷、產品推出，以及需要多實體資料的行銷活動。

**主要差異**：歷程維護即時動作的個別客戶狀態；動作/API 行銷活動會批次傳送簡單訊息；協調的行銷活動會提供具有多實體細分功能的批次工作流程畫布。

<!-- waiting for DOCAC-13912 - [See detailed comparison](#journeys-vs-campaigns) -->
[了解協調的行銷活動](../orchestrated/gs-orchestrated-campaigns.md)

+++

<!-- Waiting for DOCAC-13912
+++ Which journey type should I use?

Use the [decision guide](#decision-guide) or [comparison table](#journey-types-comparison) to choose between Unitary, Read Audience, Audience Qualification, and Business Event journeys based on your trigger mechanism and use case.

+++
-->

+++ 我可以編輯即時歷程嗎？

您可以編輯有限的元素 (名稱、訊息內容)，但結構變更需要建立新版本。[了解歷程版本](publish-journey.md#journey-versions)

+++

➡️ **更多問題？** [請檢視完整的歷程常見問題集](journey-faq.md)，包含 40 個以上的詳細答案

## 需要協助嗎？ {#help}

使用這些連結來尋找指引、疑難排解和資源。

### 常見工作的快速連結

* **[建立您的第一個歷程](journey-gs.md)** - 初學者逐步指南
* **[歷程常見問題集](journey-faq.md)** - 已回答的常見問題
* **[疑難排解](../../rp_landing_pages/troubleshoot-journey-landing-page.md)** - 診斷並修正問題
* **[錯誤碼參考](error-codes-reference.md)** - 瞭解錯誤訊息
* **[護欄和限制](../start/guardrails.md)** - 技術界限和最佳做法

### 取得有關問題的通知

設定&#x200B;**[歷程警示](../reports/alerts.md)**，以便在歷程發生錯誤或異常模式時接收即時通知。

### 其他資源

* **[歷程管理中心](../../rp_landing_pages/manage-journey-landing-page.md)** - 用於篩選、最佳化和輪廓管理的工具
* **[歷程活動參考](../../rp_landing_pages/about-journey-building-landing-page.md)** - 所有活動類型的完整指南
* **[疑難排解執行問題](troubleshooting-execution.md)** - 偵錯歷程執行問題
* **[疑難排解傳入活動](troubleshooting-inbound.md)** - 修正進入及資格問題

**準備好建立您的第一個歷程了嗎？**&#x200B;[立即開始 →](journey-gs.md)
