---
title: 建立內容實驗
description: 了解如何在行銷活動中建立內容實驗
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: e81e21f714a3c5450defa1129e1e2b9969dc1de7
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 4%

---

# 建立內容實驗 {#content-experiment}

>[!AVAILABILITY]
>
>此 **內容實驗** 功能目前僅適用於一組組織（有限可用性）。 如需詳細資訊，請聯絡您的 Adobe 代表。

使用Journey Optimizer內容實驗來定義多種傳送處理。 將興趣對象隨機分配給每個治療，以確定哪個治療對興趣度量表現最佳。 您可以選擇變更傳送內容、主旨或寄件者。

>[!NOTE]
>
>開始進行內容實驗之前，請確定已為自訂資料集設定報表設定。 請參閱[此章節](reporting-configuration.md)深入瞭解。

在以下範例中，傳送目標已分割為兩個群組，每個群組分別代表目標母體的45%，而拒絕組為10%，不會接收傳送。

目標對象中的每個人都會收到一個版本的電子郵件，主旨行為下列兩者之一：

* 直接宣傳新系列和影像的10%優惠。
* 另一個只廣告特惠，沒有指定10%的優惠，沒有任何影像。

此處的目標是根據收到的實驗，查看收件者是否會與電子郵件互動。 因此，我們將選擇 **[!UICONTROL 電子郵件開啟]** 作為此內容實驗中的主要目標量度。

![](assets/content_experiment.png)

## 建立您的行銷活動 {#campaign-experiment}

1. 從 **[!UICONTROL 行銷活動]** 頁面，按一下 **[!UICONTROL 建立行銷活動]**.

   ![](assets/content_experiment_1.png)

1. 選取您的管道，然後 **[!UICONTROL 曲面]** 您想要用於此傳送。 有關詳細資訊，請參閱 [通道曲面](../configuration/channel-surfaces.md) 頁面。

   ![](assets/content_experiment_2.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 設定 **[!UICONTROL 屬性]** 傳送時：
   * **[!UICONTROL 標題]**
   * **[!UICONTROL 說明]**
   * **[!UICONTROL 類別]**: **[!UICONTROL 行銷]** / **[!UICONTROL 交易]**

1. 若要開始內容實驗，請切換 **[!UICONTROL 內容實驗]** 選項。 此 **[!UICONTROL 內容實驗]** 中。

   ![](assets/content_experiment_3.png)

1. 定義要鎖定的對象。 若要這麼做，請按一下 **[!UICONTROL 選取對象]** 按鈕以顯示可用的Adobe Experience Platform區段清單。 [深入了解區段](../segment/about-segments.md)

   在 **[!UICONTROL 身分命名空間]** 欄位中，選擇要使用的命名空間，以識別所選區段中的個人。 [了解更多](get-started-experiment.md#content-experiment-work)

1. 若要在特定日期或循環頻率執行促銷活動，請設定「排程」區段。 [了解更多](create-campaign.md)

1. 按一下 **[!UICONTROL 編輯內容]** 開始個人化您的不同 **[!UICONTROL 處理]**.

   ![](assets/content_experiment_4.png)

## 建立您的治療方法 {#treatment-experiment}

1. 從 **[!UICONTROL 編輯內容]** 窗口，開始個性化處理A。

   針對此方式，我們會直接在主旨行中指定特別優惠方案。

   ![](assets/content_experiment_5.png)

1. 在設計您的第一個治療之後，從 **[!UICONTROL 更多動作]** 按一下 **[!UICONTROL 複製]**.

   您也可以選擇從頭開始新治療，按一下 **[!UICONTROL 內容實驗]** 按鈕 ![](assets/content_experiment_16.png) 若要存取進階選項， **[!UICONTROL 添加處理]**.

   ![](assets/content_experiment_7.png)

1. 變更 **[!UICONTROL 標題]** 以便更好地區化。

   ![](assets/content_experiment_8.png)

1. 視需要個人化您的第二個處理方式。

   在此，我們選擇不指定 **[!UICONTROL 主旨行]**.

   ![](assets/content_experiment_9.png)

將處理方式個人化後，您就可以開始設定內容實驗。

## 設定內容實驗 {#configure-experiment}

1. 兩個傳送均個人化時，從 **[!UICONTROL 編輯內容]** 窗口，選擇 **[!UICONTROL 設定內容實驗]**.

   ![](assets/content_experiment_10.png)

1. 選取您要為實驗設定的目標。

   針對我們的實驗，我們選取 **[!UICONTROL 電子郵件開啟]** 以測試收件者是否會在促銷代碼位於主旨行中時開啟其電子郵件。

   ![](assets/content_experiment_11.png)

1. 選擇以新增 **[!UICONTROL 鑒效組]** 群組至您的傳送。 此群組將不會接收來自此促銷活動的任何內容。

   開啟切換列會自動取用您10%的母體，您可以視需要調整此百分比。

   ![](assets/content_experiment_12.png)

1. 然後，您可以選擇將精確百分比分配給每個 **[!UICONTROL 治療]** 或直接開啟 **[!UICONTROL 均勻分配]** 切換欄。

   ![](assets/content_experiment_13.png)

1. 按一下 **[!UICONTROL 儲存]** 設定時。

1. 內容實驗準備就緒時，您可以按一下 **[!UICONTROL 審核以激活]** 顯示促銷活動摘要。 如果有任何參數不正確或遺失，則會顯示警報。

   ![](assets/content_experiment_15.png)

1. 檢查促銷活動是否已正確設定，然後按一下 **[!UICONTROL 啟動]** 啟動它。

   ![](assets/content_experiment_14.png)

在設定您的實驗和行銷活動後，您可以透過行銷活動報表追蹤傳送的成功。

## 目標報告 {#objectives-global}

>[!AVAILABILITY]
>
>內容實驗功能目前僅適用於一組組織（有限可用性）。 如需詳細資訊，請聯絡您的 Adobe 代表。

![](assets/performance_report.gif)

此 **[!UICONTROL 目標]** 「促銷活動」報表的標籤，可讓您透過鎖定一個特定量度來更精確地調整傳送的報表。

此 **[!UICONTROL 目標]** 清單連結至 **[!UICONTROL 資料集]** 定義與系統的連接以檢索附加資訊。 內建的清單 **[!UICONTROL 目標]** 可用，但您可以透過新增 **[!UICONTROL 資料集]**. 有關詳細的過程，請參閱 [節](reporting-configuration.md).

選取您要鎖定的目標後，這兩個 **[!UICONTROL 效能概觀]** 和 **[!UICONTROL 促銷活動目標]** 介面工具集將提供傳送效能的詳細摘要。

使用 **[!UICONTROL 促銷活動目標]** 介面工具集，您也可以選擇將主要目標與其他量度進行比較。

請注意，可視需要對每個介面工具集調整大小並刪除。 有關詳細資訊，請參閱 [節](../reports/global-report.md#modify-dashboard).

## 實驗報告 {#experimentation-global}

>[!AVAILABILITY]
>
>內容實驗功能目前僅適用於一組組織（有限可用性）。 如需詳細資訊，請聯絡您的 Adobe 代表。

![](assets/experimentation_report_3.png)

從您的行銷活動 **[!UICONTROL 全域報表]**, **[!UICONTROL 實驗]** 索引標籤會詳細說明與每個變體的執行方式以及是否有最佳執行者相關的主要資訊。

請注意，定義最佳執行者可能需要一些時間，它將用此表徵圖表示 ![](assets/experimentation_report_1.png).

此 **[!UICONTROL 實驗結果]** 介面工具集會詳細說明每個變體的效能。 您可以選取以下其中一個處理方式，以變更基線： **[!UICONTROL 基線]** 下拉式清單。 最佳待遇會以星形圖示表示。

表格顯示下列量度：

* **[!UICONTROL 設定檔]**:針對此處理的設定檔數。

* **[!UICONTROL 不重複的對外點按]**:所有對外管道的點按總數。

* **[!UICONTROL 每個設定檔的計數]**:實驗目標量度的總值除以設定檔數。

* **[!UICONTROL 信賴區間]**:基線與效能最佳處理之間的效能差異百分比。 [了解更多](../campaigns/experiment-calculations.md#confidence-intervals)。

* **[!UICONTROL 平均提升度]**:給定治療的轉換率在基線上的百分比提高。 [了解更多](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL 信賴度]**:有證據表明給予的治療與基線治療相同。 [了解更多](../campaigns/experiment-calculations.md#understand-confidence)

如需深入了解這些結果以及如何解讀，請參閱 [本頁](../campaigns/get-started-experiment.md#interpret-results).
