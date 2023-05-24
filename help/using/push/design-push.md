---
solution: Journey Optimizer
product: journey optimizer
title: 設計推送通知
description: 瞭解如何在Journey Optimizer設計推送通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 12%

---

# 設計推送通知 {#design-push-notification}

## 標題和正文 {#push-title-body}

要撰寫郵件，請按一下 **[!UICONTROL 標題]** 和 **[!UICONTROL 身體]** 的子菜單。 使用表達式編輯器定義內容、個性化資料和添加動態內容。 瞭解有關 [個性化](../personalization/personalize.md) 和 [動態內容](../personalization/get-started-dynamic-content.md) 的子菜單。

使用設備預覽部分可以直觀顯示推送通知在iOS和Android設備上的顯示方式。

## 點按時行為 {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="關於點按時行為"
>abstract="選取收件者點擊推播通知內文時的行為。"

當用戶按一下推式通知的正文時，可以選擇行為。

![](assets/title-body-push.png)

* 要開啟應用，請選擇 **[!UICONTROL 開啟應用]** 的雙曲餘切值。 與通知關聯的應用在 [通道表面](../configuration/channel-surfaces.md) （即消息預設）。
* 要將用戶重定向到應用程式內的特定內容，請選擇 **[!UICONTROL 迪普林克]** 的雙曲餘切值。  特定內容可以是特定視圖、頁面的特定部分或特定頁籤。 選中該選項後，在關聯欄位中輸入deplink。
* 要將用戶重定向到外部URL，請使用 **[!UICONTROL Web URL]** 的雙曲餘切值。 選中該選項後，在關聯欄位中輸入URL。

## 添加媒體 {#add-media-push}

在iOS版的推送通知中，您可以添加將在通知中顯示的影像、視頻或GIF。

在Android版本中，您只能添加影像表徵圖和擴展通知的影像。

![](assets/push-config-add-media.png)

有兩種選擇。 您可以：

* 使用 **[!UICONTROL 添加媒體]** 按鈕 **[!DNL Adobe Experience Manager Assets Essentials]**。

   瞭解如何使用 **[!DNL Adobe Experience Manager Assets Essentials]** 在 [此頁](../email/assets-essentials.md)。

* 或在 **[!UICONTROL 添加媒體]** 的子菜單。 在這種情況下，您可以將個性化添加到URL。

添加後，媒體將顯示在通知正文的右側。

## 添加按鈕 {#add-buttons-push}

通過向推送內容添加按鈕建立可操作的通知。

如果設備螢幕已鎖定，則不顯示以下按鈕：只有 **標題** 和 **消息** 的子菜單。 如果其設備已解鎖，則收件人將看到按鈕。

在iOS版中，最多可以添加四個按鈕。 在Android版本中，最多可以添加三個按鈕。

>[!NOTE]
>
>對於iOS，使用 **[!UICONTROL iOS]** 將操作與通知類別關聯的欄位。

1. 使用 **[!UICONTROL 「添加」按鈕]** 要定義設定，請執行以下操作：標籤和關聯操作。 可能的操作與 [按一下行為](#on-click-behavior)。

1. 使用 **[!UICONTROL 展開視圖]** 表徵圖，以預覽個性化按鈕。

![](assets/push_buttons.png)

## 傳送靜音通知 {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="關於靜音通知"
>abstract="在不打擾使用者的情況下傳送通知，通知不會顯示在通知中心或通知列中。"

靜默推送通知（或後台通知）是傳遞給應用程式的隱藏指令。 例如，它用於通知您的應用程式新內容的可用性或在後台啟動下載。

選擇 **[!UICONTROL 無提示通知]** 選項以靜默通知應用程式：在這種情況下，通知會直接轉送到申請。 設備螢幕上未顯示警報。

使用 **[!UICONTROL 自定義資料]** 的子菜單。

## 自訂資料

在 **[!UICONTROL 自定義資料]** 部分，您可以根據移動應用程式配置將自定義變數添加到負載中。 有關如何在Adobe Experience Platform和Adobe啟動中設定推送通知的詳細資訊，請參閱 [此部分](push-gs.md)

## 高級選項 {#advanced-options-push}

您可以配置 **[!UICONTROL 高級選項]** 來獲取推送通知。 下面列出了可用參數：

| 參數 | 說明 |
|---------|---------|
| **[!UICONTROL 可折疊]** (iOS/安卓) | 可折疊消息是一條消息，如果已過時，可以用新消息替換。 可折疊消息的常見使用案例是用於通知移動應用從伺服器同步資料的消息。 例如，一個運動應用會用最新分數更新用戶。 只有最新的資訊是相關的。 另一方面，對於不可折疊的消息，非常消息對客戶端應用很重要，需要傳遞。 |
| **[!UICONTROL 自定義聲音]** (iOS/安卓) | 當接收到通知時，移動終端將播放的聲音。 聲音需要捆綁在應用中。 |
| **[!UICONTROL 徽章]** (iOS/安卓) | 徽章可用來直接在應用程式圖示上顯示新未讀取資訊的數量。<br/>當使用者開啟或從應用程式讀取新內容時，徽章值就會消失。在裝置上收到通知時，它可以重新整理或新增相關應用程式的徽章值。<br/>例如，如果您正在儲存客戶的未讀文章數，則可以利用個性化功能為每個客戶發送唯一的未讀文章標籤值。 有關更多個性化設定，請參閱 [此部分](../personalization/personalize.md)。 |
| **[!UICONTROL 通知組]**  (僅iOS) | 將通知組與推送通知關聯。<br/>從iOS12開始，通知組允許您將消息線程和通知主題合併到線程ID中。 例如，品牌可能會在一個組ID下發送營銷通知，同時在一個或多個不同ID下保留更多操作類型通知。<br/>為了說明這一點，您可以使用groupID:123 「看新春毛衣系列」和groupID:456 「您的包已送達」通知組。 在本示例中，所有傳遞通知都將綁定在組ID下：456。 |
| **[!UICONTROL 通知渠道]** （僅限Android） | 將通知通道與推送通知關聯。<br/>從Android 8.0（API級別26）開始，所有通知都必須分配給一個通道才能顯示。 有關詳細資訊，請參閱 [Android開發人員文檔](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels)。 |
| **[!UICONTROL 添加內容可用性標誌]** (僅iOS) | 發送推送負載中的內容可用標誌，以確保應用在收到推送通知後立即被喚醒，這意味著應用將能夠訪問負載資料。<br/> 即使應用程式在後台運行且不需要任何用戶交互（例如點擊推送通知），這種方法仍然有效。 但是，如果應用未運行，則不適用。 如需詳細資訊，請參閱 [Apple開發人員檔案](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)。 |
| **[!UICONTROL 添加可變內容標誌]** (僅iOS) | 在推送負載中發送可變內容標誌，並將允許通過iOSSDK中提供的通知服務應用程式擴展來修改推送通知內容。 有關詳細資訊，請參閱 [Apple 開發人員文件](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)。<br/>然後，您可以利用您的移動應用擴展來進一步修改從發送的到達推送通知的內容或演示 [!DNL Journey Optimizer]。 例如，用戶可以利用此選項解密資料、更改通知的正文或標題文本、向通知添加線程標識符等。 |
| **[!UICONTROL 通知可見性]** （僅限Android） | 定義推送通知的可見性。 <br/><b>私人</b> 將在所有鎖屏上顯示通知，但在安全的鎖屏上隱藏敏感或隱私資訊。 <br/><b>公共</b> 將在所有鎖屏上顯示完整的通知。 <br/><b>秘密</b> 不會在安全鎖屏上顯示通知的任何部分。 <br/>有關詳細資訊，請參閱 [Android開發人員文檔](https://developer.android.com/reference/android/app/Notification)。 |
| **[!UICONTROL 通知優先順序]** （僅限Android） | 將推送通知的重要性從「低」定義為「最大」。 這確定推送通知在傳送時的「侵入性」。 有關詳細資訊，請參閱 [Android開發人員文檔](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL 交付優先順序]** （僅限Android） | 設定推送通知的高優先順序或普通優先順序。 如需訊息優先順序的詳細資訊，請參閱 [Google 開發人員檔案](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)。 |
