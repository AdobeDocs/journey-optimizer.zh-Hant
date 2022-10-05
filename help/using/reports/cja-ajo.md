---
title: 使用Customer Journey Analytics
description: 開始使用Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
source-git-commit: ce0906afb8561c586cb080c4a49c58fb5bfac6a9
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 7%

---

# 使用 [!DNL Customer Journey Analytics] {#cja-ajo}

![](assets/cja.png)
[!DNL Journey Optimizer] 整合 [!DNL Customer Journey Analytics] 透過自動化報表分送和資料的自訂視覺效果，提供您所有歷程的全方位檢視。

在中建立您的歷程後 [!DNL Journey Optimizer]，您可以將客戶資料匯入 [!DNL Customer Journey Analytics] 以開始報告並了解客戶與您歷程的每次互動的影響。

➡️ [DiscoverCustomer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target=&quot;_blank&quot;}

使用前 [!DNL Customer Journey Analytics] 對於您的歷程，您必須先設定此整合：

1. [建立連線](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) in [!DNL Customer Journey Analytics] 和 **[!UICONTROL 資料集]** 您要傳送至平台。

   以下 [!DNL Journey Optimizer] 可設定：
   * [歷程步驟事件](../start/datasets-query-examples.md#journey-step-event):可讓您檢視進入您歷程的人員，以及他們到達的距離。
   * [訊息意見/追蹤資料集](../start/datasets-query-examples.md#message-feedback-event-dataset):可讓您檢視透過傳送之訊息的傳送資訊 [!DNL Journey Optimizer].
   * [實體和歷程資料集](../start/datasets-query-examples.md#entity-dataset):可讓您搜尋好記名稱，並在報表中使用。

1. [建立資料檢視](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 來設定您要用於報表的維度和量度。

   您可以建立Journey Optimizer特定量度，以更妥善地反映您的歷程資料。 [了解更多](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)


使用 [!DNL Journey Optimizer] with [!DNL Customer Journey Analytics] 可能會導致報表資料中因下列原因而出現某些差異：

* **兩者 [!DNL Journey Optimizer] 和 [!DNL Customer Journey Analytics] 從Azure資料湖儲存(ADLS)同步資料以進行報告。**

   產品之間傳入資料的處理時間可能稍有不同。 因此，顯示從指定日期到當天的報表時，資料可能不相符。 若要減少差異，請使用排除當天的日期範圍。

* **在 [!DNL Journey Optimizer] 報表中，已傳送量度也包含「重試」量度。**

   **[!UICONTROL 重試]** 不會包含在 **[!UICONTROL 已傳送]** 量度 [!DNL Customer Journey Analytics]. 這會導致 [!DNL Customer Journey Analytics] **[!UICONTROL 已傳送]** 顯示小於 [!DNL Journey Optimizer]. 不過，重試資料會聚合到 **[!UICONTROL 已成功發送消息]** 或 **[!UICONTROL 跳出數]** 量度。
若要減少差異，請使用一週前或更晚的日期範圍。

* **正在從不同的資料源提供報表。**

   這可能會導致產品之間1%到2%的資料差異。
