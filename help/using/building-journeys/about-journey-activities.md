---
title: 關於歷程活動
description: 瞭解旅行活動
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 29%

---

# 關於歷程活動 {#about-journey-activities}

結合不同的事件、協調和動作活動，以建立您的多步驟跨管道情境。

## 事件活動 {#event-activities}

由技術用戶配置的事件(請參見 [此頁](../event/about-events.md))，所有內容都顯示在螢幕左側的調色板的第一個類別中。 以下活動可用：

* [一般事件](../building-journeys/general-events.md)
* [反應](../building-journeys/reaction-events.md)
* [段資格](../building-journeys/segment-qualification-events.md)

![](../assets/journey43.png)

通過拖放事件活動來開始您的旅程。 也可以按兩下它。

![](../assets/journey44.png)

## 協調活動 {#orchestration-activities}

在螢幕左側的調色板中，可以使用以下業務流程活動：

* [條件](../building-journeys/condition-activity.md)
* [結尾](../building-journeys/end-activity.md)
* [等待](../building-journeys/wait-activity.md)
* [讀取段](../building-journeys/read-segment.md)

![](../assets/journey49.png)

## 動作活動 {#action-activities}

從調色板，在螢幕左側，在下面 **[!UICONTROL Events]** 和 **[!UICONTROL Orchestration]**&#x200B;的 **[!UICONTROL Actions]** 的子菜單。 以下活動可用：

* [訊息](../building-journeys/journeys-message.md)
* [自訂動作](../building-journeys/using-custom-actions.md)
* [跳轉](../building-journeys/jump.md)

![](../assets/journey58.png)

這些活動代表不同的可用通訊通道。您可以將它們組合起來，以建立跨渠道方案。

如果已配置自定義操作，則這些操作將出現在此處(請參閱 [此頁](../building-journeys/using-custom-actions.md))。

## 最佳做法 {#best-practices}

大多數活動都允許您定義 **[!UICONTROL Label]**。 這會為畫布中活動下顯示的名稱添加尾碼。 如果您在旅途中多次使用同一活動並且希望更容易識別這些活動，則此功能非常有用。 它還使調試在出現錯誤時更容易，並使報告更易於閱讀。 您還可以添加可選 **[!UICONTROL Description]**。

![](../assets/journey59bis.png)

當動作或條件發生錯誤時，個人的歷程就會停止。唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL Add an alternative path in case of a timeout or an error]**。請參閱[本節](../building-journeys/using-the-journey-designer.md#paths)。

![](../assets/journey42.png)
