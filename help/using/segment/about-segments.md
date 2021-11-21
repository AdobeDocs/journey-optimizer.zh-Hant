---
title: 關於 Adobe Experience Platform 區段
description: 了解如何設定Adobe Experience Platform區段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 2%

---

# 關於 Adobe Experience Platform 區段 {#about-segments}

[!DNL Journey Optimizer]  可讓您直接使用Adobe Experience Platform的即時客戶設定檔資料，建立 **[!UICONTROL Segments]** 功能表，並將其運用於您的歷程中。

請注意，您也可以從分段服務本身建立區段。 了解更多 [Adobe Experience Platform區段服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

您可以在歷程中以不同方式運用區段：

* 使用 **讀取區段** 協調活動，讓屬於指定區段的所有個人進入歷程。 歷程中包含的訊息會傳送給屬於區段的個人。 假設您有「銀色客戶」區段。 透過此活動，您可以讓所有銀級客戶進入歷程，並傳送一系列個人化訊息。

   如需如何使用的詳細資訊 **[!UICONTROL Read segment]** 活動，請參閱 [本節](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* 使用 **區段資格** 事件活動，根據Adobe Experience Platform區段入口和出口，讓個人進入或前進歷程。 例如，您可以讓所有新銀級客戶進入歷程並傳送訊息。 有關如何使用此活動的詳細資訊，請參閱 [本節](../building-journeys/segment-qualification-events.md).

* 建置 **複雜條件** 在歷程中，使用簡單或進階運算式編輯器。 深入了解 [本節](../building-journeys/condition-activity.md#using-a-segment).

## Adobe Journey Optimizer評價方法 {#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer中，受眾是使用下列其中一種評估方法從區段定義產生：

* 串流區段 — 當新資料流入系統時，區段的對象清單會即時保持最新。
* 批次區段 — 區段的對象清單會根據過去一小時內到達的資料，每小時更新一次。

系統會根據評估區段規則的複雜度和成本，對每個區段定義進行批次分段和串流分段之間的決定。

您可以在 **[!UICONTROL Evaluation method]** 欄。

在您首次定義區段後，設定檔會在符合資格時新增至對象。

從先前的資料回填受眾最多需要24小時。 回填對象後，對象會持續保持最新狀態，且隨時準備進行目標定位。
