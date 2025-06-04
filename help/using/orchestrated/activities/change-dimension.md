---
solution: Journey Optimizer
product: journey optimizer
title: 使用變更維度活動
description: 瞭解如何使用變更維度活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 9606ca5710e6f91159474d76f68cdcbc2128b000
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 19%

---

# 變更維度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="產生補集"
>abstract="您可以使用剩餘族群 (其已因重複而排除) 產生額外的傳出轉變。若要這樣做，請開啟「**產生補集**」選項"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="變更維度活動"
>abstract="此活動可讓您在建立對象時變更目標市場選擇維度。其會根據資料範本和輸入維度來移動軸。例如，您可以從「合約」維度切換到「用戶端」維度。"

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調的行銷活動活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[建立協調行銷活動的重要步驟](../gs-campaign-creation.md) | [建立協調的行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[使用協調的行銷活動傳送訊息](../send-messages.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用查詢Modeler](../orchestrated-query-modeler.md)<br/><br/>[建置您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建置對象](build-audience.md) - [變更維度](change-dimension.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

行銷人員可以在協調的行銷活動中，將目標維度從一個實體切換至另一個連結的實體，並根據不同的資料集調整對象目標，例如從設定使用者到將其特定動作或預訂做為目標。

若要執行此動作，請使用&#x200B;**變更維度**&#x200B;目標定位活動。 此活動可讓您在建立協調的行銷活動時變更目標維度。 它會根據資料範本和輸入維度來移動軸。

例如，您可以將協調行銷活動的目標維度從「設定檔」切換為「合約」，以傳送訊息給目標合約所有者。

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## 設定變更維度活動 {#configure}

請依照下列步驟設定&#x200B;**變更維度**&#x200B;活動：

1. 新增&#x200B;**變更維度**&#x200B;活動至您協調的行銷活動。

   ![](../assets/change-dimension.png)

1. 定義&#x200B;**新目標維度**。 在維度變更期間，會保留所有記錄。

1. 執行協調的行銷活動以檢視結果。 比較變更維度活動前後表格中的資料，以及比較協調的行銷活動表格結構。

## 範例 {#example}

在此範例中，我們要傳送SMS傳送給已購買的所有設定檔。 若要這麼做，我們先使用連結至自訂「購買」目標維度的&#x200B;**[!UICONTROL 建立對象]**&#x200B;活動，以鎖定所有發生的購買。

然後使用&#x200B;**[!UICONTROL 變更維度]**&#x200B;活動，將協調的行銷活動目標維度切換為「收件者」。 這可讓我們鎖定符合查詢的收件者。

![](../assets/change-dimension-example.png)
