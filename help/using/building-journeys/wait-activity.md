---
solution: Journey Optimizer
product: journey optimizer
title: 等待活動
description: 瞭解如何設定等待活動
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 等待，活動，歷程，下一步，畫布
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 14%

---

# 等待活動 {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="等待活動"
>abstract="如果您要在執行路徑中的下一個活動之前等待，您可以使用等待活動。這項功能可讓您定義執行下一個活動的時刻。有兩個選項可用：期間和自訂。"

您可以使用 **[!UICONTROL 等待]** 活動，定義下一個活動執行之前的持續時間。  最長等待時間為 **29天**.

您可以設定兩種型別 **等待** 活動：

* 基於相對持續時間的等待。 [了解更多](#duration)
* 自訂日期，使用函式進行計算。 [了解更多](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## 建議 {#wait-recommendations}

### 多個等待活動 {#multiple-wait-activities}

使用多個 **等待** 歷程中的活動，請注意 [全域逾時](journey-properties.md#global_timeout) 若為歷程，則為91天，這表示設定檔一律會從歷程中退出，最多為進入後91天。 在[本頁](journey-properties.md#global_timeout)中瞭解更多。

個人可以輸入 **等待** 活動，前提是他們在91天歷程逾時前的歷程剩餘時間足以完成等待期間。 例如，如果您新增兩個 **等待** 活動設為20天，系統會偵測到第二個 **等待** 活動將在91天逾時後結束。 第二個 **等待** 因此，活動將被忽略，個人將在啟動歷程之前退出歷程。 在該範例中，客戶在歷程中總共將保留20天。

### 等待並重新進入 {#wait-re-entrance}

不使用的最佳實務 **等待** 封鎖重新進入的活動。 請改用 **允許重新進入** 歷程屬性層級的選項。 在[本頁](../building-journeys/journey-properties.md#entrance)中瞭解更多。

### 等待和測試模式 {#wait-test-modd}

在測試模式中， **[!UICONTROL 測試等待時間]** 引數可讓您定義 **等待** 活動將會持續。 預設時間為 10 秒。這將確保您能快速獲得測試結果。 在[本頁](../building-journeys/testing-the-journey.md)中瞭解更多。

## 設定 {#wait-configuration}

### 持續時間等待 {#duration}

選取 **持續時間** 輸入以設定下一個活動執行前等待的相對持續時間。 最大持續時間為 **29天**.

![定義等待持續時間](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### 自訂等待 {#custom}

選取 **自訂** 輸入以定義自訂日期，使用進階運算式，根據來自事件或自訂動作回應的欄位。 您不能直接定義相對持續時間，例如7天，但您可以視需要使用函式來計算相對持續時間（例如：購買後2天）。

![使用運算式定義自訂等待](assets/journey57.png)

編輯器中的運算式應提供 `dateTimeOnly` 格式。 請參見[此頁面](expression/expressionadvanced.md)。如需dateTimeOnly格式的詳細資訊，請參閱 [此頁面](expression/data-types.md).

最佳實務是使用您的設定檔專屬的自訂日期，並避免對所有人使用相同的日期。 例如，請勿定義 `toDateTimeOnly('2024-01-01T01:11:00Z')` 但是 `toDateTimeOnly(@event{Event.productDeliveryDate})` 每個設定檔都有其專屬性。 請注意，使用固定日期可能會導致歷程執行問題。


>[!NOTE]
>
>您可以善用 `dateTimeOnly` 運算式或使用函式轉換為 `dateTimeOnly`. 例如： `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`，事件中的欄位格式為2023-08-12T09:46:06Z
>
>此 **時區** 應在您歷程的屬性中找到。 因此，從使用者介面，無法直接指向完整的ISO-8601時間戳記混合時間和時區位移，例如2023-08-12T09:46:06.982-05。 [了解更多](../building-journeys/timezone-management.md)。


若要驗證等待活動是否如預期運作，您可以使用步驟事件。 [了解更多](../reports/query-examples.md#common-queries)。

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
