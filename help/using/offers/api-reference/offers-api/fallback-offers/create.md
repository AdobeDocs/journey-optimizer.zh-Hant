---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 建立後備產品建議
description: 如果客戶不符合其他優惠方案的資格，系統會傳送遞補優惠方案給客戶
feature: Decision Management, API
badge: label="舊版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 156d6c71-d8fd-4631-ae0c-44452d664dde
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 25%

---

# 建立後備產品建議 {#create-fallback-offer}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！[了解更多](../../experience-decisioning/gs-experience-decisioning.md)


您可以對[!DNL Offer Library] API發出POST要求，以建立遞補優惠。

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示請求標頭中包含&#x200B;*Content-Type*&#x200B;欄位的有效值：

| 標題名稱 | 價值 |
| ----------- | ----- |
| Content-Type | `application/json` |

**API格式**

```http
POST /{ENDPOINT_PATH}/offers?offer-type=fallback
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |

**要求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offers?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Fallback Offer DPS",
    "description": "Fallback Offer description",
    "status": "approved",
    "selectionConstraint": {
        "startDate": "2022-06-10T00:30:00.000+00:00",
        "endDate": "2032-06-06T23:29:21.402+00:00",
        "profileConstraintType": "none"
    },
    "representations": [
        {
            "components": [
                {
                    "deliveryURL": "https://mysite.com",
                    "type": "imagelink",
                    "format": "image/png"
                }
            ],
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234"
        }
    ],
    "rank": {
        "priority": 1
    }
}'
```

**回應**

成功的回應會傳回新建立的遞補優惠的相關資訊，包括其唯一的遞補優惠`id`。 您可在稍後的步驟中使用`id`來更新或刪除您的遞補優惠，或在稍後的教學課程中建立決定。


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
