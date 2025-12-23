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
source-git-commit: a6c80e4326454868d60e9ba335e509f806d3220f
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 38%

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

## 歷程型別

Adobe Journey Optimizer支援四種歷程型別，每種都針對不同的使用案例和進入機制而設計。 根據您想要設定檔輸入的方式選擇正確的型別，並逐步完成客戶體驗。

>[!BEGINTABS]

>[!TAB 單一歷程]

**單一歷程**&#x200B;會在特定動作發生時（例如購買、應用程式登入或表單提交），由事件個別觸發。 個人檔案在收到事件時即時進入歷程，一次進入一個，因此非常適合個人化、行為導向的體驗。

**主要特性：**

* 即時、事件導向輸入
* 個別設定檔處理中
* 最適合異動訊息和立即回應
* 支援來自觸發事件的內容資料

**使用案例：**

* 購買後的訂單確認
* 有人訂閱時歡迎電子郵件
* 瀏覽行為所觸發的購物車放棄率
* 密碼重設通知

➡️ [瞭解事件設定](../event/about-events.md) | [一般事件](general-events.md) | [傳送訊息給訂閱者使用案例](message-to-subscribers-uc.md)

>[!TAB 讀取對象歷程]

**讀取對象歷程**&#x200B;從Adobe Experience Platform中的對象開始，並批次傳送訊息給該對象中的所有設定檔。 此歷程型別會一次處理整個對象，非常適合用於排程行銷活動和週期性通訊。

**主要特性：**

* 批次處理對象區段
* 已排程或一次性執行
* 所有設定檔同時輸入
* 支援大規模通訊

**使用案例：**

* 每月電子報
* 目標區段的促銷活動
* 向所有客戶發佈產品
* 季節性行銷活動

➡️ [瞭解閱讀對象活動](read-audience.md) | [開始使用對象](../audience/about-audiences.md) | [多頻道傳訊使用案例](journeys-uc.md)

>[!TAB 對象資格歷程]

**當設定檔符合（或退出）特定對象區段資格時，就會觸發**&#x200B;對象資格歷程。 設定檔會即時符合對象條件，因此可個別進入歷程，當客戶行為變更時可立即參與。

**主要特性：**

* 以資格為基礎的即時輸入
* 持續監控對象會籍
* 符合資格的個別設定檔處理
* 串流受眾體驗最佳

**使用案例：**

* VIP層級升級通知
* 客戶非作用中時重新參與
* 首次購買慶祝訊息
* 客戶移動時的地理目標定位

➡️ [瞭解對象資格](audience-qualification-events.md) | [條件活動](condition-activity.md) | [正在建立區段定義](../audience/creating-a-segment-definition.md)

>[!TAB 商務活動歷程]

**業務事件歷程**&#x200B;是由同時影響多個設定檔的業務事件（例如庫存更新、天氣警報或價格變更）觸發。 這些歷程不會因應個別客戶行動，而是因應更廣泛的業務環境或外部因素。

**主要特性：**

* 由業務層級事件觸發，而非個別動作
* 一次影響多個設定檔
* 事件發生時鎖定特定對象
* 結合事件導向計時與受眾目標定位

**使用案例：**

* 向感興趣的客戶發出低詳細目錄警示
* 快閃銷售公告
* 天氣型促銷活動
* 價格下降通知
* 產品補貨警報

➡️ [瞭解業務活動](general-events.md) | [設定業務事件](../event/about-creating-business.md) | [專案管理](entry-management.md)

>[!ENDTABS]

## 歷程概觀

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

開始建立歷程

設計、測試、發佈和追蹤客戶歷程的逐步指南，以建立個人化的全管道行銷活動。

[建立您的第一個歷程](journey-gs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Journey Orchestration — 完整指南

涵蓋Adobe Journey Optimizer中歷程建立、管理和最佳化各個層面的完整檔案。

[探索完整的指南](journey-get-started.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

管理您的歷程

使用篩選、輪廓管理、時區和最佳化技術的工具，有效管理客戶歷程。

[了解歷程管理](/help/rp_landing_pages/manage-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

歷程活動

探索如何在歷程中設定和使用活動，例如觸發程序、決策步驟、客群管理和個人化訊息。

[探索活動](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

建立運算式

掌握如何使用強大的工具和語法為動態工作流程、資料操控和進階歷程協調建立運算式。

[了解運算式](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

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

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

## 其他資源 {#additional-resources}

* **[客戶歷程疑難排解](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)** — 診斷並解決工具、錯誤碼以及偵錯和最佳化最佳化最佳做法的歷程執行問題
* **[歷程常見問題集](journey-faq.md)** - 關於歷程的常見問題
* **[歷程警示](../reports/alerts.md)** — 設定歷程監控的警示，並訂閱即時更新的通知
* **[錯誤碼參考](error-codes-reference.md)** - 歷程錯誤碼和疑難排解步驟
* **[疑難排解](troubleshooting.md)** - 常見歷程問題和解決方案
* **[歷程教學課程（影片）](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** — 透過涵蓋功能、功能和最佳實務的實作教學課程影片，瞭解如何建立歷程
