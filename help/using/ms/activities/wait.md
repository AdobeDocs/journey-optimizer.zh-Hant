---
solution: Journey Optimizer
product: journey optimizer
title: 在協調的行銷活動中使用等待活動
description: 瞭解如何在協調的行銷活動中使用等待活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 78%

---

# 等待 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="等待活動"
>abstract="**等待**&#x200B;活動用於延遲從一個活動到另一個活動的轉變。"

「**等待**」活動是一種&#x200B;**流程控制**&#x200B;活動。此活動用於允許正在執行的兩個活動之間經過一定的時間。例如，若要在電子郵件傳送活動後等候數天，請先分析此期間產生的開啟次數和點按次數，再執行任何後續操作 (提醒電子郵件、建立客群等)。

## 設定{#wait-configuration}

請按照以下步驟設定&#x200B;**等待**&#x200B;活動：

1. 將&#x200B;**等待**&#x200B;活動新增至您協調的行銷活動。

1. 指定傳入和傳出轉變之間等待的&#x200B;**持續時間**。

1. 在&#x200B;**期間**&#x200B;欄位中選取時間單位：秒、分鐘、小時、天。

## 範例{#wait-example}

以下範例會說明典型使用案例中的 **等待**&#x200B;活動。已傳送活動的電子郵件邀請。傳送後 24 小時，會將簡訊傳送給同一個群體。

![](../assets/workflow-wait-example.png)
