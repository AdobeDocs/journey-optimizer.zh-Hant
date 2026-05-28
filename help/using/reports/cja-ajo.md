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
TQID: https://experienceleague.adobe.com/ngycFQdp8CtLTngxpPBlAW9xXtCDzo807YdH1xJ8T8A
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 488
ht-degree: 5%

---

# 手動設定[!DNL Customer Journey Analytics] {#cja-ajo}

[!DNL Journey Optimizer]與[!DNL Customer Journey Analytics]的整合可透過自動化報告發佈和自訂資料視覺效果，提供您所有歷程的整體檢視。

以下章節概述如何手動運用Journey Optimizer產生的資料，以便在Customer Journey Analytics中進行深入分析。 請注意，此整合可自動設定。 [了解更多](report-gs-cja.md)

![](assets/cja.png)

在[!DNL Journey Optimizer]中建立您的歷程後，您可以將客戶資料匯入至[!DNL Customer Journey Analytics]以開始報告，並瞭解客戶與您歷程每次互動的影響。

➡️ [探索Customer Journey Analytics](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/integrations/ajo#manually-configure-a-data-view-to-be-used-with-journey-optimizer){target="_blank"}

>[!NOTE]
>
>除了這項整合外，您也可以將Adobe Journey Optimizer資料集的內容匯出至雲端儲存位置，並將這項資訊用於報表或分析用途。 [瞭解如何將資料集匯出至雲端儲存位置](../data/export-datasets.md)
>

將[!DNL Customer Journey Analytics]用於您的歷程之前，您必須先設定此整合：

1. [使用您要傳送至Adobe Experience Platform的&#x200B;**[!UICONTROL 資料集]**，在[!DNL Customer Journey Analytics]中建立連線](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=zh-Hant){target="_blank"}。

   可以設定下列[!DNL Journey Optimizer]：
   * [歷程步驟事件](../data/datasets-query-examples.md#journey-step-event)：可讓您檢視哪些人進入您的歷程，以及他們到達的距離。
   * [訊息回饋/追蹤資料集](../data/datasets-query-examples.md#message-feedback-event-dataset)：可讓您檢視透過[!DNL Journey Optimizer]傳送之訊息的傳遞資訊。
   * [實體和歷程資料集](../data/datasets-query-examples.md#entity-dataset)：可讓您搜尋好記的名稱，並在您的報告中使用它們。

1. [建立資料檢視](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=zh-Hant){target="_blank"}以設定您要用於報告的維度和量度。

   您可以建立Journey Optimizer特定量度，以便更妥善地反映您歷程的資料。 [了解更多](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html?lang=zh-Hant#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics){target="_blank"}

>[!NOTE]
>
>如果您的沙箱有多個連線，請確認[資料檢視](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=zh-Hant){target="_blank"}參考了CJA **中標示為**&#x200B;使用的[連線](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-connections/manage-connections){target="_blank"}。 否則，[!DNL Journey Optimizer]中可能會停用CJA中的&#x200B;[**分析**&#x200B;按鈕](report-cja-manage.md#analyze)。

搭配[!DNL Customer Journey Analytics]使用[!DNL Journey Optimizer]可能會導致報告資料的某些差異，原因如下：

* **同時從Azure Data Lake Storage (ADLS)同步資料[!DNL Journey Optimizer]和[!DNL Customer Journey Analytics]以便報告。**

  不同產品的傳入資料處理時間可能略有不同。 因此，顯示從指定日期到當天的報表時，資料可能不相符。 若要減少差異，請使用當日以外的日期範圍。

* **在[!DNL Journey Optimizer]個報表中，傳送的量度也包含重試量度。**

  **[!UICONTROL 重試]**&#x200B;將不會包含在[!DNL Customer Journey Analytics]的&#x200B;**[!UICONTROL 已傳送]**&#x200B;量度中。 這會導致[!DNL Customer Journey Analytics] **[!UICONTROL 已傳送]**&#x200B;個量度顯示低於[!DNL Journey Optimizer]的值。 但是，重試資料已整合至&#x200B;**[!UICONTROL 個成功傳送的郵件]**&#x200B;或&#x200B;**[!UICONTROL 退信]**&#x200B;量度。
為了減少差異，請使用一週前或之後的日期範圍。

* **報告是由不同的資料來源提供。**

  這可能會造成產品之間出現1-2%的資料差異。
