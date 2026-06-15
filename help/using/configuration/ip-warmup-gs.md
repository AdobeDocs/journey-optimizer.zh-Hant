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
TQID: https://experienceleague.adobe.com/xjJKrCXUmQY5sZu2w-B09agQh-tb4qkSXM0Vh2-TDnc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c343082f-e963-4f57-a96b-b64d27f8118e
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 489
ht-degree: 35%

---

# 開始使用 IP 暖身計劃 {#ip-warmup-gs}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解IP熱身計畫如何協助您逐步增加傳送量，以建立寄件者信譽，並探索在Adobe Journey Optimizer中實作的重要步驟。

>[!ENDSHADEBOX]

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

## 作法影片 {#video}

了解如何建立和執行 IP 暖身計劃。

>[!VIDEO](https://video.tv.adobe.com/v/3453851/?captions=chi_hant&learn=on)

>[!NOTE]
>
>在[傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hant)中進一步瞭解透過IP暖身提高您的電子郵件信譽。

## 其他資源 {#additional-resources}

探索這些實用的部落格，以取得有關IP熱身更深入的指引：

* [Adobe Journey Optimizer傳遞能力指南：從零信譽到收件匣英雄](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950) — 涵蓋信譽基礎知識、熱身行事曆、監控和疑難排解最佳實務的全面指南。

* [瞭解如何設定IP熱身](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949) — 瞭解設定IP熱身計畫的基礎和成功實作的最佳實務。

* [&#x200B; IP熱身計畫中的進階功能](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958) — 探索進階功能與精細的控制項，以最佳化IP熱身策略。

* [IP熱身疑難排解](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952) — 尋找對象延遲等常見問題的解決方案，並瞭解智慧重試機制。
