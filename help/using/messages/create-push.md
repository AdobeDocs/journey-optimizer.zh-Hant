---
title: 設定推播通知
description: 瞭解如何在Journey Optimizer建立推送通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 9%

---

# 建立推播通知 {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="推送消息建立"
>abstract="添加推送消息，然後使用表達式編輯器對其進行個性化設定。"


推送通知可幫助您隨時聯繫您的移動應用用戶 — 尤其是當他們沒有主動使用您的應用時。 推式通知可以幫助您實現各種使用情形，如提供有關服務的更新、要求用戶採取行動、提醒用戶進行新交易等。 設備平台要求在最終用戶接收或查看您的通知之前選擇加入。 用戶選擇加入最早可以在應用首次在安裝後啟動之後接收，也可以在後續會話或工作流中接收。

[!DNL Journey Optimizer] 支援推送通知，並幫助您以業界領先的吞吐率發送高度相關的通知。 推送通知可能包括個性化和基於旅程的上下文，以便利用您的品牌對Adobe Experience Cloud的資料洞察力。

一旦 [已建立消息](get-started-content.md)，按一下 **[!UICONTROL Push Notification]** 頁籤，以定義推送通知的設定和內容。

![](assets/create-content-push.png)

使用專用頁籤定義推送通知設定 **iOS** 和 **安卓** 作業系統。

>[!NOTE]
>
>的 **[!UICONTROL Compose Message]** 節對兩者都是公用的 **[!UICONTROL iOS]** 和 **[!UICONTROL Android]** 頁籤。 本節中的任何更改都將應用於這兩個設定。

## 標題和正文 {#push-title-body}

要撰寫郵件，請按一下 **[!UICONTROL Title]** 和 **[!UICONTROL Body]** 的子菜單。 使用表達式編輯器定義內容和個性化資料。 在中的表達式編輯器中瞭解有關個性化的詳細資訊 [此部分](../personalization/personalize.md)

使用設備預覽部分可以直觀顯示推送通知在iOS和Android設備上的顯示方式。

## 按一下行為 {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="關於按一下行為"
>abstract="選擇收件人按一下推送通知正文時的行為。"

當用戶按一下推式通知的正文時，可以選擇行為。

![](assets/title-body-push.png)

* 要開啟應用，請選擇 **[!UICONTROL Open app]** 的雙曲餘切值。 與通知關聯的應用在消息中定義 **[!UICONTROL Preset]**。 [瞭解更多資訊](../configuration/message-presets.md) 關於消息預設。
* 要將用戶重定向到應用程式內的特定內容，請選擇 **[!UICONTROL Deeplink]** 的雙曲餘切值。  特定內容可以是特定視圖、頁面的特定部分或特定頁籤。 選中該選項後，在關聯欄位中輸入deplink。
* 要將用戶重定向到外部URL，請使用 **[!UICONTROL Web URL]** 的雙曲餘切值。 選中該選項後，在關聯欄位中輸入URL。

## 添加媒體 {#add-media-push}

在iOS版的推送通知中，您可以添加將在通知中顯示的影像、視頻或GIF。

在Android版本中，您只能添加影像表徵圖和擴展通知的影像。

![](assets/push-config-add-media.png)

有兩種選擇。 您可以：

* 使用 **[!UICONTROL Add media]** 按鈕 **[!DNL Adobe Experience Manager Assets Essentials]**。

   瞭解如何使用 **[!DNL Adobe Experience Manager Assets Essentials]** 在 [此頁](../design/assets-essentials.md)。

* 或在 **[!UICONTROL Add media]** 的子菜單。 在這種情況下，您可以將個性化添加到URL。

添加後，媒體將顯示在通知正文的右側。

## 添加按鈕 {#add-buttons-push}

通過向推送內容添加按鈕建立可操作的通知。

如果設備螢幕已鎖定，則不顯示以下按鈕：只有 **標題** 和 **消息** 的子菜單。 如果其設備已解鎖，則收件人將看到按鈕。

在iOS版中，最多可以添加四個按鈕。 在Android版本中，最多可以添加三個按鈕。

>[!NOTE]
>
>對於iOS，使用 **[!UICONTROL iOS category]** 將操作與通知類別關聯的欄位。

1. 使用 **[!UICONTROL Add button]** 要定義設定，請執行以下操作：標籤和關聯操作。 可能的操作與 [按一下行為](#on-click-behavior)。

1. 使用 **[!UICONTROL Expand view]** 表徵圖，以預覽個性化按鈕。

![](assets/push_buttons.png)

## 發送無提示通知 {#silent-notification}

靜默推送通知（或後台通知）是傳遞給應用程式的隱藏指令。 例如，它用於通知您的應用程式新內容的可用性或在後台啟動下載。

選擇 **[!UICONTROL Silent Notification]** 選項以靜默通知應用程式：在這種情況下，通知會直接轉送到申請。 設備螢幕上未顯示警報。

使用 **[!UICONTROL Custom data]** 的子菜單。

## 自訂資料

在 **[!UICONTROL Custom data]** 部分，您可以根據移動應用程式配置將自定義變數添加到負載中。 有關如何在Adobe Experience Platform和Adobe啟動中設定推送通知的詳細資訊，請參閱 [此部分](../configuration/push-gs.md)

## 高級選項 {#advanced-options-push}

您可以配置 **[!UICONTROL Advanced options]** 來獲取推送通知。 下面列出了可用參數：

| 參數 | 說明 |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS/安卓) | 可折疊消息是一條消息，如果已過時，可以用新消息替換。 可折疊消息的常見使用案例是用於通知移動應用從伺服器同步資料的消息。 例如，一個運動應用會用最新分數更新用戶。 只有最新的資訊是相關的。 另一方面，對於不可折疊的消息，非常消息對客戶端應用很重要，需要傳遞。 |
| **[!UICONTROL Custom sound]** (iOS/安卓) | 當接收到通知時，移動終端將播放的聲音。 聲音需要捆綁在應用中。 |
| **[!UICONTROL Badges]** (iOS/安卓) | 徽章可用來直接在應用程式圖示上顯示新未讀取資訊的數量。<br/>當使用者開啟或從應用程式讀取新內容時，徽章值就會消失。在裝置上收到通知時，它可以重新整理或新增相關應用程式的徽章值。<br/>例如，如果您正在儲存客戶的未讀文章數，則可以利用個性化功能為每個客戶發送唯一的未讀文章標籤值。 有關更多個性化設定，請參閱 [此部分](../personalization/personalize.md)。 |
| **[!UICONTROL Notification group]**  (僅iOS) | 將通知組與推送通知關聯。<br/>從iOS12開始，通知組允許您將消息線程和通知主題合併到線程ID中。 例如，品牌可能會在一個組ID下發送營銷通知，同時在一個或多個不同ID下保留更多操作類型通知。<br/>為了說明這一點，您可以使用groupID:123 「看新春毛衣系列」和groupID:456 「您的包已送達」通知組。 在本示例中，所有傳遞通知都將綁定在組ID下：456。 |
| **[!UICONTROL Notification channel]** （僅限Android） | 將通知通道與推送通知關聯。<br/>從Android 8.0（API級別26）開始，所有通知都必須分配給一個通道才能顯示。 有關詳細資訊，請參閱 [Android開發人員文檔](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels)。 |
| **[!UICONTROL Add content-availability flag]** (僅iOS) | 發送推送負載中的內容可用標誌，以確保應用在收到推送通知後立即被喚醒，這意味著應用將能夠訪問負載資料。<br/> 即使應用程式在後台運行且不需要任何用戶交互（例如點擊推送通知），這種方法仍然有效。 但是，如果應用未運行，則不適用。 如需詳細資訊，請參閱 [Apple開發人員檔案](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)。 |
| **[!UICONTROL Add mutable-content flag]** (僅iOS) | 在推送負載中發送可變內容標誌，並將允許通過iOSSDK中提供的通知服務應用程式擴展來修改推送通知內容。 有關詳細資訊，請參閱 [Apple 開發人員文件](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)。<br/>然後，您可以利用您的移動應用擴展來進一步修改從發送的到達推送通知的內容或演示 [!DNL Journey Optimizer]。 例如，用戶可以利用此選項解密資料、更改通知的正文或標題文本、向通知添加線程標識符等。 |
| **[!UICONTROL Notification visibility]** （僅限Android） | 定義推送通知的可見性。 <br/><b>私人</b> 將在所有鎖屏上顯示通知，但在安全的鎖屏上隱藏敏感或隱私資訊。 <br/><b>公共</b> 將在所有鎖屏上顯示完整的通知。 <br/><b>秘密</b> 不會在安全鎖屏上顯示通知的任何部分。 <br/>有關詳細資訊，請參閱 [Android開發人員文檔](https://developer.android.com/reference/android/app/Notification)。 |
| **[!UICONTROL Notification priority]** （僅限Android） | 將推送通知的重要性從「低」定義為「最大」。 這確定推送通知在傳送時的「侵入性」。 有關詳細資訊，請參閱 [Android開發人員文檔](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** （僅限Android） | 設定推送通知的高優先順序或普通優先順序。 如需訊息優先順序的詳細資訊，請參閱 [Google 開發人員檔案](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)。 |

**相關主題**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [配置推送通道](../configuration/push-gs.md)
* [建立新郵件](get-started-content.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
