---
solution: Journey Optimizer
product: journey optimizer
title: 存取及訂閱系統警示
description: 瞭解如何存取及訂閱系統警示
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 1%

---

# 存取及訂閱系統警示 {#alerts}

建立您的歷程與行銷活動時，請使用&#x200B;**警示**&#x200B;按鈕，在執行或發佈錯誤之前檢查並解決錯誤：

* 在[此頁面](../building-journeys/troubleshooting.md)瞭解如何疑難排解您的歷程。
* 瞭解如何在[此頁面](../campaigns/review-activate-campaign.md)上檢閱您的行銷活動。

從專用的&#x200B;**[!UICONTROL 警示]**&#x200B;功能表，您也可以訂閱[!DNL Adobe Journey Optimizer]個系統警示，如本頁所詳述。

## 存取警報 {#access-alerts}

發生失敗時，您可以在Journey Optimizer通知中心取得系統警報（應用程式內警報）及/或接收電子郵件。 若要存取這些警示，請遵循下列步驟。

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

>[!NOTE]
>
>在[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hant){target="_blank"}中進一步瞭解Adobe Experience Platform中的警示。

在左側功能表的&#x200B;**[!UICONTROL 管理]**&#x200B;下，按一下&#x200B;**[!UICONTROL 警示]**。 有數種預先設定的Journey Optimizer警報可供使用。

其列示如下，每個警報的詳細資訊如下。

* 歷程專屬警報：

   * [歷程自訂動作失敗](#alert-custom-actions)警報
   * [讀取對象觸發器失敗](#alert-read-audiences)警報

* 特定於通道設定的警示：

   * [AJO網域DNS記錄遺失](#alert-dns-record-missing)警報
  <!--* the [AJO channel configuration failure](#alert-channel-config-failure) alert
   * the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## 訂閱警報 {#subscribe-alerts}

1. 您可以選取&#x200B;**[!UICONTROL 訂閱]**&#x200B;選項，從使用者介面個別訂閱每個警示。

   ![](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >訂閱僅適用於特定沙箱。 您必須分別為每個沙箱訂閱警報。

1. 使用相同的方法&#x200B;**[!UICONTROL 取消訂閱]**。

1. 您也可以透過[I/O事件通知](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}訂閱警示。 警報規則會整理到不同的訂閱套件中。 與特定Journey Optimizer警示對應的事件訂閱在[底下](#journey-alerts)詳細說明。

1. 如果發生非預期的行為，和/或您的作業達到特定條件集（例如系統違反臨界值時會發生潛在問題），警示通知會傳送給組織中訂閱這些通知的任何使用者。

根據訂閱者的偏好設定，警報會透過電子郵件傳送，及/或直接在使用者介面右上角的Journey Optimizer通知中心（應用程式內通知）傳送。 選取您要如何在[!DNL Adobe Experience Cloud] **[!UICONTROL 偏好設定]**&#x200B;中接收這些警示。 [了解更多](../start/user-interface.md#in-product-alerts)

>[!NOTE]
>
>依預設，僅啟用應用程式內警報。

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.-->

警報解決後，訂閱者會收到「已解決」通知。

## 管理警報 {#manage-alerts}

若要管理警示，請選取專案並使用&#x200B;**[!UICONTROL 其他動作]**&#x200B;按鈕。

![](assets/alert-more-actions.png){width=80%}

預設會啟用所有警示。 若要停用警示，請從&#x200B;**[!UICONTROL 其他動作]**&#x200B;功能表選取&#x200B;**[!UICONTROL 停用警示]**&#x200B;選項。 此警報的所有訂閱者將不再收到相關通知。

選取&#x200B;**[!UICONTROL 管理警示訂閱者]**&#x200B;以檢視訂閱警示的使用者清單。 使用空白欄位以新增更多訂閱者。

![](assets/alert-subscribers.png){width=80%}

可能的警示狀態如下：

* **[!UICONTROL 已啟用]** — 警示已啟用，目前正在監視觸發條件。
* **[!UICONTROL 已停用]** — 警示已停用，目前未監視觸發條件。 您不會收到此警示的通知。
* **[!UICONTROL 已觸發]** — 目前符合警示的觸發條件。

## 歷程警報 {#journey-alerts}

>[!CAUTION]
>
>Adobe Journey Optimizer特定警示僅適用於&#x200B;**即時**&#x200B;歷程。 在測試模式中，不會為歷程觸發警報。

### 歷程自訂動作失敗 {#alert-custom-actions}

如果自訂動作失敗，此警報會警告您。 我們認為在過去5分鐘內，特定自訂動作發生超過1%的錯誤時失敗。 每30秒評估一次。

![](assets/alerts-custom-action.png)

自訂動作警報會在過去5分鐘內解決：

* 該自訂動作沒有任何錯誤（或低於1%臨界值的錯誤），

* 或者，沒有任何設定檔達到該自訂動作。

對應到自訂動作警示的I/O事件訂閱名稱為&#x200B;**歷程自訂動作失敗**。

若要疑難排解&#x200B;**自訂動作**&#x200B;警示：

* 使用其他歷程上的測試模式檢查您的自訂動作：

  ![](assets/alert-troubleshooting-2.png)

* 檢查您的歷程報告以檢視動作的錯誤原因。

  ![](assets/alert-troubleshooting-3.png)

* 檢查您的歷程stepEvents ，以尋找「failureReason」的詳細資訊。

* 檢查您的自訂動作設定，並驗證驗證是否仍然正常。 例如，使用Postman執行手動檢查。

### 讀取對象觸發器失敗 {#alert-read-audiences}

如果&#x200B;**讀取對象**&#x200B;活動在排定的執行時間後10分鐘未處理任何設定檔，此警報會警告您。 此失敗可能是技術問題或對象空白所造成。 如果失敗是由技術問題引起的，請注意，根據問題型別，重試仍可能發生（例如：如果匯出作業建立失敗，我們將每10mn重試一次，最長為1h）。

![](assets/alerts1.png)

有關&#x200B;**讀取對象**&#x200B;活動的警示僅適用於週期性歷程。 **在即時歷程中讀取對象**&#x200B;活動，其排程為&#x200B;**執行一次**&#x200B;或&#x200B;**儘快**&#x200B;會被忽略。

當設定檔進入&#x200B;**讀取對象**&#x200B;節點時，**讀取對象**&#x200B;上的警示已解決。

與&#x200B;**讀取對象觸發失敗**&#x200B;警示對應的I/O事件訂閱名稱為&#x200B;**歷程讀取對象延遲、失敗和錯誤**。

若要針對&#x200B;**讀取對象**&#x200B;警示進行疑難排解，請在Experience Platform介面中檢查您的對象計數。

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

## 設定警報 {#configuration-alerts}

### AJO網域DNS記錄遺失 {#alert-dns-record-missing}

當缺少正確傳遞能力設定所需的關鍵DNS記錄（NS或CNAME）或設定錯誤時，此警報會通知您。 如果沒有這些記錄，電子郵件傳遞能力可能會受到損害。

>[!NOTE]
>
>* NS記錄是委派給Adobe完整子網域所必需的。 [了解更多](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* CNAME記錄支援CNAME子網域設定。 [了解更多](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

當系統偵測到所需的NS或CNAME記錄不存在或不符合設定標準時，就會觸發&#x200B;**AJO網域DNS記錄遺失**&#x200B;警報。

1. 按一下警示以導向介面[中受影響的](../configuration/delegate-subdomain.md)子網域[!DNL Journey Optimizer]。

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. 請正確設定記錄並再次[提交子網域](../configuration/delegate-subdomain.md#submit-subdomain)委派，以修正DNS設定。

   >[!NOTE]
   >
   >在繼續之前，請確定已在您的網域託管解決方案上正確建立所有記錄。

1. 如果您不確定正確的值，可以在[!DNL Journey Optimizer]中建立與受影響子網域同名的新子網域。 [瞭解如何設定新的子網域](../configuration/delegate-subdomain.md#set-up-subdomain)

如果變更無法解決問題，第二天將再次觸發相同的警報。

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?

### AJO channel configuration failure {#alert-channel-config-failure}

>[!IMPORTANT]
>
>This alert applies only to **email** channel configurations using the [custom subdomain](../configuration/delegate-custom-subdomain.md) delegation type. ///Other channel types (such as SMS, push, or in-app) are not covered by this alert.///

This alert is triggered in case the system audit detects email channel configuration issues. These issues may include misconfigured channel settings, invalid DNS configuration, suppression list issue, IP inconsistency, or any other errors that can impact email delivery.

If you receive such an alert, the resolution steps are listed below:

1. Click the alert to be directed to the impacted [email channel configuration](../email/get-started-email-config.md) in the [!DNL Journey Optimizer] interface.

   For guidance on editing channel configurations, see [this section](../configuration/channel-surfaces.md#edit-channel-surface).

1. Review the configuration details and error messages provided. Common failure reasons include:

   * SPF validation failed
   * DKIM validation failed
   * MX record validation failed
   * Invalid DNS records

   >[!NOTE]
   >
   >The possible configuration failure reasons are listed in [this section](../configuration/channel-surfaces.md).

1. Resolve the issue:

   * Update the channel configuration as needed.
   * You may need to fix specific DNS issues mentioned in the alert.

   >[!NOTE]
   >
   >As a single domain can be associated with multiple channel configurations, resolving DNS issues for one channel configuration may automatically fix related issues across several configurations.

If the change does not resolve the issue, the same alert will be triggered again the next day.

When resolving email configuration issues, keep in mind the best practices listed below:

* Act promptly - Address configuration failures as soon as they are detected to avoid disruptions in email delivery.
* Check all configurations - If the alert indicates multiple impacted email configurations, review and fix each of them.

### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->





