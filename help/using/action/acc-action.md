---
title: 與 Adobe Campaign v7/v8 整合
description: 瞭解如何與Adobe Campaignv7/v8整合
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 51c63b196b11905289c3c0c450c1976eb551bbc8
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 4%

---

# 與 Adobe Campaign v7/v8 整合 {#integrating-with-adobe-campaign-classic}

此整合適用於從21.1版開始的Adobe Campaign Classicv7和Adobe Campaignv8。 它允許您使用Adobe Campaign事務性消息傳遞功能發送電子郵件、推送通知和簡訊。

Journey Optimizer實例和市場活動實例之間的連接是在預配時通過Adobe設定的。

本中介紹了端到端使用案例 [節](../building-journeys/campaign-classic-use-case.md)。

對於配置的每個操作，行程設計器調色板中都提供一個操作活動。 請參閱此 [節](../building-journeys/using-adobe-campaign-classic.md)。

## 重要備註 {#important-notes}

* 沒有消息限制。 系統根據當前市場活動SLA將可以每5分鐘發送的消息數限制為4000。 因此，Journey Optimizer只應用於單一使用情形（單個事件，而不是分段）。

* 您需要在畫布上根據要使用的模板配置一個操作。 您需要在Journey Optimizer為要從Adobe Campaign使用的每個模板配置一個操作。

* 我們建議您使用為此整合托管的專用消息中心實例，以避免影響您可能正在進行的任何其他活動操作。 營銷伺服器可以托管或內部。 所需的生成是21.1版候選版或更高版本。

* 沒有驗證有效負載或市場活動消息是否正確。

* 您不能將市場活動活動與段資格事件一起使用。

## 先決條件 {#prerequisites}

在市場活動中，您需要建立並發佈事務性消息及其關聯事件。 請參閱 [Adobe Campaign文檔](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target=&quot;_blank&quot;}。

您可以按照以下模式生成與每條消息對應的JSON負載。 然後，在Journey Orchestration中配置操作時將貼上此負載（請參閱下面）

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

* **通道**:為「市場活動」事務模板定義的渠道
* **事件類型**:市場活動活動的內部名稱
* **ctx**:根據您在郵件中的個性化設定來設定變數。

## 配置操作 {#configure-action}

在Journey Optimizer，您需要為每個事務性消息配置一個操作。 執行以下步驟：

1. 建立新操作。 請參閱此 [節](../action/action.md)。
1. 輸入名稱和說明。
1. 在 **操作類型** 欄位，選擇 **Adobe Campaign Classic**。
1. 按一下 **負載** 欄位並貼上與市場活動消息對應的JSON負載示例。 聯繫Adobe獲取此負載。
1. 根據要在「旅程」畫布上映射不同欄位，將其調整為靜態或變數。 某些欄位(如電子郵件地址的通道參數和個性化欄位(ctx))，您可能需要定義為旅行上下文中映射的變數。
1. 按一下「**儲存**」。

![](assets/accintegration1.png)
