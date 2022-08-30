---
title: 報告設定
description: 瞭解如何設定報告資料來源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 100%

---

# 報告設定 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="設定資料集以進行報告"
>abstract="報告設定允許您定義與系統的連線，以擷取要在報告中使用的其他自訂資訊。 必須由技術使用者執行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="選取資料集"
>abstract="您只能選取一個事件類型資料集，該資料集必須至少包含一個受支援的欄位群組：experienceevent-web、experienceevent-application、experienceevent-commerce。"

資料來源設定可讓您定義系統連線，以擷取將用於報告的其他資訊。

>[!NOTE]
>
>資料來源設定必須由技術使用者執行。<!--Rights?-->

有關此設定，您需要新增一個或多個包含要用於報告的屬性資料集。 請依照下列步驟以執行此操作。

>[!CAUTION]
>
>必須先建立資料集，然後才能將資料集新增到報告設定。 在 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=zh-Hant#create){target=&quot;_blank&quot;} 中進一步瞭解。
>
>您只能新增事件類型資料集，它必須至少包含支援的 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target=&quot;_blank&quot;}：**experienceevent-web**、**experienceevent-application**、**experienceevent-commerce**。

<!--
➡️ [Discover this feature in video](#video)
-->

例如，如果您想瞭解電子郵件促銷活動對商業資料 (如採購或訂單) 的影響，則需要建立體驗事件資料集 **experienceevent-commerce** 欄位群組。 同樣，如果要報告行動互動，則需要建立體驗事件資料集 **experienceevent-application** 欄位群組。 <!--If you want to report on web interactions then you need to include the web field group.--> 您可以將這些欄位群組新增到一個或多個方案中，這些方案將用於一個資料集或不同資料集。

>[!NOTE]
>
>在 [XDM 系統總覽文件](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;} 中瞭解更多有關 XDM 方案和欄位群組的詳細資訊。

1. 從 **[!UICONTROL ADMINISTRATION]** 功能表，選取 **[!UICONTROL Configurations]**。在 **[!UICONTROL Reporting]** 區段，按一下 **[!UICONTROL Manage]**。

   ![](assets/reporting-config-menu.png)

   將顯示已新增的資料集清單。

1. 在 **[!UICONTROL Dataset]** 索引標籤中，按一下 **[!UICONTROL Add dataset]**。

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >如果選取 **[!UICONTROL System dataset]** 標籤，僅顯示由系統建立的資料集。 您將無法新增其他資料集。

1. 從 **[!UICONTROL Dataset]** 下拉式清單，選取要用於報告的資料集。

   >[!CAUTION]
   >
   >只能選擇事件類型資料集，該資料集必須至少包含支援的 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}：**experienceevent-web**、 **experienceevent-application**、**experienceevent-commerce**。 如果選取的資料集與這些條件不相符，將無法儲存變更。

   ![](assets/reporting-config-datasets.png)

   在 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hant){target=&quot;_blank&quot;} 資料集中了解更多。

1. 從 **[!UICONTROL Profile ID]** 下拉式清單中，選取用於定義每一份個人資料報告的資料集欄位屬性。

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >只顯示可用於報告的 ID。

1. 此 **[!UICONTROL Use Primary ID namespace]** 選項已預設啟用。如果選取的 **[!UICONTROL Profile ID]** 是 **[!UICONTROL Identity Map]**，可以禁用此選項，然後從顯示的下拉式清單中選擇另一個命名空間。

   ![](assets/reporting-config-namespace.png)

   在 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hant) {target=&quot;_blank&quot;} 中了解更多有關命名空間的資訊。

1. 儲存變更以將選取資料集新增到報告設定清單。

   >[!CAUTION]
   >
   >如果選取了非事件類型的資料集，則無法繼續。

當產生傳遞報告時，您可以使用此資料集中的資料來擷取其他自訂資訊，並更好地調整報告。 [了解更多](content-experiment.md#objectives-global)

>[!NOTE]
>
>如果新增多個資料集，則所有資料集中的所有資料都可用於報告。


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
