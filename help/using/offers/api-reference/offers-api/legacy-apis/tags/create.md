---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 建立集合限定詞
description: 集合限定詞可讓您更妥善地組織和排序優惠方案。
feature: Decision Management, API
badge: label="舊版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 84f0efa5-28af-4569-994c-12d87828a277
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Am1w3Z6gnCGbvq4M3eea-GcPJuAy3EZ2gNKv-0-GcG8
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
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 22%

---

# 建立集合限定詞 {#create-tag}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../../../../../experience-decisioning/gs-experience-decisioning.md)


您可以對[!DNL Offer Library] API發出POST要求，同時提供容器ID，藉此建立集合限定詞（先前稱為「標籤」）。

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示請求標頭中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;欄位的有效值：

| 標題名稱 | 值 |
| ----------- | ----- |
| 接受 | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合限定詞所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**要求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Holiday sales and promotions"
    }'
```

**回應**

成功回應傳回新建立的集合限定詞的相關資訊，包括其唯一的執行個體識別碼和位置`@id`。 您可以在稍後的步驟中使用執行環境ID來更新或刪除您的集合限定詞。 在稍後的教學課程中，您可以使用唯一的集合限定詞`@id`來建立集合和個人化優惠。

```json
{
  "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2023-10-21T20:34:34.486296Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
