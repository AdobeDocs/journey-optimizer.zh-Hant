---
title: 刪除集合限定詞
description: 集合限定詞可讓您更妥善地組織和排序優惠方案。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 7%

---

# 刪除集合限定詞 {#delete-tag}

有時可能需要移除(DELETE)集合限定詞（先前稱為「標籤」）。 這可透過向以下對象執行DELETE請求來完成 [!DNL Offer Library] API使用您要刪除之集合限定詞的ID。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要刪除之實體的ID。 | `tag1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試查詢(GET)集合限定詞來確認刪除，應該會收到HTTP狀態404 （找不到），因為它已移除。