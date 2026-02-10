---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用歷程活動
description: 開始使用歷程活動
feature: Journeys, Activities, Overview
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 歷程，活動，開始，事件，動作
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 15%

---

# 開始使用歷程活動 {#about-journey-activities}

結合事件、協調和動作活動，以建立多步驟、跨管道的情境。

## 事件活動 {#event-activities}

個人化歷程以線上購買等事件開始。 設定檔進入歷程後，就會自行移動。 每個設定檔可以採用不同的路徑和步調。 當您開始事件時，歷程會在事件到達時觸發。 然後，每個設定檔都會遵循歷程中定義的步驟。

技術使用者設定的事件（請參閱[此頁面](../event/about-events.md)）會出現在浮動視窗的第一個類別中。 此類別位於畫面左側。 可使用下列事件活動：

* [一般事件](../building-journeys/general-events.md)
* [反應](../building-journeys/reaction-events.md)
* [客群鑑定](../building-journeys/audience-qualification-events.md)

![歷程設計器中的事件活動浮動視窗](assets/journey43.png)

若要開始您的歷程，請拖放事件活動。 您也可以連按兩下它。

![在歷程設計器中拖放事件活動](assets/journey44.png)

## 協調活動 {#orchestration-activities}

協調活動是有助於決定歷程中下一個步驟的條件。 這些條件包括此人是否有未解決的支援案例或完成購買。 此外也可以包含當地天氣預報，或該人士是否達到10,000點忠誠點數。

從浮動視窗的畫面左側，有下列協調活動：

<!--* [Optimize](optimize.md)-->
* [讀取對象](read-audience.md)
* [等待](wait-activity.md)
* [內容決策](content-decision.md)
* [資料集查詢](dataset-lookup.md)

![歷程設計工具中的協調流程活動浮動視窗](assets/journey-orchestration-activities.png)

## 動作活動 {#action-activities}

動作是您因某種觸發因素而想要發生的動作，例如傳送訊息。 這是客戶體驗的歷程片段。

從畫面左側的浮動視窗，在&#x200B;**[!UICONTROL 事件]**&#x200B;和&#x200B;**[!UICONTROL 協調流程]**&#x200B;下方，您可以找到&#x200B;**[!UICONTROL 動作]**&#x200B;類別。 可使用下列動作活動：

* [內建管道動作](../building-journeys/journeys-message.md)
* [自訂動作](../building-journeys/using-custom-actions.md)
* [跳轉](../building-journeys/jump.md)

歷程設計程式中的![動作活動浮動視窗](assets/journey58.png)

這些活動代表不同的可用通訊通道。您可以將其合併，以建立跨管道情境。

您也可以設定傳送訊息的特定動作：

* 如果您使用協力廠商系統來傳送訊息，則可建立特定的自訂動作。 [了解更多](../action/action.md)

* 如果您正在使用[!DNL Adobe Campaign]和[!DNL Adobe Journey Optimizer]，請參閱下列章節：

   * [[!DNL Adobe Journey Optimizer]和 [!DNL Adobe Campaign] v7/v8](../action/acc-action.md)
   * [[!DNL Adobe Journey Optimizer]和 [!DNL Adobe Campaign] 標準](../action/acs-action.md)
   * [[!DNL Adobe Journey Optimizer]和 [!DNL Adobe Marketo Engage]](../action/marketo-engage.md)

## 最佳做法 {#best-practices}

使用這些建議讓歷程可讀取、一致且易於疑難排解。

### 新增標籤

大部分活動可讓您定義&#x200B;**[!UICONTROL 標籤]**。 這會將尾碼新增至畫布中顯示在活動下方的名稱中。 如果您在歷程中多次使用相同的活動，且想要更輕鬆地識別它們，這會很有用。 這樣還可以更輕鬆地在發生錯誤時進行偵錯，並讓報表更易於閱讀。 您也可以新增選用的&#x200B;**[!UICONTROL 描述]**。

![歷程活動屬性中的標籤和說明欄位](assets/journey-action-label.png)

>[!NOTE]
>
>對於某些活動，其ID也會顯示在窗格中。 此ID可作為較標籤穩定的索引鍵用於報表，但標籤可能會變更。

### 管理進階引數 {#advanced-parameters}

大多數活動會顯示許多您無法修改的進階及/或技術引數。

![歷程活動屬性中的進階引數欄位](assets/journey-advanced-parameters.png)

為了更好的可讀性，請使用右窗格上方的&#x200B;**[!UICONTROL 隱藏唯讀欄位]**&#x200B;按鈕來隱藏這些引數。

![隱藏歷程活動屬性中的唯讀欄點陣圖示](assets/journey-hide-read-only-fields.png)

在某些特定內容中，您可以覆寫這些引數的值以供特定用途。 若要強制執行值，請按一下欄位右側的&#x200B;**[!UICONTROL 啟用參數覆寫]**&#x200B;圖示。[了解更多](../configuration/primary-email-addresses.md#override-execution-address-journey)

![在電子郵件活動屬性中啟用引數覆寫選項](assets/journey-enable-parameter-override.png)

>[!NOTE]
>
>如果進階引數已隱藏，請按一下&#x200B;**[!UICONTROL 顯示唯讀欄位]**&#x200B;按鈕
>
>![在歷程活動屬性中顯示唯讀欄點陣圖示](assets/journey-show-read-only-fields.png){width=60%}

### 新增替代路徑

當動作或條件發生錯誤時，個人的歷程就會停止。唯一能讓它繼續的方法是核取方塊&#x200B;**[!UICONTROL 在逾時或錯誤的情況下新增替代路徑]**。 請參閱[本節](../building-journeys/using-the-journey-designer.md#paths)。

![在條件活動屬性中新增替代路徑選項](assets/journey42.png)

## 疑難排解 {#troubleshooting}

在測試和發佈您的歷程之前，請先確認所有活動皆已正確設定。如果系統仍偵測到錯誤，則無法進行測試或發佈。

在此頁面[上瞭解如何疑難排解活動及歷程](troubleshooting.md)中的錯誤。

另請參閱&#x200B;**[監視與疑難排解](../../rp_landing_pages/troubleshoot-journey-landing-page.md)**。
