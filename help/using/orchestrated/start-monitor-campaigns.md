---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer開始和監視協調的行銷活動
description: 瞭解如何使用Adobe Journey Optimizer開始及監控協調的行銷活動。
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: f8afef4729e50b7c9899bf7f2fe282347220dfac
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 8%

---

# 開始並監控協調行銷活動 {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="發佈協調的行銷活動"
>abstract="若要開始您的行銷活動，您必須發佈該活動。在發佈前，請確定已經清除所有警告。"

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](configuration-steps.md)<br/><br/>[存取和管理協調的行銷活動](access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[傳送包含協調行銷活動的訊息](send-messages.md)<br/><br/><b>[開始並監視行銷活動](start-monitor-campaigns.md)</b><br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建置對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

一旦您建立了協調流程並設計了要在畫布中執行的任務，您就可以發佈它並監視其執行方式。

您也可以在測試模式下執行行銷活動，以檢查其執行和不同活動的結果。

## 測試並發佈協調的行銷活動 {#test}

Journey Optimizer可讓您在發佈前先測試協調的行銷活動。 這可讓您檢查構成行銷活動的各種任務的執行情況和結果，而不會對功能造成影響：畫布中的所有活動都會執行，但具有影響（例如&#x200B;**[!UICONTROL 儲存對象]**&#x200B;和頻道活動）的活動除外。

若要在測試模式中啟動協調的行銷活動，請開啟協調的行銷活動，然後按一下&#x200B;**[!UICONTROL 開始]**&#x200B;按鈕。

![](assets/campaign-start.png){zoomable="yes"}

一旦執行協調的行銷活動後，畫布中的每個活動就會依序執行，直到達到協調的行銷活動結束為止。

當您的行銷活動準備好上線時，請按一下&#x200B;**[!UICONTROL 發佈]**&#x200B;按鈕。 畫布中的視覺流程會重新啟動，好讓您將設定檔進度放入圖表中。

## 協調的行銷活動視覺流程

當協調的行銷活動執行時，無論是在測試模式或生產模式，您都可以使用視覺流程，即時追蹤不同任務中目標設定檔的進度。 這可讓您快速識別每個活動的狀態，以及活動中轉換的個人檔案數。

![](assets/workflow-execution.png){zoomable="yes"}

透過轉換從一個活動傳輸到另一個活動的資料會儲存在暫時工作表中。 此資料可針對每個轉變顯示。 要執行此操作，請選取轉變以在熒幕右側開啟其屬性。

* 按一下&#x200B;**[!UICONTROL 預覽結構描述]**&#x200B;以顯示工作表的結構描述。
* 按一下&#x200B;**[!UICONTROL 預覽結果]**，以視覺化方式呈現所選轉變中傳輸的資料。

![](assets/transition.png){zoomable="yes"}

## 監視行銷活動的執行

### 監視活動執行 {#activities}

每個活動方塊中的視覺指示器可讓您檢查其執行：

| 視覺指示器 | 說明 |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | 活動目前正在執行。 |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | 活動需要您注意。 這可能涉及確認傳遞的傳送或採取必要行動。 |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | 活動發生錯誤。 若要解決此問題，請開啟協調的行銷活動記錄檔，以取得詳細資訊。 |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | 已成功執行活動。 |

### 監視記錄和任務 {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="記錄和任務"
>abstract="**記錄和任務**&#x200B;畫面提供協調的行銷活動執行歷史記錄，記錄所有使用者動作和發生的錯誤。"

監視記錄檔及工作是分析協調行銷活動並確保其正常執行的關鍵步驟。 可從動作工具列及每個活動屬性窗格中的&#x200B;**[!UICONTROL 記錄檔]**&#x200B;圖示存取。

**[!UICONTROL 記錄檔與工作]**&#x200B;功能表提供協調行銷活動執行的歷程記錄，記錄所有使用者動作和遇到的錯誤。

![](assets/workflow-logs.png){zoomable="yes"}

提供兩種資訊：

* **[!UICONTROL Log]**&#x200B;索引標籤包含所有已協調行銷活動的執行歷程記錄。 其會按時間順序，對執行的操作和執行錯誤進行索引。
* **[!UICONTROL 任務]**&#x200B;索引標籤詳細說明活動的執行順序。

在這兩個標籤中，您可以選擇顯示的欄及其順序、套用篩選器，並使用搜尋欄位來快速尋找所需的資訊。

## 協調的行銷活動執行命令 {#execution-commands}

右上角的動作列提供可讓您管理協調行銷活動執行的命令。 您可以：

* **[!UICONTROL 開始]** / **[!UICONTROL 繼續]**&#x200B;執行   已協調的行銷活動，接著會採取進行中狀態。 如果協調的行銷活動已暫停，則會繼續，否則會啟動行銷活動，然後啟動初始活動。

* **[!UICONTROL 暫停]**&#x200B;執行協調的行銷活動，接著會呈現「已暫停」狀態。 在繼續之前，不會啟用任何新活動，但不會暫停進行中的作業。

* **[!UICONTROL 停止]**&#x200B;正在執行的協調行銷活動，其狀態會變成「已完成」。 如果可能的話，進行中的作業會被中斷。 您無法從已停止的同一個位置繼續從協調的行銷活動。
