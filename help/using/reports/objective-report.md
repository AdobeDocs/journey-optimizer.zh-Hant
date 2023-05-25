---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動全域報告
description: 瞭解如何使用Campaign全域報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6b8983d3f3fa989bd7190fc6a8b51fa8989b2293
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 3%

---

# 行銷活動全域報告 {#objective-report}

行銷活動全域報告可透過以下連結直接從行銷活動存取： **[!UICONTROL 檢視報告]** 按鈕。

行銷活動 **[!UICONTROL 全域報告]** 分成不同的Widget，詳細說明行銷活動的成功和錯誤。 如有需要，可以調整每個Widget的大小並將其刪除。 如需詳細資訊，請參閱此 [區段](../reports/global-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [此頁面](global-report.md#list-of-components-global.md)

## 行銷活動標籤 {#campaign-global-objectives}

### 傳送 {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

此 **[!UICONTROL 行銷活動的統計資料]** Widget會詳細說明與行銷活動相關的主要資訊：

* **[!UICONTROL 輸入的設定檔]**：開始歷程的設定檔數。

* **[!UICONTROL 動作已傳送]**：歷程中某個動作已傳送的不重複次數總計。

* **[!UICONTROL 動作失敗百分比]**：歷程中動作失敗的不重複次數總計，與動作已傳送的不重複次數總數比較。

### 目標報表 {#objective-global}

>[!AVAILABILITY]
>
>此 **目標報表** 功能目前僅適用於一組組織（可用性限制）。 如需詳細資訊，請聯絡您的 Adobe 代表。

![](assets/performance_report.gif)

此 **[!UICONTROL 目標]** 索引標籤可讓您透過鎖定一個特定量度，更好地微調傳送的報表。

此 **[!UICONTROL 目標]** 清單連結至 **[!UICONTROL 資料集]** 定義系統連線，以擷取其他資訊。 內建清單 **[!UICONTROL 目標]** 可使用，但您可以透過新增來新增您自己的 **[!UICONTROL 資料集]**. 如需詳細程式，請參閱此 [區段](../campaigns/reporting-configuration.md).

選取您要鎖定目標之後，兩項 **[!UICONTROL 效能總覽]** 和 **[!UICONTROL 行銷活動目標]** Widget將提供您傳遞效能的詳細摘要。

使用 **[!UICONTROL 行銷活動目標]** widget，您也可以選擇將主要目標與其他量度比較。

### 實驗報告 {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

此 **[!UICONTROL 實驗]** Tab提供每個變體效能的關鍵分析，並識別最成功的變體。

請注意，定義績效最佳者可能需要一些時間，其將以此圖示表示 ![](assets/experimentation_report_1.png).

+++進一步瞭解Experimentation報告可用的不同量度和Widget。

此 **[!UICONTROL 實驗結果]** Widget詳細說明每個變體的效能。 您可以變更基線，方法是從 **[!UICONTROL 基線]** 下拉式清單。 最佳處理方式將以星形圖示表示。

此表格會顯示下列量度：

* **[!UICONTROL 提升度超過基準線]**：測量指定處理的轉換率相對於基線的改善百分比。

* **[!UICONTROL 信賴度]**：指定處理與基準處理相同的證據。 [了解更多](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 不重複傳出點按]**：跨傳出頻道的點按總數。

* **[!UICONTROL 設定檔]**：針對此處理的設定檔數目。

* **[!UICONTROL 不重複傳出點按次數/設定檔]**：建立實驗時先前選取的成功量度總值除以設定檔數目。

此 **[!UICONTROL 信賴區間]** 圖表會測量改善的不確定性。 它詳細說明基準線和最佳績效處理之間的績效百分比差異。 [了解更多](../campaigns/experiment-calculations.md#confidence-intervals)。
+++

如需這些結果的深入瞭解及如何解讀，請參閱 [此頁面](../campaigns/get-started-experiment.md#interpret-results).

