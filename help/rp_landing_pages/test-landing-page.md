---
solution: Journey Optimizer
product: Journey Optimizer
title: 測試並核准
description: 測試並核准
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: dd3d91266c0edea562f75ceb1f75974c7242ee1a
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 11%

---

# 測試並核准{#section-overview}

品質保證對於提供卓越的客戶體驗至關重要。 Adobe Journey Optimizer提供全方位的測試和核准功能，協助您驗證內容、驗證歷程邏輯，並確保行銷活動在觸及對象之前符合品質標準。 從使用測試設定檔預覽個人化訊息，到模擬複雜的歷程流程，這些工具可讓您及早識別和解決問題、降低風險，並維護品牌完整性。 無論您是要測試跨裝置的電子郵件呈現、驗證多步驟歷程或建立正式核准工作流程，本節將引導您瞭解最佳實務和逐步程式，以建立對行銷活動和歷程的信心。 透過實作徹底的測試和結構化核准，您將最小化錯誤、改善傳遞能力，並建立與客戶引起共鳴的順暢體驗。

## 為什麼測試和核准很重要

測試和核准程式是重要的品質閘道，可保護您的品牌聲譽並確保行銷活動取得成功。 以下是它們之所以重要的原因：

* **在錯誤到達客戶之前即發現錯誤** — 在快速且無風險的修正受控環境中，識別中斷的連結、不正確的個人化、轉譯問題和邏輯錯誤。

* **改善傳遞能力** — 測試垃圾郵件分數、驗證電子郵件驗證，以及檢查跨電子郵件使用者端的轉譯，以最大化收件匣位置和參與率。

* **確保品牌一致性** — 預覽包含不同測試設定檔的內容，以驗證各種客戶區段可正確顯示個人化，並維護品牌標準。

* **驗證複雜的歷程** — 模擬多步驟歷程流程，以確認觸發器是否正確引發、條件是否正確評估，以及客戶是否會在正確的時間收到正確的訊息。

* **建立責任制** — 實作需要利害關係人簽署的正式核准工作流程，建立明確的所有權，並減少未經授權或過早啟動的行銷活動。

* **節省時間和資源** — 在開發週期中及早偵測問題，因為修正更便宜、更快速，避免在啟動後進行代價高昂的更正或客戶服務升級。

## 測試最佳實務

若要讓測試工作獲得最大成效，請遵循下列建議作法：

1. **及早測試，且通常為** — 請勿等候行銷活動完全建置。 在開發時以漸進方式測試內容、個人化和邏輯。

1. **使用逼真的測試設定檔** - [建立可準確代表目標受眾區段的測試設定檔](../using/audience/creating-test-profiles.md)，包括邊緣案例和不同的個人化案例。

1. **跨裝置和使用者端測試** — 驗證常用電子郵件使用者端(Gmail、Outlook、Apple Mail)和裝置（桌上型電腦、行動裝置、平板電腦）上的[電子郵件呈現](../using/content-management/rendering.md)，以確保顯示的一致性。

1. **徹底驗證個人化** — 使用多個[具有不同屬性值的測試設定檔](../using/content-management/test-profiles.md)進行測試，以確認個人化權杖正確轉譯且遞補值有效。

1. **模擬歷程路徑** — 對於具有多個分支的複雜歷程，請使用[測試模式](../using/building-journeys/testing-the-journey.md)測試不同的進入條件和設定檔屬性，以驗證所有可能的路徑。

1. **檢查傳遞能力指標** — 在大型傳送之前先檢閱[垃圾郵件分數](../using/content-management/spam-report.md)、驗證狀態和電子郵件健康狀態量度。

1. **記錄測試結果** — 記錄測試結果、發現的問題和解決方案，以改進未來的測試程式，並與團隊分享學習經驗。

1. **及早讓利害關係人參與** — 在[正式核准](../using/test-approve/gs-approval.md)之前，與利害關係人分享預覽和測試結果，以收集意見並協調期望。

## 建議的測試工作流程

遵循此系統化方法，確保進行徹底測試並順利核准：

### 1.內容開發與預覽

首先，請建立您的內容，並使用預覽功能來驗證初始設計和個人化：

* 設計您的[電子郵件](../using/email/create-email.md)、[簡訊](../using/sms/create-sms.md)、[推播通知](../using/push/create-push.md)或其他頻道內容
* 使用&#x200B;**[模擬內容](../using/content-management/preview-test.md)**&#x200B;功能，以使用測試設定檔預覽
* 檢查[個人化權杖](../using/personalization/personalization-syntax.md)、動態內容和遞補值
* 驗證不同熒幕大小和電子郵件使用者端的[呈現](../using/content-management/rendering.md)

### 2.技術驗證

驗證影響傳遞能力與功能的技術層面：

* 執行[垃圾郵件分數檢查](../using/content-management/spam-report.md)以識別潛在傳遞能力問題
* 測試連結，確保連結未中斷並正確追蹤
* 驗證[電子郵件驗證](../using/configuration/dmarc-record.md) (SPF、DKIM、DMARC)設定
* 檢閱HTML演算，並檢查CSS相容性問題
* 在行動裝置和案頭裝置上測試[回應式設計](../using/email/content-from-scratch.md)

### 3.歷程測試

針對歷程，驗證協調邏輯：

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

* **[傳送多頻道訊息](../using/building-journeys/journeys-uc.md)** — 此使用案例示範如何測試結合讀取對象、回應事件和電子郵件/推播訊息的歷程。 瞭解如何驗證從受眾目標定位到訊息傳送的整個流程，並檢視測試和發佈步驟的實際運作。

* **[傳送訊息給訂閱者](../using/building-journeys/message-to-subscribers-uc.md)** — 探索如何使用動態電子郵件位址測試該目標訂閱清單的歷程。 此範例說明如何驗證個人化運算式，並確保訊息送達正確的訂閱者。

* **[傳送時間限制訊息](../using/building-journeys/weekday-email-uc.md)** — 瞭解如何使用時間條件來測試歷程，以確保訊息在特定日期傳送。 瞭解如何驗證等待活動和排程邏輯。

* **[探索更多歷程使用案例](../using/building-journeys/jo-use-cases.md)** — 存取涵蓋體驗事件、多頻道傳訊和外部系統整合的完整實用範例集合。

## 測試並核准內容

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hant)

預覽、測試和驗證內容

了解如何使用測試輪廓、電子郵件呈現測試、垃圾郵件分數評估等，來預覽、測試和驗證個人化內容。

[探索預覽與測試內容](preview-test-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hant)

歷程與行銷活動的核准工作流程

了解如何設定、管理及執行核准流程，以確保歷程及行銷活動的品質控制。

[了解核准工作流程](approve-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hant)

測試您的歷程

使用特定輪廓進行測試以在發佈前驗證您的歷程，以確保事件、條件和動作如預期般運作。

[測試您的歷程](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hant)

歷程試運行

執行試運行以模擬和驗證您的歷程的執行路徑，在上線之前識別潛在問題。

[了解歷程試運行](../using/building-journeys/journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hant)

監視與疑難排解

存取全面的疑難排解資源、系統警示和錯誤代碼，以解決歷程執行和績效問題。

[檢視監視與疑難排解](troubleshoot-journey-landing-page.md)
:::

::::

## 其他資源

### 基本測試和驗證指南

* [您的歷程中的即時報告](../using/building-journeys/report-journey.md) — 即時監視歷程量度，以追蹤效能並識別執行期間的問題。 存取設定檔進度、事件觸發器和動作完成率的詳細劃分。

* [建立測試設定檔](../using/audience/creating-test-profiles.md) — 建立和管理測試設定檔，以模擬真實的客戶案例，並驗證個人化。 瞭解如何標幟要測試的設定檔、設定屬性值以及組織測試設定檔區段。

* [電子郵件垃圾郵件報告](../using/content-management/spam-report.md) — 在傳送前檢查您的電子郵件垃圾郵件分數，以改善傳遞能力及收件匣位置。 瞭解垃圾郵件篩選器如何評估您的內容並獲得改進建議。

* [歷程常見問題集](../using/building-journeys/journey-faq.md) — 尋找有關歷程建立、測試、執行和疑難排解的常見問題解答。 解決常見問題並瞭解歷程行為的快速參考。

### 相關主題

* [內容管理](content-management-landing-page.md) — 瞭解如何使用範本、片段和電子郵件Designer來設計、預覽和管理內容。 品牌一致性的主要內容建立最佳實務。

* [Reporting &amp; Analytics](reporting-landing-page.md) — 使用完整的報告、控制面板和量度分析行銷活動和歷程績效。 進行資料導向式決策，以最佳化客戶體驗。

* [歷程設定](configure-journeys-landing-page.md) — 設定資料來源、事件和自訂動作，以啟用複雜的歷程協調。 為歷程建立建立技術基礎。

* [行銷活動管理](../using/campaigns/get-started-with-campaigns.md) — 探索不同的行銷活動型別，並瞭解如何建立、排程和最佳化批次和即時行銷活動，以獲得最大影響。
