---
title: 建立集合限定詞
description: 集合限定詞可讓您更妥善地組織和排序優惠方案。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 13%

---


# 建立集合限定詞 {#create-tag}

您可以透過向優惠資料庫API發出POST要求，以建立集合限定詞（先前稱為「標籤」）。

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示請求標頭中包含&#x200B;*Content-Type*&#x200B;欄位的有效值：

| 標題名稱 | 價值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
POST /{ENDPOINT_PATH}/tags
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |

**要求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/tags' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{        
    "name": "Black Friday",
    "description": "Tag for black friday"
}'
```

**回應**

成功的回應傳回關於新建立的集合限定詞的資訊，包括其唯一的`id`。 您可以在稍後的步驟中使用`id`來更新或刪除您的集合限定詞。 在稍後的教學課程中，您可以使用唯一的集合限定詞`id`來建立集合和個人化優惠。

```json
{
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 1,
    "createdDate": "2023-09-07T12:36:26.602Z",
    "lastModifiedDate": "2023-09-07T12:36:26.602Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
