---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 設定事件擷取
description: 瞭解如何設定您的優惠方案綱要以擷取事件
badge: label="舊版" type="Informative"
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DhaXO7sS2zR9iewgoQjrN5ptYNpYSt97e-hflU2iq7c
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: e08599ea-8888-4294-ba74-3ba0a7762a46id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: acc16deb-1d7f-4ec9-9ce3-6cdf355afde6
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 10%

---

# 設定資料彙集 {#schema-requirements}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../../experience-decisioning/gs-experience-decisioning.md)

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
>若要讓您的自訂事件計入[頻率限定](../offer-library/add-constraints.md#capping)，您需要將體驗事件傳送至以下兩個Adobe Experience Platform資料收集端點之一，以將其連線至Edge端點：
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>如果您使用[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"}或[Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}，連線會自動建立。
