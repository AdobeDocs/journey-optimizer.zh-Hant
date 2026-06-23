---
source-git-commit: c81615909e033d52fbed56f0195467a3e346a4be
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 1%

---
# augmentedAIContent

在Journey Optimizer檔案存放庫中的一或多個Markdown檔案的結尾附加自動產生的AI助理摺疊式功能表。

## 目標存放庫

`help/using/` （相對於存放庫根目錄）

## 摺疊式功能表語法(Experience League)

```
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**規則：**
- `+++Title`在一行上 — 標題緊接在`+++`之後
- 僅`+++`線上上關閉摺疊式功能表
- 開頭`+++`之前和結尾`+++`之後的空白行

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
3. **使用下列內容產生規則產生收合式選單內容**。
4. **執行產生後驗證檢查清單** （請參閱下文） — 請勿略過。
5. **檢查** AI摺疊式功能表是否已經存在於結尾處（尋找結尾處的`+++AI Knowledge Reference`）。 如果有，詢問使用者：取代或略過？

### 步驟3 — 附加收合式選單

使用以下&#x200B;**內容產生規則**&#x200B;中定義的固定開啟區塊和完整範本。 在檔案結尾附加，緊接著是同步註解：

```
<!-- ai-accordion-version: 1 | source-hash: [first 8 chars of MD5 of file content before accordion] -->
```

此註解可讓日後的工具與編寫器偵測頁面本文何時從摺疊式功能表漂移。 請勿修改任何其他內容。

### 步驟4 — 報表

- 檔案已修改✓
- 略過的檔案+原因（已有收合式選單/空白/索引頁面）
- 在步驟2期間出現的任何驗證警告

---

## 內容產生規則

分析頁面，並以Markdown專案符號清單的順序&#x200B;**產生**&#x200B;以下的區段。 略過無法擷取任何有意義內容的區段。

### 收合式選單標題和固定開啟 — 逐字，請勿修改

每個摺疊式功能表都必須以此精確區塊開頭。 照原樣複製；請勿轉述、壓縮或重新排序：

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

產生的內容區段緊接在這兩個段落之後。

### &#x200B;1. TL；DR

頁面所教授或啟用的內容的一個句子摘要。

```
- **TL;DR:** [one sentence]
```

### &#x200B;2. 意圖

閱讀本頁面後，使用者可完成3至6件事。

```
**Intents:**
- [action]
- [action]
```

### &#x200B;3. 字彙表

此頁面/功能的特定重要辭彙，含簡短定義。 標幟產品特定詞語。

```
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
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
- [guardrail]
```

**護欄精確度規則 — 必要：**

- **將每個數值限制**&#x200B;限定為建議或強制。 範例：「每則訊息最多10個資料集查閱（硬限制）」而非「最多10個資料集查閱」。
- **將每個輸送量或速率圖**&#x200B;限定為它的範圍。 範例：「150,000則訊息/小時TPS上限（每個沙箱）」不是「150,000則訊息/小時上限」。
- **在加入頁面本文之前，交叉檢查每個護欄**。 如果頁面顯示10，而摺疊式功能表顯示5，則摺疊式功能表是錯誤的。 頁面本文是權威的。
- **請勿推斷頁面上未列出的護欄**。 如果限制存在，但頁面未指出它，請忽略它。

### &#x200B;5. 術語

正式名稱、縮寫、接受的變體、同義字、消除歧義。 主要用於AI管道標準化。

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

**狀態與生命週期精確度規則：**
當頁面描述生命週期（歷程狀態、訊息狀態、行銷活動狀態等）時，請從頁面本文複製確切的狀態標籤。 請勿轉述。 使用「請勿混淆」專案，消除共用根字但有不同含義的狀態。 範例：

```
- Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. 常見問題集

使用者可能會問3到6個問題，並提供簡短答案。

```
**FAQ:**
- **Q: [question]** — [short answer]
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

在附加之前，請在每個摺疊式功能表上執行此檢查清單。 在繼續之前標籤使用者的任何失敗。

### 護欄檢查
- [ ]摺疊式功能表中的每個數值都逐字存在或可從頁面本文衍生
- [ ]每個限制都符合建議或硬性限制
- [ ]每個輸送量圖都包含其範圍（沙箱/組織/執行個體）

### 術語檢查
- [ ]包含存在於頁面中的所有驗證模式（模擬、測試模式、練習），並以頁面精確術語命名
- [ ]所有生命週期狀態都使用頁面本文中的確切標籤
- [ ]常見問題集答案中沒有不精確的動詞（「回覆」、「合成」、「虛假資料」、「沒有真實資料」），除非在頁面中有逐字記錄

### 範圍檢查
- [ ]辭彙不包含與頁面無關的一般行銷辭彙
- [ ]常見問題解答不會引入頁面中缺少的資訊

如果任何檢查失敗，請先更正摺疊式功能表，然後再附加。 在步驟4報表中記錄更正。

---

## 同步處理責任

收合式選單是某個時間點頁面主體的衍生物。 必須將其視為頁面的一部分。

**更新頁面本文時（版本PR、更正等）：**
- 如果更新變更了摺疊面板中描述的任何護欄、限制、狀態標籤或驗證模式，→在相同的PR中重新產生或手動更新摺疊面板。
- 如果更新與摺疊式功能表內容無關（例如程式步驟、熒幕擷圖更新），→摺疊式功能表可能會維持不變，但請簡短檢閱。

在收合式選單(`<!-- ai-accordion-version -->`)之後附加的同步註解是訊號：如果收合式選單之前的檔案內容在寫入雜湊之後已變更，則收合式選單是可供檢閱的候選專案。

---

## 完整範本

```markdown
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail — type: recommended|hard — scope: sandbox|org]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
<!-- ai-accordion-version: 1 | source-hash: [hash] -->
```

---

## 附註

- 逐一處理檔案以提升品質。
- 標幟非常短或僅限索引的頁面，並詢問使用者是否要略過。
- 不要建立新檔案 — 只編輯現有的`.md`檔案。
- 產生後驗證檢查清單並非選用專案。 對每個檔案執行該檔案，包括大量作業。
