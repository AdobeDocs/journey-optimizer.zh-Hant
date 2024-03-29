---
solution: Journey Optimizer
product: journey optimizer
title: 等待活動
description: 瞭解等待活動
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 等待，活動，歷程，下一步，畫布
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 17%

---

# 等待活動{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="等待活動"
>abstract="如果您要在執行路徑中的下一個活動之前等待，您可以使用等待活動。這項功能可讓您定義執行下一個活動的時刻。有兩個選項可用：期間和自訂。"

如果您想在執行路徑中的下一個活動之前等待，可以使用 **[!UICONTROL 等待]** 活動。 這項功能可讓您定義執行下一個活動的時刻。提供下列選項：

* [持續時間](#duration)
* [自訂](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## 關於等待活動{#about_wait}

最長等待時間為29天。 在測試模式中， **[!UICONTROL 測試等待時間]** 引數可讓您定義每個等待活動的持續時間。 預設時間為 10 秒。這將確保您能快速獲得測試結果。 請參閱[此頁面](../building-journeys/testing-the-journey.md)。

在歷程中使用多個等待活動時請小心，因為全域歷程逾時為30天，這表示設定檔在進入歷程後，將一律退出歷程的最長30天。 請參閱[此頁面](../building-journeys/journey-gs.md#global_timeout)。

個人只有在歷程剩餘的時間夠在30天歷程逾時前的等待期間完成時，才能進入等待活動。 例如，如果您新增兩個分別設為20天的等待活動，系統會偵測第二個等待將在30天逾時後結束。 因此，第二個等待將被忽略，個人將在開始歷程之前退出歷程。 在該範例中，客戶在歷程中總共將保留20天。

最佳實務是不使用等待來封鎖重新進入。 請改用 **允許重新進入** 歷程屬性層級的選項。 請參閱[此頁面](../building-journeys/journey-gs.md#entrance)。

## 持續時間等待{#duration}

選取下一個活動執行前等待的持續時間。 持續時間上限為29天。

![](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## 自訂等待{#custom}

此選項可讓您根據來自事件或資料來源的欄位，使用進階運算式來定義自訂日期，例如2023年7月12日下午5點。 它無法讓您定義自訂持續時間，例如7天。 運算式編輯器中的運算式應提供dateTimeOnly格式。 請參閱此 [頁面](expression/expressionadvanced.md). 如需dateTimeOnly格式的詳細資訊，請參閱此 [頁面](expression/data-types.md).

>[!NOTE]
>
>您可以利用dateTimeOnly運算式或使用函式來轉換為dateTimeOnly。 例如： toDateTimeOnly(@event{Event.offerOpened.activity.endTime})，事件中的欄位格式為2023-08-12T09:46:06Z
>
>此 **時區** 應在您歷程的屬性中找到。 因此，現今無法從介面直接指向完整的ISO-8601時間戳記混合時間和時區位移，例如2023-08-12T09:46:06.982-05。 請參閱[此頁面](../building-journeys/timezone-management.md)。

![](assets/journey57.png)

若要驗證等待活動是否如預期運作，您可以使用步驟事件。 請參閱[此頁面](../reports/query-examples.md#common-queries)。

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you'll be notified that the default time applies.

>[!NOTE]
>
>The first event of your journey must have a namespace.
>
>This capability is only available after an **[!UICONTROL Email]** activity. You need to have Adobe Campaign Standard.

1. In the **[!UICONTROL Amount of time]** field, define the number of hours to consider to optimize email sending.
1. In the **[!UICONTROL Optimization type]** field, choose if the optimization should increase clicks or opens.
1. In the **[!UICONTROL Default time]** field, define the default time to wait if the predictive send time score is not available.

    >[!NOTE]
    >
    >Note that the send time score can be unavailable because there is not enough data to perform the calculation. In this case, you will be informed, at publication time, that the default time applies.

![](assets/journey57bis.png)-->
