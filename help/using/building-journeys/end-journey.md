---
solution: Journey Optimizer
product: journey optimizer
title: 旅程結束
description: 瞭解旅程在Journey Optimizer結束
feature: Journeys
role: User
level: Beginner
keywords: 返航，旅程，結束，實況，停止
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 1%

---

# 結束旅程{#journey-ending}

在以下兩種特定情況下，個人可以結束行程：

* 該人到達了路徑的最後一個活動。
* 這個人到達 **條件** 活動(或 **等待** 具有條件的活動)，且與任何條件不匹配。

如果允許重新進入，則人員可以重新進入旅程。 請參閱 [此頁](../building-journeys/journey-gs.md#change-properties)

要終止即時旅程，我們建議您關閉它。 然後，新客戶在旅途中的抵達將被阻止。 已經進入旅程的客戶能夠體驗到它。 請參閱 [此部分](../building-journeys/journey.md#close-journey)

只有在發生緊急情況並且所有處理需要在旅途中立即結束時，您才能停止旅程。 已經踏上旅程的人，都被阻止了。 請參閱 [此部分](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>請注意，您無法恢復已關閉或已停止的行程。

## 行程結束標籤{#end-tag}

在編寫行程時，每個路徑的末尾顯示「結束標籤」。 此節點不能由用戶添加，無法刪除，只能更改其標籤。 它標誌著旅程的每條路的結束。 如果行程中有多條路徑，建議您在每一端添加一個標籤，以便更容易閱讀報告。 請參閱[此頁面](../reports/live-report.md)。

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## 結束旅程{#close-journey}

行程可能會關閉，原因如下：

* 通過 **[!UICONTROL 接近新入口]** 按鈕
* 已完成執行的基於單次段的行程。
* 上次出現基於週期段的行程之後。

手動結束行程可確保已輸入行程的客戶可以完成其行程，但新用戶無法進入行程。 當行程關閉時（出於以上任何原因），它將具有 **[!UICONTROL 已關閉]**。 旅程不再讓新人進入旅程。 已經在旅途中的人可以正常地完成旅程。 在預設全局超時30天後，該行程將切換到 **已完成** 狀態。 請參閱[本章節](../building-journeys/journey-gs.md#global_timeout)。

無法重新啟動或刪除已結束的行程版本。 您可以建立新版本或複製該版本。 只能刪除已完成的行程。

要從旅程清單中關閉行程，請按一下 **[!UICONTROL 省略號]** 按鈕，選擇 **[!UICONTROL 接近新入口]**。

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL 旅程]** 清單中，按一下要關閉的行程。
1. 在右上角，按一下向下箭頭。

   ![](assets/finish_drop_down_list.png)

1. 按一下 **[!UICONTROL 接近新入口]**，並在對話框中進行確認。

## 停止旅行{#stop-journey}

如果你需要阻止所有人在旅途中的進步，你可以阻止它。 停止行程將超時行程中的所有人。 但是，旅途的停止，涉及已經踏上旅程的人，都被阻止了。 旅程基本上被關閉了。 如果您想結束旅程，我們建議您關閉它。

無法重新啟動已停止的行程版本。

停止時，行程狀態設定為 **[!UICONTROL 已停止]**。

例如，如果營銷人員意識到此行程針對的是錯誤的受眾，或者傳遞消息的自定義操作不能正常工作，您就可以停止此行程。 要停止從行程清單中的行程，請按一下 **[!UICONTROL 省略號]** 按鈕，選擇 **[!UICONTROL 停止]**。

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL 旅程]** 清單中，按一下要停止的行程。
1. 在右上角，按一下向下箭頭。
   ![](assets/finish_drop_down_list.png)
1. 按一下 **[!UICONTROL 停止]**，並在對話框中進行確認。
