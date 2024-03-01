---
title: 建立選擇策略
description: 瞭解如何建立選擇策略
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 1b73b398-050a-40bb-a8ae-1c66e3e26ce8
source-git-commit: c13cd73229b2fab80722663afae9fe24b660c0f9
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 19%

---

# 建立選擇策略 {#selection-strategies}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_strategies"
>title="定義您的選擇策略"
>abstract="選擇策略是一個可重複使用的項目，當中包括與適用性限制和排名方法相關聯的集合，用以確定當在決定原則中選取時要顯示的優惠。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/create-decision.html" text="建立決定原則"

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_eligibility"
>title="限制符合資格的設定檔"
>abstract="您可以限制此選擇策略的優惠選擇。 預設情況下，所有設定檔都符合資格，但您可以使用對象或規則將優惠選擇限制為僅限特定設定檔。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html" text="使用對象"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html" text="使用決定規則"

>[!BEGINSHADEBOX 「本檔案指南提供哪些內容」]

* [開始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的決定專案： [設定專案目錄](catalogs.md) - [建立決定專案](items.md) - [管理專案集合](collections.md)
* 設定專案的選取範圍： [建立決定規則](rules.md) - [建立排名方法](ranking.md)
* **[建立選取策略](selection-strategies.md)**
* [建立決定原則](create-decision.md)

>[!ENDSHADEBOX]

選擇策略是可重複使用的專案，包含與適用性限制相關的集合，以及決定要在中選取時顯示的優惠方案的排名方法。 [決定原則](create-decision.md).

## 存取及管理選擇策略

1. 前往 **[!UICONTROL 體驗決策]** > **[!UICONTROL 設定]** > **[!UICONTROL 選取策略]**.

1. 目前建立的所有選取策略都會列在清單中。 篩選器可協助您根據排名方法擷取策略。

   ![](assets/strategy-list-filters.png)

1. 按一下選取策略名稱以進行編輯。

1. 也會顯示針對每個策略選取的集合、排名方法及資格。 您可以按一下每個收藏集名稱旁的圖示，直接編輯收藏集。

   ![](assets/strategy-list-edit-collection.png)

## 建立選取策略

若要建立選取策略，請遵循下列步驟。

1. 從 **[!UICONTROL 選取策略]** 詳細目錄，按一下 **[!UICONTROL 建立選擇策略]**.

   ![](assets/strategy-create-button.png)

1. 為您的策略新增名稱。

   >[!NOTE]
   >
   >目前僅預設 **[!UICONTROL 選件]** 目錄可供使用。

1. 從名稱開始，填寫選擇策略的詳細資訊。

   ![](assets/strategy-create-screen.png)

1. 選取 [集合](collections.md) 包含要考量的選件。

1. 選取選件 [集合](collections.md) 包含要考量的選件。

1. 使用 **[!UICONTROL 資格]** 欄位，用來限制此選取策略的優惠方案選取。

   ![](assets/strategy-create-eligibility.png)

   * 若要將優惠方案的選擇限制在Experience Platform對象的成員，請選取「 」 **[!UICONTROL 受眾]** 並從清單中選擇對象。 [瞭解如何使用受眾](../audience/about-audiences.md)

   * 如果您想使用決定規則新增選擇限制，請使用 **[!UICONTROL 決定規則]** 並選取您選擇的規則。 [瞭解如何建立規則](rules.md)

1. 定義您要用來為每個設定檔選取最佳優惠方案的排名方法。 [了解更多](#select-ranking-method)

   ![](assets/strategy-create-ranking.png)

   * 依預設，如果有多個優惠方案符合此策略的資格， [優惠優先順序](#offer-priority) 方法使用在選件中定義的值。

   * 如果您想要使用特定計算的分數來選擇要遞送的合格優惠方案，請選取 [公式](#ranking-formula) 或 [AI模型](#ai-ranking).

1. 按一下 **[!UICONTROL 建立]**。現在已準備好用於 [決定](create-decision.md)

## 選取排名方法 {#select-ranking-method}

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_ranking"
>title="定義如何對優惠進行排名"
>abstract="如果多個優惠符合特定的選擇策略，請在建立選擇策略時選擇為每個設定檔選取最佳優惠的方法：優先順序或排名公式。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/create-decision.html" text="建立決定原則"

如果數個優惠方案符合指定的選取策略資格，您可以選擇在建立選取策略時，用來選取每個設定檔之最佳優惠方案的方法。 您可以依下列方式排名優惠方案：

* [優惠優先順序](#offer-priority)
* [公式](#ranking-formula)
* [AI 排名](#ai-ranking)

### 優惠優先順序 {#offer-priority}

依預設，當數個優惠方案符合決定中指定位置的資格時，具有最高位置的專案 **優先順序** 會先傳送給客戶。

![](assets/item-priority.png)

優惠的優先順序分數是在建立時指派的 [決定專案](items.md).

### 排名公式 {#ranking-formula}

除了選件優先順序之外，Journey Optimizer還允許您建立 **排名公式**. 這些公式可決定應先針對指定位置顯示哪個優惠，而不是考慮優惠的優先順序分數。

例如，您可以提升結束日期距離現在不足24小時的所有優惠方案的優先順序，或如果設定檔的興趣點為「執行中」，則提升「執行中」類別的優惠方案。 瞭解如何在中建立排名公式 [本節](ranking.md).

建立之後，您可以在選擇策略中使用此公式。 使用此選取策略時，如果多個優惠方案符合呈現的條件，決策將使用選取的公式來計算要先傳送哪個優惠方案。

### AI 排名 {#ai-ranking}

您也可以使用經過訓練的模型系統，藉由選取AI模型，自動排名要針對指定設定檔顯示的優惠方案。 瞭解如何在中建立AI模型 [本節](ranking.md).

建立AI模型後，您即可在選取策略中使用它。 如果多個優惠方案都符合條件，經過訓練的模型系統將決定應該首先針對此選擇策略顯示哪個優惠方案。
