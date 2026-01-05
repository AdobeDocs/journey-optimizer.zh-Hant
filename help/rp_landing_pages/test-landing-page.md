---
solution: Journey Optimizer
product: Journey Optimizer
title: 測試、驗證及核准
description: 探索Journey Optimizer中的所有測試和核准功能。 在啟動之前預覽內容、模擬歷程、驗證電子郵件、執行實驗、偵測衝突，以及設定核准工作流程。
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 測試，驗證，核准，品質保證， qa，測試設定檔，個人化，呈現，垃圾郵件檢查，內容實驗， a/b測試，衝突偵測，種子清單，校樣，範例資料，核准工作流程，電子郵件測試，驗證工作流程
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: 1b774d95a117903695e6954fb2c820adfdf0d3bb
workflow-type: tm+mt
source-wordcount: '2768'
ht-degree: 5%

---

# 測試、驗證及核准{#section-overview}

本節涵蓋Journey Optimizer中的所有測試和核准功能。 您會找到工具以使用測試設定檔預覽內容、驗證歷程邏輯、檢查電子郵件轉譯和垃圾郵件分數、執行A/B實驗、偵測衝突，以及設定核准工作流程。

此登陸頁面可協助您根據正在建置的內容（行銷活動與歷程）選擇正確的測試方法、引導您完成建議的測試工作流程，並可讓您快速存取所有測試和核准資源。 從[選擇下面的測試方法](#choose-your-testing-approach)開始，以識別哪些工具適用於您的使用案例。

## 為什麼測試和核准很重要

測試和核准程式是重要的品質閘道，可保護您的品牌聲譽並確保行銷活動取得成功。 以下是它們之所以重要的原因：

* **在錯誤到達客戶之前即發現錯誤** — 在快速且無風險的修正受控環境中，識別中斷的連結、不正確的個人化、轉譯問題和邏輯錯誤。

* **改善傳遞能力** — 測試垃圾郵件分數、驗證電子郵件驗證，以及檢查跨電子郵件使用者端的轉譯，以最大化收件匣位置和參與率。

* **確保品牌一致性** — 預覽包含不同測試設定檔的內容，以驗證各種客戶區段可正確顯示個人化，並維護品牌標準。

* **驗證複雜的歷程** — 模擬多步驟歷程流程，以確認觸發器是否正確引發、條件是否正確評估，以及客戶是否會在正確的時間收到正確的訊息。

* **建立責任制** — 實作需要利害關係人簽署的正式核准工作流程，建立明確的所有權，並減少未經授權或過早啟動的行銷活動。

* **節省時間和資源** — 在開發週期中及早偵測問題，因為修正更便宜、更快速，避免在啟動後進行代價高昂的更正或客戶服務升級。

## 測試功能概述

**可用的測試型別：**

* 內容測試：在傳送→[測試行銷活動](#testing-campaigns)、[測試個人化](#testing-personalization)之前，預覽及驗證訊息內容
* 歷程邏輯測試：在[測試歷程](#testing-journeys)→模擬客戶通過歷程路徑的進度
* 技術測試：驗證[技術驗證](#2-technical-validation)→轉譯、傳遞能力及驗證
* 效能測試：使用A/B實驗→[內容實驗](#content-experiments--ab-testing)比較內容變異
* 衝突測試：偵測行銷活動和歷程重疊→ [衝突偵測](#conflict-detection)
* 核准測試：啟動前的結構化稽核工作流程→[核准工作流程](#approval-workflows-for-journeys-and-campaigns)

**依據內容的金鑰功能：**

| 功能 | 套用至 | 頻道限制 | 先決條件 | 主要用途 |
|------------|-----------|---------------------|--------------|-----------------|
| [測試輪廓](../using/content-management/test-profiles.md) | 行銷活動、歷程 | 所有管道 | 已建立測試設定檔 | 預覽個人化內容 |
| [範例輸入資料](../using/test-approve/simulate-sample-input.md) | 行銷活動、歷程 | 電子郵件、簡訊、推播、網頁、程式碼、應用程式內、內容卡 | CSV/JSON檔案 | 測試多個個人化變體 |
| [測試模式](../using/building-journeys/testing-the-journey.md) | 僅限歷程 | 不適用 | 草稿歷程，已設定名稱空間 | 模擬設定檔進度 |
| [試用](../using/building-journeys/journey-dry-run.md) | 僅限歷程 | 不適用 | 歷程已建立 | 分析執行路徑 |
| [電子郵件呈現](../using/content-management/rendering.md) | 行銷活動、歷程 | 僅限電子郵件 | Litmus整合 | 驗證跨使用者端的顯示 |
| [垃圾郵件分數](../using/content-management/spam-report.md) | 行銷活動、歷程 | 僅限電子郵件 | None | 傳遞能力驗證 |
| [種子清單](../using/configuration/seed-lists.md) | 行銷活動、歷程 | 僅限電子郵件 | 種子清單已設定 | 利害關係人監控 |
| [內容實驗](../using/content-management/get-started-experiment.md) | 僅限行銷活動 | 所有管道 | None | A/B和多臂吃角子老虎機測試 |
| [衝突偵測](../using/conflict-prioritization/conflicts.md) | 行銷活動、歷程（受限） | 所有管道 | None | 防止客戶過度傳送訊息 |
| [核准工作流程](../using/test-approve/gs-approval.md) | 行銷活動、歷程 | 所有管道 | 核准原則已建立 | 結構化稽核流程 |
| [Personalization遊樂場](../using/personalization/personalize.md#playground) | 全部 | 所有管道 | None | 瞭解並測試個人化語法 |

**常見測試工作流程：**

1. 預先開發：使用[個人化遊樂場](#testing-personalization)學習語法
2. 開發期間：使用[測試設定檔](#testing-campaigns)預覽，使用[範例輸入資料](#simulate-content-variations)驗證
3. 啟動前：執行[技術測試](#2-technical-validation) （轉譯，垃圾郵件），檢查[衝突](#conflict-detection)，提交以取得[核准](#approval-workflows-for-journeys-and-campaigns)
4. 啟動後：使用即時報告進行監視（請參閱[監視和疑難排解](#monitoring--troubleshooting)），根據結果迭代


## 重要術語

**[測試設定檔](../using/content-management/test-profiles.md)** =用於預覽個人化內容的綜合客戶設定檔（不是真正的客戶）。 在即時客戶個人檔案服務中標幟。 測試模式和內容預覽的必要專案。 [瞭解如何建立測試設定檔](../using/audience/creating-test-profiles.md)

**[測試模式](../using/building-journeys/testing-the-journey.md)** =透過歷程路徑傳送測試設定檔的歷程模擬功能。 限制：僅草稿歷程，需要名稱空間，僅測試設定檔。 [請參閱測試模式檔案](../using/building-journeys/testing-the-journey.md)

**[練習](../using/building-journeys/journey-dry-run.md)** =追蹤路徑而不傳送訊息或進行API呼叫的歷程執行分析工具。 使用案例：驗證邏輯而不佔用資源。 [了解試用](../using/building-journeys/journey-dry-run.md)

**[範例輸入資料](../using/test-approve/simulate-sample-input.md)** =包含測試個人化之設定檔屬性值的CSV或JSON檔案。 最多可支援30種變體。 建立測試設定檔的替代方法。 [如何模擬內容變化](../using/test-approve/simulate-sample-input.md)

**[種子清單](../using/configuration/seed-lists.md)** =實際傳送（而非測試傳送）中自動包含內部利害關係人的電子郵件地址。 僅限電子郵件頻道。 使用案例：品質監控與法規遵循。 [設定種子清單](../using/configuration/seed-lists.md)

**[內容實驗](../using/content-management/get-started-experiment.md)** = A/B測試或比較內容變化的多臂吃角子老虎機實驗。 僅限行銷活動，不適用於歷程。 [開始使用實驗](../using/content-management/get-started-experiment.md) | [建立實驗](../using/content-management/content-experiment.md)

**[校樣](../using/content-management/proofs.md)** =使用測試設定檔資料測試傳送至特定電子郵件地址的電子郵件傳遞。 與種子清單（校樣是手動測試傳送，種子清單是利害關係人的自動副本）不同。 [傳送校樣](../using/content-management/proofs.md)

**[衝突偵測](../using/conflict-prioritization/conflicts.md)** =可識別針對相同對象之重疊行銷活動和歷程的工具。 有限歷程支援：單一、對象資格和讀取對象型別。 [瞭解衝突管理](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[核准工作流程](../using/test-approve/gs-approval.md)** =啟動前需要利害關係人核准的多步驟稽核程式。 需要核准原則設定。 [設定核准](../using/test-approve/gs-approval.md) | [建立原則](../using/test-approve/approval-policies.md)

**[呈現測試](../using/content-management/rendering.md)** =跨電子郵件使用者端(Gmail、Outlook、Apple Mail)和裝置的電子郵件顯示驗證。 需要Litmus整合。 [測試電子郵件呈現](../using/content-management/rendering.md)

**[Personalization playground](../using/personalization/personalize.md#playground)** =互動式學習環境，使用個人化語法進行實驗，並使用範例資料測試運算式。 不需要即時資料集。 [存取遊樂場](../using/personalization/personalize.md#playground)

## 測試方法選擇的決策樹

使用此決策樹快速識別適合您特定情境的測試工具。 根據您的內容（您正在建置的內容、需要驗證的內容以及您使用的頻道）回答每個問題，以直接導覽至相關功能和檔案。

+++ **問題1：您正在測試哪些專案？**

* 行銷活動→ [測試行銷活動](#testing-campaigns)
* 歷程→ [測試歷程](#testing-journeys)
* [Personalization遊樂場](#testing-personalization)→的Personalization運算式
+++

+++**問題2：哪些方面需要驗證？**

* [測試設定檔](#testing-campaigns)或[範例輸入資料](#simulate-content-variations)→的內容和個人化
* 電子郵件顯示→[電子郵件轉譯測試](#2-technical-validation)
* 傳遞能力→[垃圾郵件分數檢查](#2-technical-validation)
* [測試模式](#testing-journeys)或[→試](#journey-dry-run)的歷程邏輯和流程
* [內容實驗](#content-experiments--ab-testing)→效能比較（僅限行銷活動）
* 時間衝突→[衝突偵測](#conflict-detection)
* 利害關係人檢閱[核准→作流程](#approval-workflows-for-journeys-and-campaigns)
+++

+++**問題3：哪個頻道？**

* 電子郵件→所有可用的測試方法（請參閱[測試行銷活動](#testing-campaigns)）
* SMS、推播→[內容測試](#testing-campaigns)、[範例輸入資料](#simulate-content-variations)、[核准工作流程](#approval-workflows-for-journeys-and-campaigns)
* Web、應用程式內、程式碼型→[內容測試](#testing-campaigns)、[範例輸入資料](#simulate-content-variations)、[核准工作流程](#approval-workflows-for-journeys-and-campaigns)
* 多個管道→分別測試每個管道
+++

+++**問題4：何時在工作流程中？**

* 建→[Personalization遊樂場](#personalization-playground)之前，請先進行學習
* 在建置→[測試設定檔](#testing-campaigns)和[範例輸入資料](#simulate-content-variations)以進行驗證期間
* 啟動之前→[呈現測試](#2-technical-validation)，[垃圾郵件檢查](#email-spam-report)，[衝突偵測](#conflict-detection)，[核准](#approval-workflows-for-journeys-and-campaigns)
* 啟動[→時報告](../using/building-journeys/report-journey.md)和[監視](#monitoring--troubleshooting)後
+++


## 選擇測試方法

正確的測試方法取決於您建置的內容以及需要驗證的內容。 使用本指南針對您的案例找出最相關的測試工具。

>[!BEGINTABS]

>[!TAB 測試行銷活動]

**對於所有行銷活動：**

* 使用[測試設定檔](../using/content-management/test-profiles.md)或[範例輸入資料](../using/test-approve/simulate-sample-input.md)預覽及測試內容
* 檢查跨裝置和使用者端的[電子郵件呈現](../using/content-management/rendering.md) （僅限電子郵件通道）
* 執行[垃圾郵件分數檢查](../using/content-management/spam-report.md) （僅限電子郵件通道）
* 檢閱[與其他行銷活動和歷程的衝突](../using/conflict-prioritization/conflicts.md)
* 設定[種子清單](../using/configuration/seed-lists.md)以監視利害關係人（僅限電子郵件管道）
* 啟動前提交以進行[核准](../using/test-approve/gs-approval.md)

**用於A/B測試和最佳化：**

* 建立[內容實驗](../using/content-management/get-started-experiment.md)以測試多個處理方式並測量效能

**對於API觸發的行銷活動：**

* 使用[Campaign模擬API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}以程式設計方式觸發校訂工作

>[!TAB 正在測試歷程]

所有歷程的&#x200B;**：**

* 使用[測試模式](../using/building-journeys/testing-the-journey.md)來模擬設定檔進度（僅草稿歷程，需要名稱空間）或[試執行](../using/building-journeys/journey-dry-run.md)來分析執行路徑而不傳送訊息
* 使用[預覽和校樣](../using/content-management/preview-test.md)測試個別訊息
* 檢查[與其他歷程和行銷活動衝突](../using/conflict-prioritization/conflicts.md)
* 發佈前提交[核准](../using/test-approve/gs-approval.md)

**對於複雜歷程：**

* 使用測試模式並一起練習以徹底驗證分支邏輯和執行路徑
* 系統地測試不同的輸入條件和設定檔屬性

**注意：**&#x200B;衝突偵測和歷程上限僅適用於單一、對象資格和讀取對象歷程。

>[!TAB 測試個人化]

**建置內容之前：**

* 在[個人化遊樂場](../using/personalization/personalize.md#playground)中進行實驗，以學習語法和使用範例資料測試運算式

**內容建立期間：**

* 使用[測試設定檔](../using/content-management/test-profiles.md)預覽，以驗證個人化轉譯器是否正確
* 使用CSV/JSON檔案中的[範例輸入資料](../using/test-approve/simulate-sample-input.md)測試多個案例（支援最多30種變體）

>[!ENDTABS]

## 測試最佳實務

若要讓測試工作獲得最大成效，請遵循下列建議作法：

1. **及早測試，且通常為** — 請勿等候行銷活動完全建置。 在開發時以漸進方式測試內容、個人化和邏輯。

1. **使用逼真的測試設定檔** - [建立可準確代表目標受眾區段的測試設定檔](../using/audience/creating-test-profiles.md)，包括邊緣案例和不同的個人化案例。

1. **跨裝置和使用者端測試** — 驗證常用電子郵件使用者端(Gmail、Outlook、Apple Mail)和裝置（桌上型電腦、行動裝置、平板電腦）上的[電子郵件呈現](../using/content-management/rendering.md)，以確保顯示的一致性（僅限電子郵件頻道）。

1. **徹底驗證個人化** — 使用多個[具有不同屬性值的測試設定檔](../using/content-management/test-profiles.md)進行測試，以確認個人化權杖正確轉譯且遞補值有效。 使用[個人化遊樂場](../using/personalization/personalize.md#playground)，嘗試使用個人化運算式，並使用範例資料測試程式碼，然後再將其套用至您的行銷活動。

1. **使用範例資料測試內容變異** — 使用CSV或JSON檔案中的[範例輸入資料](../using/test-approve/simulate-sample-input.md)來測試最多30個個人化案例，而不需要建立許多測試設定檔，可節省時間並確保完整的涵蓋範圍。 支援電子郵件、簡訊、推播、網頁、程式碼型體驗、應用程式內和內容卡頻道。

1. **使用種子清單進行利害關係人監控** — 設定[種子清單](../using/configuration/seed-lists.md)以自動包含內部利害關係人，在執行階段這些利害關係人將收到所有傳遞的復本，以進行品質監控和合規性驗證（僅限電子郵件管道）。

1. **模擬歷程路徑** — 對於具有多個分支的複雜歷程，請使用[測試模式](../using/building-journeys/testing-the-journey.md)測試不同的進入條件和設定檔屬性，以驗證所有可能的路徑。 適用於使用名稱空間的草稿歷程。

1. **檢查傳遞能力指標** — 先檢閱[垃圾郵件分數](../using/content-management/spam-report.md)、驗證狀態和電子郵件健康狀態量度，再進行大量傳送（僅限電子郵件通道）。

1. **記錄測試結果** — 記錄測試結果、發現的問題和解決方案，以改進未來的測試程式，並與團隊分享學習經驗。

1. **及早讓利害關係人參與** — 在[正式核准](../using/test-approve/gs-approval.md)之前，與利害關係人分享預覽和測試結果，以收集意見並協調期望。

## 建議的測試工作流程

遵循此系統化方法，確保進行徹底測試並順利核准：

### 1.內容開發與預覽

首先，請建立您的內容，並使用預覽功能來驗證初始設計和個人化：

* 設計您的[電子郵件](../using/email/create-email.md)、[簡訊](../using/sms/create-sms.md)、[推播通知](../using/push/create-push.md)或其他頻道內容

* 使用&#x200B;**[模擬內容](../using/content-management/preview-test.md)**&#x200B;功能，以使用測試設定檔預覽

* 檢查[個人化權杖](../using/personalization/personalization-syntax.md)、動態內容和遞補值

* 在&#x200B;**[個人化遊樂場](../using/personalization/personalize.md#playground)**&#x200B;中嘗試個人化運算式，以使用範例資料測試和調整您的程式碼，然後再套用至即時內容

* 使用CSV/JSON檔案中的&#x200B;**[範例輸入資料](../using/test-approve/simulate-sample-input.md)**&#x200B;測試多個變數，以驗證各種設定檔案例中的個人化

* 驗證不同熒幕大小和電子郵件使用者端的[呈現](../using/content-management/rendering.md)

### 2.技術驗證

驗證影響傳遞能力與功能的技術層面：

* 執行[垃圾郵件分數檢查](../using/content-management/spam-report.md)以識別潛在傳遞能力問題

* 測試連結，確保連結未中斷並正確追蹤

* 驗證[電子郵件驗證](../using/configuration/dmarc-record.md) (SPF、DKIM、DMARC)設定

* 檢閱HTML演算，並檢查CSS相容性問題

* 在行動裝置和案頭裝置上測試[回應式設計](../using/email/content-from-scratch.md)

* 檢查與其他行銷活動和歷程的[潛在衝突](../using/conflict-prioritization/conflicts.md)，以防止客戶訊息疲勞和時間問題

### 3.歷程測試（僅限歷程）

如果您正在測試歷程，請驗證協調邏輯：

* 啟動&#x200B;**[測試模式](../using/building-journeys/testing-the-journey.md)**&#x200B;以模擬歷程中的設定檔進度

* 測試不同的[進入條件](../using/building-journeys/entry-management.md)和對象資格

* 驗證[等待活動](../using/building-journeys/wait-activity.md)、[條件](../using/building-journeys/condition-activity.md)和分支邏輯是否正確運作

* 使用複雜歷程的&#x200B;**[練習](../using/building-journeys/journey-dry-run.md)**&#x200B;來分析執行路徑而不傳送訊息

* 檢查[事件](../using/event/about-events.md)是否正確觸發，以及[自訂動作](../using/action/about-custom-action-configuration.md)是否如預期般執行

### 4.核准提交

測試完成且問題解決後：

* 根據您組織的[核准原則](../using/test-approve/approval-policies.md)提交行銷活動或歷程以進行核准

* 在[核准要求](../using/test-approve/request-approval.md)中包含測試結果和檔案

* 處理[核准者](../using/test-approve/review-approve-request.md)的任何意見回饋或變更要求

* 進行必要的修訂，若有重大變更則重新測試

### 5.啟動前驗證

在啟用您的行銷活動或歷程之前：

* 對所有設定、對象和[排程執行最終稽核](../using/building-journeys/journey-properties.md)

* 確認所有核准都已就緒且已記錄

* 確認傳送時間和[時區](../using/building-journeys/timezone-management.md)是否正確

* 啟用[監視和警示](../using/reports/alerts.md)以追蹤啟動後的效能

### 6.監視與重複

啟動後，請繼續監視以及早發現任何問題：

* 針對歷程錯誤、高跳出率或低參與度設定[系統警示](../using/reports/alerts.md)

* 檢閱[即時報告](../using/building-journeys/report-journey.md)以追蹤績效是否符合預期

* 如果發生嚴重問題，請準備[暫停或修改](../using/building-journeys/journey-pause.md)個歷程

* 記錄吸取的經驗教訓，以改進未來的測試流程

## 實際測試：使用案例

瞭解測試概念如何套用至真實世界的情境：

| 使用案例 | 您將瞭解的內容 | 關鍵測試焦點 |
|----------|-------------------|-------------------|
| **[傳送多頻道訊息](../using/building-journeys/journeys-uc.md)** | 測試結合讀取對象、反應事件和電子郵件/推播訊息的歷程。 驗證從受眾目標定位到訊息傳送的整個流程。 | 多管道協調、反應事件、端對端流程驗證、測試和發佈步驟 |
| **[傳送訊息給訂閱者](../using/building-journeys/message-to-subscribers-uc.md)** | 使用動態電子郵件位址測試目標訂閱清單的歷程。 驗證個人化運算式以找出正確的訂閱者目標。 | Personalization運算式，動態定址，訂閱清單目標定位 |
| **[傳送時間限制訊息](../using/building-journeys/weekday-email-uc.md)** | 使用以時間為基礎的條件測試歷程，以確保訊息在特定日期傳送。 驗證等待活動和排程邏輯。 | 以時間為基礎的條件、等待活動、排程驗證 |
| **[探索更多歷程使用案例](../using/building-journeys/jo-use-cases.md)** | 存取涵蓋體驗事件、多頻道傳訊和外部系統整合的全方位實用範例集合。 | 各種情境、進階模式、整合測試 |

## 測試並核准內容

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

預覽、測試和驗證內容

了解如何使用測試輪廓、電子郵件呈現測試、垃圾郵件分數評估等，來預覽、測試和驗證個人化內容。

[探索預覽與測試內容](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

歷程與行銷活動的核准工作流程

了解如何設定、管理及執行核准流程，以確保歷程及行銷活動的品質控制。

[了解核准工作流程](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

測試您的歷程

使用特定設定檔進行測試以在發佈前驗證您的歷程，以確保事件、條件和動作如預期般運作。 適用於使用名稱空間的草稿歷程。

[測試您的歷程](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

歷程試運行

執行試運行以模擬和驗證您的歷程的執行路徑，在上線之前識別潛在問題。

[了解歷程試運行](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

監視與疑難排解

存取全面的疑難排解資源、系統警示和錯誤代碼，以解決歷程執行和績效問題。

[檢視監視與疑難排解](troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

Personalization遊樂場

在安全環境中實驗個人化運算式。 將範例資料與預覽結果套用至您的行銷活動和歷程之前，請先測試程式碼。

[瞭解Personalization Playground](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/data.svg)

內容實驗和A/B測試

透過測試多個內容變異和測量效能以識別績效最佳的處理，最佳化您的行銷活動。 僅適用於行銷活動（支援A/B和多臂吃角子老虎機實驗）。

[瞭解內容實驗](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

利害關係人監控的種子清單

在傳遞中自動納入內部利害關係人地址，以監控傳送給客戶的實際訊息，以確保品質和法規遵循。 僅適用於電子郵件頻道。

[設定種子清單](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

衝突偵測

識別行銷活動和歷程之間的潛在重疊，以防止客戶無法同時進行太多通訊。 適用於行銷活動和單一、對象資格和讀取對象歷程。

[偵測衝突](../using/conflict-prioritization/conflicts.md)
:::

::::

## 其他資源

### 基本測試和驗證指南

* [模擬內容變化](../using/test-approve/simulate-sample-input.md) — 使用CSV或JSON檔案測試最多30個個人化案例。 不須建立多個測試設定檔即可進行多語言內容測試的理想選擇。 支援電子郵件、簡訊、推播、網頁、程式碼、應用程式內和內容卡。

* [建立測試設定檔](../using/audience/creating-test-profiles.md) — 建立和管理測試設定檔以模擬客戶案例。 瞭解如何標幟設定檔以進行測試、設定屬性以及組織測試區段。

* [電子郵件垃圾郵件報告](../using/content-management/spam-report.md) — 在傳送前檢查垃圾郵件分數，以改善傳遞能力及收件匣位置。 取得內容最佳化的可操作建議。

* [歷程常見問題集](../using/building-journeys/journey-faq.md) — 關於歷程測試、執行和疑難排解的常見問題快速參考。

<!-- ### Dependencies and relationships

Understand how testing capabilities connect to each other and to your broader Journey Optimizer workflows. This section maps prerequisites, upstream/downstream dependencies, and common capability combinations.

+++**Prerequisites (required before testing)**

* Test profiles must be created before using test mode or content preview
* Approval policies must be configured before submitting for approval
* Seed lists must be created before adding to campaigns/journeys
* Litmus integration required for email rendering tests
* Journey must be in draft status to use test mode
* Journey must have namespace configured to use test mode

+++

+++**What testing depends on (upstream)**

* Content creation: Need campaigns or journeys to test
* Test profiles: Required for test mode and content preview
* Approval policies: Required for approval workflows
* Configuration: Channel configurations, email authentication, domain settings

+++

+++**What depends on testing (downstream)**

* Campaign/journey activation: Cannot activate without resolving errors
* Publishing: Approval may be required before publishing
* Live monitoring: Post-launch monitoring and reporting
* Optimization: Use test results to refine future campaigns

+++

+++**Related capabilities**

* Testing + Approval workflows = Quality assurance process
* Testing + Conflict detection = Preventing customer over-messaging
* Testing + Content experiments = Performance optimization
* Testing + Reporting = Continuous improvement cycle
* Test profiles + Personalization = Content validation
* Dry run + Test mode = Comprehensive journey validation

+++

+++**Common capability combinations**

* Content testing: Test profiles + Sample input data + Personalization playground
* Email validation: Rendering tests + Spam scores + Test profiles + Proofs
* Journey validation: Test mode + Dry run + Test profiles
* Pre-launch checklist: All technical tests + Conflict detection + Approval workflows

+++
-->

### 常見問題

+++**問：啟動行銷活動之前需要哪些測試？**

**最小值：**包含測試設定檔的內容預覽+垃圾郵件分數檢查（電子郵件）
**建議：** +電子郵件呈現+衝突偵測+核准工作流程
**最佳實務：** +範例輸入資料測試+種子清單+ A/B實驗（如果最佳化）

+++

+++**問：如何測試個人化而不建立許多測試設定檔？**

**主要解決方案：**&#x200B;使用[範例輸入資料](../using/test-approve/simulate-sample-input.md)搭配CSV/JSON檔案（支援最多30種變體）
**替代方案：**&#x200B;建立3-5個代表性的[測試設定檔](../using/audience/creating-test-profiles.md)，涵蓋主要區段
**學習工具：**&#x200B;個人化遊樂場[中的](../using/personalization/personalize.md#playground)實驗優先

+++

+++**問：歷程的測試模式與試執行之間有何差異？**

**測試模式：**透過歷程傳送測試設定檔、觸發實際動作、產生測試訊息。 需要草稿歷程+名稱空間。
**試執行：**追蹤執行路徑而不傳送任何內容。 適用於任何歷程狀態。 未傳送任何訊息，未執行任何動作。
**搭配使用：**&#x200B;訊息測試的測試模式+邏輯驗證的試用=全面涵蓋範圍。

+++

+++**問：我可以在生產/即時狀態中測試歷程嗎？**

**測試模式：**否 — 僅草稿歷程
**練習：**是 — 適用於任何歷程狀態
**內容預覽：**是 — 隨時預覽個別訊息
**因應措施：**&#x200B;重複的即時歷程以草稿進行完整測試模式驗證

+++

+++**問：哪些測試功能需要外部整合？**

**電子郵件呈現：**需要Litmus整合（個別授權）
**其他所有專案：**內建至Journey Optimizer，不需要其他整合
**注意：**&#x200B;測試設定檔需要即時客戶設定檔服務（包含）

+++

+++**問：如何測試API觸發的行銷活動？**

**選項1：**&#x200B;使用[促銷活動模擬API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}進行程式設計測試
**選項2：**在UI中使用測試設定檔預覽內容
**選項3：**傳送校樣以測試電子郵件地址
**最佳實務：**&#x200B;結合所有這三項以進行全面驗證

+++

