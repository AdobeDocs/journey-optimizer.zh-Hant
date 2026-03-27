---
solution: Journey Optimizer
product: journey optimizer
title: 在協調的行銷活動中使用等待活動
description: 瞭解如何在協調的行銷活動中使用等待活動
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
version: Campaign Orchestration
source-git-commit: c783d638bd2a64298ff587067c29639636da0c54
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 65%

---


# 等待 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="等待活動"
>abstract="**等待**&#x200B;活動用於延遲從一個活動到另一個活動的轉變。"

**[!UICONTROL 等待]**&#x200B;活動是&#x200B;**[!UICONTROL 流量控制]**&#x200B;元件，用來在協調的行銷活動中的兩個活動之間引入延遲。 這有助於確保您的後續活動在更適當的時間進行，且與使用者參與更相關。

例如，您可以在電子郵件傳送後等候數天，以追蹤開啟次數和點按次數，再傳送後續訊息。

## 設定{#wait-configuration}

>[!IMPORTANT]
>
>暫存資料表中的資料不會持續超過&#x200B;**5天**。 當您使用&#x200B;**[!UICONTROL 持續時間]**&#x200B;或&#x200B;**[!UICONTROL 固定時間]**&#x200B;等候，請確定下一個活動完成之前的經過時間，直到該限制內為止，讓中繼資料仍然可用。

請按照以下步驟設定&#x200B;**[!UICONTROL 等待]**&#x200B;活動：

1. 將&#x200B;**[!UICONTROL 等待]**&#x200B;活動新增至您的協調行銷活動。

1. 選取最符合您需求的等待類型：

   * **[!UICONTROL 間隔時間]**：指定繼續進行下一個活動之前的延遲時間，單位為秒、分鐘、小時或天。

   * **[!UICONTROL 固定時間]**：設定下一個活動開始的特定日期和時間。

   ![](../assets/wait_activity.png)

## 範例{#wait-example}

以下範例會說明典型使用案例中的&#x200B;**[!UICONTROL 等待]**&#x200B;活動。內含促銷代碼的電子郵件會傳送給慶祝生日的輪廓。2 天後，系統會傳送簡訊給相同群組，提醒他們生日促銷代碼即將到期。

![](../assets/wait-example.png)
