---
solution: Journey Optimizer
product: journey optimizer
title: 與 Adobe Campaign v7/v8 整合
description: 瞭解如何將Journey Optimizer與Adobe Campaign v7/v8整合
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campaign， acc，整合
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: ffce95a074c5827b637d081ad23f4cd3754515fe
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 17%

---

# 與 Adobe Campaign v7/v8 整合 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Adobe Campaign v7/v8 動作"
>abstract="此整合適用於 Adobe Campaign v7 和 v8。這可讓您使用 Adobe Campaign 交易型訊息功能來傳送電子郵件、推播通知及簡訊。Journey Optimizer 和 Campaign 執行個體之間的連線在佈建時由 Adobe 設定。"

您的歷程中提供特定的自訂動作，以整合Adobe Journey Optimizer和Adobe Campaign v7/v8。

此整合適用於Adobe Campaign v7/v8的7.1發行版本，以及Adobe Campaign v8。 這可讓您使用 Adobe Campaign 交易型訊息功能來傳送電子郵件、推播通知及簡訊。

此[區段](../building-journeys/ajo-ac.md)中呈現端對端使用案例。

對於已設定的每個動作，歷程設計器浮動視窗中都提供動作活動。 請參閱本[章節](../building-journeys/using-adobe-campaign-v7-v8.md)。

## 存取 {#access}

Journey Optimizer與Campaign執行個體之間的連線在布建時由Adobe依請求設定。 如果您在布建時尚未要求連線，請聯絡Adobe Journey Optimizer支援，提供下列詳細資料以請求啟用：

從Adobe Journey Optimizer：

* 組織ID (Adobe OrgID)
* 沙箱

從Adobe Campaign：

* 促銷活動URL
* RT URL
* Campaign 版本

## 重要備註 {#important-notes}

* 沒有訊息限制。 根據目前的Campaign SLA，系統會將每5分鐘可傳送超過4000則的訊息數量限制在最高。 因此，Journey Optimizer應僅用於單一使用案例（個別事件，而非對象）。

* 您必須針對要使用的每個範本，在畫布上設定一個動作。 您需要在Journey Optimizer中，為您要從Adobe Campaign使用的每個範本設定一個動作。

* 建議您使用針對這項整合而託管的專用訊息中心執行個體，以避免影響您可能正在進行的任何其他行銷活動作業。 行銷伺服器可以是託管式或內部部署。 所需的組建版本是21.1版本候選版本或更新版本。

* 沒有驗證裝載或行銷活動訊息是否正確。

* 行銷活動動作無法與對象資格事件搭配使用。

## 先決條件 {#prerequisites}

在Campaign中，您需要建立並發佈交易式訊息及其相關事件。 請參閱[Adobe Campaign檔案](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target="_blank"}。

您可以依照以下模式，建置與每則訊息相對應的JSON裝載。 之後，當您在Journey Optimizer中設定動作時，就會貼上此裝載（請參閱下文）

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

* **頻道**：為您的Campaign交易範本定義的頻道
* **eventType**：您的行銷活動事件的內部名稱
* **ctx**：變數，根據您訊息中的個人化設定而定。

## 設定動作 {#configure-action}

在Journey Optimizer中，您需為每個異動訊息設定一個動作。 請依照下列步驟操作：

1. 建立新動作。 請參閱本[章節](../action/action.md)。
1. 輸入名稱和說明。
1. 在&#x200B;**動作型別**&#x200B;欄位中，選取&#x200B;**Adobe Campaign Classic**。
1. 按一下&#x200B;**裝載**&#x200B;欄位，然後貼上與Campaign訊息相對應的JSON裝載範例。 聯絡Adobe以取得此裝載。
1. 視您想要在歷程畫布上對應欄位，將不同的欄位調整為靜態或變數。 某些欄位，例如電子郵件地址和個人化欄位(ctx)的管道引數，您可能會想要定義為歷程內容中對應的變數。
1. 按一下&#x200B;**儲存**。

![](assets/accintegration1.png)