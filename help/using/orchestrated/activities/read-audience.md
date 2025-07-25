---
solution: Journey Optimizer
product: journey optimizer
title: 使用讀取客群活動
description: 了解如何在協調的行銷活動中使用讀取客群活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: c040ad5433d041f0f4f83fce46bc02662b77648f
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 37%

---

# 讀取對象 {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="建置客群活動"
>abstract="**讀取客群**&#x200B;活動可讓您選取將會進入協調的行銷活動客群。此刻群可以是現有的 Adobe Experience Platform 客群，或是從 CSV 檔案中提取的客群。在協調的行銷活動中傳送訊息時，不會在管道活動中定義訊息客群，而是在&#x200B;**讀取客群** 或&#x200B;**建置客群**&#x200B;活動中定義。"


+++ 目錄

| 歡迎使用協調行銷活動 | 首次投放的協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](../gs-schemas.md)</li><li>[手動結構描述](../manual-schema.md)</li><li>[檔案上傳結構描述](../file-upload-schema.md)</li><li>[擷取資料](../ingest-data.md)</li></ul>[存取及管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[同時加入](and-join.md) - [建立客群](build-audience.md) - [變更維度](change-dimension.md) - [頻道活動](channels.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調和](reconciliation.md) - [儲存客群](save-audience.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

**[!UICONTROL 讀取對象]**&#x200B;活動可讓您擷取現有的對象（先前儲存或匯入），並在協調的行銷活動中重複使用它。 此活動對於鎖定一組預先定義的設定檔而無須執行新的細分程式特別有用。

載入對象後，您可以選擇選取唯一的身分欄位，並使用其他設定檔屬性來豐富對象，以用於目標定位、個人化或報告目的，藉此調整對象。

## 設定讀取對象活動 {#read-audience-configuration}

請依照下列步驟設定&#x200B;**[!UICONTROL 讀取對象]**&#x200B;活動：

1. 將&#x200B;**[!UICONTROL 讀取對象]**&#x200B;活動新增至您協調的行銷活動。

   ![](../assets/read-audience-1.png)

1. 輸入活動的&#x200B;**[!UICONTROL 標籤]**。

1. 按一下![資料夾搜尋圖示](../assets/do-not-localize/folder-search.svg)，選取您要針對協調行銷活動鎖定的對象。

   ![](../assets/read-audience-2.png)

1. 從您的行銷活動目標維度中選擇&#x200B;**[!UICONTROL 實體&#x200B;]**。

   ➡️ [依照本頁面詳述的步驟建立您的行銷活動目標維度](../target-dimension.md)

   ![](../assets/read-audience-3.png)

1. 選取&#x200B;**[!UICONTROL 新增屬性]**，以使用其他資料擴充您選取的對象。 產生的對象將包含收件者清單，每個收件者都包含選取的設定檔屬性。

1. 選擇要新增至對象的&#x200B;**[!UICONTROL 屬性]**。

   ![](../assets/read-audience-4.png)

## 範例

在下列範例中，**[!UICONTROL 讀取對象]**&#x200B;活動是用來擷取先前建立和儲存的訂閱電子報之設定檔對象。 接著會使用&#x200B;**熟客方案會員資格**&#x200B;屬性來豐富對象，以定位已註冊熟客方案會員的使用者。

![](../assets/read-audience-5.png)
