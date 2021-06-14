---
title: 將事件傳送至歷程的其他步驟
description: 了解將事件傳送至歷程的其他步驟
feature: 事件
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 4%

---

# 傳送事件的其他步驟 {#concept_xrz_n1q_y2b}

![](../assets/do-not-localize/badge.png)

要配置要發送到&#x200B;**[!UICONTROL Streaming Ingestion APIs]**&#x200B;以及要在[!DNL Journey Optimizer]中使用的事件，需要執行以下步驟：

1. 從Adobe Experience Platform API取得入口URL。 深入了解[串流獲取API概述](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html)。
1. 從&#x200B;**[!UICONTROL Event]**&#x200B;功能表中的有效負載預覽複製有效負載。 在[本頁](../event/about-creating.md#define-the-payload-fields)中瞭解更多。

然後，您需要設定資料系統，使用您複製的裝載將事件推送至串流獲取API:

1. 設定串流獲取API URL的POSTAPI呼叫（稱為入口）。
1. 使用您從API呼叫內文(「data section」)中[!DNL Journey Optimizer]複製的裝載，來串流獲取API。 如需範例，請參閱下方
1. 決定要在何處取得有效負載中所有變數。 範例：如果事件應傳達地址，則貼上的裝載會顯示「地址」：&quot;string&quot;。 「string」應取代為變數，變數會自動填入正確值（要傳送訊息之人員的電子郵件）。 請注意，在有效負載預覽的&#x200B;**[!UICONTROL Header]**&#x200B;區段中，我們會自動填入許多預期有助於您工作的值。
1. 選取「application/json」作為內文類型。
1. 使用索引鍵「x-gw-ims-org-id」在標題中傳遞您的IMS組織ID。 若為值，請使用您的IMS組織ID(「XXX@AdobeOrg」)。

以下是串流獲取API事件的範例：

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2018-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

為方便您識別貼上「data」部件的位置，您可以使用JSON視覺化工具，例如[https://jsonformatter.curiousconcept.com](https://jsonformatter.curiousconcept.com)

若要疑難排解串流獲取API，請參閱此[page](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html)。
