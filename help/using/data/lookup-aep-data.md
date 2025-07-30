---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Experience Platform資料(Beta)
description: 瞭解如何在 [!DNL Journey Optimizer] 決策和個人化功能中使用Adobe Experience Platform資料集。
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: bd1274a5547f4ea835fc258f280c1efc667b6780
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 6%

---

# 使用 Adobe Experience Platform 資料 {#aep-data}

>[!CONTEXTUALHELP]
>id="lookup-aep-data"
>title="啟用供查詢使用"
>abstract="啟用供查詢使用"

>[!AVAILABILITY]
>
>此功能目前以公開測試版的形式提供給所有客戶。
>
>若要使用此功能，您必須先接受組織的Beta版條款。

Journey Optimizer可讓您在[!DNL Journey Optimizer]中運用Adobe Experience Platform的資料。 若要這麼做，必須首先透過API呼叫啟用查詢個人化所需的資料集，如下所述。 完成後，您可以將其資料用於[!DNL Journey Optimizer]個人化和決策功能。

## Beta限制和指引 {#guidelines}

開始之前，請檢閱下列限制和准則：

* **資料集大小**&#x200B;在生產資料集中限製為5GB，在開發沙箱資料集中限製為1GB
* **在任何時候，每個組織最多可以啟用50個資料集**&#x200B;以供查閱。
* **記錄數**&#x200B;在生產資料集中限製為5M，在開發沙箱資料集中限製為1M。
* **資料使用標籤和強制執行**&#x200B;目前未針對啟用查閱的資料集強制執行。
* **啟用查閱及用於個人化的資料集不會受到刪除保護**。 您可以自行追蹤用於個人化的資料集，以確保不會刪除或移除這些資料集。

## 啟用資料集以進行資料查詢 {#enable}

為了將資料集中的資料用於個人化，您需要使用API呼叫來擷取其狀態並啟用查詢服務。

### 先決條件 {#prerequisites-enable}

* 依照[本檔案](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)中詳述的指示，設定您的環境以傳送API命令。
* 開發人員專案必須將Adobe Journey Optimizer和Adobe Experience Platform API新增至其專案。

  ![](assets/aep-data-api.png)

* 您角色中必須有管理資料集許可權。
* 資料集所依據的結構描述必須包含可作為查詢金鑰的&#x200B;**主要身分**。

### API呼叫結構 {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

其中：

* **URL**&#x200B;是`https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* **資料集識別碼**&#x200B;是您要啟用的資料集。
* **動作**&#x200B;為啟用或停用。
* **存取權杖**&#x200B;可從開發人員主控台擷取。
* 可從開發人員主控台擷取&#x200B;**API金鑰**。
* **IMS組織ID**&#x200B;是您的Adobe組織。
* **沙箱名稱**&#x200B;是資料集所在的沙箱名稱（例如prod、dev等）。

>[!NOTE]
>
>如果您在嘗試使用API呼叫啟用資料集時遇到以下錯誤，請嘗試從開發人員控制檯專案中移除Adobe Journey Optimizer API，然後重新新增它們。
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

一旦資料集啟用使用API呼叫進行查詢後，您就可以將其資料與[!DNL Journey Optimizer]個人化和決策功能搭配使用。

* [使用 Adobe Experience Platform 資料進行個人化](../personalization/aep-data-perso.md)
* [使用 Adobe Experience Platform 資料進行決策](../experience-decisioning/aep-data-exd.md)
