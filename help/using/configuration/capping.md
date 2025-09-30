---
solution: Journey Optimizer
product: journey optimizer
title: 設定 API 上限
description: 瞭解如何使用上限API
feature: Journeys, API
role: Developer
level: Beginner
keywords: 外部， API，最佳化工具，上限
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: 13af123030449d870f44f3470710b0da2c6f4775
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 6%

---

# 使用上限API {#work}

上限API可幫助您建立、設定和監控您的上限設定。

本節提供如何使用API的全域資訊。 [Adobe Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}中提供詳細的API描述。

## 設定API說明與Postman集合的上限 {#description}

下表列出適用於上限API的可用命令。 [Adobe Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/references/journeys/){target="_blank"}提供詳細資訊，包括要求範例、引數和回應格式。

| 方法 | 路徑 | 說明 |
|---|---|---|
| [!DNL POST] | list/endpointConfig | 取得端點上限設定清單 |
| [!DNL POST] | /endpointConfigs | 建立端點上限設定 |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | 部署端點上限設定 |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | 取消部署端點上限設定 |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | 檢查是否可以部署端點上限設定 |
| [!DNL PUT] | /endpointConfigs/`{uid}` | 更新端點上限設定 |
| [!DNL GET] | /endpointConfigs/`{uid}` | 擷取端點上限設定 |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | 刪除端點上限設定 |

建立或更新設定時，會自動執行檢查以確保語法和裝載的完整性。
如果發生某些問題，作業會傳回警告或錯誤，以協助您更正設定。

此外，[這裡](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json)也提供Postman集合，協助您進行測試設定。

此集合已設定為共用透過&#x200B;__[Postman Console的整合功能產生的Adobe I/O變數集合](https://console.adobe.io/integrations) >嘗試使用>下載Postman__，這會產生具有所選整合值的Postman環境檔案。

一旦下載並上傳至 Postman，您需要新增三個變數：`{JO_HOST}`、`{BASE_PATH}`以及`{SANDBOX_NAME}`。
* `{JO_HOST}` ： [!DNL Journey Optimizer]閘道URL。
* `{BASE_PATH}` ： API的進入點。
* `{SANDBOX_NAME}`：標題 **x-sandbox-name** (例如，&#39;prod&#39;)，此名稱對應於將進行 API 操作的沙箱名稱。如需詳細資訊，請參閱[沙箱概觀](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hant){target="_blank"}。

## 端點設定

以下是端點設定的基本結構：

```json
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint (optional)>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

>[!IMPORTANT]
>
>**maxHttpConnections**&#x200B;引數是選用的。 它可讓您限制Journey Optimizer將開啟給外部系統的連線數量。
>
>可設定的最大值為400。 如果未指定任何專案，則系統可能會開啟數千個連線，視系統的動態縮放而定。
>
>部署上限設定時，如果尚未設定`maxHttpConnections`值，則會將預設`maxHttpConnections = -1`新增到部署的設定，而Journey Optimizer會使用預設系統值。

範例：

```json
{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  }
}
```

>[!IMPORTANT]
>
>只有在呼叫&#x200B;**部署**&#x200B;端點之後，設定才會啟用。

## 警告和錯誤

呼叫&#x200B;**canDeploy**&#x200B;方法時，程式會驗證設定並傳回由其唯一識別碼識別的驗證狀態：

```json
"ok" or "error"
```

可能的錯誤包括：

* **ERR_ENDPOINTCONFIG_100**：設定上限：遺漏或無效的url
* **ERR_ENDPOINTCONFIG_101**：上限設定：格式錯誤的url
* **ERR_ENDPOINTCONFIG_102**：上限設定：格式錯誤的url：主機:port不允許url中的wildchar
* **ERR_ENDPOINTCONFIG_103**：上限設定：遺失HTTP方法
* **ERR_ENDPOINTCONFIG_104**：上限設定：未定義任何通話分級
* **ERR_ENDPOINTCONFIG_107**：上限設定：無效的最大呼叫計數(maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**：上限設定：無效的最大呼叫計數(periodInMs)
* **ERR_ENDPOINTCONFIG_111**：上限設定：無法建立端點設定：無效的承載
* **ERR_ENDPOINTCONFIG_112**：上限設定：無法建立端點設定：需要JSON裝載
* **ERR_AUTHORING_ENDPOINTCONFIG_1**：無效的服務名稱`<!--<given value>-->`：必須為&#39;dataSource&#39;或&#39;action&#39;

可能的警告為：

**ERR_ENDPOINTCONFIG_106**：上限設定：未定義最大HTTP連線：預設無限制

## 使用案例

本節列出在[!DNL Journey Optimizer]中管理上限設定的主要使用案例，以及實施使用案例所需的相關API命令。

每個API命令的詳細資訊可在[API說明和Postman集合](#description)中取得。

+++建立及部署新的上限設定

要使用的API呼叫：

1. **`list`** — 擷取現有設定。
1. **`create`** — 建立新的組態。
1. **`candeploy`** — 檢查組態是否可以部署。
1. **`deploy`** — 部署設定。

+++

+++更新並部署上限設定（尚未部署）

要使用的API呼叫：

1. **`list`** — 擷取現有設定。
1. **`get`** — 擷取特定設定的詳細資料。
1. **`update`** — 修改設定。
1. **`candeploy`** — 檢查部署資格。
1. **`deploy`** — 部署設定。

+++

+++取消部署和刪除已部署的上限設定

要使用的API呼叫：

1. **`list`** — 擷取現有設定。
1. **`undeploy`** — 取消部署設定。
1. **`delete`** — 移除設定。

+++

+++在一個步驟中刪除已部署的上限設定

您只能在一個API呼叫中使用`forceDelete`引數來取消部署及刪除組態。

要使用的API呼叫：

1. **`list`** — 擷取現有設定。
1. **`delete`（含`forceDelete`引數）** — 在單一步驟中強制刪除已部署的組態。

+++

+++更新已部署的上限設定

>[!NOTE]
>
>更新已部署的組態後需要重新部署。

要使用的API呼叫：
1. **`list`** — 擷取現有設定。
1. **`get`** — 擷取特定設定的詳細資料。
1. **`update`** — 修改設定。
1. **`undeploy`** — 在套用變更之前先取消部署設定。
1. **`candeploy`** — 檢查部署資格。
1. **`deploy`** — 部署更新的設定。

+++
