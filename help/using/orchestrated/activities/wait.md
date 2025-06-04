---
solution: Journey Optimizer
product: journey optimizer
title: 在協調的行銷活動中使用等待活動
description: 瞭解如何在協調的行銷活動中使用等待活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 52226a4374fa6321b31ac2d57f76a48594df1c51
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 11%

---

# 等待 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="等待活動"
>abstract="**等待**&#x200B;活動用於延遲從一個活動到另一個活動的轉變。"

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調的行銷活動活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[建立協調行銷活動的重要步驟](../gs-campaign-creation.md) | [建立協調的行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[使用協調的行銷活動傳送訊息](../send-messages.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用查詢Modeler](../orchestrated-query-modeler.md)<br/><br/>[建置您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建置對象](build-audience.md) - [變更維度](change-dimension.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**等待**&#x200B;活動是&#x200B;**流量控制**&#x200B;元件，用來在協調行銷活動中的兩個活動之間引入延遲。 這有助於確保您的後續活動在更適當的時間進行，且與使用者參與更相關。

例如，您可以在電子郵件傳送後等候數天，以追蹤開啟次數和點按次數，再傳送後續訊息。

## 設定{#wait-configuration}

請按照以下步驟設定&#x200B;**等待**&#x200B;活動：

1. 將&#x200B;**等待**&#x200B;活動新增至您協調的行銷活動。

1. 選取最符合您需求的等待型別：

   * **持續時間**：指定繼續進行下一個活動之前的延遲時間，單位為秒、分鐘、小時或天。

   * **固定時間**：設定下一個活動開始的特定日期和時間。

   ![](../assets/wait_activity.png)

## 範例{#wait-example}

下列範例說明典型使用案例中的&#x200B;**等待**&#x200B;活動。  內含促銷代碼的電子郵件會傳送給慶祝生日的設定檔。 29天後，系統會傳送簡訊給相同群組，提醒他們生日促銷程式碼即將到期。

![](../assets/wait-example.png)
