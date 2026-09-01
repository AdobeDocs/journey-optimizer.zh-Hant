---
solution: Journey Optimizer
product: journey optimizer
title: CX Co-worker中的Journey Optimizer技能
description: 探索CX Co-worker提供的Adobe Journey Optimizer技能，其中包含深入的指引和範例提示。
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 2
source-git-commit: b56351bc92df6846dcdfd9065a170bb7771f8158
workflow-type: tm+mt
source-wordcount: '3341'
ht-degree: 6%

---


# CX Co-worker中的Journey Optimizer技能 {#ajo-coworker-skills}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;探索CX Co-worker中可用的Adobe Journey Optimizer技能（從建立和分析歷程到產生管道內容），瞭解每種技能的詳細指引、範例提示和最佳實務。

>[!ENDSHADEBOX]

## 概觀 {#overview}

CX Co-worker為Adobe Journey Optimizer帶來AI支援的功能。 [CX Co-worker](https://experienceleague.adobe.com/zh-hant/docs/cx-enterprise-coworker/content/home){target="_blank"}是Adobe的對話式體驗，可與您的商務應用程式整合，協助您更有效率地工作。

憑藉AI支援的技能，CX Co-worker可讓Journey Optimizer使用者使用自然語言介面來建立、分析和最佳化行銷歷程。 透過歷程技能，從業人員可以快速建立歷程、偵測並解決排程或對象衝突、分析績效和流失點，並識別表現最佳的歷程以復寫以供未來行銷活動。 它讓從業人員能夠進行資料導向式決策、改善客戶參與度並簡化歷程協調。

CX Co-worker提供各種管理歷程與忠誠度挑戰的技能：

**以歷程為主的技能：**

* **歷程建立**：透過自然語言提示建立及設定行銷歷程
* **頻道內容建立**：產生、編輯和管理使用AI支援的內容產生之歷程的頻道特定內容（電子郵件、推播、簡訊）
* **歷程分析**：分析歷程、偵測問題、發掘見解並最佳化歷程績效

**以忠誠度為主的技能：**

* **忠誠度挑戰管理**：使用自然語言提示建立和管理忠誠度挑戰
* **熟客方案 — 資料Insight技能**：使用自然語言查詢和分析熟客方案績效資料

<!--
feedback from Ivan: Need to remove Simulate skill from docs until Nico confirms the release timeline.

In addition, **Journey Simulation** is a Journey Optimizer feature that includes [Journey Simulate](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs), an in-product agentic skill, non conversational, with three capabilities: 

* Generating simulated users
* Generating event values
* Quick simulation
-->

## 歷程技能 {#journey-skills}

### 歷程建立 {#journey-create}

歷程建立可讓Journey Optimizer使用者使用自然語言介面建置和設定行銷歷程。 使用Journey Create，從業人員可以在對話式提示中描述其需求，以快速建立歷程。 此技能會逐步引導使用者瞭解建立歷程的不同選項，讓行銷人員聚焦於策略而非技術設定。

>[!AVAILABILITY]
>
>您需要下列許可權才能完整使用「歷程建立」功能：
>
>**管理歷程**：此許可權可讓您直接在CX Co-worker中建立新的歷程。
>
>**檢視歷程事件、資料來源及動作**：此許可權可確保CX同事能夠搜尋歷程事件和自訂動作。
>
>**檢視區段**：此許可權可確保CX Co-worker在建立歷程時可搜尋對象區段。
>
>**管理區段**：此許可權可讓您直接在CX Co-worker中建立新對象。

#### 主要使用案例

Journey Create提供可加快行銷執行進度的功能：

1. **事件觸發的歷程建立**

   * 建立根據特定客戶事件啟動的歷程。
   * 即時設計客戶動作的自動化回應。
   * 根據客戶行為建立個人化的通訊流程。

   **商店造訪歷程：**
   「建立歷程，從使用者進入我的商店位置時開始。 傳送推播通知以歡迎使用者存取存放區。 請等待2天，然後檢視使用者是否有有效的電子郵件地址。 如果使用者擁有有效的電子郵件地址，請傳送電子郵件調查以詢問其商店體驗。 如果使用者沒有有效的電子郵件地址，請傳送推播通知以提示進行註冊。」

   **購買後的歷程：**
   「建立客戶線上購買時開始的歷程。 傳送推播通知以感謝他們的購買。 接下來，檢查他們是否為忠誠會員。 如果使用者是忠誠度獎勵會員，請傳送第二個具有10%折扣代碼的推播通知。 如果使用者不是忠誠獎勵成員，請傳送推播邀請他們註冊忠誠計畫。 請等待2天，然後傳送後續推播訊息，其中包含有關其購買體驗的調查。」

   **事件型促銷活動：**
   「建立遊戲分數達到50時觸發的歷程。 傳送SMS訊息給忠誠獎勵會員，稱他們有資格從合作夥伴贊助者處免費分得披薩。」

1. **以對象為目標的歷程建立**

   * 建立以特定受眾區段為目標的歷程。
   * 設計具有策略性時機的多步驟通訊順序。

   **季節性行銷活動：**
   「我想建立以日間徒步旅行者受眾為目標的歷程。 我想要傳送電子郵件，提醒此對象我即將到來的假期銷售，其中包括各種遠足必需品。 請在傳送第一封電子郵件後等待3天，然後傳送第二封電子郵件（附有15%的優惠券且免運費）。 等候1週，然後傳送第3封電子郵件訊息，顯示我們的新睡袋和帳篷系列。 排程歷程於12/20開始。」

   **忠誠度獎勵：**
   「為SUV車主建立忠誠度感謝歷程，包括含免費洗車優惠的感謝推播通知，以及若第一則通知未在1天內互動，則提供後續推播通知提醒。」

1. **商務事件觸發的歷程建立**

   * 建立根據特定業務事件啟用的歷程，並鎖定指定的對象（例如產品補貨或遊戲分數變更）
   * 業務狀況變更時及時觸發內容感知訊息。

1. **對象資格歷程建立**

   * 建立歷程，當設定檔進入或退出對象區段定義時啟動。
   * 自動化登入和退出訊息，以支援上線、保留和贏回目標。

1. **條件式歷程流程**

   * 根據客戶屬性建立決策分支。
   * 根據客戶偏好設計分割路徑。

1. **從影像建立歷程**

   * 將參考影像上傳到同事中，並要求使用影像作為參考建立歷程
   * 歷程建立技能將從您的參考影像中擷取可編輯的提示

透過這項技能，自然語言需求將轉換為結構化的歷程設定。

#### 範圍技能

Journey Create支援下列功能：

* **自然語言歷程建立**：可讓使用者以對話式語言描述歷程流程。
* **以事件和受眾為基礎的歷程**：同時支援以觸發器和排程的歷程型別，以及商業事件和受眾資格。
* **條件式邏輯**：根據客戶屬性處理決定分割和分支。
* **多頻道傳訊**：支援推播通知、電子郵件和簡訊頻道。
* **歷程排程**：設定排程歷程的開始日期和時間。

#### 超出範圍技能

目前不支援以下功能：

* 進階歷程分析
* Cross-journey orchestration
* A/B測試設定
* InAudience運算式產生
* 資料集查詢節點
* 波段傳送設定
* 排程週期選項
* 對象的名稱空間選擇
* 自訂動作欄位對應
* 複雜的資料轉換

#### 提示最佳實務

若要讓「歷程建立」獲得最大成效，請遵循下列最佳實務：

1. **明確**：提供歷程目標、目標對象和所需動作的明確詳細資訊。 包括有關頻道、時機和條件的資訊。
1. **指定時間**：清楚指出動作之間的等待期間以及歷程應該開始的時間。
1. **定義條件**：使用條件邏輯時，請說明每個分支路徑的條件。
1. **包含頻道**：指定您要使用哪些通訊頻道（推播、電子郵件、簡訊）。
1. **提及排程**：針對排程的歷程，提供所要的開始日期和時間。
1. **自訂動作**：如果您在工作流程中使用自訂動作，您必須指定您使用自訂動作以及自訂動作的確切名稱。 範例：
當使用者進入我的存放區位置時，會使用自訂動作ExternalPush傳送歡迎訊息。 等候2天，然後使用自訂動作ExternalEmail傳送後續訊息，連同其瀏覽時的調查。
1. **驗證運算式**：請務必檢查並驗證Journey Skills建立的任何運算式，以確保使用正確的欄位和值。

#### 設定最佳實務

* **定義明確的目標**：在建立歷程之前，請先建立明確的目標（改善保留率、促進轉換、提高參與度）。
* **準備對象**：確定您的目標對象已建立且已正確分段。
* **規劃訊息內容**：在建立歷程之前，先定義您的訊息策略。
* **考慮客戶體驗**：設計尊重客戶偏好並避免過度溝通的歷程流程。

### 頻道內容建立 {#channel-content-create}

<!--Ivan : Need to speak with Amar on new options for content generation as this skill has changed. -->

>[!AVAILABILITY]
>
>此功能以有限可用性提供給所有客戶。 請聯絡您的 Adobe 代表以取得存取權。

管道內容建立可讓Journey Optimizer使用者使用AI支援的內容產生功能，產生、編輯和管理歷程的管道特定內容。

#### 主要使用案例

1. **頻道特定內容產生**：使用自然語言提示產生電子郵件、推播通知、簡訊和其他頻道的內容。

   「產生歡迎歷程的電子郵件內容。 使用友善語調為新客戶建立歡迎電子郵件，並包含10%折扣優惠。」

   「產生商店造訪歷程的推播通知。 建立歡迎訊息，鼓勵客戶登入並接收特別優惠。」

   「為我事件觸發的歷程產生SMS內容。 建立簡訊，通知客戶使用call-to-action進行閃購。」

1. **以範本為基礎的內容建立**：瀏覽並選取具有預覽功能的可用範本。

   「為我季節性行銷活動歷程顯示可用的電子郵件範本。」

   「為我的電子郵件選取設計新穎、簡潔的範本。」

1. **多頻道內容管理**：產生並管理相同歷程工作流程中多個頻道的內容。

1. **內文中內容編輯**：在「內容Designer」中開啟產生的內容以進行編輯和細分。

   「在『內容Designer』中開啟電子郵件內容，以便我可以自訂設計。」

1. **內容細分與反複專案**：使用「重新產生」動作重新產生具有不同色調或樣式的內容。

   「以更輕鬆的語調重新產生推播通知內容。」

   「更新電子郵件內容，加入促銷代碼。」

1. **歷程畫布整合**：從詳細目錄選取歷程並檢視關聯的管道。

#### 範圍技能

頻道內容建立支援下列功能：

* **AI支援的內容產生**：使用自然語言提示產生電子郵件、推播、簡訊和其他管道的內容。
* **範本管理**：瀏覽並選取具有預覽功能的可用範本。
* **In-context editing**：在Content Designer中開啟產生的內容以進行編輯和細分。
* **內容重新產生**：使用「重新產生」動作重新產生具有不同色調、樣式或傳訊的內容。
* **多頻道支援**：產生並管理相同歷程工作流程中多個頻道的內容。
* **歷程詳細目錄存取**：從詳細目錄選取歷程並檢視關聯的管道。

#### 超出範圍技能

目前不支援以下功能：

* **品牌一致性和內容品質檢查**
* **將內容節點直接插入歷程畫布**
* **範本匯入**

#### 提示最佳實務

1. **明確**：提供內容型別、語調、目標對象和關鍵訊息的明確詳細資訊。
1. **指定頻道**：清楚標示您正在建立內容的頻道（電子郵件、推播、簡訊）。
1. **定義音調**：指定所要的音調（友善、正式、隨意、緊急）。
1. **重複及調整**：使用重新產生動作來調整內容，直到符合您的需求為止。

### 歷程分析 {#journey-analyze}

歷程技能可讓Journey Optimizer使用者使用自然語言介面來分析和最佳化歷程。 透過歷程技能，從業人員可以快速識別並解決排程和/或對象衝突，偵測歷程中的使用者放棄點並提供見解或建議。 它讓從業人員能夠進行資料導向式決策、改善客戶參與度並簡化歷程協調。

>[!AVAILABILITY]
>
>所有可存取CX Co-worker的客戶皆可使用歷程技巧。 不過，您需要下列許可權才能完整使用「歷程技能」功能：
>
>**檢視歷程**：此許可權可讓您直接在CX Co-worker中檢視歷程的深入分析。
>
>**管理歷程**：此許可權可讓您直接在CX Co-worker中建立新的歷程。
>
>**檢視區段**：此許可權可讓您直接在CX Co-worker中檢視對象的深入分析。
>
>**管理區段**：此許可權可讓您直接在CX Co-worker中建立新對象。

#### 主要使用案例

Journey Analyze提供一系列可用來最佳化行銷工作的功能：

1. **歷程流失分析**

   * 確認客戶在歷程中哪個階段流失及其原因。
   * 偵測會導致中斷參與的客戶行為模式。
   * 運用洞察來改進歷程設計及提高保留率。

   範例提示：
   * 「我想針對7月4日的行銷活動歷程依節點分析流失。」
   * 「對7月4日的行銷活動歷程執行流失分析。」
   * 「在7月4日行銷活動的歷程中，設定檔損失是多少？」
   * 「顯示使用者在7月4日的行銷活動之旅中的目的地。」

1. **歷程客群重疊分析**

   * 分析多個歷程中的客群重疊情形。
   * 防止因過度鎖定目標而導致客群疲勞。
   * 將細分最佳化，確保參與情形達到平衡。

   範例提示：
   * 「超過X個歷程會使用哪些對象？」
   * 「使用[對象名稱]對象列出所有歷程。」
   * 「顯示歷程[歷程名稱]的對象重疊衝突。」
   * 「顯示歷程[歷程名稱]和其他歷程的重疊對象。」

1. **歷程排程重疊分析**

   * 偵測針對相同客群的已排程歷程之間時機衝突的狀況。
   * 避免過度通訊並提升排程效率。
   * 確保歷程在最佳時間點進行，發揮最大的客群影響力。

   範例提示：
   * 「歷程[歷程名稱]是否有任何排程衝突？」
   * 「檢查與歷程[歷程名稱]相關的排程衝突。」
   * 「醒目提示在歷程[歷程名稱]和即時歷程之間的排程重疊。」
   * 「歷程[歷程名稱]是否與其他歷程發生衝突？」

1. **運作洞察**

   * 提示型歷程深入分析 — 顯示歷程的營運深入分析，即「顯示所有即時歷程」。

   範例提示：
   * 「[歷程名稱]何時發佈？」
   * 「[歷程名稱]何時停止？」
   * 「列出目前處於測試模式的所有歷程」
   * 「我有多少個即時歷程？」
   * 「提供所有已排程的週期性歷程及其預期執行時間的清單。」

1. **歷程自訂動作錯誤分析**

   * 識別歷程中的自訂動作失敗或錯誤率飆升的時間。
   * 在失敗升級為更廣泛的歷程中斷之前診斷根本原因。
   * 使用特定的補救步驟，快速還原自訂動作的可靠性。

   範例提示：
   * 「為什麼自訂動作在歷程[歷程名稱]中失敗？」
   * 「歷程[歷程名稱]中自訂動作[自訂動作名稱]的錯誤率為何？」
   * 「顯示歷程[歷程名稱]中自訂動作失敗的根本原因。」
   * 「目前是否有任何影響歷程[歷程名稱]的自訂動作錯誤？」

#### 範圍技能

Journey Analyze支援下列功能：

* **反應式查詢**：使用者能夠詢問關於歷程績效、客群使用情形，以及排程衝突的具體問題。
* **與其他技能整合**：與Audience和Data Insights功能共同作業，以進行更深入的分析。
* **回應結構**：推理（說明邏輯）、分析摘要（強調關鍵點）、問題詳細資訊（說明問題）以及建議（建議後續步驟）。
* **自訂動作錯誤分析**：偵測並診斷歷程中的自訂動作失敗和錯誤尖峰。

#### 超出範圍技能

目前不支援以下功能：

* **自動建立歷程**
* **即時異常偵測**
* **管道重疊**
* **歷程進入分析**
* **技術問題分析**
* **疲勞分析**

#### 提示最佳實務

若要讓Journey Analytics獲得最大成效，請遵循下列最佳實務：

1. **具體**：使用清楚且簡潔的提示獲得指定目標的洞察。 例如，與其問「我的歷程為何？」，改為指定「列出上個月建立的所有歷程」。
1. **結合見解**：整合受眾的見解和資料見解功能，以整體檢視歷程績效。
1. **反覆改善**：使用流失分析和重疊分析來反覆改善歷程設計與排程。

#### 設定最佳實務

* **定義明確目標**：在分析歷程之前，先設定明確的目標 (例如提高保留率、提高轉換率)。
* **定期監視**：安排定期檢查歷程績效，以發現趨勢和異常。
* **細分最佳化**：確保客群細分維持平衡，避免疲勞並實現最高參與度。

## 熟客技能 {#loyalty-skills}

>[!AVAILABILITY]
>
>符合資格的組織可在CX Co-worker中獲得忠誠度技能。 擁有忠誠度授權的客戶可以存取這些忠誠度技能，即使他們沒有額外的CX Co-worker授權亦然。

熟客技能可讓熟客管理員和分析人員使用自然語言建立、管理和分析熟客方案。 透過這些AI支援的技能，您可以快速設計引人入勝的忠誠度挑戰、追蹤績效量度，並做出資料導向式決策，以將成員參與度和計畫獲利能力最佳化。 無論您是要提出新的挑戰，或是要分析熟客方案趨勢，熟客技能都能簡化整個熟客方案管理工作流程。

### 忠誠度挑戰管理 {#loyalty-challenge-management}

忠誠度挑戰管理可讓Journey Optimizer使用者使用自然語言提示來建立和管理CX Co-worker中的忠誠度挑戰。 如需建立、設定和管理忠誠度挑戰的完整檔案，包括詳細的設定指示，請參閱[忠誠度挑戰指南](../loyalty-challenges/get-started.md)。

#### 主要使用案例

1. **多步驟上線挑戰**

   針對新註冊的客戶，建立名為「新帳戶Kickstart」的挑戰，要求他們依序完成以下步驟：開啟支票帳戶、至少以$500的資金支付帳戶，以及下載行動應用程式。 完成所有步驟後，將以5,000點獎金獎勵他們。 請在9月1日到10月31日東部時區之間執行。」

1. **累積活動臨界值挑戰**

   「為持卡人建立名為」Spent &amp; Earn Summer「的挑戰，其會員在第三季花費1,500美元於信用卡時，可獲得$50的結算表信用。 7月1日開始，東部時區。」

1. **頻率連續挑戰**

   針對進階會員建立名為「常旅客短跑」的挑戰，其連續兩個月每月需要3次航班。 以層級狀態擴充功能和10,000額外英里獎勵完成工作。 從下個月的第一個，太平洋時區開始。」

1. **單一合格動作挑戰**

   設定名為「無紙化」的挑戰，獎勵後付費訂閱者在註冊自動轉帳後500個額外積分，並在30天內切換為無紙化帳單。 在下個月的第一個月開始，中部時區。」

1. **參與/消耗目標挑戰**

   針對八月期間要求成員完成至少3個不同類別的5個活動的成員，建立名為「Explorer Badge」的挑戰。 完成時給予1,000點和「總管」徽章的獎勵。 從8月1日山區時區開始。」

1. **每日動作挑戰**

   「幫我為抹茶愛好者建立一個挑戰，要求他們本週每天到店裡購買抹茶飲料。 如果他們完成挑戰，應該獲得額外200分的獎勵。 將其稱為「Mad about Matcha」，使用SKU matcha-001，在下週星期一開始進行，東部時區。

#### 範圍技能

忠誠度挑戰管理支援下列功能：

* **挑戰建立**：從自然語言（對象、動作條件、時間、獎勵、命名）建立挑戰設定。
* **挑戰更新**：透過反複提示修改挑戰詳細資料。
* **挑戰發佈**：直接從交談發佈支援的挑戰設定。
* **挑戰內容可見性**：反複處理時擷取並檢閱挑戰資訊。

#### 超出範圍技能

目前不支援以下功能：

* 挑戰刪除
* 熟客方案深入分析和建議技能
* 針對所有情況下的挑戰訊息提供完整的內容製作自動化

#### 提示最佳實務

1. **將其命名為**：在引號中加上清楚、難忘的標題。
1. **指定對象**：符合資格者（例如，所有成員、階層、區段、新註冊者、持卡人、訂閱者）。
1. **定義動作和數量**：成員必須做什麼，以及計為完成的頻率、臨界值或順序。
1. **設定時間範圍**：開始日期（若為固定期間，則為結束日期）加上時區。
1. **說明獎勵**：積分、里程、宣告積分、狀態延期、憑單，或完成時授予的額外津貼。
1. **參考資格確認事件**：指向挑戰追蹤的特定SKU、產品、帳戶動作或參與事件。

### 熟客代理 — 資料Insight {#loyalty-data-insight}

熟客代理 — 資料Insight技能可讓Journey Optimizer使用者使用自然語言來分析和查詢熟客方案績效資料。 此技能可提供忠誠度點數、成員層級、贖回和收入量度的深入分析，讓忠誠度管理員和分析師可針對其忠誠度計畫進行資料導向式決策。

主要使用案例：

1. **忠誠度點數分析**

   * 分析特定期間授予、獲得和兌換的熟客點數。
   * 比較不同熟客層級和方案之間的熟客點活動。
   * 依成員區段追蹤熟客點數餘額。

   範例提示：
   * 「2026年8月期間，共授予多少忠誠點數？」
   * 「2026年8月期間，會員在每個忠誠度等級中獲得多少忠誠度積分？」
   * 「向我顯示2026年8月期間，以會員忠誠度狀態（而非忠誠度等級）兌換的忠誠度總積分。」
   * 「顯示2026年8月期間依忠誠度等級劃分的忠誠度積分總餘額。」

1. **收入和折扣分析**

   * 依層級和方案分析訂單收入和熟客折扣趨勢。
   * 比較熟客方案與時段之間的收入產生。
   * 追蹤折扣對收入和成員參與的影響。

   範例提示：
   * 「2026年8月每個忠誠度等級的訂單收入總計是多少？」
   * 「2026年8月期間，各忠誠度等級適用了多少忠誠度折扣？」
   * 「顯示2026年8月期間依熟客方案劃分的熟客方案總折扣。」
   * 「2026年8月期間，每個忠誠計畫所產生的訂單收入總計是多少？」

1. **方案效能深入分析**

   * 分析每日、每週和每月的方案效能量度。
   * 比較不同產品類別和折扣策略的績效。
   * 識別成員參與和兌換模式的趨勢。

   範例提示：
   * 「顯示2026年8月期間依日劃分的熟客方案總收入。」
   * 「顯示2026年8月期間依產品類別劃分的熟客折扣總數。」
   * 「顯示2026年第三季的熟客方案績效報告。」

<!--
Feedback from Ivan: Journey simulate is not ready as a skill

## Journey Simulate: Use Cases, Agentic Skills and User Guide

## Overview

>[!BEGINSHADEBOX]

Journey Simulation is available to all Journey Optimizer customers. Journey Simulate, the in-product agentic skill within Journey Simulation, is available to customers that are a part of the Agent Orchestrator Explorer program and requires at least one of the following permissions:

* **Simulate journeys**: Run simulation workflows from the journey canvas.

* **Publish journeys**: Publish journeys, including flows that use simulation before go-live.

* **Approve and Publish journeys**: Approve and publish journeys when your organization uses approval workflows.

To use AI in **[!UICONTROL Simulation]** (**[!UICONTROL Quick simulation]**, generating simulated users with AI, **[!UICONTROL Generate event values]**), users require **[!UICONTROL Generate Content]** permission from the **[!UICONTROL AI Assistant]** capability. 

[Learn more about permissions](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/administration/permissions).

>[!ENDSHADEBOX]

Journey Simulation is a Journey Optimizer feature that enables Journey Optimizer users to safely test and validate marketing journeys before activation. Within Journey Simulation, Journey Simulate is an in-product agentic skill, not a conversational one, that automates and assists the testing process directly from the journey canvas.

Journey Simulate includes three capabilities:

* Generating simulated users
* Generating event values
* Quick simulation. 

Together, they bridge the gap between journey creation and activation, building confidence in journey logic and reducing the risk of post-launch errors.

## Use cases

### Key use cases for Journey Simulate

Journey Simulate offers three capabilities that can be leveraged to reduce testing time and improve journey quality before go-live:

**Generating simulated users**

* Generate simulated users automatically based on journey paths and required attributes.
* Create simulated users that cover all branches and conditions in a journey, including execution addresses (email, push, SMS).
* Update simulated user attributes on demand to refine test scenarios.
* Ensure all journey branches are covered by assigning the right simulated user to each path.

**Generating event values**

* Generate values for events used in a journey to drive test execution through specific paths.
* Define event attribute values that trigger the desired conditions and branches during simulation.

**Quick simulation**

* Start journey simulation and trigger test executions for all simulated users needed to test all paths of a journey, in a single interaction.
* Visualize how simulated users flow through a journey, step by step, including branching paths and conditional logic.
* Identify which simulated user flows through which path, and why, with detailed node-by-node traversal.
* Review simulation reporting at the end of a run in the Journey Optimizer UI to validate outcomes before activation.

## In scope skills and limitations

### **In scope**

The following capabilities are supported by the Journey Simulation feature:

* **Simulated user management**: View, edit, and update simulated user attributes, including execution addresses and personalization data.
* **Simulation control**: Start and stop journey simulation directly through the Journey Simulation in-product experience.
* **Test execution**: Trigger test executions for one or multiple simulated users.
* **Journey flow visualization**: View step-by-step traversal of simulated users through journey nodes, including branching, splits, and user status.
* **Simulation reporting**: View reporting at the end of a simulation run in the Journey Optimizer UI.
* **Multi-user testing**: Run and visualize tests for multiple simulated users simultaneously, covering all journey branches.

In addition to this, the following capabilities are supported by the Journey Simulate skill:

* **Simulated user generation**: Create simulated users based on journey paths, existing test profiles, or specified attributes.
* **Event value generation**: Generate and assign event attribute values to drive test execution through specific journey paths.
* **Quick simulation**: Run a full end-to-end simulation with minimal intervention. The skill automatically generates simulated users, event values, and pre-filled test settings, then executes the journey and surfaces results for review.

### **Limitations**

Simulation may not support every activity, channel, or integration that Test mode or a live journey supports, and behavior may change as the capability matures.

➡️ Learn more about [Simulation limitations](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/create-journey/simulate-journey/simulate-journey-gs#limitations) in the Journey Optimizer documentation.

-->
