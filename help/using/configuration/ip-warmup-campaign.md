---
solution: Journey Optimizer
product: journey optimizer
title: 建立 IP 暖身行銷活動
description: 瞭解如何建立IP熱身行銷活動
feature: Campaigns, IP Warmup Plans
topic: Administration
role: Admin
level: Intermediate
keywords: IP、集區、傳遞能力
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: 9d48213d8367fdc6c0fae62b73d1706bc4983d9d
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 16%

---

# 建立 IP 暖身行銷活動 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="啟用 IP 暖身計劃選項"
>abstract="當您選取此選項時，可以在 IP 暖身計劃中使用行銷活動。然後，活動排程將由與其關聯的 IP 暖身計劃驅動。"

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用IP熱身](ip-warmup-gs.md)
* **[建立IP熱身行銷活動](ip-warmup-campaign.md)**
* [建立 IP 暖身計劃](ip-warmup-plan.md)
* [執行 IP 暖身計劃](ip-warmup-execution.md)

>[!ENDSHADEBOX]

在中建立IP熱身計畫本身之前 [!DNL Journey Optimizer]，您首先需要建立一個或多個專門設計用於IP熱身計畫的行銷活動<!--through a dedicated option-->.

若要建立IP熱身行銷活動，請遵循下列步驟。

1. 建立 [電子郵件](../email/email-settings.md) 頻道 [表面](channel-surfaces.md) 用於您為預熱計畫識別的網域和IP。

   >[!NOTE]
   >
   >瞭解如何選取要在電子郵件表面中使用的網域和IP [本節](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >請與您的傳遞顧問合作，識別要用於IP熱身計畫的網域和IP。<!--TBC-->

1. 建立排程行銷 [行銷活動](../campaigns/create-campaign.md) 並選取 [電子郵件](../email/create-email.md#create-email-journey-campaign) 動作。

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

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

1. [啟動](../campaigns/review-activate-campaign.md) 行銷活動。 其狀態變更為 **[!UICONTROL 即時]**.

   >[!NOTE]
   >
   >對於已啟用IP熱身計畫的即時行銷活動， **[!UICONTROL 刪除]** 按鈕在與IP熱身計畫關聯之前可以使用。 行銷活動在計畫中使用後，即無法再刪除。

1. 行銷活動會顯示在中 **[!UICONTROL 行銷活動]** 清單。 若要輕鬆擷取在目前沙箱中建立的所有IP熱身行銷活動，您可以篩選 **[!UICONTROL IP熱身]** 行銷活動選項。

   ![](assets/ip-warmup-campaign-filter.png)

行銷活動上線後，即準備好用於IP熱身計畫。 [了解更多](ip-warmup-plan.md)

IP熱身行銷活動只能用於一個IP熱身計畫。 不過，同一IP熱身計畫的一個或多個階段中可以使用相同的行銷活動。 [了解更多](ip-warmup-plan.md#define-phases)

>[!NOTE]
>
>當在IP熱身計畫中使用即時行銷活動時，在計畫之後 [標示為已完成](ip-warmup-execution.md#mark-as-completed)，該促銷活動的狀態會變更為 **[!UICONTROL 已停止]**.

