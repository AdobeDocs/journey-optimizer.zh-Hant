---
title: 關於Adobe Experience Platform區段
description: 了解如何設定Adobe Experience Platform區段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 40dd6e3714aea3dc95183e1decbf1b8f83dad50a
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# 關於Adobe Experience Platform區段 {#about-segments}

[!DNL Journey Optimizer]  可讓您直接從功能表使用即時客戶設定檔資料建立Adobe Experience Platform區 **[!UICONTROL Segments]** 段，並運用在您的歷程中。

請注意，您也可以從分段服務本身建立區段。 如需詳細資訊，請參閱[Adobe Experience Platform分段服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)。

您可以在歷程中以不同方式運用區段：

* 使用&#x200B;**讀取區段**&#x200B;協調活動，讓屬於指定區段的所有個人進入歷程。 歷程中包含的訊息會傳送給屬於區段的個人。 假設您有「銀色客戶」區段。 透過此活動，您可以讓所有銀級客戶進入歷程，並傳送一系列個人化訊息。

   有關如何使用&#x200B;**[!UICONTROL Read segment]**&#x200B;活動的詳細資訊，請參閱[此部分](../building-journeys/read-segment.md#configuring-segment-trigger-activity)。

* 使用&#x200B;**區段資格**&#x200B;事件活動，讓個人根據Adobe Experience Platform區段入口和出口進入或前進歷程。 例如，您可以讓所有新銀級客戶進入歷程並傳送訊息。 有關如何使用此活動的詳細資訊，請參閱[此部分](../building-journeys/segment-qualification-events.md)。

* 使用簡單或進階運算式編輯器，在歷程中建立&#x200B;**複雜條件**。 進一步了解[本節](../building-journeys/condition-activity.md#using-a-segment)。

## Adobe Journey Optimizer評價方法 {#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer中，受眾是使用下列其中一種評估方法從區段定義產生：

* 串流區段 — 當新資料流入系統時，區段的對象清單會即時保持最新。
* 批次區段 — 區段的對象清單會根據過去一小時內到達的資料，每小時更新一次。

系統會根據評估區段規則的複雜度和成本，對每個區段定義進行批次分段和串流分段之間的決定。

您可以在區段清單的&#x200B;**[!UICONTROL Evaluation method]**&#x200B;欄中檢視每個區段的評估方法。

在您首次定義區段後，設定檔會在符合資格時新增至對象。

從先前的資料回填受眾最多需要24小時。 回填對象後，對象會持續保持最新狀態，且隨時準備進行目標定位。
