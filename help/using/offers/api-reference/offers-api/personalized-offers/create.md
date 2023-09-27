---
title: 建立個人化優惠
description: 個人化優惠是根據適用性規則和限制的可自訂行銷訊息。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 97dc9af3-ca31-4512-aad2-f959dfc9ad0b
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 10%

---

# 建立個人化優惠 {#create-personalized-offer}

個人化優惠是根據適用性規則和限制的可自訂行銷訊息。

您可以透過向以下網站發出POST請求，建立個人化優惠方案： [!DNL Offer Library] API。

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示包含 *Content-Type* 請求標頭中的欄位：

| 頁首名稱 | 值 |
| ----------- | ----- |
| Content-Type | `application/json` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**API格式**

```http
POST /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |

**要求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offers?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test personalized offer with frequency constraint",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "html",
                    "format": "text/html",
                    "language": [
                        "en-us"
                    ],
                    "content": "Hello You qualify for our Discount of 60%"
                }
            ]
        }
    ],
    "selectionConstraint": {
        "startDate": "2022-07-27T05:00:00.000+00:00",
        "endDate": "2023-07-29T05:00:00.000+00:00",
        "profileConstraintType": "none"
    },
    "rank": {
        "priority": 0
    },
    "cappingConstraint": {},
    "frequencyCappingConstraints": [
        {
            "enabled": false,
            "limit": 1,
            "startDate": "2023-05-15T14:25:49.622+00:00",
            "endDate": "2023-05-25T14:25:49.622+00:00",
            "scope": "global",
            "entity": "offer",
            "repeat": {
                "enabled": false,
                "unit": "month",
                "unitCount": 1
            }
        }
    ]
}'
```

**回應**

成功的回應會傳回新建立的個人化優惠詳細資料，包括id。 您可以使用 `id` 在後續步驟中更新或刪除您的個人化優惠。

```json
{
    "etag": 1,
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

## 限制 {#limitations}

行動裝置目前不支援優惠宣告和某些優惠方案限制 [!DNL Experience Edge] 例如，工作流程 `Capping`. 此 `Capping` 欄位值會指定某個優惠方案在所有使用者中顯示的次數。 如需詳細資訊，請參閱 [優惠適用性規則和限制檔案](../../../offer-library/creating-personalized-offers.md).