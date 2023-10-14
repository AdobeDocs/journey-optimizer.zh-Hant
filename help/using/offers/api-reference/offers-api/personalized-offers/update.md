---
title: 更新個人化優惠
description: 個人化優惠是根據適用性規則和限制的可自訂行銷訊息。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 9d8f2df6-aa04-4e66-8555-d51c2e409063
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 8%

---

# 更新個人化優惠 {#update-personalized-offer}

您可以透過向以下網站發出PATCH請求，修改或更新個人化優惠： [!DNL Offer Library] API

如需JSON修補程式的詳細資訊，包括可用的作業，請參閱官方檔案 [JSON修補程式檔案](https://jsonpatch.com/).

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示包含 *Content-Type* 請求標頭中的欄位：

| 頁首名稱 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要更新之實體的ID。 | `personalizedOffer1234` |

**要求**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated personalized offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated personalized offer description"
    }
]'
```

| 參數 | 說明 |
| --------- | ----------- |
| `op` | 用於定義更新連線所需動作的操作呼叫。 操作包括： `add`， `replace`， `remove`， `copy` 和 `test`. |
| `path` | 要更新之引數的路徑。 |
| `value` | 您想要用來更新引數的新值。 |

**回應**

成功的回應會傳回位置的最新詳細資料，包括位置ID。

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
