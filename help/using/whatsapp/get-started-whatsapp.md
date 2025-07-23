---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 WhatsApp 訊息
description: 了解如何在 Journey Optimizer 建立及傳送 WhatsApp 訊息
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
source-git-commit: 7f507dc0113e85191429c2c48b873112b590e3ce
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 55%

---

# 開始使用 WhatsApp 訊息 {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**目錄**

* **[開始使用 WhatsApp 訊息](get-started-whatsapp.md)**
* [開始使用 WhatsApp 設定](whatsapp-configuration.md)
* [建立 WhatsApp 訊息](create-whatsapp.md)
* [檢查並傳送 WhatsApp 訊息](send-whatsapp.md)

>[!ENDSHADEBOX]

您現在可以透過Meta的[雲端API](https://developers.facebook.com/docs/whatsapp/cloud-api/)，直接透過Journey Optimizer傳送WhatsApp訊息。 此功能可將WhatsApp緊密整合至歷程和行銷活動，加強與收件者的溝通和參與。

* 在&#x200B;**歷程**&#x200B;中。建立歷程、新增 **WhatsApp** 活動及定義基本設定，然後瀏覽至&#x200B;**[!UICONTROL 動作：WhatsApp]** 右窗格以建立 WhatsApp 訊息的內容。請在[此頁面](../building-journeys/journey-gs.md)進一步了解如何建立歷程。

* 在&#x200B;**行銷活動**&#x200B;中。建立行銷活動，選取 **WhatsApp** 作為您的動作並定義基本設定，然後編輯訊息內容以定義要傳送的 WhatsApp 訊息。請在[此頁面](../campaigns/create-campaign.md#configure)了解如何建立行銷活動。

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## 先決條件 {#prereq}

將 WhatsApp 與 Journey Optimizer 整合需要下列項目：

* Meta 企業管理員帳戶
* WhatsApp 企業帳戶
* WhatsApp 電話號碼
* [具有適當許可權的使用者授權權杖](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [核准的 Meta 範本](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)
* [Meta Webhook的設定](https://developers.facebook.com/docs/whatsapp/webhooks/)


在繼續整合之前，您還需要瞭解下列內容：

* [WhatsApp 內容規則](https://www.whatsapp.com/legal/messaging-guidelines)
* [遵守 Meta 原則](https://www.whatsapp.com/legal)
* [24 小時交談限制](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## 限制 {#limitations}

下列限制適用於WhatsApp頻道：

* Adobe Journey Optimizer中的WhatsApp頻道已可使用HIPAA，但協力廠商未納入Adobe的BAA。 客戶需自行負責法規遵循及廠商驗證。

* 請注意，不支援自動或預先定義的回應訊息。

* 自2025年4月起，針對擁有美國電話號碼（由+1撥號代碼和美國區碼所組成的號碼）的WhatsApp使用者，所有行銷範本訊息的傳送已暫時暫停。 [在中繼檔案中進一步瞭解](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* 原生整合功能不允許與協力廠商商務服務提供者(BSP)整合。

## 作法影片 {#video}


以下影片說明如何使用 WhatsApp 動作建立歷程。

+++ 請觀看影片

>[!VIDEO](https://video.tv.adobe.com/v/3451621?learn=on)

+++
