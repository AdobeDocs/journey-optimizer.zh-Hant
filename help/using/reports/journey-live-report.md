---
solution: Journey Optimizer
product: journey optimizer
title: 歷程即時報告
description: 了解如何使用歷程即時報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# 歷程即時報告 {#journey-live-report}

您可以直接從歷程存取即時報告，其中包含 **[!UICONTROL View report]** 按鈕。

![](assets/report_journey.png)

歷程 **[!UICONTROL Live report]** 頁面中顯示以下索引標籤：

* [歷程](#journey-live)
* [電子郵件](#email-live)
* [推播](#push-live)
* [簡訊](#sms-live)

歷程 **[!UICONTROL Live report]** 會分為不同的Widget，詳述您歷程的成功與錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 有關詳細資訊，請參閱 [節](live-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [本頁](live-report.md#list-of-components-live).

## 歷程標籤 {#journey-live}

從您的歷程 **[!UICONTROL Live report]**, **[!UICONTROL Journey]** 索引標籤可讓您清楚檢視歷程的最重要追蹤資料。

![](assets/journey_live_1.png)

+++進一步了解「歷程」報表可用的不同量度和Widget。

**[!UICONTROL Journey Performance]** 可讓您逐步查看目標設定檔的路徑。

此 **[!UICONTROL Journey Statistics]** 介面工具集顯示下列KPI:

* **[!UICONTROL Entered profiles]**:到達歷程進入事件的個人總數。

* **[!UICONTROL Exited profiles]**:離開歷程的個人總數。

* **[!UICONTROL Failed individual journeys]**:未成功執行的個別歷程總數。

此 **[!UICONTROL Event executed over the last 24 hours]** 和 **[!UICONTROL Events]** 介面工具集可讓您透過摘要編號、圖表和表格，查看哪個事件成功執行。

此 **[!UICONTROL Action executed over the last 24 hours]** 和 **[!UICONTROL Actions executed and errors]** 介面工具集代表觸發動作時發生的最成功動作和錯誤。 動作圖表、表格和摘要數字包含可用於動作的資料，例如：

* **[!UICONTROL Actions executed]**:成功執行歷程之動作的總數。

* **[!UICONTROL Error in actions]**:針對動作發生的錯誤總數。
+++

## 電子郵件索引標籤 {#email-live}

從您的歷程 **[!UICONTROL Live report]**, **[!UICONTROL Email]** 索引標籤會詳細列出與歷程中傳送之電子郵件相關的主要資訊。

![](assets/journey_live_2.png)

+++進一步了解「電子郵件」報表中可用的不同量度和小工具。

此 **[!UICONTROL Email Sending Statistics]** 介面工具集詳細說明了與您的訊息相關的主要資訊：

* **[!UICONTROL Delivered]**:已成功發送的消息數。

* **[!UICONTROL Bounces]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL Sending metrics by Email]** 表格和 **[!UICONTROL Email Summary]** 圖表會詳細說明您的傳送是否成功：

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功發送的消息數。

* **[!UICONTROL Bounces]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL Opens]**:傳送中開啟訊息的次數。

* **[!UICONTROL Clicks]**:內容在傳送中被點按的次數。

* **[!UICONTROL Unsubscribe]**:取消訂閱連結的點按次數。

* **[!UICONTROL Spam complaints]**:宣告郵件為垃圾郵件或垃圾郵件的次數。

此 **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** 和 **[!UICONTROL Hard and bounce - by Email]** 小工具包含與退信相關的可用資料，例如：

* **[!UICONTROL Hard bounce]**:永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知」使用者。

* **[!UICONTROL Soft bounce]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL Ignored]**:臨時的總數，例如「不在辦公室」或技術錯誤，例如，如果發送者類型是郵遞區號。

此 **[!UICONTROL Error Reasons]** 和 **[!UICONTROL Exclude Reasons]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。

此 **[!UICONTROL Email - Top recipient domain]** 圖表和表格詳細說明收件者最常使用哪些網域來開啟電子郵件。

>[!NOTE]
>
>只有在電子郵件中插入決策時，選件小工具和量度才可供使用。 有關「決策管理」的詳細資訊，請參閱 [頁面](../offers/get-started/starting-offer-decisioning.md).

此 **[!UICONTROL Offers statistic]** 和 **[!UICONTROL Offers statistics]** 一段時間後，Widget會測量選件的成功，以及對目標對象的影響。 它會使用KPI詳細說明與訊息相關的主要資訊：

* **[!UICONTROL Offer sent]**:選件的傳送總數。

* **[!UICONTROL Offer impression]**:傳遞中開啟選件的次數。

* **[!UICONTROL Offer clicks]**:傳送中點按選件的次數。
+++

## 推播通知標籤 {#push-live}

從您的歷程 **[!UICONTROL Live report]**, **[!UICONTROL Push notification]** 索引標籤會詳細說明與歷程中傳送的推送傳送相關的主要資訊。

![](assets/journey_live_3.png)

+++進一步了解「推送」報表可用的不同量度和Widget。

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** 和 **[!UICONTROL Sending metrics - by Push]** widget會詳細說明與訊息相關的主要資訊：

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功發送的消息數。

* **[!UICONTROL Bounces]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL Opens]**:傳送中開啟訊息的次數。

* **[!UICONTROL Actions]**:已傳送推播通知的動作總數，例如按鈕點擊或解除。

* **[!UICONTROL Engagements]**:此推播通知的開啟次數和動作總數，亦即設定檔開啟了推播或按了按鈕。

此 **[!UICONTROL Error Reasons]** 和 **[!UICONTROL Exclude Reasons]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。

此 **[!UICONTROL Sending statistics - Failed]** 介面工具集可讓您查看發生了多少錯誤和彈回。

此 **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** 和 **[!UICONTROL Breakdown by platform]** 圖表和表格會根據作業系統，詳細說明推播通知的成功。
+++

## SMS標籤 {#sms-live}

![](assets/journey_live_4.png)

+++進一步了解SMS報表可用的不同量度和Widget。

此 **[!UICONTROL SMS - Sending statistics]** 表格會詳細說明傳送的成功：

* **[!UICONTROL Targeted]**:符合此傳送目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL Excluded]**:未接收訊息的使用者設定檔數目，已從目標設定檔中排除。

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功發送的消息數。

* **[!UICONTROL Opens]**:傳送中開啟訊息的次數。

* **[!UICONTROL Clicks]**:內容在傳送中被點按的次數。

* **[!UICONTROL Bounces]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL SMS Summary]** 圖表會詳細說明您的傳送是否成功：

* **[!UICONTROL Delivered]**:已成功發送的消息數。

* **[!UICONTROL Bounces]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL Exclude Reasons]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。
+++
