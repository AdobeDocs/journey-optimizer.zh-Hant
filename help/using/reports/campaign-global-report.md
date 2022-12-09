---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動全域報表
description: 了解如何使用Campaign全域報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 0%

---

# 行銷活動全域報表 {#campaign-global-report}

您可以使用 **[!UICONTROL All time]** 按鈕。

![](assets/campaign_report_global_5.png)

行銷活動 **[!UICONTROL Global report]** 頁面中顯示以下索引標籤：

* [行銷活動](#campaign-global)
* [電子郵件](#email-global)
* [推播](#push-global)
* [簡訊](#sms-global)

行銷活動 **[!UICONTROL Global report]** 會分為不同的小工具，詳細說明促銷活動的成功和錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 有關詳細資訊，請參閱 [節](../reports/global-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [本頁](global-report.md#list-of-components-global.md)

## 行銷活動標籤 {#campaign-global}

### 傳送 {#delivery-global}

![](assets/campaign_report_global_1.png)

此 **[!UICONTROL Campaign's Statistics]** 介面工具集詳細說明與促銷活動相關的主要資訊：

* **[!UICONTROL Entered profiles]**:開始歷程的設定檔數。

* **[!UICONTROL Actions delivered]**:歷程中某個動作已傳送的不重複總次數。

* **[!UICONTROL Actions failed in %]**:歷程中某個動作失敗的不重複次數總計，與已傳送動作的不重複次數總計相比。

## 電子郵件索引標籤 {#email-global}

![](assets/campaign_report_global_2.png)

從您的行銷活動 **[!UICONTROL Global report]**, **[!UICONTROL Email]** 索引標籤會詳細說明與在促銷活動中傳送的電子郵件傳送相關的主要資訊。

+++進一步了解「電子郵件」報表中可用的不同量度和小工具。

此 **[!UICONTROL Email Sending Statistics]** 圖表會詳細說明您的傳送是否成功：

* **[!UICONTROL Targeted]**:傳送分析期間處理的訊息總數。

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Delivery Rate]**:已成功發送的消息的百分比。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Bounce Rate]**:跳出的電子郵件與傳送的電子郵件的百分比。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL Error Rate]**:傳送期間發生、無法傳送的錯誤百分比，與已傳送的電子郵件相比。

* **[!UICONTROL Retries]**:佇列中重試的電子郵件數。

* **[!UICONTROL Excluded]**:Adobe Journey Optimizer已排除的設定檔數目。

此 **[!UICONTROL Email - Tracking statistics]** 介面工具集包含您傳送之收件者活動的可用資料：

* **[!UICONTROL Opens]**:傳送中開啟傳送的次數。

* **[!UICONTROL Unique Opens]**:已開啟傳遞的百分比。

* **[!UICONTROL Open Rate]**:已開啟電子郵件的總數與已傳送電子郵件的總數相比。

* **[!UICONTROL Clicks]**:電子郵件中內容被點按的次數。

* **[!UICONTROL Unique Clicks]**：按一下電子郵件內容的收件者人數。

* **[!UICONTROL Unique Click Rate]**:與傳送互動的使用者百分比。

* **[!UICONTROL Unsubscriptions]**:取消訂閱連結的點按次數。

* **[!UICONTROL Spam complaints]**:宣告郵件為垃圾郵件或垃圾郵件的次數。

此 **[!UICONTROL Sending Statistics]** 圖表包含可用於傳送電子郵件的資料，例如：

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Retries]**:佇列中重試的電子郵件數。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL Bounce Reasons]** 和 **[!UICONTROL Bounce categories]** 小工具包含與退信相關的可用資料，例如：

* **[!UICONTROL Hard bounce]**:永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知」使用者。

* **[!UICONTROL Soft bounce]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL Ignored]**:臨時的總數，例如「不在辦公室」或技術錯誤，例如，如果發送者類型是郵遞區號。

如需退信的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 頁面。

此 **[!UICONTROL Error Reasons]** 圖形和表格可讓您查看在傳送期間發生的錯誤。

此 **[!UICONTROL Excluded reasons]** 圖表和表格顯示阻止從目標設定檔排除的使用者設定檔接收訊息的不同原因。

此 **[!UICONTROL Email - Top Url]** 圖表和表格會詳細說明哪些URL最常被瀏覽。

此 **[!UICONTROL Email - Top recipient domain]** 圖表和表格詳細說明收件者最常使用哪些網域來開啟電子郵件。

>[!NOTE]
>
>此 **[!UICONTROL Optimized vs non optimized]** 和 **[!UICONTROL Send time optimization]**  只有在為您的傳送啟動「傳送時間最佳化」選項時，介面工具集才可用。 如需傳送時間最佳化的詳細資訊，請參閱 [本頁](../building-journeys/journeys-message.md#send-time-optimization).

此 **[!UICONTROL Optimized vs non optimized]** 圖表詳細說明了與訊息相關的主要資訊（無論訊息是否已最佳化）:

* **[!UICONTROL Sent]**:傳送的傳送總數。
* **[!UICONTROL Opens]**:傳送中開啟傳送的次數。
* **[!UICONTROL Clicks]**:電子郵件中內容被點按的次數。

此 **[!UICONTROL Send time optimization]** 根據傳送方法，詳細說明傳送是否成功：優化或正常。

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。
* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。
+++

## 推播通知標籤 {#push-global}

從您的行銷活動 **[!UICONTROL Global report]**, **[!UICONTROL Push notification]** 索引標籤會詳細說明與促銷活動中傳送的推送傳送相關的主要資訊。

![](assets/campaign_report_global_3.png)

+++進一步了解「推送」報表可用的不同量度和Widget。

此 **[!UICONTROL Push notification - Sending statistics]** 表格會透過圖表和KPI，詳細說明與推播通知相關的主要資訊：

* **[!UICONTROL Targeted]**:傳送分析期間處理的訊息總數。

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Delivery Rate]**:已成功發送的消息的百分比。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Bounce Rate]**:跳出的推播通知與傳送的推播通知的百分比。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL Error Rate]**:與傳送的推播通知相比，傳送期間發生而無法傳送的錯誤百分比。

* **[!UICONTROL Excluded]**:Adobe Journey Optimizer已排除的設定檔數目。

此 **[!UICONTROL Push - Tracking statistics]** 包含您傳送的收件者活動可用資料：

* **[!UICONTROL Opens]**:傳送中開啟訊息的次數。

* **[!UICONTROL Open Rate]**:已開啟推播通知的百分比。

* **[!UICONTROL Actions]**:已傳送推播通知的動作總數，例如按鈕點擊或解除。

* **[!UICONTROL Engagements]**:此推播通知的開啟次數和動作總數，亦即設定檔開啟了推播或按了按鈕。

* **[!UICONTROL Engagement Rate]**:此推播通知的開啟次數和動作百分比，亦即設定檔開啟了推播或按鈕被點按時。

此 **[!UICONTROL Push notification summary]** 圖形包含可用於傳送推播通知的資料，例如：

* **[!UICONTROL Opens]**:傳送中開啟訊息的次數。

* **[!UICONTROL Actions]**:已傳送推播通知的動作總數，例如按鈕點擊或解除。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

>[!NOTE]
>
>此 **[!UICONTROL Optimized vs non optimized]** 和 **[!UICONTROL Send time optimization]**  只有在為您的傳送啟動「傳送時間最佳化」選項時，介面工具集才可用。 如需傳送時間最佳化的詳細資訊，請參閱 [本頁](../building-journeys/journeys-message.md#send-time-optimization).

此 **[!UICONTROL Optimized vs non optimized]** 圖表詳細說明了與訊息相關的主要資訊（無論訊息是否已最佳化）:

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。
* **[!UICONTROL Opens]**:傳送中開啟傳送的次數。
* **[!UICONTROL Actions]**:已傳送推播通知的動作總數，例如按鈕點擊或解除。

此 **[!UICONTROL Send time optimization]** 根據傳送方法，詳細說明傳送是否成功：優化或正常。

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。
* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

此 **[!UICONTROL Error Reasons]** 圖形和表格可讓您查看在傳送期間發生的錯誤。

此 **[!UICONTROL Excluded reasons]** 圖表和表格顯示阻止從目標設定檔排除的使用者設定檔接收訊息的不同原因。

此 **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** 和 **[!UICONTROL Breakdown by platform]** 圖形和表格會根據收件者的作業系統，詳細說明推播通知的成功。
+++

## SMS標籤 {#sms-global}

從您的行銷活動 **[!UICONTROL Global report]**, **[!UICONTROL SMS]** 索引標籤會詳細說明與促銷活動中傳送的SMS傳送相關的主要資訊。

![](assets/campaign_report_global_4.png)

+++進一步了解SMS報表可用的不同量度和Widget。

此 **[!UICONTROL SMS - Sending statistics]** 表格會詳細說明傳送的成功：

* **[!UICONTROL Targeted]**:符合此傳送目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL Excluded]**:未接收訊息的使用者設定檔數目，已從目標設定檔中排除。

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL SMS Performance by date]** 介面工具集會透過圖表詳細說明與訊息相關的主要資訊：

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** 和 **[!UICONTROL Error Reasons]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。
+++

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立促銷活動](../campaigns/create-campaign.md)
* [建立API觸發的促銷活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止促銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動上線報表](campaign-live-report.md)
