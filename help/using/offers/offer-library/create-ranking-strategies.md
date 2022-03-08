---
product: experience platform
solution: Experience Platform
title: 建立排名策略
description: 瞭解如何建立AI模型以對產品排序
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 5%

---

# 建立AI模型 {#ai-rankings}

## 建立排名策略 {#create-ranking-strategy}

要建立排名策略，請執行以下步驟：

1. 訪問 **[!UICONTROL Components]** ，然後選擇 **[!UICONTROL AI rankings]** 頁籤。

   ![](../assets/ai-ranking-list.png)

   列出了目前建立的所有排名策略。

1. 按一下「**[!UICONTROL Create strategy]**」按鈕。

1. 填寫以下欄位：

   ![](../assets/ai-ranking-fields.png)

   * **[!UICONTROL Name]**:必須提供的唯一名稱。

   * **[!UICONTROL Model type]**:當前 [!DNL Journey Optimizer] 唯一支援的模型類型是 **[!UICONTROL Auto-optimization]**。 [了解更多](ai-ranking.md#auto-optimization)

   * **[!UICONTROL Optimization metric]**：

      此選項使營銷人員能夠選擇如何構建和培訓機器學習模型：根據顯示的優惠、電子郵件中按一下的優惠和/或網上按一下的優惠。

      >[!NOTE]
      >
      >如果需要，可以選擇所有度量類型。

      有兩種優化度量：
      * **[!UICONTROL Impression]**:當前印象事件對應於顯示的所有優惠。
      * **[!UICONTROL Conversion]**:轉換事件與所有導致通過電子郵件或Web按一下的服務相對應。

      所有選定的印象事件和/或轉換事件將使用已提供的Web SDK或移動SDK自動捕獲。 在中瞭解有關此的詳細資訊 [Adobe Experience PlatformWeb SDK概述](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant)。

   * **[!UICONTROL Dataset ID]**:要進行轉換，您需要提供一個資料集，通過從下拉清單中選擇該資料集來收集事件。 瞭解如何在 [此部分](#create-dataset)。 <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >僅從與 **[!UICONTROL Experience Event - Proposition Interactions]** 欄位組（以前稱為mixin）顯示在下拉清單中。

1. 保存並激活排名策略。

   ![](../assets/ai-ranking-save-activate.png)

現在，它已準備好用於對合格的職位安排進行排名的決定。 瞭解詳情 [此部分](../offer-activities/configure-offer-selection.md#use-ranking-strategy)。<!--TBC?-->

## 建立資料集以收集事件 {#create-dataset}

您需要建立一個資料集，在該資料集中將收集轉換事件。 首先建立將在資料集中使用的架構：

1. 從 **[!UICONTROL Data Management]** 菜單，選擇 **[!UICONTROL Schema]**，轉到 **[!UICONTROL Browse]** 頁籤 **[!UICONTROL Create schema]**。

   ![](../assets/ai-ranking-create-schema.png)

1. 選擇 **[!UICONTROL XDM ExperienceEvent]**。

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    瞭解有關中的XDM架構和欄位組的詳細資訊 [XDM系統概述文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)。


1. 在 **[!UICONTROL Search]** 欄位，鍵入「命題交互」並選擇 **[!UICONTROL Experience Event - Proposition Interactions]** 欄位組。

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    將在資料集中使用的架構必須具有 **[!UICONTROL Experience Event - Proposition Interactions]** 與其關聯的欄位組。 否則，您將無法在排名策略中使用它。

1. 按一下「**[!UICONTROL Add field groups]**」。

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >欄位組以前稱為mixin。

1. 鍵入名稱並保存架構。<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    瞭解有關在中構建架構的詳細資訊 [架構組合的基礎](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas)。

您現在已準備好使用此架構建立資料集。 請依照下列步驟執行此操作：

1. 從 **[!UICONTROL Data Management]** 菜單，選擇 **[!UICONTROL Datasets]**，轉到 **[!UICONTROL Browse]** 頁籤 **[!UICONTROL Create dataset]**。

   ![](../assets/ai-ranking-create-dataset.png)

1. 選擇「**[!UICONTROL Create dataset from schema]**」。

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 從清單中選擇剛建立的架構。

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. 按一下「**[!UICONTROL Next]**」。

1. 為中的資料集提供唯一名稱 **[!UICONTROL Name]** 按一下 **[!UICONTROL Finish]**。

   ![](../assets/ai-ranking-dataset-name.png)

該資料集現在已準備好在 [建立排名策略](#create-ranking-strategy)。

## 提供架構要求 {#schema-requirements}

此時，您必須：

* 制定了排名策略，
* 定義要捕獲的事件類型 — 顯示（印象）和/或按一下（轉換）聘用，
* 以及要在哪個資料集中收集事件資料。

現在，每次顯示和/或按一下優惠時，您都希望相應的事件由 **[!UICONTROL Experience Event - Proposition Interactions]** 欄位組 [Adobe Experience PlatformWeb SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target=&quot;_blank&quot;}或移動SDK。

要能夠在事件類型（顯示的要約或已按一下的要約）中發送，必須為發送到Adobe Experience Platform的體驗事件中的每個事件類型設定正確的值。 以下是在JavaScript代碼中實現的架構要求：

### 提供顯示的方案

**事件類型：** `decisioning.propositionDisplay`
**來源：** Web.sdk/Alloy.js(`sendEvent command -> xdm : {eventType, interactionMixin}`)或批量攝取
+++**示例負載：**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for “nextBestOffer”
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for “nextBestOffer”
        }
    ]
}
```

+++

### 已按一下優惠方案

**事件類型：** `decisioning.propositionInteract`
**來源：** Web.sdk/Alloy.js(`sendEvent command -> xdm : {eventType, interactionMixin}`)或批量攝取
+++**示例負載：**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->

