---
solution: Journey Optimizer
product: journey optimizer
title: 檢閱及啟動行銷活動
description: 瞭解如何在Journey Optimizer中檢閱及啟用行銷活動
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: 行銷活動，檢閱，驗證，啟用，啟用，最佳化工具
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: 1d3638499a9e8261a5f1b09744b82642198a5d5d
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 3%

---


# 執行API觸發的行銷活動 {#execute}

啟動行銷活動後，您需要擷取產生的範例cURL請求，並將其用於API中以建置您的裝載並觸發行銷活動。

## 必讀 {#must-read}

* **行銷活動開始/結束日期** — 如果您在建立行銷活動時已設定特定的開始和/或結束日期，則不會在這些日期之外執行，且API呼叫將會失敗。

* **呼叫逾時** — 對互動式訊息執行REST API的呼叫逾時60秒。 不過，萬一發生未預期的逾時情況，內部會重試以保證傳遞。

## 觸發行銷活動 {#trigger}

1. 開啟行銷活動，然後從&#x200B;**[!UICONTROL cURL請求]**&#x200B;區段複製並貼上裝載請求。 此裝載包含訊息中使用的所有個人化（設定檔和內容）變數。 行銷活動上線後，即可使用此功能。

   ![](assets/api-triggered-curl.png)

1. 將此cURL請求用於API以建置您的裝載並觸發行銷活動。 如需詳細資訊，請參閱[互動式訊息執行API檔案](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)。

   [此頁面](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/)上也提供API呼叫範例。
