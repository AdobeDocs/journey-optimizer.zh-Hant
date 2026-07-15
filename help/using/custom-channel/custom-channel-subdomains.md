---
title: 設定自訂管道的子網域
description: 瞭解如何使用Journey Optimizer設定自訂管道子網域
role: Admin
feature: Channel Configuration
level: Intermediate
keywords: 自訂頻道、子網域、設定
badge: label="有限可用性" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 3%

---

# 設定自訂管道子網域 {#custom-channel-subdomains}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何在Adobe Journey Optimizer中設定自訂管道子網域，以透過使用現有的委派子網域或設定具有DNS記錄的新子網域來啟用訊息中的連結追蹤。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_custom_channel"
>title="委派自訂管道子網域"
>abstract="您必須設定用於自訂頻道訊息的子網域，因為您需要此子網域來建立自訂頻道設定。 您可以使用已委派給 Adobe 的子網域，也可以設定新的子網域。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/custom-channel/custom-channel-configuration" text="設定自訂頻道"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_custom_channel_subdomain"
>title="選取自訂管道子網域"
>abstract="若要建立自訂管道設定，請確定您先前已設定至少一個自訂管道子網域，以從子網域名稱清單中挑選。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/custom-channel/custom-channel-configuration" text="設定自訂頻道"

## 開始使用自訂管道子網域 {#gs-custom-channel-subdomains}

若要在自訂頻道訊息中啟用連結追蹤，您必須設定在[建立自訂頻道設定](custom-channel-configuration.md#subdomain-delegation)時將選取的子網域。

您可以使用已委派給Adobe的子網域，或設定另一個子網域。 在[本節](../configuration/delegate-subdomain.md)中進一步瞭解將子網域委派至Adobe。

自訂管道子網域設定會在所有環境之間共用。 因此，對自訂管道子網域所做的任何修改也會影響其他生產沙箱。

<!--
TBC
>[!NOTE]
>
>To access and edit custom channel subdomains, you must have the **[!UICONTROL Manage Custom Channel Subdomains]** permission on the production sandbox. Learn more about permissions in [this section](../administration/high-low-permissions.md).
-->

## 使用現有的子網域 {#custom-channel-use-existing-subdomain}

若要使用已委派給Adobe的子網域，請遵循下列步驟。

1. 瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;功能表，並選取&#x200B;**[!UICONTROL 管道產生器]** > **[!UICONTROL 子網域]**。

   ![](assets/custom_channel_subdomains.png){width="100%"}

1. 按一下&#x200B;**[!UICONTROL 建立自訂管道子網域]**。

1. 從&#x200B;**[!UICONTROL 組態型別]**&#x200B;區段中選取&#x200B;**[!UICONTROL 使用委派的子網域]**。

   ![](assets/custom_channel_create_subdomain.png){width="100%"}

1. 輸入將顯示在自訂頻道URL中的前置詞。 只允許使用英數字元和連字型大小。

   前置詞是用來建立此自訂頻道的唯一子網域。 例如，如果您輸入`promo`並選取子網域`luma.com`，則產生的子網域將是`promo.luma.com`。

   >[!CAUTION]
   >
   >請勿使用`cdn`或`data`首碼，因為這些首碼保留供內部使用。 其他限制或保留的前置詞（例如`dmarc`或`spf`）也應避免。

1. 從清單中選取委派的子網域。

   您無法選取已用作自訂管道子網域的子網域。

   >[!CAUTION]
   >
   >如果您選取使用[CNAME方法](../configuration/delegate-subdomain.md#cname-subdomain-setup)委派給Adobe的網域，您必須在您的代管平台上建立DNS記錄。 若要產生DNS記錄，此程式與您設定新的自訂管道子網域時的程式相同。 在[本節](#custom-channel-configure-new-subdomain)中瞭解如何操作。

1. 按一下&#x200B;**[!UICONTROL 提交]**。

1. 提交後，子網域會顯示在狀態為&#x200B;**[!UICONTROL 處理中]**&#x200B;的清單中。 如需子網域狀態的詳細資訊，請參閱[本區段](../configuration/delegate-subdomain.md#access-delegated-subdomains)。

   您必須等到Adobe執行必要的檢查（最多可能需要&#x200B;**4小時**），才能使用該子網域傳送訊息。

1. 檢查成功後，子網域會取得&#x200B;**[!UICONTROL Success]**&#x200B;狀態。 它已準備好用於建立自訂通道設定。

## 設定新的子網域 {#custom-channel-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_custom_channel_subdomain_dns"
>title="產生相符的 DNS 記錄"
>abstract="若要設定新的自訂管道子網域，您需要複製Journey Optimizer介面中顯示的Adobe名稱伺服器資訊，並將其貼到您的網域託管解決方案中，以產生相符的DNS記錄。 檢查成功後，子網域即準備好用來建立自訂通道設定。"

若要設定新的子網域，請遵循下列步驟。

1. 瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;功能表，然後選取&#x200B;**[!UICONTROL 管道產生器]** > **[!UICONTROL 子網域]**。

1. 按一下&#x200B;**[!UICONTROL 建立自訂管道子網域]**。

1. 從&#x200B;**[!UICONTROL 組態型別]**&#x200B;區段中選取&#x200B;**[!UICONTROL 新增您自己的網域]**。

   ![](assets/custom_channel_new_subdomain.png){width="70%"}

1. 指定要委派的子網域。

   >[!CAUTION]
   >
   >* 您無法使用現有的自訂管道子網域。
   >
   >* 子網域中不允許使用大寫字母。

   不允許將無效的子網域委派給Adobe。 請務必輸入貴組織所擁有的有效子網域，例如marketing.yourcompany.com。

   支援（相同父項網域的）多階層子網域。 例如，您可以使用「custom.marketing.yourcompany.com」。

1. 將會顯示要放置在DNS伺服器中的記錄。 複製此記錄或下載CSV檔案，然後導覽至您的網域託管解決方案，以產生相符的DNS記錄。

1. 請確定已在您的網域託管解決方案中產生DNS記錄。 如果所有專案皆已正確設定，請勾選「我確認……」方塊，然後按一下&#x200B;**[!UICONTROL 提交]**。

   ![](assets/custom_channel_new_subdomain_confirm.png)

   當您設定新的自訂管道子網域時，它始終指向CNAME記錄。

1. 提交子網域委派後，子網域會顯示在狀態為&#x200B;**[!UICONTROL 處理中]**&#x200B;的清單中。 如需子網域狀態的詳細資訊，請參閱[本區段](../configuration/delegate-subdomain.md#access-delegated-subdomains)。

使用子網域傳送自訂頻道訊息之前，您必須等待Adobe執行所需檢查，最多可能需要4小時。 檢查成功後，子網域會取得&#x200B;**[!UICONTROL Success]**&#x200B;狀態。 它已準備好用於建立自訂通道設定。

請注意，如果您無法在託管解決方案上建立驗證記錄，子網域將會標示為&#x200B;**[!UICONTROL 失敗]**。

<!--

Any specific guardrails to add? If so, can we link to email subdomain guardrails? journey-optimizer.en/help/using/configuration/delegate-subdomain.md#guardrails

Otherwise use the following from SMS subdomains?

## Guardrails {#guardrails}

Currently, the [!DNL Journey Optimizer] user interface does not support the deletion or undelegation of custom channel subdomains once they have been set up.

However, when testing features within [!DNL Journey Optimizer], it may be necessary to create a custom channel subdomain. Once the testing is complete, this can lead to cluttered environments with unnecessary configurations as the UI does not allow for removing or undelegating custom channel subdomains.

Here are some recommended steps and considerations:

* As a best practice, maintain a tidy environment by only creating necessary components and configurations.
* In situations where there is a business impact, contact your Adobe representative who may be able to assist with the removal/undelegation of the custom channel subdomain. [Learn more](#undelegate-subdomain)
* If further assistance is required, reach out to Adobe for guidance on managing your instance effectively.

## Undelegate a subdomain {#undelegate-subdomain}

If you wish to undelegate a custom channel subdomain, reach out to your Adobe representative with the subdomain you want to undelegate.

If the custom channel subdomain points to a CNAME record, you can delete the CNAME DNS record that you created for the custom channel subdomain from your hosting solution (but do not delete the original email subdomain if any).

>[!NOTE]
>
>A custom channel subdomain can point to a CNAME record because it was either an [existing subdomain](#custom-channel-use-existing-subdomain) delegated to Adobe using the [CNAME method](../configuration/delegate-subdomain.md#cname-subdomain-setup), or a [new custom channel subdomain](#custom-channel-configure-new-subdomain) that you configured.

After your request is handled by Adobe, the undelegated domain is no longer displayed on the subdomain inventory page.
-->


## 後續步驟 {#next-steps}

* [建立管道設定](custom-channel-configuration.md)，將您的自訂管道連結至行銷人員將在行銷活動和歷程中選取的子網域、認證和裝載預設值。
