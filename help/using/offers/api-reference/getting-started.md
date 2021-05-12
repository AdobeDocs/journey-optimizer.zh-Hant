---
title: 快速入門
description: 瞭解如何開始使用選件程式庫API，以使用決策管理引擎執行關鍵作業。
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 7%

---

# 決策管理API開發人員指南

本開發人員指南提供協助您開始使用[!DNL Offer Library] API的步驟。 然後，指南提供使用決策管理引擎執行關鍵操作的範例API調用。

![](../../assets/do-not-localize/how-to-video.png) [在影片中探索此功能](#video)

## 先決條件

本指南需要對Adobe Experience Platform的下列組成部分有切實的瞭解：

* [[!DNL Experience Data Model (XDM) System]](https://docs.adobe.com/content/help/en/experience-platform/xdm/home.html):組織客戶體驗資 [!DNL Experience Platform] 料的標準化架構。
   * [架構構成基礎](https://docs.adobe.com/content/help/zh-Hant/experience-platform/xdm/schema/composition.html):瞭解XDM架構的基本建置區塊。
* [決策管理](../../../using/offers/get-started/starting-offer-decisioning.md):說明「體驗決策」的一般概念和元件，特別是Offer decisioning。說明在客戶體驗期間，選擇最佳呈現選項的策略。
* [[!DNL Profile Query Language (PQL)]](https://docs.adobe.com/content/help/en/experience-platform/segmentation/pql/overview.html):PQL是一種功能強大的語言，可編寫XDM實例的表達式。PQL用於定義決策規則。

## 讀取範例API呼叫

本指南提供範例API呼叫，以示範如何格式化您的請求。 這些包括路徑、必要標題和正確格式化的請求負載。 也提供API回應中傳回的範例JSON。 如需範例API呼叫檔案中所用慣例的詳細資訊，請參閱[!DNL Experience Platform]疑難排解指南中[如何讀取範例API呼叫](https://docs.adobe.com/content/help/en/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request)一節。

## 收集必要標題的值

若要呼叫[!DNL Platform] API，您必須先完成[驗證教學課程](https://docs.adobe.com/content/help/en/experience-platform/tutorials/authentication.html)。 完成驗證教學課程後，所有[!DNL Experience Platform] API呼叫中每個所需標題的值都會顯示在下面：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

所有包含裝載(POST、PUT、PATCH)的請求都需要額外的標題：

* `Content-Type: application/json`

## 管理容器的存取權

容器是隔離機制，可讓不同的顧慮分開。 容器ID是所有儲存庫API的第一個路徑元素。 所有決策物件都位於容器中。

管理員可以將類似的承擔者、資源和存取權限群組至設定檔。 這減輕了管理負擔，並得到[Adobe Admin Console](https://adminconsole.adobe.com/)的支援。 您必須是組織中Adobe Experience Platform的產品管理員，才能建立描述檔並指派使用者。 只要在一次性步驟中建立符合特定權限的產品設定檔，然後將使用者新增至這些設定檔即可。 設定檔會當成已授與權限的群組，而該群組中每個實際使用者或技術使用者都會繼承這些權限。

給定管理員權限後，您可以通過[Adobe Admin Console](https://adminconsole.adobe.com/)授予或撤消用戶權限。 有關詳細資訊，請參閱[訪問控制概述](https://docs.adobe.com/content/help/zh-Hant/experience-platform/access-control/home.html)。

### 列出使用者可存取的容器和整合

**API格式**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 依容器與產品上下文的關聯來篩選容器清單。 | `acp` |
| `{PROPERTY}` | 篩選傳回的容器類型。 | `_instance.containerType==decisioning` |

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

成功的回應會傳回有關決策管理容器的資訊。 這包含`instanceId`屬性，其值是您的容器ID。

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

## 後續步驟

本檔案涵蓋對[!DNL Offer Library] API進行呼叫所需的先決條件知識，包括取得容器ID。 您現在可以繼續閱讀本開發人員指南中提供的範例呼叫，並依照其指示進行。

## 教學課程影片{#video}

以下視頻旨在支援您對「決策管理」元件的瞭解。

>[!NOTE]
>
>此視訊適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 然而，它提供了在Journey Optimizer背景下使用選件的一般指導。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
