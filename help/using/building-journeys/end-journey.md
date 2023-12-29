---
solution: Journey Optimizer
product: journey optimizer
title: 歷程結束
description: 瞭解歷程如何在Journey Optimizer中結束
feature: Journeys
role: User
level: Intermediate
keywords: 重新進入、歷程、結束、即時、停止
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 1%

---

# 結束歷程{#journey-ending}

歷程可以在兩個特定情境中為個人結束：

* 該人員到達路徑的最後一個活動。
* 人員到達 **條件** 活動(或 **等待** 活動（含條件），且不符合任何條件。

如果允許重新進入，則人員可以重新進入歷程。 另請參閱 [此頁面](../building-journeys/journey-gs.md#change-properties)

若要終止即時歷程，建議您將其關閉。 接著，歷程中的新客戶將遭到封鎖。 已進入歷程的客戶能夠體驗到結束。 另請參閱 [本節](../building-journeys/journey.md#close-journey)

只有在發生緊急狀況且所有處理作業需要在歷程中立即結束時，您才能停止歷程。 已進入歷程的人員都在進度中停止。 另請參閱 [本節](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>請注意，您無法繼續已關閉或已停止的歷程。

## 歷程結束標籤{#end-tag}

製作歷程時，每個路徑的結尾都會顯示「結束標籤」。 此節點無法由使用者新增、無法移除，而且只能變更其標籤。 它會標籤歷程每個路徑的結尾。 如果歷程有數個路徑，我們建議您在每個結尾新增標籤，讓報告更易於閱讀。 請參閱[此頁面](../reports/live-report.md)。

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## 關閉歷程{#close-journey}

歷程可以關閉，原因如下：

* 歷程已透過手動關閉 **[!UICONTROL 關閉新入口]** 按鈕。
* 已完成的單次區段型歷程。
* 在最後一次發生循環對象型歷程之後。

手動關閉歷程可確保已進入歷程的客戶完成其路徑，但新使用者無法進入歷程。 歷程關閉時（基於上述任何原因），會有狀態 **[!UICONTROL 已關閉]**. 歷程停止讓新個人進入歷程。 已在歷程中的人可以正常完成歷程。 在預設全域逾時30天後，歷程將切換為 **已完成** 狀態。 請參閱[本章節](../building-journeys/journey-gs.md#global_timeout)。

無法重新啟動或刪除已關閉的歷程版本。 您可以建立其新版本或加以複製。 只能刪除已完成的歷程。

若要從歷程清單關閉歷程，請按一下 **[!UICONTROL 省略符號]** 位於歷程名稱右側的按鈕並選取 **[!UICONTROL 關閉新入口]**.

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL 歷程]** 清單中，按一下您要關閉的歷程。
1. 在右上方，按一下向下箭頭。

   ![](assets/finish_drop_down_list.png)

1. 按一下 **[!UICONTROL 關閉新入口]**，並在對話方塊中確認。

## 停止歷程{#stop-journey}

如果您需要停止歷程中所有個人的進度，可以停止它。 停止歷程將逾時歷程中的所有個人。 但是，停止歷程涉及已經進入歷程的人都在他們的進度中停止。 歷程已基本關閉。 如果您想要結束歷程，我們建議您將其關閉。

無法重新啟動停止的歷程版本。

停止時，歷程狀態會設為 **[!UICONTROL 已停止]**.

例如，如果行銷人員發現歷程鎖定了錯誤的對象，或應該傳送訊息的自訂動作無法正常運作，則可以停止歷程。 若要從歷程清單停止歷程，請按一下 **[!UICONTROL 省略符號]** 位於歷程名稱右側的按鈕並選取 **[!UICONTROL 停止]**.

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL 歷程]** 清單中，按一下您要停止的歷程。
1. 在右上方，按一下向下箭頭。
   ![](assets/finish_drop_down_list.png)
1. 按一下 **[!UICONTROL 停止]**，並在對話方塊中確認。
