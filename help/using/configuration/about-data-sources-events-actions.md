---
solution: Journey Optimizer
product: journey optimizer
title: 設定歷程
description: 了解如何設定資料來源、事件和動作
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 設定歷程 {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="關於歷程設定"
>abstract="若要隨歷程傳送訊息，您需要設定資料來源、事件和動作。 資料來源可讓您定義系統連線，以擷取將用於歷程的其他資訊，例如在您的條件中。 事件可讓您在收到事件時觸發歷程。 自訂動作可讓您連線至協力廠商系統以傳送訊息。 如果您使用Journey Optimizer內建的訊息功能，則不需要設定動作。"

若要隨歷程傳送訊息，您需要設定 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**.

![](assets/admin-menu.png)

## 資料來源 {#data-sources}

資料來源設定可讓您定義系統連線，以擷取將用於歷程的其他資訊。 [深入了解](../../using/datasource/about-data-sources.md)

## 事件 {#events}

事件可讓您整體觸發歷程，以即時傳送訊息給流入歷程的個人。

在事件設定中，您會設定歷程中預期的事件。 會依照Adobe Experience Data Model(XDM)，對傳入事件的資料進行標準化。 事件來自串流獲取API，適用於已驗證和未驗證的事件（例如Adobe Mobile SDK事件）。 [深入了解](../../using/event/about-events.md)

## 動作 {#actions}

Journey Optimizer訊息功能內建：您只需將管道動作活動新增至歷程即可。 如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 [深入了解](../../using/action/action.md)

## 瀏覽Adobe Experience Platform欄位 {#friendly-names-display}

定義 [事件裝載](../event/about-creating.md#define-the-payload-fields), [欄位群組裝載](../datasource/configure-data-sources.md#define-field-groups) 和選取 [運算式編輯器](../building-journeys/expression/expressionadvanced.md)，則除了欄位名稱外，還會顯示顯示名稱。 此資訊會從Experience Data Model中的架構定義中擷取。

如果在設定結構時提供了&quot;xdm:alternateDisplayInfo&quot;之類的描述元，則好記的名稱會取代顯示名稱。 它在使用「eVar」和一般欄位時特別實用。 您可以透過API呼叫來設定好記的名稱描述元。 如需詳細資訊，請參閱 [Schema Registry開發人員指南](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target=&quot;_blank&quot;}。

![](assets/xdm-from-descriptors.png)

如果有好記的名稱，欄位將顯示為 `<friendly-name>(<name>)`. 如果沒有好記的名稱，則會顯示顯示名稱，例如 `<display-name>(<name>)`. 如果未定義這些欄位，則只會顯示欄位的技術名稱 `<name>`.

>[!NOTE]
>
>從結合結構選取欄位時，不會擷取好記名稱。
