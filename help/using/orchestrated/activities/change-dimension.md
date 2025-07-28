---
solution: Journey Optimizer
product: journey optimizer
title: 使用變更維度活動
description: 了解如何使用變更維度活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 62%

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

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](../gs-schemas.md)</li><li>[手動結構描述](../manual-schema.md)</li><li>[檔案上傳結構描述](../file-upload-schema.md)</li><li>[擷取資料](../ingest-data.md)</li></ul>[存取及管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[同時加入](and-join.md) - [建立客群](build-audience.md) - <b>[變更維度](change-dimension.md)</b> - [頻道活動](channels.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調和](reconciliation.md) - [儲存客群](save-audience.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

行銷人員可在協調的行銷活動中，從一個資料實體變更為相關的資料實體，藉此增強受眾目標定位。 這可讓您超越使用者輪廓，並專注於特定行為，例如購買、預訂或其他互動。

若要達成此目的，請使用&#x200B;**[!UICONTROL 變更維度]**&#x200B;活動。它可讓您在協調的行銷活動期間調整目標維度。

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## 設定變更維度活動 {#configure}

請按照以下步驟設定&#x200B;**[!UICONTROL 變更維度]**&#x200B;活動：

1. 新增&#x200B;**[!UICONTROL 變更維度]**&#x200B;活動至您的協調行銷活動。

   ![](../assets/orchestrated-change-dimension.png)

1. 定義&#x200B;**[!UICONTROL 新目標維度]**。在維度變更期間，會保留所有記錄。


## 範例 {#example}

此使用案例著重於傳送簡訊給在過去一個月內建立願望清單的輪廓。

從&#x200B;**[!UICONTROL 建立客群]**&#x200B;活動開始，使用&#x200B;**[!UICONTROL 願望清單]**&#x200B;目標維度來識別所有相關的願望清單。

接著，新增&#x200B;**[!UICONTROL 變更維度]**&#x200B;活動，以將目標維度從&#x200B;**[!UICONTROL 願望清單]**&#x200B;切換為&#x200B;**[!UICONTROL 收件者]。**&#x200B;此步驟會確保協調行銷活動將目標設定為連結至這些願望清單的正確設定檔，以便將SMS傳送至預期的設定檔。

![](../assets/orchestrated-change-dimension-example.png)
