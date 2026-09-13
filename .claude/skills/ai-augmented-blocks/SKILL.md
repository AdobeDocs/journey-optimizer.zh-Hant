---
name: ai-augmented-blocks
description: 產生並維護Adobe Journey Optimizer檔案的AI知識參考區塊(journey-optimizer.en)。 當說明/使用/下的新頁面需要AI區塊時、當現有頁面已變更且其區塊可能已漂移時，或當要求新增/更新/驗證AI知識參考（AI增強）內容時，可使用。 在help/_include/do-not-localize/<folder>/ai-enhanced-<page>.md下產生「不要本地化」包含，將其匯入具有{{$include}}的頁面，執行強制性的獨立驗證回合，讓區塊為真且明確無誤，在DOCAC JIRA工作中追蹤工作，以及（只有在要求作者之後）開啟PR。 永不合併。
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 0%

---


# AI知識參考區塊

此技能會產生並維護的&#x200B;**AI知識參考**摺疊式功能表區塊
Adobe Journey Optimizer檔案(`journey-optimizer.en`)。 區塊結構化，
附加至檔案頁面的非本地化內容，讓AI助理回答以下問題：
Journey Optimizer更準確。

每個區塊都會儲存為&#x200B;**不當地語系化包含** （因此永遠不會翻譯）並提取
使用`{{$include}}`進入其頁面。 區塊僅包含可從其本身頁面衍生的&#x200B;**個事實
內文** — 未從其他頁面、一般產品知識或HTML註解匯入任何內容。

> **在產生任何內容之前先讀取參考檔案。** 它們包含實際規則，而不是
> 摘要：
> - `references/generation-spec.md` — 區塊結構，固定開口，逐段
>   內容規則和每個精確度規則(硬式與建議限制、驗證模式、
>   狀態標籤、無縮寫、禁止單詞清單)。
> - `references/verification-round.md` — **強制**獨立對手事實檢查
>   這是最後的品質閘道。 這不是選用專案，無法略過。
> - `references/git-jira-tracking.md` — 分支/認可/PR流程(在開啟
>   PR；**絕不合併**)和DOCAC JIRA追蹤。

## 此技能適用時

- 在`help/using/<folder>/`下建立的&#x200B;**新頁面**→為其產生區塊。
- **現有頁面已變更**，→檢查其區塊是否從頁面本文漂移，並加以更新。
- 要求您&#x200B;**新增、更新、驗證或稽核** AI知識參考/AI增強區塊。

## 範圍和排除專案

- **範圍： `help/using/<folder>/`下的**&#x200B;頁。
- **超出範圍 — 請勿在此新增區塊：**
  - `help/rp_landing_pages/` （開始使用/登陸頁面） — 由作者規則排除。
  - 精簡導覽/連結中樞、僅限索引的頁面，以及幾乎空白的頁面。 當頁面是空頁面時
    沒有實質概念的連結清單，**略過該清單並說為什麼** — 不要強制封鎖。
  - 發行說明（`help/using/rn/`，發行說明頁面）。
- 當懷疑某個頁面是否足夠實質時，請根據內容來判斷：它是否真的有教益
概念、限制或術語會涵蓋它；如果它只指向其他地方，請略過。

## 工作流程

一次處理&#x200B;**一個資料夾（或一個頁面）**。 請勿將不相關的資料夾批次新增至一個分支。

### 1 — 決定目標和模式

詢問作者（或從請求/開啟檔案中推斷）要處理哪些頁面，並偵測
每頁模式：

- **CREATE** — 頁面沒有`{{$include .../ai-augmented-<page>.md}}`行，而且不存在
內嵌`+++ AI Knowledge Reference`區塊→產生新區塊。
- **UPDATE** — 頁面已經有區塊。 計算頁面主體雜湊並將其與
  包含同步評論中的`source-hash` （請參閱下文）。 如果兩者不同，頁面會漂移→
  重新產生/重新整理區塊。 如果兩者相符，此區塊為目前→略過的區塊（報告「最新」）。
- **移轉** — 頁面有&#x200B;*內嵌* `+++ AI Knowledge Reference`區塊（尚未完成）
外部化)，→將其移至「請勿本地化」 include中，並以 `{{$include}}`
線條，保留內容保真度。

在任何地方都以相同的方式計算頁面主體雜湊（用於同步註釋和漂移檢查）：

```bash
md5 -q help/using/<folder>/<page>.md | cut -c1-8
```

在編輯頁面&#x200B;**之前**計算它（雜湊會覆蓋內文，如同區塊所在時一樣）
（已產生）。 在Linux上使用`md5sum help/using/<folder>/<page>.md | cut -c1-8`。

### 2 — 產生（或重新整理）區塊

每個頁面完全遵循`references/generation-spec.md`。 關鍵不變數：

- 兩個&#x200B;**固定開啟段落**，逐字重複，逐位元組（從未轉譯）。
- 節順序： **TL；DR、意圖、字彙表、護欄、術語、常見問題集**。
- 只以頁面本文為根據的每個宣告。 無收縮。 限定數字為
  `(hard limit)` / `(recommended)` **僅**當頁面使用強制執行/建議時
  用詞；否則就沒有限定詞。 使用頁面的確切驗證模式和狀態標籤。
  保留`[!UICONTROL ...]` / `[!DNL ...]`字串。 絕對不要使用禁止的不精確度
  除非字詞在頁面上逐字出現。

**包含檔案** — `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`
（視需要建立`<folder>`子目錄；使用`-`平面化任何巢狀頁面路徑）：

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening paragraphs + the six sections]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of the page body> -->
```

**編輯頁面** — 只新增一行，作為最後一行內容，前面加上空白行
（請勿觸碰頁面中的其他內容）：

```
{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}
```

在UPDATE上，僅編輯包含檔案（如果您想要追蹤，請編輯增加`ai-section-version`）
修訂版本)；頁面的`{{$include}}`行通常保持不變。 重新整理`source-hash`至
區塊再次符合頁面時目前的頁面主體雜湊。

在`references/generation-spec.md`中執行&#x200B;**自我檢查** (步驟3 verify-every-claim +
產生後的檢查清單)，然後再繼續。 這是2的閘道1。

### 3 — 獨立驗證回合（強制性的最終閘道）

這是作者特別需要的步驟： **確認每個區塊有效、為真，以及
沒有模稜兩可。** 以&#x200B;*全新、獨立的*階段執行 — 最好是獨立子代理
只看到頁面本文和區塊，沒有區塊寫入方式的記憶體 — 如下
`references/verification-round.md`. 它會重新檢查每個索賠，將任何標示錯誤的限制降級，
修正同義字vs-Do-Not-confusion錯誤，並移除頁面未接地的所有專案。 套用
在繼續之前對包含檔案進行每次修正。 這是2的閘道2，無法跳過。

### 4 — 結構掃描

在認可之前，請掃描每個區塊以取得結構和衛生（請參閱中的掃描片段）
`references/git-jira-tracking.md`)：前端內容+ `# AI Knowledge Reference`標題，
`+++ … +++`個柵欄、固定開頭段落、同步註解、無縮排(排除
逐字`[!UICONTROL ...]`)，以及頁面中相符的`{{$include}}`行。

### 5 — 在JIRA中追蹤，然後詢問PR （永不合併）

關注`references/git-jira-tracking.md`：

1. 認可名為JIRA工作(`DOCAC-<key>`)的分支，絕不認可於`main`。 驗證
認可登陸到分支（先於`origin/main`認可1個），而不是在`main`上。
2. 更新DOCAC工作：以變更內容加上驗證結果，設定修正
版本，並根據您團隊的程式需要進行轉換。
3. **詢問作者是否想要提取要求。** 只有在對方同意時才開啟一個。
4. **永不合併。** 這些PR是供人工稽核；合併永遠是作者的要求。

### 6 — 報表

每頁報告：已建立/更新/已移轉/已略過（+原因），驗證結果
（已清除或已更正，包含更正）、JIRA工作及PR連結（如果已開啟）。

## 執行此項技能的作者的注意事項

- 區塊是某個時間點之頁面主體的&#x200B;**衍生** — 將其視為
頁面。 當您以接觸護欄、限制、狀態標籤或的方式變更頁面時
驗證模式，在同一變更中更新區塊。
- JIRA和PR步驟需要存取企業JIRA和GitHub。 如果您沒有
存取，仍產生+驗證區塊並在本機開啟變更；處理JIRA/PR步驟
適合有此情況的人。
- 此技能存在於存放庫中，因此整個撰寫團隊會共用一個程式。 改善
在此處參考檔案，而不是保留私人副本。
