---
title: 更新適用性規則
description: 適用性規則可讓您根據要定位的內容（例如設定檔屬性和對象）定義合格的候選人。
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 8d82b4db-2ba8-4692-a63e-9cb3c6c434c3
version: Journey Orchestration
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 8%

---

# 更新適用性規則 {#update-eligibility-rule}

您可以透過向優惠資料庫API發出PUT要求來修改或更新規則。

如需JSON PUT的詳細資訊，包括可用的作業，請參閱官方[JSON PUT檔案](https://jsonpatch.com/)。

**Accept和Content-Type標頭**

下表顯示請求標頭中包含Content-Type欄位的有效值：

| 標題名稱 | 值 |
| --------- | ----------- |
| Content-Type | `application/json` |

**API格式**

```http
PUT /{ENDPOINT_PATH}/offer-rules/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要更新之實體的ID。 | `rule1234` |

**要求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "[UPDATED] Test Offer Rule DPS",
    "description": "Offer Rule description",
    "exdRule": true,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "homeAddress.stateProvince.equals(\"CA\", false) and (select var1 from xEvent where var1.eventType.equals(\"purchase\", true) and (var1.commerce.order.priceTotal = 1000.0 and var1.commerce.order.currencyCode.equals(\"USD\", false)))"
    },
    "definedOn": {
        "": {
            "schema": {
                "altId": "_xdm.context.profile",
                "version": "1"
            },
            "referencePaths": [
                "homeAddress.stateProvince"
            ]
        },
        "xEvent": {
            "schema": {
                "altId": "_xdm.context.experienceevent",
                "version": "1"
            },
            "referencePaths": [
                "eventType",
                "commerce.order.priceTotal",
                "commerce.order.currencyCode"
            ]
        }
    }
}'
```

| 參數 | 說明 |
| --------- | ----------- |
| `value` | 您想要用來更新引數的新值。 |
| `path` | 要更新之引數的路徑。 |
| `op` | 用於定義更新連線所需動作的操作呼叫。 作業包括： `add`、`replace`、`remove`、`copy`和`test`。 |

**回應**

成功的回應會傳回適用性規則的更新詳細資料，包括ID。

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
