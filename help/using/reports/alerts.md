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
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# 開始使用警示 {#alerts}

建立您的歷程與行銷活動時，請使用&#x200B;**警示**&#x200B;按鈕，在執行或發佈錯誤之前檢查並解決錯誤。 在[此頁面](../building-journeys/troubleshooting.md)瞭解如何疑難排解您的歷程。 在[此頁面](../campaigns/review-activate-campaign.md)瞭解如何檢閱您的行銷活動。

您也可以訂閱Adobe Journey Optimizer系統警示，如本頁所述。

## 存取及訂閱警報 {#alerting-capabilities}

發生失敗時，您可以在Journey Optimizer通知中心取得系統警報（應用程式內警報）及/或接收電子郵件。

您可以從&#x200B;**警示**&#x200B;功能表檢視可用的警示並訂閱警示。 當達到您操作中的特定條件集時（例如系統違反臨界值時會發生潛在問題），系統會傳送警示訊息給組織中訂閱這些訊息的任何使用者。

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

在[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hant){target="_blank"}中進一步瞭解Adobe Experience Platform中的警示。

在左側功能表的&#x200B;**管理**&#x200B;下，按一下&#x200B;**警示**。 有兩個Journey Optimizer預先設定的警報可供使用： [歷程自訂動作失敗](#alert-custom-actions)警報和[讀取對象觸發器失敗](#alert-read-audiences)警報。 這些警報的詳細資訊如下。

您可以從&#x200B;**警報**&#x200B;儀表板選取&#x200B;**訂閱**&#x200B;選項，從使用者介面個別訂閱每個警報。 使用相同的方法取消訂閱。

![](assets/alert-subscribe.png)

您也可以透過[I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}訂閱警示。 警報規則會整理到不同的訂閱套件中。 與特定Journey Optimizer警報對應的事件訂閱詳述如下。

如果發生非預期的行為，會傳送警示通知給訂閱者。 根據使用者偏好設定，警報會透過電子郵件傳送，及/或直接在使用者介面右上角的Journey Optimizer通知中心傳送。 依預設，僅啟用應用程式內警報。 若要啟用電子郵件警示，請參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}。

警報解決後，訂閱者會收到「已解決」通知。

>[!CAUTION]
>
>Adobe Journey Optimizer特定警示僅適用於&#x200B;**即時**&#x200B;歷程。 在測試模式中，不會為歷程觸發警報。

## 歷程自訂動作失敗 {#alert-custom-actions}

如果自訂動作失敗，此警報會警告您。 我們認為在過去5分鐘內，特定自訂動作發生超過1%的錯誤時失敗。 每30秒評估一次。

![](assets/alerts-custom-action.png)

自訂動作警報會在過去5分鐘內解決：

* 該自訂動作沒有任何錯誤（或低於1%臨界值的錯誤），

* 或者，沒有任何設定檔達到該自訂動作。

對應到自訂動作警示的I/O事件訂閱名稱為&#x200B;**歷程自訂動作失敗**。

## 讀取對象觸發器失敗 {#alert-read-audiences}

如果&#x200B;**讀取對象**&#x200B;活動在排定的執行時間後10分鐘未處理任何設定檔，此警報會警告您。 此失敗可能是技術問題或對象空白所造成。

![](assets/alerts1.png)

有關&#x200B;**讀取對象**&#x200B;活動的警示僅適用於週期性歷程。 **在即時歷程中讀取對象**&#x200B;活動，其排程為&#x200B;**執行一次**&#x200B;或&#x200B;**儘快**&#x200B;會被忽略。

當設定檔進入&#x200B;**讀取對象**&#x200B;節點時，**讀取對象**&#x200B;上的警示已解決。

與&#x200B;**讀取對象觸發失敗**&#x200B;警示對應的I/O事件訂閱名稱為&#x200B;**歷程讀取對象延遲、失敗和錯誤**。

## 疑難排解 {#alert-troubleshooting}

若要疑難排解&#x200B;**讀取對象**&#x200B;警示，請在Experience Platform介面中檢查您的對象計數。

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

若要疑難排解&#x200B;**自訂動作**&#x200B;警示：

* 使用其他歷程上的測試模式檢查您的自訂動作：

  ![](assets/alert-troubleshooting-2.png)

* 檢查您的歷程報告以檢視動作的錯誤原因。

  ![](assets/alert-troubleshooting-3.png)

* 檢查您的歷程stepEvents ，以尋找「failureReason」的詳細資訊。

* 檢查您的自訂動作設定，並驗證驗證是否仍然正常。 例如，使用Postman執行手動檢查。
