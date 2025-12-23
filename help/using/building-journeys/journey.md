---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用歷程
description: 開始使用歷程
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 歷程, 探索, 開始
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
version: Journey Orchestration
source-git-commit: 7c47940713484dd6d6047eefe6e0ae0d0a276b9c
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 62%

---


# 開始使用歷程{#jo-general-principle}

Adobe Journey Optimizer 中的歷程可讓您建立個人化的多步驟客戶歷程，並即時因應客群的行為和需求。使用直覺式的拖放畫布，您可以跨多個管道協調訊息和動作，運用內容資料和客群目標定位發揮最大影響。無論您是探索即時觸發器、管理歷程屬性，還是使用自訂動作和運算式等進階工具，本節提供清楚的藍圖，協助您設計和調整歷程，以提供有意義、及時的客戶體驗。

使用 [!DNL Journey Optimizer] 可讓您善用儲存在事件或資料來源中的內容相關資料，建立即時協調流程使用案例。您可以設計具有下列功能的多步驟進階案例：

* 傳送在收到&#x200B;**事件**&#x200B;時觸發的即時[單一傳遞](general-events.md)，或使用Adobe Experience Platform **對象**&#x200B;批次的[傳遞](read-audience.md)。

* 透過&#x200B;**資料來源**，善用來自[事件](../event/about-events.md)的[內容資料](../datasource/about-data-sources.md)、來自Adobe Experience Platform的資訊，或來自協力廠商API服務的資料。

* 請使用&#x200B;**[內建動作](journeys-message.md)**&#x200B;傳送在 [!DNL Journey Optimizer] 中設計的訊息，如果您使用第三方系統來傳送訊息，則建立&#x200B;**[自訂動作](using-custom-actions.md)**。

* 使用&#x200B;**[歷程設計器](using-the-journey-designer.md)**，建置您的多步驟使用案例：輕鬆拖放進入事件或[讀取對象活動](read-audience.md)、新增[條件](condition-activity.md)並傳送個人化訊息。

Journey Optimizer [歷程設計器](using-the-journey-designer.md)提供行銷人員和歷程從業人員跨管道協調多步驟1:1歷程所需的一切。 這包括直覺式的拖放畫布，以協調歷程的每個步驟、定義目標對象，並包含目標對象成員將根據行為、情境資料和業務事件看到的跨管道訊息、選件和內容。 探索[真實的使用案例](jo-use-cases.md)，瞭解如何套用這些功能。

➡️ [在影片中探索 Journey Optimizer](#video)

## 歷程概觀

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hant)

開始建立歷程

設計、測試、發佈和追蹤客戶歷程的逐步指南，以建立個人化的全管道行銷活動。

[建立您的第一個歷程](journey-gs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hant)

Journey Orchestration — 完整指南

涵蓋Adobe Journey Optimizer中歷程建立、管理和最佳化各個層面的完整檔案。

[探索完整的指南](journey-get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hant)

管理您的歷程

使用篩選、輪廓管理、時區和最佳化技術的工具，有效管理客戶歷程。

[了解歷程管理](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hant)

歷程活動

探索如何在歷程中設定和使用活動，例如觸發程序、決策步驟、客群管理和個人化訊息。

[探索活動](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hant)

建立運算式

掌握如何使用強大的工具和語法為動態工作流程、資料操控和進階歷程協調建立運算式。

[了解運算式](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hant)

歷程使用案例

探索 Adobe Journey Optimizer 的真實使用案例，包括多管道傳訊以及與外部系統的整合。

[探索使用案例](/help/rp_landing_pages/journey-use-cases-landing-page.md)
:::

::::

## 使用案例{#uc-journey}

在歷程設計工具中，行銷人員可以在事件發生時，透過任何頻道，傳送即時觸發的 1:1 訊息。 例如，當客戶訂閱服務時，它可以[觸發歡迎電子郵件](message-to-subscribers-uc.md)，鼓勵他們第一次登入應用程式並設定其偏好設定。 完成購買、開啟電子郵件和登入應用程式等操作，可用於推動新客戶完成其歷程。

[歷程設計器](using-the-journey-designer.md)提供[內建頻道操作](journeys-message.md)，可支援輸出訊息，例如電子郵件、推播通知和 SMS/MMS，以及傳入頻道，包括行動應用程式、網站和直接在 Journey Optimizer 建立的程式碼型體驗。 您也可以使用第三方系統來傳送訊息 (不論是透過電子郵件、文字或其他管道)，Journey Optimizer 包含[自訂動作](using-custom-actions.md)，以允許這些系統直接從歷程設計器整合到歷程中。

瞭解如何在下列[端到端使用案例](jo-use-cases.md)中建立歷程。

>[!NOTE]
>
>更多有關歷程護欄與限制的資訊可參閱[此頁面](../start/guardrails.md)

## 作法影片 {#video}

探索歷程的元件，並瞭解在畫布中建立歷程的基本概念。

>[!VIDEO](https://video.tv.adobe.com/v/3430349?captions=chi_hant&quality=12)

## 其他資源 {#additional-resources}

* **[客戶歷程疑難排解](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** — 診斷並解決工具、錯誤碼以及偵錯和最佳化最佳化最佳做法的歷程執行問題
* **[歷程常見問題集](journey-faq.md)** - 關於歷程的常見問題
* **[歷程警示](../reports/alerts.md)** — 設定歷程監控的警示，並訂閱即時更新的通知
* **[錯誤碼參考](error-codes-reference.md)** - 歷程錯誤碼和疑難排解步驟
* **[疑難排解](troubleshooting.md)** - 常見歷程問題和解決方案
* **[歷程教學課程（影片）](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** — 透過涵蓋功能、功能和最佳實務的實作教學課程影片，瞭解如何建立歷程
