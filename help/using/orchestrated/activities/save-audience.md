---
solution: Journey Optimizer
product: journey optimizer
title: 使用儲存客群活動
description: 瞭解如何在協調的行銷活動中，使用儲存客群活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 81f0338935ee36b152963f2b1c0e7989b86f5f8a
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 67%

---

# 儲存客群 {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="儲存對象活動"
>abstract="**儲存客群**&#x200B;活動是&#x200B;**目標定為**&#x200B;活動，讓您可以更新現有的客群，或是從之前在協調行銷活動中產生的族群中，建立新的客群。 一旦建立完畢，就會將這些客群新增至應用程式客群清單，再從&#x200B;**客群**&#x200B;選單那邊存取。"


+++ 目錄

| 歡迎使用協調行銷活動 | 首次投放的協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](../gs-schemas.md)</li><li>[手動結構描述](../manual-schema.md)</li><li>[檔案上傳結構描述](../file-upload-schema.md)</li><li>[擷取資料](../ingest-data.md)</li></ul>[存取及管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[同時加入](and-join.md) - [建立客群](build-audience.md) - [變更維度](change-dimension.md) - [頻道活動](channels.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調和](reconciliation.md) - <b>[儲存客群](save-audience.md)</b> - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

**[!UICONTROL 儲存對象]**&#x200B;活動是&#x200B;**[!UICONTROL 鎖定目標]**&#x200B;活動，用來根據先前在協調的行銷活動中產生的母體來建立新對象或更新現有對象。 儲存後，對象會新增至應用程式對象清單，並可從&#x200B;**[!UICONTROL 對象]**&#x200B;功能表存取。

它常用於擷取在相同行銷活動工作流程中建立的對象區段，以便在未來的行銷活動中重複使用。 通常會連線到其他目標定位活動，例如&#x200B;**[!UICONTROL 建立對象]**&#x200B;或&#x200B;**[!UICONTROL 合併]**，以儲存最終目標定位母體。

## 設定儲存客群活動 {#save-audience-configuration}

請按照以下步驟，設定「**[!UICONTROL 儲存客群]**」活動：

1. 請將「**[!UICONTROL 儲存客群]**」活動新增至協調的行銷活動。

1. 輸入&#x200B;**[!UICONTROL 客群標籤]**，就能識別已儲存客群。

1. 按一下 **[!UICONTROL [新增客群屬性]]**，以便定義客群資料的結構化和儲存方式，以供日後重複使用。

   ![](../assets/save-audience-1.png)

1. 然後，選取適當的&#x200B;**[!UICONTROL 主要身分識別欄位]**&#x200B;和&#x200B;**[!UICONTROL 身分識別命名空間]**，以便確保正確的設定檔解析度。

   ![](../assets/save-audience-2.png)

1. 儲存並發佈協調的行銷活動，以便完成設定。 這將能產生並儲存客群。

之後，就可以在客群的詳細資料視圖中，使用儲存的客群內容，可以到&#x200B;**[!UICONTROL 客群]**&#x200B;選單那邊存取內容。

![](../assets/save-audience-3.png)

## 範例 {#save-audience-example}

以下範例會示範如何使用鎖定目標，建立簡易客群。 查詢可找出過去 30 天內購買的所有設定檔。 **[!UICONTROL 儲存客群]**&#x200B;活動接著會擷取以上設定檔，以便建立客群，讓近期購買者可重複使用。

![](../assets/save-audience-4.png)
