---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 更新集合限定詞
description: 集合限定詞可讓您更妥善地組織和排序優惠方案。
feature: Decision Management, API
badge: label="舊版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 918927e1-ad7a-4937-b652-2a0932e9efa1
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/f4vAvwVtpltjJU6D05cPYJJ3NSi64VN--SUiXdKoyXA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 140
ht-degree: 22%

---

# 更新集合限定詞 {#update-collection-qualifier}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../../../../experience-decisioning/gs-experience-decisioning.md)


您可以透過向選件程式庫API發出PATCH請求，修改或更新集合限定詞（先前稱為「標籤」）。

如需JSON修補程式的詳細資訊，包括可用的作業，請參閱官方[JSON修補程式檔案](https://jsonpatch.com/)。

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示請求標頭中包含&#x200B;*Content-Type*&#x200B;欄位的有效值：

| 標題名稱 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/tags/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要更新之實體的ID。 | `tag1234` |

**要求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated tag"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated tag description"
    }
]'
```

**回應**

成功的回應會傳回集合限定詞的更新詳細資料，包括其唯一的`id`。

```json
{
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 2,
    "createdDate": "2023-09-07T12:36:26.602Z",
    "lastModifiedDate": "2023-09-07T12:36:26.602Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
