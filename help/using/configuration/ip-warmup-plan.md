---
solution: Journey Optimizer
product: journey optimizer
title: 建立 IP 暖身計劃
description: 瞭解如何在Journey Optimizer中建立IP熱身計畫
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP、群組、子網域、傳遞能力
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: eb4a4929de17f0b57216f69e00da6314f7b59b07
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 11%

---

# 建立 IP 暖身計劃 {#ip-warmup}

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用 IP 暖身](ip-warmup-gs.md)
* [建立 IP 暖身行銷活動](ip-warmup-campaign.md)
* **[建立 IP 暖身計劃](ip-warmup-plan.md)**
* [執行 IP 暖身計劃](ip-warmup-execution.md)

>[!ENDSHADEBOX]

建立一或多個 [IP熱身行銷活動](ip-warmup-campaign.md) 啟用專用表面並啟用對應的選項後，您就可以開始建立IP熱身計畫。

>[!CAUTION]
>
>若要存取、建立、編輯和刪除IP熱身計畫，您必須擁有 **[!UICONTROL 傳遞能力顧問]** 許可權。 <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

## 準備IP熱身計畫檔案 {#prepare-file}

IP熱身是一項活動，包括逐漸增加從您的IP和網域傳送到主要網際網路服務提供者(ISP)的電子郵件數量，以建立您作為合法傳送者的聲譽。

此活動通常在傳遞能力專家的協助下執行，該專家會根據產業網域、使用案例、地區、ISP和各種其他因素，協助您準備完善的計畫。

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

在中建立IP熱身計畫之前 [!DNL Journey Optimizer] 介面，您必須在Excel範本中填入所有可為計畫提供摘要的資料。

>[!CAUTION]
>
>請與您的傳遞顧問合作，確認您的IP熱身計畫檔案設定正確。
>
>請務必使用範本中提供的格式。

以下是包含IP熱身計畫的檔案範例。

![](assets/ip-warmup-sample-file.png)

>[!NOTE]
>
>目前，您應將 **屬性** 和 **值** 未接觸的儲存格。

### IP熱身計畫標籤 {#ip-warmup-plan-tab}

* 在此範例中，已準備超過17天的計畫(稱為「**執行**「)達到超過一百萬個設定檔的目標數量。

* 此計畫會透過六個步驟執行 **階段**，每個檔案至少包含一個回合。

* 您可以對要傳送至的網域擁有任意數目的欄。 在此範例中，計劃分為六個欄：

   * 其中四個對應至 **現成可用的網域群組** 用於您的計畫(Gmail、Microsoft、Yahoo和Orange)。
   * 其中一個對應至自訂網域群組(您需要使用 [自訂網域群組](#custom-domain-group-tab) 標籤)。
   * 第六欄， **其他**，包含計畫未明確涵蓋之其他網域的所有剩餘位址。 此欄是選用的：如果省略，電子郵件將只傳送到指定的網域。
* 此 **參與天數** 欄會顯示僅鎖定在輸入的最後一個期間與您的品牌互動的設定檔。

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

<!--
+++ Gmail
gmail.com;gmail.fr;gmail.de;gmail.co.uk;gmail.it
+++

+++ Adobe
adobe.com;adobe.fr;adobe.es
+++

+++WP
+++

+++Comcast
+++

+++Yahoo
+++

+++Bigpond
+++

+++Orange
+++

+++Softbank
+++

+++Docomo
+++

+++United Internet
+++

+++Microsoft
+++

+++KDDI
+++

+++Italia Online
+++

+++La Poste
+++
-->

### 自訂網域群組標籤 {#custom-domain-group-tab}

您也可以包含自訂網域群組，以新增更多欄到計畫中。

使用 **[!UICONTROL 自訂網域群組]** 標籤定義新的網域群組。 您可以為每個網域新增其涵蓋的所有子網域。<!--TBC-->

例如，如果您新增自訂網域Luma，您希望加入下列子網域：luma.com、luma.co.uk、luma.it、luma.fr、luma.de等。

![](assets/ip-warmup-sample-file-custom.png)

### 範例 {#example}

假設您想要有兩個自訂網域群組：

* 一個僅適用於Hotmail網域。
* 一個用於網域群組Microsoft中的所有其他網域（因此排除所有Hotmail網域）。

請注意，所有其他網域將會收集到 **[!UICONTROL 其他]** 欄。

1. 在 **[!UICONTROL 自訂網域群組]** 標籤，建立 **Hotmail** 網域群組。

1. 在同一列新增所有Hotmail網域。

   您可以 [複製並貼上](#copy-paste) 列在「 」中的所有Hotmail網域 [IP熱身計畫標籤](#ip-warmup-plan-tab) 區段。

1. 新增另一列。

1. 建立 **Microsoft_X** 網域群組。

1. 將非Hotmail的所有Microsoft網域新增至相同列。 同樣地，您可以從上述清單複製並貼上它們。 [了解更多](#copy-paste)

1. 返回 **[!UICONTROL IP熱身計畫]** 標籤。

1. 建立三欄：一個用於 **Hotmail**，一個用於 **Microsoft_X** 一個用於 **其他**.

1. 根據您的需求填寫欄。

>[!NOTE]
>
>將IP熱身計畫上傳到後 [!DNL Journey Optimizer]，您不需要排除Microsoft網域群組。

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### 複製並貼上預設網域 {#copy-paste}

例如，如果您想建立包含所有Hotmail網域的自訂網域群組，您可以從提供的預設清單中複製並貼上網域 [以上](#ip-warmup-plan-tab).

然後使用Excel轉換工具將文字轉換為欄：

1. 選取 **[!UICONTROL 資料]** > **[!UICONTROL 文字至欄……]**，選擇 **[!UICONTROL 已分隔]** 並選取 **[!UICONTROL 下一個]**.

1. 選取 **[!UICONTROL 分號]**，按一下 **[!UICONTROL 下一個]** 和 **[!UICONTROL 完成]**.

現在，每個網域都會顯示在相同列的不同欄中。

## 存取和管理IP熱身計畫 {#manage-ip-warmup-plans}

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP熱身計畫]** 功能表。 目前所建立的所有IP熱身計畫都會顯示出來。

   ![](assets/ip-warmup-filter-list.png)

1. 您可以依狀態篩選。 不同的狀態包括：

   * **尚未開始**：尚未啟用任何執行。 [了解更多](ip-warmup-execution.md#define-runs)
   * **即時**：成功啟用第一個階段中的第一次執行後，計畫就會變更為此狀態。 [了解更多](ip-warmup-execution.md#define-runs)
   * **已完成**：計畫已標示為已完成。 <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [了解更多](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. 若要刪除IP熱身計畫，請選取 **[!UICONTROL 刪除]** 圖示並確認刪除。

   >[!NOTE]
   >
   >僅限具有下列專案的計畫： **尚未開始** 狀態可刪除。

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >將會永久刪除選取的IP熱身計畫。

## 建立 IP 暖身計劃 {#create-ip-warmup-plan}

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

若要建立IP熱身計畫，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP熱身計畫]** 功能表，然後按一下 **[!UICONTROL 建立IP熱身計畫]**.

   ![](assets/ip-warmup-create-plan.png)

1. 填寫IP熱身計畫詳細資訊：提供名稱和說明。

   ![](assets/ip-warmup-plan-details.png)

1. 選取 [表面](channel-surfaces.md) 您想要熱身。 只有行銷表面可供選取。 [進一步瞭解電子郵件型別](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >您要與IP熱身計畫關聯的行銷活動必須使用相同表面。 [瞭解如何建立IP熱身行銷活動](ip-warmup-campaign.md)

1. 上傳包含IP熱身計畫的Excel檔案。 [了解更多](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >如果上傳失敗，請確定您使用正確的格式和檔案格式(.xls或.xlsx)。 使用Adobe為您提供的範例。

1. 按一下&#x200B;**[!UICONTROL 建立]**。在您上傳的檔案中定義的所有階段、執行、欄及其內容會自動顯示在 [!DNL Journey Optimizer] 介面。

   ![](assets/ip-warmup-plan-uploaded.png)

您現在已準備好執行IP熱身計畫。 [了解更多](ip-warmup-execution.md)
