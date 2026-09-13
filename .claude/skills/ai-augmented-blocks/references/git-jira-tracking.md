---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---
# Git、PR和JIRA追蹤

如何安全地著陸變更並加以追蹤。 來自作者的兩個固定規則：

1. **開啟PR前先詢問。** 無論如何產生及驗證區塊，但僅開啟提取
若作者答應，則要求支援。
2. **永不合併。** 這些PR是為了供人工審查而存在的。 合併一律由作者決定。

## 結構掃描（在認可前執行）

對於資料夾中處理的每個頁面：

```bash
cd <repo>
for p in <page1> <page2> ...; do
  f="help/_includes/do-not-localize/<folder>/ai-augmented-$p.md"
  inc="help/using/<folder>/$p.md"
  [ -f "$f" ] || echo "MISSING BLOCK: $f"
  grep -q '^# AI Knowledge Reference' "$f"            || echo "$p: missing H1"
  grep -q '^+++ AI Knowledge Reference' "$f"          || echo "$p: missing accordion open"
  grep -q 'This section contains structured knowledge' "$f" || echo "$p: missing opening para 1"
  grep -q 'ai-section-version' "$f"                   || echo "$p: missing sync comment"
  grep -nEi "\b(isn't|aren't|don't|doesn't|didn't|can't|won't|wouldn't|couldn't|shouldn't|it's|we've|we're|you're|they're|that's|there's|haven't|hasn't|wasn't|weren't)\b" "$f" \
    | grep -vi 'UICONTROL' && echo "  ^ $p contraction"
  grep -q "do-not-localize/<folder>/ai-augmented-$p.md" "$inc" || echo "$p: MISSING include in page"
done
echo "=== sweep done ==="
git status --short
```

任何列印的行（除了「掃描完成」和`git status`清單之外）都是之前要修正的瑕疵
認可。

## 分支和認可（永遠不認可主要專案）

```bash
git checkout main -q && git pull -q origin main
git checkout -q -b DOCAC-<key> origin/main    # branch name = the JIRA task key
# ... generate + verify + sweep ...
git add help/_includes/do-not-localize/<folder>/ help/using/<folder>/*.md
git commit -q -m "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)

<one-line what + the verification result>

Co-Authored-By: Claude <model> <noreply@anthropic.com>"
```

**驗證認可是否登陸在分支上，而不是在`main`** (已知的步槍 — 如果您切換到
`main`若要檢查頁面，稍後認可可以登陸該頁面)：

```bash
git rev-parse --abbrev-ref HEAD                    # must print DOCAC-<key>
git rev-list --left-right --count origin/main...DOCAC-<key>   # must show  0<TAB>1
```

如果認可意外著陸`main`： `git branch -f DOCAC-<key> <sha>`，指向分支
按一下`git checkout DOCAC-<key>`，然後`git branch -f main origin/main`以重設本機主節點。
`origin/main`絕不受本機錯誤的影響。

推播： `git push -u origin DOCAC-<key>` (如果分支已存在，請使用`--force-with-lease`
在較舊的認可上遠端執行)。

## 詢問公關

直接詢問作者，例如： *&quot;已產生並驗證`<folder>`的區塊。 您要
我要開啟PR以供檢閱嗎？&quot;* 僅限是時：

```bash
gh pr create --base main --head DOCAC-<key> \
  --title "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)" \
  --body-file <pr-body>.md
```

PR內文結尾是必要的歸因行
(`🤖 Generated with [Claude Code](https://claude.com/claude-code)`). **不要合併** — 保留
PR開啟以供檢閱。

## JIRA追蹤

追蹤DOCAC任務中的每個變更（轉出史詩： `DOCAC-15582`）。 尋找或建立資料夾的
任務，然後：

1. **註解**，其中包含已變更的專案和驗證結果(已覆蓋/略過的頁面、驗證器
清除/修正、任何值得注意的硬式與預設呼叫)。 納入PR連結（若已開啟）。
2. **設定修正版本** （此程式使用`AJO26.9`）。
3. 根據您的工作流程，**轉換**個進行中的新→動→已解決（解析度「已修正」）。 在這個
專案轉換ID為`4` （開始進度），然後`5` （解決，含解決方式）
   `{"name":"Fixed"}`)；仍處於「新增」中的任務必須先啟動，然後才能解析。

使用公司JIRA MCP工具(`fixVersions`的`add_jira_comment`，`update_jira_issue`，
`bulk_transition_jira_issues`)或JIRA UI。 如果您沒有JIRA存取權，請將此步驟移至
有人擁有該檔案，並在您的報告中加以註記。

## 一個資料夾=一個分支=一個任務

請勿在單一分支或PR中混合無關的資料夾。 稍後新增的新頁面是它自己的小頁面
變更（「建立」模式），並可共用資料夾的工作或取得自己的工作（依您的團隊偏好而定）。
