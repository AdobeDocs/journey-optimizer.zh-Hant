---
title: 管理與設定
description: 了解管理與設定准則
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: daf5c6021a3efc8852b989fb602380c369758ead
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 56%

---

# 設定歷程

若要隨歷程傳送訊息，您需要設定 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

## 資料來源

資料來源設定可讓您定義系統連線，以擷取將用於歷程的其他資訊。 [了解更多](../../using/datasource/about-data-sources.md)

## 事件

事件可讓您整體觸發歷程，以即時傳送訊息給流入歷程的個人。

在事件設定中，您會設定歷程中預期的事件。 會依照Adobe Experience Data Model(XDM)，對傳入事件的資料進行標準化。 事件來自串流獲取 API，適用於驗證和未驗證的事件（例如 Adobe Mobile SDK 事件）。[了解更多](../../using/event/about-events.md)

## 動作

Journey Optimizer訊息功能內建：您只需要設計內容並發佈訊息。 如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 [了解更多](../../using/action/action.md)

## 透過 Adobe Experience Platform 欄位瀏覽 {#friendly-names-display}

定義[事件有效負載](../event/about-creating.md#define-the-payload-fields)、[欄位群組有效負載](../datasource/configure-data-sources.md#define-field-groups)，以及在[運算式編輯器](../building-journeys/expression/expressionadvanced.md)中選取欄位時，除了欄位名稱外，還會顯示顯示名稱。此資訊會從「Experience 資料模型」的結構定義中擷取。

如果在設定結構時提供了 &quot;xdm:alternateDisplayInfo&quot; 之類的描述元，則好記的名稱會取代顯示名稱。它在使用「eVar」和一般欄位時特別有用。 您可以透過 API 呼叫來設定好記名稱描述因子。 如需詳細資訊，請參閱 [Schema Registry開發人員指南](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hant){target=&quot;_blank&quot;}。

![](../assets/xdm-from-descriptors.png)

如果有好記的名稱，欄位便會顯示為`<friendly-name>(<name>)`。如果沒有好記的名稱，則會顯示顯示名稱`<display-name>(<name>)`。如果未定義這些欄位，則只會顯示欄位的技術名稱 `<name>`。

>[!NOTE]
>
>從結合結構選取欄位時並不會擷取好記名稱。
