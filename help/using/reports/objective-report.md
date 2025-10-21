---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動全域報告
description: 瞭解如何使用Campaign全域報告的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: ec1af88c-7b0a-4eaf-97e1-0d9676268fed
badge: label="Beta" type="Informative"
source-git-commit: 722d37dc4bcb9ab7983ea336aa0b12a6a09e01dc
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 4%

---

# 行銷活動全域報告 {#objective-report}

透過&#x200B;**[!UICONTROL 檢視報告]**&#x200B;按鈕，可以直接從您的行銷活動存取行銷活動全域報告。

行銷活動&#x200B;**[!UICONTROL 全域報告]**&#x200B;會分成不同的Widget，詳細說明行銷活動的成功與錯誤。 如有需要，可以調整每個Widget的大小並將其刪除。 如需詳細資訊，請參閱此<!--[section](../reports/global-report.md#modify-dashboard)-->。

如需Adobe Journey Optimizer中每個可用量度的詳細清單，請參閱<!--[this page](global-report.md#list-of-components-global.md)-->

## 行銷活動標籤 {#campaign-global-objectives}

### 傳遞 {#delivery-global-objectives}

<!--
![](assets/campaign_report_global_1.png)
-->

**[!UICONTROL 行銷活動的統計資料]** Widget會詳細說明與您的行銷活動相關的主要資訊：

* **[!UICONTROL 已輸入設定檔]**：開始歷程的設定檔數目。

* **[!UICONTROL 已傳遞的動作]**：歷程中某個動作已傳遞的不重複總次數。

* **[!UICONTROL 動作在%]**&#x200B;中失敗：歷程中動作失敗的不重複次數與動作傳送的不重複次數總數比較。

### 目標報表 {#objective-global}

>[!AVAILABILITY]
>
>**目標報告**&#x200B;功能目前僅可用於一組組織（可用性限制）。 如需詳細資訊，請聯絡您的 Adobe 代表。

![](assets/performance_report.gif)

**[!UICONTROL 目標]**&#x200B;索引標籤可讓您以一個特定量度為目標，以更好地調整傳遞的報告。

列出的&#x200B;**[!UICONTROL 目標]**&#x200B;連結到定義系統連線的&#x200B;**[!UICONTROL 資料集]**，以擷取其他資訊。 內建&#x200B;**[!UICONTROL 目標]**&#x200B;清單可供使用，但您可以新增新的&#x200B;**[!UICONTROL 資料集]**&#x200B;來新增您自己的目標。 如需詳細程式，請參閱此[區段](../reports/reporting-configuration.md)。

選取您要鎖定的目標之後，兩個&#x200B;**[!UICONTROL 效能總覽]**&#x200B;和&#x200B;**[!UICONTROL 行銷活動目標]** Widget將提供您傳遞效能的詳細摘要。

使用&#x200B;**[!UICONTROL 行銷活動目標]** Widget，您也可以選擇將主要目標與其他量度比較。

### 實驗報告 {#experimentation-global-objectives}

<!--
![](assets/experimentation_report_3.png)
-->

**[!UICONTROL Experimentation]**&#x200B;索引標籤提供每個變體效能的重要深入分析，並識別最成功的變體。

請注意，定義績效最佳者可能需要一些時間，其將以此圖示![](assets/experimentation_report_1.png)表示。

+++進一步瞭解Experimentation報表中可用的不同量度和Widget。

**[!UICONTROL 實驗結果]** Widget詳細說明每個變體的效能。 您可以從&#x200B;**[!UICONTROL 基準]**&#x200B;下拉式清單中選取一個處理方式，以變更基準。 最佳處理方式會以星形圖示表示。

此表格會顯示下列量度：

* **[!UICONTROL 提升度超過基準線]**：測量指定處理的轉換率超過基準線的改善百分比。

* **[!UICONTROL 信賴度]**：指定處理與基準處理相同的證據。 [了解更多](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 不重複傳出點按次數]**：跨傳出管道的點按總數。

* **[!UICONTROL 設定檔]**：針對此處理的設定檔數目。

* **[!UICONTROL 不重複傳出點按次數/設定檔]**：建立實驗時先前選取的成功量度總值除以設定檔數目。

**[!UICONTROL 信賴區間]**&#x200B;圖表會測量改善的不確定性。 它詳細說明基準線和最佳執行處理之間的效能百分比差異。 [了解更多](../content-management/experiment-calculations.md#confidence-intervals)。
+++

如需深入瞭解這些結果以及如何解譯，請參閱[此頁面](../content-management/get-started-experiment.md#interpret-results)。
