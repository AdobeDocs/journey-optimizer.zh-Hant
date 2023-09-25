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
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '798'
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

建立一或多個 [IP熱身行銷活動](ip-warmup-campaign.md) 啟用專用表面並啟用對應的選項後，您就可以開始建立IP熱身計畫。

## 填寫IP熱身範本 {#upload-plan}

在Journey Optimizer介面中建立IP熱身計畫之前，您需要以Excel格式填寫範本，填入將供給您計畫的所有資料。

>[!CAUTION]
>
>請與您的傳遞顧問合作，確認您的IP熱身計畫檔案設定正確。

以下是包含IP熱身計畫的檔案範例。

![](assets/ip-warmup-sample-file.png)

### IP熱身計畫標籤

IP熱身是一種活動，包括逐漸增加從您的IP和網域傳送到主要網際網路服務提供者(ISP)的電子郵件數量，以建立您作為合法傳送者的聲譽。

本活動通常會由傳遞顧問或專家協助執行，該顧問或專家會根據產業網域、使用案例、地區、ISP和各種其他因素，準備經過深思熟慮的計畫。

* 在此範例中，已準備超過17天的計畫，並達到目標數量xxx個設定檔。

* 此計畫透過6個階段執行。

* 您可以對要傳送至的網域擁有任意數目的欄。 在此範例中，計劃分為四個欄，對應於要在計畫中使用的網域群組：Gmail、Adobe、Yahoo和其他。

我們的想法是在第一個階段有更多執行，並逐步增加目標位址的數量，同時減少執行次數。

現成可用的網域清單如下：

* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* 橙色
* 軟銀
* Docomo
* United Internet
* Microsoft
* KDDI
* 義大利線上
* 拉波斯特
* Apple

### 自訂網域群組標籤

您也可以使用自訂網域群組新增更多欄。

使用 **[!UICONTROL 自訂網域群組]** 定位以定義新網域，並為每個網域新增其涵蓋的所有子網域。<!--TBC-->

## 存取和管理IP熱身計畫 {#manage-ip-warmup-plans}

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP熱身計畫]** 功能表。 目前所建立的所有IP熱身計畫都會顯示出來。

   ![](assets/ip-warmup-filter-list.png)

1. 您可以依狀態篩選。 不同的狀態包括：

   * **尚未開始**：尚未啟用任何執行。 [了解更多](ip-warmup-running.md#define-runs)
   * **進行中/即時**：計畫會在第一個階段中的第一次執行成功啟動後，立即採取此狀態。 [了解更多](ip-warmup-running.md#define-runs)
   * **已完成**：計畫已標示為已完成。 只有在計畫中的所有執行都位於時，才能使用此選項 **[!UICONTROL 成功]** 或 **[!UICONTROL 草稿]** 狀態(無法執行 **[!UICONTROL 即時]**)。 [了解更多](ip-warmup-running.md#define-runs#mark-as-completed)
   * **已暫停**<!--: to check (user action)-->

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

當一或多個具有的即時行銷活動時 **[!UICONTROL IP熱身計畫啟用]** 啟用的選項已啟用，您可以將其與IP熱身計畫建立關聯。

>[!CAUTION]
>
>若要建立、編輯和刪除IP熱身計畫，您必須擁有 **[!UICONTROL 傳遞能力顧問]** 許可權。 <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->
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

## 重新上傳IP熱身計畫 {#re-upload-plan}

您可以使用對應的按鈕重新上傳另一個IP熱身計畫。

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>IP熱身計畫的詳細資訊會根據新上傳的檔案而變更。 完成執行和啟動的執行不受影響。