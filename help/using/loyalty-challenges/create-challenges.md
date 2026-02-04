---
solution: Journey Optimizer
product: journey optimizer
title: 建立忠誠度挑戰
description: 瞭解如何在Adobe Journey Optimizer中建立和設定忠誠度挑戰。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人測試版" type="Informative"
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '1521'
ht-degree: 0%

---


# 創造挑戰 {#create-challenges}

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* [開始解決忠誠度挑戰](get-started.md) — 概述、工作流程、必要條件
* [存取忠誠度挑戰](access-loyalty-challenges.md) — 詳細目錄和篩選
* **建立挑戰** ◀︎**您在這裡** — 建置並設定挑戰
* [建立任務](create-tasks.md) — 定義挑戰任務
* [管理挑戰](manage-challenges.md) — 編輯、監視、最佳化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中，可能無法在您的環境中使用。 若要要求存取權，請聯絡您的Adobe代表。 深入瞭解[可用性標籤](../rn/releases.md#availability-labels)。

## 運作方式 {#how-it-works}

建立和啟動忠誠度挑戰會遵循此工作流程：

1. **[建立挑戰](#create-the-challenge)** — 選擇最符合您忠誠計畫目標的挑戰型別（標準、連續或循序）。

1. **[設定挑戰結構](#structure)** — 定義挑戰屬性、排程、客戶必須完成的工作，以及客戶將獲得的獎勵。

1. **[設定內容卡片](#configure-content-cards)** — 設計內容卡片，以視覺化方式在客戶裝置上呈現您的挑戰，顯示挑戰資訊、進度和獎勵。

1. **[設定訊息](#configure-messaging)** （選擇性） — 設定主要階段的多通道訊息（應用程式內、電子郵件、推播）：啟動、進行中及完成。

1. **[選取挑戰對象](#audience)** — 定義哪些客戶有資格參與挑戰。

1. **[產生並啟用歷程](#review-and-publish)** — 產生關聯的歷程並啟用它，讓您的目標對象可以使用此挑戰。

## 建立挑戰 {#create-the-challenge}

1. 在Journey Optimizer中導覽至&#x200B;**[!UICONTROL 忠誠度挑戰(Beta)]**。

1. 選取&#x200B;**[!UICONTROL 挑戰]**&#x200B;標籤，並選取&#x200B;**[!UICONTROL 建立挑戰]**。

   ![](assets/challenge-create.png)

1. 選擇挑戰型別：

   * **[!UICONTROL 標準]**：客戶以任何順序完成任何指定數量的工作
   * **[!UICONTROL 連續執行]**：客戶連續多次完成相同的工作
   * **[!UICONTROL 循序]**：客戶以定義的順序完成工作

## 設定挑戰結構 {#structure}

「結構」標籤可讓您定義挑戰的整理方式：其屬性、排程、要完成的工作和要給予的獎勵。

### 定義挑戰屬性並使用自訂中繼資料 {#properties}

1. 在[挑戰]屬性窗格中，設定挑戰屬性：

   ![](assets/challenge-create-properties.png)

   **名稱**：輸入質詢的描述性名稱。 此名稱會出現在挑戰清單中，並協助您識別挑戰。

   **描述**：輸入挑戰描述。

1. 使用&#x200B;**[!UICONTROL 自訂中繼資料]**&#x200B;區段，以使用索引鍵/值配對來新增自訂中繼資料。 此中繼資料可用於追蹤、細分或與外部系統的整合。

### 排程挑戰 {#schedule}

選取![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL 開啟排程]**&#x200B;圖示以排程挑戰。

* **開始日期和時間**：設定客戶可提出質詢的時間（格式： mm/dd/yyyy， —：— AM/PM）。

* **結束日期和時間**：設定質詢過期且不再接受新完成的時間（格式： mm/dd/yyyy， —：— AM/PM）。

* **時區**：挑戰預設使用收件者的當地時區。

* **任務必須完成**：選擇客戶何時可以完成任務：

   * **[!UICONTROL 在挑戰期間的任何時間]**：客戶可以在挑戰開始與結束日期之間的任何時間完成任務
   * **[!UICONTROL 在一天中的特定小時內]**：設定&#x200B;**[!UICONTROL 開始時間]**&#x200B;和&#x200B;**[!UICONTROL 結束時間]**，將工作完成限制在特定每日小時內

挑戰排程現在已設定。 您現在可以新增客戶需要完成的工作。

### 新增任務 {#add-tasks}

任務會定義客戶為獲得獎勵必須完成的特定動作或里程碑。 您可以設定任務型別（購買、支出、造訪、參與、自訂事件）、數量、產品篩選器和獎勵。

根據您的挑戰型別，客戶完成工作的方式會有所不同：

* **標準挑戰**：以任意順序完成任何指定數量的工作
* **連續挑戰**：連續多次完成相同工作
* **循序挑戰**：以定義的順序完成任務

若要新增任務至您的挑戰，請遵循下列步驟：

1. 在&#x200B;**[!UICONTROL 工作]**&#x200B;區段中，選取&#x200B;**[!UICONTROL 新增工作]**。

   ![](assets/challenge-create-add-task.png)

1. 「作業」詳細目錄隨即開啟。 從清單中選取一或多個工作，然後選取&#x200B;**[!UICONTROL 新增]**。 若要建立新工作，請選取&#x200B;**[!UICONTROL 新增]**。

   如需建立和設定工作的詳細指示，請參閱[建立工作](create-tasks.md)。

1. 在&#x200B;**[!UICONTROL 任務完成需求]**&#x200B;區段中，指定何時應將挑戰視為已完成：

   * **[!UICONTROL 客戶選擇1項任務完成]**：客戶可以從挑戰中選取並完成任何單一任務以取得獎勵
   * **[!UICONTROL 客戶完成特定數量的工作]**：客戶必須完成定義的數量工作。 輸入作業完成的所需數量。

1. 依預設，挑戰可讓客戶跨多個交易完成任務。 若要在單一交易中要求完成所有工作，請選取![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL 設定]**&#x200B;圖示並開啟&#x200B;**[!UICONTROL 單一交易]**&#x200B;選項。

   ![](assets/challenge-create-single-transaction.png)

### 設定獎勵 {#rewards}

獎勵是客戶在完成挑戰時獲得的忠誠度點數或權益。 設定如何及何時提供獎勵，以激勵客戶參與。

1. 在&#x200B;**[!UICONTROL 獎勵傳遞]**&#x200B;下拉式清單中，選擇何時應傳遞獎勵：

   * **[!UICONTROL 當挑戰完成時提供獎勵]**：當客戶完成整個挑戰時給予所有獎勵
   * **[!UICONTROL 當挑戰進度完成時，在任務完成里程碑提供獎勵]**：當客戶完成個別任務時，獎勵遞增（僅當挑戰需要完成多個任務時可用）

1. 從下拉式清單中選取您的獎勵提供者。 這是管理客戶點數和獎勵的忠誠度解決方案。

1. 根據您選取的傳送方式設定獎勵金額：

   +++完成挑戰時提供獎勵

   在&#x200B;**挑戰完成[的]忠誠度點數**&#x200B;欄位中，指定當客戶完成整個挑戰時要給予的總獎勵金額。

   欄位名稱會顯示您在所選提供者中定義的熟客點名稱。 例如，如果您的提供者使用「Luma點」，欄位會顯示「挑戰完成時的Luma點數」。

   ![](assets/challenge-create-reward-total.png)

   **範例**：在上面的熒幕擷圖中，客戶在完成挑戰賽時獲得100分。

   +++

   +++在任務完成里程碑時傳遞獎勵

   指定任務完成里程碑的獎勵金額。 此選項可讓您建立漸進式獎勵，當客戶完成挑戰時提高他們的積極性。

   對於您想要提供獎勵的任何工作，請切換獎勵選項，並指定當客戶完成該特定工作時要獎勵多少分。 您可以選擇僅獎勵特定任務完成 — 例如，如果您有10個任務，則可能僅獎勵任務1、5和10。

   ![](assets/challenge-create-reward-milestones.png)

   **範例**：在上面的熒幕擷圖中，客戶在完成第一個任務時可獲得10分，在完成第二個任務後可獲得50分，當挑戰完成時可獲得60分。

   >[!TIP]
   >
   >請考慮提高後續工作的獎勵值，以在整個挑戰中維持客戶的參與度。

   +++

挑戰結構現在已設定任務和獎勵。 您現在可以設計內容卡以向客戶顯示挑戰。

## 設定內容卡片 {#configure-content-cards}

內容卡可在客戶裝置上以視覺化方式呈現您的挑戰，顯示挑戰資訊、進度和獎勵。 深入瞭解[內容卡](../content-card/create-content-card.md)。

若要設定挑戰的內容卡：

1. 在挑戰編輯器中，瀏覽至&#x200B;**[!UICONTROL Content]**&#x200B;標籤。

1. 輸入內容卡的&#x200B;**[!UICONTROL 名稱]**。

1. 選取相關聯的&#x200B;**[!UICONTROL 通道組態]**。 管道設定會定義將內容傳送給客戶的方式和位置。 如需詳細資訊，請參閱[頻道設定](../configuration/channel-surfaces.md)。

1. 選取&#x200B;**[!UICONTROL 編輯內容]**&#x200B;以設計您的內容卡。

   ![](assets/challenge-create-content.png)

如需有關設計和個人化內容卡的詳細資訊，請參閱[設計內容卡](../content-card/design-content-card.md)。

內容卡現在已設定完畢。 您現在可以設定訊息，以在整個挑戰生命週期中吸引客戶。

### 設定傳訊 {#configure-messaging}

設定多管道訊息，在挑戰生命週期的關鍵階段與客戶互動。

1. 導覽至&#x200B;**[!UICONTROL 傳訊]**&#x200B;標籤。

1. 為每個生命週期階段設定訊息：

   ![](assets/challenge-create-messaging.png)

   * **啟動訊息**：當挑戰開始時，通知客戶並提供初始詳細資料
   * **進行中訊息**：讓客戶在挑戰期間保持參與，並提供提醒、進度更新及鼓勵以繼續
   * **完成訊息**：慶祝成功、確認獎勵分配，並建議下一個挑戰或動作

1. 針對每個階段，選取&#x200B;**[!UICONTROL 新增&#x200B;*階段*訊息]**&#x200B;以建立該階段的訊息。

1. 選擇您想要的頻道： **[!UICONTROL 應用程式內]**、**[!UICONTROL 電子郵件]**&#x200B;或&#x200B;**[!UICONTROL 推播通知]**，並選取相關的頻道設定。

1. 選取![](assets/do-not-localize/Smock_More_18_N.svg)圖示並選擇&#x200B;**[!UICONTROL 編輯]**&#x200B;來設計您的訊息內容。

   有關為特定通道建立訊息的詳細資訊，請參閱：

   * [應用程式內訊息檔案](../in-app/get-started-in-app.md)
   * [電子郵件訊息檔案](../email/get-started-email.md)
   * [推播通知檔案](../push/get-started-push.md)

1. 視需要對每個階段和管道重複這些步驟。

訊息設定現已完成。 您現在可以定義哪些客戶符合參與挑戰的資格。

## 選取挑戰對象 {#audience}

定義哪些客戶有資格參與您的忠誠度挑戰。

1. 導覽至&#x200B;**[!UICONTROL 對象]**&#x200B;標籤，然後按一下&#x200B;**[!UICONTROL 選取對象]**&#x200B;按鈕。

   ![](assets/challenge-create-audience.png)

1. 所有可用的Adobe Experience Platform對象都會顯示。 從清單中選取所需的對象。

1. 選取&#x200B;**[!UICONTROL 新增對象]**&#x200B;以確認您的選擇。

您的挑戰設定現已完成。 您現在可以產生將協調挑戰傳送的歷程。

## 產生並啟用歷程 {#review-and-publish}

當您的挑戰設定完成後，產生關聯的歷程，將協調挑戰交付和客戶互動。 若要這麼做，請選取&#x200B;**[!UICONTROL 產生歷程]**。

![](assets/challenge-create-generate-journey.png)

Journey Optimizer會自動建立草稿狀態的[歷程](../building-journeys/journey-gs.md)。 自動產生的歷程會以名稱格式「挑戰： [挑戰名稱]」出現在您的歷程詳細目錄中。

視需要檢閱歷程設定，然後[啟動歷程](../building-journeys/publish-journey.md)讓客戶可以提出挑戰。

歷程將在您指定的挑戰開始日期自動開始，並根據您的設定傳送內容和訊息。

>[!NOTE]
>
>如有需要，可自訂自動產生的歷程，以新增其他邏輯或訊息。 不過，直接對歷程進行的變更不會同步回挑戰設定。 如果您稍後編輯挑戰，則重新產生歷程時，所有歷程自訂都將遺失。

## 後續步驟 {#next-steps}

* [管理挑戰](manage-challenges.md) — 瞭解如何編輯、監控和最佳化挑戰
* [瞭解忠誠度挑戰](get-started.md) — 檢閱功能
