---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Customer Journey Analytics
description: 開始使用Customer Journey Analytics
feature: Reporting, Integrations
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 11%

---

# 使用 [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] 與整合 [!DNL Customer Journey Analytics] 透過自動化報告分發和自訂資料的視覺化，提供您所有歷程的整體檢視。

![](assets/cja.png)

在中建立您的歷程之後 [!DNL Journey Optimizer]，您可以將客戶資料匯入 [!DNL Customer Journey Analytics] 以開始報告並瞭解客戶與您歷程每次互動的影響。

➡️ [探索Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target="_blank"}

>[!NOTE]
>
>除了這項整合外，您也可以將Adobe Journey Optimizer資料集的內容匯出至雲端儲存位置，並將這項資訊用於報表或分析用途。 [瞭解如何將資料集匯出至雲端儲存位置](../data/export-datasets.md)
>
>請注意，資料集匯出功能目前是測試版，可供所有Adobe Journey Optimizer使用者使用。 如果您尚未擁有存取權，請與 Adobe 代表合作，取得目的地的存取權。

使用前 [!DNL Customer Journey Analytics] 若要進行您的歷程，您必須先設定此整合：

1. [建立連線](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=zh-Hant) 在 [!DNL Customer Journey Analytics] 使用 **[!UICONTROL 資料集]** 您要傳送至Adobe Experience Platform。

   下列專案 [!DNL Journey Optimizer] 可以設定：
   * [歷程步驟事件](../data/datasets-query-examples.md#journey-step-event)：可讓您檢視哪些人進入您的歷程，以及他們到達的距離。
   * [訊息回饋/追蹤資料集](../data/datasets-query-examples.md#message-feedback-event-dataset)：可讓您檢視所傳送訊息的傳送資訊 [!DNL Journey Optimizer].
   * [實體和歷程資料集](../data/datasets-query-examples.md#entity-dataset)：可讓您搜尋好記的名稱，並在報表中使用這些名稱。

1. [建立資料檢視](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 以設定您要用於報告的維度和量度。

   您可以建立Journey Optimizer特定量度，以便更妥善地反映您歷程的資料。 [了解更多](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

使用 [!DNL Journey Optimizer] 替換為 [!DNL Customer Journey Analytics] 可能會導致報表資料中的一些差異，原因如下：

* **兩者 [!DNL Journey Optimizer] 和 [!DNL Customer Journey Analytics] 從Azure Data Lake Storage (ADLS)同步資料以進行報告。**

  不同產品的傳入資料處理時間可能略有不同。 因此，顯示從指定日期到當天的報表時，資料可能不相符。 若要減少差異，請使用當日以外的日期範圍。

* **在 [!DNL Journey Optimizer] 報表，傳送的量度也包含重試量度。**

  **[!UICONTROL 重試]** 將不會包含在 **[!UICONTROL 已傳送]** 中的量度 [!DNL Customer Journey Analytics]. 這將導致 [!DNL Customer Journey Analytics] **[!UICONTROL 已傳送]** 顯示小於以下值的量度 [!DNL Journey Optimizer]. 不過，重試資料會融合到 **[!UICONTROL 已成功傳送的訊息]** 或 **[!UICONTROL 跳出數]** 量度。
為了減少差異，請使用一週前或之後的日期範圍。

* **報表是由不同的資料來源提供。**

  這可能會造成產品之間出現1-2%的資料差異。
