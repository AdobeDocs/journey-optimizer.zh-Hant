---
solution: Journey Optimizer
product: journey optimizer
title: 在歷程中新增訊息
description: 了解如何在歷程中新增訊息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 6%

---

# 電子郵件、簡訊、推播{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] 隨附內建的訊息功能。 您只需在歷程中新增推播、簡訊或電子郵件訊息活動，並定義設定和內容即可。 接著會在歷程的內容中執行及傳送。

您也可以設定特定動作以傳送訊息：

* 如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 了解更多資訊 [節](../action/action.md).

* 如果您正在使用Campaign和Journey Optimizer，請參閱下列區段：

   * [[!DNL Journey Optimizer] 和Campaign Classicv7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 和Campaign Standard](../action/acs-action.md)

若要在歷程中新增訊息，請遵循下列步驟：

1. 利用[事件](general-events.md)或[讀取區段](read-segment.md)活動來開始您的歷程。

1. 從調色盤的&#x200B;**動作**&#x200B;區段 ，拖放&#x200B;**電子郵件**、**簡訊**&#x200B;或&#x200B;**推播**&#x200B;活動至畫布。

1. 設定您的活動。 在下列頁面中了解建立訊息內容的詳細步驟：

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
   <a href="../sms/create-sms.md"><strong>建立SMS訊息</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## 更新即時內容{#update-live-content}

您可以更新即時歷程中的訊息內容（電子郵件、簡訊、推播）。

若要這麼做，請開啟您的即時歷程，選取訊息活動，然後按一下 **編輯內容**.

![](assets/add-a-message2.png)

不過，您無法變更個人化中使用的屬性，不論是設定檔屬性或內容資料（來自事件或歷程屬性）。

## 傳送時間最佳化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="關於傳送時間最佳化"
>abstract="Adobe Journey Optimizer的「傳送時間最佳化」功能採用Adobe的AI服務，可根據歷史開啟率和點按率，預測傳送電子郵件或推送訊息的最佳時機，以最大化參與。"

### 關於傳送時間最佳化 {#about-send-time}

Adobe Journey Optimizer的「傳送時間最佳化」功能採用Adobe的AI服務，可根據歷史開啟率和點按率，預測傳送電子郵件或推送訊息的最佳時機，以最大化參與。 使用我們的機器學習模型來排程每位使用者的個人化傳送時間，以提高訊息的開啟率和點按率。

「傳送時間最佳化」模型會內嵌您的Adobe Journey Optimizer資料，並查看使用者層級的開啟率（針對電子郵件和推播），然後按一下率（針對電子郵件），以判斷客戶何時最有可能與您的訊息互動。 「傳送時間最佳化」至少需要一個月的訊息追蹤資料，才能提供有根據的建議。 系統會針對每位使用者使用下列分數自動選擇最佳時間：

* 一週中每天最佳的小時數，以最大化參與
* 一週中最佳的一天，以最大化參與
* 一週中最佳日期的最佳小時，以最大化參與

無論您是在說打分還是訓練，模型都會有所不同。 培訓最初每週進行，然後每季進行。 分數最初是每週，然後是每月。

* 訓練 — 用於建立分數的演算法的開發
* 計分 — 根據訓練的模型將分數應用於個別設定檔

此資訊會與使用者的設定檔一起儲存，並在歷程執行時參考，告知Adobe Journey Optimizer何時傳送訊息。

>[!CAUTION]
>
>此功能與突發模式不相容。

### 啟動傳送時間最佳化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="啟動傳送時間最佳化"
>abstract="選取適當的選項按鈕，以選擇要最佳化電子郵件開啟次數還是電子郵件點進次數。 您也可以在下一個選項中輸入「傳送」的值，以括弧表示系統使用的傳送時間。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="啟動傳送時間最佳化"
>abstract="推送訊息預設為開啟選項，因為點按不適用於推送訊息。 您也可以在下一個選項中輸入「傳送」的值，以括弧表示系統使用的傳送時間。"

透過選取 **傳送時間最佳化** 從活動參數切換。

![](../building-journeys/assets/jo-message5.png)

對於電子郵件訊息，請選取適當的選項按鈕，以選擇要最佳化電子郵件開啟次數還是電子郵件點進次數。 推送訊息預設為開啟選項，因為點按不適用於推送訊息。

您也可以為 **在下一個** 選項。 如果選擇「6小時」作為值， [!DNL Journey Optimizer] 會檢查每個使用者設定檔，並在歷程執行時間起六小時內選取最佳傳送時間。
