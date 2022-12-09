---
product: experience platform
solution: Experience Platform
title: 建立資料集以收集事件
description: 了解如何建立資料集以收集事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# 建立資料集以收集事件 {#create-dataset}

建立AI模型之前，您需要建立要收集轉換事件的資料集。 首先，請建立要在資料集中使用的結構：

1. 從 **[!UICONTROL Data Management]** 菜單，選擇 **[!UICONTROL Schema]**，前往 **[!UICONTROL Browse]** 按一下 **[!UICONTROL Create schema]**.

   ![](../assets/ai-ranking-create-schema.png)

1. 選擇 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >如需XDM結構和欄位群組的詳細資訊，請參閱 [XDM系統概觀檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en){target=&quot;_blank&quot;}。

1. 從 **[!UICONTROL Field groups]** 區段，選取 **[!UICONTROL Add]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. 在 **[!UICONTROL Search]** 欄位，輸入「主張互動」並選取 **[!UICONTROL Experience Event - Proposition Interactions]** 欄位群組。

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >資料集中使用的結構必須具有 **[!UICONTROL Experience Event - Proposition Interactions]** 與其相關聯的欄位群組。 否則，您將無法在排名策略中使用它。

1. 按一下 **[!UICONTROL Add field groups]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >欄位群組先前稱為mixin。

1. 輸入名稱並儲存架構。

>[!NOTE]
>
>進一步了解如何建立結構 [結構構成基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target=&quot;_blank&quot;}。

您現在可以使用此結構建立資料集。 若要這麼做，請遵循下列步驟：

1. 從 **[!UICONTROL Data Management]** 菜單，選擇 **[!UICONTROL Datasets]**，前往 **[!UICONTROL Browse]** 按一下 **[!UICONTROL Create dataset]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. 選擇 **[!UICONTROL Create dataset from schema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 從清單中選取剛建立的架構。

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. 按一下 **[!UICONTROL Next]**.

1. 為 **[!UICONTROL Name]** 欄位，按一下 **[!UICONTROL Finish]**.

   ![](../assets/ai-ranking-dataset-name.png)

現在已可選取資料集，以收集事件資料 [建立排名策略](#create-ranking-strategy).
