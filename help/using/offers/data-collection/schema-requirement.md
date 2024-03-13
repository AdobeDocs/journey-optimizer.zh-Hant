---
product: experience platform
solution: Experience Platform
title: 設定事件擷取
description: 瞭解如何設定您的優惠方案綱要以擷取事件
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 2%

---

# 設定資料彙集 {#schema-requirements}

為了能夠取得對決策事件以外的事件型別的意見反應，您必須為中的每種事件型別設定正確的值 **體驗事件** 會傳送至Adobe Experience Platform的內容。

>[!CAUTION]
>
>對於每種事件型別，請確定資料集中使用的結構描述具有 **[!UICONTROL 體驗事件 — 主張互動]** 與其相關聯的欄位群組。 [了解更多](create-dataset.md)

以下是實作JavaScript程式碼所需的結構描述需求。

>[!NOTE]
>
>不需要傳送決定事件，因為決定管理會自動產生這些事件，並將它們放入 **[!UICONTROL ODE DecisionEvents]** 資料集<!--to check--> 是自動產生的。

## 追蹤曝光 {#track-impressions}

請確定事件型別和來源如下：

**體驗事件型別：** `decisioning.propositionDisplay`
**來源：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次擷取
+++**裝載範例：**

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
**來源：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次擷取
+++**裝載範例：**

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

對於自訂事件，資料集中使用的結構描述也必須具有 **[!UICONTROL 體驗事件 — 主張互動]** 欄位群組相關聯，但對必須用來標籤這些事件的體驗事件型別沒有特定要求。

>[!NOTE]
>
>讓您的自訂事件在中處理 [頻率限定](../offer-library/add-constraints.md#capping)，您需要將體驗事件傳送至下列兩個Edge資料收集端點之一，以將其連線至Adobe Experience Platform端點：
>
>* POST/ee/v2/interact
>* POST/ee/v2/collect
>
>如果您使用 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}，則會自動建立連線。
