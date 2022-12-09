---
solution: Journey Optimizer
product: journey optimizer
title: 設定Journey Optimizer報表以進行實驗
description: 了解如何設定報表資料來源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 0%

---

# 設定報表以供實驗 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="設定報表資料集"
>abstract="報表設定可讓您擷取將用於促銷活動報表之「目標」標籤的其他量度。 必須由技術使用者執行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="選取資料集"
>abstract="您只能選取事件類型資料集，該資料集必須至少包含一個支援的欄位群組：應用程式詳細資訊、商務詳細資訊、Web詳細資訊。"

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

報表資料來源設定可讓您擷取將用於 **[!UICONTROL Objectives]** 標籤。 [深入了解](content-experiment.md#objectives-global)

>[!NOTE]
>
>報表設定必須由技術使用者執行。 <!--Rights?-->

針對此設定，您需要新增一或多個資料集，其中包含您要用於報表的其他元素。 要執行此操作，請遵循步驟 [low](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## 必要條件


您必須先建立該資料集，才能將資料集新增至報表設定。 了解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}。

* 您只能新增事件類型資料集。

* 這些資料集至少必須包含下列其中一項 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **應用程式詳細資訊**, **商務詳細資訊**, **Web詳細資訊**.

   >[!NOTE]
   >
   >目前僅支援這些欄位群組。

   例如，如果您想要了解電子郵件促銷活動對商務資料（例如購買或訂購）的影響，您需要使用 **商務詳細資訊** 欄位群組。

   同樣地，如果您想要回報行動互動，則需要使用 **應用程式詳細資訊** 欄位群組。

   會列出與每個欄位群組對應的量度 [此處](#objective-list).

* 您可以將這些欄位群組新增至一或多個結構，以用於一或多個資料集。

>[!NOTE]
>
>如需XDM結構和欄位群組的詳細資訊，請參閱 [XDM系統概觀檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en){target=&quot;_blank&quot;}。

## 與每個欄位組對應的目標 {#objective-list}

下表顯示要新增哪些量度至 **[!UICONTROL Objectives]** 標籤。

| 欄位組 | 目標 |
|--- |--- |
| 商務詳細資訊 | 價格總計<br>付款金額<br>（不重複）結帳<br>（不重複）產品清單新增<br>（不重複）產品清單開啟<br>（不重複）移除產品清單<br>（不重複）產品清單檢視<br>（不重複）產品檢視<br>（不重複）購買<br>（唯一）為延遲儲存<br>產品價格合計<br>產品數量 |
| 應用程式詳細資訊 | （不重複）應用程式啟動<br>首次應用程式啟動<br>（唯一）應用程式安裝<br>（不重複）應用程式升級 |
| Web詳細資訊 | （不重複）頁面檢視 |

## 新增資料集 {#add-datasets}

1. 從 **[!UICONTROL ADMINISTRATION]** 菜單，選擇 **[!UICONTROL Configurations]**. 在  **[!UICONTROL Reporting]** ，按一下 **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   隨即顯示已新增的資料集清單。

1. 從 **[!UICONTROL Dataset]** 按一下 **[!UICONTROL Add dataset]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >如果您選取 **[!UICONTROL System dataset]** 索引標籤中，只會顯示系統建立的資料集。 您將無法新增其他資料集。

1. 從 **[!UICONTROL Dataset]** 下拉式清單中，選取您要用於報表的資料集。

   >[!CAUTION]
   >
   >您只能選取事件類型資料集，該資料集必須至少包含一個支援的 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;}: **應用程式詳細資訊**, **商務詳細資訊**, **Web詳細資訊**. 如果您選取的資料集不符合這些條件，便無法儲存變更。

   ![](assets/reporting-config-datasets.png)

   進一步了解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}。

1. 從 **[!UICONTROL Profile ID]** 下拉式清單中，選取要用來識別報表中每個設定檔的資料集欄位屬性。

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >僅顯示可用於報表的ID。

1. 此 **[!UICONTROL Use Primary ID namespace]** 選項。 如果選取 **[!UICONTROL Profile ID]** is **[!UICONTROL Identity Map]**，您可以停用此選項，然後從顯示的下拉式清單中選擇其他命名空間。

   ![](assets/reporting-config-namespace.png)

   進一步了解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}。

1. 儲存您的變更，將選取的資料集新增至報表設定清單。

   >[!CAUTION]
   >
   >如果您選取的資料集不是事件類型，則無法繼續。

建立促銷活動報表時，您現在可以看到與您新增資料集中使用之欄位群組相對應的量度。 前往 **[!UICONTROL Objectives]** 標籤，並選取您選取的量度，以更精確調整報表。 [深入了解](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>如果新增多個資料集，所有資料集的所有資料都可用於報表。

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
