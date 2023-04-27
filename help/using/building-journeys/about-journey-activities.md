---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用歷程活動
description: 開始使用歷程活動
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，活動，快速入門，事件，動作
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 18%

---

# 開始使用歷程活動 {#about-journey-activities}

結合不同的事件、協調和動作活動，以建立您的多步驟跨管道情境。

## 事件活動 {#event-activities}

事件是觸發個人化歷程（例如線上購買）的因素。 一旦有人進入歷程，他們就會以個人身份移動，沒有兩個人會以相同的速度或相同的路徑移動。 當您從事件開始歷程時，會在收到事件時觸發歷程。 歷程中的每個人接著分別依照歷程中定義的後續步驟操作。

由技術使用者設定的事件(請參閱 [本頁](../event/about-events.md))會顯示在浮動視窗的第一個類別中，位於畫面左側。 可使用下列事件活動：

* [一般事件](../building-journeys/general-events.md)
* [反應](../building-journeys/reaction-events.md)
* [區段資格](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

拖放事件活動，以開始您的歷程。 您也可以按兩下。

![](assets/journey44.png)

## 協調活動 {#orchestration-activities}

協調活動是不同的條件，有助於決定歷程的下一步。 可能是該人員是否有未結的支援案例、當前位置的天氣預報、是否完成購買，或是達到10,000個忠誠點數。

從浮動視窗的畫面左側，可使用下列協調活動：

* [條件](../building-journeys/condition-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [讀取區段](../building-journeys/read-segment.md)

![](assets/journey49.png)

## 動作活動 {#action-activities}

動作是您希望在某種觸發（例如傳送訊息）後發生的動作。 這是客戶體驗的歷程片段。

從浮動視窗的畫面左側，位於下方 **[!UICONTROL 事件]** 和 **[!UICONTROL 協調]**，您可以找到 **[!UICONTROL 動作]** 類別。 可使用下列動作活動：

* [電子郵件、簡訊、推播](../building-journeys/journeys-message.md)
* [自訂動作](../building-journeys/using-custom-actions.md)
* [跳轉](../building-journeys/jump.md)

![](assets/journey58.png)

這些活動代表不同的可用通訊通道。您可以結合這些量度，以建立跨管道情境。

如果您已設定自訂動作，它們也會顯示在此處。 [了解更多](../building-journeys/using-custom-actions.md)).

## 最佳做法 {#best-practices}

### 新增標籤

大部分的活動都可讓您定義 **[!UICONTROL 標籤]**. 這會新增尾碼至將出現在畫布中活動底下的名稱。 如果您在歷程中多次使用相同的活動，並且想要更輕鬆地識別，這個功能會很實用。 這也可讓除錯在發生錯誤時更輕鬆，且讓報表更容易讀取。 您也可以新增選填 **[!UICONTROL 說明]**.

![](assets/journey-action-label.png)

### 管理進階參數 {#advanced-parameters}

大部分活動會顯示許多您無法修改的進階和/或技術參數。

![](assets/journey-advanced-parameters.png)

為了提高可讀性，您可以使用 **[!UICONTROL 隱藏只讀欄位]** 按鈕。

![](assets/journey-hide-read-only-fields.png)

在某些特定內容中，您可以覆寫這些參數的值以供特定使用。 若要強制執行值，請按一下欄位右側的&#x200B;**[!UICONTROL 啟用參數覆寫]**&#x200B;圖示。[了解更多](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### 新增替代路徑

當動作或條件發生錯誤時，個人的歷程就會停止。唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL 新增替代路徑以防逾時或發生錯誤]**. 請參閱[本節](../building-journeys/using-the-journey-designer.md#paths)。

![](assets/journey42.png)
