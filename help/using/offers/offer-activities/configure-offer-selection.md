---
title: 設定決定中的優惠選擇
description: 了解如何在決策中管理選件選擇。
feature: 優惠
topic: 整合
role: User
level: Intermediate
source-git-commit: 3db5756236b6ac05d9b95b8b051dd99dc7d5cf7e
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 4%

---

# 設定決定中的優惠選擇 {#offers-selection-in-activities}

如果數個優惠方案符合指定版位的資格，您可以選擇在設定決策時（先前稱為優惠方案活動），為每個設定檔選取最佳優惠方案的方法。 您可以依下列項目來排名選件：
* 選件優先順序
* 排名公式

## 選件優先順序 {#about-offers-priority}

依預設，當數個優惠方案符合決策中指定版位的資格時（先前稱為優惠方案活動），優先順序最高&#x200B;**優先順序**&#x200B;的優惠方案會先傳送給客戶。

![](../../assets/offer-priority.png)

建立優惠方案時，會指派優惠方案的優先順序分數。 了解如何在[此區段](../offer-library/creating-personalized-offers.md)中建立個人化優惠方案。

## 排名公式 {#assign-ranking-formula}

除了選件優先順序外，Journey Optimizer還可讓您建立&#x200B;**排名公式**。 這些公式可決定應先針對指定版位呈現哪個優惠方案，而非考慮優惠方案的優先順序分數。

例如，您可以提升結束日期現在起不到24小時之所有選件的優先順序，或如果設定檔的興趣點為「執行中」，則提升「執行中」類別的選件。

了解如何在[此區段](../offer-library/create-ranking-formulas.md)中建立排名公式。

建立排名公式後，您就可以將其指派至決策中的版位（先前稱為優惠方案活動）。 若要這麼做，請遵循下列步驟：

1. 建立決策或編輯現有決策。 請參閱[建立決定](../offer-activities/create-offer-activities.md)。

1. 新增將包含您優惠方案的版位。 請參閱[建立版位](../offer-library/creating-placements.md)。

1. 為每個版位新增集合。 請參閱[建立集合](../offer-library/creating-collections.md)。

1. 從下拉式清單中選擇依&#x200B;**[!UICONTROL Ranking]**&#x200B;將選件排名，然後按一下&#x200B;**[!UICONTROL Add ranking]**。

   ![](../../assets/offer-activity-ranking.png)

1. 選擇所需的排名公式，然後按一下&#x200B;**[!UICONTROL Select]**。

   ![](../../assets/ranking-selection.png)

排名公式現在與版位相關聯。

如果有多個優惠方案符合在此版位中呈現的資格，決策會使用排名公式的公式來計算要先傳送哪個優惠方案。
