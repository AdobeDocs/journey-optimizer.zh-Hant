---
solution: Journey Optimizer
product: journey optimizer
title: 歷程結束
description: 了解歷程在Journey Optimizer中的結束方式
feature: Journeys
role: User
level: Beginner
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# 結束歷程{#journey-ending}

歷程可能會在兩種特定情境中針對個人結束：

* 人員到達路徑的最後一個活動。
* 人到達 **條件** 活動(或 **等待** 活動（具有條件），且不符合任何條件。

如果允許重新進入，則人員可以重新進入歷程。 請參閱 [本頁](../building-journeys/journey-gs.md#change-properties)

若要終止即時歷程，建議您關閉該歷程。 接著，歷程中的新客戶將會遭到封鎖。 已進入歷程的客戶可以體驗到最後。 請參閱 [本節](../building-journeys/journey.md#close-journey)

只有在發生緊急狀況且所有處理作業都需要在歷程中立即結束時，您才能停止歷程。 已進入歷程的人都會停止進行。 請參閱 [本節](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>請注意，您無法繼續已關閉或已停止的歷程。

## 歷程結束標籤{#end-tag}

編寫歷程時，每個路徑的結尾會顯示「結束標籤」。 用戶無法添加此節點，無法刪除此節點，只能更改其標籤。 它會標籤歷程的每個路徑的結尾。 如果歷程有數個路徑，建議您在每個結尾新增標籤，讓報表更容易閱讀。 請參閱 [本頁](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## 結束歷程{#close-journey}

歷程可能會關閉，原因如下：

* 歷程會透過 **[!UICONTROL Close to new entrances]** 按鈕。
* 已完成執行的單次區段型歷程。
* 在上次發生週期性區段型歷程之後。

手動關閉歷程可確保已進入歷程的客戶能夠完成其路徑，但新使用者無法進入歷程。 歷程關閉時（基於上述任何原因），其狀態都會是 **[!UICONTROL Closed]**. 歷程不再讓新人進入歷程。 已在歷程中的人員可正常完成歷程。 在30天的預設全域逾時後，歷程會切換至 **已完成** 狀態。 看這個 [節](../building-journeys/journey-gs.md#global_timeout).

無法重新啟動或刪除已關閉的歷程版本。 您可以建立新版本或加以複製。 只能刪除已完成的歷程。

若要從歷程清單關閉歷程，請按一下 **[!UICONTROL Ellipsis]** 位於歷程名稱右側的按鈕，然後選取 **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL Journeys]** 清單中，按一下您要關閉的歷程。
1. 按一下右上角的向下箭頭。

   ![](assets/finish_drop_down_list.png)

1. 按一下 **[!UICONTROL Close to new entrances]**，並在對話方塊中確認。

## 停止歷程{#stop-journey}

如果您需要停止歷程中所有個人的進度，您可以加以停止。 停止歷程會逾時歷程中的所有個人。 但是，停止歷程牽涉到已進入歷程的人，都會在進行中停止。 旅程基本上被關閉。 如果您想要結束歷程，建議您關閉歷程。

無法重新啟動已停止的歷程版本。

停止時，歷程狀態會設為 **[!UICONTROL Stopped]**.

例如，如果行銷人員發現歷程鎖定了錯誤的對象或傳送訊息的自訂動作無法正確運作，您就可以停止歷程。 若要從歷程清單中停止歷程，請按一下 **[!UICONTROL Ellipsis]** 位於歷程名稱右側的按鈕，然後選取 **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL Journeys]** 清單中，按一下您要停止的歷程。
1. 按一下右上角的向下箭頭。
   ![](assets/finish_drop_down_list.png)
1. 按一下 **[!UICONTROL Stop]**，並在對話方塊中確認。
