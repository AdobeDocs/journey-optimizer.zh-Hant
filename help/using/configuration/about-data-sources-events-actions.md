---
title: 管理和設定
description: 瞭解管理和設定准則
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 56%

---

# 設定歷程 {#configure-journeys}

為了發送包含行程的消息，您需要配置 **[!UICONTROL Data Sources]**。 **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**。

![](../assets/admin-menu.png)

## 資料來源

資料源配置允許您定義到系統的連接，以檢索將在您的行程中使用的其他資訊。 [進一步了解](../../using/datasource/about-data-sources.md)

## 活動

通過事件，您可以觸發整個行程，以即時向流入旅程的個體發送消息。

在事件配置中，您可以配置行程中預期的事件。 傳入事件的資料按照Adobe體驗資料模型(XDM)進行規範化。 事件來自串流獲取 API，適用於驗證和未驗證的事件（例如 Adobe Mobile SDK 事件）。[進一步了解](../../using/event/about-events.md)

## 動作

Journey Optimizer消息功能是內置的：您只需設計內容並發佈消息。 如果您使用第三方系統發送消息，則可以建立自定義操作。 [進一步了解](../../using/action/action.md)

## 透過 Adobe Experience Platform 欄位瀏覽 {#friendly-names-display}

定義[事件有效負載](../event/about-creating.md#define-the-payload-fields)、[欄位群組有效負載](../datasource/configure-data-sources.md#define-field-groups)，以及在[運算式編輯器](../building-journeys/expression/expressionadvanced.md)中選取欄位時，除了欄位名稱外，還會顯示顯示名稱。此資訊會從「Experience 資料模型」的結構定義中擷取。

如果在設定結構時提供了 &quot;xdm:alternateDisplayInfo&quot; 之類的描述元，則好記的名稱會取代顯示名稱。它在使用「eVar」和一般欄位時特別有用。 您可以透過 API 呼叫來設定好記名稱描述因子。 有關詳細資訊，請參見 [架構註冊表開發人員指南](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hant){target=&quot;_blank&quot;}。

![](../assets/xdm-from-descriptors.png)

如果有好記的名稱，欄位便會顯示為`<friendly-name>(<name>)`。如果沒有好記的名稱，則會顯示顯示名稱`<display-name>(<name>)`。如果未定義這些欄位，則只會顯示欄位的技術名稱 `<name>`。

>[!NOTE]
>
>從結合結構選取欄位時並不會擷取好記名稱。
