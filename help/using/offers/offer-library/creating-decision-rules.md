---
title: 建立決定規則
description: 了解如何在Adobe Experience Platform中建立決策規則。
feature: 優惠
topic: 整合
role: User
level: Intermediate
source-git-commit: dc3a5aacbd4b9bb20c384e0b057241f3080f09fa
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 13%

---

# 建立決定規則 {#creating-decision-rules}

您可以根據Adobe Experience Platform中可用的資料建立優惠方案決策規則。 決策規則決定可向誰顯示優惠方案。

例如，您可以指定只在 (性別 =「女性」) 和 (地區 =「東北部」) 時顯示「女性冬季服裝優惠方案」。

➡️ [在影片中探索此功能](#video)

可在&#x200B;**[!UICONTROL Components]**&#x200B;功能表中存取已建立的決策規則清單。

![](../../assets/decision_rules_list.png)

若要建立決策規則，請遵循下列步驟：

1. 前往&#x200B;**[!UICONTROL Rules]**&#x200B;標籤，然後按一下&#x200B;**[!UICONTROL Create rule]**。

   ![](../../assets/offers_decision_rule_creation.png)

1. 為規則命名並提供說明，然後根據您的需求設定規則。

   若要這麼做，**區段產生器**&#x200B;可協助您建立規則的條件。 [了解更多](../../segment/about-segments.md)

   在此範例中，規則會鎖定具有「金級」忠誠度的客戶。

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >與&#x200B;**[!UICONTROL Audience Destinations]**&#x200B;服務使用的區段產生器相比，用於建立決策規則的區段產生器會呈現一些特性。 例如， **[!UICONTROL Segments]**&#x200B;標籤無法使用。 不過，區段產生器檔案中所述的全域程式對於建立選件決策規則仍然有效。

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;以確認。

1. 建立規則後，規則清單中就會顯示。 您可以選取它以顯示其屬性，並加以編輯或刪除。

   ![](../../assets/rule_created.png)

>[!CAUTION]
>
>[!DNL Journey Optimizer]中目前不支援以事件為基礎的選件。 如果您根據[event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}建立決策規則，將無法在選件中運用該規則。

## 教學課程影片 {#video}

>[!NOTE]
>
>此影片適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 不過，它提供在Journey Optimizer內容中使用Offer的一般指引。

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
