---
solution: Journey Optimizer
product: journey optimizer
title: 協調行銷活動建立的關鍵步驟
description: 瞭解使用Adobe Journey Optimizer建立協調行銷活動的主要原則
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 450f83eb53068df10a63d39d1a43483ad3c7e803
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 27%

---


# 協調行銷活動建立的關鍵步驟 {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="協調的行銷活動"
>abstract="在此畫面中，您可以存取協調的行銷活動的完整清單、檢查其目前狀態、上次/下次執行日期，並建立新的協調的行銷活動。"

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調的行銷活動活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](configuration-steps.md)<br/><br/><b>[建立協調行銷活動的重要步驟](gs-campaign-creation.md)</b> | [建立協調的行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調的行銷活動設定](orchestrated-campaign-settings.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[使用協調的行銷活動傳送訊息](send-messages.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建置對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

您可以將協調的行銷活動建置到視覺畫布中，以設計跨管道流程，例如細分、行銷活動執行、檔案處理。

## 存取協調的行銷活動

**[!UICONTROL 行銷活動]**&#x200B;功能表，瀏覽至「多步驟」索引標籤以存取完整的協調行銷活動清單。

清單中每個協調的行銷活動會顯示其目前[狀態](#status)、上次執行或修改的時間，以及下一個排程執行日期和時間的相關資訊。

按一下清單右上角的「**[!UICONTROL 設定自訂版面的欄]**」圖示，即可自訂要顯示的欄。這可讓您新增其他資訊至清單，例如每個協調行銷活動的最後一個錯誤活動，或套用的目標維度。

此外，還可使用搜尋列和篩選器，以便於在清單中輕鬆搜尋。例如，您可以篩選已協調的行銷活動，以僅顯示屬於某個行銷活動的行銷活動，或顯示在特定日期範圍內處理的行銷活動。

若要複製或刪除協調的行銷活動，請按一下省略符號按鈕，然後選取&#x200B;**[!UICONTROL 複製]**&#x200B;或&#x200B;**[!UICONTROL 刪除]**。

>[!NOTE]
>
>當協調的行銷活動進行中時，您可以複製它，但無法刪除它。

## 策劃的行銷活動內含哪些內容？ {#gs-ms-campaign-inside}

精心安排的行銷活動畫布可呈現預期的情形。 其會說明要執行的各種任務以及任務如何連結在一起。

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

每個協調的行銷活動包含：

* **活動**：活動指要執行的任務。各種活動在圖表中會以圖示表示。每種活動都有特定屬性和所有活動共有的其他屬性。

  在協調的行銷活動圖表中，特定活動可產生多個任務，尤其是當有回圈或重複動作時。

* **轉變**：轉變會將來源活動連結到目標活動並定義其序列。

* **工作表**：工作表包含轉變攜帶的所有資訊。每個協調的行銷活動都使用數個工作表。 這些表格中傳送的資料可在整個協調行銷活動的生命週期中使用。

## 狀態和生命週期 {#status}

行銷活動可以有多個狀態：

* **[!UICONTROL 草稿]**：已建立並儲存協調的行銷活動。
* **[!UICONTROL 進行中]**：協調的行銷活動目前正在執行。
* **[!UICONTROL 已完成]**：協調的行銷活動執行已完成。
* **[!UICONTROL 已暫停]**：已暫停協調的行銷活動。
* **[!UICONTROL 錯誤]**：協調的行銷活動發生錯誤。 開啟協調的行銷活動並存取記錄檔與工作，以識別錯誤並加以解決。
