---
title: 結束旅程
description: 結束旅程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 57bdeadc-5801-4036-a272-c622634d5281
source-git-commit: d740b9efdba164f548fb07d6d9a96fc2c2796eff
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 1%

---

# 歷程生命週期{#journey-lifecyle}

## 旅程概況{#profile-journey}

在單一的旅程中：

* 如果啟用重新入門，配置檔案可以多次輸入行程，但在他完全退出此行程的先前實例之前無法執行此操作。

* 如果禁用重新入口，則配置檔案不能多次輸入同一行程

有關配置檔案重新入口的詳細資訊，請參閱此 [節](../building-journeys/journey-gs.md#change-properties)。

在讀段旅程中：

* 對於非循環旅程：資料只輸入一次，只輸入一次。
* 對於循環行程：如果配置檔案處於段/預期狀態，則每次重複時都會進入行程。 如果他還在從前一次的重複中走下去，他將從頭開始重新開始。

在以讀取段開始的商業事件旅程中：

知道此行程是基於業務事件的接收，如果配置檔案在預期的段中得到了資格，他將為收到的每個業務事件輸入行程，這意味著此配置檔案可以在同一行程中多次，同時，但是在不同業務事件的上下文中。

## 旅程結束{#journey-ending}

在以下兩種特定情況下，個人可以結束行程：

* 該人到達了路徑的最後一個活動。
* 這個人到達 **條件** 活動(或 **等待** 具有條件的活動)，且與任何條件不匹配。

如果允許重新進入，則人員可以重新進入旅程。 請參閱 [此頁](../building-journeys/journey-gs.md#change-properties)

要終止即時旅程，我們建議您關閉它。 然後，新客戶在旅途中的抵達將被阻止。 已經進入旅程的客戶能夠體驗到它。 請參閱 [此部分](../building-journeys/journey-end.md#close-journey)

只有在發生緊急情況並且所有處理需要在旅途中立即結束時，您才能停止旅程。 已經踏上旅程的人，都被阻止了。 請參閱 [此部分](../building-journeys/journey-end.md#stop-journey)

>[!NOTE]
>
>請注意，您無法恢復已關閉或已停止的行程。

### 行程結束標籤{#end-tag}

在編寫行程時，每個路徑的末尾顯示「結束標籤」。 此節點不能由用戶添加，無法刪除，只能更改其標籤。 它標誌著旅程的每條路的結束。 如果行程中有多條路徑，建議您在每一端添加一個標籤，以便更容易閱讀報告。 請參閱[此頁面](../reports/live-report.md)。

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

### 結束旅程{#close-journey}

行程可能會關閉，原因如下：

* 通過 **[!UICONTROL Close to new entrances]** 按鈕
* 已完成執行的基於單次段的行程。
* 上次出現基於週期段的行程之後。

手動結束行程可確保已輸入行程的客戶可以完成其行程，但新用戶無法進入行程。 當行程關閉時（出於以上任何原因），它將具有 **[!UICONTROL Closed]**。 旅程不再讓新人進入旅程。 已經在旅途中的人可以正常地完成旅程。 在預設全局超時30天後，該行程將切換到 **已完成** 狀態。 查看 [節](../building-journeys/journey-gs.md#global_timeout)。

無法重新啟動或刪除已結束的行程版本。 您可以建立新版本或複製該版本。 只能刪除已完成的行程。

要從旅程清單中關閉行程，請按一下 **[!UICONTROL Ellipsis]** 按鈕，選擇 **[!UICONTROL Close to new entrances]**。

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL Journeys]** 清單中，按一下要關閉的行程。
1. 在右上角，按一下向下箭頭。

   ![](assets/finish_drop_down_list.png)

1. 按一下 **[!UICONTROL Close to new entrances]**，並在對話框中進行確認。

### 停止旅行{#stop-journey}

如果你需要阻止所有人在旅途中的進步，你可以阻止它。 停止行程將超時行程中的所有人。 但是，旅途的停止，涉及已經踏上旅程的人，都被阻止了。 旅程基本上被關閉了。 如果您想結束旅程，我們建議您關閉它。

無法重新啟動已停止的行程版本。

停止時，行程狀態設定為 **[!UICONTROL Stopped]**。

例如，如果營銷人員意識到此行程針對的是錯誤的受眾，或者傳遞消息的自定義操作不能正常工作，您就可以停止此行程。 要停止從行程清單中的行程，請按一下 **[!UICONTROL Ellipsis]** 按鈕，選擇 **[!UICONTROL Stop]**。

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL Journeys]** 清單中，按一下要停止的行程。
1. 在右上角，按一下向下箭頭。
   ![](assets/finish_drop_down_list.png)
1. 按一下 **[!UICONTROL Stop]**，並在對話框中進行確認。
