---
title: 更新遞補優惠
description: 如果客戶不符合其他優惠條件，則會向他們發送備用優惠
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7ff69887-620f-4bc0-b8ff-5144ff30696c
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 10%

---

# 更新遞補優惠 {#update-fallback-offer}

您可以通過向PATCH請求修改或更新您的貨箱中的備用優惠 [!DNL Offer Library] API。

有關JSON修補程式（包括可用操作）的詳細資訊，請參閱 [JSON修補程式文檔](http://jsonpatch.com/)。

## 接受和內容類型標題 {#accept-and-content-type-headers}

下表顯示了組成 *內容類型* 和 *接受* 請求標題中的欄位：

| 標題名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的終結點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 回退優惠所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 回退要約的實例ID。 | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**要求**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'\
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:status",
            "value": "approved"
        }
    ]
```

| 參數 | 說明 |
| --------- | ----------- |
| `op` | 用於定義更新連接所需操作的操作調用。 操作包括： `add`。 `replace`, `remove`。 |
| `path` | 要更新的參數的路徑。 |
| `value` | 要用更新參數的新值。 |

**回應**

成功的響應將返回回退要約的更新詳細資訊，包括其唯一實例ID和回退要約 `@id`。

```json
{
    "instanceId": "b3966680-13ec-11eb-9c20-8323709cfc65",
    "@id": "xcore:fallback-offer:124e2e764b1ac1b9",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-21T22:28:11.111732Z",
    "repo:lastModifiedDate": "2020-10-21T22:33:08.676919Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
