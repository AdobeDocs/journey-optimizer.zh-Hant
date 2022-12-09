---
title: 在決策中設定選件選取項目
description: 了解如何在決策中管理選件選項
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: b890d7dc2e1508bb68d45a162236483ac6fc76bd
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---

# 在決策中設定選件選取項目 {#offers-selection-in-decisions}

如果數個優惠方案符合指定版位的資格，您可以選擇在設定決策時，為每個設定檔選取最佳優惠方案的方法。 您可以依下列項目來排名選件：
* 選件優先順序
* 排名公式
* [AI排名](#use-ranking-strategy)

![](../assets/offer-rank-by.png)

## 選件優先順序 {#offer-priority}

依預設，當數個優惠方案符合決策中指定版位的資格時，優惠方案的最高 **優先順序** 會先傳送給客戶。

![](../assets/offer-priority.png)

建立優惠方案時，會指派優惠方案的優先順序分數。 了解如何在 [本節](../offer-library/creating-personalized-offers.md).

## 排名公式 {#assign-ranking-formula}

除了優先順序外，Journey Optimizer還可讓您建立 **排名公式**. 這些公式可決定應先針對指定版位呈現哪個優惠方案，而非考慮優惠方案的優先順序分數。

例如，您可以提升結束日期現在起不到24小時之所有選件的優先順序，或如果設定檔的興趣點為「執行中」，則提升「執行中」類別的選件。

了解如何在 [本節](../ranking/create-ranking-formulas.md).

建立排名公式後，您可以將其指派給決策中的版位。 若要這麼做，請遵循下列步驟：

1. 建立決策或編輯現有決策。 請參閱 [建立決策](../offer-activities/create-offer-activities.md).

1. 新增將包含您優惠方案的版位。 請參閱 [建立版位](../offer-library/creating-placements.md).

1. 為每個版位新增集合。 請參閱 [建立集合](../offer-library/creating-collections.md).

1. 選擇 **[!UICONTROL Ranking formula]** 作為排名方法，然後按一下 **[!UICONTROL Add ranking]**.

   ![](../assets/offer-activity-ranking.png)

1. 選取所需的排名公式，然後按一下 **[!UICONTROL Select]**.

   ![](../assets/ranking-selection.png)

排名公式現在與版位相關聯。

如果有多個優惠方案符合在此版位中呈現的資格，決策會使用排名公式的公式來計算要先傳送哪個優惠方案。

## AI排名 {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

您也可以使用經過訓練的模型系統，透過選取排名策略來自動排名選件，以針對指定的設定檔顯示。 了解如何在 [本節](../ranking/create-ranking-strategies.md).

建立排名策略後，您就可以將其指派至決策中的位置。 若要這麼做，請遵循下列步驟：

1. 建立決策或編輯現有決策。 請參閱 [建立決策](../offer-activities/create-offer-activities.md).

1. 新增將包含您優惠方案的版位。 請參閱 [建立版位](../offer-library/creating-placements.md).

1. 為每個版位新增集合。 請參閱 [建立集合](../offer-library/creating-collections.md).

1. 選擇將選件排名依據 **[!UICONTROL AI ranking]** 從下拉式清單中，按一下 **[!UICONTROL Add ranking]**.

   ![](../assets/ranking-selection-ai-ranking.png)

1. 選取您建立的排名策略。 排名策略的所有詳細資訊都會顯示。

   ![](../assets/ranking-selection-ai-ranking-selected.png)

1. 按一下 **[!UICONTROL Select]**. 排名策略現在與位置相關聯。

如果多個優惠方案符合資格，經過訓練的模型系統將決定應先針對指定版位呈現哪個優惠方案。

