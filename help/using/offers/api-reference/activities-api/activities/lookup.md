---
title: 查詢決定
description: 決定包含通知優惠選擇的邏輯。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: ee242f0f-f331-4f41-9418-938b4ca1dda3
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 6%

---

# 查詢決定 {#look-up-decision}

您可以透過向[!DNL Offer Library] API發出GET請求來查詢特定決策，該API包含在請求路徑中的決策`id`。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要查閱之實體的ID。 | `offerDecision1234` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回決定的詳細資料，包括有關您唯一決定`id`的資訊。

```json
{
    "created": "2022-11-15T16:35:06.873+00:00",
    "modified": "2023-05-15T15:00:27.641+00:00",
    "etag": 3,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerDecision1234",
    "name": "Test Decision One",
    "status": "draft",
    "startDate": "2021-08-23T07:00:00.000+00:00",
    "endDate": "2021-08-25T07:00:00.000+00:00",
    "fallback": "fallbackOffer1234",
    "criteria": [
        {
            "placements": [
                "offerPlacement1234",
                "offerPlacement5678"
            ],
            "rank": {
                "priority": 0,
                "order": {
                    "orderEvaluationType": "ranking-strategy",
                    "rankingStrategy": "123456789123"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "none"
            },
            "optionSelection": {
                "filter": "offerCollection1234"
            }
        }
    ]
}
```
