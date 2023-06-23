---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的第一個歷程
description: 使用 Adobe Journey Optimizer 建置您的第一個歷程的關鍵步驟
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，第一，開始，快速入門，區段，事件，動作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 1cf62f949c1309b864ccd352059a444fd7bd07f0
workflow-type: tm+mt
source-wordcount: '1548'
ht-degree: 25%

---

# 建立您的第一個歷程{#jo-quick-start}

## 先決條件{#start-prerequisites}

若要在歷程中傳送訊息，需要下列設定：

1. **設定事件**：如果您要在收到事件時整體觸發歷程，則需要設定事件。 您可以定義預期的資訊及其處理方式。 此步驟由&#x200B;**技術使用者**&#x200B;執行。[閱讀全文](../event/about-events.md)。

   ![](assets/jo-event7bis.png)

1. **建立區段**：您的歷程也可以接聽Adobe Experience Platform區段，以批次將訊息傳送至指定的設定檔集。 為此，您需要建立區段。 [閱讀全文](../segment/about-segments.md)。

   ![](assets/segment2.png)

1. **設定資料來源**：您可以定義系統連線，以擷取將用於歷程的其他資訊，例如在您的條件中。 佈建時也會設定內建的 Adobe Experience Platform 資料來源。如果您只會運用歷程中事件的資料，則不需要執行此步驟。此步驟由&#x200B;**技術使用者**&#x200B;執行。[閱讀全文](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **設定動作**：如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 在本節瞭解更多 [區段](../action/action.md). 此步驟由&#x200B;**技術使用者**&#x200B;執行。如果您使用Journey Optimizer內建訊息功能，只需將頻道動作新增至歷程並設計內容即可。

   ![](assets/custom2.png)

## 存取歷程 {#journey-access}

在JOURNEY MANAGEMENT功能表區段中，按一下 **[!UICONTROL 歷程]**. 有兩個索引標籤可供使用：

**概觀**：此標籤會顯示控制面板，其中包含與您的歷程相關的關鍵量度：

* **已處理的設定檔**：過去24小時內處理的設定檔總數
* **即時歷程**：過去24小時內具有流量的即時歷程總數。 即時歷程包括 **單一歷程** （事件型）和 **批次歷程** （讀取區段）。
* **錯誤率**：所有錯誤的設定檔與過去24小時內輸入的設定檔總數之比。
* **捨棄率**：與過去24小時內輸入的設定檔總數相比較之所有捨棄的設定檔比率。 捨棄的設定檔代表不符合進入歷程資格的人，例如由於名稱空間不正確或由於重新進入規則。

>[!NOTE]
>
>此儀表板會考慮過去24小時內具有流量的歷程。 只會顯示您有權存取的歷程。

![](assets/journeys-dashboard.png)

**瀏覽**：此索引標籤會顯示現有歷程的清單。 您可以搜尋歷程、使用篩選器並對每個元素執行基本動作。 例如，您可以複製或刪除項目。如需詳細資訊，請參閱[本區段](../start/user-interface.md#filter-lists)。

![](assets/journeys-browse.png)

在歷程清單中，您可以從&#x200B;**[!UICONTROL 狀態及版本篩選器]**&#x200B;中根據歷程的狀態、類型與版本來篩選歷程。 型別可以是： **[!UICONTROL 單一事件]**， **[!UICONTROL 區段資格]**， **[!UICONTROL 讀取區段]** 或 **[!UICONTROL 業務事件]**.

您可以選擇僅顯示使用&#x200B;**[!UICONTROL 事件篩選器]**&#x200B;與&#x200B;**[!UICONTROL 資料篩選器]**&#x200B;中的特定事件、欄位群組或動作的歷程。此外， **[!UICONTROL 發佈篩選器]** 可讓您選取出版日期或使用者。 舉例來說，您可以選擇只顯示昨天發佈之即時歷程的最新版本。[了解更多](../building-journeys/using-the-journey-designer.md)。

![](assets/filter-journeys.png)

使用&#x200B;**[!UICONTROL 上次更新]**&#x200B;及&#x200B;**[!UICONTROL 最後更新者]**&#x200B;欄來檢查您的歷程上次更新發生的時間以及儲存者。

在事件、資料來源和動作設定窗格中，**[!UICONTROL 使用位置]**&#x200B;欄位會顯示使用該特定事件、欄位群組或操作的歷程次數。您可以按一下&#x200B;**[!UICONTROL 檢視歷程]**&#x200B;按鈕以顯示對應歷程的清單。

![](assets/journey3bis.png)

## 建置您的歷程{#jo-build}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="建置您的歷程"
>abstract="此畫面會顯示現有歷程的清單。開啟歷程或按一下「建立歷程」，並合併不同的事件、協調和動作活動以建置您的多步驟跨管道案例。"

此步驟由執行 **業務使用者**. 這是您建立歷程的位置。 結合不同的事件、協調和動作活動，以建立您的多步驟跨管道情境。

以下是透過歷程傳送訊息的主要步驟：

1. 從 **瀏覽** 標籤，按一下 **[!UICONTROL 建立歷程]** 以建立新歷程。

1. 在右側顯示的設定窗格中，編輯歷程的屬性。在本節瞭解更多 [區段](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. 從拖放事件或 **讀取區段** 活動從浮動視窗移至畫布。 若要進一步瞭解歷程設計，請參閱 [本節](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. 拖放個人將遵循的後續步驟。 例如，您可以新增條件，然後新增管道動作。 若要進一步瞭解活動，請參閱 [本節](using-the-journey-designer.md).

1. 使用測試設定檔測試您的歷程。 在本節瞭解更多 [區段](testing-the-journey.md)

1. 發佈您的歷程以啟動它。 在本節瞭解更多 [區段](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. 使用專屬的報告工具監控您的歷程，以評估歷程的成效。 在本節瞭解更多 [區段](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## 定義您的歷程屬性 {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="歷程屬性"
>abstract="本區段會顯示歷程屬性。預設情況下，會隱藏唯讀參數。可用設定會依據歷程的狀態、您的權限和產品設定而定。"

按一下右上方的鉛筆圖示，即可存取歷程的屬性。

您可以變更歷程名稱、新增說明、允許重新進入、選擇開始和結束日期，並以管理員使用者身分定義 **[!UICONTROL 逾時和錯誤]** 持續時間。 您也可以將Adobe Experience Platform統一標籤指派給您的歷程。 這可讓您輕鬆分類，並改進行銷活動清單的搜尋。 [了解如何使用標籤](../start/search-filter-categorize.md#tags)

若為即時歷程，此畫面會顯示發佈日期和發佈歷程的使用者名稱。

此 **複製技術細節** 可讓您複製支援團隊可用於疑難排解的歷程相關技術資訊。 已複製下列資訊：JourneyVersion UID、OrgID、orgName、sandboxName、lastDeployedBy、lastDeployedAt。

![](assets/journey32.png)

### 入口{#entrance}

依預設，新歷程允許重新進入。 您可以取消勾選 **允許重新進入** 「單次拍攝」歷程的選項，例如，如果您想要在人員進入商店時提供一次性禮物。

當 **允許重新進入** 選項已啟用， **重新進入等待期** 欄位。 此欄位可讓您定義在允許設定檔在單一歷程中再次進入歷程 (從事件或區段資格開始) 之前等待的時間。這可防止同一事件多次錯誤觸發歷程。預設情況下，欄位會設為 5 分鐘。 

進一步瞭解設定檔入口管理，請參閱 [本節](entry-management.md).

### 管理存取權 {#access}

若要將自訂或核心資料使用標籤指派給歷程，請按一下 **[!UICONTROL 管理存取權]** 按鈕。 [進一步瞭解物件層級存取控制(OLA)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### 時區和設定檔時區 {#timezone}

時區在歷程層級定義。

您可以輸入固定時區，或使用Adobe Experience Platform設定檔來定義歷程時區。

如果在Adobe Experience Platform設定檔中定義了時區，則可在歷程中擷取該時區。

如需時區管理的詳細資訊，請參閱 [此頁面](../building-journeys/timezone-management.md).

### 開始和結束日期 {#dates}

您可以定義 **開始日期**. 如果您尚未指定，則會在發佈時自動定義。

您也可以新增 **結束日期**. 這可讓設定檔在達到日期時自動退出。 如果您未指定結束日期，設定檔可以保留到預設歷程逾時（通常30天，Healthcare Shield附加元件為7天）。 唯一的例外是循環讀取區段歷程，具有 **在重複時強制重新進入** 已啟用，在下次發生的開始日期結束。

### 歷程活動中的逾時和錯誤 {#timeout_and_error}

編輯動作或條件活動時，您可以選擇在錯誤或逾時事件中指定替代路徑。 如果活動的處理（包括查詢協力廠商系統）超過歷程屬性中指定的逾時和錯誤處理持續時間(**[!UICONTROL 逾時和錯誤]** 欄位)，如有必要，將會選取第二個路徑以執行遞補動作。

授權值介於1到30秒之間。

建議您最好定義一個非常簡短的 **[!UICONTROL 逾時和錯誤]** 值(如果您的歷程對時間敏感（例如：對個人的即時位置做出反應），因為您的動作無法延遲超過幾秒鐘。 如果您的歷程不太敏感，您可以使用較長的值，讓系統有更多時間呼叫，以傳送有效回應。

歷程也使用全域逾時。 請參閱 [下一節](#global_timeout).

### 全域歷程逾時 {#global_timeout}

除了 [逾時](#timeout_and_error) 在歷程活動中使用，也會有全域歷程逾時，此逾時不會顯示在介面中且無法變更。 此逾時將在個人進入後30天，停止歷程中的進度。 這表示個人的歷程不能持續超過30天。 在30天逾時期間後，個人的資料會被刪除。 在逾時期間結束時仍在歷程中流動的個人將停止，並將他們視為報告中的錯誤。

>[!NOTE]
>
>歷程不會直接回應隱私權選擇退出、存取或刪除請求。 不過，全域逾時可確保個人在任何歷程中的逗留時間不會超過30天。

由於30天歷程逾時，當歷程重新進入遭到禁止時，我們無法確保重新進入封鎖會運作超過30天。 事實上，由於我們移除了在進入歷程30天後進入歷程之人員的所有資訊，因此我們無法得知該人員先前已進入（超過30天前）。

