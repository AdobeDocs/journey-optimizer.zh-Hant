---
solution: Journey Optimizer
product: journey optimizer
title: 實作IP熱身計畫
description: 瞭解如何實作IP熱身計畫
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、集區、群組、子網域、傳遞能力
hide: true
hidefromtoc: true
source-git-commit: 1ac68f1b3a9657ce71a653011ab92fb817ca80b0
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 2%

---

# 實作IP熱身計畫 {#ip-warmup}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!AVAILABILITY]
>
>IP熱身功能目前僅供特定使用者測試使用。 若要加入測試版計畫，請連絡 Adobe 客戶服務。

替換為 [!DNL Journey Optimizer]，您可以遵循最佳傳遞能力的最佳實務，以標準化且有效率的方式直接從使用者介面執行IP熱身工作流程。

>[!CAUTION]
>
>此功能僅適用於電子郵件頻道。

使用新平台傳送電子郵件時，網際網路服務提供者(ISP)會懷疑無法辨識的IP位址。 如果突然傳送大量電子郵件，ISP通常會將其標籤為垃圾郵件。

為避免被標籤為垃圾訊息，您可以使用IP熱身計畫功能逐步增加傳送量。 「管理」選單中的新選項可讓您更順暢地執行操作，而不是建立複雜的歷程。 這應該可以確保啟動階段的順利發展，並且讓您降低無效的位址的整體比率。

>[!NOTE]
>
>進一步瞭解透過IP暖身提高您的電子郵件信譽 [傳遞性最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Here are the main steps:

1. You get a deliverability plan from the deliverability consulting team.

1. Create a campaign - marketer [Learn more](#create-ip-warmup-campaign)

1. Your associated practitioner (customer's practitioner/ACS consultant/partner consultant) creates a IP warmup object in project and uploads a plan.

    The CSV manifests itself like below with numbers showing up with/without domain bifurcation. Below screen shows one phase (creative) with associated runs (The plan obviously has more such phases)

1. Practitioner associates the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

1. Then start to execute on every day basis by simply clicking the play button

1. Reports will continue to show up at campaign level with similar capabilities as today. NO enhancements in BETA. But the IP warmup plan also serves as a consolidated report at one single place of how many executions were done and so on

Benefits are as follows:

* No more creation of daily journeys and associated testing

* Standardization on Campaign which will be easy for practitioners too

* No more pain of creating queries, audiences and testing those as system will create the audiences. At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* Single place to manage and view how IP warm is progressing.

* Consolidated report at creative/campaign level as all runs for a phase 

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

實施IP熱身計畫的關鍵步驟如下：

* [建立IP熱身行銷活動](#create-ip-warmup-campaign)
* [定義IP熱身計畫](#define-ip-warmup-plan)

## 建立IP熱身行銷活動 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="啟動IP熱身計畫選項"
>abstract="選取IP熱身計畫啟用選項。 行銷活動上線後，即可與IP熱身計畫建立關聯。"

您需要建立一或多個已啟用特定選項的促銷活動，以便用於IP熱身計畫。 請遵循下列步驟。

1. 建立 [表面](channel-surfaces.md) 用於您為預熱計畫識別的網域和IP。

1. 建立 [行銷活動](../campaigns/create-campaign.md) 並選取 [電子郵件](../email/create-email.md#create-email-journey-campaign) 動作。

1. 選取您為IP預熱建立的曲面。

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 排程]** 區段，選取 **[!UICONTROL IP熱身計畫啟用]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   行銷活動 [排程](../campaigns/create-campaign.md#schedule) 將由與其相關聯的IP熱身計畫驅動，這表示排程不再於行銷活動本身中定義。

1. [啟動](../campaigns/review-activate-campaign.md) 行銷活動。 一旦上線，就可在IP熱身計畫中使用。

>[!NOTE]
>
>對於已啟用IP熱身計畫的即時行銷活動， **[!UICONTROL 刪除]** 按鈕在與IP熱身計畫關聯之前可以使用。

有關如何設定行銷活動的詳細資訊，請參閱 [此頁面](../campaigns/get-started-with-campaigns.md).

## 定義IP熱身計畫 {#define-ip-warmup-plan}

### 管理IP熱身計畫 {#manage-ip-warmup-plans}

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

### 建立IP熱身計畫 {#create-ip-warmup-plan}

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

### 定義階段 {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="選取要排除的行銷活動對象"
>abstract="從其他行銷活動中選取您想要從目前階段排除的對象。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="選取要排除的網域群組"
>abstract="選取要從目前階段排除的網域。"

1. 針對每個階段，選取您要與IP熱身計畫的此階段關聯的促銷活動。

   ![](assets/ip-warmup-plan-select-campaign.png)

   請注意下列事項：

   * 僅限具有下列專案的行銷活動： **[!UICONTROL IP熱身計畫啟用]** 選項已啟用 <!--and live?--> 可供選取。 [了解更多](#create-ip-warmup-campaign)

   * 您必須選取與為目前IP熱身計畫選取之表面相同的行銷活動。

   * 您無法選取其他IP熱身行銷活動中已使用的行銷活動。

1. 適用於每個階段：

   * **[!UICONTROL 設定檔排除]**  — 一律會排除該階段先前執行的設定檔。 例如，如果在執行#1，Leo被納入目標前6300人，則系統將自動確保Leo在執行中不會收到郵件#2

   * **[!UICONTROL 已排除行銷活動對象]**  — 從其他對象中選取對象 <!--executed/live?-->您要從目前階段排除的行銷活動。

     例如，您可能正在執行一個階段，並且由於任何原因必須分割它。 在這種情況下，在階段2中，您要將階段1中使用的行銷活動包含在此部分中，以便在階段2中，不包含先前來自階段1的聯絡人。 不只可以在相同IP熱身計畫中使用的行銷活動，也可以從其他IP熱身計畫完成此操作。

   * **[!UICONTROL 網域群組已排除]**  — 選取您要從該階段排除的網域，例如Gmail。 <!--??-->

     執行IP熱身幾天後，您發現某個網域的ISP信譽指出了Hotmail不好，而您想要透過ISP解決這個問題，但不想停止IP熱身計畫。 在這種情況下，您可以將網域群組hotmail放在排除的類別中。

     >[!NOTE]
     >
     >網域排除需要非執行的階段，因此您可能必須分割執行中的階段才能新增排除。 同樣地，如果網域群組不是OOTB網域群組，則您可能必須在Excel中建立網域群組，並上傳然後排除相同的群組。

   ![](assets/ip-warmup-plan-phase-1.png)

1. 您可以視需要新增階段 — 它會在目前的最後一個階段之後新增。 使用 **[!UICONTROL 刪除階段]** 按鈕來移除任何不想要的階段。

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >您無法復原 **[!UICONTROL 刪除]** 動作。
   >
   >如果您從IP熱身計畫刪除所有階段，我們建議您重新上傳計畫。

### 定義回合 {#define-runs}

1. 選取每次執行的排程。 <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. 選取結束時間，這基本上代表我們可以執行預熱行銷活動的視窗，以防對象工作有任何延遲。 如果未指定，我們會在開始時間嘗試但會失敗。 如果有提供結束時間，我們將會在該視窗之間執行執行。

1. 啟動每次執行。 請確定您排程的時間夠早，以允許執行細分工作。 <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >每次執行必須在實際傳送時間前至少12小時啟動。 否則，可能無法完成分段。 <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

1. 如果行銷活動尚未開始，您可以停止執行。

   行銷活動開始執行後， **[!UICONTROL 停止]** 按鈕變為無法使用。 <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. 若要新增回合，請選取 **[!UICONTROL 在下方新增回合]** 從三個點的圖示。

   ![](assets/ip-warmup-plan-run-more-actions.png)

1. 在任何時候，如果您想要使用從特定執行開始的不同行銷活動，請選取 **[!UICONTROL 分割至新階段選項]** 從三個點的圖示。 系統會為目前階段的剩餘執行建立一個新階段。 請依照步驟操作 [以上](#define-phases) 以定義新階段。

   例如，如果您為執行#4選取此選項，則#8執行的執#4將移至新階段。

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

回合可以有下列狀態<!--TBC with Medha-->：

* **[!UICONTROL 完成]**:
* **[!UICONTROL 已失敗]**:
* **[!UICONTROL 已取消]**：您已在行銷活動執行開始之前停止執行。

