---
solution: Journey Optimizer
product: journey optimizer
title: 在協調的行銷活動中使用變數
description: 瞭解如何在協調的行銷活動中使用事件變數，以建立條件和鎖定規則。
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
version: Campaign Orchestration
exl-id: 3f2a1c0d-8e9b-4a7c-b5d1-0f2e3a4b5c6d
feature_v2: id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 1%

---


# 在協調的行銷活動中使用變數 {#variables-oc}

## 如何設定變數 {#set}

在協調的行銷活動中，您可以使用變數，也就是推動鎖定目標的值、**[!UICONTROL 測試]**&#x200B;條件和其他畫布邏輯。 這些值可能來自兩個位置：

* **訊號** — 如果行銷活動排程是&#x200B;**[!UICONTROL 由訊號]**&#x200B;觸發，您可以在引發行銷活動時傳遞引數。 這些引數在該回合的觸發式協調行銷活動中成為變數而提供。 [瞭解如何使用訊號觸發協調的行銷活動](trigger-orchestrated-campaign.md)

* **全域變數** — 您可以使用&#x200B;**[!UICONTROL 編輯變數]**&#x200B;功能表，直接在促銷活動上定義名稱 — 值組，不需要API或訊號。 [瞭解如何在協調的行銷活動中定義全域變數](global-variables.md)

>[!NOTE]
>
>目前，變數僅支援&#x200B;**文字**&#x200B;值。
>
>變數會驅動&#x200B;**畫布邏輯** （規則、條件），且無法用於訊息個人化。

## 在畫布中使用變數 {#use}

變數可在畫布上的下列位置使用：

* **規則產生器** — 開啟規則的運算式編輯器，並使用&#x200B;**事件變數**&#x200B;選擇器來選取變數，並將其參照插入運算式中。 [了解如何編輯運算式](edit-expressions.md)

  在下列範例中，傳入了名為`brand`的變數，規則會將其用作篩選條件。

  使用事件變數的品牌變數的![規則產生器條件](assets/variables-rule.png){zoomable="yes"}

* **[!UICONTROL 測試]活動** — 當您定義條件時，**[!UICONTROL 條件型別]**&#x200B;下拉式清單會與&#x200B;**[!UICONTROL 母體計數]**&#x200B;一起列出範圍中的所有變數。 選取變數，以將其用作測試分支的基礎。 [瞭解如何設定&#x200B;**[!UICONTROL 測試]**&#x200B;活動](activities/test.md)

  在下列範例中，`channel`變數是用來根據流程的值將其路由到不同的轉變。

  ![測試活動條件型別下拉式清單，列出頻道變數](assets/variables-test.png){zoomable="yes"}
