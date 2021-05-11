---
title: 關於旅程活動
description: 瞭解旅程活動
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 25%

---

# 關於旅程活動{#about-journey-activities}

![](../assets/do-not-localize/badge.png)

結合不同的事件、協調和動作活動，以建立您的多步驟跨管道情境。

## 事件活動 {#event-activities}

技術使用者設定的事件（請參閱[本頁](../event/about-events.md)）都會顯示在畫面左側浮動視窗的第一類別中。 可使用下列事件活動：

* [一般事件](../building-journeys/general-events.md)
* [反應](../building-journeys/reaction-events.md)
* [區段資格](../building-journeys/segment-qualification-events.md)

![](../assets/journey43.png)

透過拖放活動來開始您的旅程。 您也可以按兩下它。

![](../assets/journey44.png)

## 協調活動 {#orchestration-activities}

從畫面左側的浮動視窗中，可進行下列協調活動：

* [條件](../building-journeys/condition-activity.md)
* [結束](../building-journeys/end-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [讀取區段](../building-journeys/read-segment.md)

![](../assets/journey49.png)

## 動作活動 {#action-activities}

從浮動視窗中，在畫面左側的&#x200B;**[!UICONTROL Events]**&#x200B;和&#x200B;**[!UICONTROL Orchestration]**&#x200B;下方，您會找到&#x200B;**[!UICONTROL Actions]**&#x200B;類別。 可使用下列動作活動：

* [訊息](../building-journeys/journeys-message.md)
* [自訂動作](../building-journeys/using-custom-actions.md)
* [跳轉](../building-journeys/jump.md)

![](../assets/journey58.png)

這些活動代表不同的可用通訊通道。您可以合併這些項目，以建立跨通道藍本。

如果您已設定自訂動作，這些動作會出現在此處（請參閱[本頁](../building-journeys/using-custom-actions.md)）。

## 最佳作法 {#best-practices}

大部分活動都允許您定義&#x200B;**[!UICONTROL Label]**。 這會在名稱中加上尾碼，名稱會顯示在畫布中的活動下方。 如果您在歷程中多次使用相同的活動，而且想要更輕鬆地識別這些活動，這個功能就很實用。 此外，在發生錯誤時，除錯也會更輕鬆，並讓報表更容易閱讀。 您也可以新增選用的&#x200B;**[!UICONTROL Description]**。

![](../assets/journey59bis.png)

當動作或條件發生錯誤時，個人的歷程就會停止。唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL Add an alternative path in case of a timeout or an error]**。請參閱[本節](../building-journeys/using-the-journey-designer.md#paths)。

![](../assets/journey42.png)
