---
product: experience platform
solution: Experience Platform
title: 內容資料與決策請求
description: 瞭解如何在決策請求中傳遞內容資料。
badge: label="舊版" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 45d060ce-0a12-4a6e-a594-ec10cdff8f38
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# 內容資料與決策請求 {#context-data-decisioning}

本節將引導您在決策請求中傳遞內容資料，並在資格規則中使用這些資料。

>[!BEGINSHADEBOX]

若要更進一步，您也可以將內容運用到&#x200B;**排名公式**&#x200B;中，以提升您的優惠。 在[此區段](../offers/ranking/create-ranking-formulas.md#context-data)中有利用內容資料的排名公式的詳細範例。

>[!ENDSHADEBOX]

## 在決策請求中傳遞內容資料

決策請求中的內容資料是使用索引鍵定義的： `xdm:ContextData`。

內容資料屬性並非由XDM結構描述驅動。 您可以在JSON中傳遞任何內容資料，作為決策請求裝載的一部分。

以下是包含內容資料的範例決策請求（請參閱`xdm:ContextData`）：

```
curl --location 'https://platform-stage.adobe.io/data/core/ods/decisions' \
--header 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
--header 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
--header 'Authorization: Bearer eyJhbGciOi....' \
--header 'x-api-key: {{api_key}}' \
--header 'x-gw-ims-org-id: {{ims_org}}' \
--header 'x-sandbox-name: {{sandbox_name}}' \
--header 'x-request-id: {{$guid}}' \
--data-raw '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:19978bf95ebfc8fb",
            "xdm:placementId": "dps:offer-placement:199772e1c90d50ac"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "test@test.com",
                        "primary": true
                    }
                ]
            },
            "xdm:contextData": [
                {
                    "@type": "_xdm.context.additionalParameters;version=1",
                    "xdm:data": {
                        "xdm:channel": "mobile",
                        "xdm:language": "en",
                        "xdm:isThirdParty": true,
                        "xdm:mobileVersion": "3.0.5106",
                        "xdm:mobileVersionMajor": "3",
                        "xdm:mobileVersionMinor": "0",
                        "xdm:mobileVersionPatch": "125",
                        "xdm:deviceType": "iOS",
                        "xdm:features": [
                            "p1000",
                            "p1001"
                        ]
                    }
                }
            ]
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}'
```

## 在適用性規則中使用內容資料

以下範例說明如何使用適用性規則中決策請求中傳遞的內容資料。

* 符合條件如果內容資料功能包含特定值：

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where contextData.features AND (select personetic from contextData.features where personetic.contains("123"))
  ```

* 如果通道非空白且等於行動裝置，則符合條件：

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where !contextData.channel.isNull() AND contextData.channel!="" AND contextData.channel="mobile"
  ```
