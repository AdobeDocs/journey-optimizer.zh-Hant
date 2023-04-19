---
solution: Journey Optimizer
product: journey optimizer
title: 與 Adobe Campaign v7/v8 整合
description: 了解如何將Journey Optimizer與Adobe Campaign v7/v8整合
feature: Actions
topic: Administration
role: Admin,Developer
level: Intermediate
keywords: campaign, acc，整合
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 20%

---

# 與 Adobe Campaign v7/v8 整合 {#integrating-with-adobe-campaign-classic}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Adobe Campaign v7/v8 動作"
>abstract="此整合適用於 Adobe Campaign Classic v7 和 v8。這可讓您使用 Adobe Campaign 異動訊息功能來傳送電子郵件、推播通知及 SMS。Journey Optimizer 和 Campaign 執行個體之間的連線在佈建時由 Adobe 設定。"

此整合適用於從7.1版開始的Adobe Campaign Classic v7和Adobe Campaign v8。 這可讓您使用 Adobe Campaign 異動訊息功能來傳送電子郵件、推播通知及 SMS。

Journey Optimizer 和 Campaign 執行個體之間的連線在佈建時由 Adobe 設定。

本節提供端對端使用案例 [節](../building-journeys/ajo-ac.md).

對於已設定的每個動作，歷程設計器浮動視窗中都會提供動作活動。 請參閱 [節](../building-journeys/using-adobe-campaign-classic.md).

## 重要備註 {#important-notes}

* 消息沒有限制。 根據目前的促銷活動SLA，系統將可傳送的訊息數量上限為每5分鐘4000個。 因此，Journey Optimizer僅應用於單一使用案例（個別事件，而非區段）。

* 您需要針對要使用的範本，在畫布上設定一個動作。 您需要在Journey Optimizer中，針對每個要從Adobe Campaign使用的範本設定一個動作。

* 建議您使用為此整合托管的專用訊息中心例項，以避免影響您可能進行的任何其他Campaign作業。 行銷伺服器可托管或內部部署。 所需的版本編號為21.1 Release Candiate或更高版本。

* 裝載或促銷活動訊息正確無誤。

* 您無法搭配區段資格事件使用促銷活動動作。

## 先決條件 {#prerequisites}

在Campaign中，您需要建立並發佈交易式訊息及其相關事件。 請參閱 [Adobe Campaign檔案](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target="_blank"}.

您可以依照下列模式，建立與每個訊息對應的JSON裝載。 然後您會在Journey Optimizer中設定動作時貼上此裝載（請參閱下方）

其範例如下：

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **頻道**:為您的Campaign交易範本定義的管道
* **eventType**:促銷活動事件的內部名稱
* **ctx**:變數。

## 設定動作 {#configure-action}

在Journey Optimizer中，您需要為每個交易式訊息設定一個動作。 請依照下列步驟操作：

1. 建立新動作。 請參閱 [節](../action/action.md).
1. 輸入名稱和說明。
1. 在 **動作類型** 欄位，選擇 **Adobe Campaign Classic**.
1. 按一下 **裝載** 欄位，並貼上與促銷活動訊息對應之JSON裝載的範例。 請聯絡Adobe以取得此裝載。
1. 視您要在歷程畫布上對應不同欄位，將其調整為靜態或變數。 某些欄位(例如電子郵件地址和個人化欄位(ctx)的管道參數)，您可能會想要定義為要在歷程內容中對應的變數。
1. 按一下&#x200B;**儲存**。

![](assets/accintegration1.png)
