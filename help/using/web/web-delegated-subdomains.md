---
solution: Journey Optimizer
product: journey optimizer
title: 設定網頁子網域
description: 瞭解如何使用Journey Optimizer設定網頁子網域
role: Admin
feature: Web Channel, Subdomains
level: Experienced
keywords: Web、子網域、設定
exl-id: 6e00466d-4ce5-4d80-89ff-c7331a5ab158
source-git-commit: ce8818e0216d4f633770fecadd4e74c2651a62f3
workflow-type: tm+mt
source-wordcount: '1075'
ht-degree: 20%

---

# 設定網頁子網域 {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="委派網頁子網域"
>abstract="您將設定您的子網域以供網頁管道使用。您可以使用已委派給 Adobe 的子網域，或設定另一個子網域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="委派網頁子網域"
>abstract="如果您將來自 Adobe Experience Manager Assets 的內容新增到您的網頁體驗中，則必須設定將用來發佈此內容的子網域。選取已委派給 Adobe 的子網域，或設定新的子網域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="設定網頁子網域"
>abstract="從已委派給 Adobe 的子網域清單中選取一個子網域。您可以將此網頁子網域設定為預設子網域，但一次只能使用一個預設子網域。"

編寫網頁體驗時，如果您新增來自[Adobe Experience Manager Assets](../integrations/assets.md)資料庫的內容，則必須設定用於發佈此內容的子網域。

您可以使用已委派給Adobe的子網域，也可以設定另一個子網域。 在[本節](../configuration/delegate-subdomain.md)中進一步瞭解將子網域委派至Adobe。

Web子網域設定是&#x200B;**所有環境通用的設定**。 因此：

* 要訪問和编辑 Web 子域，您必須在生產沙盒上具有“ **[!UICONTROL 管理 Web 子域]** ”權限。

* 對 Web 子域的任何修改也會影響生產沙箱。

您可以建立多個網路子域，但只會 **使用預設** 子域。 您可以變更預設的 Web 子域，但一次只能使用一個子域。

## 存取及管理Web子網域 {#access-web-subdomains}

1. 移至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;功能表，然後選取&#x200B;**[!UICONTROL 網頁設定]** > **[!UICONTROL 網頁子網域]**。 會顯示使用目前沙箱設定的所有子網域。

   ![](assets/web-access-subdomains.png)

1. 您可以篩選委派每個子網域的使用者或其中一個委派狀態（**[!UICONTROL 草稿]**、**[!UICONTROL 正在處理]**、**[!UICONTROL 成功]**&#x200B;或&#x200B;**[!UICONTROL 失敗]**）。

   ![](assets/web-filter-subdomains.png)

1. **[!UICONTROL 預設]**&#x200B;徽章會顯示在目前作為預設的子網域旁邊。 若要變更預設子網域，請從所要子網域旁的&#x200B;**[!UICONTROL 更多動作]**&#x200B;按鈕中選取&#x200B;**[!UICONTROL 設定為預設值]**。

   ![](assets/web-subdomain-default.png)

   您可以變更預設的 Web 子域，但一次只能使用一個子域。

## 使用現有子域 {#web-use-existing-subdomain}

要使用已委派給Adobe Systems的子域，請追隨以下步驟。

1. 存取&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;功能表，然後選取&#x200B;**[!UICONTROL 網頁設定]** > **[!UICONTROL 網頁子網域]**。

1. 按一下&#x200B;**[!UICONTROL 設定子網域]**。

1. 從&#x200B;**[!UICONTROL 組態型別]**&#x200B;區段中選取&#x200B;**[!UICONTROL 使用委派的子網域]**&#x200B;選項，並從清單中選擇委派的子網域。

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >您無法選取已用作Web子網域的子網域。

1. 將會在網頁URL中顯示的前置詞會自動新增。 您無法加以變更。

1. 若要將此子網域設定為預設值，請選取對應的選項。

   ![](assets/web-subdomain-details-default.png)

   只會使用&#x200B;**預設**&#x200B;子網域。

1. 按一下&#x200B;**[!UICONTROL 提交]**。 子網域取得&#x200B;**[!UICONTROL Success]**&#x200B;狀態。 它可供您的網頁體驗使用。

   在極少數的情況下，子網域設定可能會失敗。 在此情況下，您可以刪除&#x200B;**[!UICONTROL 失敗]**&#x200B;子網域，以使用&#x200B;**[!UICONTROL 更多動作]**&#x200B;圖示中的&#x200B;**[!UICONTROL 刪除]**&#x200B;按鈕來清除清單。

## 設定新的子網域 {#web-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_web_subdomain_dns"
>title="產生相符的 DNS 記錄"
>abstract="若要設定新的 Web 子網域，您需要將 Journey Optimizer 介面中顯示的 Adobe 名稱伺服器資訊複製後貼到您的網域託管解決方案中，以產生相符的 DNS 記錄。檢查成功後，子網域即可用於發佈來自 Adobe Experience Manager Assets 資料庫的內容。"


默認情況下， [!DNL Journey Optimizer] 最多允許您委派 **10 個子域** （涵蓋電子郵件和 Web 管道）。 然而，根據您的授權合約，您最多可委派 100 個子網域。 請聯絡您的 Adobe 聯絡人，了解更多您有權使用的子網域數量。

要配置新的子域，追隨以下步驟：

1. 訪問“**[!UICONTROL 管理]**”>**[!UICONTROL “]**&#x200B;通道”功能表，然後選擇&#x200B;**[!UICONTROL “Web 設置”>**[!UICONTROL “Web 子&#x200B;]**域]**”。

1. 點擊 **[!UICONTROL 設置子域]**。

1. 從「配置類型&#x200B;]**」部分中選擇「**[!UICONTROL &#x200B;添加自己的域&#x200B;]**」。。**[!UICONTROL 

1. 指定要委派的子域。

   >[!CAUTION]
   >
   >* 您無法使用現有的Web子網域。
   >
   >* 子網域中不允許使用大寫字母。

   ![](assets/web-add-your-own-domain.png)

   不允許將無效的子網域委派給Adobe。 請務必輸入貴組織所擁有的有效子網域，例如marketing.yourcompany.com。

   支援（相同父項網域的）多階層子網域。 例如，您可以使用「web.marketing.yourcompany.com」。

1. 若要將此子網域設定為預設值，請選取對應的選項。

   >[!NOTE]
   >
   >**只會使用預設**&#x200B;子域。

1. 將顯示要放置在 DNS 伺服器中的記錄。 複製此記錄或下載CSV文件，然後導航到域託管解決方案以生成匹配的 DNS 記錄。

1. 請確保已將 DNS 記錄生成到您的域託管解決方案中。 如果一切配置正確，請選中“我確認...”框，然後按下 **[!UICONTROL 提交]**。

   ![](assets/web-add-your-own-domain-confirm.png)

   當您設定新的 Web 子域時，它始終指向 CNAME 記錄。

1. 提交子網域委派後，子網域會顯示在狀態為&#x200B;**[!UICONTROL 處理中]**&#x200B;的清單中。 如需子網域狀態的詳細資訊，請參閱[本區段](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   在能夠使用該子域發送 Web 消息之前，您必須等到 Adobe Systems 執行所需的檢查，這最多可能需要 **4 小時**。

1. 檢查成功後，子網域會取得&#x200B;**[!UICONTROL Success]**&#x200B;狀態。 它已準備好用於建立Web Channel設定。

   請注意，如果您無法在託管解決方案上建立驗證記錄，子網域將會標示為&#x200B;**[!UICONTROL 失敗]**。

<!--
Only a subdomain with the **[!UICONTROL Success]** status can be set as default.
You cannot delete a subdomain with the **[!UICONTROL Processing]** status.
-->

## 取消委派子域 {#undelegate-subdomain}

如果您想要取消委派網頁子網域，請聯絡您的Adobe代表。

不過，在聯絡Adobe之前，您需要在使用者介面中執行數個步驟。

>[!NOTE]
>
>您只能取消委派狀態為&#x200B;**[!UICONTROL 成功]**&#x200B;的子網域。 可以從使用者介面中刪除具有&#x200B;**[!UICONTROL 草稿]**&#x200B;和&#x200B;**[!UICONTROL 失敗]**&#x200B;狀態的子網域。

首先，在[!DNL Journey Optimizer]中執行下列步驟：

1. 停用與子網域相關聯的所有管道設定。 [了解作法](../configuration/channel-surfaces.md#deactivate-a-surface)

<!--
1. If the web subdomain is using an email subdomain that was [already delegated](#lp-use-existing-subdomain) to Adobe, undelegate the email subdomain. [Learn how](../configuration/delegate-subdomain.md#undelegate-subdomain)-->

1. 停止與子網域相關聯的作用中行銷活動。 [了解作法](../campaigns/modify-stop-campaign.md#stop)

1. 停止與子網域相關聯的使用中歷程。 [了解作法](../building-journeys/end-journey.md#stop-journey)

1. 如果Web子網域是[新的委派子網域](#web-configure-new-subdomain)，請移除與該子網域相關聯的DNS專案。

完成後，請聯絡您的Adobe代表，提供您要取消委派的子網域。

Adobe Systems處理請求后，未委派的域將不再显示在子域清單頁面上。

>[!CAUTION]
>
>取消委派子域后：
>
>   * 您無法重新啟用使用該子域的通道配置。
>
>   * 您無法透過使用者介面再次委派確切的子網域。 如果您想這樣做，請聯繫您的Adobe 代表。