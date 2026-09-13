---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---
# 驗證回合 — 強制的最終品質閘道

這是2的閘道2，而且保證每個區塊的步驟為&#x200B;**有效、正確且免費
模糊&#x200B;**。 &#x200B;** 不是選用專案，不能略過**，包括單頁更新。

## 為什麼會分開

區塊作者（閘道1）離區塊太近，無法擷取其本身的接地錯誤。 閘道2
是&#x200B;**獨立的對手重新檢查**：新的檢閱者認為區塊可能錯誤
並嘗試加以證明，僅使用&#x200B;**1&rbrace;頁面內文作為真值。**&#x200B;以&#x200B;**個獨立的子代理程式執行**
尚未看到區塊如何撰寫 — 正是這種獨立性讓區塊變得有效。 的
一整批頁面，一個驗證器子代理可以覆蓋整個資料夾。

## 每頁驗證器的功能

1. 讀取&#x200B;**完整來源頁面** `help/using/<folder>/<page>.md`。 HTML-comment /
註解的內容是&#x200B;**不是**&#x200B;有效的來源。
2. 讀取&#x200B;**區塊** `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`。
3. 將&#x200B;**every**&#x200B;宣告分類為已接地/不準確/未接地，以針對頁面內文。
4. **僅編輯區塊檔案來修正每個問題** — 保留兩個已修正的開頭
段落、`+++ … +++`圍欄和同步處理註解。 絕對不要修改來源頁面。
5. 每頁報告： `clean`或`N issues` +套用的確切修正。

## 對抗性檢查清單（風險最高的專案優先）

- **數字和限制。** 每個值都相同。 只有在頁面使用時，限制才會是`(hard limit)`
強制/最大字詞；如果可引發/預設/可設定（包括「請求」），則為`(default)`
透過您的Adobe代表取得更多資訊」或「可透過API取得」)；`(recommended)`以取得建議；否
限定詞（如果頁面未提供限定詞）。 **將產生器上標標為hard的端點降級。**
每個輸送量/速率數字都有其範圍。
- **日期、識別碼、產品/欄位名稱、SQL識別碼、狀態列舉、錯誤字串** — 逐字
從頁面。 對法規遵循/法律時限的零容忍：絕不發明SLA、保留、
或執行日期；將任何日期維持在頁面宣告的完整日期並標籤為頁面
將其框架化。
- **同義字與不要混淆。** 同義字(`"A" = "B"`)需要頁面上的兩個表單
意思是一樣的。 任何對比(`"X" ≠ "Y"`)都屬於「請勿混淆」之下。 移動
標籤錯誤。
- **驗證/測試模式**&#x200B;以頁面的確切辭彙命名，並未混淆
經典vs — 重新設計的體驗或跨管道。
- **接地。** 沒有從其他頁面、一般產品知識或HTML匯入的專案
評論。 移除頁面本文不支援的任何內容。
- **樣式。** 沒有縮排（在逐字`[!UICONTROL ...]` / `[!DNL ...]`字串之外）。 無
禁用的字詞（「合成」、「虛假資料」、「沒有真實資料」、「回覆」、「回覆」）
除非在頁面上一字不差。 UI字串會完全保留。
- **結構。** 兩個固定開頭的段落完整且一字不差；有六個段落出現且位於
頁面支援它們的順序；出現同步註解。

## 可重複使用的驗證器子代理程式提示

填寫資料夾和頁面清單。 以獨立的一般用途子代理程式形式啟動。

```
You are an ADVERSARIAL fact-checker for Adobe Journey Optimizer doc "AI Knowledge Reference"
blocks. Repo: <repo path>. Assume each block MAY contain errors; try hard to find them. This is
the final accuracy gate.

PAGES (basenames): <p1> <p2> ...
SOURCE: help/using/<folder>/<p>.md   BLOCK: help/_includes/do-not-localize/<folder>/ai-augmented-<p>.md

For EACH page:
1. Read the FULL source page body (HTML-comment / commented-out content is NOT valid source).
2. Read the block.
3. Classify EVERY claim GROUNDED / INACCURATE / NOT-GROUNDED against the page body. Scrutinize:
   numeric limits (hard only if the page uses enforcement/maximum wording; downgrade any
   raisable/default/configurable value the block marked hard; every rate figure needs its
   scope); dates/IDs/field names/SQL identifiers/status enums/error strings verbatim and no
   invented SLA/legal timeframes; Synonyms are true equivalents (mislabels -> Do not confuse);
   validation/test modes named with the page's exact terms and not conflated; nothing imported
   from other pages or HTML comments; no contractions (outside verbatim [!UICONTROL ...]); no
   banned words (synthetic / fake data / without real data / revert / roll back) unless verbatim.
4. FIX every issue by editing ONLY the block file. Preserve the two fixed opening paragraphs,
   the +++ ... +++ fences, and the sync comment. Do NOT modify source pages.

Report per page: "<p>: clean" or "<p>: N issues" + the exact fixes applied.
```

## 退出條件

只有當驗證器將每個頁面報告為`clean` （它找到任一頁面）時，資料夾才會通過閘門2
沒有內容，或套用了修正，區塊現在已清除)。 如果套用修正，則已經是
在區塊檔案中 — 將其包含在最終報告中，然後繼續掃描並提交。
