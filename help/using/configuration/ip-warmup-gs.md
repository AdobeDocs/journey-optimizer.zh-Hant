---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用IP熱身計畫
description: 瞭解如何實作IP熱身計畫
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、集區、群組、子網域、傳遞能力
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 7%

---

# 開始使用IP熱身計畫 {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* **[開始使用IP熱身](ip-warmup-gs.md)**
* [建立IP熱身行銷活動](ip-warmup-campaign.md)
* [建立IP熱身計畫](ip-warmup-plan.md)
* [執行IP熱身計畫](ip-warmup-running.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>IP熱身功能目前僅供特定使用者測試使用。 若要加入測試版計畫，請連絡 Adobe 客戶服務。

替換為 [!DNL Journey Optimizer]，您可以遵循最佳傳遞能力的最佳實務，以標準化且有效率的方式直接從使用者介面執行IP熱身工作流程。

>[!CAUTION]
>
>此功能僅適用於電子郵件頻道。

使用新平台傳送電子郵件時，網際網路服務提供者(ISP)會懷疑無法辨識的IP位址。 如果突然傳送大量電子郵件，ISP通常會將其標籤為垃圾郵件。

為避免被標籤為垃圾訊息，您可以使用IP熱身計畫功能逐步增加傳送量。 中的新選項 **[!UICONTROL 管理]** 功能表可讓您更順利地執行，而不是建立複雜的每日歷程。 這應該可以確保啟動階段的順利發展，並且讓您降低無效的位址的整體比率。

>[!NOTE]
>
>進一步瞭解透過IP暖身提高您的電子郵件信譽 [傳遞性最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

實施IP熱身計畫的關鍵步驟如下：

1. 您必須先建立一或多個啟用IP熱身選項的促銷活動。 [了解更多](ip-warmup-campaign.md) <!--this is usually done by a marketer persona??)-->

1. 建立IP熱身計畫並上傳您的計畫。 [了解更多](ip-warmup-plan.md) <!--this is usually done by a deliverability consultant??-->

1. 調整計畫的每個階段並啟動執行。 [了解更多](ip-warmup-running.md)
