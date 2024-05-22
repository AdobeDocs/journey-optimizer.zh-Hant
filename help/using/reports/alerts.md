---
solution: Journey Optimizer
product: journey optimizer
title: 警報
description: 瞭解如何管理警報
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: ddf9465fb940706fb38dc05038336ac22abecbc0
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# 開始使用警示 {#alerts}

## 存取及訂閱警報 {#alerting-capabilities}

發生失敗時，您可以在Journey Optimizer通知中心取得系統警報（應用程式內警報）及/或接收電子郵件。

從 **警報** 功能表，您可以檢視可用的警報並訂閱警報。 當達到您操作中的特定條件集時（例如系統違反臨界值時會發生潛在問題），系統會傳送警示訊息給組織中訂閱這些訊息的任何使用者。

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

進一步瞭解Adobe Experience Platform中的警示，位置在： [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hant){target="_blank"}.

在左側選單中的 **管理**，按一下 **警報**. 提供兩種適用於Journey Optimizer的預先設定警報： [歷程自訂動作失敗](#alert-custom-actions) 警報和 [讀取對象觸發器失敗](#alert-read-audiences) 警報。 這些警報的詳細資訊如下。

您可以從使用者介面個別訂閱每個警報，方法是選取 **訂閱** 選項來自 **警報** 儀表板。 使用相同的方法取消訂閱。

![](assets/alert-subscribe.png)

您也可以透過以下方式訂閱警報： [I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}. 警報規則會整理到不同的訂閱套件中。 與特定Journey Optimizer警報對應的事件訂閱詳述如下。

如果發生非預期的行為，會傳送警示通知給訂閱者。 根據使用者偏好設定，警報會透過電子郵件傳送，及/或直接在使用者介面右上角的Journey Optimizer通知中心傳送。 依預設，僅啟用應用程式內警報。 若要啟用電子郵件警示，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.

警報解決後，訂閱者會收到「已解決」通知。

>[!CAUTION]
>
>Adobe Journey Optimizer特定警報僅適用於 **即時** 歷程。 在測試模式中，不會為歷程觸發警報。

## 歷程自訂動作失敗 {#alert-custom-actions}

如果自訂動作失敗，此警報會警告您。 我們認為在過去5分鐘內，特定自訂動作發生超過1%的錯誤時失敗。 每30秒評估一次。

![](assets/alerts-custom-action.png)

自訂動作警報會在過去5分鐘內解決：

* 該自訂動作沒有任何錯誤（或低於1%臨界值的錯誤），

* 或者，沒有任何設定檔達到該自訂動作。

與自訂動作警示相對應的I/O事件訂閱名稱為 **歷程自訂動作失敗**.

## 讀取對象觸發器失敗 {#alert-read-audiences}

此警報會在您收到 **讀取對象** 活動在排定的執行時間後10分鐘未處理任何設定檔。 此失敗可能是技術問題或對象空白所造成。

![](assets/alerts1.png)

警示開啟 **讀取對象** 活動僅適用於週期性歷程。 **讀取對象** 即時歷程中具有要執行排程的活動 **一次** 或 **儘快** 都會被忽略。

警示開啟 **讀取對象** 在設定檔進入 **讀取對象** 節點。

與對應的I/O事件訂閱名稱 **讀取對象觸發器失敗** 警示為 **歷程讀取對象延遲、失敗和錯誤**.

## 疑難排解 {#alert-troubleshooting}

疑難排解 **讀取對象** 警報，在Experience Platform介面中檢查您的對象計數。

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

疑難排解 **自訂動作** 警報：

* 使用其他歷程上的測試模式檢查您的自訂動作：

  ![](assets/alert-troubleshooting-2.png)

* 檢查您的歷程報告以檢視動作的錯誤原因。

  ![](assets/alert-troubleshooting-3.png)

* 檢查您的歷程stepEvents ，以尋找「failureReason」的詳細資訊。
* 檢查您的自訂動作設定，並驗證驗證是否仍然正常。 例如，使用Postman執行手動檢查。
