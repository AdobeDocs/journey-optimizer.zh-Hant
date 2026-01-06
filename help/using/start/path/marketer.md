---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 行銷人員快速入門
description: 作為歷程操作者，深入了解如何使用 Journey Optimizer
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: d1fd0b60ae60c2642108a1eb308564c9d04f5f9e
workflow-type: tm+mt
source-wordcount: '1476'
ht-degree: 98%

---

# 行銷人員快速入門 {#get-started-marketers}

身為&#x200B;**行銷人員**&#x200B;或&#x200B;**業務人員**，您需要設計客戶歷程，以為客戶提供個人化的內容體驗。您可以建立並管理這些個人化歷程的所有不同元件，包括電子郵件和推播訊息、產品建議以及決策元件，以智慧地個人化訊息內容。Journey Optimizer 提供統一的使用者體驗，您可在同一處實作完整的端到端使用案例。一旦[系統管理員](administrator.md)及[資料工程師](data-engineer.md)授予您存取權限並準備好您的環境，您就可以開始使用[!DNL Adobe Journey Optimizer]。

## 要點快速入門

Journey Optimizer 可在單一應用程式中，整合即時客戶洞察、現代全管道協調流程和智慧決策。跨電子郵件、簡訊、推播、應用程式內、網頁、內容卡等建立個人化、連線的客戶體驗。

Journey Optimizer 提供兩種強大的協調方法：

* **歷程**：即時、一對一的互動，每個客戶以自己的步調前進，由行為或事件觸發
* **協調的行銷活動**：大規模複雜的多步驟批次行銷活動，透過工作流程讓多個客群保持同一進度，非常適合品牌啟動的行銷活動，例如季節性促銷活動、產品推出或帳戶型通訊

請與您的[管理員](administrator.md)合作以取得存取權，並與[資料工程師](data-engineer.md)合作以設定客群、資料和關聯式結構描述以進行進階細分。

請依照下列核心步驟開始建立體驗：

1. **建立客群**。透過區段定義、上傳 CSV 檔案或使用客群構成來建立客群。Journey Optimizer 提供多種方法來鎖定合適的客戶。深入了解[客群](../../audience/about-audiences.md)和[建立區段定義](../../audience/creating-a-segment-definition.md)。

1. **設計內容**。跨所有管道建立吸引人的訊息，包括電子郵件、簡訊、推播、應用程式內、網頁和內容卡：
   * 根據您的品牌方針，使用 **AI 助理**&#x200B;產生電子郵件內容、主旨行以及影像。[了解 AI 內容產生](../../content-management/gs-generative.md)
   * 使用客戶資料、動態內容和條件式邏輯&#x200B;**個人化訊息**。[了解個人化](../../personalization/personalize.md)
   * **反覆處理內容資料**&#x200B;以顯示事件、自訂動作和資料集查詢的動態清單。[了解如何反覆處理內容資料](../../personalization/iterate-contextual-data.md)
   * 建立可重複使用的&#x200B;**內容範本**&#x200B;和&#x200B;**片段**，以維持品牌一致性。[使用範本](../../content-management/content-templates.md)
   * 在行動應用程式和網站中傳遞持續的非侵入式&#x200B;**內容卡**。與推播通知不同，內容卡會保持可見狀態，直至使用者將其關閉。[了解內容卡](../../content-card/create-content-card.md)
   * 使用 **Adobe Experience Manager Assets** 整合來管理資產。[了解資產](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **新增產品建議與決策**。使用 AI 驅動的決策，在適當的時間為每位客戶提供最佳產品建議。了解[決策管理](../../offers/get-started/starting-offer-decisioning.md)和[體驗決策](../../experience-decisioning/gs-experience-decisioning.md)。

   ![](../assets/offers-e2e-offers-displayed.png)

1. **測試及驗證**。 傳送前預覽和測試內容：
   * 使用&#x200B;**測試輪廓**&#x200B;來預覽個人化並檢查跨裝置轉譯
   * 使用 CSV/JSON 檔案中的&#x200B;**範例資料**&#x200B;進行測試
   * 預覽常見電子郵件用戶端之間的&#x200B;**電子郵件轉譯**
   * 執行 **A/B 測試和實驗**&#x200B;以最佳化內容變化版本。使用多臂老虎機實驗，自動分配更多流量以即時贏得變數。[了解實驗](../../content-management/content-experiment.md)
   * 為行銷活動和歷程設定&#x200B;**核准工作流程** (需要額外的授權)。[了解核准](../../test-approve/gs-approval.md)

   了解如何[測試及驗證訊息](../../content-management/preview-test.md)。

1. **建立客戶歷程**。使用歷程畫布建立即時、個人化的體驗：

   * 觸發包含&#x200B;**事件** (客戶動作) 或&#x200B;**客群** (批次傳送) 的歷程
   * 新增&#x200B;**條件**，以根據客戶資料建立個人化路徑
   * 使用&#x200B;**等待活動**&#x200B;來建立訊息間的完美時機
   * 在一個歷程中跨&#x200B;**多個管道**&#x200B;傳送訊息
   * 套用 **A/B 測試**&#x200B;並最佳化傳送時間，以最大化參與度
   * 使用&#x200B;**資料集查詢**，透過 Adobe Experience Platform 的即時資料擴充歷程。[了解資料集查詢](../../building-journeys/dataset-lookup.md)
   * 運用&#x200B;**補充識別碼**，允許同一輪廓輸入多個歷程執行個體 (例如，不同的訂單或預訂)。[了解補充識別碼](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   了解如何[設計和執行歷程](../../building-journeys/journey-gs.md)並探索[歷程使用案例](../../building-journeys/jo-use-cases.md)。了解[進入/退出條件](../../building-journeys/entry-exit-criteria-guide.md)以控制輪廓流程。

1. **啟動協調的行銷活動**。使用視覺畫布設計大規模的複雜多步驟批次行銷活動：

   * 使用關聯式查詢立即建立&#x200B;**隨選客群**，將客戶資料與帳戶、購買、訂閱和其他實體連線
   * 建立&#x200B;**多實體細分**&#x200B;以精確鎖定目標 (例如「訂閱將於 30 天後到期的客戶」或「最近購買高價值物品的客戶」)
   * **在傳送之前了解**&#x200B;啟動前的準確客群計數
   * 針對季節性促銷活動、產品推出、忠誠度產品建議或客戶型行銷，設計&#x200B;**多步驟工作流程**
   * 排程行銷活動，以立即、在特定時間或定期 (每日、每週、每月) 執行排程
   * 在&#x200B;**批次模式**&#x200B;中處理客群，透過工作流程讓所有輪廓保持同一進度

   了解如何[開始使用協調的行銷活動](../../orchestrated/gs-orchestrated-campaigns.md)，以及何時[使用行銷活動與歷程](../../orchestrated/orchestrated-campaigns-faq.md)。

1. **監視和最佳化**。追蹤績效並隨著時間改善結果：
   * 監視&#x200B;**即時歷程**&#x200B;績效並找出瓶頸
   * 分析&#x200B;**訊息傳遞**&#x200B;率和參與量度
   * 使用&#x200B;**報告儀表板**&#x200B;與 Customer Journey Analytics 整合
   * 追蹤&#x200B;**轉換**&#x200B;和業務影響
   * 使用衝突管理規則管理&#x200B;**訊息頻率和優先順序**，以防止過度通訊。[了解衝突管理](../../conflict-prioritization/gs-conflict-prioritization.md)

   了解如何[監視績效](../../reports/report-gs-cja.md)。

## 成功的最佳做法

### 內容建立

* **從範本開始**：使用預先建立的範本和內容片段來加速建立並維持一致性
* **及早測試，經常測試**：一律預覽跨裝置的內容，並使用測試輪廓來驗證個人化
* **明智地運用 AI**：使用 AI 助理處理初始草稿和變化版本，但一律檢閱並調整您的品牌語調
* **保持簡潔**：簡潔、簡明的訊息與強大的行動號召比複雜的版面效果更好

### 歷程設計

* **定義明確的目標**：先建立成功量度，再建立您的歷程
* **對應客戶體驗**：在實施前將整個歷程視覺化
* **策略性地使用等候活動**：在傳送後續追蹤前，讓客戶有時間參與
* **規劃退出策略**：定義客戶應該退出歷程的時機和原因
* **在草稿模式中測試**：在啟用之前使用試運行驗證歷程邏輯

[了解歷程最佳做法](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### 行銷活動協調

* **選擇正確的方法**： [比較歷程型別](../../building-journeys/journey.md#journey-types)以取得即時、行為觸發的體驗，或[促銷活動型別](../../campaigns/get-started-with-campaigns.md#campaign-types)以取得排程的批次促銷活動
* **定義明確的行銷活動目標**：在設計多步驟工作流程之前建立目標
* **從試驗客群開始**：在擴充之前驗證計數和細分邏輯
* **運用關聯式資料**：使用多實體細分，將客戶資料與帳戶、購買、訂閱連線，以進行精確目標定位
* **讓細分保持簡單**：使用明確且可維護的規則來最佳化績效和透明度
* **使用一致的命名**：透過明確的命名慣例，讓行銷活動管理更容易

### 客群目標定位

* **仔細細分**：根據明確條件建立特定、可操作的客群區段
* **定期重新整理**：設定適當的評估排程，確保客群保持最新狀態
* **平衡大小與精確度**：目標客群足夠大，具有統計顯著性，但也足夠具體，具有關聯性
* **使用擴充屬性**：利用計算屬性和擴充資料進行更深入的個人化

### 頻率管理

* **尊重客戶偏好**：尊重選擇退出與通訊偏好
* **設定頻率上限**：使用規則集防止跨管道的訊息疲勞
* **協調行銷活動**：使用衝突管理，以確保客戶在正確的時間收到正確的訊息
* **監視參與度**：觀察疲勞跡象 (開放率下降、取消訂閱數增加)

[了解頻率上限](../../conflict-prioritization/channel-capping.md)

## 探索使用案例

從示範 Journey Optimizer 功能的實用範例學習：

**歷程使用案例** (即時、一對一)：

* **歡迎系列**：透過個人化的多步驟歷程來吸引新客戶。[檢視使用案例](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **捨棄的購物車復原**：重新聯絡將商品留在購物車中的客戶。[檢視使用案例](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **事件導向訊息**：即時回應客戶動作
* **生日行銷活動**：傳送由輪廓日期觸發的個人化生日訊息
* **產品建議**：根據瀏覽和購買歷史記錄建議相關產品

**協調的行銷活動使用案例** (批次、一對多)：

* **季節性促銷活動**：跨客戶區段啟動協調的行銷活動 (例如，假日促銷、開學季)
* **產品推出**：透過循序傳訊向目標客群宣傳新產品
* **忠誠度計劃優惠方案**：根據購買歷史記錄提供階層優惠方案以獎勵高價值客戶
* **客戶型行銷**：定位具有特定特性及相關連絡人的客戶
* **訂閱續約**：使用多實體查詢，聯絡訂閱即將到期的客戶
* **重新參與行銷活動**：以批次模式透過目標優惠方案重新贏回不活躍的客戶。[檢視使用案例](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)

**歷程模式：**

* [傳送訊息給訂閱者](../../building-journeys/message-to-subscribers-uc.md)：鎖定包含個人化內容的訂閱清單
* [多管道傳訊](../../building-journeys/journeys-uc.md)：結合電子郵件和推播與回應事件
* [僅限工作日的電子郵件](../../building-journeys/weekday-email-uc.md)：使用時間型條件排程通訊

瀏覽完整的[歷程使用案例庫](../../building-journeys/jo-use-cases.md)，並深入了解[協調的行銷活動](../../orchestrated/gs-orchestrated-campaigns.md)。

## 跨角色共同作業

您的行銷工作連結到其他團隊：

>[!BEGINTABS]

>[!TAB 與資料工程師合作]

與[資料工程師](data-engineer.md)共同處理資料與客群設定：

* 請求新的計算屬性，以便進行個人化和細分
* 為協調的行銷活動協調關聯式結構描述
* 提供有關客群品質和資料準確度的意見回饋
* 符合進階細分的多實體資料需求

>[!TAB 與開發人員合作]

與[開發人員](developer.md)共同處理事件追蹤與實作：

* 就應該觸發歷程事件的使用者互動達成一致
* 啟動前測試行動裝置和網頁實作
* 驗證內容績效和使用者參與的追蹤
* 對訊息傳送或個人化問題進行疑難排解

>[!TAB 與管理員合作]

與[管理員](administrator.md)共同處理存取權和設定：

* 請求行銷活動和歷程的管道設定
* 確認協調的行銷活動和其他功能的授權存取權
* 報告權限或存取權問題
* 協調新功能啟用和測試環境

>[!ENDTABS]

## 後續步驟

1. **從小事做起**：建立簡單的歡迎歷程或單一訊息行銷活動，以了解平台
2. **利用 AI**：使用 AI 助理提出問題並加快內容建立
3. **加入社群**：與 [Experience League 社群](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}中的其他 Journey Optimizer 使用者交流
4. **探索教學課程**：觀看 [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hant){target="_blank"} 上的逐步影片
