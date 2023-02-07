---
solution: Journey Optimizer
product: journey optimizer
title: 警報
description: 了解如何管理警報
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: d5be5ba43351e3143fce7f64878baceb8507d7f8
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 6%

---

# 開始使用警報 {#alerts}

Journey Optimizer運用Adobe Experience Platform警報功能。 這可讓您透過使用者介面存取系統警報。 您可以檢視可用警報並訂閱警報。 當您的操作中達到某組條件時（例如，當系統違反閾值時可能出現問題），警報消息將傳送給您組織中已訂閱這些條件的任何用戶。 這些訊息可在預先定義的時間間隔內重複，直到解析警報為止。

進一步了解Adobe Experience Platform中的警報 [檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hant).
若要了解如何訂閱警報及進行設定，請參閱 [頁面](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

在左側功能表的下方 **管理**，按一下 **警報**. 提供預先設定的Journey Optimizer警報。 如果讀取段節點在定義的時間範圍內未處理任何配置檔案，則此警報將警告您。

![](assets/alerts1.png)

如果發生這種意外行為，則會通過介面右上角的電子郵件向警報的訂閱者發送警報通知。

![](assets/alerts2.png)

當 [在Adobe Experience Platform UI中檢視警報規則](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)，您可以個別訂閱每個規則。 訂閱警報時透過 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)不過，警報規則會組織成不同的訂閱套件。 與讀取區段警報對應的I/O事件訂閱名稱為：「歷程閱讀區段延遲、失敗和錯誤」。

>[!WARNING]
>
>這些警報僅適用於即時歷程。 在測試模式中，不會針對歷程觸發警報。
