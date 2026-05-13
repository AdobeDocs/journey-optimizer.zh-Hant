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
TQID: https://experienceleague.adobe.com/mVdk2WGb0rL06j1cmNEh4fj0JC-hwuro8ku-0Yv02N8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: fae48155-b23f-40d2-a252-a25bce350b4d
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 84%

---

# 開始使用電子郵件設定 {#get-starte-email-config}

為了能夠在 [!DNL Journey Optimizer] 透過歷程與行銷活動傳送電子郵件，您必須執行許多設定步驟。

1. 若要確保最佳傳遞能力並保護您的聲譽，首先將要用於傳送 [!DNL Journey Optimizer] 電子郵件的&#x200B;**子網域委派給 Adobe**。 這些子網域將決定要追蹤的網頁和鏡像頁面 URL 等元素。 [了解更多](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. 建立 IP 集區，將使用執行個體佈建的 **IP 位址分組**。 [了解更多](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. 建立&#x200B;**管道設定**，然後選取&#x200B;**[!UICONTROL 電子郵件]**&#x200B;管道。 [了解更多](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. 在每個電子郵件管道設定中，設定傳送電子郵件所需的所有&#x200B;**技術參數**。 [了解更多](email-settings.md)

   * 可在此處選取要用於傳送電子郵件的子網域，以及要與設定關聯的 IP 集區。 [了解更多](email-settings.md#ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * **[!UICONTROL 來自電子郵件前置詞]**&#x200B;和&#x200B;**[!UICONTROL 錯誤電子郵件前置詞]**&#x200B;使用目前選取的[委派子網域](../configuration/about-subdomain-delegation.md)。 可選擇地，**[!UICONTROL 寄件者名稱]**&#x200B;和&#x200B;**[!UICONTROL 寄件者電子郵件]**&#x200B;可識別不同的傳輸合作對象（完整的&#x200B;**寄件者**&#x200B;位址，未繫結至該子網域尾碼）。 [了解更多](header-parameters.md#sender-header)

   ![](assets/preset-header.png)

1. 在 Adobe Experience Platform 有多個地址可用時，確定收件者優先使用的&#x200B;**執行欄位**。 [了解更多](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. 管理將電子郵件地址傳送至禁止名單前執行&#x200B;**重試**&#x200B;的天數。 [了解更多](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
