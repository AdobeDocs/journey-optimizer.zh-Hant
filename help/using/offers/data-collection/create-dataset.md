---
product: experience platform
solution: Experience Platform
title: 建立資料集以收集事件
description: 瞭解如何建立資料集以收集事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 10%

---

# 建立資料集以收集事件 {#create-dataset}

要收集體驗事件，您首先需要建立一個資料集，在該資料集中將發送這些事件。

首先建立將在資料集中使用的架構：

1. 從 **[!UICONTROL 資料管理]** 菜單，選擇 **[!UICONTROL 架構]** 去 **[!UICONTROL 瀏覽]** 頁籤。

1. 按一下 **[!UICONTROL 建立架構]** 選擇 **[!UICONTROL XDM體驗事件]**。

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >瞭解有關中的XDM架構和欄位組的詳細資訊 [XDM系統概述文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}。

1. 從 **[!UICONTROL 欄位組]** ，選擇 **[!UICONTROL 添加]**。

   ![](../assets/ai-ranking-fields-groups.png)

1. 在 **[!UICONTROL 搜索]** 鍵入「命題交互」。

1. 選擇 **[!UICONTROL 體驗事件 — 建議交互]** 欄位組，按一下 **[!UICONTROL 添加欄位組]**。

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >將在資料集中使用的架構必須具有 **[!UICONTROL 體驗事件 — 建議交互]** 與其關聯的欄位組。 否則，您將無法在排名策略中使用它。

1. 鍵入名稱並保存架構。

>[!NOTE]
>
>瞭解有關在中構建架構的詳細資訊 [架構組合的基礎](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target="_blank"}。

您現在已準備好使用此架構建立資料集。 請依照下列步驟執行此操作：

1. 從 **[!UICONTROL 資料管理]** 菜單，選擇 **[!UICONTROL 資料集]** 去 **[!UICONTROL 瀏覽]** 頁籤。

1. 按一下 **[!UICONTROL 建立資料集]** 選擇 **[!UICONTROL 從架構建立資料集]**。

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 從清單中選擇剛建立的架構，然後按一下 **[!UICONTROL 下一個]**。

1. 為中的資料集提供唯一名稱 **[!UICONTROL 名稱]** 按一下 **[!UICONTROL 完成]**。

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>現在，可以選擇此資料集以在 [建立排名策略](#create-ranking-strategy)。
