---
solution: Journey Optimizer
product: journey optimizer
title: 使用「分支」活動
description: 瞭解如何在協調的行銷活動中使用分叉活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: d59643f18a335fe1e094156a1cfee65b717b9fce
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 27%

---

# 分支 {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="分支活動"
>abstract="**分支**&#x200B;活動可讓您建立傳出轉變，以同時啟動多個活動。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="分支活動轉變"
>abstract="依預設，透過&#x200B;**分支**&#x200B;活動建立二個轉變。按一下&#x200B;**新增轉變**&#x200B;按鈕以定義額外的傳出轉變，並輸入其標籤。"

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調的行銷活動活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[建立協調行銷活動的重要步驟](../gs-campaign-creation.md) | [建立協調的行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[使用協調的行銷活動傳送訊息](../send-messages.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用查詢Modeler](../orchestrated-rule-builder.md)<br/><br/>[建置您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建置對象](build-audience.md) - [變更維度](change-dimension.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**Fork**&#x200B;活動是&#x200B;**流量控制**&#x200B;元件，可讓您建立多個輸出轉變，讓多個活動平行執行。

## 設定分叉活動{#fork-configuration}

請按照以下步驟設定「**分支**」活動：

![](../assets/workflow-fork.png)

1. 將&#x200B;**分支**&#x200B;活動新增至您協調的行銷活動。

1. 定義&#x200B;**標籤**。

1. 為每個出站轉變指派標籤。 依預設，會提供兩個轉變。

1. 若要移除轉變，請按一下![](../assets/do-not-localize/Smock_Delete_18_N.svg)圖示。

1. 如有需要，請按一下&#x200B;**新增轉變**&#x200B;以新增額外的輸出轉變。
