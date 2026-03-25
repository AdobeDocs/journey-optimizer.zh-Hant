---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 Journey Optimizer 的資料管理
description: 瞭解資料如何進入和離開Adobe Journey Optimizer，包括關鍵概念、設定步驟和護欄。
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: ec952f64508618fa14d6f0eb16534209baa1a505
workflow-type: tm+mt
source-wordcount: '2371'
ht-degree: 0%

---


# 開始使用資料管理 {#about-data}

資料是您透過[!DNL Adobe Journey Optimizer]傳送的每個歷程、決定和訊息的基礎。

本頁提供實用的起點，讓您瞭解：

* Journey Optimizer使用的核心資料建置區塊（結構描述、資料集、身分、設定檔）
* Journey Optimizer如何使用Adobe Experience Platform資料
* 建立歷程和行銷活動之前，您的團隊必須完成哪些資料設定步驟
* 接下來要前往何處取得詳細設定和最佳實務

本指南可與您的資料工程師、管理員和行銷人員一同使用，讓每個人都能分享資料如何流進/流出Journey Optimizer的共同圖片。

>[!TIP]
>Journey Optimizer資料管理的新手嗎？ 觀看[設定資料概觀教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}，瞭解適合初學者的實用結構描述、資料集和來源逐步解說。

## Journey Optimizer如何使用Adobe Experience Platform資料 {#aep-data}

[!DNL Adobe Journey Optimizer]建置於[!DNL Adobe Experience Platform]。 它不會維護獨立的資料存放區。 而是使用與其他Experience Cloud應用程式相同的資料基礎。

結構描述和資料集在Adobe Experience Platform中上線。 身分和[即時客戶設定檔](../audience/get-started-profiles.md)是由身分服務和設定檔服務所管理。 Journey Optimizer會從Adobe Experience Platform讀取設定檔和事件資料，以評估歷程條件、個人化訊息，並選取優惠方案。 它會將互動資料（例如傳送、開啟、點選和彈回事件，以及歷程步驟事件）寫入回Experience Platform資料集。 它也可以在執行階段查詢其他資料集，而無需將該資料複製到設定檔中。

>[!TIP]
>請將Adobe Experience Platform視為您的中央資料層，將Journey Optimizer視為使用該共用資料基礎來協調歷程和訊息的應用程式。

➡️ [進一步瞭解Journey Optimizer架構](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Journey Optimizer中的重要資料概念 {#key-concepts}

在Journey Optimizer中處理資料時，您會遇到數個相關概念。 下表提供快速概覽；接下來的章節將更詳細地說明每個概念。

| 概念 | 內容 | Journey Optimizer的主要用途 |
|---|---|---|
| XDM結構描述 | 表示、驗證及格式化您的資料的規則（從類別+欄位群組建置） | 模型設定檔屬性和行為事件 |
| 資料集 | 符合結構描述之資料的儲存表 | 保留設定檔、事件和系統產生的資料 |
| Source聯結器 | 將外部系統的資料串流或批次匯入AEP | 擷取CRM、Analytics和網頁資料 |
| 資料來源 | 在歷程中公開AEP或外部欄位 | Power Journey條件和訊息個人化 |
| 身分識別 | 唯一代表個別客戶的識別碼 | 跨管道拼接設定檔 |
| 查詢資料集 | 沒有設定檔儲存空間的AEP資料執行階段參考 | 使用即時參考資料擴充訊息 |

### 結構描述（XDM結構描述） {#schema}

結構是一組規則，可代表、驗證及格式化您的資料。 它由&#x200B;**類別** （定義基本行為：記錄或時間序列）和選用的&#x200B;**欄位群組** （新增特定欄位）組成。 結構描述是使用體驗資料模型(XDM)標準定義的，並在Adobe Experience Platform中上線。

XDM的存在是為了解決實際問題：相同的概念（客戶、購買、產品）在來源系統中的命名和結構不同。 XDM提供共用語言，可在單一定義下統一這些概念，無論資料來自何處。 這可讓Journey Optimizer同時以一致的方式處理CRM、網站、行動應用程式和Data Warehouse中的資料。

在Journey Optimizer中，您通常會使用客戶屬性的&#x200B;**XDM個人設定檔**&#x200B;結構描述（名稱、偏好設定、同意）以及行為事件的&#x200B;**XDM ExperienceEvent**&#x200B;結構描述（購買、頁面檢視、註冊）。

➡️ [進一步瞭解結構描述](get-started-schemas.md)

### 資料集 {#dataset}

資料集是適用於符合結構描述之資料的儲存和管理建構，可將其視為已定義一組欄和列的表格。 Journey Optimizer使用的所有資料都儲存在Adobe Experience Platform資料集中。 這些可以是設定檔資料集（有助於即時客戶設定檔）、事件資料集（儲存行為資料以供歷程和分析），或Journey Optimizer自動建立的系統資料集，以供追蹤、回饋和歷程步驟事件。

➡️ [進一步瞭解資料集](get-started-datasets.md)

### Source聯結器 {#source-connector}

來源聯結器（也稱為&#x200B;**來源**）可協助您將多個系統(例如Adobe Analytics、Adobe Experience Platform Web SDK、雲端儲存空間(S3、Azure Blob)或CRM資料庫)的資料擷取到Adobe Experience Platform。 除了原始擷取，聯結器還能使用Experience Platform服務來建構、標籤和增強資料，包括對應至XDM結構描述的欄位和資料治理標籤。

➡️ [進一步瞭解來源聯結器](../start/get-started-sources.md)

### 資料來源(Journey Optimizer) {#data-source}

Journey Optimizer中的資料來源會定義Adobe Experience Platform （或外部API）中的哪些欄位會顯示在歷程和訊息中。 在Journey Optimizer UI中設定的資料來源通常包括內建的Adobe Experience Platform資料來源（公開即時客戶個人檔案屬性和事件），以及在Journey Runtime呼叫的選用外部或自訂資料來源，以進行其他擴充。 它們用於歷程條件、自訂動作和訊息個人化。

➡️ [進一步瞭解資料來源](../datasource/about-data-sources.md)

>[!NOTE]
>[Adobe Experience Platform字彙表](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/glossary){target="_blank"}一般將「資料來源」定義為資料來源（CRM、行動應用程式等）。 在Journey Optimizer中，**資料來源**&#x200B;具有特定含義：控制歷程和訊息中公開哪些欄位的UI設定。

### 身分和即時客戶個人檔案 {#identity}

身分識別是可唯一代表個別客戶的識別碼，例如Cookie ID、裝置ID、電子郵件地址或CRM ID。 身分會被組織為名稱空間（電子郵件、ECID、CRMID），而同一人員的多個身分會連結到統一的身分圖表中。 即時客戶設定檔會使用該圖表，透過合併來自多個管道（包括線上、離線、CRM和第三方來源）的資料，維護每個個別客戶的整體檢視。

初學者的關鍵概念是&#x200B;**個人資料片段**&#x200B;模型。 每次客戶在特定裝置或頻道（您的網站、行動應用程式、商店）上與您的品牌互動時，該互動會記錄為設定檔片段：根據特定接觸點檢視該客戶的部分內容。 即時客戶設定檔會根據共用的身分值，持續將這些片段拼接在一起，建置完整、最新的設定檔。 Journey Optimizer會從此組合設定檔中讀取，以即時評估條件、選取優惠和個人化訊息。

➡️ [進一步瞭解Journey Optimizer中的身分識別](../audience/get-started-identity.md)

### 查詢資料集 {#lookup-dataset}

查詢資料集可讓Journey Optimizer在執行階段從Adobe Experience Platform資料集中擷取參考或異動資料，而不需將該資料儲存在即時客戶設定檔上。 這對於經常變更參考資料（價格、詳細目錄、商店時間）或在訊息時間需要但不屬於設定檔的交易式資料很有用。 Journey Optimizer會在歷程或訊息執行期間，根據索引鍵（例如產品ID）執行查詢。

➡️ [進一步瞭解查詢資料集](lookup-aep-data.md)

## 資料整備檢查清單 {#checklist}

在行銷人員開始建立歷程和行銷活動之前，您的組織應完成一組資料整備步驟。 這可確保Journey Optimizer在正確的時間以符合規範的方式使用正確的資料。

>[!NOTE]
>以下步驟涉及多個角色：資料工程師、管理員和行銷人員。 使用此檢查清單作為共用計畫來準備您的環境。 步驟1至4在Adobe Experience Platform中完成；步驟5至6在Journey Optimizer中設定。

### 1.定義您的身分策略 {#identity-strategy}

選擇客戶的主要身分（例如ECID、電子郵件或CRMID），並在Adobe Experience Platform Identity Service中設定對應的名稱空間。 請確定身分欄位出現在您的啟用設定檔的結構中，並驗證設定檔是否正確連結到身分圖表。

➡️ [進一步瞭解Journey Optimizer中的身分識別](../audience/get-started-identity.md)

### 2.設計設定檔和事件資料的結構描述 {#design-schemas}

建立&#x200B;**XDM個人設定檔**&#x200B;結構描述以擷取客戶屬性，例如名稱和聯絡資訊、偏好設定和興趣，以及生命週期階段或同意狀態。 建立&#x200B;**XDM ExperienceEvent**&#x200B;結構描述，以擷取行為與交易資料，例如Web與應用程式事件、購買和離線互動。 在適當的地方，將正確的欄位標示為身分和設定檔屬性。

➡️ [進一步瞭解結構描述](get-started-schemas.md)

### 3.建立已啟用設定檔的資料集 {#create-datasets}

在Adobe Experience Platform中，根據您的XDM結構描述建立資料集，並在任何應有助於即時客戶個人檔案的資料集上啟用個人檔案。 確認Journey Optimizer建立的系統產生資料集可在資料集工作區中看見。

➡️ [進一步瞭解資料集](get-started-datasets.md)

### 4.從您的來源擷取資料 {#ingest-data}

設定企業系統（例如Adobe Analytics、Adobe Experience Platform Web SDK或CRM和POS平台）的來源聯結器，並將傳入欄位對應至您的XDM結構描述。 驗證資料是否進入正確的資料集，並如預期顯示在即時客戶個人檔案中。

➡️ [進一步瞭解來源聯結器](../start/get-started-sources.md)

➡️ [教學課程：建立資料集並擷取資料](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

### 5.在Journey Optimizer中設定資料來源 {#configure-data-sources}

資料來源是Journey Optimizer專屬的概念：不是資料所在的位置，而是您宣告Journey Optimizer在歷程及訊息執行期間可讀取哪些欄位的位置。 在歷程評估諸如「客戶是否為忠誠會員？」等條件之前 或以名字個人化訊息，相關設定檔欄位必須透過資料來源設定公開。

Journey Optimizer包含內建[Adobe Experience Platform資料來源](../datasource/adobe-experience-platform-data-source.md)，可直接存取即時客戶個人檔案屬性。 這涵蓋了絕大部分的使用案例：讀取個人化的設定檔屬性，或檢查同意和偏好設定欄位。 您也可以設定[外部資料來源](../datasource/external-data-sources.md)在歷程執行階段呼叫第三方API，例如，擷取即時忠誠度分數、產品建議或未儲存在Adobe Experience Platform中的商店詳細目錄等級。

>[!NOTE]
>透過內建的Adobe Experience Platform資料來源直接存取體驗事件資料已過時，並逐步停用。 [了解更多](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}。

設定資料來源是一項管理工作，會為歷程作者和行銷人員解除鎖定完整資料層。 一旦透過資料來源公開欄位，就可在歷程條件產生器、訊息個人化編輯器及Offer Decisioning規則中使用 — 不需要在歷程建立時間進行任何額外的工程工作。

➡️ [進一步瞭解資料來源組態](../datasource/about-data-sources.md)

### 6.驗證追蹤、回饋和歷程資料集 {#verify-datasets}

確認在資料集工作區中可以使用Journey Optimizer系統產生的資料集。 執行測試歷程和行銷活動，然後使用查詢編輯器，以驗證是否記錄傳送、開啟、按一下和退回事件，以及是否正確擷取歷程步驟事件和狀態。 使用這些資料集進行持續監控、疑難排解和歷程最佳化。

➡️ [進一步瞭解Journey Optimizer中的查詢](get-started-queries.md)

## 護欄和資料設計考量事項 {#guardrails}

有些產品護欄和限制會影響您設計資料模型和歷程的方式。 請及早檢閱這些內容，以免稍後重新作業。

>[!IMPORTANT]
>如需最新資訊，請一律參閱[Journey Optimizer護欄和限制](../start/guardrails.md)頁面。 下列摘要會強調主要專案，但可能會隨著時間而改變。

### Journey Optimizer系統資料集和TTL {#datasets-ttl}

Journey Optimizer會建立數個系統產生的資料集，用於追蹤、回饋和歷程步驟事件。 截至2025年2月，存留時間(TTL)護欄正在其中部分資料集中推出，這可能會影響資料保留多久以進行分析和疑難排解。

➡️ [進一步瞭解資料集TTL護欄](datasets-ttl.md)

### 串流細分和Journey Optimizer事件 {#streaming-segmentation}

自2024年11月1日起，串流區段不再支援Journey Optimizer追蹤和意見資料集的傳送和開啟事件。 針對使用案例（例如頻率限定和疲勞管理），請使用[商業規則](../conflict-prioritization/rule-sets.md)，而不是根據傳送/開啟事件串流區段。

➡️ [進一步瞭解資料集](get-started-datasets.md)

### 資料集查詢與決策 {#lookup-guardrails}

資料集查詢適用於經常變更的屬性（庫存、定價、天氣）或不需要儲存在即時客戶個人檔案中的資料。 在設計查詢策略之前，請檢視相關檔案中的產品特定護欄，例如資料集大小限制和查詢上限。

➡️ [進一步瞭解查詢資料集](lookup-aep-data.md)

## 範例：為歡迎歷程準備資料 {#example}

下列範例說明此頁面上的概念如何在簡單案例中搭配運作。

1. 資料工程師會為客戶屬性（名稱、電子郵件、忠誠度等級、同意）建立[XDM個人設定檔結構描述](get-started-schemas.md)，並針對網頁註冊事件建立XDM ExperienceEvent結構描述。
1. [為每個結構描述建立已啟用設定檔的資料集](get-started-datasets.md)：一個用於CRM屬性，另一個用於註冊事件。
1. Web和行動團隊透過Adobe Experience Platform Web SDK串流註冊事件；CRM資料是透過[來源聯結器](../start/get-started-sources.md)擷取。
1. 管理員在Journey Optimizer中設定[Adobe Experience Platform資料來源](../datasource/adobe-experience-platform-data-source.md)，並公開`profile.person.name.firstName`、`profile.personalEmail.address`和`profile.loyaltyTier`等欄位。
1. 行銷人員[建立歡迎歷程](../building-journeys/journey-gs.md)，此歷程會聆聽註冊事件並使用這些設定檔屬性來[個人化歡迎電子郵件](../personalization/personalize.md)。 Journey Optimizer會將傳送和開啟事件寫入追蹤資料集，並將歷程進度記錄在歷程步驟事件資料集中。
1. 開發人員使用[查詢編輯器](get-started-queries.md)來驗證事件是否正確流動，並分析效能（開啟、點按、傳送時間）。 團隊會根據這些見解調整歷程和內容。

此流程說明結構描述、資料集、來源、資料來源和查詢如何在完整、入門友善的使用案例中搭配運作。

## 相關資源 {#related-resources}

* **[開始使用結構描述](get-started-schemas.md)** — 瞭解如何在Adobe Experience Platform中建立XDM結構描述、選擇正確的類別和欄位群組，並為您的設定檔屬性和行為事件建立模型。

* **[使用資料集](get-started-datasets.md)** — 瞭解如何建立已啟用設定檔的資料集和事件資料集、監視資料擷取，以及探索Journey Optimizer為追蹤、回饋和歷程步驟事件而自動建立的系統產生資料集。

* **[設定資料來源](../datasource/about-data-sources.md)** — 設定內建Adobe Experience Platform資料來源和選用外部資料來源的逐步指南，以公開歷程中的設定檔欄位和外部API回應。

* **[使用Adobe Experience Platform資料（查詢）](lookup-aep-data.md)** — 探索如何在執行階段利用AEP資料集的參考或異動資料擴充訊息，而不將資料儲存在即時客戶設定檔上。

* **[開始使用查詢](get-started-queries.md)** — 使用查詢服務來分析Journey Optimizer資料集、驗證事件是否正確流動，以及針對傳送、開啟、點按和退回資料建立報告查詢。

* **[開始使用設定檔](../audience/get-started-profiles.md)** — 探索Real-time Customer Profile在Journey Optimizer中的運作方式，以及如何在Platform UI中瀏覽、檢查及驗證個別客戶設定檔。

* **[設定資料概觀教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}** — Journey Optimizer中資料設定的入門友善影片逐步解說，涵蓋結構描述、資料集和來源，從頭到尾。

* **[建立資料集並擷取資料教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}** — 一個實作教學課程，說明如何在Adobe Experience Platform中建立資料集並使用來源聯結器擷取資料，提供您可以在自己的沙箱中遵循的逐步指示。
