---
title: 建立排名公式
description: 排名公式可讓您定義用於排名專案的評分函式。
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 2eb3ca65-f9f2-4483-ac6a-7bd896b0e516
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 14%

---

# 建立排名公式 {#create-ranking-formula}

您可以透過向優惠資料庫API發出POST要求來建立排名公式。

**Accept和Content-Type標頭**

下表顯示請求標頭中包含Content-Type欄位的有效值：

| 標題名稱 | 價值 |
| --------- | ----------- | 
| Content-Type | application/json |

**API格式**

```http
POST /{ENDPOINT_PATH}/ranking-formulas 
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |

**要求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/ranking-formulas' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Ranking Function DPS",
    "description": "Ranking  function description",
    "exdFunction": true,
    "returnType": {
        "type": "integer"
    },
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "if(offer.rank.priority.isNotNull(), offer.rank.priority, 0) * if(offer.tags.intersects(boosted.tags), 2, 1)"
    },
    "definedOn": {
        "offer": {
            "schema": {
                "altId": "_experience.offer-management.personalized-offer",
                "version": "0"
            }
        },
        "boosted": {
            "schema": {
                "altId": "_xdm.context.foo",
                "version": "0"
            }
        }
    }
}'
```

**回應**

成功的回應會傳回新建立的排名公式的詳細資料，包括`id`。 您可在後續步驟中使用`id`來更新或刪除您的排名公式。

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
