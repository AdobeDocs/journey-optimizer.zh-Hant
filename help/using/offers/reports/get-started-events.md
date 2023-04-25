---
title: 使用決策管理事件
description: 了解如何在Adobe Experience Platform中建立決策管理報表。
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: a6a892ec20dfeb6879bef2f4c2eb4a0f8f54885f
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 21%

---

# 開始使用決定管理事件 {#monitor-offer-events}

每次決策管理人員針對指定的設定檔進行決策時，與這些事件相關的資訊都會自動傳送至Adobe Experience Platform。

這可讓您獲得決策的深入分析，例如，了解哪個選件已呈現給指定的設定檔。 您可以匯出這些資料，將其分析至您自己的報表系統，或運用Adobe Experience Platform [查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=zh-Hant) 與其他工具結合，以增強分析和報告用途。

## 資料集中可用的關鍵資訊 {#key-information}

決策時傳送的每個事件都包含四個關鍵資料點，您可運用這些資料點進行分析和報告：

![](../assets/events-dataset-preview.png)

* **[!UICONTROL 備援]**:備援優惠方案的名稱和ID，如果未選取個人化優惠方案，
* **[!UICONTROL 版位]**:用於傳送優惠方案之版位的名稱、ID和管道，
* **[!UICONTROL 選取項目]**:為設定檔選取之選件的名稱和ID,
* **[!UICONTROL 活動]**:決策的名稱和ID。

此外，您也可以運用 **[!UICONTROL identityMap]** 和 **[!UICONTROL 時間戳記]** 欄位來擷取設定檔資訊和傳送選件的時間。

有關隨每個決定傳送的所有 XDM 欄位的詳細資訊，請參閱[本節](xdm-fields.md)。

## 存取資料集 {#access-datasets}

包含Decision management事件的資料集可從Adobe Experience Platform存取 **[!UICONTROL 資料集]** 功能表。 每個執行個體佈建時會自動建立一個資料集。

![](../assets/events-datasets-list.png)

這些資料集以 **[!UICONTROL ODE DecisionEvents]** 結構，包含從決策管理傳送資訊至Adobe Experience Platform所需的所有XDM欄位。

>[!NOTE]
>
>請注意，ODE DecisionEvents 資料集是&#x200B;**非設定檔資料集**，這代表它們不能被獲取至 Experience Platform 中，以便由即時客戶設定檔所使用。
