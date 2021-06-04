---
title: 開始使用推送設定
description: 了解推播通知資料流程和元件
source-git-commit: 03d003682d796906fcf89af02aa98d549b5214a3
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# 推播通知設定{#get-started-push}

![](assets/do-not-localize/badge.png)

推播通知可協助您隨時與您的行動應用程式使用者聯絡，尤其是當使用者目前未使用您的應用程式時。 推播通知可協助您達成各種使用案例，例如提供服務的更新、要求使用者採取動作、提醒使用者留意新交易等。 裝置平台需要選擇加入，才能讓使用者收到或檢視您的通知。 使用者選擇加入的時機，最早可在應用程式於安裝後首次啟動後，或在後續的工作階段或工作流程中（視適用情況而定）收到。 [!DNL Journey Optimizer] 支援推播通知，並協助您以領先業界的吞吐率傳送高度相關的通知。推播通知可能包括個人化和歷程型內容，以運用您的品牌對Adobe Experience Cloud的資料深入分析。

此頁面將協助您設定及了解[!DNL Journey Optimizer]中推播通知的相關重要服務與工作流程。

## 使用AdobeJourney Optimizer設定推播通知

若要透過AdobeJourney Optimizer傳送推播通知，您需完成下列步驟：

1. 請依照檔案操作，在應用程式中使用[AdobeJourney Optimizer與Adobe Experience Platform Mobile SDK](https://aep-sdks.gitbook.io/docs/beta/adobe-journey-optimizer)進行設定。
1. 建立推送訊息通道](configuration/message-presets.md)的預設集[

## 推播通知與AdobeJourney Optimizer

下圖顯示與相關資料流有關的系統和服務，重點說明如何從端對端服務的角度傳送推播通知。

![](assets/push-flow.png)

1. 在Apple的APN和Google FCM推播訊息服務中註冊您的品牌行動應用程式（Android或iOS）
1. 傳訊服務會產生推播Token，此識別碼AdobeJourney Optimizer將用來透過推播通知鎖定特定裝置。
1. 先前產生的推送代號會傳遞至Adobe Experience Platform，並與即時客戶設定檔同步；這是透過易於整合的用戶端SDK所完成
1. 推送訊息是在AdobeJourney Optimizer中撰寫，推送訊息是根據訊息預設集建立
1. 推送訊息可能包含在歷程的協調畫布上
1. 在歷程發佈時，根據歷程條件的客戶設定檔可符合接收推播通知的資格，在此步驟中會個人化推播訊息裝載
1. 個人化推送裝載會轉送至內部推送訊息傳送服務
1. 然後，此內部服務會驗證與訊息相關聯的應用程式憑證，並
1. 傳送訊息至Apple &amp; Google訊息服務以進行最終傳送
1. 會記錄來自傳訊服務的意見，並記錄錯誤和成功案例，以便在Journey Live &amp; Global報表中報告
1. 推播通知會傳送至一般使用者裝置
1. 一般使用者推播通知互動會透過SDK整合，從一般使用者用戶端以體驗事件的形式傳入

## 推播通知中關鍵服務的角色

* **推播通知服務提** 供者是核心元件web服務，可從遠端伺服器傳送通知至行動應用程式。

   [!DNL Adobe Journey Optimizer]  支援Android和iOS平台，因此可與下列項目整合：
   * [Firebase雲端傳訊(FCM)](https://firebase.google.com/docs/cloud-messaging)  — 傳送通知至Android行動應用程式
   * [Apple推播通知服務(APN)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)  — 傳送通知至iOS行動應用程式

* **Adobe Experience Platform Mobile** SDK，可透過Android和iOS相容的SDK，為您的行動裝置提供用戶端整合API。SDK提供AdobeJourney Optimizer擴充功能，可公開多種專用於推送訊息的API，並啟用資料流，例如註冊推送代號或傳送推送追蹤事件或任何其他自訂體驗事件至Adobe Experience Platform。 SDK也提供多種其他擴充功能，以啟用其他Adobe Experience Cloud和第三方合作夥伴功能。

   SDK整合也需要設定Adobe Experience Platform [資料收集](https://experienceleague.adobe.com/docs/launch/using/home.html)服務，例如：

   * 建立資料流，以設定資料流入Adobe Experience Platform的設定檔和體驗事件資料集
   * 建立用戶端行動屬性並新增擴充功能。 SDK與這些擴充功能緊密整合，提供順暢的資料收集體驗。
   * 註冊行動應用程式套件識別碼和應用程式憑證

* **Adobe Experience Platform即時客戶設**  定檔會結合來自多個管道（包括網路、行動裝置、CRM和協力廠商）的資料，以維護每個客戶的整體檢視。設定檔可讓您將客戶資料併入統一檢視中，提供每個客戶互動的可操作、時間戳記帳戶。 指定應用程式使用者的推送代號會根據使用者的設定檔儲存為記錄資料，而使用者與推送通知的互動則會以時間序列事件資料來追蹤。 [深入了解Adobe Experience Platform Real-time Customer Profile](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)

* **[!DNL Adobe Journey Optimizer]** :在Adobe Experience Platform中部署行動應用程式與上述元件的整合及您的客戶設定檔後，您就可以在Adobe Journey Optimizer中撰寫和協調推播通知，以與使用者互動。

## 推播技術設定與從業人員工作流程

下圖顯示了端對端配置構成推送資料流骨架的元件時涉及的各種步驟。 已根據執行配置的角色和要配置的元件對操作項進行分類。

![](assets/user-flow.png)

