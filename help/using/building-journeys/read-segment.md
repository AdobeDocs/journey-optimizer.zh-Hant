---
solution: Journey Optimizer
product: journey optimizer
title: 在歷程中使用區段
description: 瞭解如何在旅途中使用段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 活動、行程、讀取、段、平台
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 12%

---

# 在歷程中使用區段 {#segment-trigger-activity}

## 添加讀取段活動 {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="閱讀區段活動"
>abstract="「閱讀區段」活動可讓您安排屬於 Adobe Experience Platform 區段的所有個人進入歷程。進入歷程可以執行一次，也可以定期執行。"

使用 **讀取段** 活動，使段中的所有個人進入行程。 進入歷程可以執行一次，也可以定期執行。

讓我們舉一個在中建立的「Luma應用程式開啟和簽出」段的示例 [生成段](../segment/about-segments.md) 用例。 通過「讀取段」活動，您可以讓屬於此段的所有個人進入行程，並讓他們進入個性化的行程，從而利用所有行程功能：條件，計時器，事件，動作。

>[!NOTE]
>
>若為使用讀取區段活動的歷程，則有最多可同時開始的歷程次數。 系統將執行重試，但請避免在完全相同的時間，開始超過五個歷程 (使用讀取區段、排程或「盡快」)，方法是將其分散在一段時間內，例如相隔 5 到 10 分鐘。
>
>從「讀取」區段、「區段」資格或業務事件活動開始的歷程中，無法使用體驗事件欄位群組。 

### 配置活動 {#configuring-segment-trigger-activity}

配置「讀取段」活動的步驟如下：

1. 展開 **[!UICONTROL 業務流程]** 類別並刪除 **[!UICONTROL 讀取段]** 活動到畫布中。

   活動必須定位為旅程的第一步。

1. 添加 **[!UICONTROL 標籤]** （可選）。

1. 在 **[!UICONTROL 段]** 欄位，選擇將輸入行程的Adobe Experience Platform段，然後按一下 **[!UICONTROL 保存]**。

   請注意，您可以自定義清單中顯示的列並對其進行排序。

   >[!NOTE]
   >
   >只有那些 **已實現** 和 **現有** 段參與狀態將輸入行程。 有關如何評估段的詳細資訊，請參閱 [分段服務文檔](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}。

   ![](assets/read-segment-selection.png)

   添加段後， **[!UICONTROL 複製]** 按鈕，您可以複製其名稱和ID:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. 在 **[!UICONTROL 命名空間]** 欄位中，選擇要用於標識個人的命名空間。 預設情況下，該欄位預填充了上次使用的命名空間。 [瞭解有關命名空間的詳細資訊](../event/about-creating.md#select-the-namespace)。

   >[!NOTE]
   >
   >屬於在不同身份中沒有選定身份（命名空間）的段的個人無法進入行程。 您只能選擇基於人的身份命名空間。 如果已為查找表定義了命名空間(例如：產品查找的ProductID命名空間)，在 **命名空間** 下拉清單。

1. 設定 **[!UICONTROL 限制速率]** 欄位到讀取段活動的吞吐量限制。

   此值儲存在行程版本負載中。 預設值為每秒5,000條消息。 您可以將此值從每秒500條修改為每秒20,000條消息。

   >[!NOTE]
   >
   >每個沙盒的總限制速率設定為每秒20,000條消息。 因此，在同一沙箱中同時運行的所有讀取段的頻寬限制速率每秒最多可增加20,000條消息。 您不能修改此帽。

1. 的 **[!UICONTROL 讀取段]** 活動允許您指定段進入行程的時間。 要執行此操作，請按一下 **[!UICONTROL 編輯行程計畫]** 連結以訪問行程的屬性，然後配置 **[!UICONTROL 調度程式類型]** 的子菜單。

   ![](assets/read-segment-schedule.png)

   預設情況下，段輸入行程 **[!UICONTROL 盡快]**。 如果要使段按特定日期/時間或循環基準輸入行程，請從清單中選擇所需值。

   >[!NOTE]
   >
   >請注意 **[!UICONTROL 計畫]** 只有在 **[!UICONTROL 讀取段]** 活動已被放到畫布中。

   ![](assets/read-segment-schedule-list.png)

   **增量讀取** 選項：一次性的旅行 **讀取段** 首次執行時，段中的所有配置檔案都會進入行程。 此選項允許您在第一次出現後僅針對自上次執行行程後進入段的個人。

   **重複時強制重入**:此選項允許您使行程中仍然存在的所有配置檔案在下次執行時自動退出。 例如，如果您在每天的重複行程中等待2天，則通過激活此選項，配置檔案將始終在下次行程執行時移動（因此在次日），無論它們是否在下一次運行訪問對象中。 如果此行程中配置檔案的壽命可能長於重複頻率，請不要激活此選項以確保配置檔案可以完成其行程。

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>一次性讀取段行程在行程執行30天後移至「已完成」狀態。 對於已排程的讀取區段，是在上次執行該事件後的 30 天。 

### 測試並發佈歷程 {#testing-publishing}

的 **[!UICONTROL 讀取段]** 活動允許您在單一配置檔案上或在100個隨機test從限定段的配置檔案中選擇的配置檔案上test行程。

為此，請激活test模式，然後從左窗格中選擇所需選項。

![](assets/read-segment-test-mode.png)

然後，您可以像往常一樣配置和運行test模式。 [瞭解如何test旅程](testing-the-journey.md)。

一旦test開始運行， **[!UICONTROL 顯示日誌]** 按鈕，您可以根據選定的test選項查看test結果：

* **[!UICONTROL 一次只配置一個]**:test日誌顯示與使用統一test模式時相同的資訊。 有關此內容的詳細資訊，請參閱 [此部分](testing-the-journey.md#viewing_logs)

* **[!UICONTROL 一次最多100個配置檔案]**:test日誌允許您跟蹤從Adobe Experience Platform導出的段的進度以及所有進入此行程的人員的個人進度。

   請注意，一次使用最多100個配置檔案測試行程不允許您使用視覺流跟蹤行程中的個人的進度。

   ![](assets/read-segment-log.png)

test成功後，您可以發佈您的行程(請參閱 [發佈旅程](publishing-the-journey.md))。 屬於該段的個人將在行程的屬性中指定的日期/時間輸入行程 **[!UICONTROL 調度程式]** 的子菜單。

>[!NOTE]
>
>對於基於循環段的旅程，一旦執行最後一次出現，該行程將自動關閉。 如果未指定結束日期/時間，則必須手動關閉新入口的行程以結束。

## 基於段的旅程中的受眾目標

基於段的旅程始終以 **讀取段** 活動，以檢索屬於Adobe Experience Platform段的個人。

屬於該段的受眾被定期檢索一次。

進入此行程後，您可以建立受眾業務流程使用案例，使初始段中的個人流入此行程的不同分支。

**區段**

可以使用條件執行分割 **條件** 的子菜單。 例如，您可VIP以使人員沿特定路徑VIP而不沿另一路徑流動。

分割可以基於：

* 資料源資料
* 事件的上下文部分行程資料，例如：一個人點擊了一小時前收到的消息嗎？
* 例如，日期：我們是在6月，一個人走完這趟旅程嗎？
* 例如：是早上在人的時區嗎？
* 一種算法，它根據百分比分割在旅途中流動的觀眾，例如：90% - 10%排除控制組

![](assets/read-segment-audience1.png)

**排除**

相同 **條件** 用於分割的活動（請參閱上文）還允許您排除部分人口。 例如，您可以排VIP除人員，方法是將人員流入分支中，並且在分支後立即執行結束步驟。

這種排除可能在段檢索後立即發生，用於人口計數目的或沿著多步旅行。

![](assets/read-segment-audience2.png)

**Union**

通過分段，您可以建立N個分支，並將它們連接在一起。

因此，可以讓兩個觀眾回到共同的體驗。

例如，在旅途中的十天中，在經歷了不同的體驗後，VIP非客戶VIP可以回到同一條路上。

合併後，可以通過執行分段或排除來再次分割受眾。

![](assets/read-segment-audience3.png)
