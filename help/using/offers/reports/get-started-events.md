---
title: 開始使用決策管理事件
description: 了解如何在Adobe Experience Platform中建立決策管理報表。
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# 開始使用決策管理事件 {#monitor-offer-events}

每次Decision Management針對指定的設定檔進行決策時，與這些事件相關的資訊都會自動傳送至Adobe Experience Platform。

這可讓您匯出這些資料，以將其分析至您自己的報表系統。 您也可以運用Adobe Experience Platform [查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/home.html) 與其他工具結合，以增強分析和報告用途。

包含「決策管理」事件的資料集可從Adobe Experience Platform存取 **[!UICONTROL Datasets]** 功能表。 布建時，系統會自動為每個執行個體建立一個資料集。

![](../assets/events-datasets-list.png)

這些資料集以 **[!UICONTROL ODE DecisionEvents]** 結構，包含從決策管理傳送資訊至Adobe Experience Platform所需的所有XDM欄位。

>[!NOTE]
>
>請注意，ODE DecisionEvents資料集 **非設定檔資料集**，這表示這些量度無法擷取至Experience Platform供即時客戶設定檔使用。

**相關主題：**

* [決策管理事件關鍵資訊](../reports/key-information.md)
* [存取事件XDM欄位](../reports/xdm-fields.md)
