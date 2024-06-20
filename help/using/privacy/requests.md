---
solution: Journey Optimizer
product: journey optimizer
title: 隱私權請求
description: 了解有關隱私權請求和 Privacy Service 的更多資訊。
feature: Privacy
role: User
level: Intermediate
exl-id: 19ec3410-761e-4a9c-a277-f105fc446d7a
source-git-commit: 41717213cb75185476f054bd076e67f942be0f1c
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 23%

---

# 隱私權請求 {#track-changes}

Adobe Experience Platform **Privacy Service** 提供 RESTful API 和使用者介面，幫助您管理客戶資料請求。 藉由 Privacy Service，您可以提交存取和刪除 Adobe Experience Cloud 應用程式中的個人客戶資料請求，協助促進法律資訊和組織隱私法規的自動合規性。

可以從&#x200B;**[!UICONTROL 請求]**&#x200B;功能表建立並管理隱私權請求 。

![](assets/requests.png)

有關 Privacy Service 以及如何建立和管理隱私權請求的詳細資訊，請參閱 Adobe Experience Platform 文件：

* [Privacy Service 概述](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant)
* [管理 Privacy Service UI 中的隱私作業](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hant)



## 管理您可傳送至Adobe Journey Optimizer的個別資料隱私權請求 {#data-privacy-requests}

您可以透過兩種方式提交存取和刪除Adobe Journey Optimizer中消費者資料的個別請求：

* 透過 **PRIVACY SERVICEUI**. 請參閱檔案 [此處](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/ui/user-guide#_blank).
* 透過 **PRIVACY SERVICE API**. 請參閱檔案 [此處](https://developer.adobe.com/experience-platform-apis/references/privacy-service/#_blank) 和API資訊 [此處](https://developer.adobe.com/experience-platform-apis/#_blank).

Privacy Service支援兩種請求： **資料存取** 和 **資料刪除**.

>[!NOTE]
>
>本指南僅涵蓋如何向Adobe Journey Optimizer提出隱私權請求。 如果您也計畫針對Platform Data Lake提出隱私權請求，請參閱本節 [指南](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/privacy) 除了本教學課程以外。 如需即時客戶設定檔，請參閱此 [指南](https://experienceleague.adobe.com/en/docs/experience-platform/profile/privacy) 若為Identity服務，請參閱此 [指南](https://experienceleague.adobe.com/en/docs/experience-platform/identity/privacy). 對於刪除和存取請求，您需要呼叫這些個別系統，以確保每個系統都能處理請求。 向Adobe Journey Optimizer提出隱私權請求並不會移除所有這些系統中的資料。

的 **存取要求**，從UI指定「Adobe Journey Optimizer」 （或「CJM」作為API中的產品程式碼）。

的 **刪除請求**，除了「Adobe Journey Optimizer」請求之外，您還必須向三個上游服務提交刪除請求，以防止Journey Optimizer重新插入已刪除的資料。 如果未指定這些上游服務，「Adobe Journey Optimizer」請求將維持在「處理」狀態，直到建立上游服務的刪除請求為止。

三種上游服務為：

* 設定檔（產品代碼：「profileService」）
* AEP資料湖（產品代碼：「AdobeCloudPlatform」）
* 身分（產品代碼：&quot;identity&quot;）

## 如何建立存取與刪除請求

### 先決條件

若要請求存取和刪除Adobe Journey Optimizer的資料，您必須擁有：

* IMS組織ID
* 您要對其採取動作之人員的身分識別碼以及對應的名稱空間。如需Adobe Journey Optimizer和Experience Platform中身分名稱空間的詳細資訊，請參閱 [身分名稱空間總覽](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces).

### Adobe Journey Optimizer中用於API請求的必填欄位值

```json
"companyContexts":
    "namespace": imsOrgID
    "value": <Your IMS Org ID Value>

"users":
    "action": either access or delete

    "userIDs":
        "namespace": e.g. email, aaid, ecid, etc.
        "type": standard
        "value": <Data Subject's Identity Identifier>

"include":
    CJM (which is the Adobe product code for Adobe Journey Optimizer)
    profileService (product code for Profile)
    AdobeCloudPlatform (product code for AEP Data Lake)
    identity (product code for Identity)

"regulation":
    gdpr, ccpa, pdpa, lgpd_bra, or nzpa_nzl (which is the privacy regulation that applies to the request)
```


### GDPR存取請求範例：

從UI：

![](assets/accessrequest.png)

透過API：

```json
// JSON Request
{
   "companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"745F37C35E4B776E0A49421B@AdobeOrg"
      }
   ],
   "users":[
      {
         "action":[
            "access"
         ],
         "userIDs":[
            {
               "namespace":"ecid",
               "value":"38400000-8cf0-11bd-b23e-10b96e40000d",
               "type":"standard"
            },
            {
               "namespace":"email",
               "value":"johndoe4@gmail.com",
               "type":"standard"
            }
         ]
      }
   ],
   "include":[
      "CJM"
   ],
   "regulation":"gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "access"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```

### GDPR刪除請求範例：

從UI：

![](assets/deleterequest.png)

透過API：

```json
// JSON Request
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "745F37C35E4B776E0A49421B@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": [
          "delete"
      ],
      "userIDs": [
        {
          "namespace": "ecid",
          "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
          "type": "standard"
        },
                {
          "namespace": "email",
          "value": "johndoe4@gmail.com",
          "type": "standard"
        }
      ]
    }
  ],
  "include": [
    "CJM", "profileService", "AdobeCloudPlatform", "identity"
  ],
  "regulation": "gdpr"
}
```

```json
// JSON Response
{
    "requestId": "17163122360480365RX-705",
    "totalRecords": 1,
    "jobs": [
        {
            "jobId": "e709b1f4-1796-11ef-b422-eddd0aebc40d",
            "customer": {
                "user": {
                    "key": "John Doe",
                    "action": [
                        "delete"
                    ],
                    "userIDs": [
                        {
                            "namespace": "ecid",
                            "value": "38400000-8cf0-11bd-b23e-10b96e40000d",
                            "type": "standard",
                            "namespaceId": 4,
                            "isDeletedClientSide": false
                        },
                        {
                            "namespace": "email",
                            "value": "johndoe4@gmail.com",
                            "type": "standard",
                            "namespaceId": 6,
                            "isDeletedClientSide": false
                        }
                    ]
                }
            }
        }
    ]
}
```
