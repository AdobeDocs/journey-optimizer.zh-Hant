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
source-git-commit: 9ceccdf1daca1745cc0610a97660b92524f732d2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# 手動設定[!DNL Customer Journey Analytics] {#cja-ajo}

[!DNL Journey Optimizer]與[!DNL Customer Journey Analytics]的整合可透過自動化報告發佈和自訂資料視覺效果，提供您所有歷程的整體檢視。

以下章節概述如何手動運用Journey Optimizer產生的資料，以便在Customer Journey Analytics中進行深入分析。 請注意，此整合可自動設定。 [了解更多](report-gs-cja.md)

![](assets/cja.png)

在[!DNL Journey Optimizer]中建立您的歷程後，您可以將客戶資料匯入至[!DNL Customer Journey Analytics]以開始報告，並瞭解客戶與您歷程每次互動的影響。

➡️ [探索Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/ajo#manually-configure-a-data-view-to-be-used-with-journey-optimizer){target="_blank"}

>[!NOTE]
>
>除了這項整合外，您也可以將Adobe Journey Optimizer資料集的內容匯出至雲端儲存位置，並將這項資訊用於報表或分析用途。 [瞭解如何將資料集匯出至雲端儲存位置](../data/export-datasets.md)
>

將[!DNL Customer Journey Analytics]用於您的歷程之前，您必須先設定此整合：

1. [使用您要傳送至Adobe Experience Platform的](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html){target="_blank"}資料集[!DNL Customer Journey Analytics]，在&#x200B;**[!UICONTROL 中建立連線]**。

   可以設定下列[!DNL Journey Optimizer]：
   * [歷程步驟事件](../data/datasets-query-examples.md#journey-step-event)：可讓您檢視哪些人進入您的歷程，以及他們到達的距離。
   * [訊息回饋/追蹤資料集](../data/datasets-query-examples.md#message-feedback-event-dataset)：可讓您檢視透過[!DNL Journey Optimizer]傳送之訊息的傳遞資訊。
   * [實體和歷程資料集](../data/datasets-query-examples.md#entity-dataset)：可讓您搜尋好記的名稱，並在您的報告中使用它們。

1. [建立資料檢視](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html){target="_blank"}以設定您要用於報告的維度和量度。

   您可以建立Journey Optimizer特定量度，以便更妥善地反映您歷程的資料。 [了解更多](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics){target="_blank"}

>[!NOTE]
>
>如果您的沙箱有多個連線，請確認[資料檢視](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html){target="_blank"}參考了CJA[中標示為](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html){target="_blank"}使用的&#x200B;**[!UICONTROL 連線]**。 否則，[**中可能會停用CJA中的**&#x200B;分析](report-cja-manage.md#analyze)按鈕[!DNL Journey Optimizer]。

搭配[!DNL Journey Optimizer]使用[!DNL Customer Journey Analytics]可能會導致報告資料的某些差異，原因如下：

* **同時從Azure Data Lake Storage (ADLS)同步資料[!DNL Journey Optimizer]和[!DNL Customer Journey Analytics]以便報告。**

  不同產品的傳入資料處理時間可能略有不同。 因此，顯示從指定日期到當天的報表時，資料可能不相符。 若要減少差異，請使用當日以外的日期範圍。

* **在[!DNL Journey Optimizer]個報表中，傳送的量度也包含重試量度。**

  **[!UICONTROL 重試]**&#x200B;將不會包含在&#x200B;**[!UICONTROL 的]**&#x200B;已傳送[!DNL Customer Journey Analytics]量度中。 這會導致[!DNL Customer Journey Analytics] **[!UICONTROL 已傳送]**&#x200B;個量度顯示低於[!DNL Journey Optimizer]的值。 但是，重試資料已整合至&#x200B;**[!UICONTROL 個成功傳送的郵件]**&#x200B;或&#x200B;**[!UICONTROL 退信]**量度。
為了減少差異，請使用一週前或之後的日期範圍。

* **報告是由不同的資料來源提供。**

  這可能會造成產品之間出現1-2%的資料差異。
