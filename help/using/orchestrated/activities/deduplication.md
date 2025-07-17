---
solution: Journey Optimizer
product: journey optimizer
title: 使用重複資料刪除活動
description: 瞭解如何使用重複資料刪除活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 31%

---

# 重複資料刪除 {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="用於識別重複資料的欄位"
>abstract="在&#x200B;**&#x200B;用於識別重複資料的欄位&#x200B;**&#x200B;區段，按一下&#x200B;**&#x200B;新增屬性**&#x200B;按鈕以指定可允許識別重複資料之相同值的欄位，例如：電子郵件地址、名字、姓氏等。欄位的順序可讓您指定首要處理的條件。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="重複資料刪除活動"
>abstract="「**重複資料刪除**」活動可讓您刪除傳入活動結果中的重複資料。其主要在目標市場選擇活動之後和允許使用目標資料的活動之前使用。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="產生補集"
>abstract="您可以使用剩餘族群 (其已因重複而排除) 產生額外的傳出轉變。若要這樣做，請開啟「**產生補集**」選項"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="重複項目刪除設定"
>abstract="若要刪除傳入資料中的重複項目，請在以下欄位中定義重複項目刪除方法。預設只會保留一筆記錄。您還應該根據運算式或屬性選取重複項目刪除模式。預設會隨機選取要避免重複的記錄。"


+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](../gs-schemas.md)</li><li>[手動結構描述](../manual-schema.md)</li><li>[檔案上傳結構描述](../file-upload-schema.md)</li><li>[擷取資料](../ingest-data.md)</li></ul>[存取及管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重新鎖定目標](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建立對象](build-audience.md) - [變更維度](change-dimension.md) - [頻道活動](channels.md) - [合併](combine.md) - <b>[重複資料刪除](deduplication.md)</b> - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - [儲存對象](save-audience.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

**[!UICONTROL 重複資料刪除]**&#x200B;活動是&#x200B;**[!UICONTROL 鎖定目標]**&#x200B;活動。 此活動可讓您刪除入站活動結果中的重複專案，例如收件者清單中的重複設定檔。 **[!UICONTROL 重複資料刪除]**&#x200B;活動通常用於目標定位活動之後，以及允許使用目標定位資料的活動之前。

## 設定重複資料刪除活動{#deduplication-configuration}

請依照下列步驟設定&#x200B;**[!UICONTROL 重複資料刪除]**&#x200B;活動：


1. 將&#x200B;**[!UICONTROL 重複資料刪除]**&#x200B;活動新增至您協調的行銷活動。

1. 在&#x200B;**[!UICONTROL &#x200B;用於識別重複資料的欄位&#x200B;]**&#x200B;區段，按一下&#x200B;**[!UICONTROL &#x200B;新增屬性]**&#x200B;按鈕以指定可允許識別重複資料之相同值的欄位，例如：電子郵件地址、名字、姓氏等。欄位的順序可讓您指定首要處理的條件。

   ![](../assets/deduplication-1.png)

1. 在&#x200B;**[!UICONTROL 重複資料刪除設定]**&#x200B;區段中，選擇要使用[要保留的重複專案]欄位保留多少不重複記錄。 預設值為1，這會在每個重複群組保留一個記錄。 將其設為0可保留所有重複專案。

   例如，如果記錄A和B是Y的重複專案，而記錄C是Z的重複專案：

   * **如果欄位的值為1**：只保留Y和Z記錄。
   * **如果欄位的值為0**：會保留所有記錄(A、B、C、Y、Z)。
   * **如果欄位的值為2**：會保留C和Z，再加上A、B和Y中的兩個值，隨機或根據您的重複資料刪除方法。

1. 選擇&#x200B;**[!UICONTROL 重複資料刪除方法]**，這會定義系統如何決定要保留每組重複專案的記錄：

   * **[!UICONTROL 隨機選取]**：隨機選取要保留在重複專案外的記錄。
   * **[!UICONTROL 使用運算式]**：根據您定義的運算式，保留具有最高或最低值的記錄。
   * **[!UICONTROL 非空白值]**：保留所選欄位非空白的記錄，例如，僅保留具有電話號碼的設定檔。
   * **[!UICONTROL 依循值清單]**：可讓您優先處理一或多個欄位的特定值，例如，您可以優先處理「國家/地區」設定為「法國」的記錄。 按一下&#x200B;**[!UICONTROL 屬性]**&#x200B;以選擇欄位或建立自訂運算式。 使用&#x200B;**[!UICONTROL 新增按鈕]**&#x200B;以優先順序輸入偏好的值。

   ![](../assets/deduplication-2.png)

1. 如果要利用剩餘母體，請核取&#x200B;**[!UICONTROL 產生補充]**&#x200B;選項。 補充包含所有重複專案。 隨後會將其他轉變新增至活動。

## 範例{#deduplication-example}

在下列範例中，**[!UICONTROL 重複資料刪除]**&#x200B;活動用於在傳送傳遞前，從目標對象中移除重複記錄。 系統會先篩選對象，僅納入具有非空白電子郵件欄位的設定檔。 然後，**[!UICONTROL 重複資料刪除]**&#x200B;活動會使用電子郵件地址來識別和排除重複專案。

![](../assets/deduplication-3.png)
