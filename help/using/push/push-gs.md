---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer中的推播通知流程
description: 瞭解推播通知資料流程和元件
topic: Mobile
feature: Push, Overview
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 5758c9db8b1b12367126f4adb8bd1c0bac766514
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 1%

---

# 推播通知資料流程和元件 {#get-started-push}

此頁面可協助您設定並瞭解[!DNL Journey Optimizer]中推播通知的相關重要服務與工作流程。


>[!AVAILABILITY]
>
>全新&#x200B;**行動入門快速入門工作流程**&#x200B;現已推出。 使用這項新產品功能，快速設定行動SDK，以開始收集和驗證行動事件資料，並傳送行動推播通知。 此功能可作為公開測試版透過Data Collection首頁存取。 [了解更多](mobile-onboarding-wf.md)
>

瞭解如何在[此頁面](create-push.md)上建立推播通知。

在[!DNL Adobe Journey Optimizer]中設定推播頻道的步驟已詳載於[此頁面](push-configuration.md)。

下圖顯示與相關資料流程相關的系統和服務，重點說明如何從端對端服務角度傳送推播通知。

![](assets/push-flow.png)

1. 透過Apple的APN和Google FCM推送訊息服務註冊品牌行動應用程式(Android或iOS)
1. 訊息服務會產生推播權杖，這是[!DNL Adobe Journey Optimizer]將用來以推播通知鎖定特定裝置的識別碼。
1. 先前產生的推播權杖會傳遞至Adobe Experience Platform並與即時客戶個人檔案同步；這是透過易於整合的使用者端SDK在OOTB中完成

   >[!NOTE]
   >
   >不同平台的Token處理方式不同。 在&#x200B;**Android (FCM)**&#x200B;上，當使用者清除應用程式快取或重新安裝應用程式，產生新的權杖和ECID時，權杖會自動標示為無效。 在&#x200B;**iOS (APN)**&#x200B;上，Token在這些情況下不會一致地被標籤為無效。 如果設定檔包含多個具有有效權杖的ECID，則會將推播通知傳送至所有關聯的裝置。

1. 推送訊息是在[!DNL Adobe Journey Optimizer]中製作，推送訊息是根據頻道設定（即訊息預設集）建立
1. 推播訊息可包含在歷程中的協調畫布上
1. 在歷程發佈後，根據歷程條件的客戶設定檔符合接收推播通知的資格，在此步驟中推播訊息負載會個人化
1. 個人化推播裝載會轉送至內部推播訊息傳遞服務
1. 此內部服務接著會驗證與訊息相關聯之應用程式的認證，並且
1. 傳送訊息至Apple與Google訊息服務，以進行最終傳送
1. 訊息服務的意見反應會被記錄，錯誤和成功則會記錄在Journey Live和Customer Journey Analytics報告中
1. 推播通知會傳送至一般使用者裝置
1. 一般使用者推播通知互動會透過SDK整合，從一般使用者使用者端以體驗事件的形式傳送

## 推送通知中重要服務的角色 {#roles-of-key-services}

* **推播通知服務提供者**&#x200B;是從遠端伺服器傳送通知到行動應用程式的核心元件Web服務。

  [!DNL Adobe Journey Optimizer]同時支援Android和iOS平台，因此將與下列專案整合：
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) — 傳送通知給Android行動應用程式
   * [Apple推播通知服務(APN)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) — 傳送通知給iOS行動應用程式

* **Adobe Experience Platform Mobile SDK**，可透過Android與iOS相容的SDK，為您的行動裝置提供使用者端整合API。 SDK提供[!DNL Adobe Journey Optimizer]擴充功能，公開各種推送訊息專屬的API，並啟用資料流程，例如註冊推送代號或傳送推送追蹤事件或任何其他自訂體驗事件至Adobe Experience Platform。 SDK還提供多種其他擴充功能，以啟用其他Adobe Experience Cloud以及第三方合作夥伴功能。

  SDK整合也需要設定Adobe Experience Platform [資料收集](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hant){target="_blank"}服務，例如：

   * 建立資料串流，以設定資料據以流入Adobe Experience Platform的設定檔和體驗事件資料集
   * 建立使用者端行動屬性並新增擴充功能。 SDK與這些擴充功能緊密整合，以提供順暢的資料收集體驗。
   * 註冊行動應用程式套件組合識別碼和應用程式認證

* **Adobe Experience Platform即時客戶設定檔**&#x200B;透過合併來自多個管道（包括Web、行動裝置、CRM和協力廠商）的資料，維護每個個別客戶的整體檢視。 設定檔可讓您將客戶資料合併成統一的檢視畫面，針對每個客戶互動提供可採取行動且附有時間戳記的說明。 特定應用程式使用者的推播權杖會針對使用者的設定檔儲存為記錄資料，而使用者對推播通知所做的互動則會追蹤為時間序列事件資料。 [進一步瞭解Adobe Experience Platform即時客戶個人檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}。

* **[!DNL Adobe Journey Optimizer]** ：一旦您的行動應用程式與上述元件整合就緒，且您的客戶設定檔位於Adobe Experience Platform中，您即可在[!DNL Adobe Journey Optimizer]中製作及協調推播通知，以便與使用者互動。

## 推播技術設定和從業人員工作流程 {#push-technical-setup}

下圖顯示設定構成推送資料流程骨架的元件所涉及的各種端對端步驟。 已根據執行設定的角色和正在設定的元件，將行動專案分類。

![](assets/user-flow.png)

**相關主題**

* [設定推播頻道](push-configuration.md)
* [推播通知報告](../reports/journey-global-report-cja-push.md)
* [建立推播通知](create-push.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [在行銷活動中新增訊息](../campaigns/create-campaign.md)