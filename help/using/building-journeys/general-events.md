---
solution: Journey Orchestration
title: 一般事件
description: 瞭解如何使用一般事件
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---

# 一般事件 {#section_ofg_jss_dgb}

![](../assets/do-not-localize/badge.png)

對於此類型的事件，您只能添加標籤和說明。 無法編輯其餘的配置。 由技術使用者執行。 請參閱[本頁](../event/about-events.md)。

![](../assets/general-events.png)

刪除業務事件時，它會自動添加&#x200B;**讀取段**&#x200B;活動。 有關業務事件的詳細資訊，請參閱[本節](../event/about-events.md)

## 在特定時間內監聽事件{#events-specific-time}

位於歷程中的事件活動會無限期地監聽事件。 若要僅在特定時間監聽事件，您必須設定事件逾時。

然後，歷程將在逾時中指定的時間內監聽事件。 如果在該期間收到事件，則人員將在事件路徑中流動。 如果沒有，客戶將流入逾時路徑，或結束其歷程。

若要設定事件的逾時，請依照下列步驟進行：

1. 從事件屬性中激活&#x200B;**[!UICONTROL Enable the event timeout]**&#x200B;選項。

1. 指定歷程等待活動的時間長度。

1. 如果您想在指定逾時內未收到任何事件時，將個人傳送至逾時路徑，請啟用&#x200B;**[!UICONTROL Set the timeout path]**&#x200B;選項。 如果未啟用此選項，則到達逾時後，個人的歷程將結束。

   ![](../assets/event-timeout.png)

在此範例中，歷程會傳送第一個歡迎推播給客戶。 然後，只有當顧客在第二天進入餐廳時，它才會發送餐點折扣推播。 因此，我們設定餐廳事件為1天逾時：

* 如果在歡迎推播後不到1天收到餐廳活動，則會傳送餐點折扣推播訊息。
* 如果第二天未收到餐廳事件，則訪客會透過逾時路徑流程。

請注意，如果您想要針對&#x200B;**[!UICONTROL Wait]**&#x200B;活動後所定位的多個事件設定逾時，則只需針對這些事件設定逾時。

逾時會套用至&#x200B;**[!UICONTROL Wait]**&#x200B;活動後所定位的所有事件。 如果在指定逾時後未收到任何事件，則個人會流入單一逾時路徑，或結束其歷程。

![](../assets/event-timeout-group.png)
