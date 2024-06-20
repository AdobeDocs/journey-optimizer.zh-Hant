---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的第一個歷程
description: 使用 Adobe Journey Optimizer 建置您的第一個歷程的關鍵步驟
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，第一，開始，快速入門，對象，事件，動作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 22%

---

# 建立您的第一個歷程{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="建立歷程"
>abstract="使用 **Adobe Journey Optimizer** 可讓您善用儲存在事件或資料來源中的內容關聯式資料，建置即時協調流程使用案例。"


## 先決條件{#start-prerequisites}

若要在歷程中傳送訊息，需要下列設定：

1. **設定事件**：如果您想要在收到事件時統一觸發歷程，則需要設定事件。 您可以定義預期的資訊及其處理方式。 此步驟由執行 **技術使用者**. [閱讀全文](../event/about-events.md)。

   ![](assets/jo-event7bis.png)

1. **建立對象**：您的歷程也可以監聽Adobe Experience Platform對象，以批次傳送訊息至指定的設定檔集。 為此，您需要建立對象。 [閱讀全文](../audience/about-audiences.md)。

   ![](assets/segment2.png)

1. **設定資料來源**：您可以定義系統連線，以擷取將用於歷程的其他資訊，例如在您的條件中。 佈建時也會設定內建的 Adobe Experience Platform 資料來源。如果您只會運用歷程中事件的資料，則不需要執行此步驟。此步驟由執行 **技術使用者**. [閱讀全文](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **設定動作**：如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 在本節瞭解更多 [區段](../action/action.md). 此步驟由執行 **技術使用者**. 如果您使用Journey Optimizer內建訊息功能，只需將頻道動作新增至歷程並設計內容即可。

   ![](assets/custom2.png)

## 存取歷程 {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="歷程"
>abstract="設計客戶歷程提供個人化的內容關聯式體驗。Journey Optimizer 可讓您利用儲存在事件或資料來源中的內容關聯式資料，建立即時協調流程使用案例。**概觀**&#x200B;標籤會顯示儀表板，其中包含與您的歷程相關的關鍵量度。**瀏覽**&#x200B;標籤會顯示現有歷程的清單。"

### 關鍵量度和歷程清單 {#access-metrics}

在歷程管理功能表區段中，按一下 **[!UICONTROL 歷程]**. 有兩個標籤可供使用：

**概觀**：此標籤會顯示控制面板，其中包含與您的歷程相關的關鍵量度：

* **設定檔已處理**：過去24小時內處理的設定檔總數
* **即時歷程**：過去24小時內具有流量的即時歷程總數。 即時歷程包括 **單一歷程** （事件型）和 **批次歷程** （讀取對象）。
* **錯誤率**：與過去24小時內輸入的設定檔總數相較之所有錯誤設定檔的比率。
* **捨棄率**：與過去24小時內輸入的設定檔總數相較之下，所有捨棄的設定檔比率。 捨棄的設定檔代表沒有資格進入歷程的人，例如由於名稱空間不正確或重新進入規則所導致。

>[!NOTE]
>
>此儀表板會考慮過去24小時內具有流量的歷程。 只會顯示您有權存取的歷程。 量度每30分鐘會重新整理一次，且僅當有新資料可用時才會重新整理。

![](assets/journeys-dashboard.png)

**瀏覽**：此索引標籤會顯示現有歷程的清單。 您可以搜尋歷程、使用篩選器並對每個元素執行基本動作。 例如，您可以複製或刪除專案。 如需詳細資訊，請參閱[本區段](../start/user-interface.md#filter-lists)。

![](assets/journeys-browse.png)

### 篩選歷程 {#filter}

在歷程清單中，您可以運用各種篩選器來調整歷程清單，以提高可讀性。

![](assets/filter-journeys.png)

以下是您可以執行的各種篩選作業：

根據歷程的狀態、型別、版本和指派的標籤來篩選歷程，從 **[!UICONTROL 狀態和版本篩選器]**.

型別可以是： **[!UICONTROL 單一事件]**， **[!UICONTROL 對象資格]**， **[!UICONTROL 讀取對象]** 或 **[!UICONTROL 業務事件]**.

狀態可以是：

* **已關閉**：歷程已使用 **關閉新入口** 按鈕。 歷程停止讓新個人進入歷程。 已在歷程中的人可以正常完成歷程。
* **草稿**：歷程處於第一個階段。 尚未發佈。
* **草稿（測試）**：測試模式已使用啟動 **測試模式** 按鈕。
* **已完成**：歷程會在91天後自動切換為此狀態 [全域逾時](journey-properties.md#global_timeout). 歷程中已有的設定檔會正常完成歷程。 新設定檔無法再進入歷程。
* **即時**：歷程已使用發佈 **發佈** 按鈕。
* **已停止**：歷程已使用「 」關閉 **停止** 按鈕。 所有個人會立即退出歷程。

>[!NOTE]
>
>歷程編寫生命週期也包含一組無法篩選的中間狀態：「發佈」（「草稿」與「即時」之間）、「啟用測試模式」或「停用測試模式」(「草稿」與「草稿（測試）」之間)以及「停止」（「即時」與「已停止」之間）。 當歷程處於中介狀態時，其是唯讀。

使用 **[!UICONTROL 建立篩選器]** 若要根據歷程的建立日期或建立歷程的使用者來篩選歷程。

顯示使用來自的特定事件、欄位群組或動作的歷程 **[!UICONTROL 活動篩選器]** 和 **[!UICONTROL 資料篩選器]**.

使用 **[!UICONTROL 發佈篩選器]** 以選取出版日期或使用者。 舉例來說，您可以選擇只顯示昨天發佈之即時歷程的最新版本。

若要根據特定日期範圍篩選歷程，請選取 **[!UICONTROL 自訂]** 從 **[!UICONTROL 已發佈]** 下拉式清單。

此外，在「事件」、「資料來源」和「動作」設定窗格中， **[!UICONTROL 使用位置]** 欄位會顯示使用該特定事件、欄位群組或動作的歷程次數。 您可以按一下&#x200B;**[!UICONTROL 檢視歷程]**&#x200B;按鈕以顯示對應歷程的清單。

![](assets/journey3bis.png)

## 建置您的歷程 {#jo-build}

設計歷程以提供個人化的情境式體驗。 [!DNL Journey Optimizer]可讓您利用儲存在事件或資料來源中的情境資料，建立即時協調流程使用案例。設計由下列功能提供支援的多步驟進階案例：

* 傳送在收到事件時觸發的即時&#x200B;**單一傳遞**，或使用 Adobe Experience Platform 對象&#x200B;**批次**&#x200B;傳遞。

* 利用來自事件的&#x200B;**情境資料** 、來自 Adobe Experience Platform 的資訊，或來自協力廠商 API 服務的資料。

* 使用 **內建頻道動作** （電子郵件、簡訊、推播、InApp），傳送設計的訊息 [!DNL Journey Optimizer] 或建立 **自訂動作** 如果您使用協力廠商系統來傳送訊息。

* 使用&#x200B;**歷程設計工具**，建置多步驟使用案例：輕鬆拖放進入事件或讀取對象活動、新增條件及傳送個人化訊息。

➡️ [在影片中探索此功能](journey.md#video)

以下列出透過歷程傳送訊息的步驟。

1. 從 **瀏覽** 標籤，按一下 **[!UICONTROL 建立歷程]** 以建立新的歷程。

1. 在右側顯示的設定窗格中，編輯歷程的屬性。在此瞭解如何設定您的歷程屬性 [此頁面](journey-properties.md).

   ![](assets/jo-properties.png)

1. 從拖放事件或 **讀取對象** 活動從浮動視窗移入畫布。 若要進一步瞭解歷程設計，請參閱 [本節](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. 拖放個人會遵循的後續步驟。 例如，您可以新增條件，然後新增管道動作。 若要進一步瞭解活動，請參閱 [本節](using-the-journey-designer.md).

1. 使用測試設定檔測試您的歷程。 在本節瞭解更多 [區段](testing-the-journey.md)

1. 發佈您的歷程以啟用。 在本節瞭解更多 [區段](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. 使用專屬的報告工具監控您的歷程，以評估歷程的成效。 在本節瞭解更多 [區段](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)


## 複製歷程 {#duplicate-a-journey}

您可以從以下位置複製現有歷程： **瀏覽** 標籤。 所有物件和設定都會複製到歷程副本。

請依照下列步驟執行：

1. 導覽至您要複製的歷程，按一下 **更多動作** 圖示（歷程名稱旁的三個點）。
1. 選取「**複製**」。

   ![複製歷程](assets/duplicate-jo.png)

1. 輸入歷程名稱並確認。 您也可以在歷程屬性畫面中變更名稱。 依預設，名稱設定如下： `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. 新歷程已建立並可在歷程清單中使用。
