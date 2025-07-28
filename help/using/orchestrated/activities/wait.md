---
solution: Journey Optimizer
product: journey optimizer
title: 在協調的行銷活動中使用等待活動
description: 瞭解如何在協調的行銷活動中使用等待活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 62%

---

# 等待 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="等待活動"
>abstract="**等待**&#x200B;活動用於延遲從一個活動到另一個活動的轉變。"


+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](../gs-schemas.md)</li><li>[手動結構描述](../manual-schema.md)</li><li>[檔案上傳結構描述](../file-upload-schema.md)</li><li>[擷取資料](../ingest-data.md)</li></ul>[存取及管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[同時加入](and-join.md) - [建立客群](build-audience.md) - [變更維度](change-dimension.md) - [頻道活動](channels.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調和](reconciliation.md) - [儲存客群](save-audience.md) - [分割](split.md) - <b>[等待](wait.md)</b> |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

**[!UICONTROL 等待]**&#x200B;活動是&#x200B;**[!UICONTROL 流量控制]**&#x200B;元件，用來在協調的行銷活動中的兩個活動之間引入延遲。 這有助於確保您的後續活動在更適當的時間進行，且與使用者參與更相關。

例如，您可以在電子郵件傳送後等候數天，以追蹤開啟次數和點按次數，再傳送後續訊息。

## 設定{#wait-configuration}

請按照以下步驟設定&#x200B;**[!UICONTROL 等待]**&#x200B;活動：

1. 將&#x200B;**[!UICONTROL 等待]**&#x200B;活動新增至您的協調行銷活動。

1. 選取最符合您需求的等待類型：

   * **[!UICONTROL 間隔時間]**：指定繼續進行下一個活動之前的延遲時間，單位為秒、分鐘、小時或天。

   * **[!UICONTROL 固定時間]**：設定下一個活動開始的特定日期和時間。

   ![](../assets/wait_activity.png)

## 範例{#wait-example}

以下範例會說明典型使用案例中的&#x200B;**[!UICONTROL 等待]**&#x200B;活動。內含促銷代碼的電子郵件會傳送給慶祝生日的輪廓。29 天後，系統會傳送簡訊給相同群組，提醒他們生日促銷代碼即將到期。

![](../assets/wait-example.png)
