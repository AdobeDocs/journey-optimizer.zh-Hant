---
solution: Journey Optimizer
product: journey optimizer
title: 條件活動
description: 瞭解條件活動
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 活動，條件，畫布，歷程，最佳化
badge: label="有限可用性" type="Informative"
hidefromtoc: true
hide: true
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
source-git-commit: 19130e9eb5a2144afccab9fa8e5632de67bc7157
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 6%

---

# 活動最佳化 {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="活動最佳化"
>abstract="藉由將活動&#x200B;**最佳化**，您可以根據特定準則 (包括實驗、目標選擇和特定條件) 建立多條路徑，定義每個個體在您歷程中的進展方式。"

>[!AVAILABILITY]
>
>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。

**最佳化**&#x200B;活動可讓您根據特定條件（包括實驗、目標定位和特定條件）建立多個&#x200B;**路徑**，以定義個人在您的歷程中如何前進 — 確保最大程度的參與和成功，以建立高度自訂且有效的歷程。

**歷程路徑**&#x200B;可以包含下列任一專案：

* 通訊順序；
* 兩者之間的時間；
* 通訊次數；
* 或這三個變數的任意組合。

例如，一個路徑可能包含一封電子郵件，另一個路徑可能包含兩則簡訊，而第三個路徑可能包含一封電子郵件、兩個小時的[等待](wait-activity.md)節點，然後是簡訊。

<!--With this feature, [!DNL Journey Optimizer] empowers you with the tools to deliver personalized and optimized paths to your audience, ensuring maximum engagement and success to create highly customized and effective journeys.-->

透過&#x200B;**最佳化**&#x200B;活動，您可以：

* 執行[路徑實驗](#experimentation)
* 在每個歷程路徑中善用[目標定位](#targeting)規則
* 將[條件](#conditions)套用至您的路徑

![](assets/journey-optimize.png)

歷程上線後，會根據定義的條件評估設定檔，並根據比對條件，將設定檔從歷程傳送至適當的路徑。

## 使用實驗 {#experimentation}

實驗可讓您根據隨機分割來測試不同路徑，以根據預先定義的成功量度來判斷哪些路徑的執行效果最佳。

若要在歷程中設定實驗，請遵循下列步驟。

假設您想比較三個路徑：

* 一個路徑，一個電子郵件；
* 第二個路徑，其中的「等待」節點為兩天，且會傳送電子郵件；
* 第三個路徑，其中包含電子郵件，然後是SMS訊息。

1. 將&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動拖放至歷程畫布。

1. 新增選用標籤，以便在報告和測試模式記錄中識別活動。

1. 從&#x200B;**[!UICONTROL 方法]**&#x200B;下拉式清單中選取&#x200B;**[!UICONTROL 實驗]**。

   ![](assets/journey-optimize-experiment.png){width=85%}

1. 按一下&#x200B;**[!UICONTROL 實驗設定]**。

1. 視需要設計和設定您的實驗。 [了解作法](../content-management/content-experiment.md)

   <!--
    ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}
    Replace with appropriate screenshot
    The experiment applies to all the activities in the journey.TBC
   -->

歷程上線後，會隨機指派使用者沿著不同路徑前進。 [!DNL Journey Optimizer]追蹤哪個路徑可促使更多購買，並提供可操作的深入分析。

<!--Follow the success of your journey with the [Experimentation journey report](../reports/campaign-global-report-cja-experimentation.md). Is there a report specific to experimentation in journey?-->

### 實驗使用案例 {#uc-experiment}

下列範例說明如何將&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動與&#x200B;**[!UICONTROL 實驗]**&#x200B;方法搭配使用，以決定哪一個路徑整體運作最好。

**頻道有效性**

測試透過電子郵件傳送第一條訊息還是透過簡訊傳送第一條訊息是否會提高轉換率。

* 使用轉換率作為最佳化量度（例如：購買、註冊）。

![](assets/journey-optimize-experiment-uc.png)

**訊息頻率**

執行實驗，檢查在一週內傳送一封電子郵件還是傳送三封電子郵件是否會造成更多購買。

* 使用購買或取消訂閱率作為最佳化量度。

**通訊之間的等待時間**

比較24小時等待和後續追蹤前72小時的等待，以確定哪一個時間可最大化參與。

* 使用點進率或收入作為最佳化量度。

## 善用目標定位 {#targeting}

目標定位可讓您根據特定受眾區段<!-- depending on profile attributes or contextual attributes-->，決定客戶必須符合哪些特定規則或資格，才能符合進入其中一個歷程路徑的資格。

實驗是指定路徑的隨機指派，而目標定位則是確定性的，可確保正確的對象或設定檔進入指定的路徑。

透過鎖定目標，可根據下列專案定義特定規則：

* **使用者設定檔屬性**，例如位置(例如 地理定位)、年齡或偏好設定。 例如，美國的使用者會看到「Golden Gate」促銷活動，而法國的使用者會看到「Eiffel Tower」促銷活動。

* **內容資料**，例如裝置型別(例如 裝置定位)、一天中的時間或工作階段詳細資訊。 例如，案頭使用者會收到案頭最佳化內容，而行動使用者則會收到行動最佳化內容。

* **對象**，可用來包含或排除具有特定對象成員資格的設定檔。

若要在歷程中設定鎖定目標，請遵循下列步驟。

1. 將&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動拖放至歷程畫布。

1. 新增選用標籤，以便在報告和測試模式記錄中識別活動。

1. 從&#x200B;**[!UICONTROL 方法]**&#x200B;下拉式清單中選取&#x200B;**[!UICONTROL 鎖定目標]**。

   ![](assets/journey-optimize-targeting.png){width=85%}

1. 按一下&#x200B;**[!UICONTROL 建立目標規則]**。

1. 使用規則產生器來定義條件。 例如，定義美國居民的規則、法國居民的規則以及印度居民的規則。

   ![](assets/journey-targeting-rule.png)

1. 視需要選取&#x200B;**[!UICONTROL 啟用遞補內容]**。 後援內容可讓您的對象在沒有符合目標規則時接收預設內容。 如果您未選取此選項，則不符合上述定義之目標定位規則的任何受眾都不會輸入遞補路徑。

1. 儲存您的目標規則設定。

1. 回到歷程中，拖放特定動作以自訂每個路徑。 例如，您可以為美國居民建立特定電子郵件、為法國居民建立其他電子郵件等。

   ![](assets/journey-targeting-paths.png)

1. 為您目標規則設定所定義的每個群組設計適當的內容。 您可以順暢地在不同路徑之間導覽。

   ![](assets/journey-targeting-design.png)

   在此範例中，為美國居民設計一條特定路徑，為法國居民設計另一條路徑，並為印度居民設計另一條路徑。

一旦歷程上線，系統就會處理為每個區段指定的路徑，好讓美國居民輸入特定路徑，法國居民輸入不同路徑，以此類推。

### 使用案例與定位 {#uc-targeting}

下列範例顯示如何搭配使用&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動與&#x200B;**[!UICONTROL 鎖定目標]**&#x200B;方法，為不同的子對象個人化路徑。

**區段特定管道**

金級狀態忠誠會員可以透過電子郵件接收個人化優惠，而所有其他會員則會導向簡訊提醒。

* 使用每個設定檔的收入或轉換率作為最佳化量度。

![](assets/journey-optimize-targeting-uc.png)

**行為型鎖定目標**

已開啟電子郵件但未點按的客戶會收到推播通知，而完全未開啟的客戶則會收到簡訊。

* 使用點進率或下游轉換作為最佳化量度。

**購買歷程記錄鎖定目標**

最近購買過的客戶可以進入簡短的「感謝您+交叉銷售」路徑，而沒有購買記錄的客戶則會進入更長的培育歷程。

* 使用重複購買率或參與率作為最佳化量度。

## 新增條件。 {#conditions}

您可以新增條件，根據特定條件建立多個路徑，以定義個人在您的歷程中進度。 您也可以設定處理逾時或錯誤的替代路徑，確保提供順暢的體驗。

![](assets/journey-condition.png)

瞭解如何在[本節](conditions.md)中定義條件。

可使用下列型別的條件：

* [資料Source條件](condition-activity.md#data_source_condition)
* [時間條件](condition-activity.md#time_condition)
* [百分比分割](condition-activity.md#percentage_split)
* [日期條件](condition-activity.md#date_condition)
* [設定檔上限](condition-activity.md#profile_cap)
