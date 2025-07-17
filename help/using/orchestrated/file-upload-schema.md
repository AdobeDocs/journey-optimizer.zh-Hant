---
solution: Journey Optimizer
product: journey optimizer
title: 設定步驟
description: 瞭解如何透過上傳DDL在Adobe Experience Platform中建立關聯式結構描述
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 1%

---

# 檔案上傳 {#file-upload-schema}

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[手動結構描述](manual-schema.md)</li><li>[檔案上傳結構描述](file-upload-schema.md)</li><li>[擷取資料](ingest-data.md)</li></ul><br/><br/>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/>[重新鎖定目標](retarget.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建立對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [儲存對象](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

透過建立結構描述（例如&#x200B;**忠誠會員資格**、**忠誠度交易**&#x200B;和&#x200B;**忠誠度獎勵**），定義協調行銷活動所需的關聯式資料模型。 每個結構描述都必須包含主索引鍵、版本設定屬性以及適當的關聯性，以參照&#x200B;**收件者**&#x200B;或&#x200B;**品牌**&#x200B;等實體。

您可以透過介面手動建立結構描述，或使用DDL檔案大量匯入結構描述。

本節提供如何透過上傳DDL （資料定義語言）檔案在Adobe Experience Platform中建立關聯式綱要的逐步指南。 使用DDL檔案可讓您預先定義資料模型的結構，包括表格、屬性、索引鍵和關係。

## DDL檔案上傳 {#ddl-upload}

1. 登入Adobe Experience Platform。

1. 導覽至&#x200B;**資料管理** > **結構描述**。

1. 按一下&#x200B;**建立結構描述**。

1. 系統會提示您選取兩種結構描述型別：

   * **標準**
   * **關聯式**，專門用於協調的行銷活動

   ![](assets/admin_schema_1.png)

1. 選取&#x200B;**上傳DDL檔案**&#x200B;以定義實體關聯圖並建立結構描述。

   表格結構必須包含：
   * 至少一個主索引鍵
   * 版本識別碼，例如`lastmodified`或`datetime`型別的`number`欄位。

1. 拖放您的DDL檔案，然後按一下&#x200B;**[!UICONTROL 下一步]**。

1. 輸入您的&#x200B;**[!UICONTROL 結構描述名稱]**。

1. 設定每個結構描述及其欄，確定已指定主索引鍵。

   必須指定一個屬性（例如`lastmodified`）做為版本描述項。 這個屬性（通常是`datetime`、`long`或`int`型別）是內嵌程式所必須的，以確保資料集以最新資料版本更新。

   ![](assets/admin_schema_2.png)

1. 按一下&#x200B;**[!UICONTROL 完成]**。

您現在可以在畫布內驗證表格和欄位定義。 [在下列章節中瞭解更多](#entities)

## 定義關係 {#relationships}

若要定義架構內各表格之間的邏輯連線，請遵循下列步驟。

1. 存取資料模型的畫布檢視，並選擇您要連結的兩個表格

1. 按一下Source加入旁的![](assets/do-not-localize/Smock_AddCircle_18_N.svg)按鈕，然後拖曳並引導箭頭朝向Target加入以建立連線。

   ![](assets/admin_schema_5.png)

1. 填寫指定的表單以定義連結，並在設定後按一下&#x200B;**套用**。

   ![](assets/admin_schema_3.png)

   **基數**：

   * **1-N**：來源表格的一個出現次數可以具有多個目標表格的對應出現次數，但目標表格的一個出現次數最多可以具有來源表格的一個對應出現次數。

   * **N-1**：目標表格的一個出現次數可以有來源表格的多個對應出現次數，但來源表格的一個出現次數最多可以有目標表格的對應出現次數。

   * **1-1**：來源資料表的一個執行個體最多可以具有目標資料表的一個對應執行個體。

1. 資料模型中定義的所有連結都會在畫布檢視中以箭頭表示。 按一下兩個表格之間的箭頭，即可檢視詳細資訊、進行編輯或視需要移除連結。

   ![](assets/admin_schema_6.png)

1. 使用工具列來自訂和調整您的畫布。

   ![](assets/toolbar.png)

   * **放大**：放大畫布以更清楚檢視資料模型的詳細資料。

   * **縮小**：縮小畫布大小，以更廣的檢視您的資料模型。

   * **符合檢視**：調整縮放以符合可見區域中的所有結構描述。

   * **篩選器**：選擇要顯示在畫布中的結構描述。

   * **強制自動配置**：自動排列結構描述以取得更好的組織。

   * **顯示地圖**：切換迷你地圖覆蓋，以更輕鬆地導覽大型或複雜的結構描述配置。

1. 完成時，按一下&#x200B;**儲存**。 此動作會建立結構描述和相關聯的資料集，並啟用資料集以用於協調的行銷活動。

1. 按一下&#x200B;**[!UICONTROL 開啟工作]**&#x200B;以監視建立工作的進度。 此程式可能需要幾分鐘的時間，視DDL檔案中定義的表格數量而定。

   ![](assets/admin_schema_4.png)

## 連結綱要 {#link-schema}

在&#x200B;**熟客交易**&#x200B;結構描述與&#x200B;**收件者**&#x200B;結構描述之間建立關係，以將每個交易與正確的客戶記錄建立關聯。

1. 瀏覽至&#x200B;**[!UICONTROL 結構描述]**，並開啟您先前建立的&#x200B;**熟客方案交易**。

1. 按一下客戶&#x200B;**[!UICONTROL 欄位屬性]**&#x200B;中的&#x200B;**[!UICONTROL 新增關係]**。

   ![](assets/schema_1.png)

1. 選取&#x200B;**[!UICONTROL 多對一]**&#x200B;做為關聯性&#x200B;**[!UICONTROL 型別]**。

1. 連結至現有的&#x200B;**收件者**&#x200B;結構描述。

   ![](assets/schema_2.png)

1. 輸入來自目前結構描述&#x200B;**[!UICONTROL 的]**&#x200B;關聯性名稱以及來自參考結構描述&#x200B;**[!UICONTROL 的]**&#x200B;關聯性名稱。

1. 按一下&#x200B;**[!UICONTROL 套用]**&#x200B;以儲存變更。

繼續建立&#x200B;**忠誠度獎勵**&#x200B;結構描述與&#x200B;**品牌**&#x200B;結構描述之間的關係，將每個獎勵專案與適當的品牌建立關聯。

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