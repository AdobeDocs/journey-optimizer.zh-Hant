---
solution: Journey Optimizer
product: journey optimizer
title: 一般事件
description: 瞭解如何使用一般事件
feature: Journeys, Events
topic: Content Management
role: User
level: Intermediate
keywords: 自訂，一般，事件，歷程
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 31d9189e8afd732875556b9caaa8e874f53597bb
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 13%

---

# 一般事件 {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="單一事件"
>abstract="事件可讓您一致性地觸發歷程，以即時傳送訊息給流入歷程的個人。對於這類事件，您只能新增標籤和說明。事件設定由資料工程師執行，並且無法編輯。"

事件可讓您一直觸發歷程，以即時傳送訊息給流入歷程的個人。

對於這類事件，您只能新增標籤和說明。無法編輯其餘的組態。 它由技術使用者執行。 請參閱[此頁面](../event/about-events.md)。

![](assets/general-events.png)

當您放置業務事件時，它會自動新增 **讀取對象** 活動。 有關業務事件的詳細資訊，請參閱 [本節](../event/about-events.md)

## 在特定時間接聽事件 {#events-specific-time}

位於歷程中的事件活動會無限期監聽事件。 若要只在特定時間監聽事件，您必須為事件設定逾時。

接著，歷程會在逾時中指定的時間接聽事件。 若在該期間收到事件，則人員會進入事件路徑。 如果沒有，客戶會進入逾時路徑（如果已定義），或繼續該歷程。

如果未定義逾時路徑，則逾時設定會當作等待活動，讓設定檔等候一段時間，如果事件發生在該等待結束之前，便會停止該時間。 如果您想要在逾時後從歷程中排除設定檔，您必須設定逾時路徑。

若要設定事件逾時，請遵循下列步驟：

1. 啟動 **[!UICONTROL 定義事件逾時]** 事件屬性中的選項。

1. 指定歷程將等待事件的時間長度。 持續時間上限為29天。

1. 如果在指定的逾時內未收到任何事件時，要將個人傳送到逾時路徑中，請啟用 **[!UICONTROL 設定逾時路徑]** 選項。 如果未啟用此選項，則到達逾時時間後，個人將繼續歷程。

   ![](assets/event-timeout.png)

在此範例中，歷程會傳送第一個歡迎推播給客戶。 然後只會在客戶隔天進入餐廳時傳送餐點折扣推播。 因此，我們將餐廳事件設定為1天逾時：

* 如果在歡迎推播後不到1天收到餐廳事件，則會傳送餐點折扣推播活動。
* 如果在隔天未收到餐廳事件，則人員會流經逾時路徑。

請注意，如果您想在之後放置的多個事件上設定逾時 **[!UICONTROL 等待]** 活動，您只需要針對這些事件之一設定逾時。

逾時將會套用至之後的所有事件。 **[!UICONTROL 等待]** 活動。 如果在指定的逾時前未收到任何事件，則個人將流入單一逾時路徑，或將繼續該歷程通過分支退出已定義這些逾時設定的活動。

![](assets/event-timeout-group.png)
