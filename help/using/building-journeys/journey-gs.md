---
title: 開始使用歷程
description: 使用 Adobe Journey Optimizer 建置您的第一個歷程的關鍵步驟
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: c5ddc1a5a3dc133819ba2f887dae73fc48690fe9
workflow-type: tm+mt
source-wordcount: '1846'
ht-degree: 6%

---

# 開始使用歷程{#jo-quick-start}

## 先決條件{#start-prerequisites}

為了隨行程發送消息，需要以下配置：

1. **配置事件**:如果希望在收到事件時觸發整個行程，則需要配置事件。 定義預期資訊及其處理方法。 此步驟由&#x200B;**技術使用者**&#x200B;執行。[閱讀全文](../event/about-events.md)。

   ![](assets/jo-event7bis.png)

1. **建立段**:您的旅程還可以監聽Adobe Experience Platform段，以便將郵件批量發送到指定的一組配置檔案。 為此，需要建立段。 [閱讀全文](../segment/about-segments.md)。

   ![](assets/segment2.png)

1. **配置資料源**:您可以定義到系統的連接，以檢索將在您的行程中使用的附加資訊，例如在您的條件中。 佈建時也會設定內建的 Adobe Experience Platform 資料來源。如果您只會運用歷程中事件的資料，則不需要執行此步驟。此步驟由&#x200B;**技術使用者**&#x200B;執行。[閱讀全文](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **配置操作**:Journey Optimizer郵件功能是內置的，您只需設計內容並發佈郵件即可。 請參閱[本節](../messages/get-started-content.md)。如果您使用第三方系統發送消息，則可以建立自定義操作。 瞭解更多資訊 [節](../action/action.md)。 此步驟由&#x200B;**技術使用者**&#x200B;執行。

   ![](assets/create-content-push.png)

## 構建您的旅程{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="構建您的旅程"
>abstract="此螢幕顯示現有旅程的清單。 開啟行程或按一下「建立行程」，並將不同的事件、業務流程和操作活動組合起來，以構建您的多步跨渠道方案。"

此步驟由 **業務用戶**。 這是你建立旅程的地方。 結合不同的事件、協調和動作活動，以建立您的多步驟跨管道情境。

以下是通過行程發送消息的主要步驟：

1. 在「行程管理」(JOURNEY MANAGEMENT)菜單部分，按一下 **[!UICONTROL Journeys]**。 將顯示行程清單。

   ![](assets/interface-journeys.png)

1. 按一下 **[!UICONTROL Create Journey]** 創造新的旅程。

1. 在右側顯示的設定窗格中，編輯歷程的屬性。瞭解更多資訊 [節](journey-gs.md#change-properties)。

   ![](assets/jo-properties.png)

1. 通過拖放事件或 **讀取段** 活動從元件面板到畫布。 要瞭解有關行程設計的詳細資訊，請參閱 [此部分](using-the-journey-designer.md)。

   ![](assets/read-segment.png)

1. 拖放個人將遵循的後續步驟。 例如，可以添加一個條件，然後添加一條消息。 要瞭解有關活動的詳細資訊，請參閱 [此部分](using-the-journey-designer.md)。

1. 使用test配置檔案test您的旅程。 瞭解更多資訊 [節](testing-the-journey.md)

1. 發佈您的行程以激活它。 瞭解更多資訊 [節](publishing-the-journey.md)。

   ![](assets/jo-journeyuc2_32bis.png)

1. 使用專用報告工具監控您的旅程，以衡量您的旅程的效果。 瞭解更多資訊 [節](../reports/live-report.md)。

   ![](assets/jo-dynamic_report_journey_12.png)

## 定義行程屬性 {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="歷程屬性"
>abstract="本節顯示行程屬性。 預設情況下，只讀參數將隱藏。 可用設定取決於行程的狀態、權限和產品配置。"

按一下右上角的鉛筆表徵圖以訪問行程的屬性。

您可以更改行程名稱、添加說明、允許重新進入、選擇開始和結束日期，並作為管理員用戶定義 **[!UICONTROL Timeout and error]** 持續時間。 如果為組織啟用，您還可以激活 [突發消息](#burst)。

對於即時行程，此螢幕顯示發佈日期和發佈行程的用戶的名稱。

的 **複製技術詳細資訊** 允許您複製支援團隊用於故障排除的旅程的技術資訊。 將複製以下資訊：JourneyVersion UID、OrgID、orgName、sandboxName、lastDeployedBy、lastDeployedAt。

![](assets/journey32.png)

### 入口{#entrance}

預設情況下，新旅程允許重新進入。 您可以取消選中「一次性」旅程選項，例如，如果您想在人員進入商店時提供一次性禮物。 在這種情況下，您不希望客戶能夠重新進入行程並再次收到優惠。

當旅程「結束」時，它將具有 **[!UICONTROL Closed]**。 旅程將停止讓新人進入旅程。 已經在旅途中的人將正常完成旅程。

在預設全局超時30天後，該行程將切換到 **已完成** 狀態。 查看 [節](../building-journeys/journey-gs.md#global_timeout)。

### 行程活動超時和出錯 {#timeout_and_error}

編輯操作或條件活動時，您可以在出現錯誤或超時時定義替代路徑。 如果查詢第三方系統的活動的處理超過行程的屬性中定義的超時持續時間(**[!UICONTROL Timeout and  error]** 欄位)，將選擇第二個路徑以執行可能的回退操作。

授權值介於1到30秒之間。

我們建議你定義一個 **[!UICONTROL Timeout and error]** 值（如果您的行程是時間敏感型的）(例如：對人的即時位置進行響應)，因為您不能將操作延遲超過幾秒鐘。 如果您的行程對時間不太敏感，則可以使用較長的值為調用的系統提供更多時間，以發送有效響應。

行程還使用全局超時。 查看 [下一部分](#global_timeout)。

### 全局行程超時 {#global_timeout}

除 [超時](#timeout_and_error) 在行程活動中使用，還有一個全局行程超時，該超時不顯示在介面中，無法更改。 此超時將阻止個人在進入後30天內的進度。 這意味著一個人的旅程不能超過30天。 在30天超時期後，將刪除個人的資料。 在超時期結束時仍在旅途中流動的個人將被停止，並將他們作為報告錯誤加以考慮。

>[!NOTE]
>
>旅程不會直接對隱私選擇退出、訪問或刪除請求做出反應。 但是，全局超時可確保個人在任何行程中停留的時間不超過30天。

由於30天的行程超時，當不允許再入行程時，無法確保再入阻塞工作超過30天。 事實上，當我們刪除有關在他們進入旅程30天後進入旅程的所有資訊時，我們無法知道之前在30多天前輸入的人。

### 時區和配置檔案時區 {#timezone}

時區在行程級別定義。

您可以輸入固定時區或使用Adobe Experience Platform配置檔案定義行程時區。

如果在Adobe Experience Platform配置檔案中定義了時區，則可以在行程中檢索該時區。

有關時區管理的詳細資訊，請參見 [此頁](../building-journeys/timezone-management.md)。

### 突發模式 {#burst}

拆分模式是一個Journey Optimizer附加模組，它允許在大卷中快速發送推送消息。 它用於包括 **讀取段** 活動和簡單的推送消息。 當消息傳遞的延遲對業務至關重要時，當您想在行動電話上發送緊急推送警報時，例如向已安裝新聞頻道應用的用戶發送突發新聞時，將使用Burst。

突發消息傳送附帶以下要求：

* 旅程必須以 **讀取段** 的子菜單。 不允許發生事件。
* 下一步必須是推送消息。 不允許其他渠道、活動或步驟(可選 **結束** )。
* 推送消息中不允許個性化。
* 消息必須小(&lt;2KB)。

>[!CAUTION]
>
>如果任何要求未滿足，在行程中將不提供突發模式。

激活 **突發模式**，開啟行程，然後按一下右上角的鉛筆表徵圖以訪問行程的屬性。 然後，激活 **啟用拆分模式** 切換。

![](assets/burst.png)

如果修改突發行程並添加與突發消息不符的活動（如電子郵件、任何其他操作、事件等），突發模式將自動停用。

![](assets/burst2.png)

然後test，像往常一樣發佈你的旅程。 請注意，在test模式下，消息不會通過拆分模式發送。

瞭解在此視頻中突發消息的適用使用案例，以及如何配置突發消息的行程：

>[!VIDEO](https://video.tv.adobe.com/v/334523?quality=12)


## 結束、停止或結束行程{#end-journey}

在以下兩種特定情況下，個人可以結束行程：

* 該人到達了路徑的最後一個活動。 最後一個活動可以是 **結束** 活動或其他活動。 使用 **結束** 活動不是必需的。 請參閱[此頁面](../building-journeys/end-activity.md)。
* 這個人到達 **條件** 活動(或 **等待** 具有條件的活動)，且與任何條件不匹配。

如果允許重新進入，則人員可以重新進入旅程。 請參閱 [此頁](../building-journeys/journey-gs.md#change-properties)

行程可能會關閉，原因如下：

* 通過 **[!UICONTROL Close to new entrances]** 按鈕
* 已完成執行的基於單次段的行程。
* 上次出現基於週期段的行程之後。

當行程關閉時（出於以上任何原因），它將具有 **[!UICONTROL Closed]**。 旅程不再讓新人進入旅程。 已經在旅途中的人可以正常地完成旅程。 在預設全局超時30天後，該行程將切換到 **已完成** 狀態。 查看 [節](../building-journeys/journey-gs.md#global_timeout)。

如果你需要阻止所有人在旅途中的進步，你可以阻止它。 停止行程將超時行程中的所有人。

以下是手動關閉或停止行程的方式：

的 **[!UICONTROL Stop]** 和 **[!UICONTROL Close to new entrances]** 選項允許您終止 **活** 旅程。 結束旅程需要 **新客戶在旅途中的抵達被阻止** 而且已經進入旅程的顧客能夠體驗到它的結束。 這是結束旅程的最推薦方法，因為它為客戶提供了最佳體驗。 停止旅行意味著已經踏上旅程的人都會停止前進。 旅程基本上被關閉了。

>[!NOTE]
>
>請注意，您無法恢復已關閉或已停止的行程。

### 結束旅程

您可以手動結束行程，以確保已輸入行程的客戶可以完成其路徑，但新用戶無法進入行程。

關閉時，行程將具有 **[!UICONTROL Closed]**。 在預設全局超時30天後，該行程將切換到 **已完成** 狀態。 查看 [節](../building-journeys/journey-gs.md#global_timeout)。

無法重新啟動或刪除已結束的行程版本。 您可以建立新版本或複製該版本。 只能刪除已完成的行程。

要從旅程清單中關閉行程，請按一下 **[!UICONTROL Ellipsis]** 按鈕，選擇 **[!UICONTROL Close to new entrances]**。

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL Journeys]** 清單中，按一下要關閉的行程。
1. 在右上角，按一下向下箭頭。

   ![](assets/finish_drop_down_list.png)

1. 按一下 **[!UICONTROL Close to new entrances]**，並在對話框中進行確認。

### 停止旅行

當發生緊急情況並且所有處理都需要在旅途中立即結束時，您可以停止旅程。

無法重新啟動已停止的行程版本。

停止時，行程狀態設定為 **[!UICONTROL Stopped]**。

例如，如果營銷人員意識到此行程針對的是錯誤的受眾，或者傳遞消息的自定義操作不能正常工作，您就可以停止此行程。 要停止從行程清單中的行程，請按一下 **[!UICONTROL Ellipsis]** 按鈕，選擇 **[!UICONTROL Stop]**。

![](assets/journey-finish-quick-action.png)

您也可以：

1. 在 **[!UICONTROL Journeys]** 清單中，按一下要停止的行程。
1. 在右上角，按一下向下箭頭。

![](assets/finish_drop_down_list.png)

1. 按一下 **[!UICONTROL Stop]**，並在對話框中進行確認。
