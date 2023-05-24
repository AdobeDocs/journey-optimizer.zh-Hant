---
title: 建立決定規則
description: 瞭解如何建立決策規則以定義可向誰顯示優惠
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 13%

---

# 建立決定規則 {#create-decision-rules}

您可以根據Adobe Experience Platform的可用資料建立優惠決策規則。 決策規則確定可向誰顯示報價。

例如，您可以指定只在 (性別 =「女性」) 和 (地區 =「東北部」) 時顯示「女性冬季服裝優惠方案」。

➡️ [在影片中探索此功能](#video)

可在 **[!UICONTROL 元件]** 的子菜單。

![](../assets/decision_rules_list.png)

要建立決策規則，請執行以下步驟：

1. 轉到 **[!UICONTROL 規則]** ，然後按一下 **[!UICONTROL 建立規則]**。

   ![](../assets/offers_decision_rule_creation.png)

1. 命名規則並提供說明，然後根據需要配置規則。

   為此， **段生成器** 可用於幫助您構建規則的條件。 [了解更多](../../segment/about-segments.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >為建立決策規則而提供的段生成器與與 **[!UICONTROL 分段]** 服務。 例如， **[!UICONTROL 段]** 頁籤不可用。 但是，在 [段生成器](../../segment/about-segments.md) 文檔仍然有效，可生成聘用決定規則。 在 [Adobe Experience Platform分段處檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html)。

1. 在工作區中添加和配置新欄位時， **[!UICONTROL 段屬性]** 窗格顯示屬於段的估計配置檔案的資訊。 按一下 **[!UICONTROL 刷新估計]** 更新資料。

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >當規則參數包括不在配置檔案中的資料（如上下文資料）時，配置檔案估計不可用。 例如，要求當前天氣為≥80度的資格規則。

1. 按一下 **[!UICONTROL 保存]** 確認。

1. 建立規則後，將在 **[!UICONTROL 規則]** 清單框。 可以選擇它以顯示其屬性，並編輯或刪除它。

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>當前不支援基於事件的服務 [!DNL Journey Optimizer]。 如果根據 [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}你將無法在報價中利用它。

## 教程視頻 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
