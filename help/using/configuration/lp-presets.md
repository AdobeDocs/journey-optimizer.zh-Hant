---
title: 定義登陸頁面預設集
description: 了解如何設定您的環境，以使用Journey Optimizer建立和使用登錄頁面
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 5%

---

# 定義登陸頁面預設集 {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain_header"
>title="建立登錄頁面預設集"
>abstract="若要建立登錄頁面並透過Journey Optimizer運用該頁面，您必須建立包含要使用之子網域的登錄頁面預設集。"

當 [建立登錄頁面](../landing-pages/create-lp.md#create-a-lp)，您必須選取登錄頁面預設集，才能建立登錄頁面並運用它 **[!DNL Journey Optimizer]**.

## 存取登錄頁面預設集 {#access-lp-presets}

若要存取登錄頁面預設集，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** 功能表。

1. 選擇 **[!UICONTROL 品牌推廣]** > **[!UICONTROL 登錄頁面預設集]**.

   ![](assets/lp_presets-access.png)

1. 按一下任何預設集標籤以存取登錄頁面預設集詳細資訊。

   ![](assets/lp_preset-details.png)

## 建立登錄頁面預設集 {#lp-create-preset}

若要建立登錄頁面預設集，請遵循下列步驟。

>[!NOTE]
>
>若要建立預設集，請確定您先前已設定至少一個登錄頁面子網域。 [了解如何](lp-subdomains.md)

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** ，然後選取 **[!UICONTROL 品牌推廣]** > **[!UICONTROL 登錄頁面預設集]**.

1. 選擇 **[!UICONTROL 建立登錄頁面預設集]**.

   ![](assets/lp_create-preset-temp.png)

1. 輸入預設集的名稱和說明。

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 連字型大小 `-` 字元。

1. 從下拉式清單中選取登錄頁面子網域。

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >若要選取子網域，請確定您先前已設定至少一個登錄頁面子網域。 [了解如何](#lp-subdomains)

   隨即顯示與所選子網域對應的設定。

1. 如果您想要選取登錄頁面子網域作為追蹤URL，請核取 **[!UICONTROL 與登錄頁面子網域相同]** 選項。 [進一步了解追蹤](../design/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   例如，如果登錄頁面URL為「pages.mail.luma.com」，而追蹤URL為「data.mail.luma.com」，您可以選擇「pages.mail.luma.com」作為追蹤子網域。

1. 按一下 **[!UICONTROL 提交]** 以確認建立登錄頁面預設集。 您也可以將預設集儲存為草稿，稍後繼續其設定。

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. 建立登錄頁面預設集後，該預設集會顯示在清單中，且包含 **[!UICONTROL 作用中]** 狀態。 已準備好用於您的登錄頁面。

   ![](assets/lp-preset-active-temp.png)

您現在已準備好 [建立登錄頁面](../landing-pages/create-lp.md) in [!DNL Journey Optimizer].
<!--
>[!NOTE]
>
>Learn how to create channel surfaces for push notifications and emails in [this section](channel-surfaces.md).-->

**相關主題**：

* [開始使用登陸頁面](../landing-pages/get-started-lp.md)
* [建立登陸頁面](../landing-pages/create-lp.md#create-a-lp)
