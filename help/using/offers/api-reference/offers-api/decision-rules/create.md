---
title: 建立決定規則
description: 決策規則是新增至個人化優惠方案的限制，並套用至設定檔以判斷資格。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 10%

---

# 建立決定規則

決策規則是新增至個人化優惠方案的限制，並套用至設定檔以判斷資格。

## 接受和內容類型標題

下表顯示了 *內容類型* 和 *接受* 請求標題中的欄位：

| 標題名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 決策規則所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**要求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Sales rule",
        "description": "Decisioning rule for sales",
        "condition": {
            "type": "PQL",
            "format": "pql/text",
            "value": "profile.person.name.firstName.equals(\"Joe\", false)"
        },
        "xdm:definedOn": {
            "profile": {
                "xdm:schema": {
                    "$ref": "https://ns.adobe.com/xdm/context/profile_union",
                    "version": "1"
                },
                "xdm:referencePaths": [
                    "person.name.firstName"
                ]
            }
        }
    }'
```

**回應**

成功的回應會傳回新建立決策規則的相關資訊，包括其唯一例項ID和位置 `@id`. 您可以在後續步驟中使用例項ID來更新或刪除您的決策規則。 您可以使用您的唯一決策規則 `@id` 在稍後的教學課程中，建立個人化優惠方案。

```json
{
    "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:13:43.048666Z",
    "repo:lastModifiedDate": "2020-10-21T20:13:43.048666Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
