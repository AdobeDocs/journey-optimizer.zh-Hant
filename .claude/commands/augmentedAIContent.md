---
source-git-commit: 80e67d5a60b6427ff87e106e37bf6794ac76a210
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

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

&#x200B;---

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
3. **使用以下規則產生收合式選單內容**。
4. **檢查** AI摺疊式功能表是否已經存在於結尾處（尋找結尾處的`+++AI Assistant`）。 如果有，詢問使用者：取代或略過？

### 步驟3 — 附加收合式選單

在檔案的結尾附加。 請勿修改任何其他內容。

### 步驟4 — 報表

- 檔案已修改✓
- 略過的檔案+原因（已有收合式選單/空白/索引頁面）

&#x200B;---

## 內容產生規則

分析頁面，並以Markdown專案符號清單的順序&#x200B;**產生**&#x200B;以下的區段。 略過無法擷取任何有意義內容的區段。

### 摺疊面板標題

`+++AI Assistant — Page context`

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

### &#x200B;4. 護欄

頁面上提及的限制、先決條件、許可權或限制。

```
**Guardrails:**
- [guardrail]
```

### &#x200B;5. 術語

正式名稱、縮寫、接受的變體、同義字、消除歧義。 主要用於AI管道標準化。

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

### &#x200B;6. 常見問題集

使用者可能會問3到6個問題，並提供簡短答案。

```
**FAQ:**
- **Q: [question]** — [short answer]
```

### 不要包含的內容

- 請&#x200B;**不**&#x200B;重寫或摘要內文內容（內容已位於頁面中）
- 請&#x200B;**不**&#x200B;包含逐步指示
- 請&#x200B;**不**&#x200B;該頁面不支援的發明內容

### 完整範本

```markdown
+++AI Assistant — Page context

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

&#x200B;---

## 附註

- 逐一處理檔案以提升品質。
- 標幟非常短或僅限索引的頁面，並詢問使用者是否要略過。
- 不要建立新檔案 — 只編輯現有的`.md`檔案。
