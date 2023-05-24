---
solution: Journey Optimizer
product: journey optimizer
title: 在歷程中新增訊息
description: 瞭解如何在旅途中添加消息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 旅程，消息，推送，簡訊，電子郵件，應用內
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 22%

---

# 電子郵件、應用程式內、推播、簡訊{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] 內置消息功能。 在旅途中，您只需添加推送、SMS、應用內或電子郵件活動並定義設定和內容即可。 然後，在旅程的上下文中執行併發送。

您還可以設定特定操作以發送消息：

* 如果您使用第三方系統發送消息，則可以建立自定義操作。 瞭解更多資訊 [節](../action/action.md)。

* 如果您正在使用「活動」和「Journey Optimizer」，請參閱以下部分：

   * [[!DNL Journey Optimizer] 和Campaign Classicv7/營銷活動v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 和Campaign Standard](../action/acs-action.md)

要在行程中添加消息，請執行以下步驟：

1. 利用[事件](general-events.md)或[讀取區段](read-segment.md)活動來開始您的歷程。

1. 從 **操作** ，拖放 **電子郵件**&#x200B;的 **應用程式內**&#x200B;的 **簡訊** 或 **推** 的下界。

1. 配置活動。 瞭解在以下頁面中建立消息內容的詳細步驟：

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
   <div><a href="../in-app/create-in-app.md"><strong>建立應用內消息</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="不頻繁" src="../assets/do-not-localize/push.jpg">
   </a>
   <div>
   <a href="../push/create-push.md"><strong>建立推式通知<strong></a>
   </div>
   <p>
   </td>
   <td>
   <a href="../sms/create-sms.md">
   <img alt="驗證" src="../assets/do-not-localize/sms.jpg">
   </a>
   <div>
   <a href="../sms/create-sms.md"><strong>建立SMS消息</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## 更新即時內容{#update-live-content}

您可以在即時旅程中更新消息（電子郵件、應用內、推送、簡訊）的內容。

要執行此操作，請開啟即時旅程，選擇消息活動並按一下 **編輯內容**。

![](assets/add-a-message2.png)

但是，您不能更改個性化中使用的屬性，無論這些屬性是配置檔案屬性還是上下文資料（來自事件或行程屬性）。

如果修改了上下文資料，將顯示以下錯誤消息：ERR_AUTHORING_JOURNEVERSION_201

如果修改了配置檔案屬性，將顯示以下錯誤消息：ERR_AUTHORING_JOURNEVERSION_202

請注意，對於應用內活動，可以在行程即時期間對內容進行任何更改，但無法修改應用內觸發器。

## 傳送時間最佳化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="關於傳送時間最佳化"
>abstract="Adobe Journey Optimizer 的傳送時間最佳化功能由 Adobe 的 AI 服務提供支援，可以預測傳送電子郵件或推播訊息的最佳時間，以根據歷史開啟率和點擊率將參與度提高至最大限度。"

### 關於發送時間優化 {#about-send-time}

Adobe Journey Optimizer 的傳送時間最佳化功能由 Adobe 的 AI 服務提供支援，可以預測傳送電子郵件或推播訊息的最佳時間，以根據歷史開啟率和點擊率將參與度提高至最大限度。使用我們的機器學習模型為每個用戶安排個性化發送時間，以增加消息的開啟和點擊率。

「發送時間優化」模型將接收您的Adobe Journey Optimizer資料，並查看用戶級別的開啟（對於電子郵件和推送），然後按一下（對於電子郵件）速率，以確定客戶最可能在何時開始使用您的消息。 「發送時間優化」要求最少一個月的消息跟蹤資料，以便提供有根據的建議。 對於每個用戶，系統將使用以下分數自動選擇最佳時間：

* 一週中每天的最佳時間，以最大限度地提高參與
* 一週中最好的一天，以最大限度地提高參與
* 一週中最好的一天中的最佳時刻，以最大限度地提高參與

無論您是在打分還是培訓，模型都會有所不同。 培訓每週進行一次，然後每季度進行一次。 評分最初是每週，然後是每月。

* 訓練 — 用於生成分數的算法的開發
* 評分 — 基於已訓練的模型將評分應用於單個配置檔案

此資訊與用戶的配置檔案一起儲存，並在行程執行時被引用，以告知Adobe Journey Optimizer何時發送您的消息。

>[!CAUTION]
>
>此功能與拆分模式不相容。

### 啟動傳送時間最佳化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="啟動傳送時間最佳化"
>abstract="透過選取適當的選項按鈕來選擇要將電子郵件開啟還是電子郵件點進最佳化。您還可以在下一個選項內輸入傳送的值以選擇將系統使用的傳送時間加上括號。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="啟動傳送時間最佳化"
>abstract="推播訊息預設為開啟選項，因為點擊不適用於推播訊息。您還可以在下一個選項內輸入傳送的值以選擇將系統使用的傳送時間加上括號。"

通過選擇 **發送時間優化** 從活動參數中切換。

![](../building-journeys/assets/jo-message5.png)

對於電子郵件，選擇是開啟電子郵件時進行優化，還是通過選擇相應的單選按鈕進行電子郵件點擊瀏覽。 推播訊息預設為開啟選項，因為點擊不適用於推播訊息。

您也可以通過為 **在下一個** 的雙曲餘切值。 如果你選擇&quot;六小時&quot;作為值， [!DNL Journey Optimizer] 將檢查每個用戶配置檔案，並在行程執行時間後六小時內選擇最佳發送時間。

**如果最佳時間在窗口之外，會發生什麼？**

讓我們舉一個具有以下設定的示例：

* 按一下時優化
* 行動定於上午10點開始
* 窗口為3小時

輪廓可具有窗口外的最佳開啟時間。 例如，John在按一下時的最佳開啟時間為下午5點。

在個人資料級別，每週每小時都有分數。 在此示例中，電子郵件將始終在窗口內發送。 在運行時，系統檢查該窗口（從上午10點開始的3小時窗口）內的分數清單。 然後，系統比較10、11和中午的得分，並選擇最高分。 郵件在當時發送。
