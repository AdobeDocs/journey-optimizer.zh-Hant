---
product: experience platform
solution: Experience Platform
title: 設定事件擷取
description: 了解如何設定優惠方案結構以擷取事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# 設定資料收集 {#schema-requirements}

<!--To send in feedback data, you must define how the experience events will be captured.-->

若要獲得決策事件以外的事件類型的意見，您必須為 **體驗事件** 被送到Adobe Experience Platform。

對於每個事件類型，請確定資料集中使用的結構具有 **[!UICONTROL 體驗事件 — 主張互動]** 與其相關聯的欄位群組。 [了解更多](create-dataset.md)

以下是您在JavaScript程式碼中實作所需的結構需求。

>[!NOTE]
>
>決策事件不需要傳入，因為決策管理會自動產生這些事件，並將其放入 **[!UICONTROL ODE DecisionEvents]** 資料集<!--to check--> 自動產生。

## 追蹤曝光數

請確定事件類型和來源如下：

**體驗事件類型：** `decisioning.propositionDisplay`
**來源：** Web.sdk/Alloy.js(`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次內嵌
+++**裝載範例：**

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
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for "nextBestOffer"
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for "nextBestOffer"
        }
    ]
}
```

+++

## 追蹤點按次數

請確定事件類型和來源如下：

**體驗事件類型：** `decisioning.propositionInteract`
**來源：** Web.sdk/Alloy.js(`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次內嵌
+++**裝載範例：**

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

## 追蹤自訂事件

若為自訂事件，資料集中使用的結構也必須具備 **[!UICONTROL 體驗事件 — 主張互動]** 欄位群組，但體驗事件類型上沒有必要用來標籤這些事件的特定需求。

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
