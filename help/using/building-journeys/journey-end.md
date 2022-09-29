---
title: 結束歷程
description: 結束歷程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 57bdeadc-5801-4036-a272-c622634d5281
source-git-commit: cca94d15da5473aa9890c67af7971f2e745d261e
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 1%

---

# 歷程生命週期{#journey-lifecyle}

## 歷程中的設定檔{#profile-journey}

在單一歷程中：

* 如果已啟用重新進入，設定檔可以進入歷程數次，但必須完全退出歷程的先前例項，才能進行。

* 如果停用重新進入，設定檔就無法多次輸入相同的歷程

如需設定檔重新進入的詳細資訊，請參閱 [節](../building-journeys/journey-gs.md#change-properties).

在讀取區段歷程中：

* 對於非循環歷程：設定檔會進入歷程一次，而且只進入一次。
* 針對循環歷程：如果設定檔處於區段/預期狀態，則會在每次重複執行時進入歷程。 如果他仍在前一次的復期歷程中，會從頭開始重新開始。

在從讀取區段開始的商業事件歷程中：

知道此歷程是以接收業務事件為基礎，如果設定檔符合預期區段的資格，他將為收到的每個業務事件輸入歷程，這表示此設定檔可在相同歷程中多次，同時，但位在不同業務事件的情境中。

單一歷程（從事件或區段資格開始）包含防止同一事件多次錯誤觸發歷程的護欄。 設定檔重新進入預設會暫時封鎖5分鐘。 例如，如果某個事件在12:01對特定設定檔觸發歷程，而另一個事件在12:03到達（無論是相同事件或是不同事件觸發相同歷程），該歷程將不會對此設定檔重新開始。


## 歷程結束{#journey-ending}

歷程可能會在兩種特定情境中針對個人結束：

* 人員到達路徑的最後一個活動。
* 人到達 **條件** 活動(或 **等待** 活動（具有條件），且不符合任何條件。

如果允許重新進入，則人員可以重新進入歷程。 請參閱 [本頁](../building-journeys/journey-gs.md#change-properties)

若要終止即時歷程，建議您關閉該歷程。 接著，歷程中的新客戶將會遭到封鎖。 已進入歷程的客戶可以體驗到最後。 請參閱 [本節](../building-journeys/journey-end.md#close-journey)

只有在發生緊急狀況且所有處理作業都需要在歷程中立即結束時，您才能停止歷程。 已進入歷程的人都會停止進行。 請參閱 [本節](../building-journeys/journey-end.md#stop-journey)

>[!NOTE]
>
>請注意，您無法繼續已關閉或已停止的歷程。

### 歷程結束標籤{#end-tag}

編寫歷程時，每個路徑的結尾會顯示「結束標籤」。 用戶無法添加此節點，無法刪除此節點，只能更改其標籤。 它會標籤歷程的每個路徑的結尾。 如果歷程有數個路徑，建議您在每個結尾新增標籤，讓報表更容易閱讀。 請參閱[此頁面](../reports/live-report.md)。

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

### 結束歷程{#close-journey}

歷程可能會關閉，原因如下：

* 歷程會透過 **[!UICONTROL 靠近新入口]** 按鈕。
* 已完成執行的單次區段型歷程。
* 上次發生循環區段型歷程後。

手動關閉歷程可確保已進入歷程的客戶能夠完成其路徑，但新使用者無法進入歷程。 歷程關閉時（基於上述任何原因），其狀態都會是 **[!UICONTROL 已關閉]**. 歷程不再讓新人進入歷程。 已在歷程中的人員可正常完成歷程。 在30天的預設全域逾時後，歷程會切換至 **已完成** 狀態。 看這個 [節](../building-journeys/journey-gs.md#global_timeout).

無法重新啟動或刪除已關閉的歷程版本。 您可以建立新版本或加以複製。 只能刪除已完成的歷程。

若要從歷程清單關閉歷程，請按一下 **[!UICONTROL 刪節號]** 位於歷程名稱右側的按鈕，然後選取 **[!UICONTROL 靠近新入口]**.

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL 歷程]** 清單中，按一下您要關閉的歷程。
1. 按一下右上角的向下箭頭。

   ![](assets/finish_drop_down_list.png)

1. 按一下 **[!UICONTROL 靠近新入口]**，並在對話方塊中確認。

### 停止歷程{#stop-journey}

如果您需要停止歷程中所有個人的進度，您可以加以停止。 停止歷程會逾時歷程中的所有個人。 但是，停止歷程牽涉到已進入歷程的人，都會在進行中停止。 旅程基本上被關閉。 如果您想要結束歷程，建議您關閉歷程。

無法重新啟動已停止的歷程版本。

停止時，歷程狀態會設為 **[!UICONTROL 已停止]**.

例如，如果行銷人員發現歷程鎖定了錯誤的對象或傳送訊息的自訂動作無法正確運作，您就可以停止歷程。 若要從歷程清單中停止歷程，請按一下 **[!UICONTROL 刪節號]** 位於歷程名稱右側的按鈕，然後選取 **[!UICONTROL 停止]**.

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL 歷程]** 清單中，按一下您要停止的歷程。
1. 按一下右上角的向下箭頭。
   ![](assets/finish_drop_down_list.png)
1. 按一下 **[!UICONTROL 停止]**，並在對話方塊中確認。
