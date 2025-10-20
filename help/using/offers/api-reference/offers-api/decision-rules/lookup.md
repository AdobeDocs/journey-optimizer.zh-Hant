---
title: 查詢決定規則
description: 決定規則是新增至個人化優惠的限制，並套用至設定檔以判斷適用性。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 54368710-1021-43c0-87b7-5176cc6c72f7
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 5%

---

# 查詢決定規則 {#lookup-decision-rule}

您可以透過向[!DNL Offer Library] API發出GET請求來查詢特定的決定規則，該API在請求路徑中包含決定規則`id`。

**API格式**

```http
GET /{ENDPOINT_PATH}/offer-rules/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要查閱之實體的ID。 | `offerRule1234` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回您查詢的特定決定規則的詳細資料，包括其唯一決定規則`id`的相關資訊。

```json
  {
    "created": "2022-09-16T18:59:53.651+00:00",
    "modified": "2022-09-16T18:59:53.651+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerRule1234",
    "name": "Californians with one or more purchases greater than $1000",
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
            }
}
```
