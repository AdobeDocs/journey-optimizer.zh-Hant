---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 [!DNL Journey Optimizer] 通道設定
description: 深入瞭解 [!DNL Journey Optimizer] 頻道設定
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: 設定、配置、訊息、通道、沙箱、最佳化程式
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 43%

---


# 開始使用頻道設定 {#start-optimizer-configuration}

>[!CONTEXTUALHELP]
>id="ajo_channels_rate_controls"
>title="管道的速率控制"
>abstract="管道的速率控制"

首次存取 [!DNL Journey Optimizer] 系統時，會佈建生產沙箱，並根據您的合約分配特定數量的 IP。

若要傳送訊息，您必須完成下列設定步驟：

1. 作為[Adobe Journey Optimizer系統管理員](../start/path/administrator.md)，請定義您的頻道特定設定。 請在下列頁面瞭解如何設定這些設定：

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="電子郵件" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong>電子郵件</strong></a></div></td>
    <td><a href="../sms/sms-configuration.md"><img alt="簡訊" src="../channels/assets/do-not-localize/sms.png"></a>
    <div align="center"><a href="../sms/sms-configuration.md"><strong>簡訊</strong></a></div></td>
    <td><a href="../push/push-configuration.md"><img alt="推播" src="../channels/assets/do-not-localize/push.png"></a>
    <div align="center"><a href="../push/push-configuration.md"><strong>推播通知</strong></a></div></td>
    <td><a href="../direct-mail/direct-mail-configuration.md"><img alt="直接郵件" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
    <div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>直接郵件</strong></a></div></td>
    </tr></table>

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../in-app/inapp-configuration.md"><img alt="應用程式內" src="../channels/assets/do-not-localize/inapp.jpg"></a>
    <div align="center"><a href="../in-app/inapp-configuration.md"><strong>應用程式內</strong></a></div></td>
    <td><a href="../web/web-configuration.md"><img alt="網頁" src="../channels/assets/do-not-localize/web.jpg"></a>
    <div align="center"><a href="../web/web-configuration.md"><strong>網頁</strong></a></div></td>
    <td><a href="../code-based/code-based-configuration.md"><img alt="程式碼型體驗" src="../channels/assets/do-not-localize/code.png"></a>
    <div align="center"><a href="../code-based/code-based-configuration.md"><strong>程式碼型體驗</strong></a></div></td>
    <td><a href="../content-card/content-card-configuration-prereq.md"><img alt="內容卡" src="../channels/assets/do-not-localize/cards.png"></a>
    <div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>內容卡</strong></a></div></td>
    </tr></table>

   >[!NOTE]
   >
   >針對行動裝置頻道，[引導式頻道設定](set-mobile-config.md)有助於快速設定行銷頻道，確保所有必要資源都能隨時在Experience Platform、Journey Optimizer和資料收集中取得。 這可讓您的行銷團隊開始建立行銷活動和歷程。

1. 完成之後，您必須透過建立&#x200B;**通道設定**&#x200B;來設定傳遞訊息所需的所有技術引數。 [進一步瞭解頻道設定](channel-surfaces.md)

1. 根據您使用的頻道、您的環境和您的需求，您還必須執行以下步驟：

   * 您管道的子網域設定和委派，例如[電子郵件](about-subdomain-delegation.md)、[簡訊](../sms/sms-subdomains.md)、[登陸頁面](../landing-pages/lp-subdomains.md)和[網頁體驗](../web/web-delegated-subdomains.md)。

   * 設定IP熱身計畫以獲得最佳傳遞能力。 [了解更多](ip-warmup-gs.md)

   * 定義電子郵件傳送的允許清單。 [了解更多](allow-list.md)

   * 管理將電子郵件地址傳送至禁止名單前執行重試的天數。[了解更多](manage-suppression-list.md)

   * 啟用&#x200B;**密件副本電子郵件選項**，以保留傳送給個人的郵件復本。 [了解更多](archiving-support.md#enable-bcc)

   * 設定&#x200B;**商業規則**&#x200B;以避免過度向收件者請求。 [了解更多](../conflict-prioritization/rule-sets.md)

   * 當 Adobe Experience Platform 有多個位址/號碼可用時，請確定收件者優先使用哪個電子郵件位址和/或電話號碼。[了解更多](primary-email-addresses.md)
