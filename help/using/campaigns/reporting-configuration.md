---
title: 報告配置
description: 瞭解如何設定報告資料源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 11f7ce37dc1a99de4ed29fa7793f126e259f518d
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 4%

---

# 報告配置 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="設定資料集以進行報告"
>abstract="報告配置允許您定義到系統的連接，以檢索要在報告中使用的其他自定義資訊。 必須由技術用戶執行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="選擇資料集"
>abstract="您只能選擇一個事件類型資料集，該資料集必須至少包含一個受支援的欄位組：體驗事件 — web、體驗事件 — 應用、體驗事件 — 商務。"

報告資料源配置允許您定義到系統的連接，以檢索將在報告中使用的其他資訊。

>[!NOTE]
>
>資料源配置必須由技術用戶執行。 <!--Rights?-->

對於此配置，您需要添加一個或多個包含要用於報表的屬性的資料集。 請依照下列步驟以執行此操作。

>[!CAUTION]
>
>必須先建立資料集，然後才能將資料集添加到報告配置。 瞭解 [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}。
>
>您只能添加事件類型資料集，它必須至少包含支援的 [欄位組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;: **體驗事件網**。 **體驗事件應用程式**。 **體驗事件商務**。

<!--
➡️ [Discover this feature in video](#video)
-->

例如，如果您想瞭解電子郵件活動對商業資料（如採購或訂單）的影響，則需要使用 **體驗事件商務** 欄位組。 同樣，如果要報告移動交互，則需要使用 **體驗事件應用程式** 欄位組。 <!--If you want to report on web interactions then you need to include the web field group.--> 您可以將這些欄位組添加到一個或多個方案中，這些方案將用於一個資料集或不同資料集。

>[!NOTE]
>
>瞭解有關中的XDM架構和欄位組的詳細資訊 [XDM系統概述文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

1. 從 **[!UICONTROL ADMINISTRATION]** 菜單，選擇 **[!UICONTROL Configurations]**。 在  **[!UICONTROL Reporting]** ，按一下 **[!UICONTROL Manage]**。

   ![](assets/reporting-config-menu.png)

   將顯示已添加的資料集清單。

1. 在 **[!UICONTROL Dataset]** 索引標籤中，按一下 **[!UICONTROL Add dataset]**。

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >如果選擇 **[!UICONTROL System dataset]** 頁籤，僅顯示由系統建立的資料集。 您將無法添加其他資料集。

1. 從 **[!UICONTROL Dataset]** 下拉清單，選擇要用於報表的資料集。

   >[!CAUTION]
   >
   >只能選擇事件類型資料集，該資料集必須至少包含支援的 [欄位組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;: **體驗事件網**。 **體驗事件應用程式**。 **體驗事件商務**。 如果選擇的資料集與這些條件不匹配，則將無法保存更改。

   ![](assets/reporting-config-datasets.png)

   瞭解有關 [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}。

1. 從 **[!UICONTROL Profile ID]** 下拉清單中，選擇用於標識報告中每個配置檔案的資料集欄位屬性。

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >只顯示可用於報告的ID。

1. 的 **[!UICONTROL Use Primary ID namespace]** 選項。 如果選定 **[!UICONTROL Profile ID]** 是 **[!UICONTROL Identity Map]**，可以禁用此選項，然後從顯示的下拉清單中選擇另一個命名空間。

   ![](assets/reporting-config-namespace.png)

   瞭解有關中命名空間的詳細資訊 [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}。

1. 保存更改以將所選資料集添加到報告配置清單。

   >[!CAUTION]
   >
   >如果選擇了非事件類型的資料集，則無法繼續。

在生成交貨報告時，您現在可以使用此資料集中的資料來檢索其他自定義資訊，並更好地調整報告。 [了解更多](campaign-global-report.md#objectives-global)

>[!NOTE]
>
>如果添加多個資料集，則所有資料集中的所有資料都可用於報告。


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
