---
solution: Journey Orchestration
title: 一般事件
description: 瞭解如何使用一般事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---

# 一般事件 {#general-events}

對於此類事件，只能添加標籤和說明。 無法編輯配置的其餘部分。 由技術用戶執行。 請參閱[此頁面](../event/about-events.md)。

![](assets/general-events.png)

刪除業務事件時，它會自動添加 **讀取段** 的子菜單。 有關業務事件的詳細資訊，請參閱 [此部分](../event/about-events.md)

## 在特定時間內偵聽事件 {#events-specific-time}

在行程中定位的事件活動將無限期地偵聽事件。 要僅在特定時間偵聽事件，必須為該事件配置超時。

然後，該行程將在超時指定的時間內偵聽事件。 如果在該期間收到事件，則人員將在事件路徑中流動。 否則，客戶將進入超時路徑或結束其行程。

要為事件配置超時，請執行以下步驟：

1. 激活 **[!UICONTROL Define the event timeout]** 的子菜單。

1. 指定行程等待事件的時間。

1. 如果要在指定超時內未收到任何事件時將個人發送到超時路徑，請啟用 **[!UICONTROL Set a timeout path]** 的雙曲餘切值。 如果未啟用此選項，則一旦達到超時，個人的行程將結束。

   ![](assets/event-timeout.png)

在此示例中，此行程將首次向客戶發送歡迎推送。 然後，只有顧客在次日內進入餐廳時，它才會發送一份餐價折扣申請。 因此，我們將餐廳事件配置為1天超時：

* 如果在歡迎推送後不到1天收到餐廳活動，則發送餐點折扣推送活動。
* 如果在下一天內未收到餐廳事件，則該人將通過超時路徑。

請注意，如果要配置在位於 **[!UICONTROL Wait]** 活動，您只需配置其中一個事件的超時。

超時將應用於在 **[!UICONTROL Wait]** 的子菜單。 如果在指定超時之前未收到任何事件，則這些個人將流入一個超時路徑，或結束其行程。

![](assets/event-timeout-group.png)
