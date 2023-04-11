---
title: 建立決定規則
description: 了解如何建立決策規則，以定義可向哪些對象顯示優惠方案
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 55d9befff9b9bf1bc81c6553cd76f015fdd3116e
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 10%

---

# 建立決定規則 {#create-decision-rules}

您可以根據Adobe Experience Platform中可用的資料建立優惠方案決策規則。 決策規則決定可向誰顯示優惠方案。

例如，您可以指定只在 (性別 =「女性」) 和 (地區 =「東北部」) 時顯示「女性冬季服裝優惠方案」。

➡️ [在影片中探索此功能](#video)

建立的決策規則清單可在 **[!UICONTROL 元件]** 功能表。

![](../assets/decision_rules_list.png)

若要建立決策規則，請遵循下列步驟：

1. 前往 **[!UICONTROL 規則]** ，然後按一下 **[!UICONTROL 建立規則]**.

   ![](../assets/offers_decision_rule_creation.png)

1. 為規則命名並提供說明，然後根據您的需求設定規則。

   若要這麼做， **區段產生器** 可協助您建立規則的條件。 [了解更多](../../segment/about-segments.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >與搭配使用的區段產生器相比，用於建立決策規則的區段產生器會呈現一些特性 **[!UICONTROL 對象目標]** 服務。 例如， **[!UICONTROL 區段]** 標籤無法使用。 不過， [區段產生器](../../segment/about-segments.md) 檔案對於建立優惠方案決策規則仍有效。 了解更多 [Adobe Experience Platform區段服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html).

1. 當您新增和設定工作區中的新欄位時， **[!UICONTROL 區段屬性]** 窗格會顯示屬於區段的估計設定檔資訊。 按一下 **[!UICONTROL 重新整理估計值]** 更新資料。

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >當規則參數包含不在設定檔中的資料（例如內容資料）時，設定檔估計將無法使用。 例如，適用性規則要求目前的天氣為≥80度。

1. 按一下 **[!UICONTROL 儲存]** 確認。

1. 規則建立後，就會顯示在 **[!UICONTROL 規則]** 清單。 您可以選取它以顯示其屬性，然後加以編輯或刪除。

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>目前不支援以事件為基礎的選件 [!DNL Journey Optimizer]. 如果您根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}，您將無法在優惠方案中運用它。

## 教學課程影片 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
