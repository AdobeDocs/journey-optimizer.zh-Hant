---
solution: Journey Optimizer
product: journey optimizer
title: 設定Journey Optimizer報表以進行實驗
description: 瞭解如何設定報告資料來源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
keywords: 設定，實驗，報告，最佳化工具
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 066bceb078f619e75e5776764f534619d5a0bd5a
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 28%

---

# 設定用於實驗的報告 {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="設定資料集以進行報告"
>abstract="報告設定可讓您擷取將在行銷活動報表的「物件」索引標籤中使用的其他量度。必須由技術使用者執行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="選取資料集"
>abstract="您只能選取一個事件類型的資料集，該資料集必須至少包含一個受支援的欄位群組：應用程式詳細資訊、商務詳細資訊、Web 詳細資訊。"

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

報告資料來源設定可讓您擷取將用於以下專案的其他量度： **[!UICONTROL 目標]** 標籤內的任何專案。 [了解更多](content-experiment.md#objectives-global)

>[!NOTE]
>
>報告設定必須由技術使用者執行。 <!--Rights?-->

對於此設定，您需要新增一個或多個資料集，其中包含您要用於報告的其他元素。 若要這麼做，請遵循步驟 [以下](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## 先決條件


您必須先建立該資料集，才能將資料集新增至報表設定。 瞭解如何在 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#create){target="_blank"}.

* 您只能新增事件型別資料集。

* 這些資料集必須至少包含下列其中一項 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target="_blank"}： **應用程式詳細資料**， **商務詳細資料**， **網頁詳細資訊**.

   >[!NOTE]
   >
   >目前僅支援這些欄位群組。

   例如，如果您想瞭解電子郵件行銷活動對商業資料（如購買或訂單）的影響，則需要使用建立體驗事件資料集 **商務詳細資料** 欄位群組。

   同樣地，如果您想要報告行動互動，則需要建立體驗事件資料集， **應用程式詳細資料** 欄位群組。

   會列出與每個欄位群組對應的量度 [此處](#objective-list).

* 您可以將這些欄位群組新增到一個或多個方案中，這些方案將用於一個或多個資料集。

>[!NOTE]
>
>瞭解更多關於XDM結構描述和欄位群組 [XDM系統概觀檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.

## 對應至每個欄位群組的目標 {#objective-list}

下表顯示要將哪些量度新增至 **[!UICONTROL 目標]** 標籤中每個欄位群組的行銷活動報告。

| 欄位群組 | 目標 |
|--- |--- |
| 商務詳細資料 | 總價<br>付款金額<br>（不重複）結帳<br>（不重複）產品清單新增<br>（唯一）產品清單開啟<br>（獨特）產品清單移除<br>（不重複）產品清單檢視<br>（不重複）產品檢視<br>（不重複）購買<br>（不重複）儲存供日後使用<br>產品總價<br>產品數量 |
| 應用程式詳細資料 | （不重複）應用程式啟動次數<br>首次應用程式啟動<br>（不重複）應用程式安裝次數<br>（不重複）應用程式升級 |
| 網頁詳細資訊 | （不重複）頁面檢視 |

## 新增資料集 {#add-datasets}

1. 從 **[!UICONTROL 管理]** 功能表，選取 **[!UICONTROL 設定]**. 在  **[!UICONTROL 報告]** 區段，按一下 **[!UICONTROL 管理]**.

   ![](assets/reporting-config-menu.png)

   將顯示已新增的資料集清單。

1. 從 **[!UICONTROL 資料集]** 標籤，按一下 **[!UICONTROL 新增資料集]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >如果您選取 **[!UICONTROL 系統資料集]** 索引標籤中，只會顯示由系統建立的資料集。 您將無法新增其他資料集。

1. 從 **[!UICONTROL 資料集]** 下拉式清單，選取您要用於報告的資料集。

   >[!CAUTION]
   >
   >您只能選取事件型別資料集，該資料集必須至少包含一個受支援的 [欄位群組](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant#field-group){target="_blank"}： **應用程式詳細資料**， **商務詳細資料**， **網頁詳細資訊**. 如果選取的資料集與這些條件不相符，將無法儲存變更。

   ![](assets/reporting-config-datasets.png)

   進一步瞭解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hant){target="_blank"}.

1. 從 **[!UICONTROL 設定檔ID]** 從下拉式清單中，選取用於識別報告中每個設定檔的資料集欄位屬性。

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >只顯示可用於報告的 ID。

1. 此 **[!UICONTROL 使用主要ID名稱空間]** 選項預設為啟用。 若已選取 **[!UICONTROL 設定檔ID]** 是 **[!UICONTROL 身分對應]**，您可以停用此選項，然後從顯示的下拉式清單中選擇另一個名稱空間。

   ![](assets/reporting-config-namespace.png)

   進一步瞭解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hant){target="_blank"}.

1. 儲存變更以將選取資料集新增到報告設定清單。

   >[!CAUTION]
   >
   >如果選取了非事件類型的資料集，則無法繼續。

建立行銷活動報表時，您現在可以看到與您新增的資料集中使用的欄位群組相對應的量度。 前往 **[!UICONTROL 目標]** 標籤並選取您選擇的量度，以更精細地調整報表。 [了解更多](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>如果新增多個資料集，則所有資料集中的所有資料都可用於報告。

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
