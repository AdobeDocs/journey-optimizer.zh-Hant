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
source-git-commit: 9562a194244e2a3323680d98cc8aa5ed65d93a67
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 8%

---

# 開始使用歷程活動 {#about-journey-activities}

結合不同的事件、協調和動作活動，以建置您的多步驟跨管道情境。

## 事件活動 {#event-activities}

個人化歷程由事件觸發，例如線上購買。 設定檔進入歷程後，就會以個人身分移過，而且不會有兩個人以相同速度或沿著相同路徑移動。 當您使用事件開始您的歷程時，歷程會在收到事件時觸發。 接著，歷程中的每個人都個別遵循歷程中定義的後續步驟。

技術使用者設定的事件(請參閱 [此頁面](../event/about-events.md))都會顯示在畫面左側的浮動視窗第一個類別中。 可使用下列事件活動：

* [一般事件](../building-journeys/general-events.md)
* [反應](../building-journeys/reaction-events.md)
* [對象資格](../building-journeys/audience-qualification-events.md)

![](assets/journey43.png)

透過拖放事件活動來開始您的歷程。 您也可以連按兩下它。

![](assets/journey44.png)

## 協調活動 {#orchestration-activities}

協調活動是不同的條件，可協助判斷歷程的下一步。 可能是此人是否擁有未解決的支援案例、目前地點的天氣預報、是否完成購買或達到10,000點忠誠點數。

從浮動視窗的畫面左側，有下列協調活動：

* [條件](../building-journeys/condition-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [讀取對象](../building-journeys/read-audience.md)

![](assets/journey49.png)

## 動作活動 {#action-activities}

動作是您因某種觸發而想要發生的動作，例如傳送訊息。 這是客戶體驗的歷程。

從浮動視窗的畫面左側下方 **[!UICONTROL 活動]** 和 **[!UICONTROL 協調流程]**，您可以找到 **[!UICONTROL 動作]** 類別。 可使用下列動作活動：

* [電子郵件、簡訊、推播](../building-journeys/journeys-message.md)
* [自訂動作](../building-journeys/using-custom-actions.md)
* [跳轉](../building-journeys/jump.md)

![](assets/journey58.png)

這些活動代表不同的可用通訊通道。 您可以將其合併，以建立跨管道情境。

如果您已設定自訂動作，它們也會顯示在這裡。 [瞭解更多](../building-journeys/using-custom-actions.md))。

## 最佳作法 {#best-practices}

### 新增標籤

大部分活動都可讓您定義 **[!UICONTROL 標籤]**. 這會將尾碼新增至畫布中顯示在活動下方的名稱中。 如果您在歷程中多次使用相同的活動，且想要更輕鬆地識別它們，這會很有用。 它也會讓發生錯誤時的偵錯更容易，並讓報告更易於閱讀。 您也可以新增選用的 **[!UICONTROL 說明]**.

![](assets/journey-action-label.png)

>[!NOTE]
>
>對於某些活動，其ID也會顯示在窗格中。 此ID可作為較標籤穩定的索引鍵用於報表，但標籤可能會變更。

### 管理進階引數 {#advanced-parameters}

大多數活動會顯示許多您無法修改的進階及/或技術引數。

![](assets/journey-advanced-parameters.png)

為了提高可讀性，您可以使用 **[!UICONTROL 隱藏唯讀欄位]** 按鈕。

![](assets/journey-hide-read-only-fields.png)

在某些特定內容中，您可以覆寫這些引數的值以供特定用途。 若要強制執行值，請按一下欄位右側的&#x200B;**[!UICONTROL 啟用參數覆寫]**&#x200B;圖示。[了解更多](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### 新增替代路徑

當動作或條件發生錯誤時，個人的歷程就會停止。 唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL 在逾時或錯誤的情況下新增替代路徑]**. 另請參閱 [本節](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
