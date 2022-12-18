---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用電子郵件設定
description: 進一步了解中的電子郵件設定 [!DNL Journey Optimizer]
role: Admin
level: Intermediate
feature: Application Settings
topic: Administration
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 21%

---

# 開始使用電子郵件設定 {#get-starte-email-config}

若要透過歷程和行銷活動傳送電子郵件，請在 [!DNL Journey Optimizer]，您必須執行許多設定步驟。

1. 若要確保最佳傳遞能力並保護您的聲譽，請從委派以Adobe您要用來傳送電子郵件的子網域開始 [!DNL Journey Optimizer]. 這些子網域將決定要追蹤的網頁和鏡像頁面URL等元素。 [了解更多](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. 將與您執行個體布建的IP位址分組，以改善電子郵件傳遞能力和信譽。 [了解更多](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. 建立通道曲面並選取 **[!UICONTROL 電子郵件]** 頻道。 [了解更多](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. 在每個電子郵件通道表面中，設定傳送電子郵件所需的所有技術參數。 [了解更多](email-settings.md)

   * 在此處，選擇要用於發送電子郵件的子網域，以及要與表面關聯的IP池。 [了解更多](email-settings.md#subdomains-and-ip-pools)

   ![](assets/preset-subdomain-ip-pool.png)

   * 此 **[!UICONTROL 寄件者電子郵件]** 和 **[!UICONTROL 錯誤電子郵件]** 地址必須使用當前選定的委派子域。 [了解更多](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. 在Adobe Experience Platform中有數個地址可用時，決定要優先使用給收件者的電子郵件地址。 [了解更多](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. 管理將電子郵件地址傳送至隱藏清單前執行重試的天數。[了解更多](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
