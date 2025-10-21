---
solution: Journey Optimizer
product: journey optimizer
title: 傳送事件至歷程的其他步驟
description: 瞭解將事件傳送到歷程的其他步驟
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: 步驟，設定，歷程，事件，串流， API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 3%

---

# 傳送事件的其他步驟 {#additional-steps-to-send-events}

若要設定要傳送至&#x200B;**[!UICONTROL 串流擷取API]**&#x200B;並用於[!DNL Journey Optimizer]的事件，您必須遵循下列步驟：

1. 從Adobe Experience Platform API取得入口URL。 深入瞭解[串流擷取API概觀](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target="_blank"}。
1. 從&#x200B;**[!UICONTROL Event]**&#x200B;功能表的裝載預覽複製裝載。 請在[此頁面](../event/about-creating.md#define-the-payload-fields)了解更多。

然後，您需要設定資料系統，使用您複製的裝載將事件推送至串流獲取API：

1. 設定對串流獲取API URL的POST API呼叫（稱為入口）。
1. 使用您從[!DNL Journey Optimizer]複製的裝載，該裝載位於串流獲取API之API呼叫的內文（「資料區段」）中。 如需範例，請參閱下文
1. 決定從何處取得裝載中出現的所有變數。 範例：如果事件應該要傳達位址，貼上的裝載將會顯示「address」：「string」。 「string」應該取代為會自動填入正確值的變數，也就是傳送訊息對象的電子郵件。 請注意，在裝載預覽的&#x200B;**[!UICONTROL 標題]**&#x200B;區段中，我們會自動填入許多預期有助於您工作的值。
1. 選取「application/json」作為內文型別。
1. 使用索引鍵「x-gw-ims-org-id」在標題中傳遞您的組織ID。 對於值，請使用您的組織ID (&quot;XXX@AdobeOrg&quot;)。

以下是串流擷取API事件的範例：

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
            "timestamp": "2023-05-29T00:00:00.000Z",
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

若要方便識別貼上「資料」部分的地方，您可以使用JSON視覺化工具，例如[JSON格式子](https://jsonformatter.curiousconcept.com){target="_blank"}。

若要疑難排解串流擷取API，請參閱[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}。
