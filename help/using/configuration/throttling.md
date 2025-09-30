---
solution: Journey Optimizer
product: journey optimizer
title: 節流 API
description: 瞭解如何使用節流API
feature: Journeys, API
role: Developer
level: Beginner
keywords: 外部， API，最佳化工具，上限
exl-id: b837145b-1727-43c0-a0e2-bf0e8a35347c
source-git-commit: 13af123030449d870f44f3470710b0da2c6f4775
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 48%

---

# 使用節流 API

節流API可協助您建立、設定和監視節流設定，以限制每秒傳送的事件數。

本節提供如何使用API的全域資訊。 [Adobe Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}中提供詳細的API描述。

## 必讀

* **每個組織一個組態：**&#x200B;目前每個組織只允許一個組態。 必須在生產沙箱上定義設定（透過標頭中的`x-sandbox-name`提供）。
* **組織層級應用程式：**&#x200B;在組織層級套用組態。
* **API限制處理：**&#x200B;當達到API中設定的限制時，其他事件將最多排入6小時的佇列。 無法修改此值。
* **`maxHttpConnections`引數：** `maxHttpConnections`引數是可選引數，可在Capping API中使用，僅允許您限制Journey Optimizer將開啟至外部系統的連線數目。 [瞭解如何使用上限API](../configuration/capping.md)

  如果您想限制連線的數量，同時也要限制這些外部呼叫，則可以在相同端點上設定兩個設定，一個限制和一個上限。 兩個設定可以共存於一個端點。 若要為節流端點設定「maxHttpConnections」，請使用節流API設定節流臨界值，並使用上限API設定「maxHttpConnections」。 呼叫上限API時，您可以將上限臨界值設為高於節流臨界值的專案，這樣上限規則就不會有效發揮作用。

## 節流API說明與Postman集合 {#description}

下表列出可用於節流API的命令。 [Adobe Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/references/journeys/)提供詳細資訊，包括要求範例、引數和回應格式。

| 方法 | 路徑 | 說明 |
|---|---|---|
| [!DNL POST] | list/throttlingConfigs | 取得節流設定的清單 |
| [!DNL POST] | /throttlingConfigs | 建立節流設定 |
| [!DNL POST] | /throttlingConfigs/`{uid}`/deploy | 部署節流設定 |
| [!DNL POST] | /throttlingConfigs/`{uid}`/undeploy | 取消部署節流設定 |
| [!DNL POST] | /throttlingConfigs/`{uid}`/canDeploy | 檢查是否可以部署節流設定 |
| [!DNL PUT] | /throttlingConfigs/`{uid}` | 更新節流設定 |
| [!DNL GET] | /throttlingConfigs/`{uid}` | 擷取節流設定 |
| [!DNL DELETE] | /throttlingConfigs/`{uid}` | 刪除節流設定 |

此外，[這裡](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Throttling-API_postman-collection.json){target="_blank"}也提供Postman集合，協助您進行測試設定。

此集合已設定為共用透過&#x200B;**[Postman Console的整合功能產生的Adobe I/O變數集合](https://console.adobe.io/integrations) >嘗試使用>下載Postman**，這會產生具有所選整合值的Postman環境檔案。

一旦下載並上傳至 Postman，您需要新增三個變數：`{JO_HOST}`、`{BASE_PATH}`以及`{SANDBOX_NAME}`。

* `{JO_HOST}` ： [!DNL Journey Optimizer]閘道URL。
* `{BASE_PATH}` ： API的進入點。
* `{SANDBOX_NAME}`：標題 **x-sandbox-name** (例如，&#39;prod&#39;)，此名稱對應於將進行 API 操作的沙箱名稱。如需詳細資訊，請參閱[沙箱概觀](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hant){target="_blank"}。

## 節流設定{#configuration}

以下是節流設定的結構。 **name**&#x200B;及&#x200B;**description**&#x200B;屬性為選用。

```json
{
    "name": "<given name - free text>",
    "description": "<given description - free text>"
    "urlPattern": "<endpoint URL - wildcards are allowed>",
    "methods": [ "<HTTP method such as GET, POST, PUT>" ],
    "maxThroughput": <max call throughput>
}
```

範例：

```json
{
  "name": "throttling-config-external",
  "description": "example of throttling config for an external endpoint",
  "urlPattern": "https://api.example.org/data/2.5/*",
  "methods": ["POST", "PUT"],
  "maxThroughput": 4000
}
```

>[!IMPORTANT]
>
>只有在呼叫&#x200B;**部署**&#x200B;端點之後，設定才會啟用。

## 錯誤

建立或更新設定時，流程會驗證指定的設定，並傳回以其唯一 ID 識別的驗證狀態，其中一項為：

```json
"ok" or "error"
```

>[!IMPORTANT]
>
>屬性 **maxThroughput**、**urlPattern**&#x200B;及&#x200B;**方法**&#x200B;為必填。
>
>**maxThroughput** 值必須在 200-5000 範圍內。

當建立、刪除或部署節流設定時，可能會發生以下錯誤：

* **ERR_THROTTLING_CONFIG_100**：節流設定：`<mandatory attribute>`必填
* **ERR_THROTTLING_CONFIG_101**：節流設定：maxThroughput 為必填，且必須大於或等於 200 且小於或等於 5,000
* **ERR_THROTTLING_CONFIG_104**：節流設定：格式錯誤的 URL 模式
* **ERR_THROTTLING_CONFIG_105**：節流設定：URL 模式的主機部分不允許使用萬用字元
* **ERR_THROTTLING_CONFIG_106**：節流設定：無效負載
* **THROTTLING_CONFIG_DELETE_FORBIDDEN_ERROR: 1456**，「無法刪除已部署的節流設定。 請先取消部署再刪除」
* **THROTTLING_CONFIG_DELETE_ERROR: 1457**，「無法刪除節流設定：發生意外錯誤」
* **THROTTLING_CONFIG_DEPLOY_ERROR: 1458**，「無法部署節流設定：發生意外錯誤」
* **THROTTLING_CONFIG_UNDEPLOY_ERROR: 1459**，「無法取消部署節流設定：發生意外錯誤」
* **THROTTLING_CONFIG_GET_ERROR: 1460**，「無法取得節流設定：發生意外錯誤」
* **THROTTLING_CONFIG_UPDATE_NOT_ACTIVE_ERROR: 1461**，「無法更新節流設定：執行時版本未處於活動狀態」
* **THROTTLING_CONFIG_UPDATE_ERROR: 1462**，「無法更新節流設定：發生意外錯誤」 
* **THROTTLING_CONFIG_NON_PROD_SANDBOX_ERROR: 1463**，「禁止對節流設定執行操作：非生產沙箱」 
* **THROTTLING_CONFIG_CREATE_ERROR: 1464**，「無法建立節流設定：發生意外錯誤」
* **THROTTLING_CONFIG_CREATE_LIMIT_ERROR: 1465**，「無法建立節流設定：每個組織僅允許一個設定」
* **THROTTLING_CONFIG_ALREADY_DEPLOYED_ERROR: 14466**，「無法部署節流設定：已部署」
* **THROTTLING_CONFIG_NOT_FOUND_ERROR: 14467**，「未找到節流設定」
* **THROTTLING_CONFIG_NOT_DEPLOYED_ERROR: 14468**，「無法取消部署節流設定：尚未部署」

**錯誤範例**

當嘗試在非生產沙箱上建立設定時：

```json
{
    "status": 400,
    "error": "{\"code\":1463,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Operation not allowed on throttling config: non prod sandbox\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:384\",\"schema\":\"throttlingConfigs$ui-tests\"}",
    "requestId": "5sgnAYXs8mpswwjAFEIaAU2faQYbtyHc"
}
```

如果給定的沙箱不存在：

```json
{
    "status": 500,
    "error": "{\"code\":4000,\"family\":\"INTERNAL_ERROR\",\"message\":\"INTERNAL ERROR\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.common.exceptions.ApiErrorException:43\"}",
    "requestId": "04ZJ4e5ki4bYs3lfO17a7hovRGewjvdK"
}
```

當嘗試建立其他設定時：

```json
{
    "status": 400,
    "error": "{\"code\":1465,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Can't create throttling config: only one config allowed per org\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:108\",\"schema\":\"throttlingConfigs$prod\"}",
    "requestId": "A7ezT8JhOQT4WIAf1Fv7K2wCDA8281qM"
}
```

## 在執行階段層級設定生命週期 {#config}

當取消部署設定時，會在執行階段層級將其標示為非活動狀態，且 24 小時內會繼續處理擱置事件。 然後，在執行階段服務將其刪除。

取消部署設定後，可以更新和重新部署設定。 這將建立新的執行階段設定，將在即將執行的動作中考慮該設定。

當更新已部署的設定時，會立即考慮新值。自動調整基礎系統資源。 與取消部署然後重新部署設定相比，這是最佳選擇。

## 回應範例 {#responses}

**建立 - POST**

```json
{
    "canDeploy": {
        "validationStatus": "ok"
    },
    "createdElement": {
        "name": "throttling-config-external",
        "description": "example of throttling config for an external endpoint",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "PUT",
            "POST"
        ],
        "maxThroughput": 4000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T10:48:16.099647Z"
        },
        "state": "created",
        "authoringFormatVersion": "1.0"
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "created"
}
```

**更新 - PUT**

```json
{
    "updatedElement": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "updated",
    "canDeploy": {
        "validationStatus": "ok"
    }
}
```

**讀取 (更新後) - GET**

```json
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    }
}
```

**讀取 (部署後) - GET**

```json
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "authoringFormatVersion": "1.0",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "version": "1.0",
        "state": "deployed",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z",
            "lastDeployedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastDeployedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastDeployedAt": "2023-03-22T11:46:07.532648Z"
        },
        "hasBeenDeployed": true
    }
}
```

## 使用案例 {#uc}

本節列出在[!DNL Journey Optimizer]中管理節流設定的主要使用案例，以及實施使用案例所需的相關API命令。

每個API命令的詳細資訊可在[API說明和Postman集合](#description)中取得。

+++建立及部署新的節流設定

要使用的API呼叫：

1. **`list`** — 擷取現有設定。
1. **`create`** — 建立新的組態。
1. **`candeploy`** — 檢查組態是否可以部署。
1. **`deploy`** — 部署設定。

+++

+++更新及部署節流設定（尚未部署）

要使用的API呼叫：

1. **`list`** — 擷取現有設定。
1. **`get`** — 擷取特定設定的詳細資料。
1. **`update`** — 修改設定。
1. **`candeploy`** — 檢查部署資格。
1. **`deploy`** — 部署設定。

+++

+++取消部署和刪除已部署的節流設定

要使用的API呼叫：

1. **`list`** — 擷取現有設定。
1. **`undeploy`** — 取消部署設定。
1. **`delete`** — 移除設定。

+++

+++刪除已部署的節流設定

您只能在一個API呼叫中使用`forceDelete`引數來取消部署及刪除組態。

要使用的API呼叫：

1. **`list`** — 擷取現有設定。
1. **`delete`（含`forceDelete`引數）** — 在單一步驟中強制刪除已部署的組態。

+++

+++更新已部署的節流設定

>[!NOTE]
>
>更新前不需要取消部署設定

要使用的API呼叫：

1. **`list`** — 擷取現有設定。
1. **`get`** — 擷取特定設定的詳細資料。
1. **`update`** — 修改設定。

+++
