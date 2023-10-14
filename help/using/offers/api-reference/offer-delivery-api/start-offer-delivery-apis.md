---
title: 開始使用傳遞優惠方案 API
description: 深入瞭解可用於提供個人化優惠的API。
feature: Offers, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 5%

---

# 開始使用傳遞優惠方案 API {#about-decisioning-apis}

您可以使用以下任一專案來傳遞優惠方案： **決策** 或 **邊緣決策** API。 此外， **批次決策** API可讓您透過一次呼叫，將優惠方案傳送給指定對象中的所有設定檔。 對象中每個設定檔的選件內容都會放在Adobe Experience Platform資料集中，可用於自訂批次工作流程。

在此頁面中，您會找到特定功能的相關資訊，這些功能包括 **決策** 和 **邊緣決策** API。 雖然兩者都可讓您為客戶提供優惠方案，我們建議您使用 **邊緣決策** API會儘可能用於傳入使用案例，並確保平台上有更好的延遲和輸送量。


如需如何使用API的詳細資訊，請參閱下列章節：
* [決策 API](decisioning-api.md)
* [邊緣決策 API](edge-decisioning-api.md)
* [批次決策 API](batch-decisioning-api.md)

## 管理對容器的存取 {#manage-access-to-container}

容器是一種隔離機制，可隔離不同的關注點。 容器ID是所有存放庫API的第一個路徑元素。 所有決策物件都位於容器內。

管理員可以將類似的主體、資源和存取許可權分組到設定檔中。 這能減輕管理負擔，並受到以下支援 [Adobe Admin Console](https://adminconsole.adobe.com/). 您必須是組織中Adobe Experience Platform的產品管理員，才能建立設定檔並將使用者指派給設定檔。 只需在一次性步驟中建立符合特定許可權的產品設定檔，然後只需將使用者新增到這些設定檔即可。 設定檔會作為已授予許可權的群組，而該群組中的每個實際使用者或技術使用者都會繼承這些許可權。

授予管理員許可權，您可以透過授予或撤銷使用者許可權 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hant){target="_blank"}.

### 列出可供使用者和整合使用者存取的容器 {#list-containers-accessible-to-users-and-integrations}

**API格式**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 依照容器與產品前後關聯的關聯來篩選容器清單。 | `acp` |
| `{PROPERTY}` | 篩選傳回的容器型別。 | `_instance.containerType==decisioning` |

**要求**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**回應**

成功的回應會傳回有關決定管理容器的資訊。 這包括 `instanceId` 屬性，的值為您的容器ID。

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## Edge Decisioning API功能 {#edge}

**體驗事件和決策請求的不重複請求**

有了Edge Decisioning API，您可以在一個單一請求中連同決策請求一起傳送體驗事件本身，而不是有兩個不同的請求。

例如，如果客戶造訪您的網站，要求會包含體驗事件（客戶造訪的頁面），並取得選件以填入造訪的頁面。

**將內容資料儲存至Adobe Experience Platform**

內容資料是指您只知道想要回某個優惠方案的資料。 例如，所購買文章的顏色、購買時的天氣等。

使用Edge Decisioning API請求傳遞內容資料時，資料會儲存在Adobe Experience Platform設定檔中，以便日後重複使用。

>[!NOTE]
>
>為了儲存內容資料，您需要設定專用的XDM結構描述。

## 決策API功能 {#decisioning}

下列功能僅適用於Decisioning API。 如果您需要運用其中一種來滿足需求，請使用決策API。 否則，我們建議使用邊緣決策API。

* **體驗事件**：運用體驗事件來建立您的決策規則。
* **選件內容和特性**：您可以使用專用選項來選擇不傳回選件的內容和特性。
* **優惠中繼資料**：啟用傳回選件中繼資料的選項。
* **合併原則**：在您的請求中使用與沙箱關聯的不同合併原則。
* **決策事件和頻率限定**：封鎖決策事件，不讓發生的任何頻率上限計算在內。
* **重複的主張**：啟用不重複主張的選項。
