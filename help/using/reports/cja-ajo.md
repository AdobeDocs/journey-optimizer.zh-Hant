---
title: 使用Customer Journey Analytics
description: 開始使用Customer Journey Analytics
feature: Overview
topic: Reporting
role: User
level: Beginner
source-git-commit: b7bda87c3e2d6e1841ca231aa4acc3a406655244
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 9%

---

# 使用 [!DNL Customer Journey Analytics] {#cja-ajo}

![](assets/cja.png)

在中建立您的歷程後 [!DNL Journey Optimizer]，您可以將客戶資料匯入 [!DNL Customer Journey Analytics] 以開始報告並了解客戶與您歷程的每次互動的影響。

➡️ [DiscoverCustomer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target=&quot;_blank&quot;}

使用前 [!DNL Customer Journey Analytics] 對於您的歷程，您必須先設定此整合：

1. [建立連線](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html) in [!DNL Customer Journey Analytics] 和 **[!UICONTROL 資料集]** 您要傳送至平台。

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
