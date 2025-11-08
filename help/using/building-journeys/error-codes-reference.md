---
solution: Journey Optimizer
product: journey optimizer
title: 錯誤代碼參考
description: 瞭解Adobe Journey Optimizer中的常見錯誤代碼以及如何疑難排解
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: 錯誤，程式碼，疑難排解，歷程，行銷活動，訊息
source-git-commit: 7a83bb558559ba814ed9431bb85a68929a276ed5
workflow-type: tm+mt
source-wordcount: '2394'
ht-degree: 1%

---


# 錯誤代碼參考 {#error-codes}

Adobe Journey Optimizer使用標準化的錯誤代碼，協助您快速識別並解決歷程、行銷活動和訊息設定中的問題。 瞭解這些錯誤代碼可以大幅減少疑難排解時間，並幫助您維持最佳行銷活動效能。

## 瞭解錯誤代碼結構 {#error-code-structure}

Adobe Journey Optimizer錯誤代碼遵循一致的命名模式，這有助於識別元件和問題型別：

* **服務前置詞**：指出產生錯誤的Adobe Journey Optimizer服務（例如，推播/傳輸服務的CJMPTS、歷程執行階段的CJMRT、訊息編寫服務的CJMMAS、促銷活動的CJMCMP、傳輸層的CJMTL、報告/布建服務的CJMRPS）
* **錯誤號碼**：特定錯誤條件的唯一識別碼
* **HTTP狀態碼**：標準HTTP狀態碼（例如400、403、422、500）

範例： `CJMRT-030012-422`指出錯誤碼為030012且HTTP狀態為422 （無法處理的實體）的Journey Runtime錯誤(CJMRT)。

## 錯誤碼的尋找位置 {#find-error-codes}

錯誤代碼會顯示在Adobe Journey Optimizer內的數個位置：

* 歷程執行報告和記錄
* Campaign啟用畫面
* 訊息驗證警告
* 系統通知和警示
* API回應（使用REST API時）

發生錯誤時，請注意完整的錯誤代碼以及隨附的任何請求ID，因為這些對於疑難排解和支援升級是必要的。

## 依服務的常見錯誤代碼 {#error-codes-by-service}

### CJMPTS：推送和傳輸服務錯誤 {#cjmpts-errors}

這些錯誤會在推播通知傳送和訊息傳輸作業期間發生。

| 錯誤碼 | 說明 | 根本原因 | 解決方法 |
|------------|-------------|-----------|-----------|
| **CJMPTS-1410-500** | 推播/頻道傳送動作的內部伺服器錯誤 | 管道後端中斷、憑證過期、設定錯誤或提供者錯誤 | 1.延遲後重試<br/>2。 檢查提供者設定和配額<br/>3。 確認推送認證有效<br/>4。 使用替代通道<br/>5進行測試。 若為持續性，請連絡Adobe支援並提供請求ID <br/><br/>**相關檔案**： [推播設定](../push/push-configuration.md) |
| **CJMPTS-1006-404** | 推播/簡訊失敗，顯示「找不到資源」 | 參考的提供者/頻道不存在、拼字錯誤或已取消布建 | 1.檢閱並修正提供者/頻道參考資料和ID<br/>2。 稽核沙箱/組織組態<br/>3。 驗證通道組態是否有效<br/>4。 如有必要，請重新建立管道設定&#x200B;<br/><br/>**相關檔案**： [管道表面](../configuration/channel-surfaces.md) |
| **CJMPTS-1510-500** | 推播頻道傳送時出現內部伺服器錯誤 | 後端推播/傳輸故障；提供者或基礎結構錯誤 | 1.檢查頻道布建設定<br/>2。 確認推送認證有效<br/>3。 請重試操作<br/>4。 若為持續性，請連絡Adobe支援並提供請求ID <br/><br/>**相關檔案**： [推播設定](../push/push-configuration.md) |
| **CJMPTS-1023-500** | 推播傳送/處理期間發生內部伺服器錯誤（協力廠商閘道） | 暫時性雲端故障或未知的服務錯誤 | 1.驗證提供者/通道組態<br/>2。 檢查第三方閘道狀態<br/>3。 請在幾分鐘後重試<br/>4。 檢視其他內容&#x200B;<br/><br/>**相關檔案的記錄檔**： [推播通知](../push/create-push.md) |
| **CJMPTS-1310-500** | 來自轉譯服務的內部錯誤（預覽或即時傳送） | 下游範本轉譯器失敗，通常是由於JSON/範本語法問題 | 1.驗證範本語法和結構<br/>2。 檢查所有個人化變數是否有效<br/>3。 使用測試裝載來識別問題<br/>4。 視需要簡化範本複雜度&#x200B;<br/><br/>**相關檔案**： [訊息範本](../content-management/content-templates.md)，[Personalization語法](../personalization/personalization-syntax.md) |

### CJMRT：Journey Runtime和API錯誤 {#cjmrt-errors}

這些錯誤會在歷程執行、事件處理和API作業期間發生。

| 錯誤碼 | 說明 | 根本原因 | 解決方法 |
|------------|-------------|-----------|-----------|
| **CJMRT-110001-500** | 超過工作流程步驟的最大執行次數（例如IP相似性布建步驟逾時） | 工作流程/布建工作未在允許的重試/時間內完成，通常是因為基礎架構/服務延遲或暫時性後端問題 | 1.請稍後再試<br/>2。 檢查[Adobe狀態](https://status.adobe.com/)是否有中斷情形<br/>3。 透過工作流程/工作/組織詳細資訊<br/>4向上呈報至Adobe支援。 提供記錄檔和網路擷取（若有）<br/><br/>**相關檔案**： [歷程疑難排解](troubleshooting.md) |
| **CJMRT-000071-400** | 歷程/測試事件或API呼叫期間的錯誤請求 | 裝載/引數格式錯誤或遺失；輸入參考不存在的或非使用中的資源 | 1.檢閱要求內文以取得錯誤詳細資料<br/>2。 正確的參考/引數<br/>3。 請移除進階組態並重試<br/>4。 逐一新增功能以識別問題&#x200B;<br/><br/>**相關檔案**： [歷程疑難排解](troubleshooting.md)，[事件組態](../event/about-events.md) |
| **CJMRT-000013-401** | 訊息執行階段作業/API事件期間發生未獲授權的錯誤 | 驗證失敗： Token已到期、缺少許可權，或整合/使用者已失去環境存取權 | 1.驗證許可權和角色<br/>2。 重新整理驗證Token<br/>3。 使用已知有效的使用者/服務帳戶<br/>4。 檢閱產品設定檔指派&#x200B;<br/><br/>**相關檔案**： [許可權](../administration/permissions.md) |
| **CJMRT-080605-400** | 來自歷程執行階段的錯誤請求（例如，節點觸發器、動作等） | 設定會參考已移除/重新命名或過時的功能/範本/頻道 | 1.驗證所有資源參考<br/>2。 稽核歷程組態和功能旗標<br/>3。 更新中斷的參考<br/>4。 檢閱最近的系統更新和移轉&#x200B;<br/><br/>**相關檔案**： [歷程建立](journey-gs.md) |
| **CJMRT-030012-422** | 無法處理的實體 — 動作失敗、事件無效或裝載錯誤 | 無效的輸入資料（例如，不存在的對象、事件或屬性） | 1.仔細檢查輸入/事件裝載結構<br/>2。 驗證參考的物件（對象、資料集）存在且作用中<br/>3。 驗證所有必要欄位是否存在<br/>4。 使用已知良好的承載進行測試&#x200B;<br/><br/>**相關檔案**： [歷程疑難排解](troubleshooting.md)，[事件組態](../event/about-events.md) |
| **CJMRT-130004-400** | 錯誤請求 — 歷程節點或頻道設定中的輸入格式錯誤 | 歷程裝載或設定參考已移除/無效的資源 | 1.檢閱歷程節點組態<br/>2。 驗證所有參考的資源（訊息、對象、動作）是否存在<br/>3。 修正或更新中斷的參照<br/>4。 必要時重新建置歷程設定&#x200B;<br/><br/>**相關檔案**： [歷程建立](journey-gs.md)，[自訂動作](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | 衝突 — 資源已存在 | 嘗試建立具有重複ID或名稱的資源 | 1.對所有資源使用唯一識別碼和名稱<br/>2。 檢查具有相同識別碼<br/>3的現有資源。 刪除或重新命名衝突的物件<br/>4。 檢閱命名慣例&#x200B;<br/><br/>**相關檔案**： [歷程建立](journey-gs.md) |
| **CJMRT-170016-400** | 歷程設定/預覽期間發生錯誤請求 | 承載缺少必要的相依性或損壞的範本連結 | 1.驗證所有必要資源是否為使用中<br/>2。 請確定範本和內容區塊已發佈<br/>3。 檢查所有相依性已正確連結<br/>4。 檢閱歷程測試模式結果&#x200B;<br/><br/>**相關檔案**： [測試歷程](testing-the-journey.md)，[歷程相依性](journey-gs.md) |
| **CJMRT-080608-400** | 網域/頻道/委派中的錯誤請求 | 缺少必要的DNS記錄或電子郵件/簡訊設定 | 1.完成電子郵件網域<br/>2的DNS設定。 確認子網域委派已完成<br/>3。 再次執行組態精靈<br/>4。 允許DNS傳播的時間（最長72小時）<br/><br/>**相關檔案**： [頻道介面](../configuration/channel-surfaces.md)，[子網域委派](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | 承載上的內部錯誤 | 後端資料/設定錯誤或不支援的設定 | 1.重試操作<br/>2。 若使用進階功能，則簡化設定<br/>3。 使用請求ID和確切的承載<br/>4向上呈報至Adobe支援。 檢視發行說明&#x200B;<br/><br/>**相關檔案**&#x200B;中的已知問題： [歷程疑難排解](troubleshooting.md) |

### CJMAS：訊息編寫服務錯誤 {#cjmmas-errors}

建立、編輯或發佈訊息、預設集和內容時，就會發生這些錯誤。

| 錯誤碼 | 說明 | 根本原因 | 解決方法 |
|------------|-------------|-----------|-----------|
| **CJMMAS-1732-500** | 校訂失敗 — 使用AEM資產傳送校訂/測試時所有資產未發佈 | 最近發佈的資產尚未在AJO中；資產ID不相符；跨存放庫使用；AEM同步延遲 | 1.僅使用來自正確存放庫/環境的已發佈資產ID<br/>2。 留出時間在AEM與AJO<br/>3之間同步。 請使用已知良好的資產<br/>4重試。 在AEM <br/><br/>**相關檔案**&#x200B;中驗證資產發佈狀態： [Assets整合](../integrations/assets.md) |
| **CJMMAS-1069-500** | 儲存或發佈訊息範本時發生內部錯誤 | 後端例外狀況（基礎架構/服務錯誤或內容問題）；不支援的標籤/功能 | 1.簡化或降低範本複雜度<br/>2。 以累加步驟重新新增內容以識別問題<br/>3。 檢查[Adobe狀態頁面](https://status.adobe.com/)<br/>4。 移除不支援的功能或標籤&#x200B;<br/><br/>**相關檔案**： [內容範本](../content-management/content-templates.md) |
| **CJMMAS-1149-400** | 儲存訊息、預設集或變體時發生錯誤請求 | 訊息中缺少必填欄位或設定錯誤 | 1.完成所有必要欄位（標示星號）<br/>2。 驗證訊息/預設集組態<br/>3。 檢查欄位值格式和限制<br/>4。 檢閱UI <br/><br/>**相關檔案**&#x200B;中的驗證訊息： [電子郵件頻道](../email/get-started-email.md)，[頻道介面](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | 訊息預設集編輯中無法處理的實體 | 驗證錯誤、不支援的欄位或不正確的語法 | 1.更正語法/欄位錯誤，如指示所示<br/>2。 與已知良好組態比較<br/>3。 在儲存<br/>4之前使用訊息UI驗證。 檢閱檔案&#x200B;<br/><br/>**相關檔案**&#x200B;中的欄位需求： [訊息預設集](../configuration/channel-surfaces.md)，[電子郵件設定](../email/email-settings.md) |
| **CJMMAS-1300-500** | 訊息製作發生內部錯誤 | 因基礎建設問題、大型內容或服務停機造成後端當機 | 1.簡化範本/內容（減少大小/複雜性）<br/>2。 請重試操作<br/>3。 逐步儲存工作<br/>4。 若為持續性，請升級至Adobe支援&#x200B;<br/><br/>**相關檔案**： [內容範本](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | 成功狀態但錯誤橫幅：選擇退出連結遺失 | 電子郵件變體缺少必要的取消訂閱連結 | 1.將選擇退出/取消訂閱連結新增至所有電子郵件變體<br/>2。 確定每個語言版本<br/>3都有連結。 使用個人化協助程式插入選擇退出連結<br/>4。 請先測試所有變體，再發佈&#x200B;<br/><br/>**相關檔案**： [選擇退出管理](../privacy/opt-out.md)，[電子郵件設計](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | 更新/發佈範本或預設集時禁止 | 使用者缺少必要的許可權/角色，或目前狀態不允許動作 | 1.確認使用者具有適當許可權（訊息管理員、作者等）<br/>2. 檢查預設集/範本狀態（草稿、已發佈、已封存）<br/>3。 如有需要，請要求系統管理員提供存取權<br/>4。 檢閱產品設定檔指派&#x200B;<br/><br/>**相關檔案**： [許可權](../administration/permissions.md)，[存取控制](../administration/permissions-overview.md) |

### CJMCMP：行銷活動錯誤 {#cjmcmp-errors}

這些錯誤會在行銷活動建立、設定和啟動期間發生。

| 錯誤碼 | 說明 | 根本原因 | 解決方法 |
|------------|-------------|-----------|-----------|
| **CJMCMP-6003-400** | 發佈/測試模式歷程/訊息時，「至少有一個不正確的行銷活動」 | 節點參考了遺失、未發佈或無效的行銷活動；舊版或複製歷程未建立內嵌 | 1.開啟每個訊息節點並驗證組態<br/>2。 重新連結或重新新增訊息節點<br/>3。 啟動測試模式以強制建立內嵌行銷活動<br/>4。 如果問題頻繁發生，請移至新歷程精靈&#x200B;<br/><br/>**相關檔案**： [歷程建立](journey-gs.md)，[測試歷程](testing-the-journey.md) |
| **CJMCMP-2003-400** | UI橫幅：電子郵件Designer中的「實驗不正確」 | 實驗/資料提供者過時或遺失；實驗清理失敗、結構描述不符或UI驗證Bug | 1.移除未使用的實驗欄位<br/>2。 驗證結構描述和資料提供者連線<br/>3。 重新載入UI並清除瀏覽器快取<br/>4。 如果問題尚未解決，請重新建立節點/電子郵件&#x200B;<br/><br/>**相關檔案**： [內容實驗](../content-management/content-experiment.md) |
| **CJMCMP-3001-400** | 模擬/預覽「不正確的表面型別篩選器」 | 使用舊版結構建置的節點會傳送type=surfaceId，後端需要brandingPresetId | 1.刪除並重新建立受影響的節點<br/>2。 使用新的歷程版本/範本<br/>3。 使用測試模式來清除組態<br/>4。 如果問題很普遍，請大量重新建立節點&#x200B;<br/><br/>**相關檔案**： [頻道介面](../configuration/channel-surfaces.md)，[訊息模擬](../content-management/preview.md) |
| **CJMCMP-2050-400** | 行銷活動啟動或核准中的錯誤請求 | 行銷活動參考無效/缺少原則或區段 | 1.稽核所有行銷活動節點設定<br/>2。 確認原則/區段連結為最新且有效<br/>3。 以正確的組態更新<br/>4。 在啟用之前重新測試行銷活動&#x200B;<br/><br/>**相關檔案**： [行銷活動建立](../campaigns/create-campaign.md)，[行銷活動核准](../test-approve/gs-approval.md) |

### CJMTL：傳輸層錯誤 {#cjmtl-errors}

這些錯誤會在郵件傳輸和傳遞作業期間發生。

| 錯誤碼 | 說明 | 根本原因 | 解決方法 |
|------------|-------------|-----------|-----------|
| **CJMTL-010018-422** | 儲存/傳送內容時，「網域名稱中不允許使用Personalization」 | 過於嚴格的驗證會暫時中斷動態href網域個人化 | 1.如果使用網域變數，則重構連結<br/>2。 請確認使用最新的AJO版本<br/>3。 請重試操作<br/>4。 如果問題仍然存在，請使用靜態網域&#x200B;<br/><br/>**相關檔案**： [Personalization語法](../personalization/personalization-syntax.md)，[電子郵件設計](../email/content-from-scratch.md) |
| **CJMTL-010011-422** | 無法處理的實體 — 推播/簡訊/電子郵件傳送失敗，顯示「無效欄位」 | 承載或收件者/聯絡資料遺失或無效 | 1.檢查特定欄位錯誤的記錄檔<br/>2。 修正設定檔/連絡資訊<br/>3。 使用測試設定檔<br/>4進行驗證。 視需要重構裝載格式&#x200B;<br/><br/>**相關檔案**： [設定檔管理](../audience/get-started-profiles.md)，[測試設定檔](../audience/creating-test-profiles.md) |

### CJMRPS：報表與布建服務錯誤 {#cjmrps-errors}

這些錯誤會在報告設定和資料集布建作業期間發生。

| 錯誤碼 | 說明 | 根本原因 | 解決方法 |
|------------|-------------|-----------|-----------|
| **CJMRPS-1047-409** | 「衝突。 新增報表資料集時，資料集已經新增 | 嘗試新增已布建的資料集 | 1.檢閱報告設定中的資料集組態<br/>2。 不要重新新增已經存在的資料集<br/>3。 使用正式移轉檢查清單來報告移轉<br/>4。 移除重複的資料集參考&#x200B;<br/><br/>**相關檔案**： [報告總覽](../reports/gs-reports.md)、[行銷活動報告](../reports/campaign-global-report-cja.md)、[歷程報告](../reports/journey-global-report-cja.md) |

## 一般疑難排解方法 {#troubleshooting-approach}

遇到錯誤碼時，請遵循此系統化方法：

1. **識別錯誤**：請注意完整的錯誤碼、HTTP狀態以及任何隨附的訊息或要求識別碼。

2. **尋找服務**：使用服務首碼(CJMPTS、CJMRT、CJMMAS、CJMCMP、CJMTL、CJMRPS)來識別受影響的元件。

3. **檢查狀態碼**：
   * **400 （錯誤請求）**：檢閱輸入資料和設定
   * **403 （禁止）**：檢查許可權和存取權
   * **409 （衝突）**：尋找重複或衝突的資源
   * **422 （無法處理的實體）**：根據結構描述需求驗證資料
   * **500 （內部伺服器錯誤）**：重試並可能升級至支援

4. **檢閱最近的變更**：考慮最近修改的內容（歷程更新、新的行銷活動、設定變更等）。

5. **諮詢檔案**：使用本指南中提供的連結，存取受影響功能的詳細檔案。

6. **在適當時重試**：對於500系列錯誤，幾分鐘後簡單的重試通常可解決暫時性問題。

7. **必要時上報**：如果在執行解決步驟後錯誤仍然存在，請聯絡Adobe支援：
   * 完成錯誤代碼
   * 請求ID （若有）
   * 要再現的步驟
   * 相關設定詳細資料

## 避免常見錯誤的最佳實務 {#best-practices}

### 在歷程啟用之前 {#journey-best-practices}

* **驗證所有資源**：確認所有參考的對象、事件、資料來源和自訂動作均已正確設定
* **徹底測試**：使用測試模式在發佈之前識別問題（[瞭解更多](testing-the-journey.md)）
* **驗證磁碟區**：在上線之前，先試執行以驗證對象觸及範圍和分支邏輯（[深入瞭解](journey-dry-run.md)）
* **檢查許可權**：確認您擁有所有元件必要的存取許可權
* **檢閱相依性**：確認所有連結的訊息和內容均已發佈

### 建立訊息時 {#message-best-practices}

* **完成必填欄位**：儲存前請一律填寫所有必填欄位
* **包含選擇退出連結**：新增取消訂閱連結至所有電子郵件變體（[深入瞭解](../privacy/opt-out.md)）
* **驗證個人化**：使用範例設定檔測試所有動態內容（[深入瞭解](../personalization/personalization-build-expressions.md)）
* **讓範本保持在可管理狀態**：避免過於複雜的範本可能導致轉譯問題

### 用於行銷活動管理 {#campaign-best-practices}

* **驗證對象資料**：確定目標對象已正確設定並填入
* **檢查核准狀態**：在嘗試啟用之前，請先瞭解核准需求（[深入瞭解](../test-approve/gs-approval.md)）
* **監視設定**：定期檢閱頻道介面和預設集的有效性
* **計畫DNS變更**：在更新網域時允許DNS傳播足夠的時間

## 其他資源 {#additional-resources}

* [歷程疑難排解](troubleshooting.md)
* [執行疑難排解](troubleshooting-execution.md)
* [傳入活動疑難排解](troubleshooting-inbound.md)
* [自訂動作疑難排解](../action/troubleshoot-custom-action.md)
* [歷程常見問答](journey-faq.md)
* [護欄與限制](../start/guardrails.md)

## 取得支援 {#getting-support}

如果您遇到無法使用此指南解決的持續錯誤：

1. **收集資訊**：收集錯誤碼、請求ID、時間戳記和要再現的步驟
2. **檢查系統狀態**：造訪[Adobe狀態](https://status.adobe.com/){target="_blank"}瞭解已知的服務問題
3. **搜尋檔案**：檢閱[Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=zh-Hant){target="_blank"}以瞭解解決方案
4. **參與社群**：在[Adobe Journey Optimizer社群](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}中發佈問題
5. **聯絡Adobe支援**：提交支援票證並附上所有相關詳細資料

>[!NOTE]
>
>當識別並記錄新程式碼時，此錯誤碼參考會持續更新。 如需最新資訊，請定期檢視[Adobe Journey Optimizer社群部落格](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs){target="_blank"}。

**相關主題**

* [揭露Adobe Journey Optimizer錯誤碼：第1部分](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884){target="_blank"}
* [揭露Adobe Journey Optimizer錯誤碼：第2部分](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661){target="_blank"}

