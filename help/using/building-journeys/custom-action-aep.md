---
solution: Journey Optimizer
product: journey optimizer
title: 使用自訂動作在AEP中寫入歷程事件
description: 使用自訂動作在AEP中寫入歷程事件
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer
level: Experienced
exl-id: 890a194f-f54d-4230-863a-fb2b924d716a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/TbX3usHKfEM6WQPjFRjo2jCSb78rcbYEWWmV0tpGdj4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b856530c-d60b-42d8-a19d-df2dfd7fe62aid: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1085
ht-degree: 1%

---

# 使用自訂動作在 Experience Platform 中編寫歷程事件 {#custom-action-aep}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用自訂動作和已驗證的API呼叫，將自訂歷程事件從歷程寫入Adobe Experience Platform。

>[!ENDSHADEBOX]

此使用案例說明如何使用自訂動作和已驗證的呼叫，將自訂事件從歷程寫入[!DNL Adobe Experience Platform]。

## 設定開發人員專案 {#custom-action-aep-IO}

1. 在Adobe Developer Console中，按一下&#x200B;**專案**&#x200B;並開啟您的IO專案。

1. 在&#x200B;**認證**&#x200B;區段中，按一下&#x200B;**OAuth伺服器對伺服器**。

   ![具有動作型別下拉式清單的自訂動作設定畫面](assets/custom-action-aep-1.png)

1. 按一下&#x200B;**檢視cURL命令**。

   ![[!DNL Adobe Experience Platform]動作型別選擇](assets/custom-action-aep-2.png)

1. 複製cURL命令並儲存client_id、client_secret、grant_type和scope。

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

>[!CAUTION]
>
>在Adobe Developer Console上建立專案後，請務必授予具有正確許可權的開發人員和API存取控制。 在[[!DNL Adobe Experience Platform] 檔案](https://experienceleague.adobe.com/en/docs/experience-platform/landing/platform-apis/api-authentication#grant-developer-and-api-access-control){target="_blank"}中進一步瞭解

## 使用HTTP API入口設定來源

1. 在[!DNL Adobe Experience Platform]中建立端點以寫入歷程中的資料。

1. 在[!DNL Adobe Experience Platform]中，按一下左側功能表中&#x200B;**連線**&#x200B;下的&#x200B;**來源**。 在&#x200B;**HTTP API**&#x200B;下，按一下&#x200B;**新增資料**。

   [!DNL Adobe Experience Platform]](assets/custom-action-aep-3.png)的![沙箱選取下拉式清單

1. 選取&#x200B;**新帳戶**&#x200B;並啟用驗證。 選取&#x200B;**連線至Source**。

   ![串流資料的資料集選擇介面](assets/custom-action-aep-4.png)

1. 選取&#x200B;**下一步**&#x200B;以及您要寫入資料的資料集。 按一下&#x200B;**下一步**&#x200B;和&#x200B;**完成**。

   ![XDM結構描述欄位對應到動作引數](assets/custom-action-aep-5.png)

1. 開啟新建立的資料流。 複製結構描述承載並將其儲存在記事本中。

```
{
"header": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
},
"imsOrgId": "<org_id>",
"datasetId": "<dataset_id>",
"source": {
"name": "Custom Journey Events"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
}
},
"xdmEntity": {
"_id": "test1",
"<your_org>": {
"journeyVersionId": "",
"nodeId": "", "customer_Id":""
},
"eventMergeId": "",
"eventType": "",
"producedBy": "self",
"timestamp": "2018-11-12T20:20:39+00:00"
}
}
}
```

## 設定自訂動作 {#custom-action-config}

自訂動作設定在[此頁面](../action/about-custom-action-configuration.md)上詳細說明。

在此範例中，請遵循下列步驟：

1. 開啟[!DNL Adobe Journey Optimizer]，然後按一下左側功能表中&#x200B;**管理**&#x200B;下的&#x200B;**組態**。 在&#x200B;**動作**&#x200B;下，按一下&#x200B;**管理**，然後按一下&#x200B;**建立動作**。

1. 設定URL並選取Post方法。

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. 請確定已設定標題(Content-Type、Charset、sandbox-name)。

   ![歷程畫布中的自訂動作（使用設定窗格）](assets/custom-action-aep-7bis.png)

### 設定驗證 {#custom-action-aep-authentication}

1. 選取&#x200B;**Type**&#x200B;做為&#x200B;**Custom**，並包含下列承載。

1. 貼上client_secret、client_id、scope和grant_type （來自以前使用的IO專案裝載）。

   ```
   {
   "type": "customAuthorization",
   "authorizationType": "Bearer",
   "endpoint": "https://ims-na1.adobelogin.com/ims/token/v3",
   "method": "POST",
   "headers": {},
   "body": {
   "bodyType": "form",
   "bodyParams": {
   "grant_type": "client_credentials",
   "client_secret": "********",
   "client_id": "<client_id>",
   "scope": "openid,AdobeID,read_organizations,additional_info.projectedProductContext,session"
   }
   },
   "tokenInResponse": "json://access_token",
   "cacheDuration": {
   "duration": 28000,
   "timeUnit": "seconds"
   }
   }
   ```

1. 使用&#x200B;**按一下以測試驗證**&#x200B;按鈕以測試連線。

   ![使用運算式編輯器的引數對應介面](assets/custom-action-aep-8.png)

### 設定裝載 {#custom-action-aep-payload}

1. 在&#x200B;**Request**&#x200B;與&#x200B;**Response**&#x200B;欄位中，貼上先前使用之來源連線的裝載。

   ```
   {
   "xdmMeta": {
   "schemaRef": {
   "id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
   "contentType": "application/vnd.adobe.xed-full+json;version=1.0"
   }
   },
   "xdmEntity": {
   "_id": "/uri-reference",
   "<your_org>": {
   "journeyVersionId": "Sample value",
   "nodeId": "Sample value",
   "customer_Id":""
   },
   "eventMergeId": "Sample value",
   "eventType": "advertising.completes,
   "producedBy": "self",
   "timestamp": "2018-11-12T20:20:39+00:00"
   }
   }
   ```

1. 將欄位組態從&#x200B;**常數**&#x200B;變更為&#x200B;**變數**，以動態方式填入欄位。

1. 儲存自訂動作。

## 歷程

1. 最後，在歷程中使用此自訂動作來撰寫自訂歷程事件。

1. 根據您的使用案例填入歷程版本ID、節點ID、節點名稱和其他屬性。

   複雜欄位對應的![進階模式編輯器](assets/custom-action-aep-9.png)

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

- **TL；DR：**&#x200B;此使用案例說明如何在Journey Optimizer中設定自訂動作，以使用HTTP API入口和OAuth伺服器對伺服器驗證的呼叫將歷程事件資料寫入Adobe Experience Platform。

**意圖：**
- 設定具有OAuth伺服器對伺服器憑證的Adobe Developer Console IO專案，以進行AEP API驗證
- 在Adobe Experience Platform中建立HTTP API入口來源，以接收串流歷程事件資料
- 使用正確的URL、標題和自訂持有人權杖驗證，在Journey Optimizer中設定自訂動作
- 將歷程欄位（歷程版本ID、節點ID、客戶ID）動態對應為自訂動作裝載中的變數
- 在歷程中使用自訂動作，將自訂事件寫入AEP資料集

**字彙表：**
- **HTTP API入口**： Adobe Experience Platform來源聯結器會建立串流端點，以透過HTTP POST要求擷取資料&#x200B;*（產品專用）*
- **OAuth伺服器對伺服器**： Adobe Developer Console中的驗證認證型別會產生伺服器對伺服器API呼叫的持有者權杖，而不需要使用者互動&#x200B;*（產品特定）*
- **自訂授權**： Journey Optimizer自訂動作驗證型別，它會從指定的端點擷取Bearer權杖，並在設定的期間&#x200B;*（產品特定）*&#x200B;快取該權杖
- **XDM實體**：符合體驗資料模型結構描述的資料裝載結構，在透過HTTP API入口&#x200B;*（產品特定）*&#x200B;將事件寫入AEP時作為內文
- **cacheDuration**：自訂授權組態中的權杖快取設定，可控制要求的新Bearer權杖重複使用時間長度&#x200B;*（產品特定）*

**護欄：**
- 建立Adobe Developer Console專案後，必須先明確授予開發人員和API存取控制許可權，才能使用認證
- HTTP API入口來源必須在啟用驗證的情況下建立；必須複製並儲存連線端點URL和結構描述裝載，才能用於自訂動作設定
- 自訂動作標頭必須包含Content-Type、Charset和sandbox-name
- 在執行階段要動態填入的欄位，必須在自訂動作裝載設定中從常數變更為變數

**術語：**
- 正式名稱：自訂動作 — 縮寫：無 — 變體：自訂動作組態、Journey Optimizer自訂動作
- 正式名稱：Adobe Experience Platform — 縮寫：AEP — 變體：Experience Platform、Platform
- 同義字： &quot;HTTP API Inlet&quot; = &quot;streaming endpoint&quot; = &quot;DCS collection endpoint&quot;
- 請勿混淆：「OAuth伺服器對伺服器」≠「OAuth使用者驗證」（伺服器對伺服器不需要使用者登入，而是使用使用者端認證）

**常見問題集：**
- **問：從Journey Optimizer自訂動作呼叫AEP HTTP API Inlet時，使用什麼型別的驗證？**  — 使用從Adobe IMS權杖端點擷取的OAuth伺服器對伺服器使用者端憑證進行自訂持有人權杖驗證。
- **問：我可以在哪裡找到client_id、client_secret、grant_type和範圍值？**  — 在Adobe Developer Console IO專案的「OAuth伺服器對伺服器認證」區段中，按一下「檢視cURL命令」。
- **問：如何在承載中讓歷程特定欄位（例如journeyVersionId、nodeId）成為動態欄位？**  — 在自訂動作裝載設定中，將其欄位設定從常數變更為變數，以便在執行階段從歷程內容填入。
- **問：Adobe Developer Console專案需要哪些許可權？**  — 開發人員和API存取控制必須在專案建立後授予正確的許可權，如AEP API驗證檔案所述。
- **問：驗證承載中cacheDuration設定的用途為何？**  — 控制在自訂動作要求新權杖之前，擷取的Bearer權杖要快取和重新使用多久（範例中為28,000秒）。

+++
