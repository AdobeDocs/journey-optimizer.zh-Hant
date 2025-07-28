---
solution: Journey Optimizer
product: journey optimizer
title: 設定步驟
description: 瞭解如何從支援的來源（例如SFTP、雲端儲存空間或資料庫）將資料匯入Adobe Experience Platform。
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 36%

---

# 擷取資料 {#ingest-data}

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集</br> <ul><li>[開始使用結構描述和資料集](gs-schemas.md)</li><li>[手動結構描述](manual-schema.md)</li><li>[檔案上傳結構描述](file-upload-schema.md)</li><li>[擷取資料](ingest-data.md)</li></ul>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[同時加入](activities/and-join.md) - [建立客群](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調和](activities/reconciliation.md) - [儲存客群](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>若要變更資料集的資料來源，您必須先刪除現有的資料流，才能建立參照相同資料集和新來源的新資料流。
>
>Adobe Experience Platform在資料流和資料集之間實施嚴格的一對一關係。 這可讓您維持來源與資料集之間的同步，以取得精確的增量擷取。

Adobe Experience Platform 讓您可以從外部來源擷取資料，同時可以使用 Experience Platform 服務來建立、加標籤，同時強化傳入資料。 您可以從多種來源 (如 Adobe 應用程式、雲端型儲存空間、資料庫和其他許多來源) 擷取資料。 

## 協調行銷活動的支援來源 {#supported}

下列來源支援搭配協調行銷活動使用：

<table>
  <thead>
    <tr>
      <th>類型</th>
      <th>來源</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">雲端儲存空間</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Google Cloud Storage</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">雲端資料倉儲</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">資料登陸區域<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">檔案式上傳</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">本機檔案上傳<a></td>
    </tr>

</tbody>
</table>

## 設定資料流

此範例示範如何設定將結構化資料擷取至Adobe Experience Platform的資料流程。 設定的資料流程支援自動化、排程擷取，並可啟用即時更新。

1. 請從&#x200B;**[!UICONTROL 連線]**&#x200B;選單那邊，存取&#x200B;**[!UICONTROL 來源]**&#x200B;選單。

1. 根據[協調行銷活動的支援來源](#supported)選擇您的來源。

   ![](assets/admin_sources_1.png)

1. 如果您選擇雲端型來源，請連線您的雲端儲存空間或Google雲端儲存空間帳戶。

   ![](assets/admin_sources_2.png)

1. 選擇您要擷取至Adobe Experience Platform的資料。

   ![](assets/S3_config_1.png)

1. 從&#x200B;**[!UICONTROL 資料集詳細資料]**&#x200B;頁面，勾選&#x200B;**[!UICONTROL 啟用變更資料擷取]**，以僅顯示對應到關聯式結構描述並包含主索引鍵和版本描述項的資料集。

   >[!IMPORTANT]
   >
   > 僅針對&#x200B;**檔案型來源**，資料檔案中的每一列都必須包含值為`_change_request_type` (upsert)或`U` (delete)的`D`欄。 若沒有此欄，系統不會將資料識別為支援變更追蹤，且不會出現「協調的行銷活動」切換，導致資料集無法選取以進行目標定位。

   ![](assets/S3_config_6.png)

1. 選取您先前建立的資料集，然後按一下&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/S3_config_3.png)

1. 如果您只使用檔案型來源，請從&#x200B;**[!UICONTROL 選取資料]**&#x200B;視窗，上傳本機檔案並預覽其結構和內容。

   請注意，支援的大小上限為100MB。

1. 請在&#x200B;**[!UICONTROL 對應]**&#x200B;視窗中，確認每個來源檔案屬性，都有正確對應到目標結構描述中的對應欄位。

   完成後，請按一下&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/S3_config_4.png)

1. 請根據想要的頻率，設定資料流量的&#x200B;**[!UICONTROL 排程]**。

1. 按一下&#x200B;**[!UICONTROL 完成]**，以便建立資料流一般會根據定義的排程自動執行。

1. 從&#x200B;**[!UICONTROL 連線]**&#x200B;選單中，選取&#x200B;**[!UICONTROL 來源]**&#x200B;並存取&#x200B;**[!UICONTROL 資料流]**&#x200B;索引標籤，以追蹤流量執行、檢閱擷取的記錄，以及疑難排解任何錯誤。

   ![](assets/S3_config_5.png)

