---
title: 技術設定
description: 了解管理與設定准則
hidefromtoc: true
hide: true
feature: 應用程式設定
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 8%

---

# 技術設定

![](../assets/do-not-localize/badge.png)

## 設定品牌參數{#cjm-branding}

每家公司都有品牌視覺化與技術準則。您可以定義一組規格，為客戶呈現一致的品牌，從標誌到技術層面，例如電子郵件寄件者、鏡像頁面URL的網域或訊息追蹤設定。
最終用戶無法建立或修改品牌：此設定由Adobe管理。

若要為[!DNL Journey Optimizer]實例設定品牌參數，您需要聯繫Adobe並共用以下詳細資訊：

* 公司名稱

* 發件人（發件人）電子郵件地址

* 發件人（發件人）名稱

* 回復地址

設定品牌參數後，您就能在建立訊息時選取參數。

設定品牌參數後，從&#x200B;**[!UICONTROL Presets]**&#x200B;清單建立訊息時，您便能選取這些參數。 [深入了解內容建立](../create-message.md)。

## 設定推播通知通道

了解如何在此[區段](../create-push.md)中設定推播通道。

## 子網域委派

對於要在[!DNL Journey Optimizer]中使用的任何新子網域，第一步是委派它。 您需要聯絡您的Adobe技術聯絡人。

實施解決方案時，對外部元件有以下要求：包括設定要追蹤的連結和網頁、顯示鏡像頁面等。

雖然這些需求是透過Adobe和客戶托管的元件來管理，但其中包含URL，可供電子郵件的收件者看到。  為避免有指出基礎技術解決方案或托管提供者的URL，您可以設定子網域，讓這對電子郵件的收件者透明。

在這些委派後，由Adobe建立的基礎架構可確保為每個委派或基於CNAME的傳送網域執行下列服務：

* 建立Postmaster@和Ubuse@收件箱

* 為委派的域設定反饋循環

* 基本DMARC記錄配置

由Adobe建立的參數僅從完成委派後，再由Adobe驗證時有效，並且保持正常。

[深入了解網域委派](https://helpx.adobe.com/tw/campaign/kb/domain-name-delegation.html)。


## 建立資料來源、事件和動作

使用&#x200B;**[!UICONTROL Admin]**&#x200B;區段管理&#x200B;**[!UICONTROL Data Sources]**、**[!UICONTROL Events]**&#x200B;和&#x200B;**[!UICONTROL Actions]**。

![](../assets/admin-menu.png)

### 資料來源

資料來源設定可讓您定義系統連線，以擷取將用於歷程的其他資訊。

在此[小節](../datasource/about-data-sources.md)了解更多資料來源

### 事件

事件可讓您整體觸發歷程，以即時傳送訊息給流入歷程的個人。

在事件設定中，您會設定歷程中預期的事件。 會依照Adobe Experience Data Model(XDM)，對傳入事件的資料進行標準化。 事件來自串流獲取 API，適用於驗證和未驗證的事件（例如 Adobe Mobile SDK 事件）。

進一步了解此[小節](../event/about-events.md)中的事件

### 動作

[!DNL Journey Optimizer] 訊息功能已內建：您只需要設計內容並發佈訊息。如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。

進一步了解此[小節](../action/action.md)中的動作
