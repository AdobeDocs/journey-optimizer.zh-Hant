---
solution: Journey Optimizer
product: journey optimizer
title: 使用協調的行銷活動
description: 瞭解如何協調行銷活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: e71cbc5b29a31e2f23b408ae8c8b73379a44275d
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 59%

---

# 關於協調的行銷活動 {#orchestrated-campaign-activities}


+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](../gs-schemas.md)</li><li>[手動結構描述](../manual-schema.md)</li><li>[檔案上傳結構描述](../file-upload-schema.md)</li><li>[擷取資料](../ingest-data.md)</li></ul>[存取及管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | <b>[開始使用活動](about-activities.md)</b><br/><br/>活動：<br/>[同時加入](and-join.md) - [建立客群](build-audience.md) - [變更維度](change-dimension.md) - [頻道活動](channels.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調和](reconciliation.md) - [儲存客群](save-audience.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

可將協調行銷活動歸類成三大類別。可用的活動可能會依據內容而有所不同。

以下各節會詳細介紹所有活動：

* [目標定位活動](#targeting)
* [頻道活動](#channel)
* [流量控制活動](#flow-control)

![畫布中的可用活動清單](../assets/orchestrated-activities.png){width="80%" align="left"}

## 目標定位活動 {#targeting}

這些活動會鎖定目標定位。 這些活動可讓您使用交集、聯合或排除作業定義客群，同時對其進行分割或結合，從而建置一個或多個目標。

![目標定位活動清單](../assets/targeting-activities.png){width="40%" align="left"}

* [建立客群](build-audience.md)：定義目標族群。 您可以選取現有客群或使用規則建置器定義自己的查詢。
* [變更維度](change-dimension.md)：在建置您的協調行銷活動時變更目標維度。
* [合併](combine.md)：針對傳入族群，執行細分。 您可以使用聯合、交集或排除。
* [重複資料刪除](deduplication.md)：刪除傳入活動結果中的重複項目。
* [擴充](enrichment.md)：定義要在您的協調行銷活動中處理的其他資料。 透過此活動，您可以利用傳入轉變並設定活動，以使用其他資料完成傳出轉變。
* [調和](reconciliation.md)：定義 Journey Optimizer資料中的資料與工作表中資料之間的連結，例如從外部檔案載入的資料。
* [分割](split.md)：將傳入族群分割成許多子集。

## 頻道活動 {#channel}

Adobe Journey Optimizer 讓您能夠跨越多重管道，自動執行行銷活動。您可以將頻道活動結合到畫布中，以建立跨頻道協調的行銷活動，其可以根據客戶行為來觸發動作。 還可以使用下列&#x200B;**頻道**&#x200B;活動：電子郵件和簡訊。 [瞭解如何在協調的行銷活動內容中建立管道動作](channels.md)。

## 流量控制活動 {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="結束活動"
>abstract="**End**&#x200B;活動可讓您以圖形方式標示已協調行銷活動的結尾。 此活動並不會造成功能性影響，因此為選用。"

![流量控制活動清單](../assets/flow-control-activities.png){width="30%" align="left"}

下列活動是組織和執行「協調的行銷活動」專屬的活動。 這些活動的主要任務是協調其他活動：

* [並加入](and-join.md)：同步處理協調行銷活動的多個執行分支。
* [分支](fork.md)：可讓您建立傳出轉變，以便同時啟動許多活動。
* [等待](wait.md)：暫時暫停執行部分協調的行銷活動。
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>**End**&#x200B;活動會以圖形方式標示已協調行銷活動的結尾。 此活動並不會造成功能性影響，因此為選用
