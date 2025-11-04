---
solution: Journey Optimizer
product: journey optimizer
title: 使用歷程步驟事件
description: 瞭解如何在Adobe Journey Optimizer中使用歷程步驟事件 — 瞭解其內容、重要性，以及如何將其用於分析和最佳化
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin, User
level: Intermediate, Experienced
keywords: 歷程，步驟事件，分析，報告，監控， XDM
source-git-commit: 9320777cfb75fd1370c11b601908644ba17ff21e
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 2%

---

# 使用歷程步驟事件 {#work-with-journey-step-events}

歷程步驟事件是自動產生的事件，可擷取[設定檔](../audience/get-started-profiles.md)在Adobe Journey Optimizer中進行[歷程](../building-journeys/journey.md)時所採取每個步驟的詳細資訊。 這些事件提供全面的[歷程績效](../building-journeys/report-journey.md)可視性，並啟用強大的分析功能。

## 什麼是歷程步驟事件？ {#what-are-step-events}

歷程步驟事件是系統產生的[XDM (Experience Data Model)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}事件，每當設定檔在歷程中從一個節點移至另一個節點時，Adobe Journey Optimizer會自動建立並傳送至[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=zh-Hant){target="_blank"}。 每個事件都對應到客戶歷程體驗中的特定[歷程活動](../building-journeys/about-journey-activities.md)或轉變。

歷程步驟事件有兩種主要型別：

- **journeyStepEvent**：與透過歷程步驟的個別設定檔進度相關的事件
- **journeyStepProfileEvent**：包含其他設定檔內容資訊的事件

### 哪些會觸發歷程步驟事件？ {#event-triggers}

系統會自動為各種歷程活動產生歷程步驟事件：

- **進入事件**：設定檔[進入歷程](../building-journeys/entry-management.md)時
- **動作執行**：傳送[訊息時](../building-journeys/journeys-message.md)或執行[自訂動作](../building-journeys/using-custom-actions.md)
- **條件評估**：設定檔通過[條件](../building-journeys/condition-activity.md)和決定點時
- **等待活動**：設定檔進入並結束時[等待節點](../building-journeys/wait-activity.md)
- **退出事件**：設定檔完成或[退出歷程](../building-journeys/end-journey.md)時
- **錯誤處理**：在歷程執行期間發生錯誤時

>[!NOTE]
>
>依預設，會在所有執行個體上啟用歷程步驟事件。 您無法修改或更新在布建步驟事件期間建立的[結構描述和資料集](sharing-overview.md)。 這些結構描述和資料集處於唯讀模式。

深入瞭解[歷程步驟事件結構描述](sharing-field-list.md)。

## 為什麼歷程步驟事件重要 {#why-step-events-matter}

歷程步驟事件為使用Adobe Journey Optimizer的組織提供關鍵值：

### 即時分析和監控 {#real-time-analytics}

- **歷程績效追蹤**：使用[即時報告](live-report.md)即時監視設定檔在您的歷程中的流動方式
- **轉換分析**：透過[歷程分析](journey-global-report-cja.md)瞭解流失點和成功的轉換路徑
- **錯誤偵測**：透過[監視和警示](alerts.md)識別並疑難排解問題

### 資料整合與深入分析 {#data-integration}

- **跨平台分析**：結合歷程資料與其他[Adobe Experience Platform資料來源](../datasource/adobe-experience-platform-data-source.md)
- **Customer 360檢視**：建立包含歷程互動的完整[客戶設定檔](../audience/get-started-profiles.md)
- **歸因模型**：使用[Customer Journey Analytics](cja-ajo.md)將歷程接觸點連結到下游業務結果

### 最佳化機會 {#optimization}

- **A/B測試深入分析**：使用[實驗](campaign-global-report-cja-experimentation.md)分析不同歷程路徑的效能
- **Personalization增強功能**：使用歷程行為資料來改善[動態內容](../personalization/dynamic-content.md)的未來體驗
- **營運效率**：找出瓶頸並最佳化[歷程設計](../building-journeys/using-the-journey-designer.md)

## 如何使用歷程步驟事件 {#how-to-use-step-events}

### 存取歷程步驟事件資料 {#accessing-data}

歷程步驟事件資料會自動儲存在Adobe Experience Platform中，並可透過以下方式存取：

1. **Data Lake查詢**：使用SQL查詢`journey_step_events`查詢服務[的](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=zh-Hant){target="_blank"}資料集
2. **Customer Journey Analytics**：透過[進階分析工具](cja-ajo.md)分析歷程資料
3. **即時報告**：透過Journey Optimizer的[內建報告功能存取資料](gs-reports.md)
4. **API**：以程式設計方式存取自訂應用程式的事件資料

深入瞭解[存取資料集](../data/datasets-query-examples.md)。

### 可用的關鍵資料點 {#key-data-points}

歷程步驟事件會擷取完整資訊，包括：

- **歷程識別**： [歷程識別碼、版本和名稱](sharing-journey-fields.md)
- **設定檔資訊**： [設定檔識別碼和相關聯的身分](sharing-identity-fields.md)
- **步驟詳細資料**： [節點名稱、步驟型別和執行狀態](sharing-common-fields.md)
- **時間戳記**：每個歷程步驟的精確時間
- **動作結果**： [成功/失敗狀態和執行詳細資料](sharing-execution-fields.md)
- **錯誤資訊**：發生問題時，提供詳細的[錯誤碼和說明](sharing-field-list.md#discarded-events)

探索所有[可用的欄位定義](sharing-field-list.md)。

### 常見使用實例 {#common-use-cases}

**效能監視**

```sql
-- Example: Count profiles entering a journey in the last 24 hours
SELECT count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events 
WHERE _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey-id>'
AND _experience.journeyOrchestration.stepEvents.nodeType='start'
AND DATE(timestamp) > (now() - interval '24' hour);
```

**錯誤分析**

```sql
-- Example: Identify errors by journey node
SELECT _experience.journeyOrchestration.stepEvents.nodeName,
       count(distinct _experience.journeyOrchestration.stepEvents.profileID)
FROM journey_step_events
WHERE _experience.journeyOrchestration.stepEvents.actionExecutionError IS NOT NULL
GROUP BY _experience.journeyOrchestration.stepEvents.nodeName;
```

**歷程funnel分析**

- 追蹤每個歷程步驟的轉換率
- 識別設定檔最常退出歷程的位置
- 測量不同歷程階段逗留的時間

深入瞭解funnel分析的[查詢技術](query-examples.md#common-queries)。

## 範例和資源 {#samples-resources}

### 查詢範例和範本 {#query-examples}

探索完整的查詢範例，以取得常見的歷程步驟事件分析：

- **[歷程步驟事件查詢範例](query-examples.md)**：適用於常見分析案例的現成SQL查詢
- **[資料集查詢範例](../data/datasets-query-examples.md#journey-step-event)**：查詢歷程步驟事件資料集的範例
- **[以設定檔為基礎的查詢](query-examples.md#profile-based-queries)**：追蹤個別設定檔歷程與互動

### 欄位檔案 {#field-documentation}

瞭解歷程步驟事件的完整資料結構：

- **[歷程步驟事件欄位清單](sharing-field-list.md)**：所有可用欄位的完整參考
- **[通用欄位](sharing-common-fields.md)**：跨journeyStepEvent和journeyStepProfileEvent的共用欄位
- **[動作執行欄位](sharing-execution-fields.md)**：動作執行追蹤的特定欄位
- **[歷程欄位](sharing-journey-fields.md)**：歷程特定的中繼資料和識別碼

### 最佳實務及疑難排解 {#best-practices}

**效能最佳化**

- 使用`journeyVersionID`而非`journeyVersionName`以獲得更好的查詢效能（[進一步瞭解歷程屬性](../building-journeys/expression/journey-properties.md)）
- 依日期範圍篩選，改善大型資料集的查詢速度
- 運用符合您[歷程名稱空間設定](../building-journeys/entry-management.md)的設定檔身分

**資料品質**

- 定期監視[捨棄的事件](sharing-field-list.md#discarded-events)，以識別資料問題
- 驗證事件結構符合您的分析需求
- 在自訂查詢中實作適當的錯誤處理

**分析策略**

- 結合歷程步驟事件與[訊息回饋資料](../data/datasets-query-examples.md#message-feedback-event-dataset)以進行完整歸因
- 使用時間型分析來瞭解歷程速度和瓶頸

### 進階分析功能 {#advanced-analytics}

**Customer Journey Analytics整合**
可使用[Customer Journey Analytics](cja-ajo.md)分析歷程步驟事件：

- 進階歸因模型
- 跨頻道歷程視覺效果
- 歷程結果的預測性分析

瞭解如何[設定Journey Optimizer資料的Customer Journey Analytics](report-gs-cja.md)。

## 其他資源 {#additional-resources}

### 檔案連結 {#documentation-links}

- **[歷程步驟分享概觀](sharing-overview.md)**：瞭解歷程資料如何流向Adobe Experience Platform
- **[內建結構描述字典](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh-Hant){target="_blank"}**：完整XDM結構描述參考
- **[Journey Optimizer報告](report-gs-cja.md)**： Journey Optimizer報告功能概觀

### 整合指南 {#integration-guides}

- **[Adobe Customer Journey Analytics](cja-ajo.md)**：正在分析CJA中的Journey Optimizer資料
- **[資料管理](../data/export-datasets.md)**：匯出和管理歷程資料
- **[隱私權與治理](../privacy/audit-logs.md)**：歷程事件的資料治理考量事項


**後續步驟：**

- 從[建立您的第一個歷程報告](sharing-overview.md)開始
- 探索[查詢範例](query-examples.md)以取得特定使用案例
- 瞭解[歷程管理最佳實務](../building-journeys/journey.md)
