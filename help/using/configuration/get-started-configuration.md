---
title: 開始 [!DNL Journey Optimizer] 配置
description: 瞭解有關 [!DNL Journey Optimizer] 配置
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 11%

---


# 開始 [!DNL Journey Optimizer] 配置 {#start-optimizer-configuration}

訪問 [!DNL Journey Optimizer] 您首次配置了生產沙盒並根據合同分配了特定數量的IP。

要能夠建立您的行程和發送消息，您需要完成以下配置步驟：

1. **配置消息和通道**:定義通道曲面、調整和定制消息。

   * 建立通道曲面以配置傳遞消息所需的所有技術參數。 [了解更多](message-presets.md)

   * 確定在Adobe Experience Platform有多個地址可用時優先使用的收件人電子郵件地址。 [了解更多](primary-email-addresses.md)

   * 管理在將電子郵件地址發送到禁止顯示清單之前執行重試的天數。 [了解更多](manage-suppression-list.md)

   * 在兩者中定義推送通知設定 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch]。 [了解更多](../configuration/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../configuration/push-gs.md)-->

   * 配置實例以發送SMS（當前僅適用於一組組織 — 有限可用性）。 [了解更多](sms-configuration.md)


1. **委託子域**:對於在Journey Optimizer使用的任何新子域，第一步是將其委派。 [了解更多](about-subdomain-delegation.md)

   ![](assets/subdomain.png)

1. **建立IP池**:通過將隨實例配置的IP地址組合在一起，提高電子郵件的可傳遞性和信譽。 [了解更多](ip-pools.md)

   ![](assets/ip-pool.png)

1. **配置行程**:為了構建旅程，您需要配置 **[!UICONTROL Data Sources]**。 **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**。 [了解更多](about-data-sources-events-actions.md)

   ![](assets/admin-menu.png)

   * 的 **資料源** 配置允許您定義到系統的連接，以檢索將在您的行程中使用的其他資訊。 [了解更多](../datasource/about-data-sources.md)

   * **事件** 允許你觸發整個旅程，即時地向流入旅程的個體發送消息。 在事件配置中，您可以配置行程中預期的事件。 傳入事件的資料按照Adobe體驗資料模型(XDM)進行規範化。 事件來自串流獲取 API，適用於驗證和未驗證的事件（例如 Adobe Mobile SDK 事件）。[了解更多](../event/about-events.md)

   * [!DNL Journey Optimizer] 內置消息功能，允許您設計和發送內容。 如果您使用第三方系統發送消息，請建立 **自定義操作**。 [了解更多](../action/action.md)