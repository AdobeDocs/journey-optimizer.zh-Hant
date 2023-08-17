---
title: 建立決定規則
description: 瞭解如何建立決定規則，以定義可顯示優惠的對象
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 15%

---

# 建立決定規則 {#create-decision-rules}

您可以根據Adobe Experience Platform中的可用資料來建立優惠決定規則。 決定規則會決定要向誰顯示優惠方案。

例如，您可以指定只在 (性別 =「女性」) 和 (地區 =「東北部」) 時顯示「女性冬季服裝優惠方案」。

➡️ [在影片中探索此功能](#video)

建立的決定規則清單可在以下位置存取： **[!UICONTROL 元件]** 功能表。

![](../assets/decision_rules_list.png)

若要建立決定規則，請遵循下列步驟：

1. 前往 **[!UICONTROL 規則]** 標籤，然後按一下 **[!UICONTROL 建立規則]**.

   ![](../assets/offers_decision_rule_creation.png)

1. 為規則命名並提供說明，然後視需要設定規則。

   為此，請使用Adobe Experience Platform **區段產生器** 可協助您建立規則的條件。 [瞭解如何建立區段定義](../../audience/creating-a-segment-definition.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >用來建立決定規則的區段產生器有些許特性，但與搭配使用時有所不同 **[!UICONTROL 細分]** 服務。 不過，以下說明的全域程式： [區段產生器](../../audience/creating-a-segment-definition.md) 檔案仍然有效，無法建立優惠決定規則。 在 [Adobe Experience Platform 細分服務文件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html)中了解更多。

1. 當您在工作區中新增及設定新欄位時， **[!UICONTROL 對象屬性]** 窗格會顯示受眾之預估設定檔的相關資訊。 按一下 **[!UICONTROL 重新整理預估值]** 以更新資料。

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >當規則引數包含不在設定檔中的資料（例如內容資料）時，設定檔預估無法使用。 例如，適用性規則要求目前天氣為≥80度。

1. 按一下 **[!UICONTROL 儲存]** 以確認。

1. 規則建立後，會顯示在 **[!UICONTROL 規則]** 清單。 您可以選取它以顯示其屬性，並加以編輯或刪除。

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>目前不支援事件型優惠方案 [!DNL Journey Optimizer]. 如果您根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"}，您將無法在選件中運用它。

## 教學課程影片 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
