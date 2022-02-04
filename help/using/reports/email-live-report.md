---
title: 以電子郵件傳送即時報告
description: 瞭解如何使用電子郵件即時報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 1ddfbf1a-3cd5-446a-b0fb-76b81b88c1b4
source-git-commit: 7a07f2348f08b4582a1310fb65d431c55451d9b6
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 1%

---

# 以電子郵件傳送即時報告 {#email-live-report}

電子郵件 **[!UICONTROL Live report]** 僅針對特定的電子郵件傳遞。

從 **[!UICONTROL Executions]** 頁籤 **[!UICONTROL Messages]** 菜單，選擇 **[!UICONTROL Live view]** 然後，從選定交貨的「高級」菜單中選擇 **[!UICONTROL Live report]**。

![](../assets/live_report.png)

電子郵件 **[!UICONTROL Live report]** 被分成不同的小部件，詳細列出交付的成功和錯誤。 如果需要，可以調整每個小部件的大小並將其刪除。 有關此項的詳細資訊，請參閱 [節](live-report.md#modify-dashboard)。

![](../assets/live_report_5.png)

**[!UICONTROL Email performance]** 和 **[!UICONTROL Email summary]** 小部件使用圖表和KPI詳細列出與消息相關的主要資訊：

* **[!UICONTROL Targeted]**:符合此傳遞目標配置檔案的用戶配置檔案數。

* **[!UICONTROL Sent]**:交貨的發送總數。

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Opens]**:在傳遞中開啟消息的次數。

* **[!UICONTROL Clicks]**:在傳遞中按一下內容的次數。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL Spam complaints]**:分類為垃圾郵件的郵件數。

* **[!UICONTROL Unsubscriptions]**:取消訂閱連結上的按一下次數。

* **[!UICONTROL Excluded]**:未接收消息的從目標配置檔案中排除的用戶配置檔案數。

的 **[!UICONTROL Sending Statistics]** 小部件詳細瞭解您交付的成功：

* **[!UICONTROL Delivered]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL Bounces]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL Errors]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

![](../assets/live_report_6.png)

的 **[!UICONTROL Error Reasons]** 圖形和表格允許您查看在交付期間發生的錯誤。

的 **[!UICONTROL Bounce Reasons]** 和 **[!UICONTROL Bounce categories]** 小部件包含與已恢復消息相關的可用資料，如：

* **[!UICONTROL Hard bounce]**:永久錯誤（如錯誤的電子郵件地址）的總數。 這涉及一條錯誤消息，該錯誤消息明確指出地址無效，如「未知用戶」。

* **[!UICONTROL Soft bounce]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL Ignored]**:臨時（如「外出」）或技術錯誤（例如，如果發件人類型是郵遞員）的總數。

<!--
![](../assets/live_report_8.png)

>[!NOTE]
>
>The Offers widgets and metrics are only available if a decision was inserted in an email. For more information on Decision Management, refer to this [page](../offers/get-started/starting-offer-decisioning.md).

The **[!UICONTROL Offers statistic]** and **[!UICONTROL Offers statistics]** over time widgets measure your offer's success and impact on your targeted audience. It detail the main information relative to your message with KPIs:

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression]**: Number of times the offer was opened in a delivery.

* **[!UICONTROL Offer clicks]**: Number of times an offer was clicked on in a delivery.
-->
>[!NOTE]
>
>配置檔案 **[!UICONTROL Suppressed]** 或 **[!UICONTROL Not allowed]** 在消息發送過程中，狀態被排除。 因此，當 **行程報告** 將顯示這些配置檔案在旅途中移動([讀取段](../building-journeys/read-segment.md) 和 [消息](../building-journeys/journeys-message.md) 活動), **電子郵件報告** 不會把它們包括在 **[!UICONTROL Sent]** 在發送電子郵件之前過濾掉度量。
>
>瞭解 [隱藏清單](../messages/suppression-list.md) 和 [允許清單](../messages/allow-list.md)。 要查找所有排除案例的原因，可使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。
