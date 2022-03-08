---
title: 開始使用決定管理事件
description: 瞭解如何在Adobe Experience Platform建立決策管理報告。
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 57%

---

# 開始使用決定管理事件 {#monitor-offer-events}

每次決策管理部門對給定配置檔案做出決策時，與這些事件相關的資訊都會自動發送到Adobe Experience Platform。

這可讓您匯出這些資料，以便將其分析至您自己的報吿系統。 您也可以善用 Adobe Experience Platform [查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=zh-Hant)與其他工具，以達到增強分析和報告的目的。

包含決策管理事件的資料集可以從Adobe Experience Platform訪問 **[!UICONTROL Datasets]** 的子菜單。 每個執行個體佈建時會自動建立一個資料集。

![](../assets/events-datasets-list.png)

這些資料集基於 **[!UICONTROL ODE DecisionEvents]** 架構，包含從決策管理向Adobe Experience Platform發送資訊所需的所有XDM欄位。

>[!NOTE]
>
>請注意，ODE DecisionEvents 資料集是&#x200B;**非設定檔資料集**，這代表它們不能被獲取至 Experience Platform 中，以便由即時客戶設定檔所使用。

**相關主題：**

* [決定管理事件重要資訊](../reports/key-information.md)
* [存取事件 XDM 欄位](../reports/xdm-fields.md)
