---
title: 傳送時間最佳化
description: 瞭解如何在消息中參數化發送時間優化
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 1%

---

## 傳送時間最佳化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="關於發送時間優化"
>abstract="Adobe Journey Optimizer的「發送時間優化」功能由Adobe的AI服務提供支援，可以根據歷史開啟和點擊率預測發送電子郵件或推送消息的最佳時間，以最大限度地提高參與度。"

Adobe Journey Optimizer的「發送時間優化」功能由Adobe的AI服務提供支援，可以根據歷史開啟和點擊率預測發送電子郵件或推送消息的最佳時間，以最大限度地提高參與度。 使用我們的機器學習模型為每個用戶安排個性化發送時間，以增加消息的開啟和點擊率。

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

### 激活發送時間優化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="激活發送時間優化"
>abstract="選擇是開啟電子郵件時進行優化，還是通過選擇相應的單選按鈕進行電子郵件點擊瀏覽。 您也可以通過在下一個選項中輸入「發送」值來選擇對系統使用的發送時間進行標籤。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="激活發送時間優化"
>abstract="推送消息預設為開啟選項，因為按一下不適用於推送消息。 您也可以通過在下一個選項中輸入「發送」值來選擇對系統使用的發送時間進行標籤。"

通過選擇 **發送時間優化** 從活動參數中切換。

![](../building-journeys/assets/jo-message5.png)

對於電子郵件，選擇是開啟電子郵件時進行優化，還是通過選擇相應的單選按鈕進行電子郵件點擊瀏覽。 推送消息預設為開啟選項，因為按一下不適用於推送消息。

您也可以通過為 **在下一個** 的雙曲餘切值。 如果你選擇&quot;六小時&quot;作為值， [!DNL Journey Optimizer] 將檢查每個用戶配置檔案，並在行程執行時間後六小時內選擇最佳發送時間。
