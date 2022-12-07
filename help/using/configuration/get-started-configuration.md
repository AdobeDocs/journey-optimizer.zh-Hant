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
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 40%

---


# 開始使用 [!DNL Journey Optimizer] 配置 {#start-optimizer-configuration}

首次存取 [!DNL Journey Optimizer] 系統時，會佈建生產沙箱，並根據您的合約分配特定數量的 IP。

若要建立您的歷程並傳送訊息，您必須執行下列設定步驟。

## 設定訊息和通道

定義通道表面、調整和自訂訊息。

* [委派以Adobe子網域](about-subdomain-delegation.md) 您想要用來傳送電子郵件和 [建立IP池](ip-pools.md) 將布建的IP位址與您的執行個體分組。

* 管理將電子郵件地址傳送至隱藏清單前執行重試的天數。[了解更多](manage-suppression-list.md)

* 在 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch] 中定義推播通知設定[了解更多](../push/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

* 設定您的執行個體以傳送SMS（目前僅適用於一組組織 — 有限可用性）。 [了解更多](../sms/sms-configuration.md)

* 建立通道表面以配置傳送訊息所需的所有技術參數。 [了解更多](channel-surfaces.md)

* 在Adobe Experience Platform中提供數個地址/號碼時，決定要優先用於收件者的電子郵件地址和/或電話號碼。 [了解更多](primary-email-addresses.md)

## 設定歷程

若要建立歷程，您需要設定 **[!UICONTROL 資料來源]**, **[!UICONTROL 事件]** 和 **[!UICONTROL 動作]**. [了解更多](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* 此 **資料來源** 設定可讓您定義系統的連線，以擷取將用於歷程的其他資訊。 [了解更多](../datasource/about-data-sources.md)

* **事件**&#x200B;可讓您一直觸發歷程，以即時傳送訊息給流入歷程的個人。 在事件設定中，您會設定歷程中預期的事件。 會依照 Adobe Experience Data Model (XDM)，對傳入事件的資料進行標準化。事件來自串流獲取 API，適用於驗證和未驗證的事件（例如 Adobe Mobile SDK 事件）。[了解更多](../event/about-events.md)

* [!DNL Journey Optimizer] 隨附內建的訊息功能，可讓您設計和傳送內容。 如果您使用協力廠商系統來傳送訊息，請建立 **自訂動作**. [了解更多](../action/action.md)