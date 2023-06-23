---
solution: Journey Optimizer
product: journey optimizer
title: 傳送時間最佳化
description: 瞭解如何在訊息中最佳化引數傳送時間
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 傳送時間，傳送，訊息，最佳化，歷程， AI，智慧
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 1cf62f949c1309b864ccd352059a444fd7bd07f0
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 36%

---

# 傳送時間最佳化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="關於傳送時間最佳化"
>abstract="Adobe Journey Optimizer 的傳送時間最佳化功能由 Adobe 的 AI 服務提供支援，可以預測傳送電子郵件或推播訊息的最佳時間，以根據歷史開啟率和點擊率將參與度提高至最大限度。"

Adobe Journey Optimizer 的傳送時間最佳化功能由 Adobe 的 AI 服務提供支援，可以預測傳送電子郵件或推播訊息的最佳時間，以根據歷史開啟率和點擊率將參與度提高至最大限度。使用我們的機器學習模型，為每位使用者安排個人化的傳送時間，以提高您訊息的開啟及點閱率。

傳送時間最佳化模型會擷取您的Adobe Journey Optimizer資料，並檢視使用者層級的開啟（針對電子郵件和推播）和點按（針對電子郵件）率，以判斷客戶何時最有可能參與您的傳訊。 傳送時間最佳化需要至少一個月的訊息追蹤資料，才能提出明智的建議。 系統會使用下列分數，為每位使用者自動挑選最佳時間：

* 一週中每天最佳的一小時，以最大化參與度
* 一週中最佳的一天，可讓參與度最大化
* 一週中最佳一天中最佳的一小時，以最大化參與度

無論您談論的是評分或訓練，此模式會有所不同。 培訓最初每週進行，然後每季度進行。 評分最初為每週，然後每月進行。

* 訓練 — 開發用來建立評分的演演算法
* 評分 — 根據已訓練的模型，將評分套用至個別設定檔

此資訊會儲存在使用者的設定檔中，並在歷程執行時參考，以告知Adobe Journey Optimizer何時傳送您的訊息。

## 啟動傳送時間最佳化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="啟動傳送時間最佳化"
>abstract="透過選取適當的選項按鈕來選擇要將電子郵件開啟還是電子郵件點進最佳化。您還可以在下一個選項內輸入傳送的值以選擇將系統使用的傳送時間加上括號。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="啟動傳送時間最佳化"
>abstract="推播訊息預設為開啟選項，因為點擊不適用於推播訊息。您還可以在下一個選項內輸入傳送的值以選擇將系統使用的傳送時間加上括號。"

透過選取「 」，對電子郵件或推送訊息啟用傳送時間最佳化 **傳送時間最佳化** 從活動引數切換。

![](../building-journeys/assets/jo-message5.png)

對於電子郵件訊息，選擇是否最佳化電子郵件開啟次數，或透過選取適當的選項按鈕來最佳化電子郵件點進次數。 推播訊息預設為開啟選項，因為點擊不適用於推播訊息。

您也可以輸入「 」的值，選擇將系統使用的傳送時間括起來。 **傳送於下一個** 選項。 如果您選擇「六小時」作為值， [!DNL Journey Optimizer] 將會檢查每個使用者設定檔，並在歷程執行時間的6小時內挑選最佳傳送時間。
