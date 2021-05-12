---
title: 在決策中設定選件選擇
description: 瞭解如何在決策中管理選件。
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# 在{#offers-selection-in-activities}決策中設定選件選擇

## 關於選件優先順序{#about-offers-priority}

依預設，當數個選件符合在決定中指定位置的資格（先前稱為選件活動）時，優先順序最高&#x200B;****&#x200B;的選件會先傳送給客戶。 建立選件時會指派選件的優先順序分數（請參閱[建立個人化選件](../offer-library/creating-personalized-offers.md)）。

![](../../assets/offer-priority.png)

此外，Journey Optimizer還允許您建立&#x200B;**排名公式**。 這些公式可決定在指定位置應先顯示哪個選件，而非考慮選件的優先順序分數。 例如，您可以提高結束日期不到24小時的所有選件的優先順序，或是在描述檔的興趣點為「執行中」時，提升「執行中」類別的選件。

如需如何建立排名公式的詳細資訊，請參閱[本節](../offer-library/create-ranking-formulas.md)。

## 為位置{#assign-ranking-formula}指定排名公式

建立排名公式後，您就可以將其指派給決策中的位置。 若要這麼做，請依照下列步驟進行：

* 建立決策或編輯現有決策，然後建立包含您選件的位置（請參閱[建立決策](../offer-activities/create-offer-activities.md)）。

* 對於每個位置，從下拉式清單中選擇&#x200B;**[!UICONTROL Ranking]**，然後按一下&#x200B;**[!UICONTROL Add ranking]**。

   ![](../../assets/offer-activity-ranking.png)

* 選取所要的排名公式，然後按一下&#x200B;**[!UICONTROL Select]**。

   ![](../../assets/ranking-selection.png)

排名公式現在會與位置相關聯。 如果多個選件符合在此位置中顯示的資格，則決定會使用排名公式的公式來計算要先傳送的選件。
