---
title: 開始使用決策管理事件
description: 瞭解如何在Adobe Experience Platform建立決策管理報表。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 47%

---

# 開始使用決策管理事件{#monitor-offer-events}

每當決策管理部門針對特定個人檔案做出決策時，與這些事件相關的資訊就會自動傳送至Adobe Experience Platform。

這可讓您匯出這些資料，以便將其分析至您自己的報吿系統。 您也可以善用 Adobe Experience Platform [查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=zh-Hant)與其他工具，以達到增強分析和報告的目的。

可從Adobe Experience Platform **[!UICONTROL Datasets]**&#x200B;菜單訪問包含決策管理事件的資料集。 每個執行個體佈建時會自動建立一個資料集。

![](../assets/events-datasets-list.png)

這些資料集基於&#x200B;**[!UICONTROL ODE DecisionEvents]**&#x200B;模式，該模式包含從決策管理向Adobe Experience Platform發送資訊所需的所有XDM欄位。

>[!NOTE]
>
>請注意，ODE DecisionEvents 資料集是&#x200B;**非設定檔資料集**，這代表它們不能被獲取至 Experience Platform 中，以便由即時客戶設定檔所使用。

**相關主題：**

* [決策管理事件關鍵資訊](../reports/key-information.md)
* [存取事件 XDM 欄位](../reports/xdm-fields.md)
