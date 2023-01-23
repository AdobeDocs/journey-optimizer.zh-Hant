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
ht-degree: 1%

---

# 傳送時間最佳化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="關於傳送時間最佳化"
>abstract="Adobe Journey Optimizer的「傳送時間最佳化」功能採用Adobe的AI服務，可根據歷史開啟率和點按率，預測傳送電子郵件或推送訊息的最佳時機，以最大化參與。"

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

## 啟動傳送時間最佳化{#activate-send-time-optimization}

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
