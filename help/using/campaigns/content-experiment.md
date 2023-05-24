---
solution: Journey Optimizer
product: journey optimizer
title: 建立內容實驗
description: 瞭解如何在您的活動中建立內容實驗
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: 內容、實驗、多重、受眾、治療
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="Informative"
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 10%

---

# 建立內容實驗 {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="內容實驗"
>abstract="您可以選擇改變傳遞內容、主題或寄件者，以便定義多種傳遞處理方式並確定最適合您的對象的組合。"

>[!BEGINSHADEBOX]

本文件提供下列內容：

* [開始使用內容實驗](get-started-experiment.md)
* **[建立內容實驗](content-experiment.md)**
* [瞭解統計計算](experiment-calculations.md)
* [設定實驗報告](reporting-configuration.md)
* [實驗報告中的統計計算](experiment-report-calculations.md)

>[!ENDSHADEBOX]

Journey Optimizer內容實驗使您能夠定義多個交付處理，以便衡量哪一種處理對目標受眾的效果最佳。 您可以選擇更改傳遞內容、主題或發件人。 興趣的受眾被隨機地分配到每個治療中，以確定哪個在指定的度量方面最有效。

>[!NOTE]
>
>在開始內容實驗之前，請確保已為自定義資料集設定報告配置。 請參閱[此章節](reporting-configuration.md)深入瞭解。

在下例中，交貨目標已分解為兩個組，每個組佔目標人口的45%，而拒絕組佔10%，他們將不接收交貨。

目標受眾中的每個人將收到一個版本的電子郵件，其主題行是以下兩個版本之一：

* 直接宣傳新系列和形象10%的報價。
* 另一個只是在沒有任何影像的情況下，在沒有指定10%的折扣的情況下，宣傳特價。

此處的目標是查看收件人是否會根據收到的實驗與電子郵件進行交互。 因此，我們將選擇 **[!UICONTROL 開啟電子郵件]** 作為本內容實驗中的主要目標度量。

![](assets/content_experiment.png)

## 建立市場活動 {#campaign-experiment}

1. 從 **[!UICONTROL 市場活動]** 的 **[!UICONTROL 建立市場活動]**。

   ![](assets/content_experiment_1.png)

<!--
1. In the **[!UICONTROL Properties]** section, choose your **[!UICONTROL Campaign type]**:

    * **[!UICONTROL Scheduled]**: designed to send marketing messages and can be executed immediately or at a specified date.

    * **[!UICONTROL API-Triggered]**: designed to send transactional messages, such as password reset notifications or cart abandonment reminders. 
    
        To execute an API-triggered campaign, you will need to make an API call. [Learn more](api-triggered-campaigns.md)
-->
1. 選擇您的頻道，然後 **[!UICONTROL 曲面]** 要用於此交貨，請按一下 **[!UICONTROL 建立]**。 有關詳細資訊，請參閱 [通道曲面](../configuration/channel-surfaces.md) 的子菜單。

   ![](assets/content_experiment_2.png)

1. 設定 **[!UICONTROL 屬性]** 您的交貨：
   * **[!UICONTROL 名稱]**
   * **[!UICONTROL 說明]**

1. 定義目標受眾。 要執行此操作，請按一下 **[!UICONTROL 選擇受眾]** 按鈕來顯示可用的Adobe Experience Platform段清單。 [瞭解有關網段的更多資訊](../segment/about-segments.md)

   在 **[!UICONTROL 標識命名空間]** 欄位中，選擇要用於標識選定段中的個體的命名空間。 [了解更多](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. 在 **[!UICONTROL 動作跟蹤]** 部分，指定是否跟蹤收件人對交貨的反應：您可以跟蹤點擊和/或開啟。

   市場活動一旦執行，便可以從市場活動報告訪問跟蹤結果。

1. 要在特定日期或循環頻率上執行市場活動，請配置 **[!UICONTROL 計畫]** 的子菜單。 [了解更多](create-campaign.md)

1. 按一下 **[!UICONTROL 編輯內容]** 開始個性化交付。 [了解更多](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. 從 **[!UICONTROL 編輯內容]** 窗口，開始個性化處理A。

   對於此處理，我們將直接在主題行中指定特別優惠並添加個性化。

   ![](assets/content_experiment_5.png)

## 配置內容實驗 {#configure-experiment}

1. 當您的交付個性化時，從「市場活動摘要」頁面，按一下 **[!UICONTROL 建立實驗]** 開始配置內容實驗。

   ![](assets/content_experiment_3.png)

1. 選擇 **[!UICONTROL 成功度量]** 你想為你的實驗做準備。

   為了實驗，我們選擇 **[!UICONTROL 開啟電子郵件]** test：如果促銷代碼在主題行中，收件人將開啟其電子郵件。

   ![](assets/content_experiment_11.png)

1. 按一下 **[!UICONTROL 添加處理]** 創造所需的新療法。

   ![](assets/content_experiment_8.png)

1. 更改 **[!UICONTROL 標題]** 來讓他們更加與眾不同。

1. 選擇以添加 **[!UICONTROL 保持]** 組到您的交貨。 此組將不會從此市場活動接收任何內容。

   開啟切換欄將自動佔用人口的10%，如果需要，您可以調整此百分比。

   ![](assets/content_experiment_12.png)

1. 然後，您可以選擇為每個 **[!UICONTROL 治療]** 或者乾脆開啟 **[!UICONTROL 均勻分佈]** 切換欄。

   ![](assets/content_experiment_13.png)

1. 按一下 **[!UICONTROL 建立]** 的子菜單。

## 設計您的治療 {#treatment-experiment}

1. 從 **[!UICONTROL 編輯內容]** 的子菜單。

   在此處，我們選擇不在 **[!UICONTROL 主題行]**。

   ![](assets/content_experiment_18.png)

1. 按一下 **[!UICONTROL 編輯電子郵件正文]** 進一步個性化你的治療B

   ![](assets/content_experiment_9.png)

1. 在設計治療後，按一下 **[!UICONTROL 更多操作]** 訪問與您的治療相關的選項： **[!UICONTROL 更名]**。 **[!UICONTROL 重複]** 和 **[!UICONTROL 刪除]**。

   ![](assets/content_experiment_7.png)

1. 如果需要，請訪問 **[!UICONTROL 實驗設定]** 按鈕。

   ![](assets/content_experiment_19.png)

1. 定義消息內容後，按一下 **[!UICONTROL 模擬內容]** 按鈕以控制交付內容的呈現，並使用test配置檔案檢查個性化設定。 [了解更多](../email/preview.md)

1. 內容實驗準備好後，從「市場活動」摘要頁面中，您可以按一下 **[!UICONTROL 複查以激活]** 顯示市場活動的摘要。 如果任何參數不正確或缺少，則顯示警報。

   ![](assets/content_experiment_15.png)

1. 檢查市場活動配置是否正確，然後按一下 **[!UICONTROL 激活]** 啟動它。

   ![](assets/content_experiment_14.png)

在配置了您的試驗和促銷活動後，您可以通過「促銷活動」報告跟蹤交付的成功。

## 目標報告 {#objectives-global}

>[!AVAILABILITY]
>
>「內容」實驗功能目前僅適用於一組組織（有限可用性）。 如需詳細資訊，請聯絡您的 Adobe 代表。

![](assets/performance_report.gif)

的 **[!UICONTROL 目標]** 「促銷活動」報告的標籤允許您通過確定一個特定指標來更好地調整交貨報告。

的 **[!UICONTROL 目標]** 列出 **[!UICONTROL 資料集]** 定義與系統的連接以檢索附加資訊。 內置清單 **[!UICONTROL 目標]** 可用，但您可以通過添加新 **[!UICONTROL 資料集]**。 有關詳細過程，請參閱 [節](reporting-configuration.md)。

選擇要針對的目標後， **[!UICONTROL 效能概述]** 和 **[!UICONTROL 市場活動目標]** 小部件將提供交付效能的詳細摘要。

使用 **[!UICONTROL 市場活動目標]** 小部件，您還可以選擇將主目標與其他度量進行比較。

請注意，如果需要，可以調整每個小部件的大小並將其刪除。 有關此的詳細資訊，請參閱此 [節](../reports/global-report.md#modify-dashboard)。

## 試驗報告 {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="成功量度"
>abstract="先前在建立實驗時選取的成功量度的總值除以設定檔的數量。"

>[!AVAILABILITY]
>
>「內容」實驗功能目前僅適用於一組組織（有限可用性）。 如需詳細資訊，請聯絡您的 Adobe 代表。

![](assets/experimentation_report_3.png)

從您的活動 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL 實驗]** 頁籤詳細列出與每個變型的執行方式以及是否存在最佳執行者相關的主要資訊。

請注意，定義最佳執行者可能需要一些時間，它將由此表徵圖表示 ![](assets/experimentation_report_1.png)。

的 **[!UICONTROL 實驗結果]** 小部件詳細列出每個變數的效能。 通過從 **[!UICONTROL 基線]** 下拉。 最佳治療方式將用星形表徵圖來表示。

該表顯示以下度量：

* **[!UICONTROL 配置檔案]**:針對此治療的配置檔案數。

* **[!UICONTROL 唯一的出站按一下]**:出站通道上的按一下總數。

* **[!UICONTROL 每個配置檔案的計數]**:實驗目標度量的總值除以輪廓數。

* **[!UICONTROL 置信區間]**:基線與最佳處理之間效能差異的百分比。 [了解更多](../campaigns/experiment-calculations.md#confidence-intervals)。

* **[!UICONTROL 平均升力]**:給定治療的轉換率比基線提高百分比。 [了解更多](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL 信心]**:有證據表明，某一治療與基準治療相同。 [了解更多](../campaigns/experiment-calculations.md#understand-confidence)

有關這些結果的深入瞭解和解釋方法，請參閱 [此頁](../campaigns/get-started-experiment.md#interpret-results)。
