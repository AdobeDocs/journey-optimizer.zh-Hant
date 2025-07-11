---
solution: Journey Optimizer
product: journey optimizer
title: 使用AND — 聯結活動
description: 瞭解如何在協調的行銷活動中使用AND — 加入活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 779c90f0be57749a63da103d18cc642106c5f837
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 36%

---

# 合併連結 {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="AND-join 活動"
>abstract="**合併連結**&#x200B;活動讓您可以同步處理協調的行銷活動的多個執行分支。一旦所有前面的活動完成，就會觸發此活動。這樣，您便可以確保特定活動已完成後，再繼續執行協調的行銷活動。"


+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[存取和管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重新鎖定目標](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/><b>[並加入](and-join.md)</b> - [建立對象](build-audience.md) - [變更維度](change-dimension.md) - [頻道活動](channels.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - [儲存對象](save-audience.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

檔案處理中

>[!ENDSHADEBOX]

「**[!UICONTROL 合併連結]**」活動是一種&#x200B;**[!UICONTROL 流程控制]**&#x200B;活動。它可讓您同步處理協調行銷活動的多個執行分支。

此活動只會在所有傳入轉變啟動後，才會觸發其傳出轉變，換句話說，會在所有之前的活動完成後觸發。這可讓您在繼續執行協調的行銷活動之前，先確定某些活動已完成。

## 設定合併連結活動{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="合併選項"
>abstract="選取您要參加的活動。在「**主要集合**」下拉選單中，選擇您要保留的傳入轉變群體。"

請按照以下步驟設定「**[!UICONTROL 合併連結]**」活動：

![](../assets/workflow-andjoin.png)

1. 新增多個活動（例如管道活動）以建立至少兩個不同的執行分支。

1. 將&#x200B;**[!UICONTROL AND — 加入]**&#x200B;活動插入其中一個分支。

1. 在&#x200B;**[!UICONTROL 合併選項]**&#x200B;區段下，選取您要加入的所有先前活動。

1. 從&#x200B;**[!UICONTROL 主要集]**&#x200B;下拉式清單中，選取要保留的入站轉變母體。

## 範例{#and-join-example}

此範例說明兩個協調的行銷活動分支，每個分支都有電子郵件傳送、一個以金會員為目標，另一個以銀會員為目標。 觸發兩個傳入的轉換後，**[!UICONTROL AND-join]**&#x200B;就會啟用，而且簡訊只會在兩個電子郵件傳遞完成後傳送，並會延遲7天。

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
