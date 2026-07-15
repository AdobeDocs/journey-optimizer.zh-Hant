---
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---
# augmentedAIContent

在Journey Optimizer檔案存放庫中的一或多個Markdown檔案的結尾附加自動產生的&#x200B;**快速參考**&#x200B;區段。

## 目標存放庫

`help/using/` （相對於存放庫根目錄）

## 區段和索引標籤語法(Experience League)

### 章節標題

```
## Quick reference {#quick-reference}
```

### 索引標籤

```
>[!BEGINTABS]

>[!TAB Tab name]

Content here — any standard markdown is valid.

>[!TAB Another tab]

Content here.

>[!ENDTABS]
```

**規則：**

- `>[!BEGINTABS]`和`>[!ENDTABS]`各自佔一行，由空白行包圍
- `>[!TAB Name]`在它自己的行上，在內容前接著空白行
- 索引標簽名稱為標題大寫、短整數（1-3字）
- `>[!BEGINTABS]`之前和`>[!ENDTABS]`之後的空白行

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
3. **使用以下內容產生規則產生區段內容**。
4. **執行產生後驗證檢查清單** （請參閱下文） — 請勿略過。
5. **檢查**&#x200B;是否快速參考區段在結尾已經存在（在結尾附近尋找`## Quick reference`）。 如果有，詢問使用者：取代或略過？

### 步驟3 — 驗證針對頁面本文的所有宣告

在附加之前，請依宣告重新讀取產生的區段宣告。 此步驟是&#x200B;**必要步驟，即使檔案較短，也不可略過**。 請先修正任何故障，再繼續執行步驟4。

**術語和標籤**

- [ ]區段中的每個字詞、標籤和UI名稱都會顯示在頁面本文中 — 不是從其他頁面匯入或根據一般產品知識推斷
- [ ]未列出同義字，除非兩個表單都出現在頁面上
- [ ]每個「請勿混淆」專案僅參考本頁提及的概念

**護欄和限制**

- [ ]每個數值都與頁面本文完全相符
- [ ]只有當頁面本文使用該單字或明確表示系統強制使用它（例如「不能超過」、「允許的最大值……」、「僅……支援」）時，限制才稱為&#x200B;**hard**
- [ ]只有當頁面本文使用該字或同等字詞時，限制才稱為&#x200B;**建議** （「為獲得最佳效能」，「建議使用」）
- [ ]如果頁面本文未提供限定詞，區段會提供none — 不要發明一個
- [ ]來源頁面沒有內文註解（例如：「此頁面上未說明任何特定數字」）

**字彙表定義**

- [ ]沒有定義包含頁面本文中缺少的技術細節
- [ ]沒有專案會使用檔案集中其他頁面的資訊進行詳細說明

**常見問題解答**

- [ ]每個特定詳細資訊（UI提供、按鈕名稱、欄位名稱、步驟順序）都列在頁面本文中 — 未從其他頁面推斷或匯入
- [ ]沒有回應會引入頁面本文未處理的資訊

**更正規則：**&#x200B;如果任何檢查失敗，請在&#x200B;**之前更正內容**。 在步驟5報表中記錄每次校正。

---

### 步驟4 — 附加區段

使用以下&#x200B;**內容產生規則**&#x200B;中定義的固定開啟區塊和完整範本。 在檔案結尾附加，緊接著是同步註解：

```
<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of file content before section] -->
```

此註解可讓未來的工具與編寫器偵測頁面內文何時從區段漂移。 請勿修改任何其他內容。

### 步驟5 — 報表

- 檔案已修改✓
- 略過的檔案+原因（已經有區段/空白/索引頁面）
- 在步驟2期間出現的任何驗證警告

---

## 內容產生規則

分析頁面，並依順序&#x200B;**產生**&#x200B;以下的索引標籤。 如果無法擷取任何有意義的內容，請完全略過索引標籤。

### 截面標題和固定開啟 — 逐字，不修改

每個快速參考區段都必須以此精確區塊開頭。 照原樣複製；請勿轉述、壓縮或重新排序：

```
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

`>[!BEGINTABS]`區塊緊接在這兩個段落之後。

### 標籤1 — 概觀

單句TL；DR頁面教學或啟用的摘要，接著是使用者閱讀本頁面後可完成的3至6件事。

```
>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [action]
* [action]
```

### 索引標籤2 — 字彙表

此頁面/功能的特定重要辭彙，含簡短定義。 標幟產品特定詞語。

```
>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*
```

僅包含與此頁面相關的字詞。 請勿使用一般行銷詞語填入。

**驗證模式精確度規則 — 強制：**
如果頁面涵蓋任何形式的測試、預覽或模擬執行，您必須區分頁面實際描述的所有模式。 請勿將不同的模式摺疊為單一速記專案：
- **模擬** — 呈現訊息內容而不傳送；使用真實設定檔
- **測試模式** — 僅傳送至指定的測試設定檔；使用持續性AEP測試設定檔（非合成或偽裝設定檔）
- **練習** — 執行完整的歷程邏輯而不啟動動作；使用真實的對象資料

僅包含頁面中存在的模式。 從頁面本文複製產品精確的辭彙 — 請勿將「合成設定檔」、「假資料」或「沒有真實資料」取代任何這些專案。

### 索引標籤3 — 術語

正式名稱、縮寫、接受的變體、同義字、消除歧義。 主要用於AI管道標準化。

```
>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [list]
* **Synonyms:** "[term A]" = "[term B]"
* **Do not confuse:** "[term]" ≠ "[other term]"
```

**狀態與生命週期精確度規則：**
當頁面描述生命週期（歷程狀態、訊息狀態、行銷活動狀態等）時，請從頁面本文複製確切的狀態標籤。 請勿轉述。 使用「請勿混淆」專案，消除共用根字但有不同含義的狀態。 範例：

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### 標籤4 — 護欄和限制

頁面上提及的限制、先決條件、許可權或限制。

```
>[!TAB Guardrails & Limitations]

* [guardrail]
```

**護欄精確度規則 — 必要：**

- **將每個數值限制**&#x200B;限定為建議或強制。 範例：「每則訊息最多10個資料集查閱（硬限制）」而非「最多10個資料集查閱」。
- **將每個輸送量或速率圖**&#x200B;限定為它的範圍。 範例：「150,000則訊息/小時TPS上限（每個沙箱）」不是「150,000則訊息/小時上限」。
- **在加入頁面本文之前，交叉檢查每個護欄**。 如果頁面顯示為10，而區段顯示為5，則區段是錯誤的。 頁面本文是權威的。
- **請勿推斷頁面上未列出的護欄**。 如果限制存在，但頁面未指出它，請忽略它。

### 索引標籤5 — 常見問題集

使用者可能會問3到6個問題，並提供簡短答案。 將每個問題格式化為粗體問題標題，後面跟著段落答案。

```
>[!TAB FAQ]

**Q: [question]**

[short answer]
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

在附加之前，請在每個區段上執行此檢查清單。 在繼續之前標籤使用者的任何失敗。

### 護欄檢查

- [ ]區段中的每個數值都逐字存在，或是可從頁面本文衍生
- [ ]每個限制都符合建議或硬性限制
- [ ]每個輸送量圖都包含其範圍（沙箱/組織/執行個體）

### 術語檢查
- [ ]包含存在於頁面中的所有驗證模式（模擬、測試模式、練習），並以頁面精確術語命名
- [ ]所有生命週期狀態都使用頁面本文中的確切標籤
- [ ]常見問題集答案中沒有不精確的動詞（「回覆」、「合成」、「虛假資料」、「沒有真實資料」），除非在頁面中有逐字記錄

### 範圍檢查
- [ ]辭彙不包含與頁面無關的一般行銷辭彙
- [ ]常見問題解答不會引入頁面中缺少的資訊

如果任何檢查失敗，請先更正區段，然後再進行附加。 在步驟4報表中記錄更正。

---

## 同步處理責任

快速參考區段是某個時間點頁面主體的衍生物。 必須將其視為頁面的一部分。

**更新頁面本文時（版本PR、更正等）：**

- 如果更新變更了區段中所述的任何護欄、限制、狀態標籤或驗證模式，→在相同的PR中重新產生或手動更新區段。
- 如果更新與區段內容無關（例如程式步驟、熒幕擷圖更新），→區段可能會維持不變，但請簡短檢閱。

在區段(`<!-- ai-section-version -->`)之後附加的同步註解是訊號：如果區段之前的檔案內容在寫入雜湊之後已變更，則區段是可供檢閱的候選區段。

---

## 完整範本

```markdown
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

>[!BEGINTABS]

>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [intent]

>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*

>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [variants]
* **Synonyms:** "[a]" = "[b]"
* **Do not confuse:** "[x]" ≠ "[y]"

>[!TAB Guardrails & Limitations]

* [guardrail — type: recommended|hard — scope: sandbox|org]

>[!TAB FAQ]

**Q: [question]**

[short answer]

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

## 附註

- 逐一處理檔案以提升品質。
- 標幟非常短或僅限索引的頁面，並詢問使用者是否要略過。
- 不要建立新檔案 — 只編輯現有的`.md`檔案。
- 產生後驗證檢查清單並非選用專案。 對每個檔案執行該檔案，包括大量作業。
