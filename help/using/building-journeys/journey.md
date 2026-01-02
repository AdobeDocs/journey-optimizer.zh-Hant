---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用歷程
description: 開始使用歷程
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 歷程, 探索, 開始
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 87351e845c7a6267cc78c26c838e69e77325f2b8
workflow-type: tm+mt
source-wordcount: '1420'
ht-degree: 3%

---


# 開始使用歷程{#jo-general-principle}

Adobe Journey Optimizer可讓您建立個人化的多步驟客戶歷程，並即時因應對象的行為和需求。 使用直覺式的拖放畫布，您可以跨多個管道協調訊息和動作，運用情境資料和受眾目標定位以發揮最大影響。

本指南提供清晰的藍圖，可幫助您瞭解歷程基本面、為您的使用案例選擇正確的歷程型別，並自信地設計歷程，提供有意義、即時的客戶體驗。

## 什麼是歷程？

**歷程**&#x200B;是自動的多步驟客戶體驗，可針對客戶行為、業務活動或排程的行銷活動，跨管道協調個人化互動。

使用[!DNL Journey Optimizer]來：

* 使用儲存在事件或資料來源中的內容資料，建置&#x200B;**即時協調**&#x200B;使用案例
* 設計&#x200B;**多步驟進階情境**，以動態方式回應客戶行為與業務事件
* 跨電子郵件、推播、簡訊、應用程式內、網頁等大規模提供&#x200B;**1:1個人化體驗**

![具有調色盤、畫布和屬性窗格的Journey Designer介面](assets/journey38.png)

➡️ **準備好開始建置嗎？** [在5分鐘內建立您的第一個歷程](journey-gs.md)。

## 選擇您的歷程型別 {#journey-types}

**在您開始建立**&#x200B;之前，請務必瞭解適合您使用案例的歷程型別。 Adobe Journey Optimizer支援四種歷程型別，分別針對不同的進入機制和業務案例而設計：

>[!BEGINTABS]

>[!TAB 單一歷程]

**何時使用：**&#x200B;即時事件觸發的體驗

**單一歷程**&#x200B;會在特定動作（購買、應用程式登入、表單提交）發生時個別觸發。 設定檔一次會即時輸入一個，因此非常適合用於即時行為導向的回應。

**最適合：**

* 購買後的訂單確認
* 有人訂閱時的歡迎電子郵件
* 瀏覽時觸發的購物車放棄率
* 密碼重設通知

➡️ [瞭解事件](../event/about-events.md) | [傳送訊息給訂閱者使用案例](message-to-subscribers-uc.md)

>[!TAB 讀取對象歷程]

**何時使用：**&#x200B;已排程行銷活動給對象區段

**讀取對象歷程**&#x200B;從Adobe Experience Platform對象開始，並同時以批次傳送訊息給所有設定檔。 此歷程型別適用於已排程的大型通訊。

**最適合：**

* 每月電子報
* 目標區段的促銷活動
* 產品公告
* 季節性行銷活動

➡️ [瞭解閱讀對象](read-audience.md) | [開始使用對象](../audience/about-audiences.md)

>[!TAB 對象資格歷程]

**何時使用：**&#x200B;對象成員資格變更的即時回應

當設定檔符合（或退出）特定對象的資格時，**對象資格歷程**&#x200B;會觸發。 設定檔會即時符合條件，因此可個別輸入，並在客戶行為變更時立即參與。

**最適合：**

* VIP層級升級通知
* 客戶非作用中時重新參與
* 首次購買慶祝訊息
* 客戶移動時的地理目標定位

➡️ [瞭解對象資格](audience-qualification-events.md) | [正在建立對象](../audience/creating-a-segment-definition.md)

>[!TAB 商務活動歷程]

**何時使用：**&#x200B;影響多個客戶的業務狀況

**業務事件歷程**&#x200B;是由同時影響多個設定檔的業務層級事件（庫存更新、天氣警報、價格變更）觸發。 這些功能可回應更廣泛的業務環境，而非個別動作。

**最適合：**

* 向感興趣的客戶發出低詳細目錄警示
* 快閃銷售公告
* 天氣型促銷活動
* 價格下降通知
* 產品補貨警報

➡️ [瞭解業務活動](../event/about-creating-business.md) | [專案管理](entry-management.md)

>[!ENDTABS]

>[!NOTE]
>
>不確定要選擇哪種型別？ 從事件型體驗的&#x200B;**單一歷程**&#x200B;或排程行銷活動的&#x200B;**讀取對象歷程**&#x200B;開始 — 這些涵蓋最常見的使用案例。

## 使用歷程設計器建置 {#journey-designer}

**[歷程設計器](using-the-journey-designer.md)**&#x200B;是您用來建立客戶體驗的視覺畫布。 使用直覺式的拖放介面，您無需撰寫程式碼即可協調歷程的每個步驟。

![具有調色盤、畫布和屬性窗格的Journey Designer介面](assets/journey38.png)

### 您可以在設計工具中執行的動作：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hant)

**定義進入點**

選擇客戶輸入的方式：透過事件、受眾區段或受眾資格。

[瞭解進入管理](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hant)

**傳送訊息**

針對電子郵件、推播、SMS/MMS、應用程式內、Web等使用內建頻道動作，全都在Journey Optimizer中設計。

[在歷程中傳送訊息](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hant)

**新增邏輯和條件**

根據設定檔屬性、對象成員資格或即時事件來分支您的歷程。

[使用條件](condition-activity.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hant)

**運用資料**

使用來自事件、Adobe Experience Platform或第三方API服務的內容資料。

[使用資料來源](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hant)

**連線外部系統**

建立自訂動作，以整合傳送訊息或觸發工作流程的協力廠商系統。

[設定自訂動作](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hant)

**新增協調活動**

使用等待時間、跳躍、設定檔更新和對象管理，建立複雜的流程。

[探索所有活動](about-journey-activities.md)
:::

::::

➡️ **實作學習：** [觀看歷程設計工具影片](#video)或[探索端對端使用案例](jo-use-cases.md)

## 您的歷程建立工作流程 {#workflow}

建立成功的歷程會遵循清晰、可重複的流程。 以下是您的逐步工作流程：

**1。 計畫**→**2。 設計**→**3。 測試**→**4。 發佈**→**5。 監視** → **6。 最佳化**

### &#x200B;1. **規劃您的歷程** {#plan}

開啟設計工具之前，請先釐清您的目標：

* **目標是什麼？** （例如，加入新客戶，重新與非作用中使用者互動）
* **對象是誰？** （特定區段、事件導向的個人）
* **適合哪個歷程型別？** （請參閱上述[歷程型別](#journey-types)）
* **您將使用哪些管道？** （電子郵件、推播、簡訊等）

### &#x200B;2. **在畫布中進行設計** {#design}

使用歷程設計器建置您的流程：

1. **設定專案條件** — 定義設定檔如何輸入（事件、對象、資格）
2. **新增協調邏輯** — 包含等待時間、條件和決定點
3. **設定訊息** — 設計您的通訊或運用現有的範本
4. **設定動作** — 設定要執行的內建或自訂動作
5. **定義退出條件** — 指定設定檔完成歷程的時間和方式

[瞭解如何使用歷程設計器→](using-the-journey-designer.md)

### &#x200B;3. **上線前測試** {#test}

永遠在客戶體驗問題之前測試您的歷程，以找出問題：

* 使用&#x200B;**測試模式**&#x200B;以測試設定檔模擬歷程
* 使用&#x200B;**練習**&#x200B;來預覽歷程執行，而不會影響真實資料或傳送訊息
* 確認所有條件、訊息和動作均如預期般運作
* 檢查時間、資料流程和個人化

[測試您的歷程→](testing-the-journey.md) | [了解試用→](journey-dry-run.md)

### &#x200B;4. **發佈您的歷程** {#publish}

測試完成後，發佈以讓您的歷程上線：

* 檢閱最終設定和屬性
* 發佈以針對真實客戶啟用
* 注意：即時歷程可以停止但不能編輯（您必須建立新版本）

[發佈您的歷程→](publish-journey.md)

### &#x200B;5. **監視效能** {#monitor}

追蹤您的歷程在真實世界的表現：

* 檢視歷程報告與分析
* 監視輸入、完成和錯誤率
* 設定嚴重問題的警示

[監視和報告→](report-journey.md) | [設定警示→](../reports/alerts.md)

### &#x200B;6. **最佳化及重複** {#optimize}

使用見解來改善：

* 分析參與量度和轉換率
* 測試傳送時間最佳化
* 建立有改進的新歷程版本
* 使用AI支援的建議

[最佳化您的歷程→](optimize.md) | [傳送時間最佳化→](send-time-optimization.md)

➡️ **準備好開始了嗎？** [立即→](journey-gs.md)建立您的第一個歷程

## 真實使用案例 {#use-cases}

從示範如何套用歷程概念以解決常見行銷挑戰的實務範例學習：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hant)

**歡迎新訂閱者**

當客戶訂閱您的服務時，觸發歡迎歷程，鼓勵他們完成入門步驟。

[檢視使用案例→](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=zh-Hant)

**傳送時間最佳化**

當每位客戶最有可能參與時，使用AI傳送電子郵件，最大化開啟率和點按率。

[檢視使用案例→](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hant)

**加速傳遞**

逐步增加訊息量，以提升您的傳送信譽並避免傳遞能力問題。

[檢視使用案例→](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hant)

**依據工作日**&#x200B;鎖定目標

根據客戶進入您歷程的當週日期傳送不同內容，以提高關聯性。

[檢視使用案例→](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hant)

**多頻道行銷活動**

在單一歷程中跨電子郵件、推播、簡訊和Web頻道協調順暢的體驗。

[檢視使用案例→](journeys-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hant)

**所有使用案例**

探索包含逐步實施的完整歷程使用案例庫。

[瀏覽所有→](jo-use-cases.md) | [使用案例庫→](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## 探索歷程功能 {#capabilities}

當您更熟悉建立歷程時，請探索這些強大的功能以建立複雜的客戶體驗：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hant)

**進階運算式**

使用運算式編輯器針對資料操作和複雜邏輯建立動態條件和個人化。

[了解運算式](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=zh-Hant)

**時區管理**

使用自動時區調整和最佳傳送時間來處理全域對象。

[管理時區](timezone-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hant)

**測試模式與試執行**

在上線之前，使用測試設定檔驗證歷程，並預覽執行而不影響真實資料。

[使用試用](journey-dry-run.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hant)

**複製到沙箱**

跨沙箱複製歷程以簡化測試和部署工作流程。

[複製歷程](copy-to-sandbox.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hant)

**標籤和組織**

使用標籤來分類和篩選歷程，以大規模管理效能。

[使用標籤組織](tags.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hant)

**輸送量控制**

限制訊息輸送量，以管理傳送信譽並避免系統過載。

[控制項輸送量](limit-throughput.md)
:::

::::

[檢視所有歷程功能→](/help/rp_landing_pages/manage-journey-landing-page.md)

## 觀看以學習 {#video}

取得歷程元件的視覺簡介，並瞭解在畫布中建立歷程的基本知識：

>[!VIDEO](https://video.tv.adobe.com/v/3430349?captions=chi_hant&quality=12)

➡️ **想要更多影片？** [探索歷程影片教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}

## 需要協助嗎？ {#help}

### 常見工作的快速連結

* **[建立您的第一個歷程](journey-gs.md)** — 初學者逐步指南
* **[歷程常見問題集](journey-faq.md)** — 已回答的常見問題
* **[疑難排解](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** — 診斷並修正問題
* **[錯誤代碼參考](error-codes-reference.md)** — 瞭解錯誤訊息
* **[護欄和限制](../start/guardrails.md)** — 技術界限和最佳實務

### 取得有關問題的通知

設定&#x200B;**[歷程警示](../reports/alerts.md)**，以便在歷程發生錯誤或異常模式時接收即時通知。

### 其他資源

* **[歷程管理中心](/help/rp_landing_pages/manage-journey-landing-page.md)** — 用於篩選、最佳化和設定檔管理的工具
* **[歷程活動參考](/help/rp_landing_pages/about-journey-building-landing-page.md)** — 所有活動型別的完整指南
* **[疑難排解執行問題](troubleshooting-execution.md)** — 偵錯歷程執行問題
* **[疑難排解傳入活動](troubleshooting-inbound.md)** — 修正專案及資格問題

**準備好建立您的第一個歷程了嗎？** [立即開始→](journey-gs.md)
