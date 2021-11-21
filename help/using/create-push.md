---
title: 設定推播通知
description: 了解如何在Journey Optimizer中建立推播通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 11%

---

# 建立推播通知 {#create-push-notification}

一旦您 [建立訊息](create-message.md)，按一下 **[!UICONTROL Push Notification]** 標籤來定義推播通知的設定和內容。

![](assets/create-content-push.png)

使用專用標籤來定義的推播通知設定 **iOS** 和 **Android** 作業系統。

>[!NOTE]
>
>此 **[!UICONTROL Compose Message]** 區段對兩者都很常見 **[!UICONTROL iOS]** 和 **[!UICONTROL Android]** 標籤。 本節中的任何更改都將應用於兩個頁簽。

## 標題與內文

若要撰寫訊息，請按一下 **[!UICONTROL Title]** 和 **[!UICONTROL Body]** 欄位。 使用運算式編輯器來定義內容和個人化資料。 進一步了解中的運算式編輯器中的個人化 [本節](personalization/personalize.md)

使用裝置預覽區段來視覺化推播通知在iOS和Android裝置上的顯示方式。

## 點按行為 {#on-click-behavior}

選取收件者點按推播通知內文時的行為。

![](assets/title-body-push.png)

* 使用 **[!UICONTROL Open app]** 選項以開啟與消息關聯的應用程式 **[!UICONTROL Preset]**.
* 使用 **[!UICONTROL Deeplink]** 選項，將收件者重新導向至位於應用程式內的特定內容。 在關聯欄位中輸入深層連結。
* 使用 **[!UICONTROL Web URL]** 選項，將收件者重新導向至外部URL。 在關聯欄位中輸入URL。

## 新增媒體

在iOS版的推播通知中，您可以新增將顯示在通知中的影像、影片或GIF。

在Android版本中，您只能新增影像圖示和影像以用於展開通知。

![](assets/push-config-add-media.png)

有兩個選項可供使用。 您可以：

* 按一下 **[!UICONTROL Add media]** 按鈕，以在中選取資產 **[!DNL Adobe Experience Manager Assets Essentials]**.

   了解如何使用 **[!DNL Adobe Experience Manager Assets Essentials]** in [本頁](assets-essentials.md).

* 或按一下 **[!UICONTROL Add media]** 欄位。 在此情況下，您可以新增個人化。

新增後，媒體會顯示在通知內文的右側。

## 添加按鈕

您可以新增按鈕至推播內容，以建立可操作的通知。

如果設備螢幕已鎖定，則不顯示以下按鈕：只有 **標題** 和 **訊息** 中顯示。 如果其設備已解鎖，則收件者將看到按鈕。

在iOS版本中，最多可新增4個按鈕。 在Android版本中，最多可以新增3個按鈕。

>[!NOTE]
>
>若為iOS，請使用 **[!UICONTROL iOS category]** 欄位，將動作與通知類別關聯。

按一下 **[!UICONTROL Add button]** 若要定義設定：標籤和關聯動作。 可能的動作與 [點按行為](#on-click-behavior).

按一下 **[!UICONTROL Expand view]** 預覽個人化按鈕。

![](assets/push_buttons.png)

## 傳送靜默通知

靜默推播通知（或背景通知）是傳遞至應用程式的隱藏指示。 例如，它用於通知您的應用程式新內容的可用性或在後台啟動下載。

選取 **[!UICONTROL Silent Notification]** 選項以無訊息地通知應用程式：在這種情況下，通知會直接轉送到應用程式。 設備螢幕上不顯示警報。

使用 **[!UICONTROL Custom data]** 區段來新增索引鍵值配對。

## 自訂資料

在 **[!UICONTROL Custom data]** 區段中，您可以根據行動應用程式設定，將自訂變數新增至裝載。 如需如何在Adobe Experience Platform和AdobeLaunch中設定推播通知的詳細資訊，請參閱 [本節](push-gs.md)

## 進階選項

您可以設定 **[!UICONTROL Advanced options]** 的URL。 可用參數列於下列：

| 參數 | 說明 |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS / Android) | 可折疊的訊息是一種訊息，如果已過時，可以用新訊息取代。 可折疊訊息的常見使用案例是指示行動應用程式從伺服器同步資料的訊息。 例如，運動應用程式會以最新分數更新使用者。 只有最新的訊息才相關。 另一方面，使用不可折疊的訊息，非常重要的訊息對用戶端應用程式很重要，需要傳送。 |
| **[!UICONTROL Custom sound]** (iOS / Android) | 接收通知時由移動終端播放的聲音。 音效必須整合在應用程式中。 |
| **[!UICONTROL Badges]** (iOS / Android) | 徽章可用來直接在應用程式圖示上顯示新未讀取資訊的數量。<br/>當使用者開啟或從應用程式讀取新內容時，徽章值就會消失。在裝置上收到通知時，它可以重新整理或新增相關應用程式的徽章值。<br/>例如，如果您要儲存客戶的未讀文章數量，您可以運用個人化功能，為每個客戶傳送不重複的未讀文章徽章值。 如需更多個人化資訊，請參閱 [本節](personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (僅限iOS) | 將通知群組與推播通知建立關聯。<br/>從iOS 12開始，通知群組可讓您將訊息執行緒和通知主題併入執行緒ID。 例如，品牌可能會在一個群組ID下傳送行銷通知，同時在一或多個不同ID下保留更多操作類型通知。<br/>為了說明這一點，您可以有groupID:123 「查看新的sweaters春季系列」和groupID:456 「您的套件已傳送」通知群組。 在此範例中，所有傳送通知都會整合在群組ID下：456。 |
| **[!UICONTROL Notification channel]** （僅限Android） | 將通知通道與推播通知相關聯。<br/>從Android 8.0（API層級26）開始，必須將所有通知指派給管道才能顯示。 有關詳細資訊，請參閱 [Android開發人員檔案](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (僅限iOS) | 傳送推播裝載中的可用內容標幟，以確保應用程式在收到推播通知時立即喚醒，這表示應用程式將能夠存取裝載資料。<br/> 即使應用程式在背景執行，且不需要任何使用者互動（例如點選推播通知），這仍然有效。 不過，如果應用程式未執行，則不適用。 如需詳細資訊，請參閱 [Apple開發人員檔案](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)。 |
| **[!UICONTROL Add mutable-content flag]** (僅限iOS) | 在推播裝載中傳送可變內容標幟，並允許iOS SDK中提供的通知服務應用程式擴充功能修改推播通知內容。 有關詳細資訊，請參閱 [Apple 開發人員文件](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)。<br/>接著，您就可以運用行動應用程式擴充功能，進一步修改來自 [!DNL Journey Optimizer]. 例如，用戶可以利用此選項解密資料、更改通知的正文或標題文本、向通知添加線程標識符等。 |
| **[!UICONTROL Notification visibility]** （僅限Android） | 定義推播通知的可見性。 <br/><b>私人</b> 會在所有鎖屏上顯示通知，但在安全的鎖屏上隱藏敏感或隱私資訊。 <br/><b>公開</b> 會在所有鎖屏上全部顯示通知。 <br/><b>機密</b> 不會在安全鎖屏上顯示通知的任何部分。 <br/>有關詳細資訊，請參閱 [Android開發人員檔案](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** （僅限Android） | 將推播通知的重要性從「低」定義為「最大」。 這決定了傳送推播通知時「侵入」的程度。 有關詳細資訊，請參閱 [Android開發人員檔案](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** （僅限Android） | 設定推播通知的高優先順序或一般優先順序。 如需訊息優先順序的詳細資訊，請參閱 [Google 開發人員檔案](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)。 |

**相關主題**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [設定推播通道](push-gs.md)
* [建立新訊息](create-message.md)
* [在歷程中新增訊息](building-journeys/journeys-message.md)
