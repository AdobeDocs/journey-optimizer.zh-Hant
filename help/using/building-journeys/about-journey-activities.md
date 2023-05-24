---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用歷程活動
description: 開始使用歷程活動
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 旅程，活動，入門，事件，操作
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 18%

---

# 開始使用歷程活動 {#about-journey-activities}

結合不同的事件、協調和動作活動，以建立您的多步驟跨管道情境。

## 事件活動 {#event-activities}

事件觸發了個性化的旅程，如線上購買。 一旦有人進入旅程，他們就以個人身份穿行，沒有兩個人以相同的速度或相同的路徑前進。 當您以事件開始行程時，當收到事件時，將觸發行程。 然後，旅程中的每個人，單獨地，跟隨在旅途中定義的後續步驟。

由技術用戶配置的事件(請參見 [此頁](../event/about-events.md))，所有內容都顯示在螢幕左側的調色板的第一個類別中。 以下活動可用：

* [一般事件](../building-journeys/general-events.md)
* [反應](../building-journeys/reaction-events.md)
* [段資格](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

通過拖放事件活動來開始您的旅程。 也可以按兩下它。

![](assets/journey44.png)

## 協調活動 {#orchestration-activities}

業務流程活動是幫助確定下一步的不同條件。 可能是此人是否有未結的支援案例、當前地點的天氣預報、是否完成購買或達到10 000個忠誠點。

在螢幕左側的調色板中，可以使用以下業務流程活動：

* [條件](../building-journeys/condition-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [讀取段](../building-journeys/read-segment.md)

![](assets/journey49.png)

## 動作活動 {#action-activities}

操作是您希望通過某種觸發（如發送消息）來執行的操作。 這是客戶體驗的一段旅程。

從調色板，在螢幕左側，在下面 **[!UICONTROL 事件]** 和 **[!UICONTROL 業務流程]**，您可以找到 **[!UICONTROL 操作]** 的子菜單。 以下活動可用：

* [電子郵件、簡訊、推播](../building-journeys/journeys-message.md)
* [自訂動作](../building-journeys/using-custom-actions.md)
* [跳轉](../building-journeys/jump.md)

![](assets/journey58.png)

這些活動代表不同的可用通訊通道。您可以將它們組合起來，以建立跨渠道方案。

如果已配置了自定義操作，它們也會出現在此處。 [了解更多](../building-journeys/using-custom-actions.md)).

## 最佳做法 {#best-practices}

### 添加標籤

大多數活動都允許您定義 **[!UICONTROL 標籤]**。 這會為畫布中活動下顯示的名稱添加尾碼。 如果您在旅途中多次使用同一活動並且希望更容易識別這些活動，則此功能非常有用。 它還使調試在出現錯誤時更容易，並使報告更易於閱讀。 您還可以添加可選 **[!UICONTROL 說明]**。

![](assets/journey-action-label.png)

### 管理高級參數 {#advanced-parameters}

大多數活動都顯示許多您無法修改的高級和/或技術參數。

![](assets/journey-advanced-parameters.png)

為了更好的可讀性，可以使用 **[!UICONTROL 隱藏只讀欄位]** 按鈕

![](assets/journey-hide-read-only-fields.png)

在某些特定上下文中，您可以覆蓋這些參數的值以供特定使用。 若要強制執行值，請按一下欄位右側的&#x200B;**[!UICONTROL 啟用參數覆寫]**&#x200B;圖示。[了解更多](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### 添加替代路徑

當動作或條件發生錯誤時，個人的歷程就會停止。唯一讓它繼續的方法是選中該框 **[!UICONTROL 在超時或出錯時添加備用路徑]**。 請參閱[本節](../building-journeys/using-the-journey-designer.md#paths)。

![](assets/journey42.png)
