---
title: 建立排名公式
description: 瞭解如何在Adobe Experience Platform建立排名公式。
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# 建立排名公式 {#create-ranking-formulas}

## 關於對公式{#about-ranking-formulas}進行排名

**排** 名公式可讓您定義規則，以決定在指定位置應先顯示哪個選件，而不是考慮選件的優先順序分數。

排名公式以&#x200B;**PQL語法**&#x200B;表示，並可運用描述檔屬性、上下文資料和選件屬性。 有關如何使用PQL語法的詳細資訊，請參閱[專用文檔](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html)。

建立排名公式後，您就可以將其指派至決策中的位置（先前稱為選件活動）。 如需詳細資訊，請參閱[決策中的「設定選件選擇」。](../offer-activities/configure-offer-selection.md)

## 建立排名公式{#create-ranking-formula}

若要建立排名公式，請遵循下列步驟：

* 訪問&#x200B;**[!UICONTROL Components]**&#x200B;菜單，然後選擇&#x200B;**[!UICONTROL Rankings]**&#x200B;頁籤。

* 按一下&#x200B;**[!UICONTROL Create formula]**&#x200B;以建立新的排名公式。

   ![](../../assets/ranking-create-formula.png)

* 指定排名公式名稱、說明和公式。

   在此範例中，我們希望在實際天氣炎熱時，以「hot」屬性提升所有優惠的優先順序。 為此，**contextData.weather=hot**&#x200B;在決策呼叫中傳遞。

   ![](../../assets/ranking-syntax.png)

* 按一下「**[!UICONTROL Save]**」。排名公式已建立，您可從清單中選取它以取得詳細資訊，並加以編輯或刪除。

   現在，它已可用於對符合資格的選件進行位置排名的決定（請參閱[決策中的「設定選件選擇」）。](../offer-activities/configure-offer-selection.md)

   ![](../../assets/ranking-formula-created.png)
