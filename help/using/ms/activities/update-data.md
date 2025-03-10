---
solution: Journey Optimizer
product: journey optimizer
title: 在多步驟行銷活動中使用更新資料活動
description: 瞭解如何使用更新資料活動
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 13%

---

# 更新資料 {#update-data}

**更新資料**&#x200B;活動是&#x200B;**資料管理**&#x200B;活動。 它可讓您對資料庫中的欄位執行大量更新。 數個選項可讓您個人化資料更新。

<!--
The **Operation type** field lets you choose the process to be carried out on the data in the database. Select the first option to add data or update (it if it has already been added). You can also only add data, only update data, or delete data. Select the **Update and merge collections** to select a primary record to link duplicates to, and delete those duplicates safely

Specify how to identify the records in the database: if data relate to an existing targeting dimension, select the **Using the targeting dimension** option and select the targeting dimension and fields to update. Otherwise, specify one or more custom links to identify the data in the database, or direct use of reconciliation keys.

Select the fields to update and reconciliation settings. You can use the **Auto-mapping** option to automatically identify the fields to be updated.

The **Advanced options** section let you specify additional settings to manage data and duplicates.

Toggle the **Generate an outbound transition** option to add an outbound transition that will be activated at the end of the execution of the **Update data** activity. The update generally marks the end of a targeting workflow and therefore the option is not activated by default.

Toggle the **Generate an outbound transition for rejects** option to add an outbound transition containing records that have not been correctly processed after the update (for example if there is a duplicate). The update generally marks the end of a targeting workflow and therefore the option is not activated by default.
-->

## 設定更新資料活動{#update-data-configuration}

若要設定&#x200B;**更新資料**&#x200B;活動，請從將活動新增至您的多步驟行銷活動並定義標籤開始。

![](../assets/workflow-update-data.png)

### 作業型別

**作業型別**&#x200B;欄位可讓您選擇要對資料庫中的資料執行的程式：

* **插入或更新**：如果記錄已存在於資料庫中，請插入資料或更新資料。
* **插入**：僅插入資料。 不更新已存在的記錄。如果已定義調和標準，則僅會新增未調和的記錄。
* **更新**：只更新資料庫中已存在的記錄資料。
* **刪除**：刪除資料。

**批次大小**&#x200B;欄位可讓您選取要更新的入站轉變元素數目。 例如，如果您宣告500，則處理的前500筆記錄將會更新。

### 記錄識別

您可以在此段落指定如何識別資料庫中的記錄：

* 如果資料專案與現有目標維度相關，請選取&#x200B;**使用目標維度**&#x200B;選項，然後從&#x200B;**目標維度中選取要更新**&#x200B;欄位。
* 您也可以選取&#x200B;**使用自訂連結**，並指定一或多個連結，以識別資料庫中的資料
* 如果選取的作業型別需要更新，您必須使用&#x200B;**使用調解規則**&#x200B;選項。

### 要更新的欄位

在要更新的&#x200B;**欄位**&#x200B;區段中，新增將套用更新的欄位，並視需要新增條件，以執行此更新。 若要這麼做，請使用&#x200B;**Taken account if**&#x200B;欄位。 條件會依清單順序逐一套用。使用右邊的箭頭以變更更新順序。您可以多次使用相同的目的地欄位。

您可以使用&#x200B;**自動對應**&#x200B;按鈕自動連結欄位。 自動連結會偵測具有相同名稱的欄位。

在&#x200B;**插入或更新**&#x200B;作業型別期間，您可以個別選取要對每個欄位套用的作業。 若要這麼做，請在&#x200B;**作業型別**&#x200B;欄位中選取您想要的值。

### 進階選項

**進階選項**&#x200B;可讓您指定其他選項，以處理資料更新及管理重複專案。

<!--
* **Disable automatic key management**
* **Disable audit**
* **Empty the destination value if the source value is empty**
* **Update all columns with matching names**
* **Ignore records which concern the same target**: only the first in the list of expressions will be considered
-->

最後兩個選項可讓您執行特定動作：

* **產生出站轉變**：建立將在執行結束時啟用的出站轉變。 更新通常表示目標多步驟行銷活動的結束，因此預設不會啟用選項。

* **為拒絕產生出站轉變**：建立包含更新後未正確處理的記錄的出站轉變（例如，如果有重複記錄）。 更新通常會標籤目標多步驟行銷活動的結尾，因此預設不會啟用選項。
