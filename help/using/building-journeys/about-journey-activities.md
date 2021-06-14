---
title: 關於歷程活動
description: 了解歷程活動
feature: Journeys
topic: 內容管理
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 31%

---

# 關於歷程活動 {#about-journey-activities}

![](../assets/do-not-localize/badge.png)

結合不同的事件、協調和動作活動，以建立您的多步驟跨管道情境。

## 事件活動 {#event-activities}

技術使用者設定的事件（請參閱[此頁面](../event/about-events.md)）全部顯示在畫面左側浮動視窗的第一個類別中。 可使用下列事件活動：

* [一般事件](../building-journeys/general-events.md)
* [反應](../building-journeys/reaction-events.md)
* [區段資格](../building-journeys/segment-qualification-events.md)

![](../assets/journey43.png)

拖放事件活動，以開始您的歷程。 您也可以按兩下。

![](../assets/journey44.png)

## 協調活動 {#orchestration-activities}

從浮動視窗的畫面左側，可使用下列協調活動：

* [條件](../building-journeys/condition-activity.md)
* [結尾](../building-journeys/end-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [讀取區段](../building-journeys/read-segment.md)

![](../assets/journey49.png)

## 動作活動 {#action-activities}

從浮動視窗的畫面左側，在&#x200B;**[!UICONTROL Events]**&#x200B;和&#x200B;**[!UICONTROL Orchestration]**&#x200B;下方，您會找到&#x200B;**[!UICONTROL Actions]**&#x200B;類別。 可使用下列動作活動：

* [訊息](../building-journeys/journeys-message.md)
* [自訂動作](../building-journeys/using-custom-actions.md)
* [跳轉](../building-journeys/jump.md)

![](../assets/journey58.png)

這些活動代表不同的可用通訊通道。您可以結合這些量度，以建立跨管道情境。

如果您已設定自訂動作，則會顯示在此處（請參閱[此頁面](../building-journeys/using-custom-actions.md)）。

## 最佳做法 {#best-practices}

大部分活動都可讓您定義&#x200B;**[!UICONTROL Label]**。 這會新增尾碼至將出現在畫布中活動底下的名稱。 如果您在歷程中多次使用相同的活動，並且想要更輕鬆地識別，這個功能會很實用。 這也可讓除錯在發生錯誤時更輕鬆，且讓報表更容易讀取。 您也可以新增選用&#x200B;**[!UICONTROL Description]**。

![](../assets/journey59bis.png)

當動作或條件發生錯誤時，個人的歷程就會停止。唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL Add an alternative path in case of a timeout or an error]**。請參閱[本節](../building-journeys/using-the-journey-designer.md#paths)。

![](../assets/journey42.png)
