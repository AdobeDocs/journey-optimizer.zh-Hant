---
solution: Journey Optimizer
product: journey optimizer
title: 存取及管理協調式行銷活動
description: 瞭解使用Adobe Journey Optimizer建立協調行銷活動的主要原則
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: 979b46eccf77db6e90cd47ceb7a40298bb481cc5
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 24%

---

# 存取及管理協調式行銷活動 {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="協調的行銷活動"
>abstract="在此畫面中，您可以存取協調的行銷活動的完整清單、檢查其目前狀態、上次/下次執行日期，並建立新的協調的行銷活動。"

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](configuration-steps.md)<br/><br/><b>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)</b> | [建立協調行銷活動的關鍵步驟](gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[傳送包含協調行銷活動的訊息](send-messages.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建置對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## 存取協調的行銷活動

導覽至「**[!UICONTROL 行銷活動]**」功能表，然後選取「**[!UICONTROL 協調流程]**」索引標籤以存取協調行銷活動的完整清單。

![影像顯示協調的行銷活動詳細目錄](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

清單中每個協調的行銷活動都會顯示資訊，例如行銷活動的目前[狀態](#status)、相關頻道和標籤，或上次修改行銷活動的時間。 您可以按一下![設定配置按鈕](assets/do-not-localize/inventory-configure-layout.svg)按鈕來自訂顯示的欄。

此外，還可使用搜尋列和篩選器，以便於在清單中輕鬆搜尋。例如，您可以篩選已協調的行銷活動，以僅顯示與指定頻道或標籤相關聯的行銷活動，或顯示在特定日期範圍內建立的行銷活動。

## 策劃的行銷活動內含哪些內容？ {#gs-ms-campaign-inside}

精心安排的行銷活動畫布可呈現預期的情形。 其會說明要執行的各種任務以及任務如何連結在一起。

![影像顯示協調的行銷活動畫布](assets/canvas-example.png){zoomable="yes"}{zoomable="yes"}

每個協調的行銷活動包含：

* **活動**：活動指要執行的任務。各種活動在圖表中會以圖示表示。每種活動都有特定屬性和所有活動共有的其他屬性。

  在協調的行銷活動圖表中，特定活動可產生多個任務，尤其是當有回圈或重複動作時。

* **轉變**：轉變會將來源活動連結到目標活動並定義其序列。

* **工作表**：工作表包含轉變攜帶的所有資訊。每個協調的行銷活動都使用數個工作表。 這些表格中傳送的資料可在整個協調行銷活動的生命週期中使用。

## 行銷活動狀態 {#status}

協調的行銷活動可以有多種狀態：

* **[!UICONTROL 草稿]**：已建立協調的行銷活動。 尚未發佈。
* **[!UICONTROL 發佈]**：正在發佈協調的行銷活動。
* **[!UICONTROL 即時]**：已發佈且正在執行協調的行銷活動。
* **[!UICONTROL 已排程]**：已排程協調的行銷活動執行。
* **[!UICONTROL 已完成]**：協調的行銷活動執行已完成。
  <!--* **[!UICONTROL Closed]**: The orchestrated campaign xxxx-->
* **[!UICONTROL 已封存]**：已封存協調的行銷活動。 所有已封存的行銷活動都會在最後修改日期後30天以滾動方式重新排程刪除。 您可以複製已封存的行銷活動（如有必要），以繼續處理。
* **[!UICONTROL 已停止]**：已停止協調的行銷活動執行。 若要啟動行銷活動，您必須複製它。

## 複製和刪除協調的行銷活動 {#duplicate-delete}

在某些情況下，您可能需要複製協調的行銷活動，例如執行已停止的行銷活動，或變更排程行銷活動的執行頻率。 若要這麼做，請按一下行銷活動詳細目錄中顯示[更多動作]按鈕![&#128279;](assets/do-not-localize/rule-builder-icon-more.svg)按鈕的影像，然後選取&#x200B;**[!UICONTROL 複製]**

若要刪除行銷活動，請按一下顯示[更多動作]按鈕![&#128279;](assets/do-not-localize/rule-builder-icon-more.svg)按鈕的影像，然後選取&#x200B;**[!UICONTROL 刪除]**。

>[!NOTE]
>
>只能刪除&#x200B;**[!UICONTROL 草稿]**&#x200B;行銷活動。
