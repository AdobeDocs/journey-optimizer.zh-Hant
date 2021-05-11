---
title: 更新標籤
description: 標籤可讓您更妥善地整理和排序選件。
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 8%

---

# 更新標籤

您可以對[!DNL Offer Library] API提出PATCH要求，以修改或更新容器中的標籤。

如需JSON修補程式的詳細資訊，包括可用的作業，請參閱官方的[JSON修補程式檔案](http://jsonpatch.com/)。

## 接受和內容類型標題

下表顯示請求標題中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;欄位的有效值：

| 標題名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 標籤所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新之標籤的例項ID。 | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**要求**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
          "op": "replace",
          "path": "/_instance/xdm:name",
          "value": "Sales and promotions for the holidays"
        }
    ]'
```

| 參數 | 說明 |
| --------- | ----------- |
| `op` | 用於定義更新連接所需操作的操作調用。 運營包括：`add`、`replace`和`remove`。 |
| `path` | 要更新的參數路徑。 |
| `value` | 您要用來更新參數的新值。 |

**回應**

成功的回應會傳回標籤的更新詳細資料，包括其唯一例項ID和標籤`@id`。

```json
{
    "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2020-10-21T20:36:31.782607Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
