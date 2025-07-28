---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer開始和監視協調的行銷活動
description: 瞭解如何使用Adobe Journey Optimizer開始及監控協調的行銷活動。
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 56%

---

# 開始和監視您的協調行銷活動 {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="發佈協調的行銷活動"
>abstract="若要開始您的行銷活動，您必須發佈該活動。在發佈前，請確定所有錯誤都已清除。"

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](gs-schemas.md)</li><li>[手動結構描述](manual-schema.md)</li><li>[檔案上傳結構描述](file-upload-schema.md)</li><li>[擷取資料](ingest-data.md)</li></ul>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/><b>[開始並監視行銷活動](start-monitor-campaigns.md)</b><br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[同時加入](activities/and-join.md) - [建立客群](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調和](activities/reconciliation.md) - [儲存客群](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

您建立了協調的行銷活動並設計了要在畫布中執行的任務後，即可發佈並監視其執行方式。

您也可以在測試模式下執行行銷活動，以檢查其執行和不同活動的結果。

## 發佈前測試您的行銷活動 {#test}

[!DNL Journey Optimizer]可讓您在開始使用前測試協調的行銷活動。 建立行銷活動時，預設會進入&#x200B;**草稿**&#x200B;狀態。 在此狀態下，您可以手動執行行銷活動以測試流量。

>[!IMPORTANT]
>
>畫布中的所有活動都會執行，但&#x200B;**[!UICONTROL 儲存對象]**&#x200B;活動和頻道活動除外。 對您的資料或對象沒有功能上的影響。**

若要測試行銷活動：

1. 開啟「協調流程」行銷活動。
2. 按一下「**[!UICONTROL 開始]**」。

![](assets/campaign-start.png){zoomable="yes"}

促銷活動中的每個活動都會依序執行，直到圖表結束為止。

在測試期間，您可以使用畫布中的動作列來控制行銷活動的執行。 從那裡，您可以：

* 隨時&#x200B;**停止**&#x200B;執行。
* 再次&#x200B;**開始**&#x200B;執行。
* **如果先前已暫停執行，則繼續**&#x200B;執行。

畫布工具列中的&#x200B;**[!UICONTROL 警示]** / **[!UICONTROL 警告]**&#x200B;圖示會通知您發生的問題，包括執行之前可能主動出現的警告，以及在執行期間或執行之後發生的錯誤。

![](assets/campaign-warning.png){zoomable="yes"}

您也可以使用直接顯示在每個活動上的[視覺狀態指標](#activities)，快速識別失敗的活動。如需詳細的疑難排解，請開啟[行銷活動的記錄](#logs-tasks)，其中提供有關錯誤及其內容的深入資訊。

<!--WAITING FOR PM's TEST TO UNHIDE

If you have added channel activities in the canvas, you can preview and test the content of your messages using the **[!UICONTROL Simulate Content]** button. [Learn how to work with channel activities](activities/channels.md)

-->

驗證後，即可發佈行銷活動。

## 發佈此行銷活動 {#publish}

在您的行銷活動經過測試且準備就緒後，按一下「**[!UICONTROL 發佈]**」，讓行銷活動上線。

![](assets/campaign-publish.png){zoomable="yes"}

>[!NOTE]
>
>如果&#x200B;**[!UICONTROL 發佈]**&#x200B;按鈕已停用（灰色），請從動作列存取記錄檔並檢查錯誤訊息。 所有錯誤必須先修正，才能發佈行銷活動。

視覺流量會重新啟動，而真實設定檔會開始即時流過歷程。

如果發佈動作失敗（例如，由於缺少訊息內容），您會收到警報，必須在重試之前修正問題。 成功發佈後，行銷活動就會開始執行（立即或依排程）、從&#x200B;**草稿**&#x200B;移至&#x200B;**即時**&#x200B;狀態，並變成「唯讀」。

## 監視行銷活動的執行 {#monitor}

### 視覺流量監視 {#flow}

執行時 (在測試或即時模式下)，視覺流量會顯示設定檔如何即時在歷程中移動。畫面上會顯示任務之間轉變的設定檔數目。

![](assets/workflow-execution.png){zoomable="yes"}

透過轉變從一個活動傳輸到另一個活動的資料會儲存在暫時工作表中。此資料可針對每個轉變顯示。若要檢查在活動之間傳遞的資料：

1. 選取轉變。
1. 在屬性窗格中，按一下「**[!UICONTROL 預覽結構描述]**」以檢視工作表結構描述。選取「**[!UICONTROL 預覽結果]**」以檢視傳輸的資料。

![](assets/transition.png){zoomable="yes"}

### 活動執行指標 {#activities}

視覺狀態指標可協助您了解每個活動的執行方式：

| 視覺指標 | 說明 |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | 活動目前正在執行。 |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | 活動需要您注意。這可能涉及確認傳遞的傳送或採取必要行動。 |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | 活動發生錯誤。若要解決此問題，請開啟協調的活動記錄檔，以取得詳細資訊。 |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | 活動已成功執行。 |

### 記錄和任務 {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="記錄和任務"
>abstract="**記錄檔與工作**&#x200B;畫面提供協調行銷活動執行的歷史記錄，記錄所有使用者動作與遇到的錯誤。"

監視記錄檔和任務是分析協調行銷活動並確保其正常執行的關鍵步驟。 在測試與即時模式下，可從畫布工具列或每個活動的屬性窗格中的「**[!UICONTROL 記錄]**」按鈕，存取記錄和任務。

**[!UICONTROL 記錄和任務]**&#x200B;畫面提供執行行銷活動的完整歷史記錄，其中記錄所有使用者動作和發生的錯誤。

![](assets/workflow-logs.png){zoomable="yes"}

可用的資訊類型有兩種：

* 「**[!UICONTROL 記錄]**」索引標籤包含所有作業和錯誤的時間順序歷史記錄。
* 「**[!UICONTROL 任務]**」索引標籤詳細說明了活動的逐步執行順序。

在這兩個標籤中，您可以選擇顯示的欄及其順序，套用篩選器，並使用搜尋欄位來快速尋找所需的資訊。
