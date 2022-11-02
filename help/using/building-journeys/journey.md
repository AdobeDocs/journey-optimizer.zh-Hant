---
solution: Journey Optimizer
product: journey optimizer
title: 一般原則
description: 一般原則
feature: Journeys
topic: Content Management
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 992f1ee215cc7f14d7f29a0bd592838fead2568c
workflow-type: tm+mt
source-wordcount: '1253'
ht-degree: 8%

---

# 一般原則{#jo-general-principle}

[!DNL Journey Optimizer]可讓您善用儲存在事件或資料來源中的情境資料，建立即時協調使用案例。

設計由下列功能提供支援的多步驟進階案例：

* 傳送在收到事件時觸發的即時&#x200B;**單一傳遞**，或使用 Adobe Experience Platform 分段&#x200B;**批次**&#x200B;傳遞。

* 利用來自事件的&#x200B;**情境資料** 、來自 Adobe Experience Platform 的資訊，或來自協力廠商 API 服務的資料。

* 使用 **內建動作** 發送設計在 [!DNL Journey Optimizer] 或建立 **自訂動作** 如果您使用協力廠商系統來傳送訊息。

* 使用&#x200B;**歷程設計器**，建立您的多步驟使用案例：輕鬆拖放登入事件或讀取區段活動、新增條件及傳送個人化訊息。

## 歷程生命週期{#journey-lifecyle}

### 歷程中的設定檔{#profile-journey}

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


### 歷程結束{#journey-ending}

歷程可能會在兩種特定情境中針對個人結束：

* 人員到達路徑的最後一個活動。
* 人到達 **條件** 活動(或 **等待** 活動（具有條件），且不符合任何條件。

如果允許重新進入，則人員可以重新進入歷程。 請參閱 [本頁](../building-journeys/journey-gs.md#change-properties)

若要終止即時歷程，建議您關閉該歷程。 接著，歷程中的新客戶將會遭到封鎖。 已進入歷程的客戶可以體驗到最後。 請參閱 [本節](../building-journeys/journey.md#close-journey)

只有在發生緊急狀況且所有處理作業都需要在歷程中立即結束時，您才能停止歷程。 已進入歷程的人都會停止進行。 請參閱 [本節](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>請注意，您無法繼續已關閉或已停止的歷程。

#### 歷程結束標籤{#end-tag}

編寫歷程時，每個路徑的結尾會顯示「結束標籤」。 用戶無法添加此節點，無法刪除此節點，只能更改其標籤。 它會標籤歷程的每個路徑的結尾。 如果歷程有數個路徑，建議您在每個結尾新增標籤，讓報表更容易閱讀。 請參閱[此頁面](../reports/live-report.md)。

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

#### 結束歷程{#close-journey}

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

#### 停止歷程{#stop-journey}

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



## 歷程版本{#journey-versions}

在歷程清單中，所有歷程版本都會以版本號碼顯示。 請參閱[此頁面](../building-journeys/using-the-journey-designer.md)。

當您搜尋歷程時，最新版本會在首次開啟應用程式時出現在清單頂端。 然後，您可以定義所要的排序，而應用程式會將其保留為使用者偏好設定。 歷程的版本也會顯示在歷程版本介面的頂端、畫布上方。

![](assets/journeyversions1.png)

>[!NOTE]
>
>在大多數情況下，設定檔無法同時在同一歷程中出現多次。 如果已啟用重新進入，設定檔可以重新進入歷程，但必須完全退出歷程的先前例項，才能執行此動作。 [閱讀全文](#journey-ending)

如果您需要修改至即時歷程，請建立新版本的歷程。

1. 開啟您最新版的即時歷程，按一下 **[!UICONTROL 建立新版本]** 並確認。

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能從歷程的最新版本建立新版本。

1. 進行修改，按一下 **[!UICONTROL 發佈]** 並確認。

   ![](assets/journeyversions3.png)

從歷程發佈之時，個人就會開始進入歷程的最新版本。 已輸入舊版的使用者會保留在舊版中，直到完成歷程為止。 如果他們稍後重新進入相同的歷程，將會進入最新版本。

歷程版本可個別停止。 所有版本的歷程都具有相同名稱。

當您發佈新版本的歷程時，舊版會自動結束，並切換至 **已關閉** 狀態。 旅行中的入口是不可能的。 即使您停止最新版本，舊版仍會保持關閉狀態。

>[!NOTE]
>
>進一步了解歷程版本護欄和限制，位於 [本頁](../start/guardrails.md#journey-versions-limitations)