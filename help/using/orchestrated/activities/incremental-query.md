---
solution: Journey Optimizer
product: journey optimizer
title: 使用增量查詢活動
description: 瞭解如何使用Adobe Journey Optimizer中的增量查詢活動，在協調的行銷活動中只定位新的設定檔。
feature: Campaigns
topic: Building campaigns
role: User
level: Intermediate
version: Campaign Orchestration
source-git-commit: 384f4e4b4c3acd9f1f1d73d4b140845870b31289
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 22%

---


# 增量查詢 {#incremental-query}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery"
>title="增量查詢"
>abstract="增量查詢是一種目標定位活動，每當協調的行銷活動執行時，就會執行資料庫查詢。 它只會傳回新記錄，並排除先前執行中已包含的任何人，因此您可以避免重新鎖定相同人員或重新匯出相同列。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery_processeddata"
>title="已處理的資料"
>abstract="在處理資料底下，選擇如何排除先前執行中的記錄。 透過使用日期欄位選項，活動使用所選的日期欄位而不是追蹤個別ID，並且每次執行只傳回日期在最後一次執行之後的列。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery_history"
>title="歷史記錄（天）"
>abstract="此設定控制該清單的保留時間。 0 值表示無限期保留；不會移除任何記錄。"

**[!UICONTROL 增量查詢]**&#x200B;活動是&#x200B;**[!UICONTROL 目標定位]**&#x200B;活動，每次執行協調的行銷活動時都會執行資料庫查詢。 重要部分是它只輸出&#x200B;**新**&#x200B;記錄。 會排除先前執行中擷取的任何人，以避免重新鎖定相同人員或重新匯出相同列。

當行銷活動可以執行多次時，例如當您排程行銷活動時（例如每週），或當行銷活動由外部訊號或API觸發時，可使用它。 每次執行只會鎖定上次執行未傳回的記錄，因此您可以避免重複專案。

一般用途：

* **傳訊與對象**：只將新註冊、新購買者或其他「自上次執行以來的新專案」區段提取至下一個步驟（例如電子郵件、簡訊）。
* **持續匯出**：只將新的或更新後的資料列傳送至檔案以供報表或BI工具使用，而不會複製您已匯出的資料。

當執行未傳回任何資料列時，協調的行銷活動會在&#x200B;**增量查詢**&#x200B;停止。 只有在有資料時（行銷活動再次執行時），增量查詢之後的活動才會執行。

## 設定增量查詢活動 {#incremental-query-configuration}

設定目標維度、建立查詢，然後選擇活動如何決定要從未來執行中排除哪些記錄。

1. 將&#x200B;**[!UICONTROL 增量查詢]**&#x200B;活動拖放到您的協調行銷活動中。

1. 在&#x200B;**[!UICONTROL 對象]**&#x200B;中，選取&#x200B;**[!UICONTROL 目標維度]** （例如收件者、訂閱者），然後按一下&#x200B;**[!UICONTROL 繼續]**。 深入瞭解[目標維度](../target-dimension.md)。

   ![](../assets/incremental-query.png)

1. 按一下&#x200B;**[!UICONTROL 新增條件]**&#x200B;以定義查詢。 [瞭解如何使用規則產生器](../orchestrated-rule-builder.md)。

   ![](../assets/incremental-query-2.png)

1. 在&#x200B;**[!UICONTROL 已處理的資料]**&#x200B;下，選擇您的&#x200B;**[!UICONTROL 日期欄位路徑]**。 屬性必須使用&#x200B;**日期時間**&#x200B;格式。 每次執行只傳回日期在最後一次執行之後的列。

   ![在協調的行銷活動畫布中的增量查詢活動設定](../assets/incremental-query-3.png)

<!--
   * **[!UICONTROL Exclude results of previous execution]**: The activity maintains a list of records returned in prior runs. Each run excludes those records and returns only new ones. **[!UICONTROL History in days]** controls the retention period for that list. 0 indicates indefinite retention, no records are removed.

   >[!IMPORTANT]
   >
   >This mode stores the primary key of each processed record. Personally identifiable information (PII) must not be used as the primary key.

-->

## 範例 {#incremental-query-example}

下列範例會傳送歡迎電子郵件給剛成為金會員的設定檔。 此行銷活動可排程為每週、每週一執行。 每次執行只會鎖定自上次執行以來符合金級成員資格的設定檔，因此每位收件者都會收到一次歡迎電子郵件。

* **[!UICONTROL 增量查詢]**：選取金會員。 第一次執行：所有目前的金會員。 稍後執行：僅自上次執行以來成為金會員的設定檔。
* **[!UICONTROL 電子郵件傳遞]**：透過查詢將歡迎電子郵件傳送至設定檔輸出。

![在協調的行銷活動畫布中的增量查詢活動設定](../assets/incremental-query-example.png)

