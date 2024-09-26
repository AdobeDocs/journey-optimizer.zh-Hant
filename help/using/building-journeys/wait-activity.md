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
source-git-commit: 18296fe54dcef6620d4f74374848199368f01475
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 18%

---

# 等待活動 {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="等待活動"
>abstract="如果您要在執行路徑中的下一個活動之前等待，您可以使用等待活動。這項功能可讓您定義執行下一個活動的時刻。有兩個選項可用：期間和自訂。"

您可以使用&#x200B;**[!UICONTROL 等待]**&#x200B;活動，在執行下一個活動之前定義持續時間。  等待持續時間上限為&#x200B;**90天**。

您可以設定兩種型別的&#x200B;**等待**&#x200B;活動：

* 基於相對持續時間的等待。 [了解更多](#duration)
* 自訂日期，使用函式進行計算。 [了解更多](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## 建議 {#wait-recommendations}

### 多個等待活動 {#multiple-wait-activities}

在歷程中使用多個&#x200B;**等待**&#x200B;活動時，請注意，歷程的[全域逾時](journey-properties.md#global_timeout)為91天，這表示設定檔在進入歷程後，一律會退出歷程的最長91天。 在[本頁](journey-properties.md#global_timeout)中瞭解更多。

個人只有在歷程中剩餘的時間足以在91天歷程逾時前完成等待期間時，才能進入&#x200B;**等待**&#x200B;活動。

### 等待並重新進入 {#wait-reentrance}

不使用&#x200B;**等待**&#x200B;活動以封鎖重新進入的最佳作法。 請改用歷程屬性層級的&#x200B;**允許重新進入**&#x200B;選項。 在[本頁](../building-journeys/journey-properties.md#entrance)中瞭解更多。

### 等待和測試模式 {#wait-test-modd}

在測試模式中，測試&#x200B;]**中的**[!UICONTROL &#x200B;等待時間引數可讓您定義每個&#x200B;**等待**&#x200B;活動的持續時間。 預設時間為 10 秒。這將確保您能快速獲得測試結果。 在[本頁](../building-journeys/testing-the-journey.md)中瞭解更多。

## 設定 {#wait-configuration}

### 持續時間等待 {#duration}

選取&#x200B;**持續時間**&#x200B;型別，以設定下一個活動執行前等待的相對持續時間。 持續時間上限為&#x200B;**90天**。

![定義等待期間](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### 自訂等待 {#custom}

選取&#x200B;**自訂**&#x200B;型別以定義自訂日期，使用進階運算式，根據來自事件或自訂動作回應的欄位。 您不能直接定義相對持續時間，例如7天，但您可以視需要使用函式來計算相對持續時間（例如：購買後2天）。

![使用運算式定義自訂等待](assets/journey57.png)

編輯器中的運算式應提供`dateTimeOnly`格式。 請參見[此頁面](expression/expressionadvanced.md)。如需dateTimeOnly格式的詳細資訊，請參閱[此頁面](expression/data-types.md)。

最佳實務是使用您的設定檔專屬的自訂日期，並避免對所有人使用相同的日期。 例如，不要定義`toDateTimeOnly('2024-01-01T01:11:00Z')`，而是要定義每個設定檔專屬的`toDateTimeOnly(@event{Event.productDeliveryDate})`。 請注意，使用固定日期可能會導致歷程執行問題。


>[!NOTE]
>
>您可以運用`dateTimeOnly`運算式或使用函式來轉換成`dateTimeOnly`。 例如： `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`，事件中的欄位格式為2023-08-12T09:46:06Z。
>
>您歷程的屬性中應該有&#x200B;**時區**。 因此，從使用者介面，無法直接指向完整的ISO-8601時間戳記混合時間和時區位移，例如2023-08-12T09:46:06.982-05。 [了解更多](../building-journeys/timezone-management.md)。


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

## 自動等待節點  {#auto-wait-node}


>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="關於自動等待節點"
>abstract="系統會在此活動之後自動新增&#x200B;**等待**&#x200B;活動。等待活動的時間設為 3 天。您可以視需求移除或設定等待活動。"

每個傳入訊息活動（應用程式內訊息、程式碼型體驗或卡片）都隨附3天的&#x200B;**等待**&#x200B;活動。 由於當設定檔到達歷程終點時，傳入訊息會自動結束，因此我們假設您想要使用者至少在3天內看到它。 您可以移除此&#x200B;**等待**&#x200B;活動，或視需要變更其設定。