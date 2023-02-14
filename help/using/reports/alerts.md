---
solution: Journey Optimizer
product: journey optimizer
title: 警報
description: 了解如何管理警報
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 46fe345d424a5a201cf75a8ee0e2035bc68621fe
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 開始使用警報 {#alerts}

Journey Optimizer運用Adobe Experience Platform警報功能。 這可讓您透過使用者介面存取系統警報。 您可以檢視可用警報並訂閱警報。 

當您的操作中達到某組條件時（例如，當系統違反閾值時可能出現問題），警報消息將傳送給您組織中已訂閱這些條件的任何用戶。 這些訊息可在預先定義的時間間隔內重複，直到解析警報為止。

進一步了解Adobe Experience Platform中的警報 [檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hant).
若要了解如何訂閱警報及進行設定，請參閱 [頁面](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>「讀取區段觸發器失敗」警報的部分設計變更正在進行中，因此此警報暫時暫停。 變更發佈後，此警報會再次呈現，您便能訂閱。

在左側功能表的下方 **管理**，按一下 **警報**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

如果發生非預期的行為，則會透過介面右上角的電子郵件，傳送警報通知給警報的訂閱者。

<!--![](assets/alerts2.png)-->


當 [在Adobe Experience Platform UI中檢視警報規則](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)，您可以個別訂閱每個規則。 訂閱警報時透過 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)不過，警報規則會組織成不同的訂閱套件。

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
