---
solution: Journey Optimizer
product: journey optimizer
title: 區段資格事件
description: 瞭解區段資格事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 資格，事件，區段，歷程，平台
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 10%

---

# 區段資格事件 {#segment-qualification}

## 關於區段資格事件{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="區段資格事件"
>abstract="本活動可讓您的歷程聆聽 Adobe Experience Platform 區段中設定檔的入口和出口，讓個人得以在歷程中進入或前進。"

本活動可讓您的歷程聆聽 Adobe Experience Platform 區段中設定檔的入口和出口，讓個人得以在歷程中進入或前進。如需區段建立的詳細資訊，請參閱本節 [區段](../segment/about-segments.md).

假設您有「銀級客戶」區段。 透過此活動，您可以讓所有新的銀級客戶進入歷程，並向他們傳送一系列個人化訊息。

此類事件可定位為歷程的第一步或後續步驟。

>[!IMPORTANT]
>
>請記住，Adobe Experience Platform區段每天計算一次(**批次** 區段)或即時(**串流** 區段(使用Adobe Experience Platform的「高頻對象」選項)。
>
>如果選取的區段經過串流處理，則屬於此區段的個人可能會即時進入歷程。 如果區段為批次，則新符合此區段資格的人可能會在Adobe Experience Platform上執行區段計算時進入歷程。
>
>從「讀取」區段、「區段」資格或業務事件活動開始的歷程中，無法使用體驗事件欄位群組。 


1. 展開 **[!UICONTROL 事件]** 類別與放置 **[!UICONTROL 區段資格]** 活動放入您的畫布。

   ![](assets/segment5.png)

1. 新增 **[!UICONTROL 標籤]** 至活動。 此步驟為選填。

1. 按一下 **[!UICONTROL 區段]** 欄位並選取您要運用的區段。

   >[!NOTE]
   >
   >請注意，您可以自訂清單中顯示的欄並加以排序。

   ![](assets/segment6.png)

   新增區段後， **[!UICONTROL 複製]** 按鈕可讓您複製其名稱和ID：

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. 在 **[!UICONTROL 行為]** 欄位，選擇您要監聽區段入口、出口或兩者。

   >[!NOTE]
   >
   >請注意 **[!UICONTROL 輸入]** 和 **[!UICONTROL 退出]** 對應至 **已實現** 和 **已退出** 來自Adobe Experience Platform的區段參與狀態。 如需如何評估區段的詳細資訊，請參閱 [Segment Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. 選取名稱空間。 只有在將事件定位為歷程的第一步時，才需要此專案。 依預設，欄位會使用上次使用的名稱空間預先填入。

   >[!NOTE]
   >
   >您只能選取以人物為基礎的身分名稱空間。 如果您已定義查閱表格的名稱空間（例如：產品查閱的ProductID名稱空間），它將無法在 **名稱空間** 下拉式清單。

   ![](assets/segment7.png)

裝載包含下列內容資訊，您可在條件和動作中使用：

* 行為（入口、出口）
* 資格的時間戳記
* 區段id

在後續的條件或動作中使用運算式編輯器時 **[!UICONTROL 區段資格]** 活動，則您可存取 **[!UICONTROL 區段資格]** 節點。 您可以選擇 **[!UICONTROL 上次合格時間]** 和 **[!UICONTROL 狀態]** （進入或退出）。

另請參閱 [條件活動](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

包含區段資格事件的新歷程在發佈十分鐘後即可運作。 此時間間隔對應於專用服務的快取重新整理間隔。 因此，您必須等待十分鐘才能使用此歷程。

## 最佳做法 {#best-practices-segments}

此 **[!UICONTROL 區段資格]** 活動可讓在Adobe Experience Platform區段中取得資格或被取消資格的個人在歷程中立即進入。

此資訊的接收速度很快。 所做的測量顯示速度為每秒接收10,000個事件。 因此，您應該確保瞭解入口尖峰可能如何發生、如何避免以及如何讓您的歷程準備好迎接它們。

### 批次區段{#batch-speed-segment-qualification}

針對批次區段使用區段資格時，請注意，入口尖峰將發生在每日計算時。 峰值的大小將取決於每天進入（或退出）區段的個人數量。

此外，如果批次區段是新建立並立即用於歷程中，則第一批計算可能會使大量個人進入歷程。

### 串流區段{#streamed-speed-segment-qualification}

針對串流區段使用區段資格時，由於持續評估區段，入口/出口出現大型峰值的風險較低。 然而，如果區段定義導致大量客戶同時符合資格，則也可能出現峰值。

如需串流區段的詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### 如何避免多載{#overloads-speed-segment-qualification}

以下是一些最佳實務，有助於避免在歷程中運用的系統過載（資料來源、自訂動作、管道動作活動）。

請勿使用，在 **[!UICONTROL 區段資格]** 活動，批次區段建立後立即生效。 它會避免第一個計算尖峰。 請注意，如果您即將使用從未計算的區段，歷程畫布中將會出現黃色警告。

![](assets/segment-error.png)

為歷程中使用的資料來源和動作設定上限規則，以避免其過載。 進一步瞭解 [Journey Orchestration檔案](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target="_blank"}. 請注意，上限規則沒有重試。 如果您需要重試，您必須核取方塊，以在歷程中使用替代路徑 **[!UICONTROL 在逾時或錯誤的情況下新增替代路徑]** 在條件或動作中。

在生產歷程中使用區段之前，請務必先評估每天符合此區段資格的個人數量。 若要這麼做，您可以檢查 **[!UICONTROL 區段]** 功能表，開啟區段，然後檢視 **[!UICONTROL 一段時間的設定檔]** 圖表。

![](assets/segment-overload.png)
