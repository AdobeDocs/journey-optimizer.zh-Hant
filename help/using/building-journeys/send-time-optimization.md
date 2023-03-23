---
solution: Journey Optimizer
product: journey optimizer
title: 傳送時間最佳化
description: 了解如何為訊息中的傳送時間最佳化參數
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 傳送時間，傳送，訊息，最佳化，歷程， AI，智慧
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 36%

---

# 傳送時間最佳化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="關於傳送時間最佳化"
>abstract="Adobe Journey Optimizer 的傳送時間最佳化功能由 Adobe 的 AI 服務提供支援，可以預測傳送電子郵件或推播訊息的最佳時間，以根據歷史開啟率和點擊率將參與度提高至最大限度。"

Adobe Journey Optimizer 的傳送時間最佳化功能由 Adobe 的 AI 服務提供支援，可以預測傳送電子郵件或推播訊息的最佳時間，以根據歷史開啟率和點擊率將參與度提高至最大限度。使用我們的機器學習模型來排程每位使用者的個人化傳送時間，以提高訊息的開啟率和點按率。

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

## 啟動傳送時間最佳化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="啟動傳送時間最佳化"
>abstract="透過選取適當的選項按鈕來選擇要將電子郵件開啟還是電子郵件點進最佳化。您還可以在下一個選項內輸入傳送的值以選擇將系統使用的傳送時間加上括號。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="啟動傳送時間最佳化"
>abstract="推播訊息預設為開啟選項，因為點擊不適用於推播訊息。您還可以在下一個選項內輸入傳送的值以選擇將系統使用的傳送時間加上括號。"

透過選取 **傳送時間最佳化** 從活動參數切換。

![](../building-journeys/assets/jo-message5.png)

對於電子郵件訊息，請選取適當的選項按鈕，以選擇要最佳化電子郵件開啟次數還是電子郵件點進次數。 推播訊息預設為開啟選項，因為點擊不適用於推播訊息。

您也可以為 **在下一個** 選項。 如果選擇「6小時」作為值， [!DNL Journey Optimizer] 會檢查每個使用者設定檔，並在歷程執行時間起六小時內選取最佳傳送時間。
