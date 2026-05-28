---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 更新集合
description: 集合是優惠方案的子集，根據行銷人員定義的預先定義條件，例如優惠方案類別。
feature: Decision Management, API, Collections
badge: label="舊版" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: bf12d22f-e6c0-45fd-a2b2-149d3f4cf882
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/6IMCGBo0Mi1Xokge4f7i9QBfdoVikblWSOuT76Ziapw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 188
ht-degree: 17%

---

# 更新集合 {#update-collection}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../../../../../experience-decisioning/gs-experience-decisioning.md)


您可以透過向[!DNL Offer Library] API發出PATCH請求來修改或更新集合

如需JSON修補程式的詳細資訊，包括可用的作業，請參閱官方[JSON修補程式檔案](https://jsonpatch.com/)。

## Accept和Content-Type標題 {#accept-and-content-type-headers}

下表顯示請求標頭中包含&#x200B;*Content-Type*&#x200B;和&#x200B;*Accept*&#x200B;欄位的有效值：

| 標題名稱 | 值 |
| ----------- | ----- |
| 接受 | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**API格式**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | 集合所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | 您要更新之集合的執行個體ID。 | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**要求**

```shell
curl -X PATCH \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/vnd.adobe.platform.xcore.patch.hal+json; version=1; schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
            "op": "add",
            "path": "/_instance/xdm:filterType",
            "value": "anyTags"
    },
    {
            "op": "add",
            "path": "/_instance/xdm:ids",
            "value": ["xcore:tag:124e147572cd7866"]
    }
]'
```

| 參數 | 說明 |
| --------- | ----------- |
| `op` | 用於定義更新連線所需動作的操作呼叫。 作業包括： `add`、`replace`和`remove`。 |
| `path` | 要更新之引數的路徑。 |
| `value` | 您想要用來更新引數的新值。 |

**回應**

成功的回應會傳回集合的更新詳細資料，包括其唯一的執行個體識別碼和集合`@id`。

```json
{
    "instanceId": "0bf31c20-13f1-11eb-a752-e58fd7dc4cb3",
    "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2023-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
