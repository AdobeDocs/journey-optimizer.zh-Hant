---
title: 建立決定規則
description: 了解如何在Adobe Experience Platform中建立決策規則。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 12%

---

# 建立決定規則 {#creating-decision-rules}

您可以根據Adobe Experience Platform中可用的資料建立優惠方案決策規則。 決策規則決定可向誰顯示優惠方案。

例如，您可以指定只在 (性別 =「女性」) 和 (地區 =「東北部」) 時顯示「女性冬季服裝優惠方案」。

➡️ [在影片中探索此功能](#video)

建立的決策規則清單可在 **[!UICONTROL Components]** 功能表。

![](../../assets/decision_rules_list.png)

若要建立決策規則，請遵循下列步驟：

1. 前往 **[!UICONTROL Rules]** ，然後按一下 **[!UICONTROL Create rule]**.

   ![](../../assets/offers_decision_rule_creation.png)

1. 為規則命名並提供說明，然後根據您的需求設定規則。

   若要這麼做， **區段產生器** 可協助您建立規則的條件。 [了解更多](../../segment/about-segments.md)

   在此範例中，規則會鎖定具有「金級」忠誠度的客戶。

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >與搭配使用的區段產生器相比，用於建立決策規則的區段產生器會呈現一些特性 **[!UICONTROL Audience Destinations]** 服務。 例如， **[!UICONTROL Segments]** 標籤無法使用。 不過，區段產生器檔案中所述的全域程式對於建立選件決策規則仍然有效。

1. 按一下 **[!UICONTROL Save]** 確認。

1. 建立規則後，規則清單中就會顯示。 您可以選取它以顯示其屬性，並加以編輯或刪除。

   ![](../../assets/rule_created.png)

>[!CAUTION]
>
>目前不支援以事件為基礎的選件 [!DNL Journey Optimizer]. 如果您根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}，您將無法在選件中運用它。

## 教學課程影片 {#video}

>[!NOTE]
>
>此影片適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 不過，它提供在Journey Optimizer內容中使用Offer的一般指引。

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
