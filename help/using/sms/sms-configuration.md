---
solution: Journey Optimizer
product: journey optimizer
title: 設定簡訊頻道
description: 瞭解如何設定您的環境，以使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: af03ad62c2c7b29d695670f083e0dfb6d0c71b93
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 37%

---

# 開始使用簡訊設定 {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="使用 Journey Optimizer 設定您的 SMS 服務提供者"
>abstract="Adobe Journey Optimizer 會透過簡訊服務供應商發送文字訊息。選取您的服務提供者並填寫您的 API 認證。"

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="使用 Journey Optimizer 設定您的 MMS 服務提供者"
>abstract="Adobe Journey Optimizer 會透過 MMS 服務提供者發送媒體內容。選取您的服務提供者並填寫您的 API 認證。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="使用 Journey Optimizer 設定您的 SMS/MMS 服務提供者"
>abstract="在傳送文字簡訊 (SMS/MMS) 之前，您必須將提供者設定和 Journey Optimizer 整合。完成後，您將需要建立一個 SMS/MMS 表面。這些步驟必須由 Adobe Journey Optimizer 系統管理員執行。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/sms/configure-sms/sms-configuration-surface" text="建立簡訊管道表面"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="選取簡訊供應商設定"
>abstract="選取為您的簡訊供應商設定的 API 憑證。"

傳送SMS或MMS之前，您必須設定Adobe Journey Optimizer環境。 若要執行此動作：

1. 整合提供者設定與Journey Optimizer：
   * [與Sinch](sms-configuration-sinch.md)
   * [使用Infobip](sms-configuration-infobip.md)
   * [使用自訂提供者](sms-configuration-custom.md)
1. [建立簡訊表面](sms-configuration-surface.md)

這些步驟必須由Adobe Journey Optimizer [系統管理員](../start/path/administrator.md)執行。

## 先決條件{#sms-prerequisites}

Adobe Journey Optimizer目前與獨立於Adobe Journey Optimizer提供文字訊息服務的第三方提供者整合。 支援的文字訊息及MMS提供者為： **Sinch**、**Twilio**&#x200B;和&#x200B;**Infobip**。

在設定SMS通道之前，您必須與其中一個提供者建立帳戶，以取得您的&#x200B;**API Token**&#x200B;和&#x200B;**服務ID**，您需要這些帳戶來設定Adobe Journey Optimizer與適用提供者之間的連線。

您對簡訊和MMS服務的使用受適用提供者的其他條款與條件的約束。 作為協力廠商解決方案，Adobe Journey Optimizer使用者可透過整合使用Sinch、Twilio和Infobip。 Adobe不會控制，且對協力廠商產品不負任何責任。 如有任何與簡訊服務(SMS/MMS)相關的問題或尋求協助的請求，請聯絡您的提供者。

>[!CAUTION]
>
>若要存取及編輯SMS子網域，您必須對生產沙箱具有&#x200B;**[!UICONTROL 管理SMS子網域]**&#x200B;許可權。 在[本頁面](../administration/high-low-permissions.md#administration-permissions)中深入了解權限。
>

