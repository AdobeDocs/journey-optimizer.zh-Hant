---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 IP 暖身計劃
description: 了解如何實施 IP 暖身計劃
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, 傳遞能力
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 43%

---

# 開始使用 IP 暖身計劃 {#ip-warmup-gs}

透過[!DNL Journey Optimizer]，您可以遵循最佳傳遞能力的最佳實務，以標準化且有效率的方式直接從使用者介面執行IP熱身工作流程。 使用新平台傳送電子郵件時，網際網路服務提供商 (ISP) 會懷疑無法辨識的 IP 位址。 如果突然傳送大量電子郵件，ISP 通常會將其標記為垃圾郵件。

為避免遭標記為垃圾郵件，您可以使用 IP 暖身計劃功能逐步增加傳送量。 **[!UICONTROL 管理]**&#x200B;選單中的這個新選項可讓您自動化磁碟區管理並簡化熱身程式，而不需要複雜的歷程設定。

>[!NOTE]
>
>在實作IP熱身計畫之前，請先在此[IP熱身傳遞指南](ip-warmup-deliverability-guide.md)中瞭解傳遞能力基礎、聲譽建立和最佳實務。

➡️ [在此影片中瞭解如何建立及執行IP熱身計畫](#video)

>[!AVAILABILITY]
>
>此功能只能在生產型別的沙箱上啟用。

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

## 操作說明影片 {#video}

了解如何建立和執行 IP 暖身計劃。

>[!VIDEO](https://video.tv.adobe.com/v/3453851/?captions=chi_hant&learn=on)

>[!NOTE]
>
>在[傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hant)中進一步瞭解透過IP暖身提高您的電子郵件信譽。

## 其他資源 {#additional-resources}

探索這些實用的部落格，以取得有關IP熱身更深入的指引：

* [Adobe Journey Optimizer傳遞能力指南：從零信譽到收件匣英雄](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=zh-Hant) — 涵蓋信譽基礎知識、熱身行事曆、監控和疑難排解最佳實務的全面指南。

* [瞭解如何設定IP熱身](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949?profile.language=zh-Hant) — 瞭解設定IP熱身計畫的基礎和成功實作的最佳實務。

* [&#x200B; IP熱身計畫中的進階功能](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958?profile.language=zh-Hant) — 探索進階功能與精細的控制項，以最佳化IP熱身策略。

* [IP熱身疑難排解](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952?profile.language=zh-Hant) — 尋找對象延遲等常見問題的解決方案，並瞭解智慧重試機制。
