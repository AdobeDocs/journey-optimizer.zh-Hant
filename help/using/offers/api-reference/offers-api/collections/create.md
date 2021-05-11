---
title: 建立集合
description: 系列是選件的子集，根據行銷人員定義的預先定義條件，例如選件類別。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---

# 建立集合

系列是選件的子集，根據行銷人員定義的預先定義條件，例如選件類別。

您可以在提供容器ID的同時，向[!DNL Offer Library] API提出POST請求，以建立系列。

## 接受和內容類型標題

下表顯示請求標題中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;欄位的有效值：

| 標題名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 系列所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**要求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Offer Collection 1",
        "xdm:filterType": "anyTags",
        "xdm:ids": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**回應**

成功的回應會傳回新建立之系列的資訊，包括其唯一例項ID和位置`@id`。 您可以在後續步驟中使用例項ID來更新或刪除系列。 您可以在稍後的教學課程中使用您唯一的系列`@id`來建立決策。

```json
{
    "instanceId": "0bf31c20-13f1-11eb-a752-e58fd7dc4cb3",
    "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2020-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
