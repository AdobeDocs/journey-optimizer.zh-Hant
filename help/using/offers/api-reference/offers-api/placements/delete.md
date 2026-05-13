---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 刪除版位
description: 版位是用來展示優惠方案的容器。
feature: Decision Management, API
badge: label="舊版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/ACEsOlaOqRgSxKAkgd-X2IK0oL8IQ7vmv4RwTwyOMTA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: ed0d8d0e-04b9-4326-be72-a0fbca265377id: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 0%

---

# 刪除位置 {#delete-placement}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer]的全新決策功能「決策」現在可透過程式碼型體驗和電子郵件通道使用！ [進一步瞭解](../../../../experience-decisioning/gs-experience-decisioning.md)


有時可能必須移除(DELETE)位置。 使用您要刪除之位置的ID對[!DNL Offer Library] API執行DELETE要求，即可完成此作業。

**API格式**

```http
DELETE /{ENDPOINT_PATH}/placements/{ID}
```

| 引數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 持續性API的端點路徑。 | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | 您要更新之位置的例項ID。 | `offerPlacement1234` |

**要求**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回HTTP狀態200和空白內文。

您可以嘗試向位置查詢(GET)請求來確認刪除，應該會收到HTTP狀態404 （找不到），因為位置已移除。
