---
solution: Journey Optimizer
product: journey optimizer
title: 設定Journey Optimizer報表以進行實驗
description: 瞭解如何設定報告資料來源
feature: Experimentation, Reporting
topic: Administration
role: Admin
level: Intermediate
keywords: 設定，實驗，報告，最佳化工具
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 1490ac2efd39c6bf9b6ca97e682750463e9f054d
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 29%

---

# 為實驗設定報告 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="設定資料集以進行報告"
>abstract="報告設定可讓您擷取將在行銷活動報表中使用的其他量度。必須由技術使用者執行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="選取資料集"
>abstract="您只能選取一個事件類型的資料集，該資料集必須至少包含一個受支援的欄位群組：應用程式詳細資訊、商務詳細資訊、Web 詳細資訊。"

資料來源設定可讓您定義系統連線，以擷取將用於報告的其他資訊。

<!--The reporting data source configuration allows you to retrieve additional metrics that will be used in the **[!UICONTROL Objectives]** tab of your campaign reports.-->

>[!NOTE]
>
>報告設定必須由技術使用者執行。 <!--Rights?-->

對於此設定，您需要新增一個或多個包含您想用於報告的其他元素的資料集。 請依照下列步驟以執行此操作 [以下](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## 先決條件


必須先建立該資料集，才能將資料集新增到報表設定。 瞭解如何在 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#create){target="_blank"}.

* 您只能新增事件型別資料集。

* 這些資料集必須包括 `Experience Event - Proposition Interactions` [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target="_blank"}.

* 這些資料集可能也包含下列其中一項 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target="_blank"}： `Application Details`， `Commerce Details`， `Web Details`.

  >[!NOTE]
  >
  >可能還包括其他欄位群組，但Journey Optimizer報表中目前僅支援上述欄位群組。

  例如，如果您想瞭解電子郵件行銷活動對商業資料（如購買或訂單）的影響，則需要使用建立體驗事件資料集 `Commerce Details` 欄位群組。

  同樣地，如果您想要報告行動互動，則需要建立體驗事件資料集，包含 `Application Details` 欄位群組。

  <!--The metrics corresponding to each field group are listed [here](#objective-list).-->

* 您可以將這些欄位群組新增到一個或多個方案中，這些方案將用於一個或多個資料集。

>[!NOTE]
>
>瞭解更多關於XDM結構描述和欄位群組 [XDM系統總覽檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.

<!--
## Objectives corresponding to each field group {#objective-list}

The table below shows which metrics will be added to the **[!UICONTROL Objectives]** tab of your campaign reports for each field group.

| Field group | Objectives |
|--- |--- |
| Commerce Details | Price Total<br>Payment Amount<br>(Unique) Checkouts<br>(Unique) Product List Adds<br>(Unique) Product List Opens<br>(Unique) Product List Removal<br>(Unique) Product List Views<br>(Unique) Product Views<br>(Unique) Purchases<br>(Unique) Save For Laters<br>Product Price Total<br>Product Quantity |
| Application Details | (Unique) App Launches<br>First App Launches<br>(Unique) App Installs<br>(Unique) App Upgrades |
| Web Details | (Unique) Page Views |
-->

## 新增資料集 {#add-datasets}

1. 從 **[!UICONTROL 管理]** 功能表，選取 **[!UICONTROL 設定]**. 在  **[!UICONTROL 報告]** 區段，按一下 **[!UICONTROL 管理]**.

   ![](assets/reporting-config-menu.png)

   將顯示已新增的資料集清單。

1. 從 **[!UICONTROL 資料集]** 標籤，按一下 **[!UICONTROL 新增資料集]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >如果您選取 **[!UICONTROL 系統資料集]** 標籤中，僅顯示由系統建立的資料集。 您將無法新增其他資料集。

1. 從 **[!UICONTROL 資料集]** 從下拉式清單中，選取要用於報告的資料集。

   >[!CAUTION]
   >
   >您只能選取事件型別資料集，該資料集必須至少包含其中一個支援的 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target="_blank"}： **應用程式詳細資料**， **商業細節**， **網頁詳細資訊**. 如果選取的資料集與這些條件不相符，將無法儲存變更。

   ![](assets/reporting-config-datasets.png)

   進一步瞭解中的資料集 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hant){target="_blank"}.

1. 從 **[!UICONTROL 設定檔ID]** 從下拉式清單中，選取用於識別報表中每個設定檔的資料集欄位屬性。

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >只顯示可用於報告的 ID。

1. 此 **[!UICONTROL 使用主要ID名稱空間]** 選項預設為啟用。 若已選取 **[!UICONTROL 設定檔ID]** 是 **[!UICONTROL 身分對應]**，您可以停用此選項，然後從顯示的下拉式清單中選擇另一個名稱空間。

   ![](assets/reporting-config-namespace.png)

   進一步瞭解中的名稱空間 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hant){target="_blank"}.

1. 儲存變更以將選取資料集新增到報告設定清單。

   >[!CAUTION]
   >
   >如果選取了非事件類型的資料集，則無法繼續。

請注意，針對網頁和應用程式內頻道，您需要確認 [資料集](../data/get-started-datasets.md) 針對資料收集所設定的專案也會新增至此報告設定。 否則，網頁和應用程式內資料將不會顯示在內容實驗報表中。

* 瞭解更多有關Web通道的內容實驗先決條件，請參閱 [本節](../web/web-prerequisites.md#experiment-prerequisites).

* 進一步瞭解中的應用程式內頻道設定，請參閱 [本節](../in-app/inapp-configuration.md).

<!--
When building your campaign reports, you can now see the metrics corresponding to the field groups used in the datasets you added. Go to the **[!UICONTROL Objectives]** tab and select the metrics of your choice to better fine-tune your reports. [Learn more](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>If you add several datasets, all data from all datasets will be available for reporting.


## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
