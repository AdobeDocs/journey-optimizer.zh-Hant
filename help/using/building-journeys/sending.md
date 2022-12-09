---
solution: Journey Optimizer
product: journey optimizer
title: 開始歷程執行
description: 了解如何開始您的歷程並傳送訊息
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# 歷程執行 {#message-execution}

## 測試您的歷程

您可以使用測試設定檔來測試您的歷程。 建議您執行此步驟來驗證您的設定和訊息。

了解更多資訊 [節](testing-the-journey.md).

## 啟動您的歷程

您必須發佈歷程才能啟動。

![](assets/jo-journeyuc2_32bis.png)

了解更多資訊 [節](publishing-the-journey.md).


發佈後，您就可以使用專屬的報告工具監控您的歷程，以評估歷程的成效。

![](assets/jo-dynamic_report_journey_12.png)

[進一步了解報表](../reports/live-report.md)

## 傳送訊息 {#send-messages}

當訊息已定義內容時，即可透過 [歷程](journey.md).

傳送訊息後，您可以透過多個指標來監控其執行。 [深入了解報告](../global-report.md).

## 排程訊息 {#schedule-messages}

可透過 **[!UICONTROL Read Segment]** 活動 [歷程](journey.md). 您可以指定區段何時會進入歷程。 [深入了解「讀取區段」活動](read-segment.md).

若要這麼做，請遵循下列步驟：

1. 編輯歷程，拖放 **[!UICONTROL Read Segment]** 活動並開始設定。 [深入了解設定讀取區段活動](read-segment.md#configuring-segment-trigger-activity).

1. 按一下 **[!UICONTROL Edit journey schedule]** 連結以存取歷程的屬性。

   ![](assets/message-read-segment-schedule.png)

1. 設定 **[!UICONTROL Scheduler type]** 欄位：從清單中選取所需值，讓區段以特定日期/時間或循環基準輸入歷程。

   >[!NOTE]
   >
   >此 **[!UICONTROL Schedule]** 區段僅在 **[!UICONTROL Read Segment]** 活動已拖放至畫布中。

   ![](assets/message-read-segment-scheduler.png)

1. 如果您選取 **[!UICONTROL Once]**，定義區段將進入歷程的特定日期和時間。

   ![](assets/message-read-segment-scheduler-once.png)

1. 如果您選取循環方法，請編輯開始日期和時間。 您也可以定義可選的結束日期和時間。

   ![](assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >依預設，區段會輸入歷程 **[!UICONTROL As soon as possible]**，表示歷程發佈後1小時。

1. 按一下 **[!UICONTROL OK]** 來儲存變更。

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
