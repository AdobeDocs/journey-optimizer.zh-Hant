---
solution: Journey Optimizer
product: journey optimizer
title: 使用規則產生器
description: 了解如何為您的協調行銷活動建立規則
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 87%

---


# 使用規則產生器 {#orchestrated-rule-builder}

+++ 目錄

| 歡迎使用協調行銷活動 | 首次投放的協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](gs-schemas.md)</li><li>[手動結構描述](manual-schema.md)</li><li>[檔案上傳結構描述](file-upload-schema.md)</li><li>[擷取資料](ingest-data.md)</li></ul>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | <b>[使用規則產生器](orchestrated-rule-builder.md)</b><br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[同時加入](activities/and-join.md) - [建立客群](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調和](activities/reconciliation.md) - [儲存客群](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

協調的行銷活動隨附規則產生器，可簡化根據各種條件篩選資料庫的流程。規則產生器能有效管理非常複雜和冗長的查詢，提供增強的彈性和精確度。

它也支援條件內預先定義的篩選器，使您可輕鬆調整查詢，同時利用進階運算式和運算子實現全面的客群目標定位和細分策略。

## 存取規則產生器

查詢建模工具適用於每個您需要定義篩選資料的規則的環境。

| 使用方式 | 範例 |
|  ---  |  ---  |
| **建立客群**：使用&#x200B;**[!UICONTROL 建立客群]**&#x200B;活動，指定您要在協調行銷活動中設為目標的群體，並輕鬆建立符合您需求的新客群。[了解如何建立客群](../orchestrated/activities/build-audience.md) | ![顯示如何存取客群建立介面的影像](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **在行銷活動畫布中建立條件**：使用&#x200B;**[!UICONTROL 分割]**&#x200B;活動在行銷活動畫布中套用規則，以符合您的特定需求。[了解如何使用分割活動](../orchestrated/activities/split.md) | ![顯示如何存取工作流程自訂選項的影像](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **建立進階篩選器**：建立規則以篩選清單中顯示的資料，例如工作流程記錄或目標定位維度。 | ![顯示如何自訂清單篩選器的影像](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## 規則產生器介面 {#interface}

規則產生器提供中央畫布，您可在其中建立查詢，以及提供規則相關資訊的屬性窗格。

![顯示規則產生器介面的影像](assets/rule-builder-interface.png)

* 您可以在&#x200B;**中央畫布**&#x200B;新增並合併不同元件以建立規則。[了解如何建立規則](../orchestrated/build-query.md)

* **[!UICONTROL 規則屬性]**&#x200B;窗格會提供有關您規則的資訊。它可讓您執行各種作業來檢查規則，並確保它符合您的需求。

  建立查詢以建立客群時，會顯示此窗格。[了解如何檢查及驗證您的查詢](build-query.md#check-and-validate-your-query)
