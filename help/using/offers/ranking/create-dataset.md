---
product: experience platform
solution: Experience Platform
title: 建立資料集以收集事件
description: 瞭解如何建立資料集以收集事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 12%

---

# 建立資料集以收集事件 {#create-dataset}

在建立AI模型之前，您需要建立一個資料集，在該資料集中將收集轉換事件。 首先建立將在資料集中使用的架構：

1. 從 **[!UICONTROL Data Management]** 菜單，選擇 **[!UICONTROL Schema]**，轉到 **[!UICONTROL Browse]** 頁籤 **[!UICONTROL Create schema]**。

   ![](../assets/ai-ranking-create-schema.png)

1. 選擇 **[!UICONTROL XDM ExperienceEvent]**。

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >瞭解有關中的XDM架構和欄位組的詳細資訊 [XDM系統概述文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

1. 從 **[!UICONTROL Field groups]** ，選擇 **[!UICONTROL Add]**。

   ![](../assets/ai-ranking-fields-groups.png)

1. 在 **[!UICONTROL Search]** 欄位，鍵入「命題交互」並選擇 **[!UICONTROL Experience Event - Proposition Interactions]** 欄位組。

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >將在資料集中使用的架構必須具有 **[!UICONTROL Experience Event - Proposition Interactions]** 與其關聯的欄位組。 否則，您將無法在排名策略中使用它。

1. 按一下「**[!UICONTROL Add field groups]**」。

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >欄位組以前稱為mixin。

1. 鍵入名稱並保存架構。

>[!NOTE]
>
>瞭解有關在中構建架構的詳細資訊 [架構組合的基礎](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target=&quot;_blank&quot;}。

您現在已準備好使用此架構建立資料集。 請依照下列步驟執行此操作：

1. 從 **[!UICONTROL Data Management]** 菜單，選擇 **[!UICONTROL Datasets]**，轉到 **[!UICONTROL Browse]** 頁籤 **[!UICONTROL Create dataset]**。

   ![](../assets/ai-ranking-create-dataset.png)

1. 選擇「**[!UICONTROL Create dataset from schema]**」。

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 從清單中選擇剛建立的架構。

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. 按一下「**[!UICONTROL Next]**」。

1. 為中的資料集提供唯一名稱 **[!UICONTROL Name]** 按一下 **[!UICONTROL Finish]**。

   ![](../assets/ai-ranking-dataset-name.png)

該資料集現在已準備好在 [建立排名策略](#create-ranking-strategy)。
