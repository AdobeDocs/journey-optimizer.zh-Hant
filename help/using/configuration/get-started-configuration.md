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
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---


# 開始使用 [!DNL Journey Optimizer] 配置 {#start-optimizer-configuration}

存取 [!DNL Journey Optimizer] 系統會首次布建生產沙箱，並根據您的合約分配特定數量的IP。

若要建立您的歷程並傳送訊息，您必須執行下列設定步驟。

## 設定訊息和通道

1. 若要建立和傳送訊息，您需要根據通道執行特定設定。

   * 若 **電子郵件** 管道中，您需要將子網域委派給Adobe，並建立IP池以將IP位址分組。 [深入了解](../email/get-started-email-config.md)

   * 若 **推播** 管道，您必須在 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch]. [深入了解](../push/push-configuration.md)

   * 若 **簡訊** 通道時，您需要設定執行個體以傳送簡訊，包括整合提供者設定與 [!DNL Journey Optimizer]. [深入了解](../sms/sms-configuration.md)

1. 完成後，您必須建立 **通道曲面** 設定傳送訊息所需的所有技術參數。 [深入了解](channel-surfaces.md)

1. 您也可以：

   * 在將電子郵件地址發送到隱藏清單之前，管理執行重試的天數。 [深入了解](manage-suppression-list.md)

   * 啟用 **BBC電子郵件選項** 保存傳送給個人的訊息副本。 [深入了解](archiving-support.md#enable-bcc)

   * 設定 **頻率規則** 以避免過度關注收件者。 [深入了解](frequency-rules.md)

   * 當Adobe Experience Platform中有數個地址/號碼可用時，決定要優先用於收件者的電子郵件地址和/或電話號碼。 [深入了解](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>這些步驟必須由 [Adobe Journey Optimizer系統管理員](../start/path/administrator.md).

## 設定歷程

若要建立歷程，您需要設定 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**. [深入了解](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* 此 **資料來源** 設定可讓您定義系統的連線，以擷取將用於歷程的其他資訊。 [深入了解](../datasource/about-data-sources.md)

* **事件** 可讓您一直觸發歷程，即時傳送訊息給流入歷程的個人。 在事件設定中，您會設定歷程中預期的事件。 會依照Adobe Experience Data Model(XDM)，對傳入事件的資料進行標準化。 事件來自串流獲取API，適用於已驗證和未驗證的事件（例如Adobe Mobile SDK事件）。 [深入了解](../event/about-events.md)

* [!DNL Journey Optimizer] 隨附內建的訊息功能，可讓您設計和傳送內容。 如果您使用協力廠商系統來傳送訊息，請建立 **自訂動作**. [深入了解](../action/action.md)