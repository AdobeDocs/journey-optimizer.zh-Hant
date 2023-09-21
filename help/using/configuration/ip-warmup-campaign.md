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
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '233'
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

您需要建立一或多個已啟用特定選項的促銷活動，以便用於IP熱身計畫。

若要建立IP熱身行銷活動，請遵循下列步驟。

1. 建立 [表面](channel-surfaces.md) 用於您為預熱計畫識別的網域和IP。<!--how do you identify these or who does it at the customer level?-->

1. 建立 [行銷活動](../campaigns/create-campaign.md) 並選取 [電子郵件](../email/create-email.md#create-email-journey-campaign) 動作。

1. 選取您為IP預熱建立的曲面。

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 排程]** 區段，選取 **[!UICONTROL IP熱身計畫啟用]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   行銷活動 [排程](../campaigns/create-campaign.md#schedule) 將由與其相關聯的IP熱身計畫驅動，這表示排程不再於行銷活動本身中定義。

1. [啟動](../campaigns/review-activate-campaign.md) 行銷活動。 一旦上線，就可在IP熱身計畫中使用。

>[!NOTE]
>
>對於已啟用IP熱身計畫的即時行銷活動， **[!UICONTROL 刪除]** 按鈕在與IP熱身計畫關聯之前可以使用。

有關如何設定行銷活動的詳細資訊，請參閱 [此頁面](../campaigns/get-started-with-campaigns.md).

