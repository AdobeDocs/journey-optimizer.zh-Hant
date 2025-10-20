---
title: 建立適用性規則
description: 適用性規則可讓您根據要定位的內容（例如設定檔屬性和對象）定義合格的候選人。
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 39c6e82e-c1b1-4dda-a941-3db6324cef37
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 5%

---

# 建立適用性規則 {#create-eligibility-rule}

您可以向優惠資料庫API提出POST要求，以建立適用性規則。

**API格式**

```http
POST /{ENDPOINT_PATH}/eligibility-rules 
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |

**要求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '
{
    "name": "test dule",
    "description": "xxxxxx",
    "exdRule": true,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "inSegment(\"849807b6-0a76-4895-96d9-89996477f23b\") and billingAddress.city.equals(\"san jose\", false)"
    }
}'
```

**回應**

成功的回應會傳回新建立的適用性規則的詳細資料，包括ID。 您可在後續步驟中使用ID來更新或刪除適用性規則。

```json
{
    "etag": 1,
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
