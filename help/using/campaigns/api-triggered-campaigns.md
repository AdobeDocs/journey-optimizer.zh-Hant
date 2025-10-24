---
solution: Journey Optimizer
product: journey optimizer
title: 使用 API 觸發的行銷活動
description: 瞭解如何使用Journey Optimizer API觸發行銷活動。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 行銷活動， API觸發， REST，最佳化工具，訊息
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 35%

---


# 使用 API 觸發的行銷活動 {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="由 API 觸發的行銷活動"
>abstract="**交易型 API 觸發的行銷活動**<br/>&#x200B;透過 API 呼叫觸發即時訊息&#x200B;<br/><br/>**行銷訊息**<br/>&#x200B;促銷內容 (需要選擇加入，並遵循業務規則)<br/><br/>**交易型訊息**<br/>&#x200B;服務相關內容 (確認、提醒，無需獲得行銷同意)<br/><br/>**可用管道**<br/>&#x200B;電子郵件、簡訊、推播通知"

## 關於API觸發的行銷活動 {#about}

API觸發的行銷活動可讓行銷通訊在適當的時間聯絡對象，或讓交易/營運訊息聯絡個人，例如重設密碼，其中需求可能涉及使用設定檔屬性以及觸發程式中的即時內容資料（即REST API裝載）的個人化。

若要這麼做，您必須先在Journey Optimizer中建立API觸發的行銷活動，然後使用[互動式訊息執行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)，透過API呼叫來啟動其執行。

➡️ [在影片中探索此功能](#video)

>[!NOTE]
>
>支援的頻道為： [電子郵件](../email/get-started-email.md)、[簡訊](../sms/get-started-sms.md)、[推播通知](../push/get-started-push.md)。 高輸送量API觸發的行銷活動目前僅支援電子郵件頻道。
>
>可用的通道因您的授權模式及附加元件而異。

## API觸發的行銷活動建立的關鍵步驟 {#steps}

開始行銷活動之前，請檢查本節[中列出的下列必要條件](get-started-with-campaigns.md#permissions)。 在滿足這些先決條件後，您就可以開始建立行銷活動：

1. [定義行銷活動屬性](api-triggered-campaign-properties.md)
1. [設定行銷活動動作](api-triggered-campaign-action.md)
1. [編輯行銷活動的內容](api-triggered-campaign-content.md)
1. [定義行銷活動的客群](api-triggered-campaign-audience.md)
1. [安排行銷活動](api-triggered-campaign-schedule.md)
1. [審閱並啟動行銷活動](review-activate-api-triggered-campaign.md)
1. [觸發行銷活動執行](trigger-campaigns.md)

## 作法影片 {#video}

瞭解如何使用互動式訊息執行REST API，根據使用者互動從外部系統建立及觸發行銷活動。

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
