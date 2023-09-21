---
solution: Journey Optimizer
product: journey optimizer
title: 建立IP熱身計畫
description: 瞭解如何建立IP熱身計畫
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、集區、群組、子網域、傳遞能力
hide: true
hidefromtoc: true
source-git-commit: 53be033ff0474cbafff71ed36194c18627234fd4
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 5%

---

# 建立IP熱身計畫 {#ip-warmup}

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用IP熱身](ip-warmup-gs.md)
* [建立IP熱身行銷活動](ip-warmup-campaign.md)
* **[建立IP熱身計畫](ip-warmup-plan.md)**
* [執行IP熱身計畫](ip-warmup-running.md)

>[!ENDSHADEBOX]

一旦您 [已建立一或多個行銷活動](ip-warmup-campaign.md) 啟用專用表面和IP熱身選項後，您就可以開始建立IP熱身計畫。

## 存取和管理IP熱身計畫 {#manage-ip-warmup-plans}

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP熱身計畫]** 功能表。 目前所建立的所有IP熱身計畫都會顯示出來。

   ![](assets/ip-warmup-filter-list.png)

1. 您可以依狀態篩選。 不同的狀態包括：

   * **尚未開始**：未發生任何回合
   * **進行中**：當一個回合開始時 <!--or is done?-->
   * **已暫停**
   * **已完成**：計畫中的所有執行都已完成

1. 若要刪除IP熱身計畫，請選取 **[!UICONTROL 刪除]** 圖示並確認刪除。

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >將會永久刪除選取的IP熱身計畫。

## 建立IP熱身計畫 {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="指定您的IP熱身計畫"
>abstract="下載CSV範本，並填入IP熱身階段的資料和目標設定檔數量。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="選取行銷表面"
>abstract="您必須選取與您要與IP熱身計畫關聯的行銷活動中選取的相同表面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=zh-Hant" text="設定頻道介面"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=zh-Hant" text="建立IP熱身行銷活動"

>[!CAUTION]
>
>若要建立、編輯和刪除IP熱身計畫，您必須擁有 **[!UICONTROL 傳遞能力顧問]** 許可權。
<!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

當一或多個具有的即時行銷活動時 **[!UICONTROL IP熱身計畫啟用]** 啟用的選項已啟用，您可以將其與IP熱身計畫建立關聯。

>[!CAUTION]
>
>請與您的傳遞顧問合作，確定您的IP熱身計畫範本已正確設定。 <!--TBC-->

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP熱身計畫]** 功能表，然後按一下 **[!UICONTROL 建立IP熱身計畫]**.

   ![](assets/ip-warmup-create-plan.png)

1. 填寫IP熱身計畫詳細資訊：提供名稱和說明。

   ![](assets/ip-warmup-plan-details.png)

1. 選取 [表面](channel-surfaces.md). 只有行銷表面可供選取。 [進一步瞭解電子郵件型別](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >您必須選取與您要與IP熱身計畫關聯的行銷活動中選取的相同表面。 [瞭解如何建立IP熱身行銷活動](#create-ip-warmup-campaign)

1. 上傳包含IP熱身計畫的Excel檔案<!--which formats are allowed?-->. 您可以使用傳遞團隊提供的範本。<!--TBC?--> [了解更多](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。系統會自動顯示您上傳的檔案中定義的階段數，每個階段的所有執行都會顯示出來。 [了解更多](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

### 重新上傳IP熱身計畫 {#re-upload-plan}

您可以使用對應的按鈕重新上傳另一個IP熱身計畫。

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>IP熱身計畫的詳細資訊會根據新上傳的檔案而變更。 完成執行和啟動的執行不受影響。

### 上傳包含計畫的檔案 {#upload-plan}

以下是包含IP熱身計畫的檔案範例。

![](assets/ip-warmup-sample-file.png)

每個階段都對應一個由數個執行組成的期間，您將會指派單一行銷活動給該期間。

對於每次執行，您都有特定數量的收件者，且您將定義執行此執行的日期。

您可以對要傳送至的網域擁有任意數目的欄。 在此範例中，您有三個欄：Gmail、Adobe和「其他」，這表示

我們的想法是在第一個階段有更多執行，並逐步增加目標位址的數量，同時減少執行次數。
