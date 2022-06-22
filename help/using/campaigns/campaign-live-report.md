---
title: 市場活動實況報告
description: 瞭解如何使用市場活動即時報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 43a076632d2f2195ce0293f741dfbc28d4eea24a
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---

# 市場活動實況報告 {#campaign-live-report}

您可以通過 **[!UICONTROL Live view]** 按鈕

市場活動 **[!UICONTROL Live report]** 的子菜單。

* [Campaign](#campaign-live)
* [電子郵件](#email-live)
* [推播](#push-live)

市場活動 **[!UICONTROL Live report]** 被分成不同的小部件，詳細列出您的活動的成功和錯誤。 如果需要，可以調整每個小部件的大小並將其刪除。 有關此的詳細資訊，請參閱此 [節](../reports/live-report.md#modify-dashboard)。

## 市場活動頁籤 {#campaign-global}

### 傳遞 {#delivery-global}

的 **[!UICONTROL Campaign Statistics]** 小部件詳細列出與市場活動相關的主要資訊：

* **[!UICONTROL Entered profiles]**:開始此行程的配置檔案數。

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->
## 電子郵件頁籤 {#email-live}

從您的活動 **[!UICONTROL Live report]**，也請參見Wiki頁。 **[!UICONTROL Email]** 頁籤詳細列出與市場活動中發送的電子郵件交貨相關的主要資訊。

有關特定電子郵件傳遞的詳細報告，請參閱 [電子郵件即時報告](../reports/email-live-report.md) 的子菜單。

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

的 **[!UICONTROL Bounce Reasons]**。 **[!UICONTROL Bounce categories]** 和 **[!UICONTROL Hard and bounce - by Email]** 小部件包含與已恢復消息相關的可用資料，如：

* **[!UICONTROL Hard bounce]**:永久錯誤（如錯誤的電子郵件地址）的總數。 這涉及一條錯誤消息，該錯誤消息明確指出地址無效，如「未知用戶」。

* **[!UICONTROL Soft bounce]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL Ignored]**:臨時（如「外出」）或技術錯誤（例如，如果發件人類型是郵遞員）的總數。

的 **[!UICONTROL Error Reasons]** 和 **[!UICONTROL Exclude Reasons]** 圖形和表格允許您查看在交付期間發生的錯誤和排除。

的 **[!UICONTROL Email - Top recipient domain]** 圖表和表詳細資訊，哪些域是收件人開啟電子郵件時最常用的域。

## 推式頁籤 {#push-live}

從您的活動 **[!UICONTROL Live report]**，也請參見Wiki頁。 **[!UICONTROL Push]** 頁籤詳細列出與市場活動中發送的推送交貨相關的主要資訊。

有關特定推送交付的詳細報告，請參閱 [推送即時報告](../reports/push-live-report.md) 的子菜單。

**[!UICONTROL Push notification sending performance]**。 **[!UICONTROL Push notification summary]** 和 **[!UICONTROL Sending metrics - by Push]** 小部件詳細列出與您的消息相關的主要資訊：

* **[!UICONTROL Sent]**:交貨的發送總數。

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL Opens]**:在傳遞中開啟消息的次數。

* **[!UICONTROL Actions]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

* **[!UICONTROL Engagements]**:此推送通知的開啟和操作總數，即，如果配置檔案開啟了推送或按一下了按鈕。

的 **[!UICONTROL Error Reasons]** 和 **[!UICONTROL Exclude Reasons]** 圖形和表格允許您查看在交付期間發生的錯誤和排除。

的 **[!UICONTROL Sending statistics - Failed]** 小部件允許您查看發生了多少個錯誤和彈出。

的 **[!UICONTROL Tracking by platform]**。 **[!UICONTROL Sending by platform]** 和 **[!UICONTROL Breakdown by platform]** 圖表和表根據作業系統詳細說明了推送通知的成功。
