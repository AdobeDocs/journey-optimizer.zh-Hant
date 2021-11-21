---
title: 發佈和修改訊息
description: 了解如何發佈和更新訊息
snippet: y
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 116e2223-a806-4f68-9a8c-c0bde6008010
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# 發佈您的訊息 {#publish-manage-messages}

## 發佈訊息 {#publish-message}

建立訊息後，您就可以發佈訊息，以便供執行。

>[!CAUTION]
>
>發佈前，請檢查並解決警報。 [了解更多](alerts.md)

![](assets/publish-message.png)

訊息發佈後，就會以 **[!UICONTROL Published]** 狀態。

現在已可由一或多個 [歷程](building-journeys/journey.md).

## 更新唯讀訊息 {#modify-message}

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

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version. -->
