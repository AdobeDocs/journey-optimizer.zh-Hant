---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的第一個歷程
description: 使用 Adobe Journey Optimizer 建置您的第一個歷程的關鍵步驟
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: journey，旅程，第一，開始，快速啟動，段，事件，操作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '1512'
ht-degree: 27%

---

# 建立您的第一個歷程{#jo-quick-start}

## 先決條件{#start-prerequisites}

為了隨行程發送消息，需要以下配置：

1. **配置事件**:如果希望在收到事件時觸發整個行程，則需要配置事件。 定義預期資訊及其處理方法。 此步驟由&#x200B;**技術使用者**&#x200B;執行。[閱讀全文](../event/about-events.md)。

   ![](assets/jo-event7bis.png)

1. **建立段**:您的旅程還可以監聽Adobe Experience Platform段，以便將郵件批量發送到指定的一組配置檔案。 為此，需要建立段。 [閱讀全文](../segment/about-segments.md)。

   ![](assets/segment2.png)

1. **配置資料源**:您可以定義到系統的連接，以檢索將在您的行程中使用的附加資訊，例如在您的條件中。 佈建時也會設定內建的 Adobe Experience Platform 資料來源。如果您只會運用歷程中事件的資料，則不需要執行此步驟。此步驟由&#x200B;**技術使用者**&#x200B;執行。[閱讀全文](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **配置操作**:如果您使用第三方系統發送消息，則可以建立自定義操作。 瞭解更多資訊 [節](../action/action.md)。 此步驟由&#x200B;**技術使用者**&#x200B;執行。如果您使用的是Journey Optimizer內置的消息功能，您只需在旅途中添加渠道操作並設計內容即可。

   ![](assets/custom2.png)

## 訪問旅程 {#journey-access}

在「行程管理」(JOURNEY MANAGEMENT)菜單部分，按一下 **[!UICONTROL 旅程]**。 有兩個頁籤可用：

**概述**:此頁籤顯示具有與您的行程相關的關鍵度量的儀表板：

* **已處理的配置檔案**:過去24小時內處理的配置檔案總數
* **即時旅行**:過去24小時有交通的實況旅行總數。 即時旅程包括 **單一旅程** （基於事件）和 **批行程** （讀取段）。
* **錯誤率**:與過去24小時內輸入的配置檔案總數相比，出錯的所有配置檔案的比率。
* **丟棄率**:所有記錄檔的比率，與過去24小時內輸入的記錄檔總數的比率。

>[!NOTE]
>
>此儀表板考慮了過去24小時內的流量。 僅顯示您有權訪問的行程。

![](assets/journeys-dashboard.png)

**瀏覽**:此頁籤顯示現有旅程的清單。 您可以搜索行程、使用篩選器並對每個元素執行基本操作。 例如，您可以複製或刪除項目。如需詳細資訊，請參閱[本區段](../start/user-interface.md#filter-lists)。

![](assets/journeys-browse.png)

在歷程清單中，您可以從&#x200B;**[!UICONTROL 狀態及版本篩選器]**&#x200B;中根據歷程的狀態、類型與版本來篩選歷程。 類型可以是： **[!UICONTROL 單一事件]**、**[!UICONTROL 區段資格]**、**[!UICONTROL 讀取區段]**、**[!UICONTROL 企業活動]**&#x200B;或 **[!UICONTROL 突發事件]**。

您可以選擇僅顯示使用&#x200B;**[!UICONTROL 事件篩選器]**&#x200B;與&#x200B;**[!UICONTROL 資料篩選器]**&#x200B;中的特定事件、欄位群組或動作的歷程。此外， **[!UICONTROL 發佈篩選器]** 允許您選擇發佈日期或用戶。 舉例來說，您可以選擇只顯示昨天發佈之即時歷程的最新版本。[了解更多](../building-journeys/using-the-journey-designer.md)。

![](assets/filter-journeys.png)

使用&#x200B;**[!UICONTROL 上次更新]**&#x200B;及&#x200B;**[!UICONTROL 最後更新者]**&#x200B;欄來檢查您的歷程上次更新發生的時間以及儲存者。

在事件、資料來源和動作設定窗格中，**[!UICONTROL 使用位置]**&#x200B;欄位會顯示使用該特定事件、欄位群組或操作的歷程次數。您可以按一下&#x200B;**[!UICONTROL 檢視歷程]**&#x200B;按鈕以顯示對應歷程的清單。

![](assets/journey3bis.png)

## 建置您的歷程{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="建置您的歷程"
>abstract="此畫面會顯示現有歷程的清單。開啟歷程或按一下「建立歷程」，並合併不同的事件、協調和動作活動以建置您的多步驟跨管道案例。"

此步驟由 **業務用戶**。 這是你建立旅程的地方。 結合不同的事件、協調和動作活動，以建立您的多步驟跨管道情境。

以下是通過行程發送消息的主要步驟：

1. 從 **瀏覽** 按鈕 **[!UICONTROL 建立行程]** 創造新的旅程。

1. 在右側顯示的設定窗格中，編輯歷程的屬性。瞭解更多資訊 [節](journey-gs.md#change-properties)。

   ![](assets/jo-properties.png)

1. 通過拖放事件或 **讀取段** 活動從元件面板到畫布。 要瞭解有關行程設計的詳細資訊，請參閱 [此部分](using-the-journey-designer.md)。

   ![](assets/read-segment.png)

1. 拖放個人將遵循的後續步驟。 例如，可以添加一個條件，然後是通道操作。 要瞭解有關活動的詳細資訊，請參閱 [此部分](using-the-journey-designer.md)。

1. 使用test配置檔案test您的旅程。 瞭解更多資訊 [節](testing-the-journey.md)

1. 發佈您的行程以激活它。 瞭解更多資訊 [節](publishing-the-journey.md)。

   ![](assets/jo-journeyuc2_32bis.png)

1. 使用專用報告工具監控您的旅程，以衡量您的旅程的效果。 瞭解更多資訊 [節](../reports/live-report.md)。

   ![](assets/jo-dynamic_report_journey_12.png)

## 定義行程屬性 {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="歷程屬性"
>abstract="本區段會顯示歷程屬性。預設情況下，會隱藏唯讀參數。可用設定會依據歷程的狀態、您的權限和產品設定而定。"

按一下右上角的鉛筆表徵圖以訪問行程的屬性。

您可以更改行程名稱、添加說明、允許重新進入、選擇開始和結束日期，並作為管理員用戶定義 **[!UICONTROL 超時和錯誤]** 持續時間。 您還可以將Adobe Experience Platform統一標籤分配給您的行程。 這可讓您輕鬆分類，並改進行銷活動清單的搜尋。 [了解如何使用標籤](../start/search-filter-categorize.md#tags)

對於即時行程，此螢幕顯示發佈日期和發佈行程的用戶的名稱。

的 **複製技術詳細資訊** 允許您複製支援團隊用於故障排除的旅程的技術資訊。 將複製以下資訊：JourneyVersion UID、OrgID、orgName、sandboxName、lastDeployedBy、lastDeployedAt。

![](assets/journey32.png)

### 入口{#entrance}

預設情況下，新旅程允許重新進入。 您可以取消選中 **允許重新進入** 選擇「一次性」旅行，例如，當一個人進入商店時，你想提供一次性禮物。

當 **允許重新進入** 選項， **重新進入等待期** 的下界。 此欄位可讓您定義在允許設定檔在單一歷程中再次進入歷程 (從事件或區段資格開始) 之前等待的時間。這可防止同一事件多次錯誤觸發歷程。預設情況下，欄位會設為 5 分鐘。 

瞭解有關配置檔案入口管理的詳細資訊，請參閱 [此部分](entry-management.md)。

### 管理訪問 {#access}

要為行程分配自定義或核心資料使用標籤，請按一下 **[!UICONTROL 管理訪問]** 按鈕 [瞭解有關對象級訪問控制(OLA)的詳細資訊](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### 時區和配置檔案時區 {#timezone}

時區在行程級別定義。

您可以輸入固定時區或使用Adobe Experience Platform配置檔案定義行程時區。

如果在Adobe Experience Platform配置檔案中定義了時區，則可以在行程中檢索該時區。

有關時區管理的詳細資訊，請參見 [此頁](../building-journeys/timezone-management.md)。

### 開始日期和結束日期 {#dates}

您可以定義 **開始日期**。 如果尚未指定，則將在發佈時自動定義。

也可以添加 **結束日期**。 這可讓設定檔在達到日期時自動退出。 如果未指定結束日期，則pofiles可以一直持續到預設行程超時（Healthcare Shield附加產品通常為30天，7天）。 唯一的例外是重複讀段旅程 **重複時的力重入** 已激活，在下次出現的開始日期結束。

### 行程活動超時和出錯 {#timeout_and_error}

編輯操作或條件活動時，您可以在出現錯誤或超時時定義替代路徑。 如果查詢第三方系統的活動的處理超過行程的屬性中定義的超時持續時間(**[!UICONTROL 超時和錯誤]** 欄位)，將選擇第二個路徑以執行可能的回退操作。

授權值介於1到30秒之間。

我們建議你定義一個 **[!UICONTROL 超時和錯誤]** 值（如果您的行程是時間敏感型的）(例如：對人的即時位置進行響應)，因為您不能將操作延遲超過幾秒鐘。 如果您的行程對時間不太敏感，則可以使用較長的值為調用的系統提供更多時間，以發送有效響應。

行程還使用全局超時。 查看 [下一部分](#global_timeout)。

### 全局行程超時 {#global_timeout}

除 [超時](#timeout_and_error) 在行程活動中使用，還有一個全局行程超時，該超時不顯示在介面中，無法更改。 此超時將阻止個人在進入後30天內的進度。 這意味著一個人的旅程不能超過30天。 在30天超時期後，將刪除個人的資料。 在超時期結束時仍在旅途中流動的個人將被停止，並將他們作為報告錯誤加以考慮。

>[!NOTE]
>
>旅程不會直接對隱私選擇退出、訪問或刪除請求做出反應。 但是，全局超時可確保個人在任何行程中停留的時間不超過30天。

由於30天的行程超時，當不允許再入行程時，無法確保再入阻塞工作超過30天。 事實上，當我們刪除有關在他們進入旅程30天後進入旅程的所有資訊時，我們無法知道之前在30多天前輸入的人。

