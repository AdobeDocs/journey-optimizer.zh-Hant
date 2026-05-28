---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 刪除決定規則
description: 決定規則是新增至個人化優惠的限制，並套用至設定檔以判斷適用性。
feature: Decision Management, API
badge: label="舊版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/JZhp7DudmeNDzePS2JYGVq-JHcnKPSj-HgsEvFtiSmc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 20%

---

# 刪除決定規則 {#delete-decision-rule}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../../../../experience-decisioning/gs-experience-decisioning.md)


有時可能必須移除(DELETE)決定規則。 這是透過使用您要刪除的決定規則`id`對[!DNL Offer Library] API執行DELETE要求來完成。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | 您要刪除之實體的ID。 | `offerRule1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以透過嘗試對決定規則進行查詢(GET)請求來確認刪除，並且應該會收到HTTP狀態404 （找不到），因為決定規則已移除。
