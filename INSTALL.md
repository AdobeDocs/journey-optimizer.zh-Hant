---
source-git-commit: 08eaa7ae974c134ea2e920a1fa854dcf6a971e18
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---
# 🚀正在安裝游標代理程式

游標代理程式是共用工具，可協助您更有效率地建立和維護檔案。

## 首次設定

您只需要為每個存放庫執行此&#x200B;**次**。

### 選項1：使用游標（建議使用⭐）

1. 開啟游標聊天（`Cmd+L`或`Ctrl+L`）
2. 型別：

   ```
   @setup-agents
   ```

3. 代理程式將自動：
   - 測試SSH和HTTPS存取
   - 使用工作方法
   - 視需要引導您完成設定
4. 完成！✨

**注意：**&#x200B;代理程式會自動偵測您是否擁有`git.corp.adobe.com`的SSH或HTTPS存取權，並使用適當的方法。 如果兩者皆不運作，則提供引導式設定。

### 選項2：使用終端機

1. 在存放庫根目錄中開啟您的終端機
2. 執行：

   ```bash
   ./setup-agents.sh
   ```

   指令碼將自動：
   - 測試SSH和HTTPS存取
   - 使用工作方法
   - 視需要顯示設定指示

   或手動（如果您知道自己的Git已設定）：

   ```bash
   git submodule update --init --recursive
   ```

3. 完成！✨

## 驗證

安裝之後，請確認安裝：

```bash
ls .cursor-agents/agents/
```

您應會看到：
- `draft-page-generator.md`
- `fix-grammar.md`
- 等

## 使用方式

安裝之後，您便可以使用游標中的代理程式：

```
@draft-page      # Generate a new documentation page
@fix-grammar     # Fix grammar in current file
```

請參閱[AGENTS.md](AGENTS.md)以取得可用代理程式的完整清單。

## 更新代理程式

若要取得所有代理程式的最新版本：

### 選項1：使用游標

```
@update-agents
```

### 選項2：使用終端機

```bash
git submodule update --remote
```

## 疑難排解

### 「找不到代理程式」錯誤

如果您看到此錯誤，表示尚未安裝代理程式。 執行：

```
@setup-agents
```

### 子模組是空的

如果`.cursor-agents/`存在但空白：

```bash
git submodule update --init --recursive --remote
```

### 權限遭拒

確定安裝程式指令碼為可執行檔：

```bash
chmod +x setup-agents.sh
```

### 網路/VPN問題

- 確保您已連線至Adobe VPN
- 檢查網路連線
- 驗證Git存取權：

  ```bash
  git ls-remote https://git.corp.adobe.com/AdobeDocs/CursorAgents
  ```

## 運作方式

資料指標代理程式會以&#x200B;**Git子模組**&#x200B;的形式分佈：

```
your-repo/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  └── your-content/
```

子模組指向：
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

這可確保每個人都使用相同的、最新的代理程式。

## 適用於維護者

### 新增至新存放庫

1. 新增子模組：

   ```bash
   git submodule add https://git.corp.adobe.com/AdobeDocs/CursorAgents.git .cursor-agents
   ```

2. 複製安裝檔案：
   - `setup-agents.sh`
   - `setup-agent.md` （置於根中，而非子模組中）
   - `INSTALL.md`

3. 認可：

   ```bash
   git add .gitmodules .cursor-agents setup-agents.sh
   git commit -m "Add Cursor Agents submodule"
   ```

### 更新中央存放庫

應在下列位置變更代理程式：
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

所有存放庫都將透過`git submodule update --remote`接收更新。

---

**需要協助嗎？**&#x200B;請連絡您的檔案團隊負責人或檢視內部Wiki。
