---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 使用決策管理事件
description: 了解如何在 Adobe Experience Platform 建立決策管理報吿。
badge: label="舊版" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/r3bOKyWcAT-sqI7KXA3J-Yi5TUax9KGi-8JY62QD6tA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: c132d929-fa62-4271-803e-b823be07b914id: c20d46e7-1c7d-476c-a50e-3961d4dce35fid: ed0d8d0e-04b9-4326-be72-a0fbca265377id: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 321
ht-degree: 100%

---

# 開始使用決策管理事件 {#monitor-offer-events}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../../experience-decisioning/gs-experience-decisioning.md)

每當決策管理為特定輪廓做出決定時，這些事件的相關資訊就會自動傳送至 Adobe Experience Platform。

這可讓您針對決策獲得洞察，例如，了解哪項產品建議已呈現給指定輪廓。 您可匯出這些資料，將其分析至您自己的報告系統，或善用 Adobe Experience Platform [查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=zh-Hant)與其他工具，以達到增強分析與報告的目的。

## 資料集的可用重要資訊 {#key-information}

每個在決策時傳送的事件都包含四個關鍵資料點，可供您用於分析和報告用途：

![](../assets/events-dataset-preview.png)

* **[!UICONTROL 遞補內容]**：後備產品建議的名稱和 ID，若未選取個人化產品建議，
* **[!UICONTROL 位置]**：用來傳遞產品建議之位置的名稱、ID 和頻道，
* **[!UICONTROL 選取項目]**：為輪廓選取之產品建議的名稱和 ID，
* **[!UICONTROL 活動]**：決策的名稱與 ID。

此外，您也可以運用 **[!UICONTROL identityMap]** 與&#x200B;**[!UICONTROL 時間戳記]**&#x200B;欄位來擷取有關輪廓和傳遞產品建議時間的資訊。

有關隨每個決定傳送的所有 XDM 欄位的詳細資訊，請參閱[本節](xdm-fields.md)。

## 存取資料集 {#access-datasets}

包含決策管理事件的資料集可從 Adobe Experience Platform **[!UICONTROL 資料集]**&#x200B;選單存取。 每個執行個體佈建時會自動建立一個資料集。

![](../assets/events-datasets-list.png)

這些資料集以 **[!UICONTROL ODE DecisionEvents]** 結構描述為基礎，其中包含將資訊從決策管理傳送到 Adobe Experience Platform 所需的所有 XDM 欄位。

>[!NOTE]
>
>請注意，ODE DecisionEvents 資料集是&#x200B;**非輪廓資料集**，這代表它們不能擷取至 Experience Platform 中，以便由即時客戶輪廓所使用。
