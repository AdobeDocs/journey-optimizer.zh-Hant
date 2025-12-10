---
solution: Journey Optimizer
product: Journey Optimizer
title: 設定事件擷取
description: 瞭解如何設定您的優惠方案綱要以擷取事件
feature: Ranking, Datasets, Decisioning
role: Developer
level: Experienced
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---

# 設定資料彙集 {#schema-requirements}

若要取得非決定事件的事件型別意見反應，您必須在傳送至Adobe Experience Platform的&#x200B;**體驗事件**&#x200B;中，為每個事件型別設定正確的值。

>[!CAUTION]
>
>對於每個事件型別，請確定資料集中使用的結構描述具有與其關聯的&#x200B;**[!UICONTROL 體驗事件 — 主張互動]**&#x200B;欄位群組。<!--[Learn more](create-dataset.md)-->

以下是實作JavaScript程式碼所需的結構描述需求。

## 追蹤曝光 {#track-impressions}

請確定下列欄位已正確設定：

**體驗事件型別：** `decisioning.propositionDisplay`

**propositionEventType：** `_experience.decisioning.propositionEventType.display`

**Source：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次擷取

+++**範例承載：**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "display": 1
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionDisplay",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b219",
  "timestamp": "2025-10-07T20:22:00Z"
}
```

+++

## 追蹤點按 {#track-clicks}

請確定下列欄位已正確設定：

**體驗事件型別：** `decisioning.propositionInteract`

**propositionEventType：** `_experience.decisioning.propositionEventType.interact`

**Source：** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`)或批次擷取

主張中的每個優惠方案都包含一個追蹤權杖，這是Adobe產生的唯一識別碼。 此Token必須完全依照收到的方式在對應點選或曝光事件中傳遞（不會變更）。 比對追蹤權杖可確保Adobe能夠準確地將使用者動作與正確的優惠決定建立關聯，以啟用下游報告和人工智慧為基礎的最佳化。

>[!CAUTION]
>
>如果您在追蹤點選時未在`propositionAction.tokens`欄位中傳遞追蹤權杖，則點選事件將不會正確歸因於對應的選件。 這將導致不完整的追蹤資料，並將對報表和AI型排名最佳化產生負面影響。 請一律確保將主張中的追蹤Token納入您的點選追蹤實作中。

+++**範例承載：**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "interact": 1
      },
      "propositionAction": {
        "tokens": [
          "Vx9fwWXmp6/kyYRVOUZWEQ"
        ]
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionInteract",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b765",
  "timestamp": "2025-10-07T20:50:00Z"
}
```

+++

## 追蹤自訂事件 {#track-custom-events}

對於自訂事件，在資料集中使用的結構描述也必須有與之關聯的&#x200B;**[!UICONTROL 體驗事件 — 主張互動]**&#x200B;欄位群組，但對於必須用來標籤這些事件的體驗事件型別沒有特定要求。

<!--

>[!NOTE]
>
>To have your custom events accounted for in [capping](../items.md#capping), you need to connect the experience event to Adobe Experience Platform endpoints by sending it to either one of these two Edge data collection endpoints:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>If you are using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hant){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=zh-Hant){target="_blank"}, the connection is made automatically.-->
