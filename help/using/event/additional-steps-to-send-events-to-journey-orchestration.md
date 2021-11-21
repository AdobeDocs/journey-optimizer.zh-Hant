---
title: 將事件傳送至歷程的其他步驟
description: 了解將事件傳送至歷程的其他步驟
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 5%

---

# 傳送事件的其他步驟 {#concept_xrz_n1q_y2b}

配置要發送到的事件 **[!UICONTROL Streaming Ingestion APIs]** 和 [!DNL Journey Optimizer]，您需要遵循下列步驟：

1. 從Adobe Experience Platform API取得入口URL。 深入了解 [串流獲取API概觀](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target=&quot;_blank&quot;}。
1. 從 **[!UICONTROL Event]** 功能表。 在[本頁](../event/about-creating.md#define-the-payload-fields)中瞭解更多。

然後，您需要設定資料系統，使用您複製的裝載將事件推送至串流獲取API:

1. 設定串流獲取API URL的POSTAPI呼叫（稱為入口）。
1. 使用您從 [!DNL Journey Optimizer] (位於對串流獲取API呼叫的內文（「資料區段」）中。 如需範例，請參閱下方
1. 決定要在何處取得有效負載中所有變數。 範例：如果事件應傳達地址，則貼上的裝載會顯示「地址」：&quot;string&quot;。 「string」應取代為變數，變數會自動填入正確值（要傳送訊息之人員的電子郵件）。 請注意，在裝載預覽中， **[!UICONTROL Header]** 區段中，我們會自動填入許多值，以方便您工作。
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

為方便您識別「資料」部件貼上位置，您可以使用JSON視覺化工具，例如 [JSON格式](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}。

若要疑難排解串流獲取API，請參閱 [Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}。
