---
solution: Journey Optimizer
product: journey optimizer
title: 協調的行銷活動護欄和限制
description: 瞭解協調的行銷活動護欄和限制
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 10%

---

# 護欄與限制 {#guardrails}

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](gs-schemas.md)</li><li>[手動結構描述](manual-schema.md)</li><li>[檔案上傳結構描述](file-upload-schema.md)</li><li>[擷取資料](ingest-data.md)</li></ul>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[同時加入](activities/and-join.md) - [建立客群](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調和](activities/reconciliation.md) - [儲存客群](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

## 資料流對資料集的限制

Adobe Experience Platform中的每個資料集一次只能與一個作用中資料流相關聯。 此1:1基數由平台強制執行。

如果您需要切換資料來源(例如從Amazon S3切換至Salesforce)：

您必須刪除連線至資料集的現有資料流。

然後，使用對應至相同資料集的新來源建立新資料流。

這能確保可靠的資料擷取，且在使用「變更資料擷取」(CDC)時十分重要，因為增量更新需依賴定義的主索引鍵和版本設定屬性（例如lastmodified）。


## 關聯式結構描述/資料擷取限制

* 關聯式資料存放區最多可支援200個關聯式結構描述（表格）。

* 用於Campaign Orchestration的關聯式結構描述總大小不應超過100 GB。

* Campaign Orchestration的批次擷取不應超過每15分鐘一次。

* 關聯式結構描述的每日變更應維持在記錄總數的20%以下。

## 資料模式

* 版本描述項在所有結構描述上都是強制性的，包括事實表格。

* 每個表格都需要主索引鍵。

* 資料集建立期間指派的table_name可用於區段UI和個人化功能。

  此名稱是永久性的，建立後即無法變更。

* 目前不支援欄位群組。

## 資料攝取

* 需要設定檔+關聯式資料擷取。

* 檔案式擷取需要變更型別欄位，而雲端資料庫擷取必須啟用表格記錄。 這是變更資料擷取(CDC)的必要專案。

* 在Snowflake中，從擷取到資料可用性的延遲時間介於15分鐘到2小時之間，端視資料量、並行和作業型別而定（插入比更新更快）。

* Snowflake中的資料監視正在開發中；目前沒有成功擷取的原生確認。

* 不支援直接更新Snowflake或資料集。 所有變更都必須透過CDC來源。

  查詢服務是唯讀的。

* 不支援ETL — 客戶必須以必要格式提供資料。

* 不允許部分更新。 每一列都必須作為完整記錄提供。

* 擷取仰賴查詢服務和資料Distiller。

## 分段

* LOV （值清單）和列舉目前可供使用。

* 已儲存的對象是靜態清單，其內容反映執行行銷活動時可用的資料。

* 不支援附加至已儲存的對象。 更新內容需要完全覆寫。

* 對象必須僅包含純量屬性；不支援對應和陣列。

* 分段主要支援關聯式資料。 雖然允許與設定檔資料混合，但引進大型設定檔資料集可能會影響效能。 若要防止此情況：

* 已設立護欄，例如限制在批次或串流對象中選取的設定檔屬性數量。

* 讀取對象不會快取 — 每次行銷活動執行都會觸發完全讀取。

  大型或複雜受眾需要最佳化。