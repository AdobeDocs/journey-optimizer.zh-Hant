---
title: 快速入門
description: 瞭解如何開始使用「提供庫API」使用決策管理引擎執行關鍵操作。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 5%

---

# 決策管理API開發人員指南 {#decision-management-api-developer-guide}

本開發人員指南提供了幫助您開始使用 [!DNL Offer Library] API。 然後，本指南提供了使用決策管理引擎執行關鍵操作的示例API調用。

➡️ [瞭解有關此視頻中決策管理元件的更多資訊](#video)

## 先決條件 {#prerequisites}

本指南要求對Adobe Experience Platform的下列組成部分有工作上的理解：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;:標準化框架 [!DNL Experience Platform] 組織客戶體驗資料。
   * [架構組合的基礎](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html){target=&quot;_blank&quot;:瞭解XDM架構的基本構建塊。
* [決策管理](../../../using/offers/get-started/starting-offer-decisioning.md):說明一般和特別是Offer decisioning中用於經驗決策的概念和元件。 說明了在客戶體驗期間用於選擇最佳選擇的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target=&quot;_blank&quot;:PQL是一種功能強大的語言，可在XDM實例上編寫表達式。 PQL用於定義決策規則。

## 讀取示例API調用 {#reading-sample-api-calls}

本指南提供了示例API調用，以演示如何格式化請求。 這些包括路徑、必需的標頭和正確格式化的請求負載。 還提供了API響應中返回的示例JSON。 有關示例API調用文檔中使用的約定的資訊，請參見上的 [如何讀取示例API調用](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target=&quot;_blank&quot;} [!DNL Experience Platform] 疑難解答指南。

## 收集所需標題的值 {#gather-values-for-required-headers}

為了呼叫 [!DNL Adobe Experience Platform] API，必須首先完成 [驗證教程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;}。 完成身份驗證教程將提供所有中每個必需標頭的值 [!DNL Experience Platform] API調用，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

包含負載(POST、PUT、PATCH)的所有請求都需要附加的標頭：

* `Content-Type: application/json`

## 管理對容器的訪問 {#manage-access-to-container}

容器是一種隔離機構，用於將不同的問題分開。 容器ID是所有儲存庫API的第一個路徑元素。 所有決策對象都駐留在容器中。

管理員可以將類似的承擔者、資源和訪問權限分組到配置式中。 這減輕了管理負擔，並受 [Adobe Admin Console](https://adminconsole.adobe.com/)。 您必須是組織中Adobe Experience Platform的產品管理員才能建立配置檔案並為其分配用戶。 只需在一次性步驟中建立與某些權限相匹配的產品配置檔案，然後將用戶添加到這些配置檔案即可。 配置檔案充當已授予權限的組，該組中的每個實際用戶或技術用戶都繼承這些權限。

給定管理員權限，您可以通過 [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}。 有關詳細資訊，請參見 [訪問控制概述](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

### 列出可供用戶和整合訪問的容器 {#list-containers-accessible-to-users-and-integrations}

**API格式**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的終結點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 按容器與產品上下文的關聯篩選容器清單。 | `acp` |
| `{PROPERTY}` | 篩選返回的容器類型。 | `_instance.containerType==decisioning` |

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

成功的響應返回有關決策管理容器的資訊。 這包括 `instanceId` 屬性，其值為容器ID。

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

## 後續步驟 {#next-steps}

本文檔涵蓋了呼叫 [!DNL Offer Library] API，包括獲取容器ID。 現在，您可以繼續閱讀本開發人員指南中提供的示例調用，並按照其說明進行操作。

>[!NOTE]
>
> Adobe Journey Optimizer的In-app消息通道使用offer decisioning對象。 如果您的組織使用應用內消息傳遞通道，則對象的API清單請求將包括應用內消息傳遞服務建立的對象，並且可以忽略這些對象以用於offer decisioning使用案例。 為應用內消息建立的對象將具有 `createdBy = “Mobile_Sheliak”`。

## How-to視頻 {#video}

以下視頻旨在支援您對「決策管理」元件的瞭解。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

