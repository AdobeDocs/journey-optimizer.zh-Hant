---
name: ajo-ai-accordion
description: 在每個Markdown檔案結尾加上AI Assistant摺疊式功能表區段，以豐富Adobe Journey Optimizer檔案頁面。 讀取每個頁面，根據頁面主題自動產生相關的AI Assistant內容，並將其插入為可摺疊的摺疊式功能表。 當使用者想要將AI資訊新增至AJO檔案、透過AI內容擴充AJO Markdown頁面，或透過AI摺疊式功能表區段處理Markdown檔案的檔案或資料夾時使用。
disable-model-invocation: true
source-git-commit: 80e67d5a60b6427ff87e106e37bf6794ac76a210
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---


# AJO AI摺疊式功能表擴充

在Journey Optimizer檔案存放庫中的一或多個Markdown檔案的結尾附加自動產生的AI助理摺疊式功能表。

## 目標存放庫

`/Users/sauviat/GitHub/GHEC/journey-optimizer.en/help/using/`

## 摺疊式功能表語法(Experience League)

```markdown
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**規則：**
- `+++Title`在一行上 — 標題緊接在`+++`後面，中間沒有空格
- 僅`+++`線上上關閉摺疊式功能表
- 開頭`+++`之前和結尾`+++`之後的空白行

---

## 工作流程

### 步驟1 — 詢問目標

詢問使用者：

> 您要擴充哪個檔案或資料夾？
> - 單一檔案：相對於存放庫根目錄的路徑（例如`help/using/email/get-started-email.md`）
> - 資料夾：以遞回方式處理內部的所有`.md`檔案（例如`help/using/email`）
> - 檔案/資料夾清單

使用`AskQuestion` （如果可用），否則請以對話方式詢問。

如果提供了資料夾，請列出找到的所有`.md`檔案，並在處理之前與使用者確認。

### 步驟2 — 針對每個檔案：讀取和產生

對於每個目標檔案：

1. **完整讀取檔案**。
2. **瞭解頁面主題** — 它涵蓋什麼功能、概念或工作？
3. **使用下列內容產生規則產生收合式選單內容**。
4. **檢查**&#x200B;檔案結尾是否已有AI摺疊式功能表（在結尾附近尋找`+++`）。 如果有，則詢問使用者是否要取代或略過。

### 步驟3 — 附加收合式選單

在檔案結尾附加：

```markdown
+++[ACCORDION_TITLE]

[GENERATED_CONTENT]

+++
```

檔案中的其他內容不應修改。

### 步驟4 — 報表

處理完所有檔案後：
- 已修改的檔案清單✓
- 略過的清單檔案和原因（已有摺疊式功能表、空白檔案、不相關等）

---

## 內容產生規則

分析Markdown頁面以產生摺疊式功能表內容。 以&#x200B;**的順序產生下列區段**，格式為Markdown專案符號清單。 略過無法從頁面擷取任何有意義內容的區段。

---

### 摺疊面板標題

使用： `+++AI Assistant — Page context`

---

### 要產生的區段（依序）

**1. TL；DR**

一個句子。 此頁面會教導或啟用哪些功能？

```markdown
- **TL;DR:** [one sentence summary]
```

---

**2. 意圖**

使用者在閱讀本頁後可完成的任務專案符號清單（3-6個專案）。

```markdown
**Intents:**
- [action the user can perform]
- [action the user can perform]
```

---

**3. 字彙表**

此頁面/功能的特定重要辭彙，定義簡短。 標幟產品特定詞語。

```markdown
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
- **[Term]**: [definition]
```

僅包含與本頁主題相關的詞語。 請勿使用一般行銷詞語填入。

---

**4. 護欄**

頁面上提及的限制、先決條件、許可權或限制。

```markdown
**Guardrails:**
- [guardrail or prerequisite]
- [guardrail or prerequisite]
```

---

**5. 術語**

標準產品名稱、縮寫、接受的變體、同義字和去除混淆提示。 本節主要說明AI管道標準化。

```markdown
**Terminology:**
- Canonical name: [e.g. Adobe Journey Optimizer]
- Acronym: [e.g. AJO] — variants: [e.g. Journey Optimizer, A-JO]
- Synonyms: [e.g. "brand guidelines" = "brand rules", "branding standards"]
- Do not confuse: [e.g. "AI Assistant" ≠ "Adobe Sensei"]
```

僅包含頁面上出現或隱含的專案。

---

**6. 常見問題集**

使用者可能會詢問關於此頁面內容的3到6個問題，並提供簡短回答。

```markdown
**FAQ:**
- **Q: [question]** — [short answer]
- **Q: [question]** — [short answer]
```

---

### 不要包含的內容

- 請&#x200B;**不要**&#x200B;重寫或摘要頁面的內文內容（該內容已經存在）。
- 請&#x200B;**不**&#x200B;包含逐步指示（在頁面中）。
- 請&#x200B;**不**&#x200B;建立頁面不支援的內容。

---

### 完整摺疊式功能表範本

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
- Canonical name: [name]
- Acronym: [acronym] — variants: [variants]

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

---

## 附註

- 逐一處理檔案，而非大量處理，以維持高產生品質。
- 如果頁面很短或完全是重新導向/索引頁面，請將其標幟並詢問使用者是否要略過它。
- 不要建立新檔案 — 只編輯現有的`.md`檔案。
