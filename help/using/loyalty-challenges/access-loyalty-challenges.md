---
solution: Journey Optimizer
product: journey optimizer
title: 存取忠誠度挑戰
description: 瞭解如何存取、搜尋和篩選Adobe Journey Optimizer中的忠誠度挑戰。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人測試版" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---


# 存取忠誠度挑戰 {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* [開始解決忠誠度挑戰](get-started.md) — 概述、工作流程、必要條件
* **存取忠誠度挑戰** ◀︎ **您在這裡** — 詳細目錄和篩選
* [建立挑戰](create-challenges.md) — 建置並設定挑戰
* [建立任務](create-tasks.md) — 定義挑戰任務
* [管理挑戰](manage-challenges.md) — 編輯、監視、最佳化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中，可能無法在您的環境中使用。 若要要求存取權，請聯絡您的Adobe代表。 深入瞭解[可用性標籤](../rn/releases.md#availability-labels)。

## 存取忠誠度挑戰詳細目錄 {#access-inventory}

<!-- SCREENSHOT: Journey Optimizer main menu showing "Loyalty challenges" under "Customer journeys" section -->

若要存取忠誠度挑戰，請導覽至Journey Optimizer，並在「**[!UICONTROL 客戶歷程]**」區段下選取「**[!UICONTROL 忠誠度挑戰]**」。

<!-- SCREENSHOT: Loyalty Challenges landing page showing the two tabs: Challenges and Tasks -->

「忠誠度挑戰」頁面會顯示兩個標籤：

* **[!UICONTROL 挑戰]**：檢視和管理所有忠誠度挑戰

* **[!UICONTROL 任務]**：檢視和管理所有可在挑戰中重複使用的任務

## 挑戰詳細目錄 {#challenges-tab}

<!-- SCREENSHOT: Challenges tab showing the inventory table with columns: Challenge name, Status, Type, Start date, End date, Created by, Last modified, Tags -->

「挑戰」索引標籤會依上次修改日期排序顯示所有挑戰，最近修改的挑戰會先出現。 會顯示下列資訊：

* **[!UICONTROL 挑戰名稱]**：您指派給挑戰的名稱
* **[!UICONTROL 狀態]**：目前詢問的狀態（請參閱下方的狀態說明）
* **[!UICONTROL 型別]**：挑戰型別（標準、條紋或循序）
* **[!UICONTROL 開始日期]**：挑戰變成使用中時
* **[!UICONTROL 結束日期]**：挑戰到期的時間
* **[!UICONTROL 建立者]**：建立挑戰的使用者
* **[!UICONTROL 上次修改]**：上次修改的日期和時間
* **[!UICONTROL 標籤]**：適用於組織挑戰的任何標籤

### 挑戰狀態 {#challenge-statuses}

<!-- VISUAL: Status badges showing different challenge statuses with color coding: Draft (gray), Scheduled (blue), Live (green), Completed (gray), Stopped (red), Archived (gray) -->

挑戰會以不同的狀態顯示，指示其在生命週期中的目前狀態：

* **草稿**：正在建立或編輯挑戰
* **已排程**：挑戰已發佈，將於開始日期生效
* **已上線**：挑戰正在進行，客戶可以參加
* **已完成**：挑戰結束日期已過，或已達成目標
* **已停止**：在完成前已手動停止挑戰
* **已封存**：已封存挑戰以供組織使用

如需狀態轉換與挑戰生命週期的詳細資訊，請參閱[挑戰生命週期](manage-challenges.md#challenge-lifecycle)。

### 搜尋和篩選挑戰 {#search-challenges}

<!-- SCREENSHOT: Search bar and filter panel showing available filters (status, type, dates, tags) with an example of active filters applied -->

您可以使用搜尋和篩選器快速找出挑戰：

**搜尋：**

* 從挑戰名稱或說明輸入關鍵字，使用搜尋列來尋找挑戰。 當您輸入時，搜尋會即時更新。

**篩選器：**

* 套用一或多個篩選器以縮小結果範圍：
   * **狀態**：依質詢狀態篩選（草稿、已排程、即時、已完成、已停止、已封存）
   * **型別**：依挑戰型別篩選（標準、條紋、循序）
   * **日期**：依開始日期或結束日期範圍篩選
   * **標籤**：依套用至挑戰的標籤篩選

您可以同時合併多個篩選器。 例如，篩選標籤為「Summer2024」的Live Standard挑戰，以快速找到作用中的季節性行銷活動。

若要清除篩選器，請選取&#x200B;**[!UICONTROL 全部清除]**&#x200B;或移除個別篩選器。

### 針對挑戰採取行動 {#inventory-actions}

<!-- SCREENSHOT: More actions menu (three dots) expanded showing options: Edit, Duplicate, Stop, Archive, Delete -->

在「挑戰」標籤中，您可以對挑戰執行快速動作：

* **檢視挑戰詳細資料**：選取挑戰名稱以開啟其詳細資料頁面
* **編輯挑戰**：選取&#x200B;**[!UICONTROL 更多動作]**&#x200B;功能表（三個點），然後選擇&#x200B;**[!UICONTROL 編輯]**
* **複製挑戰**：選取&#x200B;**[!UICONTROL 其他動作]**&#x200B;功能表，然後選擇&#x200B;**[!UICONTROL 複製]**
* **停止即時挑戰**：選取&#x200B;**[!UICONTROL 其他動作]**&#x200B;功能表，然後選擇&#x200B;**[!UICONTROL 停止]**
* **封存挑戰**：選取&#x200B;**[!UICONTROL 其他動作]**&#x200B;功能表，然後選擇&#x200B;**[!UICONTROL 封存]**
* **刪除草稿挑戰**：選取&#x200B;**[!UICONTROL 更多動作]**&#x200B;功能表，然後選擇&#x200B;**[!UICONTROL 刪除]** （僅適用於草稿）

如需建立後管理挑戰的詳細資訊，包括編輯限制、複製策略、效能監控和疑難排解，請參閱[管理挑戰](manage-challenges.md)。

## 任務詳細目錄 {#tasks-tab}

<!-- SCREENSHOT: Tasks tab showing the inventory table with columns: Task name, Task type, Description, Created by, Last modified, Used in challenges -->

「任務」標籤會顯示可用於多個挑戰的所有可重複使用任務。 建立或編輯任何挑戰時，可選取此處建立的任務。

「作業」詳細目錄會顯示下列資訊：

* **[!UICONTROL 任務名稱]**：您指派給任務的名稱
* **[!UICONTROL 任務型別]**：動作型別（購買、支出金額、造訪、參與、自訂事件）
* **[!UICONTROL 描述]**：工作所需內容的簡短描述
* **[!UICONTROL 建立者]**：建立工作的使用者
* **[!UICONTROL 上次修改]**：上次修改的日期和時間
* **[!UICONTROL 用於挑戰]**：目前使用此任務的挑戰數

### 對任務執行動作 {#tasks-actions}

在「工作」標籤中，您可以對工作執行動作：

* **檢視工作詳細資料**：選取工作名稱以檢視完整組態
* **編輯工作**：選取&#x200B;**[!UICONTROL 更多動作]**&#x200B;功能表（三個點），然後選擇&#x200B;**[!UICONTROL 編輯]**
* **複製工作**：選取&#x200B;**[!UICONTROL 其他動作]**&#x200B;功能表，然後選擇&#x200B;**[!UICONTROL 複製]**
* **刪除工作**：選取&#x200B;**[!UICONTROL 更多動作]**&#x200B;功能表並選擇&#x200B;**[!UICONTROL 刪除]** （除非未用於任何使用中的挑戰）
* **檢視使用量**：檢視目前使用任務的挑戰

## 後續步驟 {#next-steps}

現在您知道如何存取和瀏覽忠誠度挑戰詳細目錄：

* [建立挑戰](create-challenges.md) — 瞭解如何建立您的第一個挑戰並設定任務
* [建立任務](create-tasks.md) — 瞭解如何針對挑戰定義可重複使用的任務
* [管理挑戰](manage-challenges.md) — 瞭解如何編輯、監控和最佳化挑戰
