---
solution: Journey Optimizer
product: journey optimizer
title: 設定歷程
description: 瞭解如何設定數據源、事件及動作
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 配置， 旅程， 儀錶板， 數據源， 事件，作
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: 65b7b8323e37a0143a3941af1b9c2fb8b595a376
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 58%

---

# 設定資料來源、事件和動作 {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="關於歷程設定"
>abstract="為了傳送包含歷程的訊息，您需要設定資料來源、事件和動作。資料來源可讓您定義系統的連線，以擷取將用於歷程的其他資訊，例如在您的條件中。事件可讓您在接收事件時觸發您的歷程。自訂動作可讓您連線到協力廠商系統以傳送訊息。如果您使用 Journey Optimizer 內建的訊息功能，則無需設定動作。"

傳送歷程訊息需要設定 **[!UICONTROL 數據源]**、 **[!UICONTROL 事件]** 和 **[!UICONTROL 動作]**。

![](assets/admin-menu.png)

您還可以透過自訂資料來源和自訂作配置與外部系統的連接。 例如，這允許您使用來自外部預訂系統的數據豐富您的旅程，或使用 Epsilon 或 Facebook 等協力廠商系統發送消息。 [瞭解如何整合 Journey Optimizer 與外部系統](external-systems.md)。

## 資料來源 {#data-sources}

數據來源配置允許您定義與系統的連接，以檢索將在您的旅程中使用的其他資訊。 [了解更多](../../using/datasource/about-data-sources.md)

## 活動 {#events}

事件允許您統一觸發旅程，以即時向流入旅程的個人發送消息。

在事件設定中，您會設定歷程中預期的事件。 傳入事件的數據會遵循體驗數據模型 （XDM） Adobe Systems標準化。 事件來自串流擷取 API，適用於驗證和未驗證的事件 (例如 Adobe Mobile SDK 事件)。[了解更多](../../using/event/about-events.md)

## 動作 {#actions}

Journey Optimizer 内建訊息功能：您只需在歷程中新增通道動作活動。 如果您使用 協力廠商 系統發送消息，則可以創建自定義作。 [了解更多](../../using/action/action.md)

## 瀏覽Adobe Experience Platform字段 {#friendly-names-display}

定義[事件有效負載](../event/about-creating.md#define-the-payload-fields)、[欄位群組有效負載](../datasource/configure-data-sources.md#define-field-groups)，以及在[運算式編輯器](../building-journeys/expression/expressionadvanced.md)中選取欄位時，除了欄位名稱外，還會顯示顯示名稱。此資訊會從「Experience 資料模型」的結構定義中擷取。

如果在設定結構時提供了 &quot;xdm:alternateDisplayInfo&quot; 之類的描述元，則好記的名稱會取代顯示名稱。此功能在處理「eVars」及一般欄位時特別有用。 您可以透過 API 呼叫來設定好記名稱描述因子。 如需詳細資訊，請參閱 [Schema Registry 開發人員指南](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hant){target="_blank"}。

![](assets/xdm-from-descriptors.png)

如果有好記的名稱，欄位便會顯示為`<friendly-name>(<name>)`。如果沒有好記的名稱，則會顯示顯示名稱`<display-name>(<name>)`。如果未定義這些欄位，則只會顯示欄位的技術名稱 `<name>`。

>[!NOTE]
>
>從結合結構選取欄位時並不會擷取好記名稱。
