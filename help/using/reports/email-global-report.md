---
title: 以電子郵件形式傳送全域報告
description: 了解如何使用電子郵件全域報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 2bead395-082a-4fea-ad10-b2b2c5f484e9
source-git-commit: f0e34e040dd0e0ba2fa8293f4290ab55e1781426
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# 以電子郵件傳送全域報告 {#email-global-report}

電子郵件 **[!UICONTROL Global report]** 僅鎖定特定電子郵件傳送。

從 **[!UICONTROL Executions]** 的 **[!UICONTROL Messages]** 菜單，選擇 **[!UICONTROL Global view]** 然後，從所選傳送的進階功能表中選取 **[!UICONTROL Global report]**.

![](../assets/global_report_3.png)

電子郵件 **[!UICONTROL Global report]** 會分為不同的小工具，詳述傳送的成功和錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 如需詳細資訊，請參閱 [節](global-report.md#modify-dashboard).

![](../assets/global_report_4.png)

**[!UICONTROL Email performance]** 使用KPI詳細說明與訊息相關的主要資訊：

* **[!UICONTROL Sent]**:傳送的傳送總數。

* **[!UICONTROL Delivery Rate]**:已成功發送的消息的百分比。

* **[!UICONTROL Bounce Rate]**:跳出的電子郵件與傳送的電子郵件的百分比。

* **[!UICONTROL Error Rate]**:傳送期間發生、無法傳送的錯誤百分比，與已傳送的電子郵件相比。

* **[!UICONTROL Open Rate]**:已開啟郵件的百分比。

* **[!UICONTROL Click Rate]**:傳送中的點按百分比。

* **[!UICONTROL Spam Complaint Rate]**:收件者標示為垃圾訊息的電子郵件與已傳送郵件的百分比。 如需投訴的詳細資訊，請參閱 [傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}。

* **[!UICONTROL Unsubscribe Rate]**:不重複取消訂閱與已傳送訊息數量的百分比。 此指標不取決於取消訂閱連結的點按次數，而是根據收件者起始的取消訂閱次數。 了解更多取消訂閱，請參閱 [頁面](../consent.md).

此 **[!UICONTROL Email - Tracking statistics]** 包含您傳送之收件者活動的可用資料：

* **[!UICONTROL Opens]**:傳送中開啟傳送的次數。

* **[!UICONTROL Unique Opens]**:已開啟傳遞的百分比。

* **[!UICONTROL Open Rate]**:已開啟電子郵件的總數與已傳送電子郵件的總數相比。

* **[!UICONTROL Clicks]**:電子郵件中內容被點按的次數。

* **[!UICONTROL Unique Clicks]**：按一下電子郵件內容的收件者人數。

* **[!UICONTROL Click through rate]**:與歷程互動的使用者百分比。

此 **[!UICONTROL Sending Statistics]** 圖表會詳細說明您的傳送是否成功：

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

![](../assets/global_report_5.png)

此 **[!UICONTROL Bounce Reasons]** 和 **[!UICONTROL Bounce categories]** 小工具包含與退信消息相關的可用資料，例如：

* **[!UICONTROL Hard bounce]**:永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知」使用者。

* **[!UICONTROL Soft bounce]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL Ignored]**:臨時（例如不在辦公室）或技術錯誤（例如，如果發送者類型是郵遞員）的總數。

如需退信的詳細資訊，請參閱 [隱藏清單](../suppression-list.md) 頁面。

此 **[!UICONTROL Error Reasons]** 圖形和表格可讓您查看在傳送期間發生的錯誤。

![](../assets/global_report_6.png)

此 **[!UICONTROL Email - Top recipient domain]** 圖表和表格詳細說明收件者最常使用哪些網域來開啟電子郵件。

此 **[!UICONTROL Email - Top Url]** 圖表和表格會詳細說明哪些URL最常被瀏覽。

此 **[!UICONTROL Open vs Click]** 識別收件者與傳送的互動：

* **[!UICONTROL Unique Clicks]**：按一下電子郵件內容的收件者人數。

* **[!UICONTROL Unique Opens]**:開啟傳遞的收件者人數。

![](../assets/global_report_20.png)

>[!NOTE]
>
>只有在電子郵件中插入決策時，選件小工具和量度才可供使用。 有關「決策管理」的詳細資訊，請參閱 [頁面](../offers/get-started/starting-offer-decisioning.md).

此 **[!UICONTROL Offers statistic]** 和 **[!UICONTROL Offers statistics]** 一段時間後，Widget會測量選件的成功，以及對目標對象的影響。 它會使用KPI詳細說明與訊息相關的主要資訊：

* **[!UICONTROL Offer sent]**:選件的傳送總數。

* **[!UICONTROL Offer impression]**:傳遞中開啟選件的次數。

* **[!UICONTROL Offer clicks]**:傳送中點按選件的次數。

此 **[!UICONTROL Offers detailed statistic]** 表格包含您選件中收件者活動的可用資料：

* **[!UICONTROL Placement name]**:用來顯示優惠方案的版位名稱。 有關投放位置的詳細資訊，請參閱 [頁面](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**:傳送中新增的選件名稱。 有關投放位置的詳細資訊，請參閱 [頁面](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**:選件的傳送總數。

* **[!UICONTROL Offer impression rate]**:已開啟選件與已傳送選件數量的百分比。

* **[!UICONTROL Offer click rate]**:與優惠方案互動的使用者百分比。

>[!NOTE]
>
>具有 **[!UICONTROL Suppressed]** 或 **[!UICONTROL Not allowed]** 在訊息傳送程式期間會排除狀態。 因此，若 **歷程報表** 會將這些設定檔顯示為已在歷程中移動([讀取區段](../building-journeys/read-segment.md) 和 [訊息](../building-journeys/journeys-message.md) 活動), **電子郵件報表** 不會將其納入 **[!UICONTROL Sent]** 量度，因為在傳送電子郵件前會先將量度篩選掉。
>
>深入了解 [隱藏清單](../suppression-list.md) 和 [允許的清單](../allow-list.md). 若要找出所有排除案例的原因，您可以使用 [Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。
