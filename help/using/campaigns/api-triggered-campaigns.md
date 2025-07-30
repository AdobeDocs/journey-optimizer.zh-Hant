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
source-git-commit: 15f5fdfde0e9f7c93739a624918838dbd6787833
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 26%

---


# 使用 API 觸發的行銷活動 {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="API 觸發的行銷活動"
>abstract="**交易型 API 觸發的行銷活動**<br/>&#x200B;透過 API 呼叫觸發即時訊息&#x200B;<br/><br/>**行銷訊息**<br/>&#x200B;促銷內容 (需要選擇加入，並遵循業務規則)<br/><br/>**交易型訊息**<br/>&#x200B;服務相關內容 (確認、提醒，無需獲得行銷同意)<br/><br/>**可用管道**<br/>&#x200B;電子郵件、簡訊、推播通知"

## 關於API觸發的行銷活動 {#about}

API觸發的行銷活動可讓行銷通訊在適當的時間聯絡對象，或讓交易/營運訊息聯絡個人（例如密碼重設），其需求可能涉及個人化，不僅使用設定檔屬性，還會在觸發程式（即REST API裝載）中使用即時內容資料。

若要這麼做，您必須先在Journey Optimizer中建立API觸發的行銷活動，然後使用[互動式訊息執行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution)，透過API呼叫來啟動其執行。

API觸發的行銷活動的可用管道包括電子郵件、簡訊和推播訊息。

➡️ [在影片中探索此功能](#video)

## API觸發的行銷活動建立的關鍵步驟 {#steps}

1. [定義行銷活動屬性](api-triggered-campaign-properties.md)
1. [設定行銷活動動作](api-triggered-campaign-action.md)
1. [編輯行銷活動內容](api-triggered-campaign-content.md)
1. [定義行銷活動對象](api-triggered-campaign-audience.md)
1. [排程行銷活動](api-triggered-campaign-schedule.md)
1. [檢閱及啟動行銷活動](review-activate-api-triggered-campaign.md)
1. [觸發行銷活動執行](trigger-campaigns.md)

## 作法影片 {#video}

瞭解如何使用互動式訊息執行REST API，根據使用者互動從外部系統建立及觸發行銷活動。

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
