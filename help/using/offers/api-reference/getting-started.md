---
title: 快速入門
description: 了解如何開始使用優惠方案庫API，以使用決策管理引擎執行重要作業。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 6%

---

# Decision Management API開發人員指南

本開發人員指南提供步驟，協助您開始使用 [!DNL Offer Library] API。 然後，指南會提供使用決策管理引擎執行關鍵作業的範例API呼叫。

➡️ [在影片中探索此功能](#video)

## 先決條件

本指南需要妥善了解下列Adobe Experience Platform元件：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}:標準化框架 [!DNL Experience Platform] 組織客戶體驗資料。
   * [結構構成基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html){target=&quot;_blank&quot;}:了解XDM結構的基本建置組塊。
* [決策管理](../../../using/offers/get-started/starting-offer-decisioning.md):一般說明Experience Decisioning使用的概念和元件，尤其是Offer decisioning。 說明在客戶體驗期間，用於選擇要呈現的最佳選項的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target=&quot;_blank&quot;}:PQL是一種功能強大的語言，可通過XDM實例編寫表達式。 PQL用於定義決策規則。

## 讀取範例API呼叫

本指南提供範例API呼叫，以示範如何設定請求格式。 這些功能包括路徑、必要標題和格式正確的請求裝載。 也提供API回應中傳回的範例JSON。 如需範例API呼叫檔案中所使用慣例的相關資訊，請參閱 [如何閱讀API呼叫範例](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target=&quot;_blank&quot;}，位於 [!DNL Experience Platform] 疑難排解指南。

## 收集必要標題的值

若要對 [!DNL Platform] API，您必須先完成 [驗證教學課程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;}。 完成驗證教學課程會提供所有 [!DNL Experience Platform] API呼叫，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

所有包含裝載(POST、PUT、PATCH)的請求都需要額外的標題：

* `Content-Type: application/json`

## 管理容器的存取權

容器是隔離機制，可分開不同的關注點。 容器ID是所有存放庫API的第一個路徑元素。 所有決策物件都位於容器中。

管理員可將類似的主體、資源和存取權限分組至設定檔中。 這可減輕管理負擔，並受支援 [Adobe Admin Console](https://adminconsole.adobe.com/). 您必須是組織中Adobe Experience Platform的產品管理員，才能建立設定檔並指派使用者。 只要在一次性步驟中建立符合特定權限的產品設定檔，然後將使用者新增至這些設定檔即可。 設定檔會作為已獲授權的群組，該群組中的每位實際使用者或技術使用者都會繼承這些權限。

您可以透過 [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}。 如需詳細資訊，請參閱 [存取控制概觀](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

### 清單容器供使用者存取及整合

**API格式**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | 依容器與產品內容的關聯來篩選容器清單。 | `acp` |
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

成功的回應會傳回關於決策管理容器的資訊。 這包括 `instanceId` 屬性，其值為容器ID。

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

本檔案說明呼叫 [!DNL Offer Library] API，包括取得容器ID。 您現在可以繼續閱讀開發人員指南中提供的範例呼叫，並遵循其指示。

## 教學課程影片 {#video}

以下影片旨在協助您了解決策管理的元件。

>[!NOTE]
>
>此影片適用於以Adobe Experience Platform為基礎的Offer decisioning應用程式服務。 不過，它提供在Journey Optimizer內容中使用Offer的一般指引。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
