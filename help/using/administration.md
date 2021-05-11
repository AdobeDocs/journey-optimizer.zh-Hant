---
title: 技術設定
description: 瞭解管理與設定准則
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 7%

---

# 技術設定

![](assets/do-not-localize/badge.png)

## 設定品牌參數{#cjm-branding}

每家公司都有品牌視覺化與技術準則。您可以定義一組規格，為客戶呈現一致的品牌，從標誌到技術層面，例如電子郵件傳送者、鏡像頁面URL的網域或訊息追蹤設定。
用戶不能建立或修改品牌：此配置由Adobe管理。

要為[!DNL Journey Optimizer]實例設定品牌參數，您需要聯繫Adobe並共用以下詳細資訊：

* 公司名稱

* 寄件者（寄件者）電子郵件地址

* 發件人（發件人）名稱

* 回覆地址

在設定品牌參數後，您就可以在建立訊息時加以選取。

在配置了品牌參數後，從&#x200B;**[!UICONTROL Presets]**&#x200B;清單中建立消息時，您將能夠選擇這些參數。 [進一步瞭解內容建立](create-message.md)。

## 設定推播通知頻道

瞭解如何在此[區段](configure-push.md)中設定推播頻道。

## 子域委派

對於要用於[!DNL Journey Optimizer]的任何新子域，第一步是將其委派。 您需要與Adobe技術聯絡。

實施解決方案時，對外部元件有以下要求：這些功能包括設定要追蹤的連結和網頁、顯示鏡像頁面等。

雖然這些需求是透過Adobe和客戶托管的元件來管理，但它們包含URL，讓電子郵件的收件者可以看到。  為避免URL顯示基礎技術解決方案或代管供應商，可以設定子網域，讓電子郵件的收件者能夠透明化此URL。

在這些委派後，Adobe建立的基礎架構可確保對每個委派或基於CNAME的發送域執行以下服務：

* 建立postmaster@和ubuse@ inbox

* 為委託域設定反饋環

* 基本DMARC記錄設定

由Adobe建立的參數僅在完成委託後由Adobe驗證時有效，並且仍然有效。

[進一步瞭解網域委派](https://helpx.adobe.com/tw/campaign/kb/domain-name-delegation.html)。


## 建立資料來源、事件和動作

使用&#x200B;**[!UICONTROL Admin]**&#x200B;部分管理&#x200B;**[!UICONTROL Data Sources]**、**[!UICONTROL Events]**&#x200B;和&#x200B;**[!UICONTROL Actions]**。

![](assets/admin-menu.png)

### 資料來源

「資料來源」設定可讓您定義系統連線，以擷取將用於歷程的其他資訊。

在此[節](../using/datasource/about-data-sources.md)中進一步瞭解Data Sources

### 事件

事件可讓您觸發整個旅程，以即時傳送訊息給流入旅程的個人。

在事件設定中，您可設定預期於歷程中的事件。 傳入事件的資料會依照Adobe Experience Data Model(XDM)進行標準化。 事件來自串流獲取 API，適用於驗證和未驗證的事件（例如 Adobe Mobile SDK 事件）。

進一步瞭解此[節](../using/event/about-events.md)中的事件

### 動作

[!DNL Journey Optimizer] 消息功能是內置的：您只需要設計內容並發佈訊息。如果您使用協力廠商系統來傳送訊息，可以建立自訂動作。

進一步瞭解此[節](../using/action/action.md)中的動作
