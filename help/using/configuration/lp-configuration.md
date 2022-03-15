---
title: 登錄頁配置
description: 瞭解如何配置環境以建立和使用登錄頁與Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 2cee54221871979bb1ae2c8b7990debe1c80ce67
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 2%

---

# 設定登陸頁面 {#lp-configuration}

## 配置登錄頁子域 {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="建立登錄頁預設"
>abstract="要能夠建立登錄頁預設，請確保您以前至少配置了一個登錄頁子域，以便從 **子域名** 清單框。"

能夠 [建立登錄頁預設](#lp-create-preset)，您必須設定用於登錄頁的子域。

可以使用已委派給Adobe的子域，或配置其他子域。 瞭解有關將子域委託給Adobe的詳細資訊 [此部分](delegate-subdomain.md)。

### 使用現有子域 {#lp-use-existing-subdomain}

要使用已委託給Adobe的子域，請執行以下步驟。

1. 訪問 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** ，然後選擇 **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**。

   ![](assets/lp_access-subdomains.png)

1. 按一下「**[!UICONTROL Set up subdomain]**」。

   ![](assets/lp_set-up-subdomain.png)

1. 選擇 **[!UICONTROL Use delegated domain]** 從 **[!UICONTROL Configuration type]** 的子菜單。

   ![](assets/lp_use-delegated-subdomain.png)

1. 輸入將在登錄頁URL中顯示的前置詞。

   >[!NOTE]
   >
   >只允許使用字母數字字元和連字元。

1. 從清單中選擇委派的子域。

   >[!NOTE]
   >
   >不能選擇已用作登錄頁子域的子域。

   ![](assets/lp_prefix-and-subdomain.png)

   >[!CAUTION]
   >
   >如果您選擇的域是使用 [CNAME方法](delegate-subdomain.md#cname-subdomain-delegation)，必須在托管平台上建立DNS記錄。 要生成DNS記錄，該過程與配置新登錄頁子域時的過程相同。 瞭解 [此部分](#lp-configure-new-subdomain)。

1. 按一下「**[!UICONTROL Submit]**」。

1. 提交後，子域將顯示在清單中 **[!UICONTROL Processing]** 狀態。 有關子域狀態的詳細資訊，請參閱 [此部分](access-subdomains.md)。<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >在能夠使用該子域發送消息之前，必須等待Adobe執行所需的檢查，這可能需要4小時。<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. 檢查成功後，子域將 **[!UICONTROL Success]** 狀態。 它已準備好用於建立登錄頁預設。

### 配置新子域 {#lp-configure-new-subdomain}

要配置新子域，請執行以下步驟。

1. 訪問 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** ，然後選擇 **[!UICONTROL Email configuration]** > **[!UICONTROL Landing page subdomains]**。

1. 按一下「**[!UICONTROL Set up subdomain]**」。

1. 選擇 **[!UICONTROL Add your own domain]** 從 **[!UICONTROL Configuration type]** 的子菜單。

   ![](assets/lp_add-your-own-subdomain.png)

1. 指定要委託的子域。

   >[!CAUTION]
   >
   >不能使用現有登錄頁子域。

   不允許將無效的子域委託給Adobe。 確保輸入組織擁有的有效子域，如marketing.yourcompany.com。

   當前不支援「email.marketing.yourcompany.com」等多級子域。

1. 將顯示要放置在DNS伺服器中的記錄。 複製此記錄，或下載CSV檔案，然後導航到域托管解決方案以生成匹配的DNS記錄。

1. 確保已在域托管解決方案中生成DNS記錄。 如果所有內容都配置正確，請選中「I confirm...（我確認……）」框，然後按一下 **[!UICONTROL Submit]**。

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >配置新登錄頁子域時，它始終指向CNAME記錄。

1. 提交子域委派後，子域將顯示在清單中， **[!UICONTROL Processing]** 狀態。 有關子域狀態的詳細資訊，請參閱 [此部分](access-subdomains.md)。<!--Same statuses?-->

   >[!NOTE]
   >
   >在能夠使用該子域發送消息之前，必須等待Adobe執行所需的檢查，這可能需要4小時。<!--Learn more in [this section](#subdomain-validation).-->

1. 檢查成功後，子域將 **[!UICONTROL Success]** 狀態。 它已準備好用於建立登錄頁預設。

   請注意，子域將標籤為 **[!UICONTROL Failed]** 如果您未能在托管解決方案上建立驗證記錄。

## 定義登錄頁預設 {#lp-define-preset}

當 [建立登錄頁](../landing-pages/create-lp.md#create-a-lp)，必須選擇登錄頁預設才能生成登錄頁並利用它 **[!DNL Journey Optimizer]**。

### 訪問登錄頁預設 {#lp-presets}

要訪問登錄頁預設，請執行以下步驟。

1. 訪問 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** 的子菜單。

1. 選擇 **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

   ![](assets/lp_presets-access.png)

1. 按一下任何預設標籤以訪問登錄頁預設詳細資訊。

   ![](assets/lp_preset-details.png)

### 建立登錄頁預設 {#lp-create-preset}

要建立登錄頁預設，請執行以下步驟。

>[!NOTE]
>
>要能夠建立預設，請確保以前至少配置了一個登錄頁子域。 [瞭解如何](#lp-subdomains)

1. 訪問 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** ，然後選擇 **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**。

1. 選擇「**[!UICONTROL Create landing page preset]**」。

   ![](assets/lp_create-preset-temp.png)

1. 輸入預設的名稱和說明。

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含字母數字字元。 您還可以使用下划線 `_`，點`.` 連字元 `-` 字元。

1. 從下拉清單中選擇登錄頁子域。

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >要能夠選擇子域，請確保您以前至少配置了一個登錄頁子域。 [瞭解如何](#lp-subdomains)

   與所選子域對應的設定顯示。

1. 如果要選擇登錄頁子域作為跟蹤URL，請檢查 **[!UICONTROL Same as landing page subdomain]** 的雙曲餘切值。 [瞭解有關跟蹤的更多資訊](../messages/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   例如，如果登錄頁URL為「pages.mail.luma.com」，而跟蹤URL為「data.mail.luma.com」，則可以選擇「pages.mail.luma.com」作為跟蹤子域。

1. 按一下 **[!UICONTROL Submit]** 確認登錄頁預設建立。 您也可以將預設另存為草稿，並稍後恢復其配置。

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. 一旦建立了登錄頁預設，它就會顯示在清單中 **[!UICONTROL Active]** 狀態。 它已準備好用於您的登錄頁。

   ![](assets/lp-preset-active-temp.png)

您現在已準備好 [建立登錄頁](../landing-pages/create-lp.md) 在 [!DNL Journey Optimizer]。

>[!NOTE]
>
>瞭解如何為中的推送通知和電子郵件建立郵件預設 [此部分](message-presets.md)。

**相關主題**：

* [開始使用登陸頁面](../landing-pages/get-started-lp.md)
* [建立登陸頁面](../landing-pages/create-lp.md#create-a-lp)
