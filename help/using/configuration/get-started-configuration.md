---
title: Journey Optimizer設定與設定准則
description: 了解訊息和歷程設定准則
audience: administrators
content-type: reference
role: Administrator
level: Intermediate
product: Adobe Journey Optimizer
solution: Journey Optimizer
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: 應用程式設定
topic: 管理
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 10%

---


# 開始使用[!DNL Journey Optimizer]配置

第一次存取[!DNL Journey Optimizer]時，您會布建生產沙箱，並根據您的合約分配特定數量的IP。

若要建立歷程及傳送訊息，您必須執行下列設定步驟：

1. **設定訊息和通道**:定義預設集、調整和自訂電子郵件及推播訊息

   * 定義[!DNL Adobe Experience Platform]和[!DNL Adobe Experience Platform Launch]中的推播通知設定。 [了解更多](../push-gs.md)

   * 建立訊息預設集，以設定電子郵件和推播通知訊息所需的所有技術參數。 [了解更多](message-presets.md)

   * 在Adobe Experience Platform中有數個地址可用時，決定要優先使用給收件者的電子郵件地址。 [了解更多](primary-email-addresses.md)

   * 在將電子郵件地址發送到隱藏清單之前，管理執行重試的天數。 [了解更多](manage-suppression-list.md)

   <!--
    * Understand push notification flow. [Learn more](../push-gs.md)
    -->

1. **委派子網域**:若要在Journey Optimizer中使用任何新子網域，第一步是將其委派。[了解更多](about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **建立IP池**:將與您執行個體布建的IP位址分組，以改善電子郵件傳遞能力和信譽。[了解更多](ip-pools.md)

   ![](../assets/ip-pool.png)

1. **設定歷程**:若要建立歷程，您需要設 **[!UICONTROL Data Sources]**&#x200B;定 **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**。[了解更多](about-data-sources-events-actions.md)

   ![](../assets/admin-menu.png)

   * **資料來源**&#x200B;設定可讓您定義系統連線，以擷取將用於歷程的其他資訊。 在此[小節](../datasource/about-data-sources.md)了解更多資料來源

   * **** 事件可讓您觸發歷程，以即時傳送訊息給流入歷程的個人。在事件設定中，您會設定歷程中預期的事件。 會依照Adobe Experience Data Model(XDM)，對傳入事件的資料進行標準化。 事件來自串流獲取 API，適用於驗證和未驗證的事件（例如 Adobe Mobile SDK 事件）。進一步了解此[小節](../event/about-events.md)中的事件

   * [!DNL Journey Optimizer] 隨附內建訊息功能：您可以設計內容並發佈訊息。如果您使用協力廠商系統來傳送訊息，請建立&#x200B;**自訂動作**。 進一步了解此[小節](../action/action.md)中的動作