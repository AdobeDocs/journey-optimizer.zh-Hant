---
title: 設定登陸頁面子網域
description: 了解如何使用Journey Optimizer設定登錄頁面子網域
role: Admin
level: Intermediate
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 1%

---

# 設定登陸頁面子網域 {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp_header"
>title="委派登錄頁面子網域"
>abstract="您將設定您的子網域以供登錄頁面使用。 您可以使用已委派給Adobe的子網域，或設定其他子網域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="委派登錄頁面子網域"
>abstract="您必須設定要用於登錄頁面的子網域，因為您需要此子網域才能建立登錄頁面預設集。 您可以使用已委派給Adobe的子網域，或設定新的子網域。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="建立登錄頁面預設集"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="建立登錄頁面預設集"
>abstract="若要建立登錄頁面預設集，請確定您先前已設定至少一個要從子網域名稱清單挑選的登錄頁面子網域。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="建立登錄頁面預設集"

才能 [建立登錄頁面預設集](lp-presets.md)，您必須設定要用於登錄頁面的子網域。

您可以使用已委派給Adobe的子網域，或可以設定其他子網域。 進一步了解如何將子網域委派至Adobe [本節](delegate-subdomain.md).

## 使用現有的子網域 {#lp-use-existing-subdomain}

若要使用已委派給Adobe的子網域，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** ，然後選取 **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 登陸頁面子網域]**.

   ![](assets/lp_access-subdomains.png)

1. 按一下 **[!UICONTROL 設定子網域]**.

   ![](assets/lp_set-up-subdomain.png)

1. 選擇 **[!UICONTROL 使用委派的網域]** 從 **[!UICONTROL 配置類型]** 區段。

   ![](assets/lp_use-delegated-subdomain.png)

1. 輸入將在登錄頁面URL中顯示的首碼。

   >[!NOTE]
   >
   >只允許使用英數字元和連字型大小。

1. 從清單中選取委派的子網域。

   >[!NOTE]
   >
   >您無法選取已用作登錄頁面子網域的子網域。

   ![](assets/lp_prefix-and-subdomain.png)

   請注意，您無法使用相同上層網域的多個委派子網域。 例如，如果已將「marketing1.yourcompany.com」委派給登錄頁面的Adobe，則您將無法使用「marketing2.yourcompany.com」。 不過，登陸頁面支援的多層級子網域，您可以使用&#39;marketing1.yourcompany.com&#39;（例如&#39;email.marketing1.yourcompany.com&#39;）的子網域或不同的上層網域繼續操作。

   >[!CAUTION]
   >
   >如果您選取了委派給Adobe的網域，使用 [CNAME方法](delegate-subdomain.md#cname-subdomain-delegation)，您必須在托管平台上建立DNS記錄。 若要產生DNS記錄，程式與您設定新登錄頁面子網域時的程式相同。 了解 [本節](#lp-configure-new-subdomain).

1. 按一下&#x200B;**[!UICONTROL 提交]**。

1. 提交後，子網域會顯示在清單中，且包含 **[!UICONTROL 處理]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](access-subdomains.md).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >在能夠使用該子網域來傳送訊息之前，您必須等到Adobe執行所需的檢查，這最多需要4小時。<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 它已可用來建立登錄頁面預設集。

## 設定新子網域 {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="生成匹配的DNS記錄"
>abstract="若要設定新的登錄頁面子網域，您必須複製Journey Optimizer介面中顯示的Adobe名稱伺服器資訊，並貼到您的網域托管解決方案中，以產生相符的DNS記錄。 檢查成功後，子網域即可供用來建立登錄頁面預設集。"

若要設定新子網域，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** ，然後選取 **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 登陸頁面子網域]**.

1. 按一下 **[!UICONTROL 設定子網域]**.

1. 選擇 **[!UICONTROL 新增您自己的網域]** 從 **[!UICONTROL 配置類型]** 區段。

   ![](assets/lp_add-your-own-subdomain.png)

1. 指定要委派的子網域。

   >[!CAUTION]
   >
   >您無法使用現有的登錄頁面子網域。

   不允許將無效的子網域委派至Adobe。 請務必輸入貴組織擁有的有效子網域，例如marketing.yourcompany.com。

   >[!NOTE]
   >
   >若為登錄頁面，則支援多層級子網域。 例如，您可以使用「email.marketing.yourcompany.com」。

1. 將顯示要放置在DNS伺服器中的記錄。 複製此記錄或下載CSV檔案，然後導覽至您的網域托管解決方案，以產生相符的DNS記錄。

1. 請確定已在您的網域托管解決方案中產生DNS記錄。 如果所有項目皆已正確設定，請核取「I confirm...」方塊，然後按一下 **[!UICONTROL 提交]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >當您設定新的登錄頁面子網域時，它一律會指向CNAME記錄。

1. 提交子網域委派後，子網域會顯示在清單中，並搭配 **[!UICONTROL 處理]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](access-subdomains.md).<!--Same statuses?-->

   >[!NOTE]
   >
   >在能夠使用該子網域來傳送訊息之前，您必須等到Adobe執行所需的檢查，這最多需要4小時。<!--Learn more in [this section](#subdomain-validation).-->

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 它已可用來建立登錄頁面預設集。

   請注意，子網域將標示為 **[!UICONTROL 失敗]** 如果您未在托管解決方案上建立驗證記錄。
