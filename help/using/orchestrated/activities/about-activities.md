---
solution: Journey Optimizer
product: journey optimizer
title: 使用協調的行銷活動
description: 瞭解如何協調行銷活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: 22655a1ad08bb96d7fee86eb31b0542e4ea669c7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 29%

---

# 關於協調行銷活動 {#orchestrated-campaign-activities}

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[建立協調行銷活動的重要步驟](../gs-campaign-creation.md) | [建立協調的行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[使用協調的行銷活動傳送訊息](../send-messages.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用查詢Modeler](../orchestrated-rule-builder.md)<br/><br/>[建置您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建置對象](build-audience.md) - [變更維度](change-dimension.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

協調的行銷活動分為三個類別。 可用的活動可能會依據內容而有所不同。

以下各節會詳細介紹所有活動：

* [目標定位活動](#targeting)
* [管道活動](#channel)
* [流量控制活動](#flow-control)

![畫布中可用的活動清單](../assets/orchestrated-activities.png){width="80%" align="left"}

## 目標定位活動 {#targeting}

這些活動特定於定位。 這些活動可讓您使用交集、聯合或排除作業定義客群並分割或結合這些客群，從而建置一個或多個目標。

![目標定位活動清單](../assets/targeting-activities.png){width="40%" align="left"}

* [![建立對象](../assets/build-audience-icon.png)](build-audience.md)：定義您的目標母體。 您可以選取現有對象，或使用查詢建模器來定義您自己的查詢。
* [變更維度](change-dimension.md)：在建置您的協調行銷活動時，變更目標維度。
* [合併](combine.md)：對傳入母體執行分段。 您可以使用聯合、交集或排除。
* [重複資料刪除](deduplication.md)：刪除傳入活動結果中的重複專案。
* [擴充](enrichment.md)：定義要在您的協調行銷活動中處理的其他資料。 透過此活動，您可以利用傳入轉變並設定活動，以使用其他資料完成傳出轉變。
* [調解](reconciliation.md)：定義Journey Optimizer資料中的資料與工作表中的資料之間的連結，例如從外部檔案載入的資料。
* [分割](split.md)：將傳入母體分割成數個子集。

## 管道活動 {#channel}

Adobe Journey Optimizer可讓您跨多個管道自動執行行銷活動。 您可以將頻道活動結合到畫布中，以建立跨頻道協調的行銷活動，其可根據客戶行為觸發動作。 有下列&#x200B;**頻道**&#x200B;活動可用：電子郵件和簡訊。 [瞭解如何在協調的行銷活動內容中建立管道動作](channels.md)。

## 流程控制活動 {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="結束活動"
>abstract="**結束**&#x200B;活動讓您可以用圖形方式標記協調的行銷活動之結束。此活動並不會造成功能性影響，因此為選用。"

![流量控制活動清單](../assets/flow-control-activities.png){width="30%" align="left"}

下列活動是組織和執行協調行銷活動專屬的活動。 這些活動的主要任務是協調其他活動：

* [並加入](and-join.md)：同步處理協調行銷活動的多個執行分支。
* [分支](fork.md)：建立出站轉變，以同時啟動多個活動。
* [等待](wait.md)：暫時暫停執行部分協調的行銷活動。
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>**End**&#x200B;活動會以圖形方式標示已協調行銷活動的結尾。 此活動對功能沒有影響，因此是選用的
