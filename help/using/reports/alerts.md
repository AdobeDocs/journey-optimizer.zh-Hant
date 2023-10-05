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
source-git-commit: 6386a5ee5a0d1f221beab67f43636c599531736a
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 4%

---

# 開始使用警示 {#alerts}

Journey Optimizer運用Adobe Experience Platform警報功能。 這可讓您透過使用者介面存取系統警示。 您可以檢視可用警報並訂閱警報。 

當達到您操作中的特定條件集時（例如系統違反臨界值時會發生潛在問題），系統會傳送警示訊息給組織中訂閱這些訊息的任何使用者。

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

進一步瞭解Adobe Experience Platform中的警示 [檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hant).

若要瞭解如何訂閱及設定警報，請參閱本 [頁面](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>「讀取對象觸發器失敗」警報的部分設計變更進行中，因此此警報暫時暫停，並暫時從使用者介面移除。 這些變更發佈後，警報將再次顯示，您可以訂閱它。

在左側選單中的 **管理**，按一下 **警報**. 適用於Journey Optimizer的預先設定警報可供使用。 如果自訂動作失敗，此警報會警告您。 我們認為在過去5分鐘內，特定自訂動作發生超過1%的錯誤時失敗。 每30秒評估一次。

![](assets/alerts-custom-action.png)


<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

如果發生非預期的行為，系統會根據使用者偏好設定，透過電子郵件或直接在介面右上角的Journey Optimizer中，將警報通知傳送給警報的訂閱者。

警報解決後，您會收到「已解決」通知。 對於自訂動作警報，發生此狀況有兩個原因：
* 在過去5分鐘內，該自訂動作沒有任何錯誤（或低於1%臨界值的錯誤）。
* 沒有設定檔達到該自訂動作。

時間 [在Adobe Experience Platform UI中檢視警報規則](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html)，您可以個別訂閱每個規則。 透過訂閱警報時 [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)但是，警示規則會整理到不同的訂閱套件中。 與自訂動作警報相對應的I/O事件訂閱名稱為：「歷程自訂動作失敗」。

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".-->

>[!WARNING]
>
>這些警報僅適用於即時歷程。 在測試模式中的歷程不會觸發警報。

