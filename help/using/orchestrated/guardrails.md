---
solution: Journey Optimizer
product: journey optimizer
title: 協調的行銷活動護欄和限制
description: 瞭解協調的行銷活動護欄和限制
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 5%

---

# 護欄與限制 {#guardrails}

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](gs-schemas.md)</li><li>[手動結構描述](manual-schema.md)</li><li>[檔案上傳結構描述](file-upload-schema.md)</li><li>[擷取資料](ingest-data.md)</li></ul>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/>[重新鎖定目標](retarget.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建立對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [儲存對象](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

## 資料流對資料集的限制

Adobe Experience Platform中的每個資料集一次只能與一個作用中資料流相關聯。 此1:1基數由平台嚴格執行。

如果您需要切換資料來源(例如從Amazon S3切換至Salesforce)：

您必須刪除連線至資料集的現有資料流。

然後，使用對應至相同資料集的新來源建立新資料流。

這能確保可靠的資料擷取，且在使用「變更資料擷取」(CDC)時十分重要，因為增量更新需依賴定義的主索引鍵和版本設定屬性（例如lastmodified）。


## 關聯式結構描述/資料擷取限制

* 結構描述數 — 關聯式結構描述（關聯式資料存放區中的表格）的最大數量為200
* 關聯式結構描述大小 — Campaign Orchestration的關聯式結構描述大小上限為100GB。
* 資料擷取頻率 — Campaign Orchestration的批次資料擷取頻率不得超過每15分鐘一次。
* 變更/更新 — 指定關聯式結構描述的每日更新/變更應該少於記錄總數的20%
