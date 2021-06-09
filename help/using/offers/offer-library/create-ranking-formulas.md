---
title: 建立排名公式
description: 了解如何在Adobe Experience Platform中建立排名公式。
source-git-commit: ea8a3644ecef911a14ea087b03d367976f0c898d
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 2%

---

# 建立排名公式 {#create-ranking-formulas}

## 關於排名公式{#about-ranking-formulas}

**排名** 公式化可讓您定義規則，以決定應先針對指定版位顯示哪個優惠方案，而非考慮優惠方案的優先順序分數。

排名公式以&#x200B;**PQL語法**&#x200B;表示，並且可以利用配置檔案屬性、上下文資料和選件屬性。 有關如何使用PQL語法的詳細資訊，請參閱[專用文檔](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html)。

建立排名公式後，您就可以將其指派至決策中的版位（先前稱為優惠方案活動）。 如需詳細資訊，請參閱[在決策](../offer-activities/configure-offer-selection.md)中設定選件選取項目。

## 建立排名公式{#create-ranking-formula}

若要建立排名公式，請遵循下列步驟：

1. 訪問&#x200B;**[!UICONTROL Components]**&#x200B;菜單，然後選擇&#x200B;**[!UICONTROL Rankings]**&#x200B;頁簽。 將顯示先前建立的排名清單。

   ![](../../assets/rankings-list.png)

1. 按一下&#x200B;**[!UICONTROL Create ranking]**&#x200B;以建立新的排名公式。

   ![](../../assets/ranking-create-formula.png)

1. 指定排名公式名稱、說明和公式。

   在此範例中，如果實際天氣炎熱，我們想利用「hot」屬性提升所有選件的優先順序。 為此，已在決策呼叫中傳遞&#x200B;**contextData.weather=hot**。

   ![](../../assets/ranking-syntax.png)

1. 按一下「**[!UICONTROL Save]**」。排名公式已建立，您可以從清單中選取它以取得詳細資訊，並加以編輯或刪除。

   現在已可用於為版位排名合格優惠方案的決策（請參閱[在決策](../offer-activities/configure-offer-selection.md)中設定優惠方案選取項目）。

   ![](../../assets/ranking-formula-created.png)
