---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 4%

---
# 產生規格 — AI知識參考區塊

AI知識參考區塊包含內容的單一信任來源及其方式
已寫入。 每一個頁面都完全遵循它。 (這反映了舊版的
`.claude/commands/augmentedAIContent.md`；技能是標準版本。)

## 黃金法則

區塊只能包含&#x200B;**從它自己的頁面主體衍生的內容。** 不是其他頁面，不是
一般產品知識，而非HTML註解/註解的內容。 如果頁面未顯示
也就是說，區塊也不會。

## 收合式選單+包含語法

```
+++ AI Knowledge Reference

Content here — standard markdown.

+++
```

- `+++ AI Knowledge Reference`開啟（`+++`後一個空格）；僅`+++`關閉。
- 開頭`+++`之前和結尾`+++`之後的空白行。
- 標題一律為`AI Knowledge Reference`。
- 整個摺疊式功能表都位於「請勿本地化」包含中，頁面會將其拉入
  `{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}`. 下的內容
  `help/_includes/do-not-localize/`已從本地化中排除 — 這就是區塊保留的方式
  未翻譯。

## 包含檔案結構

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening — verbatim]

[the six sections in order]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of page body> -->
```

- **檔案名稱：**&#x200B;衍生自相對於其最上層的頁面路徑 `help/using/<folder>/`
區段：移除`.md`，將任何剩餘的`/`取代為`-`，首碼為`ai-augmented-`。
  - `help/using/building-journeys/end-journey.md` → `ai-augmented-end-journey.md`
  - `help/using/building-journeys/expression/journey-properties.md`→
    `ai-augmented-expression-journey-properties.md`
- 每個頂層區段(`building-journeys/`、`email/`、`data/`、...)一個子資料夾。

## 固定開啟 — 逐字，不修改

每個區塊都以這兩個段落開始。 逐位元組複製；請勿轉譯
壓縮或重新排序：

```
This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

## 六個區段，依序排列

只有在頁面沒有為其產生有意義的內容時，才跳過區段。

### &#x200B;1. TL；DR
一個句子：頁面所教授或啟用的內容。`* **TL;DR:** [one sentence]`

### &#x200B;2. 意圖
讀取頁面後，使用者可完成3到6件事。

### &#x200B;3. 字彙表
重要頁面特定辭彙，含簡短定義；以標示產品特定辭彙
`*(product-specific)*`. 沒有通用的行銷內距。

**驗證模式精確度（必要）：** （如果頁面涵蓋測試/預覽/模擬）
執行，區分頁面實際名稱的每個模式 — 不要將其摺疊。 使用
頁面的確切辭彙(例如`Simulate content`、`Simulate content (AEP profiles)`、
`Send proof`, `Test mode`, `Dry run`, `Simulation`, `test profile`, `sample input`). 從不
將「合成設定檔」、「虛假資料」或「沒有真實資料」取代為其中任何。

### &#x200B;4. 護欄
頁面上所述的限制、必要條件、許可權、限制。

- **將每個數值限制**&#x200B;限定為`(hard limit)`或`(recommended)` — 但&#x200B;**僅限**&#x200B;當
頁面使用強制措辭（錯誤/已拒絕/上限/不能超過/僅限……支援）
或建議用語（為獲得最佳效能/建議使用）。 如果頁面未提供
限定詞，不提供。 **永遠不要將可產生、預設或可設定的值標示為實數。**
可「連絡您的Adobe代表」或透過API提出的值包括
  `(default)`，不是硬式。
- **將每個輸送量/速率數字限定為其範圍** （每個沙箱/每個組織/每個執行個體）。
- **對照頁面內文交叉檢查每個數字。** 頁面本文是權威的。
- **請勿推斷**&#x200B;頁面未顯示的護欄。 無中繼註解(「此頁面不
指定……」)。

### &#x200B;5. 術語
正式名稱、縮寫、變體、同義字、消除歧義。

- **同義字** (`"A" = "B"`)僅適用於&#x200B;**true等同專案** — 兩個表單都必須出現在頁面上
意思是一樣的。 任何*對比*&#x200B;低於&#x200B;**請勿混淆**
(`"X" ≠ "Y"`)，不是同義字。
- **狀態/生命週期精確度：**&#x200B;從頁面本文複製精確的狀態標籤；不要
轉述。 使用「請勿混淆」來分隔共用根字的狀態。

### &#x200B;6. 常見問題集
3-6個可能的問題和簡短答案。 答案使用與頁面相同的&#x200B;**動詞和名詞
內文**。 除非頁面使用，否則請勿引入「回覆」、「重設」或「回覆」。

## 不要包含的內容

- 請勿重寫或摘要內文內容，或提供逐步指示。
- 不要創作頁面不支援的內容。
- 請勿使用這些不精確的辭彙，除非它們出現在頁面上&#x200B;**逐字**：
&quot;synthetic&quot;、&quot;fake data&quot;、&quot;without real data&quot;、&quot;revert&quot;、&quot;roll back&quot;。
- **區塊散文中的任何地方都沒有收縮** — 拼出「不是」、「不是」、「無法」、
&quot;it is&quot;等。(唯一的例外是逐字產品UI字串，例如
  `[!UICONTROL configuration doesn't exist]`，將完全保留。)

## 步驟3 — 確認每一項申請（自行檢查，閘門1）

在撰寫包含檔案之前，請先透過宣告重新讀取產生的內容宣告。 強制，即使是
短頁。 在寫入之前更正任何錯誤，並在報表中記錄更正。

- 區塊中的每個字詞/標籤/UI名稱都會顯示在頁面本文中。
- 除非兩個表單都出現在頁面上，否則沒有同義字；每個「不要混淆」僅供參考
此頁面上的概念。
- 每個數值都完全符合頁面內文；每個限制限定詞都由
頁面的用詞；沒有發明的限定詞。
- 沒有從其他頁面或一般知識匯入的字彙表/常見問題集詳細資訊。
- 除非頁面上一字不差，否則不得禁止使用不精確的辭彙；不得使用縮寫。

## 產生後的檢查清單（閘門1，繼續）

- [ ]每個數值都是逐字存在/是從頁面主體衍生的。
- [ ]每個限制都正確限定（硬限與建議限與無限）；沒有預設/可引的數值
 標示錯誤，為硬。
- [ ]每個輸送量數字都有其範圍。
- [ ]頁面上出現的所有驗證模式都以頁面精確術語命名。
- [ ]所有生命週期狀態都使用確切的頁面標籤。
- [ ]同義字為True等同專案；對比專案位於「不要混淆」下。
- [ ]沒有禁止的字詞/沒有縮寫（在逐字UI字串之外）。
- [ ]字彙表沒有泛用術語；常見問題集不會引入頁面中缺少的內容。

閘門1是檢查自己工作的區塊作者。 它&#x200B;**不會**&#x200B;取代
`verification-round.md`中的獨立驗證回合（閘門2）。
