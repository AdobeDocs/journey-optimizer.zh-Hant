---
solution: Journey Optimizer
product: journey optimizer
title: 設定步驟
description: 瞭解如何透過上傳DDL在Adobe Experience Platform中建立關聯式結構描述
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 88eb1438-0fe5-4a19-bfb6-2968a427e9e8
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 57%

---

# 使用DDL檔案建立關聯式結構描述 {#file-upload-schema}

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](gs-schemas.md)</li><li>[手動結構描述](manual-schema.md)</li><li>[檔案上傳結構描述](file-upload-schema.md)</li><li>[擷取資料](ingest-data.md)</li></ul>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[同時加入](activities/and-join.md) - [建立客群](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調和](activities/reconciliation.md) - [儲存客群](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

透過建立結構描述（例如&#x200B;**忠誠會員資格**、**忠誠度交易**&#x200B;和&#x200B;**忠誠度獎勵**），定義協調行銷活動所需的關聯式資料模型。 每個結構描述都必須包含主索引鍵、版本設定屬性以及適當的關聯性，以參照實體，例如&#x200B;**收件者**&#x200B;或&#x200B;**品牌**。

您可以透過介面手動建立結構描述，或使用DDL檔案大量匯入結構描述。

本章節提供如何透過上傳 DDL (資料定義語言) 檔案，可在 Adobe Experience Platform 中建立關聯式結構描述的逐步指南。使用 DDL 檔案，讓您可以預先定義資料模式的結構，包括表格、屬性、索引鍵和關係。

1. [上傳DDL檔案](#ddl-upload)以建立關聯式結構描述並定義其結構。

1. [定義資料模型中資料表之間的關係](#relationships)。

1. [連結結構描述](#link-schema)以連線您的關聯式資料與現有的設定檔實體，例如收件者或品牌。

1. [從支援的來源將資料](ingest-data.md)擷取到您的資料集中。

## 上傳DDL檔案{#ddl-upload}

透過上傳DDL檔案，您可以預先定義資料模型的結構，包括表格、屬性、索引鍵和關係。

支援以Excel為基礎的結構描述檔案上傳。 下載[提供的範本](assets/template.zip)以輕鬆準備您的結構描述定義。

+++在Adobe Experience Platform中建立關聯式結構時，支援下列功能

* **列舉**\
  以DDL為基礎和手動建立結構描述均支援ENUM欄位，可讓您使用一組固定的允許值來定義屬性。

* 資料控管的&#x200B;**結構描述標籤**\
  架構欄位層級支援標籤功能，可強制資料治理原則，例如存取控制和使用限制。 如需詳細資訊，請參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)。

* **複合索引鍵**\
  關聯式結構描述定義支援複合主索引鍵，可一起使用多個欄位以唯一識別記錄。

+++

1. 登入Adobe Experience Platform。

1. 導覽至&#x200B;**資料管理** > **結構描述**&#x200B;功能表。

1. 按一下&#x200B;**建立結構描述**。

1. 選取&#x200B;**[!UICONTROL 關聯式]**&#x200B;作為您的&#x200B;**結構描述型別**。

   ![](assets/admin_schema_1.png)

1. 選取&#x200B;**[!UICONTROL 匯入 DDL 檔案]**，以便定義實體關係圖，同時建立結構描述。

   表格結構必須包含以下元素：
   * 至少有單一主索引鍵
   * 版本識別碼，例如`lastmodified`欄位類型`datetime`或`number`。
   * 針對變更資料擷取(CDC)擷取，為名為`_change_request_type`且型別為`String`的特殊欄，其指示資料變更的型別（例如，插入、更新、刪除）並啟用增量處理


   >[!IMPORTANT]
   >
   > 任何用於定位的結構描述都必須包含至少一個型別`String`的身分欄位，並具有相關聯的&#x200B;**身分名稱空間**。\
   >這可確保與Adobe Journey Optimizer的定位和身分解析功能相容。

1. 拖放 DDL 檔案，然後按一下&#x200B;**[!UICONTROL 下一步]**。

   請注意，支援的DDL檔案大小上限為10MB。

1. 輸入&#x200B;**[!UICONTROL 結構描述名稱]**。

1. 設定每個結構描述及欄位，確定已指定主索引鍵。

   必須指定單一屬性，例如`lastmodified`，做為版本描述項。這個屬性通常是`datetime`、`long`或`int`類型，為內嵌程式所必須，確保資料集完成最新資料版本更新。

   ![](assets/admin_schema_2.png)

1. 完成後，請按一下&#x200B;**[!UICONTROL 完成]**。

目前可以在畫布內，驗證表格和欄位定義。[請參閱下列章節深入了解](#entities)

## 定義關係 {#relationships}

若想定義結構描述內所有表格之間的邏輯連線，請遵循下列步驟操作。

1. 存取資料模式的畫布視圖，然後選擇您想連結的兩個表格

1. 按一下來源聯結旁的![](assets/do-not-localize/Smock_AddCircle_18_N.svg)按鈕，然後拖放並導引箭頭朝向目標聯結，以便建立連線。

   ![](assets/admin_schema_5.png)

1. 請填寫指定表單，以便定義連結，並在完成設定後，按一下&#x200B;**套用**。

   ![](assets/admin_schema_3.png)

   **基數**：

   * **1-N**：來源表格的單一發生次數可以擁有眾多目標表格對應的發生次數，但目標表格的單一發生次數，最多只可以擁有來源表格的單一對應發生次數。

   * **N-1**：目標表格的單一發生次數可以擁有眾多來源表格對應的發生次數，但來源表格單一發生次數，最多只可以擁有目標表格的單一對應發生次數。

   * **1-1**：來源表格的單一發生次數，最多可以擁有目標表格對應的單一發生次數。

1. 資料模式中定義的所有連結，全都會顯示在畫布視圖下方，會以箭頭表示。 請按一下兩個表格之間的箭頭，即可檢視詳細資訊，進行編輯，或可視需要移除連結。

   ![](assets/admin_schema_6.png)

1. 使用工具列，即可自訂、調整您的畫布。

   ![](assets/toolbar.png)

   * **放大顯示**：放大畫布，即可更清楚地檢視資料模式的詳細資料。

   * **縮小顯示**：縮小畫布大小，以便廣泛地檢視您的資料模式。

   * **符合視圖**：調整縮放，即可符合可見區域中的所有結構描述。

   * **篩選器**：請選擇想要顯示在畫布中的結構描述。

   * **強制自動版面**：自動排列結構描述，以便以更好的方式組織內容。

   * **顯示地圖**：切換迷你地圖覆蓋，即可協助瀏覽大型或複雜的結構描述版面配置。

1. 完成後，請按一下&#x200B;**儲存**。 此動作會建立結構描述、相關資料集，同時啟用資料集，即可用於協調行銷活動。

1. 請按一下&#x200B;**[!UICONTROL 開啟工作]**，以便監視建立工作的進度。 此流程可能需要幾分鐘的時間，全視 DDL 檔案中定義的表格數目而定。

   您也可以開啟&#x200B;**[!UICONTROL 上傳DDL檔案]**&#x200B;視窗並選取&#x200B;**[!UICONTROL 檢視所有關聯式工作]**，以存取關聯式工作。

   ![](assets/admin_schema_4.png)

## 連結結構描述 {#link-schema}

>[!IMPORTANT]
>
> 系統只會辨識DDL檔案中明確定義的關係。 任何存在於DDL檔案外部的實體關係都會被忽略且不處理。

請在&#x200B;**忠誠度交易**&#x200B;結構描述與&#x200B;**收件者**&#x200B;結構描述之間，建立關係，以便將每次交易和對的客戶記錄之間建立起關係。

1. 瀏覽至&#x200B;**[!UICONTROL 結構描述]**，開啟之前建立的&#x200B;**忠誠度交易**。

1. 按一下客戶&#x200B;**[!UICONTROL 欄位屬性]**&#x200B;中的&#x200B;**[!UICONTROL 新增關係]**。

   ![](assets/schema_1.png)

1. 選取&#x200B;**[!UICONTROL 多對一]**&#x200B;作為關係&#x200B;**[!UICONTROL 類型]**。

1. 連結至現有的&#x200B;**收件者**&#x200B;結構描述。

   ![](assets/schema_2.png)

1. 輸入來自&#x200B;**目前結構描述的關係名稱**&#x200B;[!UICONTROL &#x200B;以及&#x200B;]&#x200B;**來自參考結構描述的關係名稱**。

1. 按一下&#x200B;**[!UICONTROL 套用]**，以便儲存變更內容。

繼續建立&#x200B;**忠誠度獎勵**&#x200B;結構描述與&#x200B;**品牌**&#x200B;結構描述之間的關係，在每個獎勵輸入與合適品牌之間建立關聯。

![](assets/schema_3.png)


<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->
