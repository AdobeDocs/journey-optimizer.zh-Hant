---
title: 在旅程中使用區段
description: 瞭解如何在歷程中使用細分
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 2%

---

# 在歷程{#segment-trigger-activity}中使用區段

![](../assets/do-not-localize/badge.png)

## 關於讀取段活動{#about-segment-trigger-actvitiy}

「讀取區段」活動可讓您讓屬於Adobe Experience Platform區段的所有個人進入歷程。 進入歷程可以執行一次，也可以定期執行。

讓我們以[Build segments](../segment/about-segments.md)使用案例中建立的「Luma應用程式開啟與結帳」區段為例。 透過「讀取區段」活動，您可以讓屬於此區段的所有個人進入歷程，並讓他們進入個人化歷程，以運用所有歷程功能：條件、計時器、事件、動作。

>[!NOTE]
>
>無法在1小時以內的較短時間內觸發以區段為基礎的歷程。

### 配置活動{#configuring-segment-trigger-activity}

設定「讀取」區段活動的步驟如下：

1. 展開&#x200B;**[!UICONTROL Orchestration]**&#x200B;類別，並將&#x200B;**[!UICONTROL Read Segment]**&#x200B;活動拖曳至畫布中。

   活動必須定位為旅程的第一步。

1. 新增&#x200B;**[!UICONTROL Label]**&#x200B;至活動（選用）。

1. 在&#x200B;**[!UICONTROL Segment]**&#x200B;欄位中，選擇將進入歷程的Adobe Experience Platform區段，然後按一下&#x200B;**[!UICONTROL Save]**。

   請注意，您可以自訂清單中顯示的欄，並加以排序。

   >[!NOTE]
   >
   >只有具有&#x200B;**Emariabled**&#x200B;和&#x200B;**Existing**&#x200B;區段參與狀態的個人才會進入歷程。 如需如何評估區段的詳細資訊，請參閱[區段服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results)。

   ![](../assets/read-segment-selection.png)

   新增區段後，**[!UICONTROL Copy]**&#x200B;按鈕可讓您複製其名稱和ID:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](../assets/read-segment-copy.png)

1. 在&#x200B;**[!UICONTROL Namespace]**&#x200B;欄位中，選擇要使用的命名空間以識別個人。 [進一步瞭解命名空間](../event/about-creating.md#select-the-namespace)。

   >[!NOTE]
   >
   >屬於不同身分之間沒有選取身分（命名空間）之群體的個人無法進入歷程。

1. **[!UICONTROL Read Segment]**&#x200B;活動可讓您指定區段將進入歷程的時間。 若要這麼做，請按一下&#x200B;**[!UICONTROL Edit journey schedule]**&#x200B;連結以存取歷程的屬性，然後設定&#x200B;**[!UICONTROL Scheduler type]**&#x200B;欄位。

   ![](../assets/read-segment-schedule.png)

   依預設，區段會輸入歷程&#x200B;**[!UICONTROL As soon as possible]**，這表示歷程發佈後1小時。 如果您要讓區段以特定日期／時間或循環方式輸入歷程，請從清單中選取所需值。

   >[!NOTE]
   >
   >請注意，**[!UICONTROL Schedule]**&#x200B;區段僅在畫布中放置了&#x200B;**[!UICONTROL Read Segment]**&#x200B;活動時可用。

   ![](../assets/read-segment-schedule-list.png)

### 測試並發佈歷程 {#testing-publishing}

**[!UICONTROL Read Segment]**&#x200B;活動可讓您在單一描述檔上或在100個隨機測試從符合區段的描述檔中選取的描述檔上測試歷程。

若要這麼做，請啟動測試模式，然後從左窗格中選取所需的選項。

![](../assets/read-segment-test-mode.png)

然後，您可以照常設定並執行測試模式。 [瞭解如何測試旅程](testing-the-journey.md)。

在測試執行後，**[!UICONTROL Show logs]**&#x200B;按鈕可讓您根據選取的測試選項來查看測試結果：

* **[!UICONTROL Single profile at a time]**:測試日誌顯示與使用統一測試模式時相同的資訊。有關詳細資訊，請參閱[本節](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Up to 100 profiles at once]**:測試記錄可讓您追蹤從Adobe Experience Platform出口區段的進度，以及所有進入旅程的人員的個人進度。

   請注意，一次使用最多100個描述檔來測試旅程，不允許您使用視覺流來追蹤個人在旅程中的進度。

   ![](../assets/read-segment-log.png)

測試成功後，您就可以發佈您的歷程（請參閱[發佈歷程](publishing-the-journey.md)）。 屬於該群體的個人將在旅程的屬性&#x200B;**[!UICONTROL Scheduler]**&#x200B;區段中指定的日期／時間進入旅程。

>[!NOTE]
>
>當執行非循環（「盡快開始」或「一次」）的區段型歷程時，其狀態會自動變更為「已關閉」。
>
>對於循環性區段型歷程，歷程會在最後一次發生時自動關閉。 如果沒有指定結束日期／時間，您必須手動關閉通往新入口的旅程，以結束它。


## 細分歷程中的受眾鎖定

以區段為基礎的歷程一律以&#x200B;**讀取區段**&#x200B;活動開始，以擷取屬於Adobe Experience Platform區段的個人。

屬於區段的觀眾會定期擷取一次。

進入歷程後，您可以建立受眾協調使用案例，讓從最初細分到旅程不同分支的個人都能參與。

**區段**

您可以使用條件來使用&#x200B;**Condition**&#x200B;活動執行分段。 例如，您可讓VIP人們選擇特定路徑，而不VIP流入其他路徑。

區段可以基於：

* 資料源資料
* 例如，事件的上下文部分是歷程資料：有人點擊了她一小時前收到的留言嗎？
* 例如：我們是在六月，當一個人走過這段旅程時嗎？
* 例如：是否是早上在人員的時區？
* 根據百分比來分割旅程中流動的觀眾的演算法，例如：90% - 10%排除控制群組

![](../assets/read-segment-audience1.png)

**排除**

區段使用的相同&#x200B;**Condition**&#x200B;活動（請參閱上文）也可讓您排除部分人口。 例如，您可以排除VIP人員，方法是讓人員在緊接在後面進入具有結束步驟的分支。

此排除可能發生在區段擷取後、用於人口計數或進行多步驟歷程。

![](../assets/read-segment-audience2.png)

**Union**

歷程可讓您建立N個分支，並在劃分後將它們結合在一起。

因此，您可以讓兩個觀眾回到共同的體驗。

例如，在旅程的十天中，在遵循不同的體驗後，VIP非客VIP戶可以回到相同的路徑。

在合併後，您可以執行分段或排除，再次分割觀眾。

![](../assets/read-segment-audience3.png)
