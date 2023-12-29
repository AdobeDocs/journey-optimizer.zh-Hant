---
product: experience platform
solution: Experience Platform
title: 建立資料集以收集事件
description: 瞭解如何建立資料集以收集事件
feature: Ranking, Decision Management, Datasets
role: Data Engineer, Developer
level: Experienced
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 7%

---

# 建立資料集以收集事件 {#create-dataset}

若要收集體驗事件，您必須先建立要傳送這些事件的資料集。

首先，請建立要在資料集中使用的結構描述：

1. 從 **[!UICONTROL 資料管理]** 功能表，選取 **[!UICONTROL 結構描述]**.

1. 按一下 **[!UICONTROL 建立結構描述]**，在右上方，選取 **[!UICONTROL 體驗事件]** 並按一下 **下一個**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >瞭解更多關於XDM結構描述和欄位群組 [XDM系統總覽檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.

1. 輸入綱要的名稱和說明，然後按一下 **完成**.
   ![](../assets/ai-ranking-xdm-event-2.png)

1. 從 **[!UICONTROL 欄位群組]** 部分，選取 **[!UICONTROL 新增]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. 在 **[!UICONTROL 搜尋]** 欄位，輸入「主張互動」。

1. 選取 **[!UICONTROL 體驗事件 — 主張互動]** 欄位群組並按一下 **[!UICONTROL 新增欄位群組]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >資料集中使用的結構描述必須具有 **[!UICONTROL 體驗事件 — 主張互動]** 與其相關聯的欄位群組。 否則，您將無法在AI模型中使用它。

1. 儲存結構。

>[!NOTE]
>
>進一步瞭解在中建立結構描述 [結構描述組合基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#understanding-schemas){target="_blank"}.

您現在已準備好使用此結構描述建立資料集。 請依照下列步驟執行此操作：

1. 從 **[!UICONTROL 資料管理]** 功能表，選取 **[!UICONTROL 資料集]** 並前往 **[!UICONTROL 瀏覽]** 標籤。

1. 按一下 **[!UICONTROL 建立資料集]** 並選取 **[!UICONTROL 從結構描述建立資料集]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 從清單中選取您剛建立的綱要，然後按一下 **[!UICONTROL 下一個]**.

1. 為中的資料集提供唯一名稱 **[!UICONTROL 名稱]** 欄位並按一下 **[!UICONTROL 完成]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>現在可以選取此資料集，以便在下列情況下收集事件資料： [建立AI模型](../ranking/create-ranking-strategies.md).
