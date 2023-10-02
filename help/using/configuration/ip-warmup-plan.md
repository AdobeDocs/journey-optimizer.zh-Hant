---
solution: Journey Optimizer
product: journey optimizer
title: 建立IP熱身計畫
description: 瞭解如何在Journey Optimizer中建立IP熱身計畫
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、群組、子網域、傳遞能力
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: 205f26d3f31b9f003fc1dbaf679021464429d144
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 14%

---

# 建立IP熱身計畫 {#ip-warmup}

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用IP熱身](ip-warmup-gs.md)
* [建立 IP 暖身行銷活動](ip-warmup-campaign.md)
* **[建立IP熱身計畫](ip-warmup-plan.md)**
* [執行IP熱身計畫](ip-warmup-execution.md)

>[!ENDSHADEBOX]

建立一或多個 [IP熱身行銷活動](ip-warmup-campaign.md) 啟用專用表面並啟用對應的選項後，您就可以開始建立IP熱身計畫。

## 準備IP熱身計畫檔案 {#prepare-file}

IP熱身是一項活動，包括逐漸增加從您的IP和網域傳送到主要網際網路服務提供者(ISP)的電子郵件數量，以建立您作為合法傳送者的聲譽。

此活動通常在傳遞能力專家的協助下執行，該專家會根據產業網域、使用案例、地區、ISP和各種其他因素，協助您準備完善的計畫。

使用時 [!DNL Journey Optimizer] IP預熱功能，此計畫採用Excel檔案的形式，必須包含許多預先定義的欄。 在中建立IP熱身計畫之前 [!DNL Journey Optimizer] 介面，您必須填入此範本中所有可為您計畫提供摘要的資料。

>[!CAUTION]
>
>請與您的傳遞顧問合作，確認您的IP熱身計畫檔案設定正確。

以下是包含IP熱身計畫的檔案範例。

![](assets/ip-warmup-sample-file.png)

### IP熱身計畫標籤

* 在此範例中，已準備超過17天的計畫(稱為「**執行**「)達到超過100萬個設定檔的目標數量。

* 此計畫透過6執行 **階段**，每個檔案至少包含一個回合。

* 您可以對要傳送至的網域擁有任意數目的欄。 在此範例中，計劃分為6個資料欄：其中5個對應至 **主要網域群組** 用於您的計畫(Gmail、Microsoft、Yahoo、Orange和Apple)和第六欄， **其他**，包含其他網域的所有剩餘位址。
* 此 **參與天數** 欄會顯示僅鎖定過去30天內與您的品牌互動的設定檔。

我們的想法是逐步增加每個執行中的目標位址數量，同時減少每個階段的執行數量。

以下列出您可以新增到計畫中的現成主要網域群組：

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

您也可以包含自訂網域群組，以新增更多欄到計畫中。

使用 **[!UICONTROL 自訂網域群組]** 標籤定義新的網域群組。 您可以為每個網域新增其涵蓋的所有子網域。<!--TBC-->

例如，如果您新增自訂網域Luma，您希望加入下列子網域：luma.com、luma.co.uk、luma.it、luma.fr、luma.de等。

![](assets/ip-warmup-sample-file-custom.png)

## 存取和管理IP熱身計畫 {#manage-ip-warmup-plans}

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP熱身計畫]** 功能表。 目前所建立的所有IP熱身計畫都會顯示出來。

   ![](assets/ip-warmup-filter-list.png)

1. 您可以依狀態篩選。 不同的狀態包括：

   * **尚未開始**：尚未啟用任何執行。 [了解更多](ip-warmup-execution.md#define-runs)
   * **即時**：成功啟用第一個階段中的第一次執行後，計畫就會變更為此狀態。 [了解更多](ip-warmup-execution.md#define-runs)
   * **已完成**：計畫已標示為已完成。 只有在計畫中的所有執行都位於時，才能使用此選項 **[!UICONTROL 已完成]** 或 **[!UICONTROL 草稿]** 狀態(無法執行 **[!UICONTROL 即時]**)。 [了解更多](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. 若要刪除IP熱身計畫，請選取 **[!UICONTROL 刪除]** 圖示並確認刪除。

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >將會永久刪除選取的IP熱身計畫。

## 建立IP熱身計畫 {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="指定您的 IP 暖身計劃"
>abstract="下載 CSV 範本並在其中填入 IP 暖身階段和設定檔目標數量的資料。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="選取行銷表面"
>abstract="您選取的表面必須相同於您想要與 IP 暖身計畫相關聯之行銷活動的所選表面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=zh-Hant" text="設定頻道介面"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=zh-Hant" text="建立 IP 暖身行銷活動"

當一或多個具有的即時行銷活動時 **[!UICONTROL IP熱身計畫啟用]** 啟用的選項已啟用，您可以將其與IP熱身計畫建立關聯。

>[!CAUTION]
>
>若要建立、編輯和刪除IP熱身計畫，您必須擁有 **[!UICONTROL 傳遞能力顧問]** 許可權。 <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP熱身計畫]** 功能表，然後按一下 **[!UICONTROL 建立IP熱身計畫]**.

   ![](assets/ip-warmup-create-plan.png)

1. 填寫IP熱身計畫詳細資訊：提供名稱和說明。

   ![](assets/ip-warmup-plan-details.png)

1. 選取 [表面](channel-surfaces.md). 只有行銷表面可供選取。 [進一步瞭解電子郵件型別](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >您選取的表面必須相同於您想要與 IP 暖身計畫相關聯之行銷活動的所選表面。[瞭解如何建立IP熱身行銷活動](ip-warmup-campaign.md)

1. 上傳包含IP熱身計畫的Excel檔案。 [了解更多](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。在您上傳的檔案中定義的所有階段、執行、欄及其內容會自動顯示在 [!DNL Journey Optimizer] 介面。 [了解更多](ip-warmup-execution.md)

   ![](assets/ip-warmup-plan-uploaded.png)
