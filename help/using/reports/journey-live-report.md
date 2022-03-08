---
title: 歷程即時報告
description: 瞭解如何使用行程即時報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 1%

---

# 歷程即時報告 {#journey-live-report}

您可以直接通過 **[!UICONTROL Live report]** 按鈕

![](../assets/report_1.png)

旅程 **[!UICONTROL Live report]** 的子菜單。

* [歷程](#journey-live)
* [電子郵件](#email-live)
* [推播](#push-live)

旅程 **[!UICONTROL Live report]** 被分成不同的小部件，詳細描述你旅途的成功和錯誤。 如果需要，可以調整每個小部件的大小並將其刪除。 有關此的詳細資訊，請參閱此 [節](live-report.md#modify-dashboard)。

## 行程頁籤 {#journey-live}

從你的旅程 **[!UICONTROL Live report]**，也請參見Wiki頁。 **[!UICONTROL Journey]** 頁籤可讓您清楚地查看有關行程的最重要跟蹤資料。

![](../assets/report_journey_2.png)

**[!UICONTROL Journey Performance]** 允許您逐步查看目標配置檔案的路徑。

的 **[!UICONTROL Journey Statistics]** 小部件顯示以下KPI:

* **[!UICONTROL Entered profiles]**:到達旅程的入門事件的個人總數。

* **[!UICONTROL Exited profiles]**:離開旅程的個人總數。

* **[!UICONTROL Failed individual journeys]**:未成功執行的單個行程的總數。

![](../assets/report_journey_3.png)

的 **[!UICONTROL Event executed over the last 24 hours]** 和 **[!UICONTROL Events]** 通過小部件，您可以通過摘要編號、圖形和表來查看哪些事件已成功執行。

![](../assets/report_journey_4.png)

的 **[!UICONTROL Action executed over the last 24 hours]** 和 **[!UICONTROL Actions executed and errors]** 小部件表示觸發操作時發生的最成功的操作和錯誤。 「操作」圖形、表和摘要編號包含可用於操作的資料，例如：

* **[!UICONTROL Actions executed]**:成功執行行程的操作總數。

* **[!UICONTROL Error in actions]**:為操作發生的錯誤總數。

<!--
![](../assets/live_report_7.png)

>[!NOTE]
>
>The Offers widgets and metrics are only available if a decision was inserted in an email. For more information on Decision Management, refer to this [page](../offers/get-started/starting-offer-decisioning.md).

The **[!UICONTROL Offers statistic]** and **[!UICONTROL Offers statistics]** over time widgets measure your offer's success and impact on your targeted audience. It detail the main information relative to your message with KPIs:

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression]**: Number of times the offer was opened in a delivery.

* **[!UICONTROL Offer clicks]**: Number of times an offer was clicked on in a delivery.
-->

## 電子郵件頁籤 {#email-live}

從你的旅程 **[!UICONTROL Live report]**，也請參見Wiki頁。 **[!UICONTROL Email]** 頁籤，詳細列出與在旅途中發送的電子郵件遞送相關的主要資訊。

有關特定電子郵件傳遞的詳細報告，請參閱 [電子郵件即時報告](email-live-report.md) 的子菜單。

![](../assets/report_email_1.png)

的 **[!UICONTROL Email Sending Statistics]** 小部件詳細列出與消息相關的主要資訊：

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL Sending metrics by Email]** 表格和 **[!UICONTROL Email Summary]** 圖表詳細說明了您交付的成功：

* **[!UICONTROL Sent]**:交貨的發送總數。

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL Opens]**:在傳遞中開啟消息的次數。

* **[!UICONTROL Clicks]**:在傳遞中按一下內容的次數。

* **[!UICONTROL Unsubscribe]**:取消訂閱連結上的按一下次數。

* **[!UICONTROL Spam complaints]**:將郵件聲明為垃圾郵件或垃圾郵件的次數。

![](../assets/report_email_2.png)

的 **[!UICONTROL Bounce Reasons]**。 **[!UICONTROL Bounce categories]** 和 **[!UICONTROL Hard and bounce - by Email]** 小部件包含與已恢復消息相關的可用資料，如：

* **[!UICONTROL Hard bounce]**:永久錯誤（如錯誤的電子郵件地址）的總數。 這涉及一條錯誤消息，該錯誤消息明確指出地址無效，如「未知用戶」。

* **[!UICONTROL Soft bounce]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL Ignored]**:臨時（如「外出」）或技術錯誤（例如，如果發件人類型是郵遞員）的總數。

的 **[!UICONTROL Error Reasons]** 圖形和表格允許您查看在交付期間發生的錯誤。

## 推式頁籤 {#push-live}

從你的旅程 **[!UICONTROL Live report]**，也請參見Wiki頁。 **[!UICONTROL Push]** 頁籤詳細列出與在行程中發送的推送交貨相關的主要資訊。

有關特定推送交付的詳細報告，請參閱 [推送即時報告](push-live-report.md) 的子菜單。

![](../assets/report_push_1.png)

**[!UICONTROL Push notification sending performance]**。 **[!UICONTROL Push notification summary]** 和 **[!UICONTROL Sending metrics - by Push]** 小部件詳細列出與您的消息相關的主要資訊：

* **[!UICONTROL Sent]**:交貨的發送總數。

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL Opens]**:在傳遞中開啟消息的次數。

* **[!UICONTROL Actions]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

* **[!UICONTROL Engagements]**:此推送通知的開啟和操作總數，即，如果配置檔案開啟了推送或按一下了按鈕。

的 **[!UICONTROL Error Reasons]** 圖形和表格允許您查看在交付期間發生的錯誤。

![](../assets/report_push_2.png)

的 **[!UICONTROL Tracking by platform]**。 **[!UICONTROL Sending by platform]** 和 **[!UICONTROL Breakdown by platform]** 圖表和表根據作業系統詳細說明了推送通知的成功。

的 **[!UICONTROL Sending statistics - Failed]** 小部件允許您查看發生了多少錯誤和彈出。
