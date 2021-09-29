---
title: 以電子郵件傳送即時報告
description: 了解如何使用電子郵件即時報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 1ddfbf1a-3cd5-446a-b0fb-76b81b88c1b4
source-git-commit: d814fa98a08d91f1c0744f106c53dd991d544dc2
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 1%

---

# 以電子郵件傳送即時報告 {#email-live-report}

電子郵件&#x200B;**[!UICONTROL Live report]**&#x200B;只會以特定電子郵件傳送為目標。

從&#x200B;**[!UICONTROL Messages]**&#x200B;菜單的&#x200B;**[!UICONTROL Executions]**&#x200B;頁簽中，選擇&#x200B;**[!UICONTROL Live view]**，然後從所選傳送的高級菜單中選擇&#x200B;**[!UICONTROL Live report]**。

![](../assets/live_report.png)

電子郵件&#x200B;**[!UICONTROL Live report]**&#x200B;會分為不同的小工具集，詳述您的傳送成功和錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 有關詳細資訊，請參閱此[節](live-report.md#modify-dashboard)。

![](../assets/live_report_5.png)

**[!UICONTROL Email performance]** 和小 **[!UICONTROL Email summary]** 工具集會透過圖表和KPI，詳細說明與訊息相關的主要資訊：

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

**[!UICONTROL Sending Statistics]**&#x200B;介面工具集會詳細說明傳送的成功：

* **[!UICONTROL Delivered]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL Bounces]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL Errors]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

![](../assets/live_report_6.png)

**[!UICONTROL Error Reasons]**&#x200B;圖表和表格可讓您查看在傳送期間發生的錯誤。

**[!UICONTROL Bounce Reasons]**&#x200B;和&#x200B;**[!UICONTROL Bounce categories]**&#x200B;介面工具集包含與退信消息相關的可用資料，例如：

* **[!UICONTROL Hard bounce]**:永久錯誤的總數，例如錯誤的電子郵件地址。這包含明確指出地址無效的錯誤訊息，例如「未知」使用者。

* **[!UICONTROL Soft bounce]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL Ignored]**:臨時的總數，例如「不在辦公室」或技術錯誤，例如，如果發送者類型是郵遞區號。

>[!NOTE]
>
>狀態為&#x200B;**[!UICONTROL Suppressed]**&#x200B;或&#x200B;**[!UICONTROL Not allowed]**&#x200B;的設定檔會在訊息傳送程式期間排除。 因此，雖然&#x200B;**歷程報表**&#x200B;會將這些設定檔顯示為已在歷程（[讀取區段](../building-journeys/read-segment.md)和[訊息](../building-journeys/journeys-message.md)活動）中移動，但&#x200B;**電子郵件報表**&#x200B;不會在電子郵件傳送前篩選掉的&#x200B;**[!UICONTROL Sent]**&#x200B;量度中納入這些設定檔。
>
>進一步了解[隱藏清單](../suppression-list.md)和[允許清單](../allow-list.md)。 若要找出所有排除案例的原因，您可以使用[Adobe Experience Platform查詢服務](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}。
