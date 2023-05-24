---
solution: Journey Optimizer
product: journey optimizer
title: 定義登陸頁面預設集
description: 瞭解如何配置環境以建立和使用登錄頁與Journey Optimizer
role: Admin
level: Intermediate
keywords: 登錄，登錄頁，配置，環境，子域，預設
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 17%

---

# 定義登陸頁面預設集 {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="建立一個登陸頁面預設集"
>abstract="為了建置登陸頁面並透過 Journey Optimizer 加以利用，您必須建立一個包含要使用的子網域的登陸頁面預設集。"

當 [建立登錄頁](../landing-pages/create-lp.md#create-a-lp)，必須選擇登錄頁預設才能生成登錄頁並利用它 **[!DNL Journey Optimizer]**。

## 訪問登錄頁預設 {#access-lp-presets}

要訪問登錄頁預設，請執行以下步驟。

1. 訪問 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 的子菜單。

1. 選擇 **[!UICONTROL 品牌]** > **[!UICONTROL 登錄頁預設]**。

   ![](assets/lp_presets-access.png)

1. 按一下任何預設標籤以訪問登錄頁預設詳細資訊。

   ![](assets/lp_preset-details.png)

## 建立一個登陸頁面預設集 {#lp-create-preset}

要建立登錄頁預設，請執行以下步驟。

>[!NOTE]
>
>要能夠建立預設，請確保以前至少配置了一個登錄頁子域。 [了解作法](lp-subdomains.md)

1. 訪問 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** ，然後選擇 **[!UICONTROL 品牌]** > **[!UICONTROL 登錄頁預設]**。

1. 選擇 **[!UICONTROL 建立登錄頁預設]**。

   ![](assets/lp_create-preset-temp.png)

1. 輸入預設的名稱和說明。

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含字母數字字元。 您還可以使用下划線 `_`，點`.` 連字元 `-` 字元。

1. 從下拉清單中選擇登錄頁子域。

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >要能夠選擇子域，請確保您以前至少配置了一個登錄頁子域。 [了解作法](#lp-subdomains)

   與所選子域對應的設定顯示。

1. 如果要為跟蹤URL選擇登錄頁子域，請檢查 **[!UICONTROL 與登錄頁子域相同]** 的雙曲餘切值。 [瞭解有關跟蹤的更多資訊](../email/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   例如，如果登錄頁URL為「pages.mail.luma.com」，而跟蹤URL為「data.mail.luma.com」，則可以選擇「pages.mail.luma.com」作為跟蹤子域。

1. 按一下 **[!UICONTROL 提交]** 確認登錄頁預設建立。 <!--You can also save the preset as draft and resume its configuration later on.-->

   <!--![](assets/lp_preset-subdomain-settings-submit.png)-->

1. 一旦建立了登錄頁預設，它就會顯示在清單中 **[!UICONTROL 活動]** 狀態。 它已準備好用於您的登錄頁。

   ![](assets/lp-preset-active-temp.png)

您現在已準備好 [建立登錄頁](../landing-pages/create-lp.md) 在 [!DNL Journey Optimizer]。
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](channel-surfaces.md).-->

**相關主題**：

* [開始使用登陸頁面](../landing-pages/get-started-lp.md)
* [建立登陸頁面](../landing-pages/create-lp.md#create-a-lp)
