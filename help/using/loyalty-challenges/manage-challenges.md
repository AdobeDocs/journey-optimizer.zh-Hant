---
solution: Journey Optimizer
product: journey optimizer
title: 管理忠誠度挑戰
description: 瞭解如何在Adobe Journey Optimizer中管理、監控和最佳化忠誠度挑戰。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人測試版" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# 管理挑戰與工作 {#manage-challenges}

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* [開始解決忠誠度挑戰](get-started.md) — 概述、工作流程、必要條件
* [存取忠誠度挑戰](access-loyalty-challenges.md) — 詳細目錄和篩選
* [建立挑戰](create-challenges.md) — 建置並設定挑戰
* [建立任務](create-tasks.md) — 定義挑戰任務
* **管理挑戰** ◀︎**您在這裡** — 編輯、監視、最佳化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中，可能無法在您的環境中使用。 若要要求存取權，請聯絡您的Adobe代表。 深入瞭解[可用性標籤](../rn/releases.md#availability-labels)。

## 管理挑戰 {#manage-challenges-section}

### 挑戰狀態 {#challenge-lifecycle}

挑戰在生命週期中會經歷不同的狀態：

* **草稿**：正在建立或編輯挑戰，客戶尚未能使用。
* **已發佈**：挑戰正在作用中，而且已建立關聯的歷程。

### 編輯挑戰 {#edit-challenges}

您可以在「挑戰」詳細目錄中開啟挑戰，以編輯挑戰。 編輯行為因挑戰狀態而異：

**草稿挑戰**：您擁有完整的編輯功能。 所有屬性、工作、內容和訊息都可以不受限制地修改。

**已發佈的挑戰**：當您開啟已發佈的挑戰以進行編輯時，必須先將其還原為草稿狀態。

* 直接對自動產生的歷程進行的任何自訂都將遺失。
* 挑戰會回到草稿狀態。
* 進行變更後，您必須儲存並再次發佈挑戰。
* 您必須重新發佈關聯的歷程，才能讓客戶使用更新的挑戰。

>[!IMPORTANT]
>
>將已發佈的質詢還原為草稿無法復原。 在繼續之前，請先考慮對您作用中歷程的影響。

### 重複的挑戰 {#duplicate-challenges}

複製挑戰會建立完整的復本，且所有工作、內容和訊息均完整無缺，讓您能夠快速建立新版本，而不用從頭開始。

複製挑戰：

1. 導覽至&#x200B;**[!UICONTROL 挑戰]**&#x200B;標籤，並找出您要複製的挑戰。

1. 選取該挑戰旁的![](assets/do-not-localize/Smock_More_18_N.svg)圖示，然後選擇&#x200B;**[!UICONTROL 複製]**。

1. 挑戰副本已建立。 開啟重複的挑戰並修改必要的屬性。

1. 儲存複製的挑戰並產生關聯的歷程。

### 監視效能 {#monitor-performance}

<!-- SCREENSHOT: Challenge Performance tab showing key metrics dashboard with participation, completion, reward, and engagement metrics -->

透過關鍵量度追蹤挑戰效能：

* **參與率量度**：
   * 註冊：加入挑戰的客戶數量
   * 主動參與者：目前參與挑戰的客戶
* **完成量度**：
   * 完成率：完成挑戰的已註冊客戶百分比
   * 平均完成時間：完成所有任務所花費的平均時間
* **獎勵量度**：
   * 分配的獎勵總計：所有獎勵的彙總值
   * 依型別的獎勵：依獎勵類別的獎勵細目
* **參與量度**：
   * 內容卡片曝光次數：挑戰內容卡片顯示的次數
   * 訊息傳送：成功跨所有通道傳送的訊息數

若要存取效能資料：

1. 導覽至「忠誠度挑戰」詳細目錄中的&#x200B;**[!UICONTROL 挑戰]**&#x200B;索引標籤。

1. 選取您要監視的挑戰。

1. 開啟&#x200B;**[!UICONTROL 效能]**&#x200B;標籤以檢視即時度量和分析。

<!-- SCREENSHOT: Journey report showing challenge performance data with graphs and tables -->

您也可以存取[自動產生的歷程報告](../reports/journey-global-report-cja.md)中的詳細效能資料，這些報告會提供其他見解和歷史趨勢。

## 管理任務 {#manage-tasks}

任務是可重複使用的元件，可用於應對多個挑戰。 有效管理任務可確保在忠誠度方案間的一致性，並可讓您更輕鬆地集中更新任務定義。 在一個挑戰中建立的任務可以重複用於其他挑戰，減少重複並保持標準化。

### 編輯任務 {#edit-tasks}

您可以從任務詳細目錄中編輯現有任務。 考慮以下事項：

* **未用於使用中挑戰的任務**：可以自由編輯。 所有屬性都可以修改而不會造成影響。
* **用於即時挑戰的任務**：請小心，因為變更會影響使用該任務的所有挑戰。 修改會立即套用至所有參照挑戰。

若要編輯任務：

1. 導覽至「忠誠度挑戰」詳細目錄中的&#x200B;**[!UICONTROL 任務]**&#x200B;標籤。

1. 找到您要編輯的工作。

1. 選取工作名稱，以在編輯模式中開啟它。

1. 視需要修改工作屬性：
   * 更新任務名稱或描述
   * 變更活動型別或屬性
   * 調整適用料號與排除專案
   * 修改數量或金額需求

1. 儲存您的變更。

>[!WARNING]
>
>當編輯在即時挑戰中積極使用的任務時，請考慮使用新版本建立副本，而不是修改原始版本。 這可防止對使用中挑戰進行意外變更，並讓您在套用修改之前先測試修改。

### 刪除任務 {#delete-tasks}

任務目前未用於任何挑戰時，才能將其刪除。 刪除任務之前：

* 檢查任務詳細目錄中的&#x200B;**[!UICONTROL 用於挑戰]**&#x200B;計數。
* 確保沒有草稿、已排程或即時挑戰參考任務。

若要刪除任務，請執行下列動作：

1. 導覽至「忠誠度挑戰」詳細目錄中的&#x200B;**[!UICONTROL 任務]**&#x200B;標籤。

1. 找到您要刪除的工作。

1. 驗證&#x200B;**[!UICONTROL 用於挑戰]**&#x200B;計數是否顯示0。 如果計數大於0，您必須在刪除之前先從所有挑戰中移除任務。

1. 選取工作旁的![](assets/do-not-localize/Smock_More_18_N.svg)圖示。

1. 選擇&#x200B;**[!UICONTROL 刪除]**。

1. 在對話方塊中確認刪除。

>[!NOTE]
>
>如果任務用於任何挑戰（草稿、已排程或即時），您必須先將其從所有挑戰中移除，然後才能將其刪除。 如果您未來可能需要，請考慮封存或複製任務，而不是刪除它們。
