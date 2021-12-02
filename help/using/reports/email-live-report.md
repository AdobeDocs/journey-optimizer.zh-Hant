---
title: 以電子郵件傳送即時報告
description: 了解如何使用電子郵件即時報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 1ddfbf1a-3cd5-446a-b0fb-76b81b88c1b4
source-git-commit: 36c9b672e9e183cd0aac58582ddd54ccdebd84f7
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 1%

---

# 以電子郵件傳送即時報告 {#email-live-report}

電子郵件 **[!UICONTROL Live report]** 僅鎖定特定電子郵件傳送。

從 **[!UICONTROL Executions]** 的 **[!UICONTROL Messages]** 菜單，選擇 **[!UICONTROL Live view]** 然後，從所選傳送的進階功能表中選取 **[!UICONTROL Live report]**.

![](../assets/live_report.png)

電子郵件 **[!UICONTROL Live report]** 會分為不同的小工具，詳述傳送的成功和錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 如需詳細資訊，請參閱 [節](live-report.md#modify-dashboard).

![](../assets/live_report_5.png)

**[!UICONTROL Email performance]** 和 **[!UICONTROL Email summary]** 小工具會透過圖表和KPI詳細說明與訊息相關的主要資訊：

* **[!UICONTROL Targeted]**:符合此傳送目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Opens]**:傳送中開啟訊息的次數。

* **[!UICONTROL Clicks]**:內容在傳送中被點按的次數。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL Spam complaints]**:分類為垃圾郵件的郵件數。

* **[!UICONTROL Unsubscriptions]**:取消訂閱連結的點按次數。

* **[!UICONTROL Excluded]**:未接收訊息的使用者設定檔數目，已從目標設定檔中排除。

此 **[!UICONTROL Sending Statistics]** 介面工具集會詳細說明您傳送的成功：

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

![](../assets/live_report_6.png)

此 **[!UICONTROL Error Reasons]** 圖形和表格可讓您查看在傳送期間發生的錯誤。

此 **[!UICONTROL Bounce Reasons]** 和 **[!UICONTROL Bounce categories]** 小工具包含與退信消息相關的可用資料，例如：

* **[!UICONTROL Hard bounce]**:永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知」使用者。

* **[!UICONTROL Soft bounce]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL Ignored]**:臨時的總數，例如「不在辦公室」或技術錯誤，例如，如果發送者類型是郵遞區號。

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
>具有 **[!UICONTROL Suppressed]** 或 **[!UICONTROL Not allowed]** 在訊息傳送程式期間會排除狀態。 因此，若 **歷程報表** 會將這些設定檔顯示為已在歷程中移動([讀取區段](../building-journeys/read-segment.md) 和 [訊息](../building-journeys/journeys-message.md) 活動), **電子郵件報表** 不會將其納入 **[!UICONTROL Sent]** 量度，因為在傳送電子郵件前會先將量度篩選掉。
>
>深入了解 [隱藏清單](../suppression-list.md) 和 [允許的清單](../allow-list.md). 若要找出所有排除案例的原因，您可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。
