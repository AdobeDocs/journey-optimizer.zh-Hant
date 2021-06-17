---
title: 發佈和修改訊息
description: 了解如何發佈和更新訊息
snippet: y
feature: Journeys
topic: 內容管理
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 4%

---

# 發佈訊息{#publish-manage-messages}

## 發佈訊息{#publish-message}

建立訊息後，您就可以發佈訊息，以便供執行。

>[!CAUTION]
>
>發佈前，請檢查並解決警報。 [了解更多](alerts.md)。

![](assets/publish-message.png)

發佈訊息後，訊息會新增至狀態為&#x200B;**[!UICONTROL Published]**&#x200B;的訊息清單。

現在已可由一或多個[journeys](building-journeys/journey.md)觸發。

## 更新只讀消息{#modify-message}

發佈後，訊息會處於唯讀模式。 您仍可以建立該訊息的新草稿來更新訊息。

這可讓您更新內容或修正問題，例如，不需重新發佈使用訊息的整個歷程。

>[!NOTE]
>
>草稿版本仍可發佈且處於作用中狀態時編輯。

若要更新已發佈的訊息：

1. 從訊息清單中，選取您的訊息以開啟它。

1. 按一下「**[!UICONTROL Modify]**」。

   ![](assets/message-modify.png)

1. 確認您的選取。訊息的草稿版本隨即建立。

   ![](assets/message-modify-v2.png)

1. 編輯內容或視需要變更設定。
1. 按一下「**[!UICONTROL Publish]**」。此動作會發佈將用於下次執行之訊息的新版本。

新版本發佈後，下次API呼叫時，就會產生新訊息執行。 下一個傳入的設定檔將接收新版本。

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version.-->
