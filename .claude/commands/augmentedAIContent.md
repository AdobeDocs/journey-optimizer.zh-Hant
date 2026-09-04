---
source-git-commit: 341538e14ef7de012cce89561727bdecb44d8183
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 0%

---
# augmentedAIContent

為Journey Optimizer檔案存放庫中的一或多個Markdown頁面產生自動建立的&#x200B;**AI知識參考**&#x200B;摺疊式功能表，並將其儲存為&#x200B;**非當地語系化包含**，因此不會翻譯。

## 目標存放庫

`help/using/` （相對於存放庫根目錄）

## 摺疊式功能表語法(Experience League)

```
+++ AI Knowledge Reference

Content here — any standard markdown is valid.

+++
```

**規則：**

- `+++ AI Knowledge Reference`開啟收合式選單（`+++`後一個空格）；只有`+++`在一行中關閉它
- 開頭`+++`之前和結尾`+++`之後的空白行
- 標題一律為`AI Knowledge Reference`

## 包含語法(Experience League)

```
{{$include /help/_includes/do-not-localize/<folder>/<include-file>.md}}
```

透過`{{$include}}`從`help/_includes/do-not-localize/`提取的內容是&#x200B;**從本地化排除** — 這是區塊未翻譯的方式。

---

## 工作流程

### 步驟1 — 詢問目標

詢問使用者：
> 您要擴充哪個檔案或資料夾？
> - 單一檔案：相對於存放庫根目錄的路徑（例如`help/using/email/get-started-email.md`）
> - 資料夾：所有`.md`檔案遞回（例如`help/using/email`）
> - 檔案/資料夾清單

如果提供了資料夾，請列出找到的`.md`個檔案，並在處理前進行確認。

### 步驟2 — 針對每個檔案：讀取和產生

1. **完整讀取檔案**。
2. **瞭解頁面主題** — 它涵蓋什麼功能、概念或工作？
3. **使用以下內容產生規則產生區塊內容**。
4. **執行產生後驗證檢查清單** （請參閱下文） — 請勿略過。
5. **檢查** AI知識參考區塊是否已經存在 — 內嵌（`+++ AI Knowledge Reference`接近結尾）或已經外部化（`{{$include /help/_includes/do-not-localize/.../ai-augmented-...}}`行）。 如果有，詢問使用者：取代或略過？ 取代時，覆寫包含檔案（如果區塊仍內嵌，請移除內嵌區塊並改為新增包含行）。

### 步驟3 — 驗證針對頁面本文的所有宣告

在寫入區塊之前，請透過宣告重新讀取產生的內容宣告。 此步驟是&#x200B;**必要步驟，即使檔案較短，也不可略過**。 請先修正任何故障，再繼續執行步驟4。

**術語和標籤**

- [ ]區塊中的每個字詞、標籤和UI名稱都會顯示在頁面本文中 — 不是從其他頁面匯入或根據一般產品知識推斷而來
- [ ]未列出同義字，除非兩個表單都出現在頁面上
- [ ]每個「請勿混淆」專案僅參考本頁提及的概念

**護欄和限制**

- [ ]每個數值都與頁面本文完全相符
- [ ]只有當頁面本文使用該單字或明確表示系統強制使用它（例如「不能超過」、「允許的最大值……」、「僅……支援」）時，限制才稱為&#x200B;**hard**
- [ ]只有當頁面本文使用該字或同等字詞時，限制才稱為&#x200B;**建議** （「為獲得最佳效能」，「建議使用」）
- [ ]如果頁面本文未提供限定詞，區塊會提供none — 不要發明一個
- [ ]來源頁面沒有內文註解（例如：「此頁面上未說明任何特定數字」）

**字彙表定義**

- [ ]沒有定義包含頁面本文中缺少的技術細節
- [ ]沒有專案會使用檔案集中其他頁面的資訊進行詳細說明

**常見問題解答**

- [ ]每個特定詳細資訊（UI提供、按鈕名稱、欄位名稱、步驟順序）都列在頁面本文中 — 未從其他頁面推斷或匯入
- [ ]沒有回應會引入頁面本文未處理的資訊

**更正規則：**&#x200B;如果任何檢查失敗，請在寫入區塊&#x200B;**之前更正內容**。 在步驟5報表中記錄每次校正。

---

### 步驟4 — 將區塊寫入「不要本地化」包含，然後包含它

產生的區塊必須&#x200B;**未本地化**，因此它不會內嵌寫入頁面中。 而是位在`help/_includes/do-not-localize/`下的個別包含檔案中，該檔案會排除在翻譯之外，頁面會將其與`{{$include}}`拉入。 （這是DOCAC-15581慣例）。

**a。 從`help/using/`底下相對於其最上層區段資料夾的頁面路徑衍生包含檔案名稱**：移除`.md`副檔名，以`-`取代任何剩餘的`/`，以`ai-augmented-`加上前置詞。 此平面化可讓平面包含目錄不受撞擊。

範例（區段`building-journeys`）：

| 頁面 | 包含檔案 |
|---|---|
| `help/using/building-journeys/end-journey.md` | `ai-augmented-end-journey.md` |
| `help/using/building-journeys/expression/journey-properties.md` | `ai-augmented-expression-journey-properties.md` |

**b。 在`help/_includes/do-not-localize/<section-folder>/<include-file>`寫入包含檔案** （如果沒有，請建立`<section-folder>`子目錄 — 每個頂層AJO區段一個子資料夾，例如`building-journeys/`、`email/`）。 完全使用此結構 — `title` frontmatter、一個`# AI Knowledge Reference`標題、以下&#x200B;**完整範本**&#x200B;中的完整摺疊式功能表，然後是同步處理註解：

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

[complete "+++ AI Knowledge Reference" accordion from the Full template below]

<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of the including page's body, excluding the {{$include}} line] -->
```

**c。 新增包含呼叫**&#x200B;作為頁面的最後一行，前面加上空白行。 請勿修改任何其他頁面內容：

```
{{$include /help/_includes/do-not-localize/<section-folder>/<include-file>}}
```

同步註解仍會啟用漂移偵測：來源雜湊會在包含頁面的本文上計算，以便日後的工具和撰寫者能分辨頁面何時從區塊漂移。 每頁變更兩個檔案： **包含檔案** （已建立）和&#x200B;**頁面** （已新增一`{{$include}}`行）。

### 步驟5 — 報表

- 已修改的檔案✓ （包括已建立的檔案+頁面的`{{$include}}`行）
- 略過的檔案+原因（已經有區塊/空白/索引頁面）
- 在步驟2期間出現的任何驗證警告

---

## 內容產生規則

分析頁面，並在摺疊式功能表內依順序&#x200B;**產生低於**&#x200B;的部分。 如果無法擷取某個區段的有意義的內容，請完全略過該區段。

### 固定開啟 — 逐字，不修改

每個「AI知識參考」摺疊式功能表都必須以這個確切的區塊開頭。 照原樣複製；請勿轉述、壓縮或重新排序：

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

以下頁面特定區段緊接在這兩個段落之後，仍位於相同的摺疊式功能表內。 (整個摺疊式功能表會根據「步驟4」（而不是內嵌在頁面中）寫入「不要本地化」(do-not-localize)包含檔案。)

### &#x200B;1. TL；DR

一句話：此頁面會教導或啟用哪些功能？

```
* **TL;DR:** [one sentence]
```

### &#x200B;2. 意圖

閱讀本頁面後，使用者可完成3至6件事。

```
**Intents:**

* [action]
* [action]
```

### &#x200B;3. 字彙表

此頁面/功能的特定重要辭彙，含簡短定義。 標幟產品特定詞語。

```
**Glossary:**

* **[Term]**: [definition] *(product-specific)*
```

僅包含與此頁面相關的字詞。 請勿使用一般行銷詞語填入。

**驗證模式精確度規則 — 強制：**
如果頁面涵蓋任何形式的測試、預覽或模擬執行，您必須區分頁面實際描述的所有模式。 請勿將不同的模式摺疊為單一速記專案：
- **模擬** — 呈現訊息內容而不傳送；使用真實設定檔
- **測試模式** — 僅傳送至指定的測試設定檔；使用持續性AEP測試設定檔（非合成或偽裝設定檔）
- **練習** — 執行完整的歷程邏輯而不啟動動作；使用真實的對象資料

僅包含頁面中存在的模式。 從頁面本文複製產品精確的辭彙 — 請勿將「合成設定檔」、「假資料」或「沒有真實資料」取代任何這些專案。

### &#x200B;4. 護欄

頁面上提及的限制、先決條件、許可權或限制。

```
**Guardrails:**

* [guardrail]
```

**護欄精確度規則 — 必要：**

- **將每個數值限制**&#x200B;限定為建議或強制。 範例：「每則訊息最多10個資料集查閱（硬限制）」而非「最多10個資料集查閱」。
- **將每個輸送量或速率圖**&#x200B;限定為它的範圍。 範例：「150,000則訊息/小時TPS上限（每個沙箱）」不是「150,000則訊息/小時上限」。
- **在加入頁面本文之前，交叉檢查每個護欄**。 如果頁面顯示10，而區塊顯示5，則區塊錯誤。 頁面本文是權威的。
- **請勿推斷頁面上未列出的護欄**。 如果限制存在，但頁面未指出它，請忽略它。

### &#x200B;5. 術語

正式名稱、縮寫、接受的變體、同義字、消除歧義。 主要用於AI管道標準化。

```
**Terminology:**

* Canonical name: [name] — Acronym: [acronym] — variants: [list]
* Synonyms: "[term A]" = "[term B]"
* Do not confuse: "[term]" ≠ "[other term]"
```

**狀態與生命週期精確度規則：**
當頁面描述生命週期（歷程狀態、訊息狀態、行銷活動狀態等）時，請從頁面本文複製確切的狀態標籤。 請勿轉述。 使用「請勿混淆」專案，消除共用根字但有不同含義的狀態。 範例：

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. 常見問題集

使用者可能會問3到6個問題，並提供簡短答案。

```
**FAQ:**

* **Q: [question]** — [short answer]
```

**常見問題集精確度規則：**
答案必須使用與頁面主體相同的動詞和名詞選擇。 請勿引入「回覆」、「重設」或「回覆」等動詞，除非頁面使用這些動詞。 如果轉變結束工作階段（例如，退出測試模式將歷程傳回其先前的狀態），準確地說 — 不要說「歷程還原為草稿」。

### 不要包含的內容

- 請&#x200B;**不**&#x200B;重寫或摘要內文內容（內容已位於頁面中）
- 請&#x200B;**不**&#x200B;包含逐步指示
- 請&#x200B;**不**&#x200B;該頁面不支援的發明內容
- 請&#x200B;**不**&#x200B;使用下列不精確的辭彙，除非它們一字不差地出現在頁面本文中：「合成」、「假資料」、「沒有真實資料」、「回覆」、「回覆」（描述產品狀態轉換時）

---

## 產生後驗證檢查清單

在寫入包含檔案之前，請在每個區塊上執行此檢查清單。 在繼續之前標籤使用者的任何失敗。

### 護欄檢查

- [ ]區塊中的每個數值都是逐字存在，或是可從頁面本文衍生
- [ ]每個限制都符合建議或硬性限制
- [ ]每個輸送量圖都包含其範圍（沙箱/組織/執行個體）

### 術語檢查
- [ ]包含存在於頁面中的所有驗證模式（模擬、測試模式、練習），並以頁面精確術語命名
- [ ]所有生命週期狀態都使用頁面本文中的確切標籤
- [ ]常見問題集答案中沒有不精確的動詞（「回覆」、「合成」、「虛假資料」、「沒有真實資料」），除非在頁面中有逐字記錄

### 範圍檢查
- [ ]辭彙不包含與頁面無關的一般行銷辭彙
- [ ]常見問題解答不會引入頁面中缺少的資訊

如果任何檢查失敗，請先更正區塊，再寫入Include。 在「步驟5」報表中記錄更正。

---

## 同步處理責任

AI知識參考區塊是某個時間點頁面主體的衍生。 必須將其視為頁面的一部分。

**更新頁面本文時（版本PR、更正等）：**

- 如果更新變更區塊中描述的任何護欄、限制、狀態標籤或驗證模式，→在相同的PR中重新產生或手動更新區塊。
- 如果更新與區塊內容無關（例如程式步驟、熒幕擷圖更新），→區塊可能會維持不變，但請簡短檢閱。

包含檔案(`<!-- ai-section-version -->`)內的同步處理註解是訊號：如果包含頁面的內文在寫入雜湊後已變更，則區塊是可供檢閱的候選專案。 更新時，請編輯`help/_includes/do-not-localize/`下的包含檔案，而非頁面。

---

## 完整範本

包含檔案(`help/_includes/do-not-localize/<section-folder>/ai-augmented-<page>.md`)：

```markdown
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

* **TL;DR:** [one sentence]

**Intents:**

* [intent]

**Glossary:**

* **[Term]**: [definition] *(product-specific)*

**Guardrails:**

* [guardrail — qualify each numeric limit as recommended|hard, each throughput figure with scope sandbox|org]

**Terminology:**

* Canonical name: [name] — Acronym: [acronym] — variants: [variants]
* Synonyms: "[a]" = "[b]"
* Do not confuse: "[x]" ≠ "[y]"

**FAQ:**

* **Q: [question]** — [short answer]

+++

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

新增到頁面的行：

```
{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-end-journey.md}}
```

## 附註

- 逐一處理檔案以提升品質。
- 標幟非常短或僅限索引的頁面，並詢問使用者是否要略過。
- 每個頁面唯一建立的新檔案是其「不本地化」包含（步驟4）；頁面本身只會進行編輯以新增單一`{{$include}}`行。 否則，請勿建立或重新建構檔案。
- 產生後驗證檢查清單並非選用專案。 對每個檔案執行該檔案，包括大量作業。
