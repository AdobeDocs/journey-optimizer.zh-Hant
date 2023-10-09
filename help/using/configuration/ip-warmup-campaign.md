---
solution: Journey Optimizer
product: journey optimizer
title: 建立 IP 暖身行銷活動
description: 瞭解如何建立IP熱身行銷活動
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: IP、集區、傳遞能力
hide: true
hidefromtoc: true
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 21%

---

# 建立 IP 暖身行銷活動 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="啟用 IP 暖身計劃選項"
>abstract="當您選取此選項時，可以在 IP 暖身計劃中使用行銷活動。然後，活動排程將由與其關聯的 IP 暖身計劃驅動。"

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用 IP 暖身](ip-warmup-gs.md)
* **[建立 IP 暖身行銷活動](ip-warmup-campaign.md)**
* [建立 IP 暖身計劃](ip-warmup-plan.md)
* [執行 IP 暖身計劃](ip-warmup-execution.md)

>[!ENDSHADEBOX]

在中建立IP熱身計畫本身之前 [!DNL Journey Optimizer]，您首先需要建立一或多個已啟用專用選項的行銷活動，以便用於IP熱身計畫。

若要建立IP熱身行銷活動，請遵循下列步驟。

1. 建立 [電子郵件](../email/email-settings.md) 頻道 [表面](channel-surfaces.md) 用於您為預熱計畫識別的網域和IP。

   >[!NOTE]
   >
   >瞭解如何選取要在電子郵件表面中使用的網域和IP [本節](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >請與您的傳遞顧問合作，識別要用於IP熱身計畫的網域和IP。<!--TBC-->

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
   >對於已啟用IP熱身計畫的即時行銷活動， **[!UICONTROL 刪除]** 按鈕在與IP熱身計畫關聯之前可以使用。 行銷活動在計畫中使用後，即無法再刪除。

1. 行銷活動會顯示在中 **[!UICONTROL 行銷活動]** 清單。 若要輕鬆擷取在目前沙箱中建立的所有IP熱身行銷活動，您可以篩選 **[!UICONTROL IP熱身]** 行銷活動選項。

   ![](assets/ip-warmup-campaign-filter.png)

行銷活動上線後，即準備好用於IP熱身計畫。 [了解更多](ip-warmup-plan.md)

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->
