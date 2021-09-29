---
product: experience platform
solution: Experience Platform
title: 建立排名策略
description: 了解如何在Adobe Experience Platform中建立排名策略。
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 4%

---

# AI 排名 {#ai-rankings}

## 開始使用AI排名

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can use an trained model system that ranks offers to display for a given profile.

>[!CAUTION]
>
>目前，僅供選取使用者提早存取，才可使用AI排名。

此功能可讓您根據業務目標建立不同的&#x200B;**排名策略**。 在決策中使用這些不同的目標型策略（先前稱為優惠方案活動），經過訓練的模型系統將幫助您了解不同的排名策略如何影響您的目標。

例如，您可以為電子郵件管道選取排名策略，為推播管道選取另一個排名策略。 對於每個管道，經過訓練的模型系統將利用多個資料點來決定應先針對指定版位呈現哪個優惠方案，而非考慮優惠方案的優先順序分數或[排名公式](create-ranking-formulas.md)。

<!--This feature is not enabled by default. To be able to use it, reach out to your Adobe contact.-->

建立排名策略後，將其指派至決策中的位置。 進一步了解[在決策](../offer-activities/configure-offer-selection.md)中設定選件選取項目。

## 建立排名策略 {#create-ranking-strategy}

若要建立排名策略，請遵循下列步驟：

1. 訪問&#x200B;**[!UICONTROL Components]**&#x200B;菜單，然後選擇&#x200B;**[!UICONTROL AI rankings]**&#x200B;頁簽。

   ![](../../assets/ai-ranking-list.png)

   列出了目前建立的所有排名策略。

1. 按一下「**[!UICONTROL Create strategy]**」按鈕。

1. 填寫下列欄位：

   ![](../../assets/ai-ranking-fields.png)

   * **[!UICONTROL Name]**:必須提供的唯一名稱。

   * **[!UICONTROL Model type]**:目前唯一支援的模型類型 **[!UICONTROL Auto-optimization]**&#x200B;是。<!--More will be supported in the future so the drop-down list will be enabled.-->

   * **[!UICONTROL Optimization metric]**：

      此選項可讓行銷人員選擇機器學習模型的建立與訓練方式：會根據顯示的選件、點按電子郵件的選件，和/或點按網頁的選件。

      >[!NOTE]
      >
      >您可以視需要選取所有量度類型。

      最佳化量度有兩種類型：
      * **[!UICONTROL Impression]**:目前曝光事件對應至顯示的所有選件。
      * **[!UICONTROL Conversion]**:轉換事件對應至所有導致透過電子郵件或網頁點按的選件。

      所有選取的曝光事件和/或轉換事件都會使用已提供的Web SDK或行動SDK自動擷取。 如需詳細資訊，請參閱[Adobe Experience Platform Web SDK概述](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant)。

   * **[!UICONTROL Dataset ID]**:若要轉換，您必須從下拉式清單中選取資料集，以便提供收集事件的資料集。了解如何在[此區段](#create-dataset)中建立這類資料集。 <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >只有從與&#x200B;**[!UICONTROL Experience Event - Proposition Interactions]**&#x200B;欄位群組（先前稱為mixin）相關聯的結構建立的資料集才會顯示在下拉式清單中。

1. 儲存並啟動排名策略。

   ![](../../assets/ai-ranking-save-activate.png)

現在已可用於決定對符合資格的優惠方案排名以刊登版位。 了解更多[此部分](../offer-activities/configure-offer-selection.md#use-ranking-strategy)。<!--TBC?-->

## 建立資料集以收集事件 {#create-dataset}

您需要建立要收集轉換事件的資料集。 首先，請建立要在資料集中使用的結構：

1. 從&#x200B;**[!UICONTROL Data Management]**&#x200B;菜單中，選擇&#x200B;**[!UICONTROL Schema]**，轉到&#x200B;**[!UICONTROL Browse]**&#x200B;頁簽，然後按一下&#x200B;**[!UICONTROL Create schema]**。

   ![](../../assets/ai-ranking-create-schema.png)

1. 選擇&#x200B;**[!UICONTROL XDM ExperienceEvent]**。

   ![](../../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    [XDM系統概觀檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)中，深入了解XDM結構和欄位群組。


1. 在&#x200B;**[!UICONTROL Search]**&#x200B;欄位中，鍵入&quot;postimation interaction&quot;並選擇&#x200B;**[!UICONTROL Experience Event - Proposition Interactions]**&#x200B;欄位組。

   ![](../../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    資料集中使用的結構必須具有與之關聯的&#x200B;**[!UICONTROL Experience Event - Proposition Interactions]**&#x200B;欄位群組。 否則，您將無法在排名策略中使用它。

1. 按一下「**[!UICONTROL Add field groups]**」。

   ![](../../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >欄位群組先前稱為mixin。


1. 鍵入名稱並保存架構。<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    進一步了解在[結構構成基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas)中建立結構。

您現在可以使用此結構建立資料集。 若要這麼做，請遵循下列步驟：

1. 從&#x200B;**[!UICONTROL Data Management]**&#x200B;菜單中，選擇&#x200B;**[!UICONTROL Datasets]**，轉到&#x200B;**[!UICONTROL Browse]**&#x200B;頁簽，然後按一下&#x200B;**[!UICONTROL Create dataset]**。

   ![](../../assets/ai-ranking-create-dataset.png)

1. 選擇「**[!UICONTROL Create dataset from schema]**」。

   ![](../../assets/ai-ranking-create-dataset-from-schema.png)

1. 從清單中選取剛建立的架構。

   ![](../../assets/ai-ranking-dataset-select-schema.png)

1. 按一下「**[!UICONTROL Next]**」。

1. 在&#x200B;**[!UICONTROL Name]**&#x200B;欄位中提供資料集的唯一名稱，然後按一下&#x200B;**[!UICONTROL Finish]**。

   ![](../../assets/ai-ranking-dataset-name.png)

現在，當[建立排名策略](#create-ranking-strategy)時，可以選取資料集來收集轉換事件。

<!--## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision (previously known as offer activity). For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).-->

