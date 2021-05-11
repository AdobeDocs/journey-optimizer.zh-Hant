---
title: 監視消息執行
description: 瞭解監控准則
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# 消息監視{#monitor-message-execution}

![](assets/do-not-localize/badge.png)

為了確保您的訊息能成功執行、傳送及傳送，[!DNL Journey Optimizer]提供了監控目前發佈及觸發之訊息的功能。 您可從&#x200B;**[!UICONTROL Executions]**&#x200B;清單中即時查看您的訊息在各歷程<!--and APIs-->間的執行情形。

要訪問此清單，請從&#x200B;**[!DNL Journey Optimizer]**&#x200B;首頁中選擇&#x200B;**[!UICONTROL Messages]** ，然後按一下&#x200B;**[!UICONTROL Executions]**&#x200B;頁籤。

此標籤提供兩種檢視：**[!UICONTROL Live view]**&#x200B;和&#x200B;**[!UICONTROL Global view]**。

* **[!UICONTROL Live view]**&#x200B;標籤提供過去24小時內由一個或多個[reyersyles](building-journeys/journey.md) **觸發的所有已執行消息的**&#x200B;即時概述。****

   ![](assets/message-execution-tab-live.png)

   此清單每60秒自動重新整理一次。 如果特定消息在過去24小時內未執行，則所有列都將顯示該消息的空值(0)。

* **[!UICONTROL Global view]**&#x200B;標籤提供自消息開始日期&#x200B;**以來由一個或多個[reyreys](building-journeys/journey.md)**&#x200B;觸發的所有已執行消息&#x200B;**的概述。**

   ![](assets/message-execution-tab-global.png)

   此清單每90分鐘自動重新整理一次。 自每個消息開始日期起，這些資料會隨著時間進行聚合。

如果訊息已發佈但尚未由歷程觸發，則不會列在任何標籤中。 僅列出下列元素：
* 已觸發但尚未啟動（待定）的訊息。
* 已觸發且目前正在執行（進行中）的訊息。

對於多頻道訊息，每則訊息會顯示每個頻道一列。

![](assets/message-execution-multichannel.png)

如果訊息已用於數個歷程，**[!UICONTROL Source]**&#x200B;欄會顯示&#x200B;**[!UICONTROL Multiple]**。

預設情況下，消息將從最近的執行日期開始顯示。 按一下&#x200B;**[!UICONTROL Filters]**&#x200B;圖示，以根據頻道、開始日期和／或結束日期搜尋訊息。

![](assets/message-execution-tab-filters.png)

如果您在&#x200B;**[!UICONTROL Live view]**&#x200B;中，則<!--**[!UICONTROL Quick action]**-->第二欄可以開啟相應的[消息](create-message.md)並訪問[即時報告](reports/live-report.md)；如果您在&#x200B;**[!UICONTROL Global view]**&#x200B;中，則可以訪問[全局報告](reports/global-report.md)。

![](assets/message-execution-open-live-report.png)

對於每個消息執行，會顯示一些指示符：

* **[!UICONTROL Message label]**:建立消息時定義的 [消息標題](create-message.md)。
* **[!UICONTROL Execution ID]**:自動產生的識別碼。
* **[!UICONTROL Source]**:利用該訊息的歷程名稱。
* **[!UICONTROL Start date]**:從歷程中執行訊息的日期和時間。
* **[!UICONTROL Excluded]**:由於排除規則而從初始目標中排除的設定檔數。
* **[!UICONTROL Sent]**:已發送的消息數。
* **[!UICONTROL Delivered]**:在收件者的郵箱（電子郵件）或裝置（推播）中成功傳送的訊息數目，而不產生彈回數或任何其他傳送錯誤。
* **[!UICONTROL Bounces]**:因傳送失敗而無法傳送的訊息數。[進一步瞭解彈回數](suppression-lists.md#delivery-failures)。
* **[!UICONTROL Opens]**:已開啟的消息數。
* **[!UICONTROL Clicks]**:電子郵件中連結的點按次數。

   >[!NOTE]
   >
   >推播通知不存在點按：當使用者按一下推播通知時，會開啟應用程式，而此應用程式只能視為開啟。

* **[!UICONTROL Errors]**:因技術故障而無法傳送的訊息數。

按一下每個超連結將開啟相應的消息摘要視圖。 [進一步瞭解訊息](create-message.md)。
