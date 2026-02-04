---
solution: Journey Optimizer
product: journey optimizer
title: 瞭解忠誠度挑戰
description: 瞭解Adobe Journey Optimizer中的忠誠度挑戰功能、工作流程和功能。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人測試版" type="Informative"
source-git-commit: 419c7b3913ca4da50c69ed36ffc1a8c8520607b4
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 2%

---


# 瞭解忠誠度挑戰 {#understand-loyalty-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="關於忠誠度挑戰"
>abstract="忠誠度挑戰可讓您建立個人化的參與優惠，以激勵客戶完成特定動作並獲得獎勵。"

忠誠度挑戰可讓您設計和部署個人化參與優惠方案，以激勵客戶完成特定行動並獲得獎勵。

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* [開始進行忠誠度挑戰](gs-loyalty-challenges.md) — 快速概覽和後續步驟
* **瞭解忠誠度挑戰** ◀︎ **您在這裡** — 功能、工作流程、先決條件
* [建立挑戰](create-challenges.md) — 建置並設定挑戰
* [管理挑戰](manage-challenges.md) — 編輯、監視、最佳化

>[!ENDSHADEBOX]

## 概觀 {#overview}

「忠誠度挑戰」提供完整解決方案，可大規模建立忠誠度計畫，從定義任務和里程碑，到跨管道提供內容和追蹤效能。 您可以建立三種型別的挑戰體驗、設定獎勵、在關鍵生命週期階段傳送多管道通知，並透過自動產生的歷程來監控效能，同時保持與外部忠誠度管理系統的整合。

## 運作方式 {#how-it-works}

建立和啟動忠誠度挑戰會遵循此工作流程：

1. **設定資料擷取** — 設定Experience Platform來源聯結器（如Chariceline）以擷取忠誠度事件資料，並追蹤客戶動作和進度。

2. **建立挑戰** — 定義基本挑戰屬性，包括名稱、型別（標準、連續或循序）、對象和日期範圍。

3. **新增任務** — 定義客戶必須完成的特定動作，包括任務型別（購買、支出、造訪等）、數量、產品篩選器和獎勵。

4. **設計內容卡** — 使用顯示在客戶裝置上的Journey Optimizer內容卡，以視覺化方式呈現您的挑戰。

5. **設定訊息** （選擇性） — 設定主要階段的多通道訊息（應用程式內、電子郵件、推播）：啟動、進行中及完成。

6. **檢閱並發佈** — 使用測試設定檔測試您的挑戰，然後發佈它以供您的目標對象使用。

7. **自動產生的歷程** — 當您發佈時，Journey Optimizer會自動建立協調內容卡傳遞和傳訊的歷程。

8. **啟用歷程** — 自動產生的歷程會在您的挑戰開始日期啟用，並管理所有客戶互動。

9. **監視效能** — 透過內建報告和歷程畫布，追蹤參與率、完成率、獎勵發佈和訊息參與。

>[!NOTE]
>
>自動產生的歷程會顯示在您的歷程詳細資料中，並可視需要自訂。 不過，直接對歷程進行的變更不會同步回挑戰設定。

## 主要功能 {#key-capabilities}

使用忠誠度挑戰來：

* **建立三種型別的挑戰**：
   * **Standard**：客戶完成任何數量的工作即可獲得獎勵。
   * **Streak**：客戶多次完成相同的工作。
   * **循序**：客戶以特定順序完成工作。

* **設計挑戰內容**：使用Journey Optimizer內容卡在客戶裝置上建立您挑戰的視覺化呈現。 內容卡片會在客戶裝置上顯示挑戰資訊、進度和獎勵。

* **設定任務需求**：定義客戶必須做什麼才能獲得獎勵，包括：
   * 任務型別（購買、支出金額、造訪等）
   * 數量需求
   * 使用SKU的產品包含/排除
   * 自訂屬性和條件

* **設定獎勵**：定義客戶在完成工作或完成整個挑戰後獲得的獎勵

* **傳送通知**：在關鍵階段跨多個管道（應用程式內、電子郵件、推播）傳遞訊息：
   * **啟動**：挑戰開始時
   * **進行中**：客戶在中途進出
   * **完成**：客戶完成挑戰時

* **追蹤效能**：監視自動產生的歷程並檢閱挑戰效能

### 重要限制 {#limitations}

* **沒有分類帳系統**：忠誠度挑戰不會追蹤貨幣值或點數餘額。 當客戶完成挑戰並獲得獎勵時，Journey Optimizer會呼叫您的外部忠誠度管理系統以處理點數分配。

* **僅限對象選擇**：您可以選取現有對象，但無法從「忠誠度挑戰」UI建立新對象。

## 先決條件 {#prerequisites}

使用忠誠度挑戰之前，請確定您擁有：

### 資料擷取設定 {#data-ingestion}

忠誠度挑戰需要透過Experience Platform來源聯結器擷取的資料來追蹤客戶進度和任務完成。

1. **設定支援的來源聯結器**：目前，毛細管聯結器一般可用。 已規劃其他聯結器。

2. **驗證資料擷取**：確保忠誠度事件和客戶資料流入Experience Platform並在Journey Optimizer中使用。

如需詳細指示，請參閱：

* [Experience Platform來原始檔](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [在Journey Optimizer中設定來源聯結器](../start/get-started-sources.md)

### 必要權限 {#required-permissions}

若要使用忠誠度挑戰，您需要Journey Optimizer中的適當許可權。 如果您無法存取此功能，請聯絡管理員。

## 存取忠誠度挑戰 {#access}

若要瞭解忠誠度挑戰：

1. 在Adobe Journey Optimizer的左側導覽功能表中選取&#x200B;**[!UICONTROL 忠誠度挑戰]**。

2. 「忠誠度挑戰」詳細目錄會以資訊顯示所有現有的挑戰，例如：
   * 挑戰名稱和說明
   * 狀態（草稿、即時、已停止等）
   * 挑戰型別（標準、條紋、循序）
   * 開始和結束日期
   * 上次修改日期

3. 選取&#x200B;**[!UICONTROL 建立挑戰]**&#x200B;以開始建立新的挑戰。

### 搜尋和篩選挑戰 {#search-filter}

使用搜尋和篩選功能快速尋找特定挑戰：

* **搜尋**：在搜尋欄位中輸入挑戰名稱或關鍵字
* **依狀態篩選**：草稿、已排程、即時、已完成、已停止或已封存
* **依型別篩選**：標準、連續或循序挑戰
* **依日期篩選**：特定日期範圍內的挑戰
* **依標籤篩選**：套用特定標籤的挑戰

## 後續步驟 {#next-steps}

現在您已瞭解忠誠度挑戰，瞭解如何創造您的第一個挑戰：

* [創造挑戰](create-challenges.md)
* [管理挑戰](manage-challenges.md)
