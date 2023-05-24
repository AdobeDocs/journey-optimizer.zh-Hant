---
solution: Journey Optimizer
product: journey optimizer
title: 警報
description: 瞭解如何管理警報
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 1832f3395b07580e62f32c886a0a4256267b2970
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 6%

---

# 開始使用警報 {#alerts}

Journey Optimizer利用Adobe Experience Platform警報功能。 這允許您通過用戶介面訪問系統警報。 您可以檢視可用警報並訂閱警報。 

當您的操作中達到某組條件時（例如當系統違反閾值時可能出現的問題），警報消息將發送給組織中已訂閱這些條件的任何用戶。 這些消息可以在預定義的時間間隔內重複，直到警報解決。

瞭解有關Adobe Experience Platform警報的更多資訊 [文檔](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hant)。
要瞭解如何訂閱和配置警報，請參閱此 [頁](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)。

>[!AVAILABILITY]
>
>「讀取段觸發器不成功」警報的某些設計更改正在進行中，因此此警報暫時暫停，已從用戶介面中臨時刪除。 一旦這些更改發佈，警報將再次出現，您將能夠訂閱該警報。

在左菜單中，在 **管理**&#x200B;按一下 **警報**。

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

如果發生意外行為，則會通過電子郵件將警報通知發送給該警報的訂閱者，該通知位於介面右上角。

<!--![](assets/alerts2.png)-->


當 [查看Adobe Experience PlatformUI中的警報規則](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)，您可以單獨訂閱每個規則。 訂閱警報時 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)但是，警報規則被組織到不同的訂閱包中。

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
