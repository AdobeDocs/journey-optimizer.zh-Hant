---
title: 條件活動
description: 瞭解條件活動
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
source-git-commit: 7588a675319324e43bbc61a71b1fdfaab9cce93a
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 7%

---

# 條件活動{#condition-activity}

這些類型的條件可用：

* [資料源條件](#data_source_condition)
* [時間條件](#time_condition)
* [分解百分比](#percentage_split)
* [日期條件](#date_condition)
* [輪廓帽](#profile_cap)

![](../assets/journey49.png)

## 關於條件活動 {#about_condition}

在旅途中使用多個條件時，您可以為每個條件定義標籤，以便更容易地識別它們。

按一下 **[!UICONTROL Add a path]** 的雙曲餘切值。 對於每個條件，在活動後的畫布中都會添加新路徑。

![](../assets/journey47.png)

請注意，行程設計對功能有影響。 當在條件後定義多個路徑時，將只執行第一個符合條件的路徑。 這意味著您可以通過將路徑置於彼此之上或之下來改變路徑的優先順序。

例如，我們以第一條路的條件「人是VIP」和第二條路的條件「人是男性」為例。 如果符合兩個條件的人(男VIP)通過此步驟，則即使此人也有資格獲得第二條路徑，也將選擇第一條路徑，因為第一條路徑是「高於」。 要更改此優先順序，請按另一個垂直順序移動活動。

![](../assets/journey48.png)

您可以通過選中為不符合定義條件條件的受眾建立其他路徑 **[!UICONTROL Show path for other cases than the one(s) above]**。 請注意，此選項在分解條件中不可用。 請參閱 [分解百分比](#percentage_split)。

簡單模式允許您基於欄位組合執行簡單查詢。 螢幕左側顯示所有可用欄位。 將欄位拖放到主區域。 要組合不同的元素，請將它們互鎖到彼此中以建立不同的組和/或組級。 然後，您可以選取邏輯運算子來組合同一層級的元素：

* 和：兩個標準的交集。 只考慮與所有條件匹配的元素。
* 或：兩個標準的結合。 考慮匹配兩個條件中至少一個的元素。

![](../assets/journey64.png)

如果你用的 [Adobe Experience Platform分段服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}可建立段，您可以在行程條件中利用這些段。 請參閱 [在條件中使用段](../building-journeys/condition-activity.md#using-a-segment)。


>[!NOTE]
>
>不能使用簡單編輯器對時間序列（例如購買清單、以前按一下消息）執行查詢。 為此，您需要使用高級編輯器。 請參閱 [AdobeJourney Orchestration文檔](expression/expressionadvanced.md)。

當動作或條件發生錯誤時，個人的歷程就會停止。唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL Add an alternative path in case of a timeout or an error]**。請參閱[本節](../building-journeys/using-the-journey-designer.md#paths)。

在簡單編輯器中，您還將在事件和資料源類別下找到「行程屬性」類別。 此類別包含與給定配置檔案的行程相關的技術欄位。 這是系統從即時行程中檢索的資訊，如行程ID或遇到的特定錯誤。 有關詳細資訊，請參見 [AdobeJourney Orchestration文檔](expression/journey-properties.md)

## 資料源條件 {#data_source_condition}

這允許您基於資料源中的欄位或先前在行程中定位的事件來定義條件。 要瞭解如何使用表達式編輯器，請參見 [AdobeJourney Orchestration文檔](expression/expressionadvanced.md)。 使用高級表達式編輯器，可以設定操作集合或使用需要傳遞參數的資料源的更高級條件。 請參閱[此頁面](../datasource/external-data-sources.md)。

![](../assets/journey50.png)

## 時間條件{#time_condition}

這允許您根據一天中的小時和/或一週中的某天執行不同的操作。 例如，您可以決定在白天發送SMS消息，在工作日發送夜間電子郵件。

>[!NOTE]
>
>時區不再特定於某個條件，現在在行程屬性中的行程級別定義。 請參見[此頁面](../building-journeys/timezone-management.md)。

![](../assets/journey51.png)

## 分解百分比 {#percentage_split}

此選項允許您隨機分割受眾，以便為每個組定義不同的操作。 定義每個路徑的拆分數和重新分區。 分割計算是統計的，因為系統無法預測在旅途中會有多少人流入。 因此，分割具有非常低的誤差裕度。 此函式基於Java隨機機制(請參見 [頁](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html))。

在test模式下，當達到拆分時，總是選擇頂部分支。 如果希望test選擇其他路徑，則可以重新組織拆分分支的位置。 請參見[此頁面](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>請注意，在百分比分解條件中沒有添加路徑的按鈕。 路徑數將取決於拆分數。 在拆分條件中，無法為其他情況添加路徑，因為它不會發生。 人們總是走在一條分割的路上。

![](../assets/journey52.png)

## 日期條件 {#date_condition}

這允許您根據日期定義不同的流。 例如，如果人員在「銷售」期間進入步驟，您將向他們發送特定消息。 今年剩餘時間，你會再發一條消息。

>[!NOTE]
>
>時區不再特定於某個條件，現在在行程屬性中的行程級別定義。 請參閱[此頁面](../building-journeys/timezone-management.md)。

![](../assets/journey53.png)

## 輪廓帽 {#profile_cap}

使用此條件類型可設定行程路徑的最大配置檔案數。 當達到此限制後，輸入的個人資料將採用替代路徑。 這可確保您的行程永遠不會超過定義的限制。

您可以使用此條件類型來增加交貨量。 查看 [用例](ramp-up-deliveries-uc.md)。

預設上限為1000。

計數器僅應用於所選行程版本。 計數器在一個月後重置為零。 重置後，輸入的配置檔案將再次沿公稱路徑走，直到達到計數器限制。

標稱路徑始終優先於備用路徑，即使您將備用路徑移到行程畫布上標稱路徑上方。

對於即時旅程，以下是確保達到限制的閾值：

* 對於大於10000的帽，要注入的不同輪廓的數量必須至少是帽的1.3倍。
* 對於低於10000的封頂，要注入的不同輪廓數必須加上封頂數1000。

在test模式中未考慮配置檔案上限。

![](../assets/profile-cap-condition.png)

## 在條件中使用區段 {#using-a-segment}

本節說明如何在行程條件中使用段。 有關網段以及如何構建這些網段的詳細資訊，請參閱 [此部分](../segment/about-segments.md)。

要在行程條件中使用段，請執行以下步驟：

1. 開路，放下 **[!UICONTROL Condition]** 活動，然後選擇 **資料源條件**。
   ![](../assets/journey47.png)

1. 按一下 **[!UICONTROL Add a path]** 每條額外路徑。 對於每個路徑，按一下 **[!UICONTROL Expression]** 的子菜單。

   ![](../assets/segment3.png)

1. 在左側， **[!UICONTROL Segments]** 的下界。 拖放要用於條件的段。 預設情況下，段上的條件為true。

   ![](../assets/segment4.png)

   >[!NOTE]
   >
   >請注意，只有 **已實現** 和 **現有** 段參與狀態將被視為段的成員。 有關如何評估段的詳細資訊，請參閱 [分段服務文檔](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}。
