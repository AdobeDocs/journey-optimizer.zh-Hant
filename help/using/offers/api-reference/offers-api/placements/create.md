---
title: 建立版位
description: 版位是用來展示優惠方案的容器。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7b735873-86f5-466f-b079-5e84d9f03a08
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# 建立版位 {#create-placement}

您可以向 [!DNL Offer Library] API，同時提供容器ID。

## 接受和內容類型標題 {#accept-and-content-type-headers}

下表顯示了 *內容類型* 和 *接受* 請求標題中的欄位：

| 標題名稱 | 值 |
| ----------- | ----- |
| 接受 | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| 內容類型 | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 版位所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**要求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Sales Placement",
        "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
        "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
        "xdm:description": "A test placement to contain offers"
    }'
```

**回應**

成功的回應會傳回新建立版位的詳細資訊，包括其唯一例項ID和版位 `@id`. 您可以在後續步驟中使用例項ID來更新或刪除您的版位。 您可以使用不重複位置 `@id` 在稍後的教學課程中，建立決策、決策規則和備援優惠方案。

```json
{
    "instanceId": "9aa58fd0-13d7-11eb-928b-576735ea4db8",
    "@id": "xcore:offer-placement:124e0be5699743d3",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T19:57:09.837456Z",
    "repo:lastModifiedDate": "2020-10-21T19:57:09.837456Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
