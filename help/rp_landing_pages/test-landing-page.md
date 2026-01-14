---
solution: Journey Optimizer
product: Journey Optimizer
title: 測試、驗證及核准
description: 探索 Journey Optimizer 中的所有測試和核准功能。在啟動之前預覽內容、模擬歷程、驗證電子郵件、執行實驗、偵測衝突，以及設定核准工作流程。
feature: Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 測試、驗證、核准、品質保證、QA、測試輪廓、個人化、轉譯、垃圾郵件檢查、內容實驗、a/b 測試、衝突偵測、種子清單、校樣、範例資料、核准工作流程、電子郵件測試、驗證工作流程
redpen-status: CREATED_||_2025-08-11_20-30-59
exl-id: a770412f-2f80-459d-8cce-32212154d154
source-git-commit: c3535f39b351d671054031b9cc391bf6d9d83a09
workflow-type: ht
source-wordcount: '2328'
ht-degree: 100%

---

# 測試、驗證及核准{#section-overview}

本節涵蓋了 Journey Optimizer 中的所有測試和核准功能。您會找到工具來使用測試輪廓預覽內容、驗證歷程邏輯、檢查電子郵件轉譯和垃圾郵件分數、執行 A/B 實驗、偵測衝突，以及設定核准工作流程。

此登陸頁面可協助您根據正在建立的內容 (行銷活動與歷程) 選擇正確的測試方法，引導您完成建議的測試工作流程，並可讓您快速存取所有測試和核准資源。從[選擇下面的測試方法](#choose-your-testing-approach)開始，以識別哪些工具適用於您的使用案例。如需關鍵測試術語的定義，請參閱[關鍵術語](#key-terminology)。

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

使用特定輪廓進行測試以在發佈前驗證您的歷程，以確保事件、條件和動作如預期般運作。適用於使用命名空間的草稿歷程。

[測試您的歷程](../using/building-journeys/testing-the-journey.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

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

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code.svg)

個人化遊樂場

在安全環境中實驗個人化運算式。在套用至行銷活動和歷程之前，請使用範例資料測試程式碼並預覽結果。

[瞭解個人化遊樂場](../using/personalization/personalize.md#playground)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hant)

內容實驗和 A/B 測試

透過測試多個內容變化版本和測量績效以識別績效最佳的處理方式，最佳化您的行銷活動。僅適用於行銷活動 (支援 A/B 和多臂老虎機實驗)。

[瞭解內容實驗](../using/content-management/get-started-experiment.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

利害關係人監視的種子清單

在傳遞中自動納入內部利害關係人地址，監視傳送給客戶的實際訊息，以確保品質和合規性。僅適用於電子郵件管道。

[設定種子清單](../using/configuration/seed-lists.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg)

衝突偵測

識別行銷活動和歷程之間的潛在重疊，以防止同時向客戶傳送過多通訊。適用於行銷活動和單一、客群資格和閱讀客群歷程。

[偵測衝突](../using/conflict-prioritization/conflicts.md)
:::

::::

## 為什麼測試和核准很重要

測試和核准流程是重要的品質閘道，可保護您的品牌聲譽並確保行銷活動取得成功。以下是其重要的原因：

* **在錯誤到達客戶之前發現錯誤** - 在進行快速且無風險修正的受控環境中，識別中斷的連結、不正確的個人化、轉譯問題和邏輯錯誤。

* **改善傳遞能力** - 測試垃圾郵件分數、驗證電子郵件驗證，以及檢查跨電子郵件用戶端的轉譯，以最大限度地利用收件匣版位和提高參與率。

* **確保品牌一致性** - 預覽包含不同測試輪廓的內容，以驗證各種客戶區段是否正確顯示個人化，並維護品牌標準。

* **驗證複雜的歷程** - 模擬多步驟歷程流程，以確認觸發程序是否正確引發、條件是否正確評估，以及客戶是否會在正確的時間收到正確的訊息。

* **建立責任制** - 實作需要利害關係人簽核的正式核准工作流程，建立明確的所有權，並減少未經授權或過早啟動的行銷活動。

* **節省時間和資源** - 在開發週期中及早偵測問題，因為在此時進行修正更便宜、更快速，避免在啟動後進行代價高昂的更正或客戶服務升級。

<!--## Testing capabilities overview

**Testing types available:**

* Content testing: Preview and validate message content before sending → [Choose your testing approach](#choose-your-testing-approach)
* Journey logic testing: Simulate customer progression through journey paths → [Choose your testing approach](#choose-your-testing-approach)
* Technical testing: Validate rendering, deliverability, and authentication → [Technical validation](#2-technical-validation)
* Performance testing: Compare content variations using A/B experiments → [Content Experiments & A/B Testing](#test--approve-content)
* Conflict testing: Detect campaign and journey overlaps → [Conflict Detection](#test--approve-content)
* Approval testing: Structured review workflows before activation → [Approval Workflows](#test--approve-content)

**Key capabilities by context:**

| Capability | Applies to | Channel restrictions | Prerequisites | Primary purpose |
|------------|-----------|---------------------|--------------|-----------------|
| [Test profiles](../using/content-management/test-profiles.md) | Campaigns, Journeys | All channels | Test profiles created | Preview personalized content |
| [Sample input data](../using/test-approve/simulate-sample-input.md) | Campaigns, Journeys | Email, SMS, Push, Web, Code-based, In-app, Content cards | CSV/JSON file | Test multiple personalization variants |
| [Test mode](../using/building-journeys/testing-the-journey.md) | Journeys only | N/A | Draft journey, namespace configured | Simulate profile progression |
| [Dry run](../using/building-journeys/journey-dry-run.md) | Journeys only | N/A | Journey created | Analyze execution paths |
| [Email rendering](../using/content-management/rendering.md) | Campaigns, Journeys | Email only | Litmus integration | Verify display across clients |
| [Spam score](../using/content-management/spam-report.md) | Campaigns, Journeys | Email only | None | Deliverability validation |
| [Seed lists](../using/configuration/seed-lists.md) | Campaigns, Journeys | Email only | Seed list configured | Stakeholder monitoring |
| [Content experiments](../using/content-management/get-started-experiment.md) | Campaigns only | All channels | None | A/B and multi-armed bandit testing |
| [Conflict detection](../using/conflict-prioritization/conflicts.md) | Campaigns, Journeys (limited) | All channels | None | Prevent customer over-messaging |
| [Approval workflows](../using/test-approve/gs-approval.md) | Campaigns, Journeys | All channels | Approval policy created | Structured review process |
| [Personalization playground](../using/personalization/personalize.md#playground) | All | All channels | None | Learn and test personalization syntax |

**Common testing workflows:**

1. Pre-development: Use [personalization playground](#test--approve-content) to learn syntax
2. During development: Preview with [test profiles](#choose-your-testing-approach), validate with [sample input data](#choose-your-testing-approach)
3. Pre-launch: Run [technical tests](#2-technical-validation) (rendering, spam), check [conflicts](#test--approve-content), submit for [approval](#test--approve-content)
4. Post-launch: Monitor with live reports (see [Monitoring & Troubleshooting](#test--approve-content)), iterate based on results

-->

<!--
## Decision tree for testing method selection

Use this decision tree to quickly identify the right testing tools for your specific scenario. Answer each question based on your context (what you're building, what you need to validate, and which channel you're using) to navigate directly to the relevant capabilities and documentation.

+++ **Question 1: What are you testing?**

* Campaign → [Choose your testing approach](#choose-your-testing-approach)
* Journey → [Choose your testing approach](#choose-your-testing-approach)
* Personalization expressions → [Personalization playground](#test--approve-content)
+++

+++**Question 2: What aspect needs validation?**

* Content and personalization → [Test profiles](#choose-your-testing-approach) or [sample input data](#choose-your-testing-approach)
* Email display → [Email rendering tests](#2-technical-validation)
* Deliverability → [Spam score checks](#2-technical-validation)
* Journey logic and flow → [Test mode](#choose-your-testing-approach) or [dry run](#test--approve-content)
* Performance comparison → [Content experiment](#test--approve-content) (campaigns only)
* Timing conflicts → [Conflict detection](#test--approve-content)
* Stakeholder review → [Approval workflow](#test--approve-content)
+++

+++**Question 3: What channel?**

* Email → All testing methods available (see [Choose your testing approach](#choose-your-testing-approach))
* SMS, Push → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Web, In-app, Code-based → [Content testing](#choose-your-testing-approach), [sample input data](#choose-your-testing-approach), [approval workflows](#test--approve-content)
* Multiple channels → Test each channel separately
+++

+++**Question 4: When in the workflow?**

* Before building → [Personalization playground](#test--approve-content) for learning
* During building → [Test profiles](#choose-your-testing-approach) and [sample input data](#choose-your-testing-approach) for validation
* Before launch → [Rendering tests](#2-technical-validation), [spam checks](#2-technical-validation), [conflict detection](#test--approve-content), [approvals](#test--approve-content)
* After launch → [Live reports](../using/building-journeys/report-journey.md) and [monitoring](#test--approve-content)
+++

-->

## 選擇測試方法

正確的測試方法取決於您建立的內容以及需要驗證的內容。使用本指南針對您的案例找出最相關的測試工具。

>[!BEGINTABS]

>[!TAB 測試行銷活動]

**對於所有行銷活動：**

* 使用[測試輪廓](../using/content-management/test-profiles.md)或[範例輸入資料](../using/test-approve/simulate-sample-input.md)預覽及測試內容
* 檢查跨裝置和用戶端的[電子郵件轉譯](../using/content-management/rendering.md) (僅限電子郵管道)
* 執行[垃圾郵件分數檢查](../using/content-management/spam-report.md) (僅限電子郵件管道)
* 檢閱與其他行銷活動和歷程的[衝突](../using/conflict-prioritization/conflicts.md)
* 設定[種子清單](../using/configuration/seed-lists.md)以監視利害關係人 (僅限電子郵件管道)
* 啟用前提交以進行[核准](../using/test-approve/gs-approval.md)

**對於 A/B 測試和最佳化：**

* 建立[內容實驗](../using/content-management/get-started-experiment.md)以測試多個處理方式並測量績效

**對於 API 觸發的行銷活動：**

* 使用[行銷活動模擬 API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/) {target-&quot;_blank&quot;}，以程式設計方式觸發校訂工作

>[!TAB 測試歷程]

**對於所有歷程：**

* 使用[測試模式](../using/building-journeys/testing-the-journey.md)來模擬輪廓進度 (僅草稿歷程，需要命名空間) 或[試運行](../using/building-journeys/journey-dry-run.md)來分析執行路徑而不傳送訊息
* 使用[預覽和校樣](../using/content-management/preview-test.md)測試個別訊息
* 檢查與其他歷程和行銷活動的[衝突](../using/conflict-prioritization/conflicts.md)
* 發佈前提交以進行[核准](../using/test-approve/gs-approval.md)

**對於複雜歷程：**

* 使用測試模式並一起試運行，以徹底驗證分支邏輯和執行路徑
* 系統地測試不同的輸入條件和輪廓屬性

**注意：**&#x200B;衝突偵測和歷程上限僅適用於單一、客群資格和讀取客群歷程。

>[!TAB 測試個人化]

**建立內容之前：**

* 在[個人化遊樂場](../using/personalization/personalize.md#playground)中進行實驗，以學習語法和使用範例資料測試運算式

**內容建立期間：**

* 使用[測試輪廓](../using/content-management/test-profiles.md)預覽，以驗證個人化轉譯是否正確
* 使用 CSV/JSON 檔案中的[範例輸入資料](../using/test-approve/simulate-sample-input.md)測試多個案例 (支援最多 30 種變化版本)

>[!ENDTABS]

## 測試最佳做法

為了讓測試工作發揮最大的效用，請遵循以下建議做法：

1. **及早並經常測試** - 請勿等到行銷活動完全建立好再進行測試。在開發時以漸進方式測試內容、個人化和邏輯。

1. **使用逼真的測試輪廓** - [建立可準確代表目標客群區段的測試輪廓](../using/audience/creating-test-profiles.md)，包括邊緣案例和不同的個人化案例。

1. **跨裝置和用戶端測試** - 驗證常用電子郵件用戶端 (Gmail、Outlook、Apple Mail) 和裝置 (桌上型電腦、行動裝置、平板電腦) 上的[電子郵件轉譯](../using/content-management/rendering.md)，以確保顯示的一致性 (僅限電子郵件管道)。

1. **徹底驗證個人化** - 使用多個具有不同屬性值的[測試輪廓](../using/content-management/test-profiles.md)進行測試，以確認個人化權杖正確轉譯且遞補值有效。使用[個人化遊樂場](../using/personalization/personalize.md#playground)，實驗個人化運算式，並使用範例資料測試程式碼，然後再將其套用至您的行銷活動。

1. **使用範例資料測試內容變化版本** - 使用 CSV 或 JSON 檔案中的[範例輸入資料](../using/test-approve/simulate-sample-input.md)來測試最多 30 個個人化案例，而不需要建立許多測試輪廓，可節省時間並確保完整的涵蓋範圍。支援電子郵件、簡訊、推播、網頁、程式碼型體驗、應用程式內和內容卡管道。

1. **使用種子清單進行利害關係人監視** - 設定[種子清單](../using/configuration/seed-lists.md)以自動包含內部利害關係人，在執行階段這些利害關係人將收到所有傳遞的複本，以進行品質監視和合規性驗證 (僅限電子郵件管道)。

1. **模擬歷程路徑** - 對於具有多個分支的複雜歷程，請使用[測試模式](../using/building-journeys/testing-the-journey.md)測試不同的進入條件和輪廓屬性，以驗證所有可能的路徑。適用於使用命名空間的草稿歷程。

1. **檢查傳遞能力指標** - 先檢閱[垃圾郵件分數](../using/content-management/spam-report.md)、驗證狀態和電子郵件健康情況量度，再進行大量傳送 (僅限電子郵件管道)。

1. **記錄測試結果** - 記錄測試結果、發現的問題和解決方案，以改進未來的測試流程，並與團隊分享學習經驗。

1. **及早讓利害關係人參與** - 在[正式核准](../using/test-approve/gs-approval.md)之前，與利害關係人分享預覽和測試結果，以收集意見並協調期望。

## 建議的測試工作流程

在啟動之前，請依照此 4 階段方法，驗證您的行銷活動和歷程：

| 階段 | 測試內容 | 關鍵動作 |
|-------|-------------|-------------|
| **1. 內容驗證** | 個人化、設計、轉譯 | [使用測試輪廓預覽](../using/content-management/preview-test.md)、使用 CSV/JSON 測試[多個變化版本](../using/test-approve/simulate-sample-input.md)、驗證跨裝置的[轉譯](../using/content-management/rendering.md) |
| **2. 技術檢查** | 傳遞能力、連結、衝突 | 執行[垃圾郵件分數檢查](../using/content-management/spam-report.md)、驗證連結、檢查是否與其他行銷活動[衝突](../using/conflict-prioritization/conflicts.md) |
| **3.歷程邏輯** (僅限歷程) | 進入條件、流程、分支 | 使用[測試模式](../using/building-journeys/testing-the-journey.md)來模擬進度，針對複雜路徑執行[試運行](../using/building-journeys/journey-dry-run.md) |
| **4.啟動前** | 設定、核准、監視 | 提交以進行[核准](../using/test-approve/gs-approval.md)、驗證排程和客群、啟用[警示](../using/reports/alerts.md) |

**專業提示：**&#x200B;從[個人化遊樂場](../using/personalization/personalize.md#playground)開始，在建立內容之前先測試運算式，並一律在啟動之前檢查[衝突偵測](../using/conflict-prioritization/conflicts.md)，以防止過度傳訊。

## 實際測試：使用案例

瞭解測試概念如何套用至真實案例：

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/journeys-uc.md">
<img alt="傳送多管道訊息" src="../using/assets/do-not-localize/start-journey.jpeg">
</a>
<div>
<a href="../using/building-journeys/journeys-uc.md"><strong>傳送多管道訊息</strong></a>
</div>
<p>
測試結合讀取客群、回應事件和電子郵件/推播訊息的歷程。驗證從客群目標定位到訊息傳送的整個流程。專注於多管道協調、回應事件、端到端流程驗證和測試/發佈步驟。
</p>
</td>
<td>
<a href="../using/building-journeys/message-to-subscribers-uc.md">
<img alt="傳送訊息給訂閱者" src="../using/assets/do-not-localize/start-quick.png">
</a>
<div>
<a href="../using/building-journeys/message-to-subscribers-uc.md"><strong>傳送訊息給訂閱者</strong></a>
</div>
<p>
使用動態電子郵件位址測試定位訂閱清單的歷程。驗證個人化運算式以找出正確的訂閱者目標。著重於個人化運算式、動態定址和訂閱清單目標定位。
</p>
</td>
<td>
<a href="../using/building-journeys/weekday-email-uc.md">
<img alt="傳送時效性訊息" src="../using/assets/do-not-localize/calendar.jpeg">
</a>
<div>
<a href="../using/building-journeys/weekday-email-uc.md"><strong>傳送時效性訊息</strong></a>
</div>
<p>
使用以時間為基礎的條件測試歷程，以確保訊息在特定日期傳送。驗證等待活動和排程邏輯。著重於以時間為基礎的條件、等待活動和排程驗證。
</p>
</td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../using/building-journeys/jo-use-cases.md">
<img alt="探索更多歷程使用案例" src="../using/assets/do-not-localize/icon-quick-start.svg">
</a>
<div>
<a href="../using/building-journeys/jo-use-cases.md"><strong>探索更多歷程使用案例</strong></a>
</div>
<p>
存取涵蓋體驗事件、多管道傳訊和外部系統整合的全方位實用範例集合。探索各種案例、進階模式和整合測試方法。
</p>
</td>
</tr></table>

## 重要術語

熟悉這些基本的測試概念，以便更加瞭解 Journey Optimizer 的測試和核准功能。每個詞語都連結到詳細文件。

**[測試輪廓](../using/content-management/test-profiles.md)** - 用於預覽個人化內容的綜合客戶輪廓 (不是真正的客戶)。在即時客戶輪廓服務中標記。測試模式和內容預覽的必需項[瞭解如何建立測試輪廓](../using/audience/creating-test-profiles.md)

**[測試模式](../using/building-journeys/testing-the-journey.md)** - 透過歷程路徑傳送測試輪廓的歷程模擬功能。限制：僅限草稿歷程，需要命名空間，僅限測試輪廓。[參閱測試模式文件](../using/building-journeys/testing-the-journey.md)

**[試運行](../using/building-journeys/journey-dry-run.md)** - 追蹤路徑而不傳送訊息或進行 API 呼叫的歷程執行分析工具。使用案例：驗證邏輯而不佔用資源。[瞭解試運行](../using/building-journeys/journey-dry-run.md)

**[範例輸入資料](../using/test-approve/simulate-sample-input.md)** - 包含測試個人化之輪廓屬性值的 CSV 或 JSON 檔案。最多可支援 30 種變化版本。建立測試輪廓的替代方法。[如何模擬內容變化版本](../using/test-approve/simulate-sample-input.md)

**[種子清單](../using/configuration/seed-lists.md)** - 實際傳遞 (而非測試傳送) 中自動包含的內部利害關係人電子郵件地址。僅限電子郵件管道。使用案例：品質監視與合規性。[設定種子清單](../using/configuration/seed-lists.md)

**[內容實驗](../using/content-management/get-started-experiment.md)** - 比較內容變化版本的 A/B 測試或多臂老虎機實驗。僅限行銷活動，不適用於歷程。[開始使用實驗](../using/content-management/get-started-experiment.md) | [建立實驗](../using/content-management/content-experiment.md)

**[校樣](../using/content-management/proofs.md)** - 使用測試輪廓資料測試傳送至特定電子郵件地址的電子郵件傳遞。與種子清單不同 (校樣是手動測試傳送，種子清單是利害關係人的自動複本)。[傳送校樣](../using/content-management/proofs.md)

**[衝突偵測](../using/conflict-prioritization/conflicts.md)** - 可識別針對相同客群之重疊行銷活動和歷程的工具。有限歷程支援：僅限單一、客群資格和讀取客群類型。[了解衝突管理](../using/conflict-prioritization/gs-conflict-prioritization.md)

**[核准工作流程](../using/test-approve/gs-approval.md)** - 需要利害關係人在啟用前核准的多步驟檢閱流程。需要核准原則設定。[設定核准](../using/test-approve/gs-approval.md) | [建立原則](../using/test-approve/approval-policies.md)

**[轉譯測試](../using/content-management/rendering.md)** - 跨電子郵件用戶端 (Gmail、Outlook、Apple Mail) 和裝置的電子郵件顯示驗證。需要 Litmus 整合。[測試電子郵件轉譯](../using/content-management/rendering.md)

**[個人化遊樂場](../using/personalization/personalize.md#playground)** - 互動式學習環境，使用個人化語法進行實驗，並使用範例資料測試運算式。不需要即時資料集。[存取遊樂場](../using/personalization/personalize.md#playground)

## 其他資源

>[!BEGINTABS]

>[!TAB 基本指南]

* [模擬內容變化版本](../using/test-approve/simulate-sample-input.md) - 使用 CSV 或 JSON 檔案測試最多 30 個個人化案例。適用於進行多語言內容測試，且無需建立多個測試輪廓。支援電子郵件、簡訊、推播、網頁、程式碼型、應用程式內和內容卡。

* [建立測試輪廓](../using/audience/creating-test-profiles.md) - 建立和管理測試輪廓，以模擬客戶案例。瞭解如何標記輪廓以進行測試、設定屬性以及整理測試區段。

* [電子郵件垃圾郵件報告](../using/content-management/spam-report.md) - 在傳送前檢查垃圾郵件分數，以改善傳遞能力及收件匣版位。取得內容最佳化的可操作建議。

* [歷程常見問題集](../using/building-journeys/journey-faq.md) - 有關歷程測試、執行和疑難排解的常見問題快速參考。

>[!TAB 相依性和關係]

瞭解測試功能如何相互連線以及如何連線至您更廣泛的 Journey Optimizer 工作流程。本節將對應先決條件、上游/下游相依性及常見功能組合。

+++**先決條件 (測試前必須滿足)**

* 必須先建立測試輪廓，才能使用測試模式或內容預覽
* 在提交以進行核准之前，必須先設定核准原則
* 必須先建立種子清單，才能新增至行銷活動/歷程
* 電子郵件轉譯測試需要 Litmus 整合
* 歷程必須處於草稿狀態，才能使用測試模式
* 歷程必須已將命名空間設定為使用測試模式

+++

+++**測試取決於什麼 (上游)**

* 內容建立：需要行銷活動或歷程進行測試
* 測試輪廓：測試模式和內容預覽的必需項
* 核准原則：核准工作流程的必需項
* 設定：管道設定、電子郵件驗證、網域設定

+++

+++**測試取決於什麼 (下游)**

* 行銷活動/歷程啟用：不解決錯誤就無法啟用
* 發佈：發佈前可能需要核准
* 即時監視：啟動後的監視和報告
* 最佳化：使用測試結果來調整未來的行銷活動

+++

+++**相關功能**

* 測試 + 核准工作流程 - 品質保證流程
* 測試 + 衝突偵測 - 防止過度傳訊給客戶
* 測試 + 內容實驗 - 績效最佳化
* 測試 + 報告 - 持續改善週期
* 測試輪廓 + 個人化 - 內容驗證
* 試運行 + 測試模式 - 完整的歷程驗證

+++

+++**常見功能組合**

* 內容測試：測試輪廓 + 範例輸入資料 + 個人化遊樂場
* 電子郵件驗證：轉譯測試 + 垃圾郵件分數 + 測試輪廓 + 校樣
* 歷程驗證：測試模式 + 試運行 + 測試輪廓
* 啟動前檢查清單：所有技術測試 + 衝突偵測 + 核准工作流程

+++

>[!TAB 常見問題]

+++**問：啟動行銷活動之前需要進行哪些測試？**

**最基本做法：**使用測試輪廓進行內容預覽 + 垃圾郵件分數檢查 (電子郵件)
**建議做法：** + 電子郵件轉譯 + 衝突偵測 + 核准工作流程
**最佳做法：** + 範例輸入資料測試 + 種子清單 + A/B 實驗 (如果最佳化)

+++

+++**問：如何測試個人化而不建立許多測試輪廓？**

**主要解決方案：**&#x200B;使用[範例輸入資料](../using/test-approve/simulate-sample-input.md)搭配 CSV/JSON 檔案 (支援最多 30 種變化版本)
**替代方案：**&#x200B;建立 3-5 個代表性的[測試輪廓](../using/audience/creating-test-profiles.md)，涵蓋主要區段
**學習工具：**&#x200B;先在[個人化遊樂場](../using/personalization/personalize.md#playground)進行實驗

+++

+++**問：歷程的測試模式與試運行之間有何差異？**

**測試模式：**透過歷程傳送測試輪廓、觸發實際動作、產生測試訊息。需要草稿歷程 + 命名空間。
**試運行：**追蹤執行路徑而不傳送任何內容。適用於任何歷程狀態。不傳送任何訊息，不執行任何動作。
**搭配使用：**&#x200B;測試訊息的測試模式 + 驗證邏輯的試運行 - 完整的涵蓋範圍。

+++

+++**問：我可以在生產/即時狀態中測試歷程嗎？**

**測試模式：**否 - 僅限草稿歷程
**試運行：**是 - 適用於任何歷程狀態
**內容預覽：**是 - 隨時預覽個別訊息
**因應措施：**&#x200B;複製即時歷程並轉換為草稿狀態，進行完整測試模式驗證

+++

+++**問：哪些測試功能需要外部整合？**

**電子郵件轉譯：**需要 Litmus 整合 (單獨授權)
**其他所有功能：**內建至 Journey Optimizer，不需要其他整合
**注意：**&#x200B;測試輪廓需要即時客戶輪廓服務 (已包含)

+++

+++**問：如何測試 API 觸發的行銷活動？**

**選項 1：**&#x200B;使用[行銷活動模擬 API](https://developer.adobe.com/journey-optimizer-apis/references/simulations/) {target-&quot;_blank&quot;} 進行程式設計測試
**選項 2：**在 UI 中使用測試輪廓預覽內容
**選項 3：**傳送校樣以測試電子郵件地址
**最佳做法：**&#x200B;結合所有這三項以進行全面驗證

+++

>[!ENDTABS]
