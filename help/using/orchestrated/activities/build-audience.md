---
solution: Journey Optimizer
product: journey optimizer
title: 使用建立對象活動
description: 瞭解如何在協調的行銷活動中使用建立對象活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 62f16b6f582e6bf5620b75df4a75d4c15441ca4a
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 24%

---

# 建置客群 {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="建置客群活動"
>abstract="**建置客群**&#x200B;活動讓您可以定義會進入協調的行銷活動的客群。在協調的行銷活動內容中傳送訊息時，訊息對象未定義於頻道活動中，而是定義於&#x200B;**建立對象**&#x200B;活動中。"


>[!CONTEXTUALHELP]
>id="acw_orchestration_read_audience"
>title="建置客群活動"
>abstract="**讀取對象**&#x200B;活動可讓您選取將進入協調行銷活動的現有對象。 在協調的行銷活動內容中傳送訊息時，訊息對象未定義於頻道活動中，而是定義於&#x200B;**讀取對象**&#x200B;或&#x200B;**建置對象**&#x200B;活動中。"


+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[建立協調行銷活動的重要步驟](../gs-campaign-creation.md) | [建立協調的行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[使用協調的行銷活動傳送訊息](../send-messages.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用查詢Modeler](../orchestrated-rule-builder.md)<br/><br/>[建置您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建置對象](build-audience.md) - [變更維度](change-dimension.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

身為行銷人員，您可以透過直覺式介面建立複雜的受眾區段，讓您根據廣泛的條件和行為來鎖定使用者，以更有效地量身打造您的行銷活動。

若要這麼做，請使用&#x200B;**[!UICONTROL 建立對象]**&#x200B;目標定位活動。 此活動會定義進入協調行銷活動的對象。 當傳送訊息做為協調行銷活動的一部分時，會在&#x200B;**[!UICONTROL 建立對象]**&#x200B;活動中定義對象，而不是在協調的行銷活動中。

## 設定建置對象活動 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="客群"
>abstract="選取您的對象，與您設計新傳遞時使用對象的方式相同。"

請按照以下步驟設定「**[!UICONTROL 建置客群]**」活動：

1. 新增「**[!UICONTROL 建置客群]**」活動。

   ![](../assets/build-audience.png)

1. 定義&#x200B;**[!UICONTROL 標籤]**。

1. 請依照下列標籤中詳述的步驟設定您的對象。

1. 選擇「**[!UICONTROL 目標定位維度]**」。目標市場選擇維度可讓您定義作業的目標群體：收件者、合約受益人、操作者、訂閱者等。預設情況下，會從收件者中選取目標。

1. 按一下&#x200B;**[!UICONTROL 繼續]**。

1. 使用查詢建模器來定義您的查詢。 [在本節中進一步瞭解查詢模型工具](../orchestrated-rule-builder.md)

1. 指定對象為空時是否應產生出站轉變。

## 範例{#build-audience-examples}

以下是包含兩個&#x200B;**[!UICONTROL 建立對象]**&#x200B;活動的協調行銷活動範例。 第一個目標是購物車中包含專案的設定檔，然後是電子郵件傳送。 第二個以願望清單定位設定檔，然後是SMS傳送。

![](../assets/build-audience-2.png)
