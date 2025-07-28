---
solution: Journey Optimizer
product: journey optimizer
title: 使用合併連結活動
description: 瞭解如何在協調的行銷活動中使用AND — 加入活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 60%

---

# 合併連結 {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="AND-join 活動"
>abstract="**並加入**&#x200B;活動可讓您同步處理協調行銷活動的多個執行分支。 一旦所有前面的活動完成，就會觸發此活動。這可讓您在繼續執行「協調流程」行銷活動之前，確定特定活動已完成。"


+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](../gs-schemas.md)</li><li>[手動結構描述](../manual-schema.md)</li><li>[檔案上傳結構描述](../file-upload-schema.md)</li><li>[擷取資料](../ingest-data.md)</li></ul>[存取及管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/><b>[同時加入](and-join.md)</b> - [建立客群](build-audience.md) - [變更維度](change-dimension.md) - [頻道活動](channels.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調和](reconciliation.md) - [儲存客群](save-audience.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

「**[!UICONTROL 合併連結]**」活動是一種&#x200B;**[!UICONTROL 流程控制]**&#x200B;活動。它可讓您同步處理協調行銷活動的多個執行分支。

此活動只會在所有傳入轉變啟動後，才會觸發其傳出轉變，換句話說，會在所有之前的活動完成後觸發。這可讓您在繼續執行「協調流程」行銷活動之前，確定特定活動已完成。

## 設定合併連結活動{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="合併選項"
>abstract="選取您要參加的活動。在「**主要集合**」下拉選單中，選擇您要保留的傳入轉變群體。"

請按照以下步驟設定&#x200B;**[!UICONTROL 合併連結]**&#x200B;活動：

![](../assets/workflow-andjoin.png)

1. 新增許多活動，例如頻道活動，以便建立至少兩種不同的執行分支。

1. 請將&#x200B;**[!UICONTROL 合併連結]**&#x200B;活動新增至任何分支。

1. 請在&#x200B;**[!UICONTROL 合併選項]**&#x200B;區段下，選取您想加入的所有之前活動。

1. 請在「**[!UICONTROL 主要集合]**」下拉選單中，選擇您想保留的傳入轉變族群。

## 範例{#and-join-example}

此範例會說明兩個協調行銷活動分支，每個分支都經由電子郵件傳送、一個會以金牌會員為目標，另一個以銀牌會員為目標。 觸發兩個傳入轉換後，就會啟用&#x200B;**[!UICONTROL 合併連結]**，只會在傳遞完兩個電子郵件後，再傳送簡訊，大概會往後延遲 7 天左右。

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
