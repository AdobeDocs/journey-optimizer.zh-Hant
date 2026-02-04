---
solution: Journey Optimizer
product: journey optimizer
title: 建立針對忠誠度挑戰的任務
description: 瞭解如何在Adobe Journey Optimizer中針對忠誠度挑戰建立及設定任務。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人測試版" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---


# 建立任務 {#create-tasks}

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* [開始解決忠誠度挑戰](get-started.md) — 概述、工作流程、必要條件
* [存取忠誠度挑戰](access-loyalty-challenges.md) — 詳細目錄和篩選
* [建立挑戰](create-challenges.md) — 建置並設定挑戰
* **建立任務** ◀︎ **您在這裡** — 定義挑戰任務
* [管理挑戰](manage-challenges.md) — 編輯、監視、最佳化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中，可能無法在您的環境中使用。 若要要求存取權，請聯絡您的Adobe代表。 深入瞭解[可用性標籤](../rn/releases.md#availability-labels)。

## 概觀 {#overview}

任務會定義客戶在忠誠度挑戰中必須完成的特定動作或里程碑，才能獲得獎勵。 您可以設定任務型別、數量、產品需求和獎勵值，以建立吸引人且個人化的忠誠度體驗。

每項任務都代表可測量的動作，有助於完成挑戰。 任務是可重複使用的元件，可以獨立建立，然後新增到一個或多個挑戰，或直接在挑戰中建立。

### 任務在不同挑戰型別中的運作方式 {#task-overview}

<!-- VISUAL: Diagram showing how task completion works differently for Standard, Streak, and Sequential challenges with examples -->

根據您的挑戰型別（標準、連續或順序），客戶完成任務的方式有所不同：

* **標準挑戰**：客戶以任何順序完成任何指定數量的工作
* **連續挑戰**：客戶連續多次完成相同工作
* **循序挑戰**：客戶以定義的順序完成任務

## 建立任務 {#create-task}

<!-- SCREENSHOT: Two screenshots side by side showing the two entry points: Tasks tab with "Create task" button, and challenge editor with "Add task" button -->

您可以從兩個進入點建立任務。 無論您從何處開始，設定程式都相同。

+++從任務詳細目錄

1. 導覽至Journey Optimizer中的&#x200B;**[!UICONTROL 忠誠度挑戰]**。

1. 選取&#x200B;**[!UICONTROL 工作]**&#x200B;標籤。

1. 選取&#x200B;**[!UICONTROL 建立任務]**。

從詳細目錄建立的任務會儲存起來，並可在多個挑戰中重複使用。

+++

+++從挑戰中

1. 開啟現有的挑戰或建立新的挑戰。

1. 導覽至&#x200B;**[!UICONTROL 工作]**&#x200B;區段。

1. 選取&#x200B;**[!UICONTROL 新增工作]**，然後選擇&#x200B;**[!UICONTROL 建立新工作]**。

以這種方式建立的任務會自動新增到您的挑戰中，也會儲存到任務詳細目錄中以供在其他挑戰中重複使用。

+++

### 定義任務屬性 {#define-task-properties}

<!-- SCREENSHOT: Task properties form showing Task name and Task description fields -->

設定基本工作資訊：

* **工作名稱**：輸入工作的描述性名稱。 您和您的團隊可以看見此名稱，但根據您的內容卡設計，客戶可能不會看到此名稱。
* **工作說明**： （選擇性）新增有關工作目的或需求的詳細資料。

### 選擇客戶活動 {#choose-activity}

<!-- SCREENSHOT: Activity type selection showing Purchase and Spend options with radio buttons -->

選取客戶必須執行的客戶活動型態，才能完成此作業：

* **[!UICONTROL 購買]**：客戶必須購買一或多個專案才能完成此工作
* **[!UICONTROL 支出]**：客戶必須支出指定的金額才能完成此工作

選取最符合您結果目標的客戶活動。 每個活動型別都有特定的可設定屬性，可進一步定義及塑造任務需求。

### 定義屬性 {#define-attributes}

<!-- SCREENSHOT: Attributes form for Purchase activity showing Quantity field, Eligible items & exclusions field, and parameters icon for optional attributes -->

根據您選取的活動型別設定工作屬性：

+++針對購買活動

設定下列屬性：

* **數量**：輸入完成此任務必須購買的專案數
* **符合資格的專案和排除**：定義計入任務完成的專案或專案群組，以及不計入任務完成的專案或專案群組。深入瞭解[定義合格專案和排除專案](#eligible-items-exclusions)

**選用屬性** （透過引數圖示設定）：

* **最小支出值金額**：設定最低購買金額需求
* **最大交易數**：限制可用於完成工作的交易數

+++

+++針對支出活動

設定下列屬性：

* **金額**：輸入完成工作所需的總支出金額
* **交易數上限**：指定允許符合支出需求的交易數。 如果您不想限制交易數目，可以從引數圖示停用此屬性
* **合格專案與排除**： （選擇性）定義計入任務完成的專案或專案群組，以及不計入任務完成的專案或專案群組。深入瞭解[定義合格專案和排除專案](#eligible-items-exclusions)

+++

設定所有屬性後，選取&#x200B;**[!UICONTROL 建立]**&#x200B;以儲存工作。 任務會儲存到您的任務詳細目錄，如果是從挑戰中建立的，則會自動新增到該挑戰。

## 定義適用料號與排除專案 {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

對於「採購」與「支出」作業，您可以定義適用的料號與群組，也可以排除料號與群組。 這可讓您鎖定特定產品、類別或位置，以符合您的挑戰目標。

**使用案例：**

* 建立一項工作，獎勵購買咖啡專案的客戶，但不包括清倉產品
* 將支出任務限制在特定產品類別
* 在任務完成時排除禮品卡或促銷專案

### 設定合格專案 {#configure-eligible-items}

若要定義符合資格的專案，請使用&#x200B;**[!UICONTROL 符合資格的任務購買僅限於下列]**&#x200B;區段：

* 輸入特定專案ID、類別或目的地ID （以逗號分隔）
* 範例：`SKU001, SKU002, CategoryA, StoreLocation123`
* **秘訣**：輸入`*`，讓所有購買都符合資格（如果留空則為預設行為）

### 設定排除專案 {#configure-exclusions}

若要從任務排除專案，請使用&#x200B;**[!UICONTROL 下列專案已從此任務排除]**&#x200B;區段：

* 輸入不應計入任務完成的特定專案ID、類別或目的地ID
* 範例：`CLEARANCE01, GIFTCARD, SALE_CATEGORY`
* 常見排除專案：銷售或結算專案、禮品卡、促銷專案

>[!NOTE]
>
>排除專案的優先順序高於適用專案。 如果專案同時符合合格專案和排除專案，則會將其從任務中排除。

## 後續步驟 {#next-steps}

現在您知道如何建立和設定工作了：

* [建立挑戰](create-challenges.md) — 瞭解如何建立完整的挑戰並設定獎勵
* [管理挑戰](manage-challenges.md) — 瞭解如何編輯、監控和最佳化挑戰
