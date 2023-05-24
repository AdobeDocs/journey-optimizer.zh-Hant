---
solution: Journey Optimizer
product: journey optimizer
title: 關於 Adobe Experience Platform 區段
description: 瞭解如何配置Adobe Experience Platform段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 6c255d66fb89ba756add062d8a4315dd622fd8e7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 8%

---

# 開始使用Adobe Experience Platform段 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="區段"
>abstract="透過使用即時客戶設定檔資料，Adobe Experience Platform 使您能夠輕鬆建立鎖定區段，以擷取客戶的獨特行為和偏好。"

[!DNL Journey Optimizer]  允許您直接使用即時客戶配置檔案資料建立Adobe Experience Platform段 **[!UICONTROL 段]** 菜單，並將其用於您的行程或活動。

此外，還可以從分段服務本身建立段。 在 [Adobe Experience Platform分段處檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)。

## 在 [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

您可以在 **[!DNL Journey Optimizer]** 以不同方式：

* 選擇段作為 **競選的觀眾**，其中消息將發送到屬於選定段的所有個人。 [瞭解如何定義市場活動的受眾](../campaigns/create-campaign.md#define-the-audience-audience)。

* 使用 **讀取段** 行程中的業務流程活動，使段中的所有人員進入行程並接收行程中包含的消息。

   假設您有「銀色客戶」部分。 通過本練習，您可以讓所有銀發客戶輸入行程併發送一系列個性化消息。 [瞭解如何配置讀取段活動](../building-journeys/read-segment.md#configuring-segment-trigger-activity)。

* 使用 **分部資格** 旅程中的活動，根據Adobe Experience Platform段出入口讓個人進入或前進。

   例如，您可以讓所有新銀客戶輸入行程併發送消息。 有關如何使用此活動的詳細資訊，請參閱 [瞭解如何配置段資格活動](../building-journeys/segment-qualification-events.md)。

* 使用 **條件** 在基於段成員身份構建條件的旅程中進行活動。 [瞭解如何在條件中使用段](../building-journeys/condition-activity.md#using-a-segment)。

## 受眾評價方法{#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer，使用以下兩種評價方法之一從段定義生成受眾：

* **流分段**:當新資料流入系統時，該段的受眾清單會即時保持最新。

   串流分段是一種持續的資料選取流程，會根據使用者活動更新您的區段。一旦生成並保存了段，就會針對傳入的資料應用段定義。 這意味著當個人的個人資料資料發生更改時，將從網段中添加或刪除個人，以確保您的目標受眾始終具有相關性。

* **批分段**:每24小時評估一次該節目的受眾清單。

   批處理分段是流式分段的替代方法，它通過段定義一次處理所有配置檔案資料。 這將建立可保存和導出以供使用的受眾的快照。 但是，與流式分割不同，批量分割不會持續即時更新受眾清單，而在批處理之後傳入的新資料在下一個批處理之前不會反映在資料段中。」

系統根據分段規則的複雜度和評估成本，對每個分段定義確定分批分段和流分段。 可查看中每個段的評估方法 **[!UICONTROL 評價方法]** 的子菜單。

![](assets/evaluation-method.png)

>[!NOTE]
>
>如果 **[!UICONTROL 評價方法]** 列不顯示，您需要使用清單右上角的配置按鈕添加它。

在您首次定義段後，配置檔案在符合條件時添加到受眾。

從先前資料中回填觀眾最多需要24小時。 在觀眾回填後，觀眾會不斷更新，隨時準備瞄準。
