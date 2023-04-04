---
solution: Journey Optimizer
product: journey optimizer
title: 設定SMS子網域
description: 了解如何使用Journey Optimizer設定SMS子網域
role: Admin
level: Intermediate
keywords: SMS，子網域，設定
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 24%

---

# 設定SMS子網域 {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="委派 SMS 子網域"
>abstract="您將設定您的子網域以供 SMS 使用。您可以使用已委派給 Adobe 的子網域，或設定另一個子網域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="委派 SMS 子網域"
>abstract="您必須設定要用於 SMS 訊息的子網域，因為您需要此子網域才能建立 SMS 表面。您可以使用已委派給 Adobe 的子網域，或設定新的子網域。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="建立 SMS 表面"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="選取 SMS 子網域"
>abstract="為了能夠建立 SMS 表面，請確保您之前已設定了至少一個 SMS 子網域，才能從子網域名稱清單中挑選。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="建立 SMS 表面"

若要縮短新增至SMS訊息的URL，您必須設定要在 [建立SMS表面](sms-configuration.md#message-preset-sms).

您可以使用已委派給Adobe的子網域，或可以設定其他子網域。 進一步了解如何將子網域委派至Adobe [本節](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>SMS子網域設定是所有環境通用的。 因此：
>
>* 若要存取及編輯SMS子網域，您必須具備 **[!UICONTROL 管理SMS子網域]** 對生產沙箱的權限。
>
> * 對SMS子網域進行任何修改也會影響生產沙箱。


## 使用現有的子網域 {#sms-use-existing-subdomain}

若要使用已委派給Adobe的子網域，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** ，然後選取 **[!UICONTROL SMS設定]** > **[!UICONTROL SMS子網域]**.

   ![](assets/sms_access-subdomains.png)

1. 按一下 **[!UICONTROL 設定子網域]**.

   ![](assets/sms_set-up-subdomain.png)

1. 選擇 **[!UICONTROL 使用委派的子網域]** 從 **[!UICONTROL 配置類型]** 區段。

   ![](assets/sms_use-delegated-subdomain.png)

1. 輸入會在您的SMS URL中顯示的首碼。

   >[!NOTE]
   >
   >只允許使用英數字元和連字型大小。

1. 從清單中選取委派的子網域。

   >[!NOTE]
   >
   >您無法選取已作為SMS子網域的子網域。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >如果您選取了委派給Adobe的網域，使用 [CNAME方法](../configuration/delegate-subdomain.md#cname-subdomain-delegation)，您必須在托管平台上建立DNS記錄。 若要產生DNS記錄，程式與設定新SMS子網域時的程式相同。 了解 [本節](#sms-configure-new-subdomain).

1. 按一下&#x200B;**[!UICONTROL 提交]**。

1. 提交後，子網域會顯示在清單中，且包含 **[!UICONTROL 處理]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >在能夠使用該子網域來傳送訊息之前，您必須等到Adobe執行所需的檢查，這最多需要4小時。<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 它已可用來建立SMS通道表面。

## 設定新子網域 {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="產生相符的 DNS 記錄"
>abstract="若要設定新的 SMS 子網域，您需要將 Journey Optimizer 介面中顯示的 Adobe 名稱伺服器資訊複製後貼到您的網域託管解決方案中，以產生相符的 DNS 記錄。一旦檢查成功，子網域就準備好可用於建立 SMS 表面。"

若要設定新子網域，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** ，然後選取 **[!UICONTROL SMS設定]** > **[!UICONTROL SMS子網域]**.

1. 按一下 **[!UICONTROL 設定子網域]**.

1. 選擇 **[!UICONTROL 新增您自己的網域]** 從 **[!UICONTROL 配置類型]** 區段。

   ![](assets/sms_add-your-own-subdomain.png)

1. 指定要委派的子網域。

   >[!CAUTION]
   >
   >您無法使用現有的SMS子網域。
   >
   >子網域中不允許使用大寫字母。

   不允許將無效的子網域委派至Adobe。 請務必輸入貴組織擁有的有效子網域，例如marketing.yourcompany.com。

   >[!NOTE]
   >
   >支援多層級子網域（屬於相同的上層網域）。 例如，您可以使用「sms.marketing.yourcompany.com」。

1. 將顯示要放置在DNS伺服器中的記錄。 複製此記錄或下載CSV檔案，然後導覽至您的網域托管解決方案，以產生相符的DNS記錄。

1. 請確定已在您的網域托管解決方案中產生DNS記錄。 如果所有項目皆已正確設定，請核取「I confirm...」方塊，然後按一下 **[!UICONTROL 提交]**.

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >當您設定新的SMS子網域時，它一律會指向CNAME記錄。

1. 提交子網域委派後，子網域會顯示在清單中，並搭配 **[!UICONTROL 處理]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >在能夠使用該子網域傳送SMS訊息之前，您必須等到Adobe執行所需的檢查，最多需要4小時。<!--Learn more in [this section](#subdomain-validation).-->

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 它已可用來建立SMS通道表面。

   請注意，子網域將標示為 **[!UICONTROL 失敗]** 如果您未在托管解決方案上建立驗證記錄。
