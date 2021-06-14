---
title: 建立個人化優惠
description: 個人化優惠方案是根據適用性規則和限制而自訂的行銷訊息。
feature: 優惠
topic: 整合
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 12%

---

# 建立個人化優惠

個人化優惠方案是根據適用性規則和限制而自訂的行銷訊息。

您可以向[!DNL Offer Library] API提出POST要求，同時提供容器ID，借此建立個人化優惠方案。

## 接受和內容類型標題

下表顯示了請求標題中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;欄位的有效值：

| 標題名稱 | 值 |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 個人化優惠方案所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**要求**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Sale offer",
        "xdm:status": "draft",
        "xdm:representations": [
            {
                "xdm:components": [
                    {
                        "dc:language": [
                            "en"
                        ],
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                        "dc:format": "text/html"
                    }
                ],
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
            }
        ],
        "xdm:selectionConstraint": {
            "xdm:startDate": "2020-10-01T16:00:00Z",
            "xdm:endDate": "2021-12-13T16:00:00Z",
            "xdm:eligibilityRule": "xcore:eligibility-rule:124e0faf5b8ee89b"
        },
        "xdm:rank": {
            "xdm:priority": 1
        },
        "xdm:cappingConstraint": {
            "xdm:globalCap": 150
        },
        "xdm:tags": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**回應**

成功的回應會傳回新建立之個人化優惠方案的資訊，包括其唯一例項ID和版位`@id`。 您可以在後續步驟中使用執行個體ID來更新或刪除您的個人化優惠方案。

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2020-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
