---
solution: Journey Optimizer
product: journey optimizer
title: 使用儲存對象活動
description: 瞭解如何在協調的行銷活動中使用「儲存對象」活動
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 3%

---

# 儲存客群 {#save-audience}

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[存取和管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重新鎖定目標](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建立對象](build-audience.md) - [變更維度](change-dimension.md) - [頻道活動](channels.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - <b>[儲存對象](save-audience.md)</b> - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++


**[!UICONTROL 儲存對象]**&#x200B;活動是&#x200B;**[!UICONTROL 鎖定目標]**&#x200B;活動，可讓您更新現有的對象，或是從先前在協調的行銷活動中產生的母體中建立新的對象。 建立後，這些對象會新增至應用程式對象清單，並可從&#x200B;**[!UICONTROL 對象]**&#x200B;功能表存取。

此活動對於保留在相同的協調行銷活動中計算的對象區段特別有用，以便將來行銷活動中重複使用。 它通常連線到其他目標定位活動，例如&#x200B;**[!UICONTROL 建立對象]**&#x200B;或&#x200B;**[!UICONTROL 合併]**，以擷取並儲存產生的母體。

## 設定「儲存對象」活動 {#save-audience-configuration}

請依照下列步驟設定&#x200B;**儲存對象**&#x200B;活動：

1. 新增&#x200B;**儲存對象**&#x200B;活動至您協調的行銷活動。

1. 在&#x200B;**模式**&#x200B;下拉式清單中，選取您要執行的動作：

   * **建立或更新現有的對象**：定義&#x200B;**對象標籤**。 如果對象已存在，則會更新；否則，會建立新對象。

   * **更新現有的對象**：從現有的對象清單中選擇要更新的&#x200B;**對象**。

1. 選取套用至現有對象的&#x200B;**更新模式**：

   * **以新資料取代對象內容**：所有對象內容都會被取代，而舊資料會遺失。 僅保留&#x200B;**儲存對象**&#x200B;活動之入站轉變的資料。 此選項會清除更新對象的對象型別和目標定位維度。

   * **使用新資料完成對象**：保留舊對象內容，並新增&#x200B;**儲存對象**&#x200B;活動之入站轉變的資料。

1. 若要在&#x200B;**儲存對象**&#x200B;活動後新增轉變，請核取&#x200B;**產生出站轉變**&#x200B;選項。

之後儲存的對象內容便可在對象的詳細資料檢視中使用，您可從&#x200B;**對象**&#x200B;功能表存取該內容。 此檢視中可用的欄對應於協調的行銷活動&#x200B;**儲存對象**&#x200B;活動的入站轉變的欄。

## 範例 {#save-audience-example}

以下範例說明如何從目標定位進行簡單的對象更新。 排程器每月執行一次協調的行銷活動。 查詢會擷取訂閱了不同可用應用程式的所有設定檔。 **儲存對象**&#x200B;活動會移除自上次協調行銷活動執行以來從服務取消訂閱的設定檔，並新增新訂閱的設定檔，以更新對象。
