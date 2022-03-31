---
title: 開始使用推播設定
description: 瞭解推送通知資料流和元件
topic: Mobile
feature: Push
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 3%

---

# 開始使用推播設定 {#get-started-push}

此頁將幫助您設定和瞭解與推送通知相關的關鍵服務和工作流 [!DNL Journey Optimizer]。 瞭解如何在中建立推送通知 [此頁](../messages/create-push.md)。

在中配置推送通道的步驟 [!DNL Adobe Journey Optimizer] 詳見 [此頁](push-configuration.md)。

## 推送通知和 [!DNL Adobe Journey Optimizer] {#push-notifications-and-journey-optimizer}

下圖顯示了與關聯資料流相關的系統和服務，突出了從端到端服務的角度提供推送通知的方式。

![](assets/push-flow.png)

1. 在Apple的APNs和GoogleFCM推送消息服務中註冊您的品牌移動應用(Android或iOS)
1. 消息服務生成推令牌，該令牌是 [!DNL Adobe Journey Optimizer] 將用於使用推式通知瞄準特定設備。
1. 先前生成的推令牌被傳遞給Adobe Experience Platform並與即時客戶配置檔案同步；這是通過易於整合的客戶端SDK完成的
1. 推送消息創作於 [!DNL Adobe Journey Optimizer]，根據消息預設建立推送消息
1. 推送消息可能包含在Rougners中的業務流程畫布中
1. 在Journey發佈後，基於Journey條件的客戶配置檔案經鑑定可接收推送通知，推送消息負載在此步驟中個性化
1. 將個性化推送有效載荷轉發到內部推送消息傳遞服務
1. 然後，此內部服務驗證與消息關聯的應用的憑據，並
1. 將消息發送到Apple和Google消息服務以進行最終傳遞
1. 在Journey Live和Global報告中記錄來自消息服務的反饋，記錄錯誤和成功
1. 推送通知被傳送到最終用戶設備
1. 最終用戶推送通知交互通過SDK整合作為體驗事件從最終用戶客戶端發送

## 推送通知中關鍵服務的角色 {#roles-of-key-services}

* **推送通知服務提供程式** 是核心元件Web服務，它將通知從遠程伺服器傳送到移動應用程式。

   [!DNL Adobe Journey Optimizer]  支援Android和iOS平台，因此與以下產品整合：
   * [Firebase雲消息(FCM)](https://firebase.google.com/docs/cloud-messaging)  — 向Android移動應用發送通知
   * [Apple推送通知服務(APN)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)  — 向iOS移動應用發送通知

* **Adobe Experience Platform移動SDK** 它通過Android和iOS相容的SDK為您的手機提供客戶端整合API。 SDK提供 [!DNL Adobe Journey Optimizer] 擴展顯示用於推送消息傳遞的各種特定API，並啟用資料流，如註冊推送令牌或將推送跟蹤事件或任何其他自定義體驗事件發送到Adobe Experience Platform。 SDK還提供了多種其他擴展，可支援其他Adobe Experience Cloud以及第三方合作夥伴功能。

   SDK整合還需要設定Adobe Experience Platform [資料收集](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html){target=&quot;_blank&quot;服務，如：

   * 建立資料流以配置資料流入Adobe Experience Platform的配置檔案和體驗事件資料集
   * 建立客戶端移動屬性並添加擴展。 SDK與這些擴展緊密整合，以提供無縫的資料收集體驗。
   * 註冊移動應用捆綁標識符和應用憑據

* **Adobe Experience Platform即時客戶概要**  通過合併來自多個渠道（包括web 、 mobile 、 CRM和第三方）的資料，維護每個客戶的整體視圖。 配置檔案允許您將客戶資料整合到一個統一視圖中，為每次客戶交互提供一個可操作且時間戳記的帳戶。 將給定應用用戶的推送令牌作為記錄資料根據用戶的配置檔案儲存，同時將用戶與推送通知的交互作為時間序列事件資料進行跟蹤。 [瞭解有關Adobe Experience Platform即時客戶概要資訊的更多資訊](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

* **[!DNL Adobe Journey Optimizer]** :一旦您的移動應用與上述元件的整合到位，並且您的客戶配置檔案在Adobe Experience Platform，您就可以編寫並協調推送通知 [!DNL Adobe Journey Optimizer] 與您的用戶接洽。

## 推送技術設定和從業人員工作流 {#push-technical-setup}

下圖顯示了配置構成推送資料流骨架的元件時涉及的各種步驟。 已根據執行配置的角色和正在配置的元件對措施項進行分類。

![](assets/user-flow.png)
