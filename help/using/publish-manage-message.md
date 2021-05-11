---
title: 發佈並修改訊息
description: 瞭解如何發佈和更新訊息
snippet: y
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# 發佈您的訊息{#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## 發佈訊息{#publish-message}

在您的訊息建立後，您可以發佈訊息，讓訊息可供執行。

>[!CAUTION]
>
>發佈前，請檢查並解決警報。 [了解更多](alerts.md)。

![](assets/publish-message.png)

發佈消息後，消息將添加到狀態為&#x200B;**[!UICONTROL Published]**&#x200B;的消息清單中。

現在可由一或多個[reyerlys](building-journeys/journey.md)觸發。

## 更新唯讀消息{#modify-message}

發佈後，訊息會處於唯讀模式。 您仍可以建立新的訊息草稿來更新訊息。

這可讓您更新內容或修正問題，例如，不需重新發佈整個使用訊息的歷程。

>[!NOTE]
>
>在發佈版本仍然發佈且作用中時，可編輯草稿版本。

要更新已發佈的消息，請執行以下操作：

1. 從訊息清單中，選取您的訊息以開啟訊息。

1. 按一下「**[!UICONTROL Modify]**」。

   ![](assets/message-modify.png)

1. 確認您的選取。建立消息的草稿版本。

   ![](assets/message-modify-v2.png)

1. 編輯內容或視需要變更設定。
1. 按一下「**[!UICONTROL Publish]**」。此操作將發佈將用於下次執行的消息的新版本。

新版本一發佈，下次API呼叫時，就會產生新訊息執行。 下一個傳入的配置檔案將接收新版本。

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version.-->
