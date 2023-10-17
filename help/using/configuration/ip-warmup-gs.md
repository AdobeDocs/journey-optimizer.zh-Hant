---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 IP 暖身計劃
description: 了解如何實施 IP 暖身計劃
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: IP, 傳遞能力
hide: true
hidefromtoc: true
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: 82c189545ab4f37a2e4b1044c0b8cfeb539aed13
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 100%

---

# 開始使用 IP 暖身計劃 {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

本文件指南提供以下內容：

* **[開始使用 IP 暖身](ip-warmup-gs.md)**
* [建立 IP 暖身行銷活動](ip-warmup-campaign.md)
* [建立 IP 暖身計劃](ip-warmup-plan.md)
* [執行 IP 暖身計劃](ip-warmup-execution.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>IP 暖身功能目前僅作為 Beta 版提供給部分使用者。若要加入 Beta 版計畫，請連絡 Adobe 客戶服務。

透過 [!DNL Journey Optimizer]，您可以按照標準化、有效率的方式，依照最佳傳遞能力的最佳實務進行，直接從使用者介面輕鬆執行 IP 暖身工作流程。

>[!CAUTION]
>
>此功能僅適用於電子郵件頻道。

使用新平台傳送電子郵件時，網際網路服務提供商 (ISP) 會懷疑無法辨識的 IP 位址。 如果突然傳送大量電子郵件，ISP 通常會將其標記為垃圾郵件。

為避免遭標記為垃圾郵件，您可以使用 IP 暖身計劃功能逐步增加傳送量。 這項新選項位於&#x200B;**[!UICONTROL 管理]**&#x200B;功能表，可讓您以整合的方式更輕鬆地操作，而不是建立複雜的每日歷程。 這應該可以確保順利開發暖身階段，並讓您降低整體的無效位址率。

>[!NOTE]
>
>請在[傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hant)中了解更多透過 IP 暖身功能提高電子郵件聲譽。

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

實施 IP 暖身計劃的重要步驟如下：

1. 您必須先建立一或多個啟用 IP 暖身選項的行銷活動。 [了解更多](ip-warmup-campaign.md)

1. 在 [!DNL Journey Optimizer] 中建立 IP 暖身計劃，然後在傳遞能力顧問的協助下上傳備妥的 Excel 工作表。 [了解更多](ip-warmup-plan.md)

1. 為計劃的每個階段選取行銷活動，然後啟用對應的執行。 [了解更多](ip-warmup-execution.md)
