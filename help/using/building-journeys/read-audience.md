---
solution: Journey Optimizer
product: journey optimizer
title: 在歷程中使用對象
description: 瞭解如何在歷程中使用對象
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 活動，歷程，讀取，對象，平台
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 2%

---

# 在歷程中使用對象 {#segment-trigger-activity}

## 新增讀取對象活動 {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="讀取對象活動"
>abstract="「讀取對象」活動可讓您讓屬於Adobe Experience Platform對象的所有個人進入歷程。 進入歷程可以執行一次，也可以定期執行。"

使用 **讀取對象** 讓對象的所有個人進入歷程的活動。 進入歷程可以執行一次，也可以定期執行。

以中建立的「Luma應用程式開啟和結帳」受眾為例。 [建立對象](../audience/about-audiences.md) 使用案例。 透過「讀取對象」活動，您可以讓屬於此對象的所有個人進入歷程，並讓他們流入將運用所有歷程功能（條件、計時器、事件、動作）的個人化歷程。

>[!NOTE]
>
>若為使用讀取對象活動的歷程，則有最多可同時開始的歷程次數。 系統將執行重試，但請避免在完全相同的時間，開始超過五個歷程（讀取對象、排程或「儘快」），方法是將其分散在一段時間內，例如相隔5到10分鐘。
>
>體驗事件欄位群組不能用於以讀取對象、對象資格或業務事件活動開始的歷程。

### 設定活動 {#configuring-segment-trigger-activity}

設定「讀取對象」活動的步驟如下：

1. 展開 **[!UICONTROL 協調流程]** 類別與放置 **[!UICONTROL 讀取對象]** 活動放入您的畫布。

   活動必須定位為歷程的第一步。

1. 新增 **[!UICONTROL 標籤]** 至活動（選用）。

1. 在 **[!UICONTROL 對象]** 欄位，選擇將進入歷程的Adobe Experience Platform對象，然後按一下 **[!UICONTROL 儲存]**.

   請注意，您可以自訂清單中顯示的欄並加以排序。

   >[!NOTE]
   >
   >只有具備下列條件的個人 **已實現** 和 **現有** 對象參與狀態將進入歷程。 如需如何評估對象的詳細資訊，請參閱 [Segment Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

   ![](assets/read-segment-selection.png)

   在新增對象後， **[!UICONTROL 複製]** 按鈕可讓您複製其名稱和ID：

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. 在 **[!UICONTROL 名稱空間]** 欄位，選擇要使用的名稱空間以識別個人。 依預設，欄位會使用上次使用的名稱空間預先填入。 [進一步瞭解名稱空間](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >如果屬於某個受眾的個人在其不同身分中沒有所選身分（名稱空間），則無法進入歷程。 您只能選取以人物為基礎的身分名稱空間。 如果您已定義查閱表格的名稱空間（例如：產品查閱的ProductID名稱空間），它將無法在 **名稱空間** 下拉式清單。

1. 設定 **[!UICONTROL 節流率]** 欄位至讀取對象活動的輸送量限制。

   此值會儲存在歷程版本裝載中。 預設值為每秒5,000則訊息。 您可以將此值從每秒500則訊息修改為每秒20,000則訊息。

   >[!NOTE]
   >
   >每個沙箱的整體節流率設定為每秒20,000則訊息。 因此，在同一沙箱中同時執行的所有讀取對象節流率每秒最多可新增20,000則訊息。 您無法修改此上限。

1. 此 **[!UICONTROL 讀取對象]** 活動可讓您指定對象將進入歷程的時間。 若要這麼做，請按一下 **[!UICONTROL 編輯歷程排程]** 連結以存取歷程的屬性，然後設定 **[!UICONTROL 排程器型別]** 欄位。

   ![](assets/read-segment-schedule.png)

   依預設，對象會進入歷程 **[!UICONTROL 儘快]**. 如果您想要讓對象在特定日期/時間或循環的基礎上進入歷程，請從清單中選取所需的值。

   >[!NOTE]
   >
   >請注意 **[!UICONTROL 排程]** 區段僅在以下情況下可用： **[!UICONTROL 讀取對象]** 已在畫布中捨棄活動。

   ![](assets/read-segment-schedule-list.png)

   **增量讀取** 選項：當具有週期性歷程時 **讀取對象** 第一次執行時，對象中的所有設定檔都會進入歷程。 此選項可讓您在第一次發生後，只將目標鎖定在自上次執行歷程以來進入對象的個人。

   **在重複時強制重新進入**：此選項可讓您讓歷程中仍存在的所有設定檔在下次執行時自動退出。 例如，如果您在每日循環歷程中等候2天，透過啟用此選項，設定檔將一律會在下次歷程執行（也就是之後的那天）中移動，無論它們是否在下次執行的對象中。 如果此歷程中設定檔的生命週期可能長於週期性頻率，請勿啟用此選項以確保設定檔可完成其歷程。

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
>一次性讀取對象歷程在歷程執行30天後會移至「已完成」狀態。 對於已排程的讀取閱聽眾，是在上次執行後的30天。

### 測試並發佈歷程 {#testing-publishing}

此 **[!UICONTROL 讀取對象]** 活動可讓您在單一設定檔上測試歷程，或在符合對象資格之設定檔中隨機選取的100個測試設定檔上測試歷程。

若要這麼做，請啟動測試模式，然後從左窗格中選取所需的選項。

![](assets/read-segment-test-mode.png)

然後您可以照常設定並執行測試模式。 [瞭解如何測試歷程](testing-the-journey.md).

測試執行後， **[!UICONTROL 顯示記錄]** 按鈕可讓您根據選取的測試選項檢視測試結果：

* **[!UICONTROL 一次一個設定檔]**：測試記錄會顯示與使用單一測試模式時相同的資訊。 有關詳細資訊，請參閱 [本節](testing-the-journey.md#viewing_logs)

* **[!UICONTROL 一次最多100個設定檔]**：測試記錄檔可讓您追蹤從Adobe Experience Platform匯出對象的進度，以及所有進入歷程人員的個人進度。

  請注意，一次使用最多100個設定檔測試歷程不允許您使用視覺流程追蹤歷程中個人的進度。

  ![](assets/read-segment-log.png)

測試成功後，您就可以發佈歷程(請參閱 [發佈歷程](publishing-the-journey.md))。 屬於對象的個人將在歷程屬性中指定的日期/時間進入歷程 **[!UICONTROL 排程器]** 區段。

>[!NOTE]
>
>對於循環的對象型歷程，該歷程將在執行其最後一次發生次數後自動關閉。 如果未指定結束日期/時間，您必須手動將歷程關閉至新入口，才能將其結束。

## 受眾型歷程中的受眾目標定位

受眾型歷程一律以 **讀取對象** 活動以擷取屬於Adobe Experience Platform對象的個人。

屬於對象的對象會擷取一次或定期擷取。

進入歷程後，您可以建立受眾協調使用案例，讓初始受眾的個人進入歷程的不同分支。

**區段**

您可以使用條件來執行分段，方法是 **條件** 活動。 例如，您可以讓VIP人員採用特定路徑，而非VIP人員則採用其他路徑。

區段可根據：

* 資料來源資料
* 歷程資料中事件部分的內容，例如：有人點按了一小時前收到的訊息嗎？
* 日期，例如：某人瀏覽歷程時，我們是在6月嗎？
* 時間，例如：現在是個人時區的早上嗎？
* 根據百分比分割歷程中流動的對象的演演算法，例如：90% - 10%以排除控制組

![](assets/read-segment-audience1.png)

**排除**

相同 **條件** 用於區段的活動（請參閱上文）也可讓您排除部分母體。 例如，您可以排除VIP人員，方法是讓他們流入後面有結束步驟的分支。

此排除作業可能會發生在對象擷取之後、基於母體計數目的或沿著多步驟歷程進行。

![](assets/read-segment-audience2.png)

**Union**

歷程可讓您建立N個分支，並在分段後將其聯結。

因此，您可以讓兩個受眾回到共同體驗。

例如，在歷程中連續十天追蹤不同體驗後，VIP和非VIP客戶可以返回相同路徑。

聯合後，您可以執行細分或排除來再次分割對象。

![](assets/read-segment-audience3.png)
