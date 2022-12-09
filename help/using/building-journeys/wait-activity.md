---
solution: Journey Optimizer
product: journey optimizer
title: 等待活動
description: 了解等候活動
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 等待活動{#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="等待活動"
>abstract="如果要在路徑中執行下一個活動之前等待，則可以使用等待活動。 它可讓您定義下一個活動的執行時間。 有兩個選項可用：持續時間和自訂。"

如果您想在路徑中執行下一個活動之前等待，可以使用 **[!UICONTROL Wait]** 活動。 它可讓您定義下一個活動的執行時間。 有三個可用選項：

* [持續時間](#duration)
* [自訂](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## 關於等待活動{#about_wait}

等待時間上限為30天。 在測試模式中， **[!UICONTROL Wait time in test]** 參數可讓您定義每個等待活動的持續時間。 預設時間為10秒。 這可確保您快速取得測試結果。 請參閱 [本頁](../building-journeys/testing-the-journey.md)

在歷程中使用多個等待活動時請小心，因為全域歷程逾時為30天，這表示設定檔在其輸入後最多30天將一律從歷程中退出。

## 持續等待{#duration}

選取下一個活動執行之前等待的持續時間。

![](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## 自訂等待{#custom}

此選項可讓您根據來自事件或資料來源的欄位，使用進階運算式來定義自訂日期，例如2020年7月12日下午5點。 它不會讓您定義自訂持續時間，例如7天。 運算式編輯器中的運算式應提供dateTimeOnly格式。 請參閱 [頁面](expression/expressionadvanced.md). 如需dateTimeOnly格式的詳細資訊，請參閱 [頁面](expression/data-types.md).

>[!NOTE]
>
>您可以運用dateTimeOnly運算式，或使用函式來轉換為dateTimeOnly。 例如：toDateTimeOnly(@{Event.offerOpened.activity.endTime})，事件中的欄位為2016-08-12T09格式:46:06Z。
>
>此 **時區** 在歷程的屬性中是預期的。 因此，今天無法從介面直接指向完整的ISO-8601時間戳，混合時間和時區偏移，如2016-08-12T09:46:06.982-05。 請參閱 [本頁](../building-journeys/timezone-management.md).

![](assets/journey57.png)

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you’ll be notified that the default time applies.

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
