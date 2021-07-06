---
title: 監視消息執行
description: 了解監控准則
feature: 監控
topic: 內容管理
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# 訊息監視 {#monitor-message-execution}

為確保您的訊息成功執行、傳送及傳送，[!DNL Journey Optimizer]提供監控目前發佈及觸發之訊息的功能。 您可以從&#x200B;**[!UICONTROL Executions]**&#x200B;清單中即時查看您的訊息在歷程<!--and APIs-->間的執行情形。

要訪問此清單，請從&#x200B;**[!DNL Journey Optimizer]**&#x200B;首頁選擇&#x200B;**[!UICONTROL Messages]**，然後按一下&#x200B;**[!UICONTROL Executions]**&#x200B;頁簽。

此索引標籤提供兩個檢視：**[!UICONTROL Live view]**&#x200B;和&#x200B;**[!UICONTROL Global view]**。

* **[!UICONTROL Live view]**&#x200B;索引標籤提供過去24小時內，由一或多個[journeys](building-journeys/journey.md) **所觸發的所有已執行訊息**&#x200B;的&#x200B;**即時概覽，僅**。

   ![](assets/message-execution-tab-live.png)

   此清單每60秒自動重新整理一次。 如果過去24小時內特定訊息未執行，則所有欄會為該訊息顯示空值(0)。

* **[!UICONTROL Global view]**&#x200B;索引標籤提供自訊息開始日期&#x200B;**以來，由一或多個[journeys](building-journeys/journey.md)**&#x200B;觸發的所有已執行訊息&#x200B;**的概觀。**

   ![](assets/message-execution-tab-global.png)

   此清單每90分鐘自動重新整理一次。 資料會自每個訊息開始日期起隨時間匯總。

如果訊息已發佈，但尚未由歷程觸發，則不會列在任何標籤中。 僅列出下列元素：
* 已觸發但尚未啟動的訊息（擱置中）。
* 已觸發且目前執行（進行中）的訊息。

<!--For multichannel messages, one row per channel is displayed for each message. STILL VALID? looks like NOT-->

>[!NOTE]
>
>如果訊息已用於數個歷程，則每個執行的每個歷程會顯示一列。

<!--![](assets/message-execution-multichannel.png)-->

<!--If a message has been used in several journeys, the **[!UICONTROL Source]** column displays **[!UICONTROL Multiple]**.-->

依預設，訊息會從最近的執行日期開始顯示。 按一下&#x200B;**[!UICONTROL Filters]**&#x200B;圖示，以根據通道、開始日期及/或結束日期來搜尋訊息。

![](assets/message-execution-tab-filters.png)

如果您位於&#x200B;**[!UICONTROL Live view]**&#x200B;中，則<!--**[!UICONTROL Quick action]**-->第二列可以開啟相應的[消息](create-message.md)並訪問[即時報告](reports/live-report.md)；如果您位於&#x200B;**[!UICONTROL Global view]**&#x200B;中，則可以訪問[全局報告](reports/global-report.md)。

![](assets/message-execution-open-live-report.png)

對於每個訊息執行，會顯示許多指標：

* **[!UICONTROL Message label]**:您在建立訊息時定 [義的訊息標題](create-message.md)。自動產生的執行ID會以括弧顯示。

   <!--**[!UICONTROL Execution ID]**: Automatically generated identifier.
  **[!UICONTROL Source]**: Name of the journey leveraging that message.-->

* **[!UICONTROL Journey - Version - Action]**:運用訊息的歷程名稱、歷程版本，以及運用歷程中訊息的動作標籤。

* **[!UICONTROL Status]**:消息執行狀態。  <!--List all the possible statuses? For now only Live status? The user cannot stop or cancel the execution. TBC by Fred-->

* **[!UICONTROL Start date]**:從歷程執行訊息的日期和時間。

   <!--Targeted: Number of targeted profiles for each message execution. To come?-->

* **[!UICONTROL Excluded]**:因排除規則而從初始目標中排除的設定檔數。

* **[!UICONTROL Sent]**:已傳送的訊息數。

* **[!UICONTROL Delivered]**:在收件者的信箱（電子郵件）或裝置（推送）中成功傳送而未產生退信或任何其他傳送錯誤的訊息數目。

* **[!UICONTROL Bounces]**:因傳送失敗而無法傳送的訊息數。[進一步了解跳出數](suppression-list.md)。

* **[!UICONTROL Opens]**:已開啟的郵件數。

* **[!UICONTROL Clicks]**:電子郵件中連結的點按次數。

   >[!NOTE]
   >
   >推播通知不存在點按次數：使用者按一下推播通知時，會開啟應用程式，而此應用程式只能視為開啟。

* **[!UICONTROL Errors]**:因技術故障而無法傳送的訊息數。

* **[!UICONTROL Spam complaints]**:收件者標示為垃圾訊息的郵件數。[傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}中提供投訴的詳細資訊。

按一下每個超連結將開啟相應的消息摘要視圖。 [進一步了解訊息](create-message.md)。
