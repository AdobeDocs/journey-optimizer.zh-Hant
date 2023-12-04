---
solution: Journey Optimizer
product: journey optimizer
title: 在歷程中新增訊息
description: 瞭解如何在歷程中新增訊息
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，訊息，推播，簡訊，電子郵件，應用程式內
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 898ad9dadd2d9e71e6881113730ac469a36257bc
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 14%

---

# 電子郵件、應用程式內、推播、簡訊/多媒體簡訊{#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="訊息活動"
>abstract="Journey Optimizer 內建訊息功能。您只需在歷程中新增推播、簡訊(SMS/MMS)、應用程式內或電子郵件訊息活動，以及定義設定和內容即可。 然後會在歷程的內容中執行和傳送。"

[!DNL Journey Optimizer] 隨附內建訊息功能。 您只需在歷程中新增推播、簡訊/多媒體簡訊、應用程式內或電子郵件訊息活動，以及定義設定和內容即可。 然後會在歷程的內容中執行和傳送。

您也可以設定傳送訊息給您的特定動作：

* 如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 在本節瞭解更多 [區段](../action/action.md).

* 如果您正在使用Campaign和Journey Optimizer，請參閱下列區段：

   * [[!DNL Journey Optimizer] 和Campaign Classicv7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 和Campaign Standard](../action/acs-action.md)

若要在歷程中新增訊息，請遵循下列步驟：

1. 透過以下專案開始您的歷程 [事件](general-events.md) 或 [讀取對象](read-audience.md) 活動。

1. 從 **動作** 區段，拖放 **電子郵件**，和 **應用程式內**，和 **簡訊** 或 **推播** 活動加入畫布。

1. 設定您的活動。 在以下頁面瞭解建立訊息內容的詳細步驟：

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="銷售機會" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>建立電子郵件</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../in-app/create-in-app.md">
   <img alt="銷售機會" src="../assets/do-not-localize/in-app.jpg">
   </a>
   <div><a href="../in-app/create-in-app.md"><strong>建立應用程式內訊息</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="不頻繁" src="../assets/do-not-localize/push.jpg">
   </a>
   <div>
   <a href="../push/create-push.md"><strong>建立推播通知<strong></a>
   </div>
   <p>
   </td>
   <td>
   <a href="../sms/create-sms.md">
   <img alt="驗證" src="../assets/do-not-localize/sms.jpg">
   </a>
   <div>
   <a href="../sms/create-sms.md"><strong>建立文字訊息（簡訊/多媒體簡訊）</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## 更新即時內容{#update-live-content}

您可以在即時歷程中更新訊息內容（電子郵件、應用程式內、推播、簡訊）。

若要這麼做，請開啟您的即時歷程，選取訊息活動並按一下 **編輯內容**.

![](assets/add-a-message2.png)

但是，您無法變更個人化中使用的屬性，無論是設定檔屬性或內容資料（來自事件或歷程屬性）。

如果您修改內容資料，將會顯示下列錯誤訊息： ERR_AUTHORING_JOURNEYVERSION_201

如果您修改設定檔屬性，將會顯示下列錯誤訊息：ERR_AUTHORING_JOURNEYVERSION_202

請注意，針對應用程式內活動，可以在歷程上線時對內容進行任何變更，但無法修改應用程式內觸發器。

## 傳送時間最佳化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="關於傳送時間最佳化"
>abstract="Adobe Journey Optimizer 的傳送時間最佳化功能由 Adobe 的 AI 服務提供支援，可以預測傳送電子郵件或推播訊息的最佳時間，以根據歷史開啟率和點擊率將參與度提高至最大限度。"

### 關於傳送時間最佳化 {#about-send-time}

Adobe Journey Optimizer的傳送時間最佳化功能採用Adobe的AI服務，可根據歷史開啟率和點按率，預測傳送電子郵件或推送訊息的最佳時機，最大化參與程度。 使用我們的機器學習模型，為每位使用者排程個人化的傳送時間，以提高您訊息的開啟及點閱率。

傳送時間最佳化模型會擷取您的Adobe Journey Optimizer資料，並檢視使用者層級的開啟（針對電子郵件和推播）和點按（針對電子郵件）率，以判斷客戶何時最有可能參與您的傳訊。 傳送時間最佳化需要至少一個月的訊息追蹤資料，才能提出明智的建議。 對於每個使用者，系統將使用下列分數自動挑選最佳時間：

* 一週中每天的最佳時刻，以最大化參與度
* 一週中最佳的一天，可最大化參與度
* 一週中最佳一天的最佳時刻，最大化參與度

無論您談論的是評分還是訓練，這個模型各有不同。 培訓最初每週進行，然後每季進行。 評分最初為每週，然後每月進行。

* 訓練 — 開發用來建立評分的演演算法
* 評分 — 根據已訓練的模型，將評分套用至個別設定檔

此資訊會與使用者的設定檔儲存，並在歷程執行時參考，以告知Adobe Journey Optimizer何時傳送您的訊息。

>[!CAUTION]
>
>此功能與高載模式不相容。

### 常見問答 {#faq-send-time}

傳送時間最佳化有什麼作用？ 如何處理新設定檔？ 這會將傳送分散到6/12/24小時的時段中嗎？

傳送時間最佳化會嘗試預測與客戶互動的最佳時機，並最佳化電子郵件的開啟/點按率。 此分數為以下格式 `3*7*24` 每個設定檔的屬性。 此 `7*24` 屬性說明向收件者傳送電子郵件的預測最佳時間排名，3用於最佳化電子郵件開啟率、電子郵件點按率和推播開啟率。

我可以在哪裡看到每個設定檔的預期傳送時間？

您可以在中檢視整體分數 **設定檔** 介面。 對於三組168分中的每一組，排名會從–83增加到84。 排名越高，選擇與收件者互動的時間就越好。 由於您可以定義歷程的開始和持續時間，因此最佳排名(84)可能不會落入該時間範圍內。 在這種情況下，我們建議選擇排名值最高的小時。

有哪些報表可供使用？

存取您的歷程，按一下 **檢視報告** 按鈕並選取 **歷程** 索引標籤在左側。 [閱讀全文](../reports/journey-global-report.md)

傳送時間最佳化資料如何影響設定檔豐富度？

傳送時間最佳化會將分數/屬性新增至每個設定檔，但不會建立新設定檔。

### 啟動傳送時間最佳化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="啟動傳送時間最佳化"
>abstract="透過選取適當的選項按鈕來選擇要將電子郵件開啟還是電子郵件點進最佳化。您還可以在下一個選項內輸入傳送的值以選擇將系統使用的傳送時間加上括號。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="啟動傳送時間最佳化"
>abstract="推播訊息預設為開啟選項，因為點擊不適用於推播訊息。您還可以在下一個選項內輸入傳送的值以選擇將系統使用的傳送時間加上括號。"

選取電子郵件或推播訊息的傳送時間最佳化 **傳送時間最佳化** 從活動引數切換。

![](../building-journeys/assets/jo-message5.png)

針對電子郵件訊息，選取適當的選項按鈕，以選擇最佳化電子郵件開啟次數或電子郵件點進次數。 推送訊息預設為開啟選項，因為點按不適用於推送訊息。

您也可以輸入「 」的值，選擇將系統使用的傳送時間括起來 **在下一次傳送中** 選項。 如果您選擇「六小時」作為值， [!DNL Journey Optimizer] 將會檢查每個使用者設定檔，並在歷程執行時間起的六小時內挑選最佳傳送時間。

**如果最佳時間在視窗之外，會發生什麼情況？**

以下列設定為例：

* 點按時最佳化
* 動作預定在上午10點開始
* 視窗為3小時

設定檔在視窗外可以有最佳的開啟時間。 例如，John的最佳點按開啟時間是下午5點。

在設定檔層級，有一週中每個小時的分數。 在此範例中，電子郵件一律會在視窗中傳送。 在執行階段，系統會檢查該時段（上午10點開始的3小時時段）內的分數清單。 然後系統會比較10、11和中午的分數，並選取最高分。 屆時會傳送電子郵件。
