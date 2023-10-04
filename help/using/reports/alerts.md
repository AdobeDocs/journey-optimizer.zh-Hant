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
source-git-commit: 01bc2351b08fc7226c5e5633820f476c8621e404
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 1%

---

# 開始使用警示 {#alerts}

## 警示功能 {#alerting-capabilities}

您可以透過使用者介面存取系統警報，或在失敗發生時收到電子郵件。 從 **警報** 功能表，您可以檢視可用的警報並訂閱警報。 當達到您操作中的特定條件集時（例如系統違反臨界值時會發生潛在問題），系統會傳送警示訊息給組織中訂閱這些訊息的任何使用者。

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

進一步瞭解Adobe Experience Platform中的警示，位置在： [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hant){target="_blank"}.

在左側選單中的 **管理**，按一下 **警報**. 提供兩種適用於Journey Optimizer的預先設定警報： [歷程自訂動作失敗](#alert-custom-actions) 警報和 [讀取區段觸發器失敗](#alert-read-audiences) 警報。 這些警報的詳細資訊如下。

您可以從使用者介面個別訂閱每個警報，方法是選取 **訂閱** 選項來自 **警報** 儀表板。 使用相同的方法取消訂閱。

![](assets/alert-subscribe.png)

您也可以透過以下方式訂閱警報： [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}但是，警示規則會整理到不同的訂閱套件中。

如果發生非預期的行為，會傳送警示通知給訂閱者。 根據使用者偏好設定，警報會透過電子郵件傳送，或直接在使用者介面右上角的Journey Optimizer通知中心內傳送。

警報解決後，訂閱者會收到「已解決」通知。

>[!WARNING]
>
>Adobe Journey Optimizer特定警報僅適用於 **即時** 歷程。 在測試模式中，不會為歷程觸發警報。

## 歷程自訂動作失敗 {#alert-custom-actions}

如果自訂動作失敗，此警報會警告您。 我們認為在過去5分鐘內，特定自訂動作發生超過1%的錯誤時失敗。 每30秒評估一次。

![](assets/alerts-custom-action.png)

自訂動作警報會在過去5分鐘內解決：

* 該自訂動作沒有任何錯誤（或低於1%臨界值的錯誤），

* 或者，沒有任何設定檔達到該自訂動作。

與自訂動作警示相對應的I/O事件訂閱名稱為 **歷程自訂動作失敗**.

## 讀取區段觸發器失敗 {#alert-read-audiences}

此警報會在您收到 **讀取區段** 活動在排定的執行時間後10分鐘未處理任何設定檔。 此失敗可能是技術問題或對象空白所造成。

![](assets/alerts1.png)

警示開啟 **讀取區段** 活動僅適用於週期性歷程。 **讀取區段** 即時歷程中具有要執行排程的活動 **一次** 或 **儘快** 都會被忽略。

警示開啟 **讀取區段** 在設定檔進入 **讀取區段** 節點。

與對應的I/O事件訂閱名稱 **讀取區段** 警示為 **歷程讀取區段延遲、失敗和錯誤**.
