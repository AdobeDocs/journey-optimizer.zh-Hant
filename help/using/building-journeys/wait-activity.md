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
version: Journey Orchestration
source-git-commit: c30a74ccdaec81cbbb28e3129d5c351a0fe64bfc
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 12%

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

在歷程中使用多個&#x200B;**等待**&#x200B;活動時，請注意，歷程的[全域逾時](journey-properties.md#global_timeout)為91天，這表示設定檔在進入歷程後，一律會退出歷程的最長91天。 請在[此頁面](journey-properties.md#global_timeout)了解更多。

個人只有在歷程中剩餘的時間足以在91天歷程逾時前完成等待期間時，才能進入&#x200B;**等待**&#x200B;活動。

### 等待並重新進入 {#wait-reentrance}

不使用&#x200B;**等待**&#x200B;活動以封鎖重新進入的最佳作法。 請改用歷程屬性層級的&#x200B;**允許重新進入**&#x200B;選項。 請在[此頁面](../building-journeys/journey-properties.md#entrance)了解更多。

### 等待和測試模式 {#wait-test-mode}

在測試模式中，測試&#x200B;**[!UICONTROL 中的]**&#x200B;等待時間引數可讓您定義每個&#x200B;**等待**&#x200B;活動的持續時間。 預設時間為 10 秒。這將確保您能快速獲得測試結果。 請在[此頁面](../building-journeys/testing-the-journey.md)了解更多。

### 等待和行動裝置頻道 {#wait-mobile-channels}

如果您想要在傳送[推播通知](../in-app/create-in-app.md)後立即顯示[應用程式內訊息](../../rp_landing_pages/push-landing-page.md)，請使用&#x200B;**等待**&#x200B;活動來允許應用程式內訊息裝載時間傳播。 通常建議等候5至15分鐘，但確切時間會因裝載複雜性和個人化需求而有所不同。

## 設定 {#wait-configuration}

### 持續時間等待 {#duration}

選取&#x200B;**持續時間**&#x200B;型別，以設定下一個活動執行前等待的相對持續時間。 持續時間上限為&#x200B;**90天**。

![定義等待期間](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![Wait activity configuration panel with duration and fixed date options](assets/journey56.png)

-->

### 自訂等待 {#custom}

選取&#x200B;**自訂**&#x200B;型別以定義自訂日期，使用進階運算式，根據來自事件或自訂動作回應的欄位。 您不能直接定義相對持續時間，例如7天，但您可以視需要使用函式來計算相對持續時間（例如：購買後2天）。

![使用運算式定義自訂等待](assets/journey57.png)

編輯器中的運算式應提供`dateTimeOnly`格式。 請參見[此頁面](expression/expressionadvanced.md)。如需dateTimeOnly格式的詳細資訊，請參閱[此頁面](expression/data-types.md)。

最佳實務是使用您的設定檔專屬的自訂日期，並避免對所有人使用相同的日期。 例如，不要定義`toDateTimeOnly('2024-01-01T01:11:00Z')`，而是要定義每個設定檔專屬的`toDateTimeOnly(@event{Event.productDeliveryDate})`。 請注意，使用固定日期可能會導致歷程執行問題。 在[本節](entry-management.md#wait-activities-impact)中進一步瞭解等待活動對歷程處理率的影響。


>[!NOTE]
>
>您可以運用`dateTimeOnly`運算式或使用函式來轉換成`dateTimeOnly`。 例如： `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`，事件中的欄位格式為2023-08-12T09:46:06Z。
>
>您歷程的屬性中應該有&#x200B;**時區**。 因此，從使用者介面，無法直接指向完整的ISO-8601時間戳記混合時間和時區位移，例如2023-08-12T09:46:06.982-05。 [了解更多](../building-journeys/timezone-management.md)。

>[!CAUTION]
>
>使用`toDateTimeOnly()`建立自訂等待運算式時，請避免在運算式結果中附加&#39;Z&#39;或任何時區位移（例如&#39;-05:00&#39;）。 運算式必須使用有效的ISO日期/時間語法，該語法會參照歷程設定的時區，而不會使用明確的時區指示器。
>
>**正確範例：** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00"))`
>
>**不正確的範例：** `toDateTimeOnly(concat(toString(toDateOnly(nowWithDelta(2, "days"))),"T10:00:00Z"))` ❌ （包含&#39;Z&#39;）
>
>使用不支援的時區指示器可能會導致設定檔停滯在等待活動中，而不是按預期前進。

若要驗證等待活動是否如預期運作，您可以使用步驟事件。 [了解更多](../reports/query-examples.md#common-queries)。

## 等待後重新整理設定檔 {#profile-refresh}

當設定檔停留在以&#x200B;**讀取對象**&#x200B;活動開始的歷程中的&#x200B;**等待**&#x200B;活動時，歷程會自動從整合設定檔服務(UPS)重新整理設定檔的屬性，以擷取最新的可用資料。

* **在歷程專案**：設定檔使用歷程開始時所評估之對象快照中的屬性值。
* **在等待節點之後**：歷程會執行查詢，以從UPS擷取最新的設定檔資料，而非較舊的快照集資料。 這表示自歷程開始以來，設定檔屬性可能已變更。

此行為可確保下游活動在等待期間後使用目前的設定檔資訊。 不過，如果您預期歷程在整個執行期間僅使用原始快照集資料，則可能會產生非預期的結果。

範例：如果設定檔在歷程開始時符合「銀級客戶」對象的資格，但在3天等待期間升級為「金級客戶」，則等待後的活動會看到更新的「金級客戶」狀態。

## 自動等待節點  {#auto-wait-node}

>[!CONTEXTUALHELP]
>id="ajo_journey_auto_wait_node "
>title="關於自動等待節點"
>abstract="系統會在此活動之後自動新增&#x200B;**等待**&#x200B;活動。等待活動的時間設為 3 天。您可以視需求移除或設定等待活動。"

每個傳入體驗活動（應用程式內訊息、程式碼型體驗或卡片）都隨附3天&#x200B;**等待**&#x200B;活動。 由於當設定檔到達歷程終點時，傳入訊息會自動結束，因此我們假設您想要使用者至少在3天內看到它。 您可以移除此&#x200B;**等待**&#x200B;活動，或視需要變更其設定。
