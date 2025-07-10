---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer開始和監視協調的行銷活動
description: 瞭解如何使用Adobe Journey Optimizer開始及監控協調的行銷活動。
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 0ae8372c179707a87a6b512a5420753a4aaef754
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 2%

---

# 建立重新定位查詢 {#retarget}

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](configuration-steps.md)<br/><br/>[存取和管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/><b>[重新鎖定目標](retarget.md)</b> | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建立對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [儲存對象](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

檔案處理中

>[!ENDSHADEBOX]

重新目標定位可讓您根據收件者對先前協調之行銷活動的回應方式，來追蹤收件者。 例如，您可以傳送第二封電子郵件給已收到但未點按第一封的設定檔。

協調的行銷活動提供此專案的兩個主要資料來源：

- **訊息回饋**：擷取傳遞相關的事件，例如已傳送、已開啟、已退回的訊息等。

- **電子郵件追蹤**：擷取使用者動作，例如點按和開啟。

## 建立意見反應式重新目標定位規則

回饋式重新目標定位規則可讓您根據&#x200B;**訊息回饋**&#x200B;資料集中擷取的訊息傳遞事件，重新目標定位收件者。 這些事件包括已傳送、已開啟、已退回或標示為垃圾郵件的郵件等結果。

使用此資料，您可以定義規則來識別收到先前訊息但未與其互動的收件者，以啟用根據特定傳送狀態的後續通訊。

1. 建立新的&#x200B;**協調的行銷活動**。

2. 新增&#x200B;**建置對象**&#x200B;活動，並將目標維度設為&#x200B;**收件者(caas)**。

3. 在&#x200B;**規則產生器**&#x200B;中，按一下&#x200B;**新增條件**&#x200B;並從屬性選擇器選取&#x200B;**訊息回饋**。 按一下「**確認**」。

4. 新增&#x200B;**意見狀態**&#x200B;的條件，並將值設定為&#x200B;**已傳送的訊息**。

5. 若要鎖定特定協調的行銷活動：

   - 新增其他條件、搜尋`entity`，並導覽至：\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`。

   - 選取&#x200B;**協調的行銷活動名稱**&#x200B;並指定行銷活動名稱。

6. 若要鎖定該協調行銷活動中的特定訊息或活動：

   - 新增其他條件、搜尋`entity`，並導覽至：\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`。

   - 選取&#x200B;**協調的行銷活動動作名稱**&#x200B;並指定行銷活動動作名稱。

     按一下畫布中活動旁的![資訊圖示](assets/do-not-localize/info-icon.svg)，即可找到動作名稱。

   >[!TIP]
   >
   >您也可以依&#x200B;**促銷活動ID** (UUID)進行篩選，而不使用名稱，您可在促銷活動屬性中找到該篩選器。

## 建立追蹤型重新鎖定目標規則

追蹤式重新目標定位規則會使用&#x200B;**電子郵件追蹤**&#x200B;資料集的資料，根據收件者與訊息的互動來鎖定收件者。 它會擷取使用者動作，例如電子郵件開啟和連結點按。

若要根據訊息互動（例如，開啟或按一下）重新鎖定收件者，請依照下列方式使用&#x200B;**電子郵件追蹤**&#x200B;實體：

1. 建立新的&#x200B;**協調的行銷活動**，然後新增具有&#x200B;**收件者(caas)**&#x200B;的&#x200B;**建立對象**&#x200B;活動作為目標維度，以著重處理先前協調的行銷活動收件者。

1. 新增&#x200B;**電子郵件追蹤**&#x200B;的條件。 按一下&#x200B;**確認**&#x200B;以建立「電子郵件追蹤存在，例如」條件。

1. 在該條件內，新增條件並搜尋&#x200B;**互動型別**&#x200B;屬性。

1. 從自訂條件選項中，使用&#x200B;**包含在**&#x200B;中作為運運算元，並根據您的使用案例選取一或多個值。 例如：
   - **已開啟訊息**
   - **訊息連結已點按**

1. 若要將追蹤資料與特定行銷活動建立關聯：

   - 在電子郵件追蹤區塊中新增條件。

   - 瀏覽至`_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`。

   - 為&#x200B;**協調的行銷活動名稱**&#x200B;新增條件，如有需要，也為&#x200B;**協調的行銷活動動作名稱**&#x200B;新增條件。

     按一下畫布中活動旁的![資訊圖示](assets/do-not-localize/info-icon.svg)，即可找到動作名稱。

   >[!TIP]
   >
   >您也可以依&#x200B;**促銷活動ID** (UUID)進行篩選，而不使用名稱，您可在促銷活動屬性中找到該篩選器。
