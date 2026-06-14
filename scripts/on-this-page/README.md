---
source-git-commit: a4123db7ae90552a15e6f425bce0037426053a78
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---
# 「在此頁面上」方塊工具

用於新增及驗證標準&#x200B;**「在此頁面上」**&#x200B;頂部陰影方塊的工具
AJO檔案頁面。檢視`.cursor/rules/on-this-page-box.mdc`中的規格。
已在epic **DOCAC-14936**&#x200B;下追蹤轉出（每個頂層資料夾一個任務）。

## 此方塊的外觀

```text
# Page Title {#anchor}

>[!BEGINSHADEBOX]

**On this page:** <one clear sentence describing the page's purpose>

>[!ENDSHADEBOX]
```

## 建議的工作流程（依資料夾/Jira任務）

從存放庫根目錄(`journey-optimizer.en/`)執行。

1. **插入方塊** (從每一頁的前端內容植入第一稿句子
   `description`). 機械式、等冪、絕不接觸前置物件：

   ```bash
   python scripts/on-this-page/add_on_this_page.py help/using/reports --seed-from-description
   ```

   先使用`--dry-run`預覽。

2. **調整措辭。** 種子是起點 — 編輯每個句子
讀為目的陳述（一句話、純文字、美式英文）。 如果您
略過`--seed-from-description`，已插入`{{TODO...}}`預留位置，並且
驗證器會標籤任何剩餘的專案。

3. 開啟PR之前&#x200B;**驗證**：

   ```bash
   python scripts/on-this-page/validate_on_this_page.py help/using/reports --require
   ```

   退出程式碼在任何失敗時都是非零的，因此它可以閘道CI。

## 範圍/排除專案

預設會排除參考和語法頁面(路徑部分`api-reference`，
`expression`, `functions`). 必要時使用`--exclude ...`覆寫。

## 全存放庫進度檢查

```bash
python scripts/on-this-page/validate_on_this_page.py help
```

如果沒有`--require`，仍遺漏方塊的頁面會回報為`pending` (非
失敗)，因此您可以在整個指南中追蹤轉出進度。
