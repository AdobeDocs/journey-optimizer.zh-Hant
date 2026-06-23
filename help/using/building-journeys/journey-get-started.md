---
solution: Journey Optimizer
product: journey optimizer
title: Journey Orchestration - 完成指南
description: 在 [!DNL Adobe Journey Optimizer]中開始使用歷程協調的完整指南
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
keywords: 歷程，協調，快速入門，入門，功能
exl-id: 96b1d619-986d-493d-a73b-d7c63b92cca8
TQID: https://experienceleague.adobe.com/Ht6fS6uanOs-rXoT4bAnK6eGvm9kOmH-N5B-y8KU6Rc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1602
ht-degree: 29%

---

# Journey Orchestration — 完整指南{#journey-orchestration-guide}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;取得Adobe Journey Optimizer中歷程協調的完整指南，內容包括如何設計、管理和調整即時適應的多步驟、多頻道客戶歷程。

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]中的歷程可讓您建立個人化、多步驟的客戶歷程，這些歷程會即時因應您對象的行為和需求。 使用直覺式拖放版面，您就可以跨多管道，協調訊息和動作，運用內容資料和客群目標定位，發揮最大效果。

無論您是探索即時觸發器、管理歷程屬性，還是使用自訂動作和運算式等進階工具，本指南都提供清晰的藍圖，讓您自信地設計和調整歷程，提供有意義、及時的客戶體驗。

## 什麼是歷程？

使用 [!DNL Journey Optimizer] 可讓您善用儲存在事件或資料來源中的內容相關資料，建立即時協調流程使用案例。 設計多步驟進階情境，即時回應客戶行為和業務事件。

Journey Optimizer 歷程設計工具提供行銷人員和歷程實踐者所需的一切，能夠跨頻道協調多步驟 1:1歷程。 這包括直覺式的拖放畫布，用以協調歷程的每個步驟、定義目標對象，並包含目標對象成員將根據行為、情境資料和業務事件看到的跨頻道訊息、優惠和內容。

![具有調色盤、畫布和屬性面板的歷程設計工具介面](assets/journey38.png)

**準備好開始建置嗎？** 在[此頁面](journey-gs.md)瞭解如何建立及設計您的第一個歷程。


## 主要功能 {#capabilities}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hant)

**即時和批次傳遞**

傳送在收到事件時觸發的即時&#x200B;**單一傳遞**，或使用[!DNL Adobe Experience Platform]對象批次&#x200B;**中的**。

[瞭解歷程登入](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=zh-Hant)

**內容資料**

善用來自事件的&#x200B;**內容資料**、來自[!DNL Adobe Experience Platform]的資訊，或來自協力廠商API服務的資料。

[使用資料來源](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hant)

**內建動作**

使用&#x200B;**內建頻道動作**，透過電子郵件、推播、SMS/RCS/MMS等傳送在[!DNL Journey Optimizer]中設計的訊息。

[可在歷程中傳送訊息](journey-action.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hant)

**自訂動作**

如果您使用協力廠商系統來傳送訊息或連線到外部API，請建立&#x200B;**自訂動作**。

[設定自訂動作](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hant)

**視覺化歷程設計工具**

使用&#x200B;**歷程設計工具**，建置多步驟使用案例：輕鬆拖放進入事件或讀取客群活動、新增條件及傳送個人化訊息。

[探索歷程設計器](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hant)

**可重複使用的歷程片段**

一次建置一組歷程節點（例如資格檢查或管道路由邏輯），並使用&#x200B;**歷程片段**&#x200B;在歷程中重複使用。

[瞭解歷程片段](journey-fragments.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hant)

**測試與最佳化**

發佈前先測試您的歷程、監控其效能，並使用進階功能（例如傳送時間最佳化）最佳化傳送。

[測試並發佈歷程](testing-the-journey.md)
:::

::::

## 使用案例和範例 {#use-cases}

在歷程設計工具中，行銷人員可以在事件發生時，透過任何頻道，傳送即時觸發的 1:1 訊息。 例如，當客戶訂閱服務時，它可以[觸發歡迎電子郵件](message-to-subscribers-uc.md)，鼓勵他們第一次登入應用程式並設定其偏好設定。 完成購買、開啟電子郵件和登入應用程式等操作，可用於推動新客戶完成其歷程。

[歷程設計器](using-the-journey-designer.md)提供[內建頻道動作](journey-action.md)，可支援輸出訊息，例如電子郵件、推播通知和SMS/RCS/MMS，以及輸入頻道，包括行動應用程式、網站和直接在Journey Optimizer中建置的程式碼型體驗。 您也可以使用協力廠商系統來傳送訊息 — Journey Optimizer包含[自訂動作](using-custom-actions.md)，以允許這些系統直接從歷程設計器整合到歷程中。


:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hant)

**透過使用案例學習**

探索全面的端對端歷程使用案例，展示真實世界的實作和最佳作法。

[探索所有使用案例](jo-use-cases.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hant)

**歡迎新的訂閱者**

當客戶訂閱您的服務時，傳送個人化的歡迎歷程，引導他們完成入門步驟。

[了解更多](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=zh-Hant)

**最佳化電子郵件傳送時間**

使用AI支援的傳送時間最佳化，在每個客戶最有可能參與時傳送電子郵件。

[了解更多](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hant)

**加快交付速度**

逐步增加訊息量，以便改善寄件者的信譽，避開傳遞能力問題。

[了解更多](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hant)

**依據工作日鎖定目標**

根據客戶進入您歷程的星期幾傳送不同內容。

[了解更多](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/question.svg?lang=zh-Hant)

**歷程常見問題集**

尋找有關歷程建立、疑難排解和最佳實務的常見問題解答。

[檢視常見問題集](journey-faq.md)
:::

::::



## 學習資源 {#learning-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hant)

**建立和管理歷程**

設計、測試、發佈和追蹤客戶歷程的逐步指南，以建立個人化的全管道行銷活動。

[探索歷程建立](../../rp_landing_pages/create-journey-landing-page.md) | [學習歷程管理](../../rp_landing_pages/manage-journey-landing-page.md) | [歷程工作流程步驟](journey.md#workflow)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hant)

**歷程活動**

探索如何在歷程中設定和使用活動，例如觸發程序、決策步驟、客群管理和個人化訊息。

[探索活動](../../rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hant)

**運算式與條件**

掌握如何使用強大的工具和語法為動態工作流程、資料操控和進階歷程協調建立運算式。

[了解運算式](../../rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=zh-Hant)

**疑難排解和監視**

診斷並解決歷程執行問題，包括工具、錯誤代碼以及偵錯和最佳化的最佳實務。

[疑難排解指南](../../rp_landing_pages/troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hant)

**歷程設計工具總覽**

瞭解歷程畫布、浮動視窗，以及如何使用視覺化介面設計客戶歷程。

[瞭解設計工具](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hant)

**測試與發佈**

發佈歷程之前，請先徹底測試歷程，確保歷程如預期般運作並提供適當的體驗。

[測試指南](testing-the-journey.md)
:::

::::

### 教學課程影片 {#video}

探索歷程的元件，並瞭解在畫布中建立歷程的基本概念。

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

### 其他資源

* **[錯誤碼參考](error-codes-reference.md)** - 歷程錯誤碼和疑難排解步驟
* **[警示](../reports/alerts.md)** - 設定歷程監視的警示
* **[疑難排解](troubleshooting.md)** - 常見歷程問題和解決方案
* **[歷程教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** — 透過實作影片教學課程瞭解如何建立歷程
* **[歷程護欄和限制](../start/guardrails.md)** — 使用[!DNL Adobe Journey Optimizer]時檢查護欄和限制

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此為Adobe Journey Optimizer中歷程協調的全方位快速入門手冊，涵蓋關鍵功能（即時和批次傳送、情境資料、內建和自訂動作、視覺化設計工具、歷程片段和測試）、常見使用案例，以及所有主要學習資源的連結。

**意圖：**
* 在建置第一個歷程之前，先瞭解Journey Optimizer歷程設計器中可用的關鍵功能
* 導覽至建立、管理、測試或疑難排解歷程的正確資源
* 瞭解如何使用歷程設計工具觸發任何管道上的1:1則即時訊息
* 探索歷程片段如何實現跨歷程重複使用通用節點邏輯
* 存取常見歷程使用案例（例如歡迎系列、購物車放棄和傳送時間最佳化）的影片教學課程和逐步指南

**字彙表：**
* **歷程設計器**： Adobe Journey Optimizer中的拖放式視覺畫布可用來建置和協調多步驟客戶歷程&#x200B;*（產品專用）*
* **歷程片段**：一組可重複使用的歷程節點（例如資格檢查、管道路由邏輯），已建置一次並插入多個歷程&#x200B;*（產品專屬）*
* **單一傳遞**：當特定事件發生時，針對單一設定檔觸發的即時訊息&#x200B;*（產品特定）*
* **批次傳送**：一次或依排程&#x200B;*（產品特定）*&#x200B;傳送給Adobe Experience Platform對象中所有設定檔的訊息
* **傳送時間最佳化(STO)**： AI驅動的功能，可預測傳送訊息給每個個別設定檔的最佳時間，以最大化參與度&#x200B;*（產品特定）*
* **自訂動作**：透過API連線至協力廠商系統的歷程活動，以傳送訊息或擷取資料&#x200B;*（產品特定）*

**護欄：**
* 歷程護欄和限制在護欄頁面上分開詳述，並在大規模設計之前檢閱
* 自訂動作必須先由技術使用者設定，才能用於歷程中
* 歷程片段必須先處於作用中狀態，才能將其插入歷程中

**術語：**
* 正式名稱：Journey — 首字母縮寫：none — 變體：customer journey、orchestration flow、multistep journey
* 同義字： &quot;journey designer&quot; = &quot;journey canvas&quot; = &quot;journey builder&quot;
* 請勿混淆：「內建頻道動作」≠「自訂動作」 — 內建動作使用原生AJO頻道；自訂動作呼叫外部第三方API

**常見問題集：**
* **問：在歷程中，即時（單一）傳遞和批次傳遞之間有何差異？**  — 單一傳遞會在事件發生時即時觸發一個設定檔的訊息。 批次傳送會使用讀取對象活動，一次或依排程處理對象中的所有設定檔。
* **問：我可以在多個歷程中重複使用通用邏輯（例如資格檢查）嗎？**  — 是；將節點儲存為歷程片段並將作用中片段插入跨沙箱的任何歷程中。
* **問：我該前往何處建立第一個歷程？**  — 遵循「建立您的第一個歷程」頁面上的逐步指南，逐步說明登入點選擇、畫布設計、測試和發佈。
* **問：如何透過協力廠商系統從歷程傳送訊息？**  — 設定自訂動作以呼叫外部API，然後將其新增為歷程畫布中的動作活動。
* **問：我可以在哪裡找到常見歷程問題的解答？**  — 請造訪歷程常見問題集頁面，瞭解概念、建立、測試、執行、監控和最佳實務等問題的解答。

+++
