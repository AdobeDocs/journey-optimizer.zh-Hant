---
title: 設定決定中的優惠選擇
description: 了解如何在決策中管理選件選擇。
feature: 優惠
topic: 整合
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 4%

---

# 設定決定中的優惠選擇 {#offers-selection-in-activities}

## 關於選件優先順序{#about-offers-priority}

依預設，當數個優惠方案符合決策中指定版位的資格時（先前稱為優惠方案活動），優先順序最高&#x200B;**優先順序**&#x200B;的優惠方案會先傳送給客戶。 建立優惠方案時會指派優惠方案的優先順序分數（請參閱[建立個人化優惠方案](../offer-library/creating-personalized-offers.md)）。

![](../../assets/offer-priority.png)

此外，Journey Optimizer可讓您建立&#x200B;**排名公式**。 這些公式可決定應先針對指定版位呈現哪個優惠方案，而非考慮優惠方案的優先順序分數。 例如，您可以提升結束日期現在起不到24小時之所有選件的優先順序，或如果設定檔的興趣點為「執行中」，則提升「執行中」類別的選件。

有關如何建立排名公式的詳細資訊，請參閱[此區段](../offer-library/create-ranking-formulas.md)。

## 將排名公式分配給版位{#assign-ranking-formula}

建立排名公式後，您可以將其指派給決策中的版位。 若要這麼做，請遵循下列步驟：

* 建立決策或編輯現有決策，然後建立將包含您選件的版位（請參閱[建立決策](../offer-activities/create-offer-activities.md)）。

* 對於每個位置，從下拉式清單中選取&#x200B;**[!UICONTROL Ranking]**，然後按一下&#x200B;**[!UICONTROL Add ranking]**。

   ![](../../assets/offer-activity-ranking.png)

* 選擇所需的排名公式，然後按一下&#x200B;**[!UICONTROL Select]**。

   ![](../../assets/ranking-selection.png)

排名公式現在與版位相關聯。 如果多個優惠方案符合在此版位中呈現的資格，決策會使用排名公式的公式來計算要先傳送哪個優惠方案。
