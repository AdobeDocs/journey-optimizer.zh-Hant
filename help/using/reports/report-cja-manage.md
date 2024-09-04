---
solution: Journey Optimizer
product: journey optimizer
title: 報告新的UI
description: 開始使用報告新介面
feature: Reporting
topic: Content Management
role: User
level: Intermediate
badge: label="限量開放使用" type="Informative"
exl-id: d2ff175a-8bca-4b62-931c-a909cfd9308d
source-git-commit: 9be8b3864a41b37f3a61f24b6e6b54ec184d41aa
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 1%

---

# 管理您的報告 {#channel-cja-manage}

## 在Customer Journey Analytics中分析 {#analyze}

![](assets/cja-analyze.png)

運用所有報告內可用的&#x200B;**[!UICONTROL 在CJA中分析]**&#x200B;功能，使用您的&#x200B;**[!DNL Customer Journey Analytics]**&#x200B;授權增強您的資料分析體驗。

這個功能強大的選項可順暢地將您重新導向至&#x200B;**[!DNL Customer Journey Analytics]**&#x200B;環境，讓您能夠廣泛個人化您的報告。 您可以使用專門的Customer Journey Analytics量度擴充您的Widget，將您的見解提升到全新的境界。

[進一步瞭解Customer Journey Analytics介面。](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-getting-started)

## 定義報告期間 {#report-period}

![](assets/cja-time-period.png)

存取報表時，您可以套用位於報表右上角的時段篩選器。

依預設，行銷活動或歷程的篩選期間會設為其開始和結束日期。 如果沒有結束日期，則篩選器將預設為目前日期。

若要修改篩選器，您可以選取自訂開始日期和持續時間，或從預設集選項（例如上週或兩個月前）中選擇。

套用或修改篩選器後，報表將自動更新。

## 匯出您的報告 {#export-reports}

您可以輕鬆地將不同的報表匯出為PDF或CSV格式，以便共用或列印它們。 匯出報告的步驟會在以下標籤中詳細說明。

>[!BEGINTABS]

>[!TAB 將報表匯出為CSV檔案]

1. 從您的報表按一下[匯出]****，然後選取[CSV檔案]****&#x200B;來產生整體報表層級的CSV檔案。

   ![](assets/export_cja_csv.png)

1. 您的檔案會自動下載，並位於您的本機檔案中。

   如果在報表層級產生檔案，檔案會包含每個Widget的詳細資訊，包括其標題和資料。

>[!TAB 將報表匯出為PDF檔案]

1. 在報表中按一下[匯出]，然後選取[PDF檔案]。********

   ![](assets/export_cja_pdf.png)

1. 要求下載後，按一下&#x200B;**[!UICONTROL 下載]**。

   ![](assets/export_cja_pdf_2.png)

1. 您的檔案會自動在瀏覽器中開啟。

您的報告現在可以檢視、下載或共用pdf檔案。

>[!ENDTABS]

## 建立簡單量度 {#create-simple-metric}

您可以直接在報表中建立自訂計算量度。 您可以結合兩個現有量度，以符合您的特定報告需求，產生更量身打造的深入分析，並更好地分析資料。

1. 首先，存取您要新增量度的報表。

1. 在報表的表格中，按住`Shift`或`CTRL/CMD`鍵，同時按一下所需的量度，加以選取。 然後，按一下滑鼠右鍵並選取&#x200B;**[!UICONTROL 從選取專案建立量度]**。

   如果選取兩個以上的量度，量度產生器中只會使用前兩個量度。

   ![](assets/cja-create-metric_2.png)

1. 在計算量度產生器中，輸入&#x200B;**[!UICONTROL 標題]**&#x200B;欄位以命名您的新量度。 您也可以新增&#x200B;**[!UICONTROL 描述]**。

   >[!NOTE]
   >
   >如果您擁有Customer Journey Analytics，則可使用其他選項進一步個人化您的量度。 [了解更多](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/cm-build-metrics#areas-of-the-calculated-metrics-builder)

1. 選擇適當的&#x200B;**[!UICONTROL 小數位數]**，並根據您希望量度的顯示方式，選取&#x200B;**[!UICONTROL 格式]** （小數、時間、百分比或貨幣）。

1. 選取將決定如何計算量度的運運算元，例如加、減、乘或除。

   ![](assets/cja-create-metric.png)

1. 您可以視需要重新排序元件。

1. 當您對設定感到滿意時，請按一下[套用] ****&#x200B;以完成新量度。

1. 您的新量度會出現在報表中的原始量度旁。

   ![](assets/cja-create-metric_3.png)

將報表匯出為PDF或CSV檔案時，新建立的量度將會包含在內。 不過，一旦您退出，系統就會將其從報表中移除。

## 使用探索分析探索資料 {#exploratory}

使用探索分析工具，從您選取的&#x200B;**[!UICONTROL Dimension]**&#x200B;和&#x200B;**[!UICONTROL 量度]**&#x200B;輕鬆建立表格和視覺效果。 此工具可簡化資料探索，讓您輕鬆自動自訂和分析資訊。 深入瞭解[此檔案](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/quickinsight)。

1. 首先，存取您要使用「探索分析」的報告。

1. 從左側欄選單中選取「探索分析」選單。

   ![](assets/exploratory_analysis_1.png)

1. 使用下拉式功能表選擇&#x200B;**[!UICONTROL Dimension]**&#x200B;和&#x200B;**[!UICONTROL 量度]**，以建立查詢。 如有需要，您也可以選取&#x200B;**[!UICONTROL 區段]**。

   ![](assets/exploratory_analysis_2.png)

1. 定義分析的日期範圍，以指定您要專注的期間。 依預設，日期範圍將設為報表面板中使用的日期範圍。

1. 使用&#x200B;**[!UICONTROL 新增劃分]**&#x200B;或&#x200B;**[!UICONTROL 新增量度]**&#x200B;選項來包含其他維度，以允許更詳細的資料劃分。

   請注意，您最多只能新增三個&#x200B;**[!UICONTROL Dimension]**、**[!UICONTROL 量度]**&#x200B;和&#x200B;**[!UICONTROL 區段]**。

您現在可以使用自訂表格和視覺化工具來分析資料。

<!--## Create a down-funnel metric {#down-funnel}

1. Create a new journey or open an existing one. [Learn more on journey creation](../building-journeys/journey-gs.md)

1. On the canvas editor, select the option to "add a metric".

c. In the metric selector, choose whichever conversion metric seems appropriate and publish your journey

d. Open the report for the journey that you added the metric to and ensure that the metric has been added to the table alongside all the other pre-configured metrics.
-->

## 從報表資料建立對象 {#create-audience}

>[!IMPORTANT]
>
>每個組織僅限發佈25個對象。 此外，使用者每小時最多可發佈5個對象，每天最多可發佈20個

您現在可以選取表格中的特定資料，並從這些選取專案直接建立對象，以精簡及簡化對象建立流程。

1. 首先，導覽至包含您要轉換為對象之資料的報表表格。

1. 用滑鼠右鍵按一下所需的儲存格，然後選取&#x200B;**[!UICONTROL 建立對象]**。

   或者，您可以選取節點，然後按一下滑鼠右鍵，從&#x200B;**[!UICONTROL 歷程畫布]** Widget開始建立對象。

1. 在&#x200B;**[!UICONTROL 建立對象]**&#x200B;視窗中，輸入&#x200B;**[!UICONTROL 名稱]**，並為您計畫發佈的對象設定&#x200B;**[!UICONTROL 一次性日期範圍]**。

   >[!NOTE]
   >
   >如果您擁有Customer Journey Analytics，則可使用其他選項進一步個人化您的量度。 [了解更多](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/audiences/publish)

   ![](assets/audience_1.png)

1. 按一下「**[!UICONTROL 建立]**」按鈕，完成建立對象。 請注意，此程式可能需要一些時間才能完成。

您現在可以繼續將新建立的對象用於歷程或行銷活動。

