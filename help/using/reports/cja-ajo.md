---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Customer Journey Analytics
description: 開始使用Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 0e45d6e4995f4f21dc5122203b715ae999e2b760
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 11%

---

# 使用 [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] 整合 [!DNL Customer Journey Analytics] 通過自動報告分發和資料的自定義可視化功能，提供所有行程的整體視圖。

![](assets/cja.png)

在建立您的旅程後 [!DNL Journey Optimizer]，您可以將客戶資料導入 [!DNL Customer Journey Analytics] 啟動報告並瞭解客戶與您的旅程之間的每次交互的影響。

➡️ [發現Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target="_blank"}

>[!NOTE]
>
>除此整合外，您還可以將Adobe Journey Optimizer資料集的內容導出到雲儲存位置，並將此資訊用於報告或分析目的。 [瞭解如何將資料集導出到雲儲存位置](../data/export-datasets.md)
>
>請注意，資料集導出功能當前處於測試版中，可供所有Adobe Journey Optimizer用戶使用。 如果您尚未擁有存取權，請與 Adobe 代表合作，取得目的地的存取權。

使用前 [!DNL Customer Journey Analytics] 對於您的行程，您必須首先配置此整合：

1. [建立連接](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=zh-Hant) 在 [!DNL Customer Journey Analytics] 和 **[!UICONTROL 資料集]** 你想送Adobe Experience Platform。

   以下 [!DNL Journey Optimizer] 可以配置：
   * [行程步驟事件](../data/datasets-query-examples.md#journey-step-event):讓您查看誰進入了您的旅程，以及他們到達的距離。
   * [消息反饋/跟蹤資料集](../data/datasets-query-examples.md#message-feedback-event-dataset):允許您查看有關通過發送的郵件的傳遞資訊 [!DNL Journey Optimizer]。
   * [實體和旅程資料集](../data/datasets-query-examples.md#entity-dataset):允許您搜索友好名稱並在報告中使用它們。

1. [建立資料視圖](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 配置要用於報表的維和度量。

   您可以建立Journey Optimizer特定的指標，以更好地反映您的旅程資料。 [了解更多](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

使用 [!DNL Journey Optimizer] 與 [!DNL Customer Journey Analytics] 可能導致報告資料出現一些差異，原因是：

* **兩者 [!DNL Journey Optimizer] 和 [!DNL Customer Journey Analytics] 同步Azure資料湖儲存(ADLS)中的資料以進行報告。**

   輸入資料的處理時間在產品之間可能略有不同。 因此，當顯示從給定日期到當前日期的報告時，資料可能不匹配。 要減少差異，請使用日期範圍（不包括當天）。

* **在 [!DNL Journey Optimizer] 報告，已發送度量還包括重試度量。**

   **[!UICONTROL 重試次數]** 將不包括在 **[!UICONTROL 已發送]** 度量 [!DNL Customer Journey Analytics]。 這會導致 [!DNL Customer Journey Analytics] **[!UICONTROL 已發送]** 顯示低於 [!DNL Journey Optimizer]。 但是，重試資料會聚到 **[!UICONTROL 已成功發送消息]** 或 **[!UICONTROL 邊界]** 度量。
要減少差異，使用日期範圍為一週前甚至更晚。

* **正在從其他資料源提供報告。**

   這可能導致產品之間1%至2%的資料差異。
