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
source-git-commit: 28380dbadf485ba05f7ef6788a50253876718441
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 43%

---

# 報告設定 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="設定資料集以進行報告"
>abstract="報告配置允許您檢索將在市場活動報告的「目標」標籤中使用的其他度量。 必須由技術使用者執行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="選取資料集"
>abstract="您只能選擇一個事件類型資料集，該資料集必須至少包含一個受支援的欄位組：應用程式詳細資訊、商務詳細資訊、Web詳細資訊。"

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

報告資料源配置允許您檢索將在 **[!UICONTROL Objectives]** 頁籤。 [了解更多](content-experiment.md#objectives-global)

>[!NOTE]
>
>報告配置必須由技術用戶執行。 <!--Rights?-->

對於此配置，您需要添加一個或多個資料集，其中包含要用於報表的其他元素。 要執行此操作，請執行步驟 [下](#add-datasets)。

<!--
➡️ [Discover this feature in video](#video)
-->

## 先決條件


必須先建立該資料集，然後才能將資料集添加到報告配置。 在 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=zh-Hant#create){target=&quot;_blank&quot;} 中進一步瞭解。

* 只能添加事件類型資料集。

* 這些資料集必須至少包含以下其中之一 [欄位組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target=&quot;_blank&quot;: **應用程式詳細資訊**。 **商業詳細資訊**。 **Web詳細資訊**。

   >[!NOTE]
   >
   >當前僅支援這些欄位組。

   例如，如果您想瞭解電子郵件活動對商業資料（如採購或訂單）的影響，則需要使用 **商業詳細資訊** 欄位組。

   同樣，如果要報告移動交互，則需要使用 **應用程式詳細資訊** 欄位組。

   列出與每個欄位組對應的度量 [這裡](#objective-list)。

* 您可以將這些欄位組添加到一個或多個方案中，這些方案將用於一個或多個資料集。

>[!NOTE]
>
>在 [XDM 系統總覽文件](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;} 中瞭解更多有關 XDM 方案和欄位群組的詳細資訊。

## 對應於每個欄位組的目標 {#objective-list}

下表顯示了將添加到 **[!UICONTROL Objectives]** 按鈕。

| 欄位群組 | 目標 |
|--- |--- |
| 商業詳細資訊 | 價格合計<br>付款金額<br>（唯一）簽出<br>（唯一）產品清單添加<br>（唯一）產品清單開啟<br>（唯一）刪除產品清單<br>（唯一）產品清單視圖<br>（唯一）產品視圖<br>（唯一）購買<br>（唯一）為後台保存<br>產品價格合計<br>產品數量 |
| 應用程式詳細資訊 | （唯一）應用程式啟動<br>首次應用啟動<br>（唯一）應用程式安裝<br>（唯一）應用程式升級 |
| Web詳細資訊 | （唯一）頁面視圖 |

## 添加資料集 {#add-datasets}

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
   >只能選擇事件類型資料集，該資料集必須至少包含支援的 [欄位組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;: **應用程式詳細資訊**。 **商業詳細資訊**。 **Web詳細資訊**。 如果選取的資料集與這些條件不相符，將無法儲存變更。

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

在生成市場活動報告時，您現在可以查看與添加的資料集中使用的欄位組相對應的度量。 轉到 **[!UICONTROL Objectives]** 頁籤，然後選擇您選擇的度量以更好地調整報告。 [了解更多](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>如果新增多個資料集，則所有資料集中的所有資料都可用於報告。

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
