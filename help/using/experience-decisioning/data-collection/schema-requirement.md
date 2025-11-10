---
product: experience platform
solution: Experience Platform
title: 設定事件擷取
description: 瞭解如何設定您的優惠方案綱要以擷取事件
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
hide: true
hidefromtoc: true
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---

# 設定資料彙集 {#schema-requirements}

若要取得非決定事件的事件型別意見反應，您必須在傳送至Adobe Experience Platform的&#x200B;**體驗事件**&#x200B;中，為每個事件型別設定正確的值。

>[!CAUTION]
>
>對於每個事件型別，請確定資料集中使用的結構描述具有與其關聯的&#x200B;**[!UICONTROL 體驗事件 — 主張互動]**&#x200B;欄位群組。 [了解更多](create-dataset.md)

以下是實作JavaScript程式碼所需的結構描述需求。

>[!NOTE]
>
>決定事件不需要傳送，因為決定管理會自動產生這些事件，並將其放入自動產生的&#x200B;**[!UICONTROL ODE DecisionEvents]**&#x200B;資料集<!--to check-->中。

## 追蹤曝光 {#track-impressions}

請確定事件型別和來源如下：

**體驗事件型別：** `decisioning.propositionDisplay`
**Source：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次擷取
+++**範例承載：**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

## 追蹤點按 {#track-clicks}

請確定事件型別和來源如下：

**體驗事件型別：** `decisioning.propositionInteract`
**Source：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次擷取
+++**範例承載：**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

## 追蹤自訂事件 {#track-custom-events}

對於自訂事件，在資料集中使用的結構描述也必須有與之關聯的&#x200B;**[!UICONTROL 體驗事件 — 主張互動]**&#x200B;欄位群組，但對於必須用來標籤這些事件的體驗事件型別沒有特定要求。

>[!NOTE]
>
>若要在[上限](../items.md#capping)中說明您的自訂事件，您必須將體驗事件傳送至以下兩個Adobe Experience Platform資料收集端點之一，以將其連線至Edge端點：
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>如果您使用[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"}或[Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}，連線會自動建立。
