---
title: 行銷活動全域報告
description: 瞭解如何從市場活動全局報告中使用資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 行銷活動全域報告 {#campaign-global-report}

您可以直接從市場活動訪問市場活動全局報告， **[!UICONTROL Global view]** 按鈕

市場活動 **[!UICONTROL Global report]** 的子菜單。

* [Campaign](#campaign-global)
* [電子郵件](#email-global)
* [推播](#push-global)

市場活動 **[!UICONTROL Global report]** 被分成不同的小部件，詳細列出您的活動的成功和錯誤。 如果需要，可以調整每個小部件的大小並將其刪除。 有關此的詳細資訊，請參閱此 [節](../reports/global-report.md#modify-dashboard)。

## 市場活動頁籤 {#campaign-global}

### 傳遞 {#delivery-global}

![](assets/campaign_report_global_1.png)

的 **[!UICONTROL Campaign's Statistics]** 小部件詳細列出與市場活動相關的主要資訊：

* **[!UICONTROL Entered profiles]**:開始此行程的配置檔案數。

* **[!UICONTROL Actions delivered]**:在行程中執行操作的唯一時間總數。

* **[!UICONTROL Actions failed in %]**:在行程中某個操作失敗的唯一次數與已傳遞操作的唯一次數之和。

<!--
### Experimentation tab (#experimentation-global)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## 電子郵件頁籤 {#email-global}

從您的活動 **[!UICONTROL Global report]**，也請參見Wiki頁。 **[!UICONTROL Email]** 頁籤詳細列出與「市場活動」中發送的電子郵件交貨相關的主要資訊。

有關特定電子郵件傳遞的詳細報告，請參閱 [電子郵件全局報告](../reports/email-global-report.md) 的子菜單。

的 **[!UICONTROL Email Sending Statistics]** 圖表詳細說明了您交付的成功：

* **[!UICONTROL Targeted]**:在傳遞分析期間處理的郵件總數。

* **[!UICONTROL Sent]**:交貨的發送總數。

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Delivery Rate]**:成功發送的郵件百分比。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Bounce Rate]**:與發送的電子郵件相比，已跳轉的電子郵件的百分比。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL Error Rate]**:與發送的電子郵件相比，在發送過程中發生的阻止發送錯誤的百分比。

* **[!UICONTROL Retries]**:隊列中重試的電子郵件數。

* **[!UICONTROL Excluded]**:被Adobe Journey Optimizer排除的檔案數。

的 **[!UICONTROL Email - Tracking statistics]** 包含您交貨的收件人活動的可用資料：

* **[!UICONTROL Opens]**:在交貨中開啟交貨的次數。

* **[!UICONTROL Unique Opens]**:已開啟交貨的百分比。

* **[!UICONTROL Open Rate]**:已開啟電子郵件的總數與已發送電子郵件的數量相比。

* **[!UICONTROL Clicks]**:在電子郵件中按一下內容的次數。

* **[!UICONTROL Unique Clicks]**：按一下電子郵件內容的收件人數。

* **[!UICONTROL Unique Click Rate]**:與遞送互動的用戶百分比。

* **[!UICONTROL Unsubscriptions]**:取消訂閱連結上的按一下次數。

* **[!UICONTROL Spam complaints]**:將郵件聲明為垃圾郵件或垃圾郵件的次數。

的 **[!UICONTROL Sending Statistics]** 圖形包含可用於已發送電子郵件的資料，如：

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Retries]**:隊列中重試的電子郵件數。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL Bounce Reasons]** 和 **[!UICONTROL Bounce categories]** 小部件包含與已恢復消息相關的可用資料，如：

* **[!UICONTROL Hard bounce]**:永久錯誤（如錯誤的電子郵件地址）的總數。 這涉及一條錯誤消息，該錯誤消息明確指出地址無效，如「未知用戶」。

* **[!UICONTROL Soft bounce]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL Ignored]**:臨時（如「外出」）或技術錯誤（例如，如果發件人類型是郵遞員）的總數。

有關退貨的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 的子菜單。

的 **[!UICONTROL Error Reasons]** 圖形和表格允許您查看在交付期間發生的錯誤。

的 **[!UICONTROL Excluded reasons]** 圖形和表顯示阻止從目標配置檔案中排除的用戶配置檔案接收消息的不同原因。

的 **[!UICONTROL Email - Top Url]** 圖表和表詳細資訊，您傳遞的URL訪問量最大。

的 **[!UICONTROL Email - Top recipient domain]** 圖表和表詳細資訊，哪些域是收件人開啟電子郵件時最常用的域。

>[!NOTE]
>
>的 **[!UICONTROL Optimized vs non optimized]** 和 **[!UICONTROL Send time optimization]**  只有在為您的交貨激活「發送時間優化」選項時，小部件才可用。 有關發送時間優化的詳細資訊，請參閱此 [頁](../building-journeys/journeys-message.md#send-time-optimization)。

的 **[!UICONTROL Optimized vs non optimized]** 圖表詳細列出了與消息相關的主要資訊，這些資訊是否已優化：

* **[!UICONTROL Sent]**:交貨的發送總數。
* **[!UICONTROL Opens]**:在交貨中開啟交貨的次數。
* **[!UICONTROL Clicks]**:在電子郵件中按一下內容的次數。

的 **[!UICONTROL Send time optimization]** 根據發送方法詳細說明您的交付成功：已優化或正常。

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。
* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

## 推式頁籤 {#push-global}

從您的活動 **[!UICONTROL Global report]**，也請參見Wiki頁。 **[!UICONTROL Push]** 頁籤詳細列出與市場活動中發送的推送交貨相關的主要資訊。

有關特定推送交付的詳細報告，請參閱 [推送全局報告](../reports/push-global-report.md)。

的 **[!UICONTROL Push notification - Sending statistics]** 表詳細列出了與使用圖表和KPI的推送通知相關的主要資訊：

* **[!UICONTROL Targeted]**:在傳遞分析期間處理的郵件總數。

* **[!UICONTROL Sent]**:交貨的發送總數。

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Delivery Rate]**:成功發送的郵件百分比。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Bounce Rate]**:與發送的推送通知相比，已跳轉的推送通知的百分比。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL Error Rate]**:與發送的推送通知相比，在發送過程中發生的錯誤阻止發送的百分比。

* **[!UICONTROL Excluded]**:被Adobe Journey Optimizer排除的檔案數。

的 **[!UICONTROL Push - Tracking statistics]** 包含您交貨的收件人活動的可用資料：

* **[!UICONTROL Opens]**:在傳遞中開啟消息的次數。

* **[!UICONTROL Open Rate]**:開啟的推送通知百分比。

* **[!UICONTROL Actions]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

* **[!UICONTROL Engagements]**:此推送通知的開啟和操作總數，即，如果配置檔案開啟了推送或按一下了按鈕。

* **[!UICONTROL Engagement Rate]**:此推送通知的開啟和操作的百分比，即，如果配置檔案開啟了推送或按一下了按鈕。

的 **[!UICONTROL Push notification summary]** 圖形包含可用於發送推送通知的資料，如：

* **[!UICONTROL Opens]**:在傳遞中開啟消息的次數。

* **[!UICONTROL Actions]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

>[!NOTE]
>
>的 **[!UICONTROL Optimized vs non optimized]** 和 **[!UICONTROL Send time optimization]**  只有在為您的交貨激活「發送時間優化」選項時，小部件才可用。 有關發送時間優化的詳細資訊，請參閱此 [頁](../building-journeys/journeys-message.md#send-time-optimization)。

的 **[!UICONTROL Optimized vs non optimized]** 圖表詳細列出了與消息相關的主要資訊，這些資訊是否已優化：

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。
* **[!UICONTROL Opens]**:在交貨中開啟交貨的次數。
* **[!UICONTROL Actions]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

的 **[!UICONTROL Send time optimization]** 根據發送方法詳細說明您的交付成功：已優化或正常。

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。
* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

的 **[!UICONTROL Error Reasons]** 圖形和表格允許您查看在交付期間發生的錯誤。

的 **[!UICONTROL Excluded reasons]** 圖形和表顯示阻止從目標配置檔案中排除的用戶配置檔案接收消息的不同原因。

的 **[!UICONTROL Tracking by platform]**。 **[!UICONTROL Sending by platform]** 和 **[!UICONTROL Breakdown by platform]** 圖表和表格根據收件人的作業系統詳細說明推送通知的成功。

## 其他資源

* [開始使用行銷活動](get-started-with-campaigns.md)
* [建立行銷活動](create-campaign.md)
* [建立API觸發的市場活動](api-triggered-campaigns.md)
* [修改或停止行銷活動](modify-stop-campaign.md)
* [行銷活動即時報告](campaign-live-report.md)
