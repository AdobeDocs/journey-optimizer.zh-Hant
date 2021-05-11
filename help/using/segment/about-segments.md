---
title: 關於Adobe Experience Platform區段
description: 瞭解如何設定Adobe Experience Platform區段
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# 關於Adobe Experience Platform區段{#about-segments}

![](../assets/do-not-localize/badge.png)

Journey Optimizer可讓您直接從&#x200B;**[!UICONTROL Segments]**&#x200B;功能表使用即時客戶個人檔案資料建立Adobe Experience Platform區段，並將它們運用在您的歷程中。

請注意，您也可以從區段服務本身建立區段。 請參閱[Adobe Experience Platform細分服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)瞭解更多資訊。

您可以以不同方式在歷程中運用區段：

* 使用&#x200B;**讀區段**&#x200B;協調活動，讓屬於指定區段的所有個人進入歷程。 您歷程中包含的訊息會傳送給屬於該群體的個人。 假設您有「銀色客戶」群體。 透過此活動，您可以讓所有銀級客戶進入歷程並傳送一系列個人化訊息。

   有關如何使用&#x200B;**[!UICONTROL Read segment]**&#x200B;活動的詳細資訊，請參閱[本節](../building-journeys/read-segment.md#configuring-segment-trigger-activity)。

* 使用&#x200B;**區段資格**&#x200B;活動活動，讓個人根據Adobe Experience Platform區段入口和出口進入或前進旅程。 例如，您可以讓所有新的銀級客戶進入歷程並傳送訊息。 有關如何使用此活動的詳細資訊，請參閱[本節](../building-journeys/segment-qualification-events.md)。

* 使用簡單或進階運算式編輯器，在您的歷程中建立&#x200B;**複雜條件**。 進一步瞭解[本節](../building-journeys/condition-activity.md#using-a-segment)。
