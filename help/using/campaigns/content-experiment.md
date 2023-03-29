---
solution: Journey Optimizer
product: journey optimizer
title: 建立內容實驗
description: 了解如何在行銷活動中建立內容實驗
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: 內容，實驗，多個，觀眾，治療
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="Informity"
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 9%

---

# 建立內容實驗 {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="內容實驗"
>abstract="您可以選擇改變傳遞內容、主題或寄件者，以便定義多種傳遞處理方式並確定最適合您的對象的組合。"

>[!BEGINSHADEBOX]

本檔案提供下列內容：

* [開始使用內容實驗](get-started-experiment.md)
* **[建立內容實驗](content-experiment.md)**
* [瞭解統計計算](experiment-calculations.md)
* [設定實驗報告](reporting-configuration.md)
* [實驗報告中的統計計算](experiment-report-calculations.md)

>[!ENDSHADEBOX]

Journey Optimizer內容實驗可讓您定義多個傳送處理，以測量哪個處理對目標對象執行效果最佳。 您可以選擇變更傳送內容、主旨或寄件者。 興趣對象會隨機分配給每個處理，以決定哪個處理對指定量度最有效。

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

<!--
1. In the **[!UICONTROL Properties]** section, choose your **[!UICONTROL Campaign type]**:

    * **[!UICONTROL Scheduled]**: designed to send marketing messages and can be executed immediately or at a specified date.

    * **[!UICONTROL API-Triggered]**: designed to send transactional messages, such as password reset notifications or cart abandonment reminders. 
    
        To execute an API-triggered campaign, you will need to make an API call. [Learn more](api-triggered-campaigns.md)
-->
1. 選取您的管道，然後 **[!UICONTROL 曲面]** 您要用於此傳送，然後按一下 **[!UICONTROL 建立]**. 有關詳細資訊，請參閱 [通道曲面](../configuration/channel-surfaces.md) 頁面。

   ![](assets/content_experiment_2.png)

1. 設定 **[!UICONTROL 屬性]** 傳送時：
   * **[!UICONTROL 名稱]**
   * **[!UICONTROL 說明]**

1. 定義要鎖定的對象。 若要這麼做，請按一下 **[!UICONTROL 選取對象]** 按鈕以顯示可用的Adobe Experience Platform區段清單。 [深入了解區段](../segment/about-segments.md)

   在 **[!UICONTROL 身分命名空間]** 欄位中，選擇要使用的命名空間，以識別所選區段中的個人。 [了解更多](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. 在 **[!UICONTROL 動作追蹤]** 區段中，指定是否要追蹤收件者對您傳送的反應：您可以追蹤點按和/或開啟次數。

   執行促銷活動後，即可從促銷活動報表存取追蹤結果。

1. 若要在特定日期或循環頻率上執行促銷活動，請設定 **[!UICONTROL 排程]** 區段。 [了解更多](create-campaign.md)

1. 按一下 **[!UICONTROL 編輯內容]** 開始個人化傳遞。 [了解更多](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. 從 **[!UICONTROL 編輯內容]** 窗口，開始個性化處理A。

   對此處理，我們將直接在主旨行中指定特殊優惠方案，並新增個人化。

   ![](assets/content_experiment_5.png)

## 設定內容實驗 {#configure-experiment}

1. 當您的傳送個人化時，請從促銷活動摘要頁面，按一下 **[!UICONTROL 建立實驗]** 以開始設定內容實驗。

   ![](assets/content_experiment_3.png)

1. 選取 **[!UICONTROL 成功量度]** 想要為實驗設定。

   針對我們的實驗，我們選取 **[!UICONTROL 電子郵件開啟]** 以測試收件者是否會在促銷代碼位於主旨行中時開啟其電子郵件。

   ![](assets/content_experiment_11.png)

1. 按一下 **[!UICONTROL 添加處理]** 來創造所需的新治療。

   ![](assets/content_experiment_8.png)

1. 變更 **[!UICONTROL 標題]** 以便更好地區化。

1. 選擇以新增 **[!UICONTROL 鑒效組]** 群組至您的傳送。 此群組將不會接收來自此促銷活動的任何內容。

   開啟切換列會自動取用您10%的母體，您可以視需要調整此百分比。

   ![](assets/content_experiment_12.png)

1. 然後，您可以選擇將精確百分比分配給每個 **[!UICONTROL 治療]** 或直接開啟 **[!UICONTROL 均勻分配]** 切換欄。

   ![](assets/content_experiment_13.png)

1. 按一下 **[!UICONTROL 建立]** 設定時。

## 設計您的治療方案 {#treatment-experiment}

1. 從 **[!UICONTROL 編輯內容]** 窗口，選擇處理B以更改內容。

   在此，我們選擇不指定 **[!UICONTROL 主旨行]**.

   ![](assets/content_experiment_18.png)

1. 按一下 **[!UICONTROL 編輯電子郵件內文]** 進一步個性化治療B。

   ![](assets/content_experiment_9.png)

1. 在設計處理之後，按一下 **[!UICONTROL 更多動作]** 要訪問與治療相關的選項： **[!UICONTROL 重新命名]**, **[!UICONTROL 複製]** 和 **[!UICONTROL 刪除]**.

   ![](assets/content_experiment_7.png)

1. 如有需要，請存取 **[!UICONTROL 實驗設定]** 的子菜單。

   ![](assets/content_experiment_19.png)

1. 定義訊息內容後，按一下 **[!UICONTROL 模擬內容]** 按鈕，控制傳遞的呈現，並使用測試設定檔檢查個人化設定。 [了解更多](../email/preview.md)

1. 內容實驗準備就緒後，從促銷活動摘要頁面，按一下 **[!UICONTROL 審核以激活]** 顯示促銷活動摘要。 如果有任何參數不正確或遺失，則會顯示警報。

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

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="成功量度"
>abstract="先前在建立實驗時選取的成功量度的總值除以設定檔的數量。"

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
