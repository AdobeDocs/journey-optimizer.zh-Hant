---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動上線報表
description: 了解如何使用Campaign即時報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# 行銷活動上線報表 {#campaign-live-report}

您可以使用 **[!UICONTROL Live view]** 按鈕。

行銷活動 **[!UICONTROL Live report]** 頁面中顯示以下索引標籤：

* [行銷活動](#campaign-live)
* [電子郵件](#email-live)
* [推播](#push-live)
* [簡訊](#sms-live)


行銷活動 **[!UICONTROL Live report]** 會分為不同的小工具，詳細說明促銷活動的成功和錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 有關詳細資訊，請參閱 [節](../reports/live-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [本頁](live-report.md#list-of-components-live).

## 行銷活動標籤 {#campaign-global}

### 傳送 {#delivery-global}

此 **[!UICONTROL Campaign Statistics]** 介面工具集詳細說明與促銷活動相關的主要資訊：

* **[!UICONTROL Entered profiles]**:開始歷程的設定檔數。

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## 電子郵件索引標籤 {#email-live}

從您的行銷活動 **[!UICONTROL Live report]**, **[!UICONTROL Email]** 索引標籤會詳細列出與促銷活動中所傳送之電子郵件傳送相關的主要資訊。

![](assets/campaign_report_live_1.png)

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
+++

## 推播通知標籤 {#push-live}

從您的行銷活動 **[!UICONTROL Live report]**, **[!UICONTROL Push notification]** 索引標籤會詳細說明與促銷活動中傳送的推送傳送相關的主要資訊。

![](assets/campaign_report_live_2.png)

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

從您的行銷活動 **[!UICONTROL Live report]**, **[!UICONTROL SMS]** 索引標籤會詳細說明與促銷活動中傳送的SMS傳送相關的主要資訊。

![](assets/campaign_report_live_3.png)

+++進一步了解SMS報表可用的不同量度和Widget。

此 **[!UICONTROL SMS - Sending statistics]** 表格會詳細說明傳送的成功：

* **[!UICONTROL Targeted]**:符合此傳送目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL Excluded]**:未接收訊息的使用者設定檔數目，已從目標設定檔中排除。

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功發送的消息數。

* **[!UICONTROL Bounces]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL SMS Performance by date]** 介面工具集會透過圖表詳細說明與訊息相關的主要資訊：

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功發送的消息數。

* **[!UICONTROL Bounces]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** 和 **[!UICONTROL Error Reasons]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。
+++

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立促銷活動](../campaigns/create-campaign.md)
* [建立API觸發的促銷活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止促銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動全域報表](campaign-global-report.md)
