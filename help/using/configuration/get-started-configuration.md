---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 [!DNL Journey Optimizer] 配置
description: 深入了解 [!DNL Journey Optimizer] 配置
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 11%

---


# 開始使用 [!DNL Journey Optimizer] 配置 {#start-optimizer-configuration}

存取 [!DNL Journey Optimizer] 系統會首次布建生產沙箱，並根據您的合約分配特定數量的IP。

若要建立歷程及傳送訊息，您必須執行下列設定步驟：

1. **設定訊息和通道**:定義通道曲面、調整和自訂訊息。

   * 建立通道表面以配置傳送訊息所需的所有技術參數。 [了解更多](channel-surfaces.md)

   * 在Adobe Experience Platform中有數個地址可用時，決定要優先使用給收件者的電子郵件地址。 [了解更多](primary-email-addresses.md)

   * 在將電子郵件地址發送到隱藏清單之前，管理執行重試的天數。 [了解更多](manage-suppression-list.md)

   * 在兩者中定義推播通知設定 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch]. [了解更多](../configuration/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../configuration/push-gs.md)-->

   * 設定您的執行個體以傳送SMS（目前僅適用於一組組織 — 有限可用性）。 [了解更多](sms-configuration.md)


1. **委派子網域**:若要在Journey Optimizer中使用任何新子網域，第一步是將其委派。 [了解更多](about-subdomain-delegation.md)

   ![](assets/subdomain.png)

1. **建立IP池**:將與您執行個體布建的IP位址分組，以改善電子郵件傳遞能力和信譽。 [了解更多](ip-pools.md)

   ![](assets/ip-pool.png)

1. **設定歷程**:若要建立歷程，您需要設定 **[!UICONTROL 資料來源]**, **[!UICONTROL 事件]** 和 **[!UICONTROL 動作]**. [了解更多](about-data-sources-events-actions.md)

   ![](assets/admin-menu.png)

   * 此 **資料來源** 設定可讓您定義系統的連線，以擷取將用於歷程的其他資訊。 [了解更多](../datasource/about-data-sources.md)

   * **事件** 可讓您一直觸發歷程，即時傳送訊息給流入歷程的個人。 在事件設定中，您會設定歷程中預期的事件。 會依照Adobe Experience Data Model(XDM)，對傳入事件的資料進行標準化。 事件來自串流獲取 API，適用於驗證和未驗證的事件（例如 Adobe Mobile SDK 事件）。[了解更多](../event/about-events.md)

   * [!DNL Journey Optimizer] 隨附內建的訊息功能，可讓您設計和傳送內容。 如果您使用協力廠商系統來傳送訊息，請建立 **自訂動作**. [了解更多](../action/action.md)