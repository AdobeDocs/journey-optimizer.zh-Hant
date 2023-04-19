---
solution: Journey Optimizer
product: journey optimizer
title: 設定 API 上限
description: 了解如何使用上限設定API
role: User
level: Beginner
keywords: 外部， API，優化程式，限定
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 30%

---

# 使用上限設定API {#work}

上限API可協助您建立、設定及監控上限設定。

本節提供如何使用API的全域資訊。 如需詳細的API說明，請參閱 [Adobe Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/).

## 設定API說明上限

| 方法 | 路徑 | 說明 |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | 獲取端點限定配置清單 |
| [!DNL POST] | /endpointConfigs | 建立端點限定配置 |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | 部署端點限定配置 |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | 取消部署端點限定配置 |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | 檢查是否可部署端點限定配置 |
| [!DNL PUT] | /endpointConfigs/`{uid}` | 更新端點限定配置 |
| [!DNL GET] | /endpointConfigs/`{uid}` | 擷取端點上限設定 |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | 刪除引入點限定配置 |

建立或更新設定時，會自動執行檢查，以保證有效負載的語法和完整性。
如果發生某些問題，操作會傳回警告或錯誤，以協助您修正設定。

## 端點設定

端點設定的基本結構如下：

```
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

### 範例：

```
`{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "maxHttpConnections": 30000,
      "rating": {
        "maxCallsCount": 5000,
        "periodInMs": 1000
      }
    }
  },
  "orgId": "<IMS Org Id>"
}
```

## 警告和錯誤

當 **canDeploy** 方法呼叫時，程式會驗證設定並傳回以其唯一ID識別的驗證狀態，其中一項為：

```
"ok" or "error"
```

潛在錯誤為：

* **ERR_ENDPOINTCONFIG_100**:限定配置：遺失或無效的url
* **ERR_ENDPOINTCONFIG_101**:限定配置：格式錯誤的url
* **ERR_ENDPOINTCONFIG_102**:限定配置：格式錯誤的url:主機中不允許在url中使用通配符
* **ERR_ENDPOINTCONFIG_103**:限定配置：缺少HTTP方法
* **ERR_ENDPOINTCONFIG_104**:限定配置：未定義呼叫評級
* **ERR_ENDPOINTCONFIG_107**:限定配置：最大呼叫計數無效(maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**:限定配置：最大呼叫計數無效(periodInMs)
* **ERR_ENDPOINTCONFIG_111**:限定配置：無法建立端點配置：有效負載
* **ERR_ENDPOINTCONFIG_112**:限定配置：無法建立端點配置：應為JSON裝載
* **ERR_AUTHORING_ENDPOINTCONFIG_1**:無效的服務名稱 `<!--<given value>-->`:必須是「dataSource」或「action」

潛在警告是：

**ERR_ENDPOINTCONFIG_106**:限定配置：未定義的最大HTTP連接數：預設不限制

## 使用案例

在本節中，您會找到可在中執行以管理上限設定的五個主要使用案例 [!DNL Journey Optimizer].

為協助您進行測試和設定，可在[此處](https://raw.githubusercontent.com/AdobeDocs/JourneyAPI/master/postman-collections/Journey-Orchestration_Capping-API_postman-collection.json)取得 Postman 集合。

此 Postman 集合已設定為共用透過 __[Adobe I/O 主控台的整合](https://console.adobe.io/integrations)產生的 Postman 變數集合 > 試用 > 下載 Postman__，會產生包含選取整合值的 Postman 環境檔案。

一旦下載並上傳至 Postman，您需要新增三個變數：`{JO_HOST}`、`{BASE_PATH}`以及`{SANDBOX_NAME}`。
* `{JO_HOST}` : [!DNL Journey Optimizer]閘道 URL
* `{BASE_PATH}`：API 的進入點。 
* `{SANDBOX_NAME}`：標題 **x-sandbox-name** (例如，&#39;prod&#39;)，此名稱對應於將進行 API 操作的沙箱名稱。如需詳細資訊，請參閱[沙箱概觀](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hant)。

您將在下節找到用於執行使用案例的 Rest API 呼叫排序清單。

使用案例n°1: **建立和部署新的上限設定**

1. list
1. create
1. candeploy
1. deploy

使用案例n°2: **更新並部署尚未部署的上限設定**

1. list
1. get
1. update
1. candeploy
1. deploy

用例n°3: **取消部署和刪除已部署的上限配置**

1. list
1. undeploy
1. delete

使用案例n°4: **刪除已部署的上限配置。**

在僅一個 API 呼叫，您可以使用 forceDelete 參數來取消部署和刪除設定。
1. list
1. 刪除，使用 forceDelete 參數

使用案例n°5: **更新已部署的上限配置**

1. list
1. get
1. update
1. undeploy
1. candeploy
1. deploy
