---
title: 建立收件匣
description: 開始使用 Adobe Journey Optimizer 中的收件匣，以傳送永久、非侵入式訊息給您的使用者。
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 92%

---

# 開始使用收件匣 {#inbox-gs}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解收件匣通道如何讓行銷訊息保留在應用程式或網站內的一個固定位置，方便使用者返回閱讀並採取行動。

>[!ENDSHADEBOX]

收件匣會在您行動應用程式或網站內的單一位置傳送持續性、低摩擦的訊息。 應用程式內及推播在滑動或點選後可能會消失；收件匣可保持訊息可用，方便使用者在適合時開啟、閱讀及操作。

收件匣建立在內容卡管道上，並新增：

* **持續性訊息**：內容會保留在收件匣中，直到您移除它或它過期為止，因此使用者可以在關閉通知或離開應用程式後返回收件匣查看。
* **集中式位置**：應用程式或網站中用於相關行銷訊息的單一郵箱。
* **彈性的實作**：使用現成的收件匣容器，或在您自己的 UI 中量身打造體驗。
* **讀取狀態**：可在開啟訊息的裝置上將訊息標記為已讀取或未讀取。

## 快速入門手冊

請依照下列步驟設定並使用收件匣：

1. [設定 Adobe Journey Optimizer](inbox-configuration.md)

   在&#x200B;**管道設定**&#x200B;下新增&#x200B;**收件匣**&#x200B;管道設定，讓 Journey Optimizer 知道收件匣在何處執行以及如何執行 (網頁或規則，或行動應用程式介面)。

1. [在 Journey Optimizer 中建立收件匣](inbox-create.md)

   建立使用&#x200B;**內容卡**&#x200B;動作的行銷活動，並選擇&#x200B;**收件匣**&#x200B;作為傳遞位置，已從 UI 排程或由 API 觸發。

1. [設計您的收件匣](inbox-design.md)

   挑選收件匣範本和清單或展開版面，讓訊息符合您的品牌和 UX。

1. [建立內容卡並將其連結至您的收件匣](../content-card/create-content-card.md)

   在設計工具中製作卡片內容、完成收件匣特定選項，然後啟動您的行銷活動，使訊息可送達收件匣。

## 其他資源

* [收件匣 UI (iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS)：透過 Adobe Experience Platform Mobile SDK (iOS 15 或更新版本、Xcode 15 或更新版本、Swift 5.1 或更新版本) 在 iOS 應用程式中實作 Journey Optimizer 收件匣的需求、公用 API 介面、收件匣設定，以及教學課程連結。

* [擷取及顯示收件匣](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox)：載入 Journey Optimizer 收件匣訊息，並在 Android 上轉譯收件匣 UI (Adobe Developer 文件)。

* [自訂收件匣](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox)：調整 Android 應用程式的收件匣版面配置、樣式和互動行為 (Adobe Developer 文件)。

* [聆聽收件匣事件](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events)：訂閱 Android 上的使用者動作和生命週期更新的收件匣回呼 (Adobe Developer 文件)。
