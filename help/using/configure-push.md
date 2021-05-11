---
title: 設定推播通知
description: 瞭解如何在Journey Optimizer建立推播通知
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 13%

---

# 設定推播通知{#create-push-notification}

![](assets/do-not-localize/badge.png)

在&#x200B;**[!UICONTROL Push Notification]**&#x200B;標籤中建立訊息時設定推播通知（請參閱[建立訊息](create-message.md)）。

您可以使用專用標籤，為iOS或Android作業系統設定推播通知內容。

![](assets/create-content-push.png)

## 標題與內文

要合成消息，請按一下&#x200B;**[!UICONTROL Title]**&#x200B;和&#x200B;**[!UICONTROL Body]**&#x200B;欄位。 使用運算式編輯器來定義內容和個人化資料。

在[本節](personalization/personalize.md)中進一步瞭解個人化

使用中央區段，以視覺化方式顯示推播通知在iOS和Android終端機中的顯示方式。

>[!NOTE]
>
>**[!UICONTROL Compose Message]**&#x200B;區段是&#x200B;**[!UICONTROL iOS]**&#x200B;和&#x200B;**[!UICONTROL Android]**&#x200B;標籤的共同區段。 本節中的任何變更都適用於這兩種作業系統。

## 按一下行為{#on-click-behavior}

選取收件者點按推播通知內文時的行為：

* 使用&#x200B;**[!UICONTROL Open app]**&#x200B;選項開啟與消息&#x200B;**[!UICONTROL Preset]**&#x200B;關聯的應用程式。
* 使用&#x200B;**[!UICONTROL Deeplink]**&#x200B;選項，將收件者重新導向至位於應用程式內的特定內容。 在關聯欄位中輸入深層連結。
* 使用&#x200B;**[!UICONTROL Web URL]**&#x200B;選項將收件者重新導向至外部URL。 在相關欄位中輸入URL。

## 傳送無訊息通知

無訊息推播通知（或背景通知）是傳遞至應用程式的隱藏指示。 例如，它會通知您的應用程式新內容的可用性，或在背景啟動下載。

選擇&#x200B;**[!UICONTROL Silent Notification]**&#x200B;選項以無訊息方式通知應用程式：在這種情況下，通知會直接傳送到應用程式。 設備螢幕上不顯示警報。

使用&#x200B;**[!UICONTROL Custom data]**&#x200B;部分添加鍵／值對。

## 進階選項

配置&#x200B;**[!UICONTROL Advanced options]**。 可用參數包括：

| 參數 | 可用性 | 說明 |
|---------|----------|---------|
| **[!UICONTROL Collapsible]** | iOS / Android | 可折疊的消息是可由新消息替換的消息。 例如，應用程式會更新使用者有關主題的最新消息。 在這種情況下，只有最近的訊息是相關的。 另一方面，使用不可收合的訊息時，每則訊息對用戶端應用程式而言都很重要，而且需要傳遞。 |
| **[!UICONTROL Custom sound]** | iOS / Android | 當收到通知時，移動終端將播放的聲音。 音效必須整合在應用程式中。 |
| **[!UICONTROL Badges]** | iOS / Android | 徽章可用來直接在應用程式圖示上顯示新未讀取資訊的數量。<br/>當使用者開啟或從應用程式讀取新內容時，徽章值就會消失。在裝置上收到通知時，它可以重新整理或新增相關應用程式的徽章值。<br/>例如，如果您儲存客戶的未讀文章數目，您可以利用個人化來傳送每個客戶的唯一未讀文章徽章值。如需更多個人化資訊，請參閱[本節](personalization/personalize.md)。 |
| **[!UICONTROL Notification group]** / | iOS | 將通知群組關聯至推播通知。<br/>從iOS 12開始，通知群組可讓您將訊息執行緒和通知主題整合至執行緒ID。例如，品牌可能會在一個群組ID下傳送行銷通知，同時在一或多個不同ID下保留更多作業類型通知。<br/>為了說明這一點，您可以有groupID:123 「查看新春套裝系列」和groupID:456 「您的包裹已送達」通知群組。在此範例中，所有傳送通知都會套裝在群組ID下：456. |
| **[!UICONTROL Notification channel]** | Android | 將通知渠道與推播通知建立關聯。<br/>從Android 8.0（API層級26）開始，所有通知都必須指派給渠道才能顯示。如需詳細資訊，請參閱[Android開發人員檔案](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels)。 |
| **[!UICONTROL Add content-availability flag]** | iOS | 傳送推播裝載中的內容可用標幟，以確保應用程式在收到推播通知後立即喚醒，這表示應用程式將能夠存取裝載資料。<br/> 即使應用程式在背景執行，而且不需要任何使用者互動（例如點選推播通知），這個功能仍然有效。 不過，如果應用程式未執行，則不適用。如需詳細資訊，請參閱 [Apple開發人員檔案](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)。 |
| **[!UICONTROL Add mutable-content flag]** | iOS | 傳送推播裝載中的可變內容標幟，並允許iOS SDK中提供的通知服務應用程式擴充功能修改推播通知內容。 有關詳細資訊，請參閱 [Apple 開發人員文件](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)。<br/>然後，您就可以運用行動應用程式擴充功能進一步修改來自傳送的推播通知的內容或呈現方式。例如， [!DNL Journey Optimizer] For example, users can bley this option to decrypt data, change body or title text of a notification, add a thread identifier to a notification等。 |
| **[!UICONTROL Notification visibility]** | Android | 定義推播通知的可見性。 <b>隱私</b> 權會在所有鎖定螢幕上顯示通知，但在安全的鎖定螢幕上隱藏敏感或私人資訊。<b>Public</b> 會在所有螢幕上完整顯示通知。<b>Secretwill</b> 不會在安全的螢幕上透露通知的任何部分。如需詳細資訊，請參閱[Android開發人員檔案](https://developer.android.com/reference/android/app/Notification)。 |
| **[!UICONTROL Notification priority]** | Android | 定義推播通知的重要性，從「低」到「最大」。 這會決定推播通知傳送時的「侵入性」。 如需詳細資訊，請參閱[Android開發人員檔案](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** | Android | 設定推播通知的高優先順序或一般優先順序。 如需訊息優先順序的詳細資訊，請參閱 [Google 開發人員檔案](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)。 |

## 自訂資料

在&#x200B;**[!UICONTROL Custom data]**&#x200B;區段中，您可以根據行動應用程式的設定，將自訂變數新增至裝載。 如需如何在Adobe Experience Platform和Adobe啟動中設定推播通知的詳細資訊，請參閱[本節](push-configuration.md)

