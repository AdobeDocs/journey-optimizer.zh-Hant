---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用電子郵件設定
description: 深入了解  [!DNL Journey Optimizer] 中的電子郵件組態
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: 電子郵件、設定、表面、子網域
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: bd5e5e501d557e11fb0c1c71a0f9289f39601348
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 100%

---

# 開始使用電子郵件設定 {#get-starte-email-config}

為了能夠在 [!DNL Journey Optimizer] 透過歷程與行銷活動傳送電子郵件，您必須執行許多設定步驟。

1. 若要確保最佳傳遞能力並保護您的聲譽，首先將要用於傳送 [!DNL Journey Optimizer] 電子郵件的子網域委派給 Adobe。這些子網域將決定要追蹤的網頁和鏡像頁面 URL 等元素。 [了解更多](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. 將與您執行個體佈建的 IP 位址分組，以改善電子郵件傳遞能力和信譽。[了解更多](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. 建立通道表面並選取&#x200B;**[!UICONTROL 電子郵件]**&#x200B;通道。 [了解更多](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. 在每個電子郵件通道表面，設定傳送電子郵件所需的所有技術參數。 [了解更多](email-settings.md)

   * 可在此處選取要用於傳送電子郵件的子網域，以及要與表面關聯的 IP 集區。[了解更多](email-settings.md#subdomains-and-ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * 此&#x200B;**[!UICONTROL 寄件者電子郵件]**&#x200B;和&#x200B;**[!UICONTROL 錯誤電子郵件]**&#x200B;地址必須使用目前選定的委派子網域。 [了解更多](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. 在 Adobe Experience Platform 有多個地址可用時，確定收件者優先使用的電子郵件地址。[了解更多](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. 管理將電子郵件地址傳送至禁止名單前執行重試的天數。[了解更多](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
