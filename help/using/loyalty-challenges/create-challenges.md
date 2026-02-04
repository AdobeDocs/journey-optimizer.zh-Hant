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
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '888'
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

<!-- SCHEMA: Visual workflow showing the 5 main steps with icons: Create challenge → Add tasks → Design content cards → Configure messaging → Review and publish -->

建立和啟動忠誠度挑戰會遵循此工作流程：

1. **建立挑戰** — 定義基本挑戰屬性，包括名稱、型別（標準、連續或循序）、對象和日期範圍。

1. **新增任務** — 定義客戶必須完成的特定動作，包括任務型別（購買、支出、造訪等）、數量、產品篩選器和獎勵。

1. **設計內容卡** — 使用顯示在客戶裝置上的Journey Optimizer內容卡，以視覺化方式呈現您的挑戰。

1. **設定訊息** （選用） — 設定關鍵階段的多通道訊息（應用程式內、電子郵件、推播、簡訊）：啟動、進行中及完成。

1. **檢閱並發佈** — 使用測試設定檔測試您的挑戰，然後發佈它以供您的目標對象使用。

## 建立挑戰 {#create-challenge}

<!-- SCREENSHOT: Challenge creation screen showing challenge properties form with fields for name, type, audience, dates -->

若要建立新的忠誠度挑戰：

1. 導覽至Journey Optimizer中的&#x200B;**[!UICONTROL 忠誠度挑戰]**。

1. 選取&#x200B;**[!UICONTROL 挑戰]**&#x200B;標籤。

1. 選取&#x200B;**[!UICONTROL 建立挑戰]**。

1. 設定挑戰屬性：

   **挑戰名稱**：輸入挑戰的描述性名稱。 此名稱會出現在挑戰清單中，並協助您識別挑戰。

   **挑戰型別**：選取下列其中一種型別：
   * **[!UICONTROL 標準]**：客戶以任何順序完成任何指定數量的工作
   * **[!UICONTROL 連續執行]**：客戶連續多次完成相同的工作
   * **[!UICONTROL 循序]**：客戶以定義的順序完成工作

   **目標對象**：選取定義誰可以參與此挑戰的對象區段。 您必須先在Experience Platform中建立受眾，才能建立挑戰。 如需詳細資訊，請參閱[開始使用對象](../audience/about-audiences.md)。

   **開始日期**：設定客戶何時可提出挑戰。

   **結束日期**：設定質詢過期且不再接受新完成的時間。

<!-- VISUAL: Comparison table or diagram showing the three challenge types (Standard, Streak, Sequential) with examples of each -->

### 新增任務 {#add-tasks}

任務會定義客戶為獲得獎勵必須完成的特定動作或里程碑。 您可以設定任務型別（購買、支出、造訪、參與、自訂事件）、數量、產品篩選器和獎勵。

根據您的挑戰型別，客戶完成工作的方式會有所不同：

* **標準挑戰**：以任意順序完成任何指定數量的工作
* **連續挑戰**：連續多次完成相同工作
* **循序挑戰**：以定義的順序完成任務

若要新增任務至您的挑戰，請選取[任務]區段中的[新增任務] **&#x200B;**，並設定任務屬性。

如需建立和設定工作的詳細指示，請參閱[建立工作](create-tasks.md)。

### 設定內容卡片 {#configure-content-cards}

<!-- SCREENSHOT: Content cards configuration section in the challenge editor -->

內容卡可在客戶裝置上以視覺化方式呈現您的挑戰，顯示挑戰資訊、進度和獎勵。 深入瞭解[內容卡](../content-card/get-started-content-card.md)。

<!-- VISUAL: Example content card designs showing different states: challenge start, in-progress with progress bar, completion with reward -->

若要設定挑戰的內容卡：

1. 在挑戰編輯器中，導覽至&#x200B;**[!UICONTROL 內容卡]**&#x200B;區段。

1. 選取&#x200B;**[!UICONTROL 建立內容卡]**&#x200B;或選擇現有的範本。

1. 設計您的內容卡：
   * 新增影像、文字和品牌元素
   * 包含[個人化權杖](../personalization/personalization-syntax.md)以顯示客戶特定資訊
   * 顯示挑戰進度指示器
   * 顯示獎勵和獎勵

1. 設定內容卡片顯示的時間：
   * **挑戰開始**：顯示挑戰何時可用
   * **進行中**：當客戶主動參與時顯示
   * **完成**：在客戶完成所有任務後顯示

1. 預覽不同裝置上的內容卡以確保正確顯示。

1. 儲存內容卡設定。

如需有關設計和個人化內容卡的詳細資訊，請參閱[設計內容卡](../content-card/design-content-card.md)。

### 設定傳訊 {#configure-messaging}

<!-- SCREENSHOT: Messaging configuration section showing the three lifecycle stages: Launch, In-progress, Completion -->

設定多管道訊息，在挑戰生命週期的關鍵階段與客戶互動。

<!-- VISUAL: Timeline diagram showing when each message type is sent during the challenge lifecycle -->

設定訊息以因應挑戰：

1. 在挑戰編輯程式中，導覽至&#x200B;**[!UICONTROL 傳訊]**&#x200B;區段。

1. 為每個生命週期階段設定訊息：

   **啟動訊息** — 當挑戰開始時通知客戶：
   * 選取頻道： [應用程式內](../in-app/get-started-in-app.md)、[電子郵件](../email/get-started-email.md)、[推播通知](../push/get-started-push.md)或[簡訊](../sms/get-started-sms.md)
   * 設計包含挑戰詳細資訊和call-to-action的訊息
   * 設定時間：當挑戰上線或排程特定時間時立即傳送

   **進行中訊息** — 在挑戰期間保持客戶參與：
   * 定義觸發條件（例如50%完成、特定任務完成）
   * 建立提醒訊息以鼓勵持續參與
   * 包含進度更新和後續步驟

   **完成訊息** — 慶祝成功並傳送獎勵：
   * 恭喜客戶完成挑戰
   * 確認獎勵分配
   * 提供申請獎勵的說明
   * 建議下一個挑戰或行動

有關為特定通道建立訊息的詳細資訊，請參閱：

* [應用程式內訊息檔案](../in-app/get-started-in-app.md)
* [電子郵件訊息檔案](../email/get-started-email.md)
* [推播通知檔案](../push/get-started-push.md)
* [SMS訊息檔案](../sms/get-started-sms.md)

## 檢閱並發佈挑戰 {#review-and-publish}

<!-- SCREENSHOT: Review screen showing summary of challenge configuration with all components listed -->

發佈挑戰前：

1. **檢閱所有元件**：驗證挑戰內容、工作、獎勵、內容卡和傳訊設定。

1. **測試體驗**：使用[測試設定檔](../test-approve/test-profiles.md)來驗證內容卡顯示和工作觸發程式行為。

1. **發佈**：選取&#x200B;**[!UICONTROL 發佈]**，讓您的目標對象可以使用挑戰。

<!-- SCREENSHOT: Journeys inventory showing the auto-generated journey in Draft status with name format "Challenge: [Challenge Name]" -->

當您發佈挑戰時，Journey Optimizer會自動建立草稿狀態的[歷程](../building-journeys/journey-gs.md)。 自動產生的歷程會以名稱格式「挑戰： [挑戰名稱]」出現在您的歷程詳細目錄中。

若要讓客戶瞭解此挑戰：

1. 導覽至Journey Optimizer中的&#x200B;**[!UICONTROL 歷程]**&#x200B;詳細目錄。

1. 找到自動產生的歷程（其名稱會以「Challenge：」作為前置詞）。

1. [啟動歷程](../building-journeys/publishing-the-journey.md)。

歷程會在您指定的挑戰開始日期自動開始。

>[!NOTE]
>
>自動產生的歷程會顯示在您的歷程詳細資料中，並可視需要自訂。 不過，直接對歷程進行的變更不會同步回挑戰設定。

## 後續步驟 {#next-steps}

* [管理挑戰](manage-challenges.md) — 瞭解如何編輯、監控和最佳化挑戰
* [瞭解忠誠度挑戰](get-started.md) — 檢閱功能

