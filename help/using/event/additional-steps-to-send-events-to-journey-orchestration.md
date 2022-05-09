---
title: 將事件發送到行程的其他步驟
description: 瞭解將事件發送到行程的其他步驟
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 5%

---

# 傳送事件的其他步驟 {#additional-steps-to-send-events}

配置要發送到的事件 **[!UICONTROL Streaming Ingestion APIs]** 和 [!DNL Journey Optimizer]，您需要執行以下步驟：

1. 從Adobe Experience PlatformAPI獲取入口URL。 瞭解詳情 [流式接收API概述](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target=&quot;_blank&quot;}。
1. 從中的負載預覽複製負載 **[!UICONTROL Event]** 的子菜單。 在[本頁](../event/about-creating.md#define-the-payload-fields)中瞭解更多。

然後，您需要配置資料系統，該資料系統使用您複製的負載將事件推送到Streaming Ingestion API:

1. 設定對流接收API URL的POSTAPI調用（稱為入口）。
1. 使用從中複製的負載 [!DNL Journey Optimizer] API調用的正文（「資料部分」）中。 有關示例，請參閱下面
1. 確定從何處獲取負載中存在的所有變數。 示例：如果事件應傳遞地址，則貼上的負載將顯示「地址」：&quot;字串&quot;。 &quot;string&quot;應替換為自動填充正確值的變數，即要向其發送消息的人員的電子郵件。 請注意，在負載預覽中， **[!UICONTROL Header]** 部分，我們將自動填充許多值以便您工作。
1. 選擇「application/json」作為正文類型。
1. 使用鍵「x-gw-ims-org-id」在題頭中傳遞您的組織ID。 對於該值，請使用您的組織ID(「XXX@AdobeOrg」)。

以下是流接收API事件的示例：

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

為便於識別貼上「data」部件的位置，可以使用JSON可視化工具，如 [JSON格式化程式](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}。

要排除流接收API故障，請參閱 [Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}。
