---
solution: Journey Optimizer
product: journey optimizer
title: 建立IP熱身行銷活動
description: 瞭解如何建立IP熱身行銷活動
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、集區、群組、子網域、傳遞能力
hide: true
hidefromtoc: true
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 3%

---

# 建立IP熱身行銷活動 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="啟動IP熱身計畫選項"
>abstract="選取IP熱身計畫啟用選項。 行銷活動上線後，即可與IP熱身計畫建立關聯。"

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用IP熱身](ip-warmup-gs.md)
* **[建立IP熱身行銷活動](ip-warmup-campaign.md)**
* [建立IP熱身計畫](ip-warmup-plan.md)
* [執行IP熱身計畫](ip-warmup-running.md)

>[!ENDSHADEBOX]

在中建立IP熱身計畫本身之前 [!DNL Journey Optimizer]，您首先需要建立一或多個已啟用專用選項的行銷活動，以便用於IP熱身計畫。

若要建立IP熱身行銷活動，請遵循下列步驟。

1. 建立 [電子郵件](../email/email-settings.md) 頻道 [表面](channel-surfaces.md) 用於您為預熱計畫識別的網域和IP。

   >[!NOTE]
   >
   >瞭解如何選取要在電子郵件表面中使用的網域和IP [本節](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >如有需要，請與您的傳遞顧問合作，找出要用於IP熱身計畫的網域和IP。<!--TBC-->

1. 建立 [行銷活動](../campaigns/create-campaign.md) 並選取 [電子郵件](../email/create-email.md#create-email-journey-campaign) 動作。

1. 選取您為IP預熱建立的曲面。

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 排程]** 區段，選取 **[!UICONTROL IP熱身計畫啟用]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   行銷活動 [排程](../campaigns/create-campaign.md#schedule) 將由與其相關聯的IP熱身計畫驅動，這表示促銷活動本身不再定義排程。

1. 完成步驟以建立電子郵件行銷活動，例如定義行銷活動屬性 [對象](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->、和 [內容](../email/get-started-email-design.md#key-steps).

   >[!NOTE]
   >
   >有關如何設定行銷活動的詳細資訊，請參閱 [此頁面](../campaigns/get-started-with-campaigns.md).

1. [啟動](../campaigns/review-activate-campaign.md) 行銷活動。

   >[!NOTE]
   >
   >對於已啟用IP熱身計畫的即時行銷活動， **[!UICONTROL 刪除]** 按鈕在與IP熱身計畫關聯之前可以使用。 此行銷活動一旦用於IP熱身計畫中，便無法再刪除。

1. 行銷活動會顯示在中 **[!UICONTROL 行銷活動]** 清單。 若要輕鬆擷取在目前沙箱中建立的所有IP熱身行銷活動，您可以對行銷活動選項進行篩選 **[!UICONTROL IP熱身]**.

   ![](assets/ip-warmup-campaign-filter.png)

行銷活動上線後，即準備好用於IP熱身計畫。 [了解更多](ip-warmup-plan.md)

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

