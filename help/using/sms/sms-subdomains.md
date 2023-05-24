---
solution: Journey Optimizer
product: journey optimizer
title: 配置SMS子域
description: 瞭解如何使用Journey Optimizer配置SMS子域
role: Admin
level: Intermediate
keywords: SMS、子域、配置
exl-id: 08a546d1-060c-43e8-9eac-4c38945cc3e1
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 24%

---

# 配置SMS子域 {#lp-subdomains}

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

要縮短添加到SMS消息的URL，必須設定在 [建立SMS曲面](sms-configuration.md#message-preset-sms)。

可以使用已委派給Adobe的子域，或配置其他子域。 瞭解有關將子域委託給Adobe的詳細資訊 [此部分](../configuration/delegate-subdomain.md)。

>[!CAUTION]
>
>SMS子域配置對所有環境都是通用的。 因此：
>
>* 要訪問和編輯SMS子域，您必須具有 **[!UICONTROL 管理SMS子域]** 在生產沙盒上的權限。
>
> * 對SMS子域的任何修改也會影響生產沙盒。


## 使用現有子域 {#sms-use-existing-subdomain}

要使用已委託給Adobe的子域，請執行以下步驟。

1. 訪問 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** ，然後選擇 **[!UICONTROL SMS配置]** > **[!UICONTROL SMS子域]**。

   ![](assets/sms_access-subdomains.png)

1. 按一下 **[!UICONTROL 設定子域]**。

   ![](assets/sms_set-up-subdomain.png)

1. 選擇 **[!UICONTROL 使用委託子域]** 從 **[!UICONTROL 配置類型]** 的子菜單。

   ![](assets/sms_use-delegated-subdomain.png)

1. 輸入將顯示在SMS URL中的前置詞。

   >[!NOTE]
   >
   >只允許使用字母數字字元和連字元。

1. 從清單中選擇委派的子域。

   >[!NOTE]
   >
   >不能選擇已用作SMS子域的子域。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >如果您選擇的域是使用 [CNAME方法](../configuration/delegate-subdomain.md#cname-subdomain-delegation)，必須在托管平台上建立DNS記錄。 要生成DNS記錄，該過程與配置新SMS子域時的過程相同。 瞭解 [此部分](#sms-configure-new-subdomain)。

1. 按一下&#x200B;**[!UICONTROL 提交]**。

1. 提交後，子域將顯示在清單中 **[!UICONTROL 處理]** 狀態。 有關子域狀態的詳細資訊，請參閱 [此部分](../configuration/about-subdomain-delegation.md#access-delegated-subdomains)。<!--Same statuses?-->

   >[!NOTE]
   >
   >在能夠使用該子域發送消息之前，必須等待Adobe執行所需的檢查，這可能需要4小時。<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 檢查成功後，子域將 **[!UICONTROL 成功]** 狀態。 它已準備好用於建立SMS通道曲面。

## 配置新子域 {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="產生相符的 DNS 記錄"
>abstract="若要設定新的 SMS 子網域，您需要將 Journey Optimizer 介面中顯示的 Adobe 名稱伺服器資訊複製後貼到您的網域託管解決方案中，以產生相符的 DNS 記錄。一旦檢查成功，子網域就準備好可用於建立 SMS 表面。"

要配置新子域，請執行以下步驟。

1. 訪問 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** ，然後選擇 **[!UICONTROL SMS配置]** > **[!UICONTROL SMS子域]**。

1. 按一下 **[!UICONTROL 設定子域]**。

1. 選擇 **[!UICONTROL 添加您自己的域]** 從 **[!UICONTROL 配置類型]** 的子菜單。

   ![](assets/sms_add-your-own-subdomain.png)

1. 指定要委託的子域。

   >[!CAUTION]
   >
   >不能使用現有的SMS子域。
   >
   >子域中不允許使用大寫字母。

   不允許將無效的子域委託給Adobe。 確保輸入組織擁有的有效子域，如marketing.yourcompany.com。

   >[!NOTE]
   >
   >支援多級子域（屬於同一父域）。 例如，您可以使用「sms.marketing.yourcompany.com」。

1. 將顯示要放置在DNS伺服器中的記錄。 複製此記錄，或下載CSV檔案，然後導航到域托管解決方案以生成匹配的DNS記錄。

1. 確保已在域托管解決方案中生成DNS記錄。 如果所有內容都配置正確，請選中「I confirm...（我確認……）」框，然後按一下 **[!UICONTROL 提交]**。

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >配置新SMS子域時，它始終指向CNAME記錄。

1. 提交子域委派後，子域將顯示在清單中， **[!UICONTROL 處理]** 狀態。 有關子域狀態的詳細資訊，請參閱 [此部分](../configuration/about-subdomain-delegation.md#access-delegated-subdomains)。<!--Same statuses?-->

   >[!NOTE]
   >
   >在能夠使用該子域發送SMS消息之前，必須等待Adobe執行所需的檢查，這可能需要4小時。<!--Learn more in [this section](#subdomain-validation).-->

1. 檢查成功後，子域將 **[!UICONTROL 成功]** 狀態。 它已準備好用於建立SMS通道曲面。

   請注意，子域將標籤為 **[!UICONTROL 失敗]** 如果您未能在托管解決方案上建立驗證記錄。
