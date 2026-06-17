---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 17%

---
未授與Wiki工具許可權。 我會繼續使用票證本身的詳細資訊，其中包含關鍵規格（透過效能附加元件的500 TPS預設值、1000/1500 TPS層級、僅推播、支援高載/有限期間增加）。

---

解決方案： Journey Optimizer
product： journey optimizer
title：搭配使用API觸發的行銷活動
description：瞭解如何使用Journey Optimizer API觸發行銷活動。
功能： Campaigns， API
主題：內容管理
角色：開發人員
level： Experience
關鍵字：促銷活動、API觸發、REST、最佳化工具、訊息
exl-id： 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID： https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2：
- id： cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label： Journey Optimizer
feature_v2：
- id： a653cc2e-bc85-4353-a306-399e5b247978
internal-label： Journey Optimizer促銷活動
subfeature_v2：
- id： f7479fa1-474b-479d-8c98-f6cee5865a38
內部標籤： API觸發的行銷活動
- id： ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label：行銷活動管理
role_v2：
- id： ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label：開發人員
topic_v2：
- id： e0eb8757-182f-49f3-94a4-1587d16f5094
internal-label： Personalization

以下是完整的更新Markdown檔案：

---

```
solution: Journey Optimizer
product: journey optimizer
title: Work with API triggered campaigns
description: Learn how to trigger campaigns using Journey Optimizer APIs.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campaigns, API-triggered, REST, optimizer, messages
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
    internal-label: Journey Optimizer campaigns
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
    internal-label: API triggered campaigns
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
    internal-label: Campaign management
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
```

# 使用 API 觸發的行銷活動 {#trigger-campaigns}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;透過REST API呼叫建立並啟動API觸發的行銷活動，以便您可以使用設定檔和內容資料傳送即時行銷和異動訊息。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="由 API 觸發的行銷活動"
>abstract="**交易型 API 觸發的行銷活動**<br/>&#x200B;透過 API 呼叫觸發即時訊息&#x200B;<br/><br/>**行銷訊息**<br/>&#x200B;促銷內容 (需要選擇加入，並遵循業務規則)<br/><br/>**交易型訊息**<br/>&#x200B;服務相關內容 (確認、提醒，無需獲得行銷同意)<br/><br/>**可用管道**<br/>&#x200B;電子郵件、簡訊、推播通知"

## 關於API觸發的行銷活動 {#about}

API觸發的行銷活動可讓行銷通訊在適當的時間聯絡對象，或讓交易/營運訊息聯絡個人，例如重設密碼，其中需求可能涉及使用設定檔屬性以及觸發程式中的即時內容資料（即REST API裝載）的個人化。

若要這麼做，您必須先在Journey Optimizer中建立API觸發的行銷活動，然後使用[互動式訊息執行REST API](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution)，透過API呼叫來啟動其執行。

➡️ [在影片中探索此功能](#video)

>[!NOTE]
>
>如需支援管道的詳細資訊，請參閱本節中的表格：[歷程與行銷活動中的管道](../channels/gs-channels.md#channels)。
>
>可用的通道因您的授權模式及附加元件而異。

## 推播通知輸送量 {#push-throughput}

根據預設，API觸發的行銷活動支援推播通知傳遞的每秒最多&#x200B;**500個交易(TPS)**。 具有大量作業傳訊需求的組織可透過&#x200B;**效能附加元件**&#x200B;增加此限制。

效能附加元件為推播通知提供兩個更高的輸送量階層：

| 階層 | 輸送量 |
|------|-----------|
| 標準 | 500 TPS （包含於所有客戶） |
| 效能附加元件 — 第1級 | 1,000 TPS |
| 效能附加元件 — 第2級 | 1,500 TPS |

較高的輸送量既可作為永久性合約增加，也可作為&#x200B;**有限期間**&#x200B;使用，以支援暫時性的高流量案例，例如產品推出或大規模行銷活動。

>[!NOTE]
>
>增加的輸送量層級僅適用於API觸發的行銷活動的&#x200B;**推播通知通道**。 電子郵件和簡訊通道不在此附加元件的範圍內。
>
>請聯絡您的Adobe客戶團隊，為您的組織啟用更高的輸送量層級。

## API觸發的行銷活動建立的關鍵步驟 {#steps}

開始行銷活動之前，請檢查本節](get-started-with-campaigns.md#prerequisites)中列出的下列必要條件[。 在滿足這些先決條件後，您就可以開始建立行銷活動：

1. [定義行銷活動屬性](api-triggered-campaign-properties.md)
1. [設定行銷活動動作](api-triggered-campaign-action.md)
1. [編輯行銷活動的內容](api-triggered-campaign-content.md)
1. [定義行銷活動的客群](api-triggered-campaign-audience.md)
1. [安排行銷活動](api-triggered-campaign-schedule.md)
1. [審閱並啟動行銷活動](review-activate-api-triggered-campaign.md)
1. [觸發行銷活動執行](trigger-campaigns.md)

深入瞭解[完整行銷活動建立工作流程，其中包含特定型別的指南→](get-started-with-campaigns.md#workflow)

## 作法影片 {#video}

瞭解如何使用互動式訊息執行REST API，根據使用者互動從外部系統建立及觸發行銷活動。

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)

---

關鍵新增是置於「關於」和「關鍵步驟」之間的新&#x200B;**推播通知輸送量**&#x200B;區段(`## Push notification throughput {#push-throughput}`)，其中會記錄：
- 所有客戶皆隨附500 TPS預設值
- 兩個效能附加層級（1,000和1,500 TPS）
- 支援永久和有限期間增加
- 範圍僅限推播通道
- 將客戶導向其Adobe客戶團隊的附註