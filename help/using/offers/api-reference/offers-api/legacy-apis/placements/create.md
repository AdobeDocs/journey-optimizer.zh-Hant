---
title: 建立位置
description: 版位是用來展示優惠方案的容器。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c7301f6-95d3-4720-81fe-5f2602cd30ec
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 9%

---

# 建立位置 {#create-placement}

您可以透過向以下網站發出POST請求來建立位置： [!DNL Offer Library] API，同時提供容器ID。

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示包含 *Content-Type* 和 *Accept* 請求標頭中的欄位：

| 頁首名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 位置所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

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

成功的回應會傳回新建立位置的詳細資訊，包括其唯一的執行個體ID和位置 `@id`. 您可在後續步驟中使用執行個體ID來更新或刪除您的位置。 您可以使用不重複的位置 `@id` 在稍後的教學課程中，以建立決定、決定規則和遞補優惠。

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
