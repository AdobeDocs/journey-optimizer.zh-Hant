---
title: 開始體驗歷程
description: 開始體驗歷程
translation-type: tm+mt
source-git-commit: 0b48a0b0793d523021a2e19f86e101bdbab88305
workflow-type: tm+mt
source-wordcount: '1464'
ht-degree: 7%

---

# 開始使用journeys{#jo-quick-start}

![](../assets/do-not-localize/badge.png)

## 先決條件

若要傳送包含歷程的訊息，必須進行下列設定：

1. **設定事件**:如果您想在收到事件時觸發整個歷程，您必須設定事件。您可定義預期的資訊，以及處理方式。 此步驟由&#x200B;**技術使用者**&#x200B;執行。[閱讀全文](../event/about-events.md).

   ![](../assets/jo-event7.png)

1. **建立區段**:您的旅程也可以監聽Adobe Experience Platform區段，以便批次傳送訊息至指定的描述檔集。為此，您需要建立區段。 [閱讀全文](../segment/about-segments.md).

   ![](../assets/segment2.png)

1. **設定資料來源**:您可以定義系統的連線，以擷取將用於歷程的其他資訊，例如在您的條件中。佈建時也會設定內建的 Adobe Experience Platform 資料來源。如果您只會運用歷程中事件的資料，則不需要執行此步驟。此步驟由&#x200B;**技術使用者**&#x200B;執行。[閱讀全文](../datasource/about-data-sources.md)

   ![](../assets/jo-datasource.png)

1. **設定動作**:Journey Optimizer的訊息功能已內建，您只需要設計內容並發佈訊息。請參閱[本節](../get-started-content.md)。如果您使用協力廠商系統來傳送訊息，可以建立自訂動作。 請參閱[一節](../action/action.md)瞭解更多資訊。 此步驟由&#x200B;**技術使用者**&#x200B;執行。

   ![](../assets/create-content-push.png)

## 建立您的旅程{#jo-build}

此步驟由&#x200B;**業務用戶**&#x200B;執行。 這是您建立歷程的地方。 結合不同的事件、協調和動作活動，以建立您的多步驟跨管道情境。

以下是透過歷程傳送訊息的主要步驟：

1. 在左菜單中，按一下&#x200B;**[!UICONTROL Journeys]**。 將顯示歷程清單。

   ![](../assets/interface-journeys.png)

1. 按一下&#x200B;**[!UICONTROL Create]**&#x200B;以建立新的歷程。

1. 在右側顯示的設定窗格中，編輯歷程的屬性。請參閱[一節](journey-gs.md#change-properties)瞭解更多資訊。

   ![](../assets/jo-properties.png)

1. 首先，從浮動視窗拖放事件或&#x200B;**讀取區段**&#x200B;活動至畫布。 若要進一步瞭解歷程設計，請參閱[本節](using-the-journey-designer.md)。

   ![](../assets/read-segment.png)

1. 拖放個人將遵循的後續步驟。 例如，您可以新增條件，後面接著訊息。 若要進一步瞭解活動，請參閱[本節](using-the-journey-designer.md)。

1. 使用測試設定檔來測試您的旅程。 進一步瞭解[章節](testing-the-journey.md)

1. 發佈您的歷程以啟動它。 請參閱[一節](publishing-the-journey.md)瞭解更多資訊。

   ![](../assets/jo-journeyuc2_32bis.png)

1. 使用專屬的報告工具監控您的歷程，以評估您的歷程成效。 請參閱[一節](../reports/live-report.md)瞭解更多資訊。

   ![](../assets/jo-dynamic_report_journey_12.png)

## 變更屬性 {#change-properties}

按一下右上角的鉛筆圖示，以存取歷程的屬性。

您可以變更旅程的名稱、新增說明、允許重新進入、選擇開始和結束日期，並定義&#x200B;**[!UICONTROL Timeout and error]**&#x200B;持續時間（如果您是管理員）。

**複製技術詳細資訊**&#x200B;允許您複製支援團隊可用於故障排除的歷程的技術資訊。 會複製下列資訊：JourneyVersion UID、OrgID、orgName、sandboxName。

![](../assets/journey32.png)

### 入口{#entrance}

依預設，新的旅程允許重新進入。 您可以取消勾選「單拍」歷程的選項，例如，當某人進入商店時，您想要提供一次性禮品。 在這種情況下，您不希望客戶能夠重新進入歷程並再次收到優惠。

當旅程「結束」時，狀態為&#x200B;**[!UICONTROL Closed (no entrance)]**。 這段旅程將不再讓新人進入這段旅程。 已經在旅途中的人將正常完成旅程。

在預設全域逾時30天後，歷程將切換至&#x200B;**Finished**&#x200B;狀態。 請參閱此[節](../building-journeys/journey-gs.md#global_timeout)。

### 歷程活動的逾時和錯誤{#timeout_and_error}

在編輯動作或條件活動時，您可以定義替代路徑，以防發生錯誤或逾時。 如果詢問第三方系統的活動的處理超過在歷程的屬性（**[!UICONTROL Timeout and  error]**&#x200B;欄位）中定義的超時持續時間，則選擇第二路徑以執行潛在的備援動作。

授權值介於1到30秒之間。

如果您的歷程對時間很敏感，建議您定義非常短的&#x200B;**[!UICONTROL Timeout and error]**&#x200B;值(例如：回應人員的即時位置)，因為您無法將動作延遲超過幾秒。 如果您的歷程對時間不太敏感，您可以使用較長的值，為呼叫傳送有效回應的系統提供更多時間。

Journeys也使用全域逾時。 請參閱[下一節](#global_timeout)。

### 全域歷程逾時{#global_timeout}

除了在歷程活動中使用的[timeout](#timeout_and_error)之外，還有一個全局歷程超時，該超時不會顯示在介面中，也不能更改。 此逾時會在個人進入後30天內停止歷程中的進度。 這表示個人的旅程不能超過30天。 在30天逾時期間後，會刪除個人的資料。 在逾時期間結束時仍在行程中流動的個人將停止，並將其視為報告中的錯誤。

>[!NOTE]
>
>旅程不會直接回應隱私權選擇退出、存取或刪除要求。 不過，全域逾時可確保個人在任何行程中不會停留超過30天。

由於30天的行程逾時，當行程重新進入不允許時，我們無法確保重新進入的阻擋作用超過30天。 事實上，由於我們刪除了所有有關在他們進入旅程30天後進入旅程的資訊，因此我們無法知道在30天前進入的人。

### 時區和描述檔時區{#timezone}

時區是在歷程層級定義。

您可以輸入固定時區或使用Adobe Experience Platform描述檔來定義旅程時區。

有關時區管理的詳細資訊，請參見[本頁](../building-journeys/timezone-management.md)。

## 結束旅程

旅程可能會因為兩個原因而結束：

* 人到達路徑的最後一個活動。 最後一個活動可以是結束活動或其他活動。 沒有義務以結束活動結束路徑。 請參閱[本頁](../building-journeys/end-activity.md)。
* 該人員到達條件活動（或具有條件的等待活動），且不符合任何條件。

如果允許重新入場，人就可以重新進入旅程。 請參閱[本頁](../building-journeys/journey-gs.md#change-properties)

由於下列原因，旅程可能會結束：

* 歷程會透過&#x200B;**[!UICONTROL Close to new entrances]**&#x200B;按鈕手動關閉。
* 一次性分段的歷程，已完成執行。
* 在上次發生循環區段歷程後。

當旅程關閉時（基於上述任何原因），其狀態將為&#x200B;**[!UICONTROL Closed (no entrance)]**。 這段旅程將不再讓新人進入這段旅程。 已經在旅途中的人將正常完成旅程。 在預設全域逾時30天後，歷程將切換至&#x200B;**Finished**&#x200B;狀態。 請參閱此[節](../building-journeys/journey-gs.md#global_timeout)。

如果您需要阻止旅程中所有個人的進步，您可以阻止它。 停止旅程將逾時旅程中的所有個人。

以下是手動關閉或停止歷程的方式：

**[!UICONTROL Stop]**&#x200B;和&#x200B;**[!UICONTROL Close to new entrances]**&#x200B;選項可讓您終止&#x200B;**即時**&#x200B;歷程。 結束歷程需要&#x200B;**：新客戶在歷程中的到達被阻止**，並且已進入歷程的客戶能夠體驗到最終。 這是結束旅程的最推薦方式，因為它為客戶提供最佳體驗。 旅途的阻止，是指已經踏上旅程的人，都被阻止在進程中。 旅程基本上被關閉了。

>[!NOTE]
>
>請注意，您無法繼續結束或停止的旅程。

### 結束旅程

您可以手動結束歷程，以確保已進入歷程的客戶能夠完成其歷程，但新使用者無法進入歷程。

當關閉時，歷程的狀態為&#x200B;**[!UICONTROL Closed (no entrance)]**。 在預設全域逾時30天後，歷程將切換至&#x200B;**Finished**&#x200B;狀態。 請參閱此[節](../building-journeys/journey-gs.md#global_timeout)。

無法重新啟動或刪除已結束的歷程版本。 您可以建立新版本或複製。 只能刪除已完成的歷程。

您可以按一下&#x200B;**[!UICONTROL Close to new entrances]**，將滑鼠暫留在歷程清單中的歷程上，以結束歷程。

![](../assets/do-not-localize/journey-finish-quick-action.png)

您也可以：

1. 在&#x200B;**[!UICONTROL Journeys]**&#x200B;清單中，按一下您要關閉的歷程。
1. 在右上方，按一下向下箭頭。

   ![](../assets/finish_drop_down_list.png)

1. 按一下「**[!UICONTROL Close to new entrances]**」。對話方塊隨即顯示。
1. 按一下&#x200B;**[!UICONTROL Close to new entrances]**&#x200B;進行確認。

### 停止旅程

當發生緊急狀況且所有處理程式都需要在旅程中立即結束時，您可以停止旅程。

無法重新啟動已停止的歷程版本。

當停止時，旅程的狀態為&#x200B;**[!UICONTROL Stopped]**。

您可以在將滑鼠暫留在歷程清單中的歷程上時，按一下&#x200B;**[!UICONTROL Stop]**&#x200B;來停止歷程（例如，行銷人員發現歷程鎖定了錯誤的對象，或自訂動作本應傳送訊息無法正確運作……）。

![](../assets/do-not-localize/journey-stop-quick-action.png)

您也可以：

1. 在&#x200B;**[!UICONTROL Journeys]**&#x200B;清單中，按一下您要停止的歷程。
1. 在右上方，按一下向下箭頭。

![](../assets/finish_drop_down_list.png)

1. 按一下「**[!UICONTROL Stop]**」。對話方塊隨即顯示。
1. 按一下&#x200B;**[!UICONTROL Stop]**&#x200B;進行確認。
