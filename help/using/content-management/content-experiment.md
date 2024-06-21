---
solution: Journey Optimizer
product: journey optimizer
title: 建立內容實驗
description: 瞭解如何在行銷活動中建立內容實驗
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: 內容，實驗，多個，對象，處理
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 13%

---

# 建立內容實驗 {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="內容實驗"
>abstract="您可以選擇改變訊息內容、主題或寄件者，以便定義多種處理方式並確定最適合您的對象的組合。"

>[!NOTE]
>
>開始內容實驗之前，請確定您的報告設定已針對自訂資料集設定。 請參閱[此章節](reporting-configuration.md)深入瞭解。

Journey Optimizer內容實驗可讓您定義多種傳送處理方式，以衡量哪種方式最適合您的目標對象。 您可以選擇變更傳遞內容、主旨或寄件者。 感興趣的對象會隨機分配給每個處理，以決定哪個處理在指定量度方面效果最佳。

![](../rn/assets/do-not-localize/experiment.gif)

在下列範例中，傳遞目標已分割為兩個群組，分別代表目標人口的45%，以及不會收到傳遞的保留群組10%。

目標對象中的每個人都會收到一個版本的電子郵件，主旨列是以下兩個版本之一：

* 直接促銷新系列和影像的10%優惠方案。
* 另一個則只會宣傳特殊優惠方案，未指定任何影像的10%優惠。

此處的目標是檢視收件者是否會根據收到的實驗與電子郵件互動。 因此，我們將選擇 **[!UICONTROL 電子郵件開啟次數]** 作為此內容實驗中的主要目標量度。

![](assets/content_experiment.png)

## 建立您的內容 {#campaign-experiment}

1. 從建立和設定您的電子郵件、簡訊或推播通知開始 [行銷活動](../campaigns/create-campaign.md) 或 [歷程](../building-journeys/journeys-message.md) 根據您的需求。

   >[!AVAILABILITY]
   >
   >歷程中的實驗目前僅適用於一組組織（可用性限制）。 若要取得存取權，請和您的 Adobe 代表聯絡。

1. 從 **[!UICONTROL 編輯內容]** 視窗，開始個人化處理A。

   針對此處理方式，我們將直接在主旨行中指定特殊優惠方案，並新增個人化。

   ![](assets/content_experiment_5.png)

1. 建立或匯入原始內容，並視需要加以個人化。

## 設定您的內容實驗 {#configure-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_dimension"
>title="維度"
>abstract="選擇用於追蹤實驗的特定維度，例如特定頁面的特定點擊數或瀏覽數。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_success_metric"
>title="成功量度"
>abstract="成功量度用於追蹤和評估實驗中表現最佳的處理。在使用之前，請務必針對特定量度設定資料集。"

1. 當您的訊息已個人化時，從行銷活動摘要頁面，按一下 **[!UICONTROL 建立實驗]** 以開始設定您的內容實驗。

   ![](assets/content_experiment_3.png)

1. 選取 **[!UICONTROL 成功量度]** 您想要為實驗設定。

   在此範例中，選取 **[!UICONTROL 電子郵件開啟]** 以測試設定檔是否會開啟其電子郵件（如果促銷代碼在主題行中）。

   ![](assets/content_experiment_11.png)

1. 使用應用程式內或網頁通道設定實驗，然後選擇 **[!UICONTROL 傳入點按次數]**， **[!UICONTROL 不重複傳入點按次數]** ， **[!UICONTROL 頁面檢視]** ，或 **[!UICONTROL 不重複頁面檢視量度]** ，則 **[!UICONTROL 點按動作]**  下拉式清單可讓您精確追蹤和監控特定頁面上的點按次數和檢視次數。

   ![](assets/content_experiment_20.png)

1. 按一下 **[!UICONTROL 新增處理方式]** 以建立所需數量的新處理。

   ![](assets/content_experiment_8.png)

1. 變更 **[!UICONTROL 標題]** 以更能區分您的治療方式。

1. 選擇以新增 **[!UICONTROL 保留樣本]** 群組至您的傳遞。 此群組將不會收到來自此行銷活動的任何內容。

   切換列會自動取得母體的10%，您可以視需要調整此百分比。

   >[!IMPORTANT]
   >
   >當在動作中使用保留群組進行內容實驗時，保留指派僅適用於該特定動作。 動作完成後，保留群組中的設定檔將繼續沿歷程路徑前進，並可接收其他動作的訊息。 因此，請確保任何後續的訊息不依賴可能位於保留群組內的設定檔所接收的訊息。 如果是，您可能需要移除保留組指派。

   ![](assets/content_experiment_12.png)

1. 然後，您可以選擇將精確百分比分配給每個 **[!UICONTROL 處理]** 或直接開啟 **[!UICONTROL 平均分配]** 切換列。

   ![](assets/content_experiment_13.png)

1. 按一下 **[!UICONTROL 建立]** 設定您的設定時。

## 設計您的處理方式 {#treatment-experiment}

1. 從 **[!UICONTROL 編輯內容]** 視窗中，選取您的處理B以變更內容。

   在此，我們選擇不指定 **[!UICONTROL 主旨列]**.

   ![](assets/content_experiment_18.png)

1. 按一下 **[!UICONTROL 編輯電子郵件內文]** 以進一步個人化您的處理方式B。

   ![](assets/content_experiment_9.png)

1. 設計處理方式後，按一下 **[!UICONTROL 更多動作]** 若要存取與處理相關的選項： **[!UICONTROL 重新命名]**， **[!UICONTROL 複製]** 和 **[!UICONTROL 刪除]**.

   ![](assets/content_experiment_7.png)

1. 如有需要，請存取 **[!UICONTROL 實驗設定]** 功能表以變更您的處理設定。

   ![](assets/content_experiment_19.png)

1. 定義訊息內容後，按一下 **[!UICONTROL 模擬內容]** 按鈕來控制傳遞的呈現，並使用測試設定檔檢查個人化設定。 [了解更多](../content-management/preview-test.md)

設定實驗後，您可以在報表中追蹤傳送成功。 [了解更多](../reports/campaign-global-report.md#experimentation-report)
