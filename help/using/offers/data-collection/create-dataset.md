---
product: experience platform
solution: Experience Platform
title: 建立資料集以收集事件
description: 了解如何建立資料集以收集事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 12%

---

# 建立資料集以收集事件 {#create-dataset}

若要收集體驗事件，您必須先建立資料集，以便傳送這些事件。

首先，請建立要在資料集中使用的結構：

1. 從 **[!UICONTROL 資料管理]** 菜單，選擇 **[!UICONTROL 結構]**，前往 **[!UICONTROL 瀏覽]** 按一下 **[!UICONTROL 建立結構]**.

   ![](../assets/ai-ranking-create-schema.png)

1. 選擇 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >如需XDM結構和欄位群組的詳細資訊，請參閱 [XDM系統概觀檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.

1. 從 **[!UICONTROL 欄位群組]** 區段，選取 **[!UICONTROL 新增]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. 在 **[!UICONTROL 搜尋]** 欄位，輸入「主張互動」並選取 **[!UICONTROL 體驗事件 — 主張互動]** 欄位群組。

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >資料集中使用的結構必須具有 **[!UICONTROL 體驗事件 — 主張互動]** 與其相關聯的欄位群組。 否則，您將無法在排名策略中使用它。

1. 按一下 **[!UICONTROL 新增欄位群組]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >欄位群組先前稱為mixin。

1. 輸入名稱並儲存架構。

>[!NOTE]
>
>進一步了解如何建立結構 [結構構成基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target="_blank"}.

您現在可以使用此結構建立資料集。 請依照下列步驟執行此操作：

1. 從 **[!UICONTROL 資料管理]** 菜單，選擇 **[!UICONTROL 資料集]**，前往 **[!UICONTROL 瀏覽]** 按一下 **[!UICONTROL 建立資料集]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. 選取&#x200B;**[!UICONTROL 「從結構建立資料集」]**。

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 從清單中選取剛建立的架構。

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. 按&#x200B;**[!UICONTROL 「下一步」]**。

1. 為 **[!UICONTROL 名稱]** 欄位，按一下 **[!UICONTROL 完成]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>現在可選取此資料集，以在 [建立排名策略](#create-ranking-strategy).
