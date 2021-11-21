---
title: 更新決策
description: 決策包含通知選件選擇的邏輯。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 98c5ccf9-2a7f-4129-a520-d0671a86e13d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 8%

---

# 更新決定

您可以借由向 [!DNL Offer Library] API。

如需JSON修補程式的詳細資訊，包括可用的操作，請參閱 [JSON修補程式檔案](http://jsonpatch.com/).

## 接受和內容類型標題

下表顯示了 *內容類型* 和 *接受* 請求標題中的欄位：

| 標題名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 決策的例項ID。 | `f88c9be0-1245-11eb-8622-b77b60702882` |

**要求**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '[
        {
            "op": "replace",
            "path": "/_instance/xdm:name",
            "value": "Example Activity Name"
        }
    ]'
```

| 參數 | 說明 |
| --------- | ----------- |
| `op` | 用來定義更新連線所需動作的操作呼叫。 操作包括： `add`, `replace`，和 `remove`. |
| `path` | 要更新的參數的路徑。 |
| `value` | 您要用更新參數的新值。 |

**回應**

成功的回應會傳回決策的更新詳細資訊，包括其唯一例項ID和決策 `@id`.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 2,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T21:28:24.284719Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
