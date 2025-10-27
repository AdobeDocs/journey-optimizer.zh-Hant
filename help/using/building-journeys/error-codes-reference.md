---
solution: Journey Optimizer
product: journey optimizer
title: 錯誤代碼參考
description: 瞭解Adobe Journey Optimizer中的常見錯誤代碼以及如何疑難排解
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
keywords: 錯誤，程式碼，疑難排解，歷程，行銷活動，訊息
source-git-commit: 012efffe4b38ccfdc88545566bc49b519c796ad2
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 1%

---


# 錯誤代碼參考 {#error-codes}

Adobe Journey Optimizer使用標準化的錯誤代碼，協助您快速識別並解決歷程、行銷活動和訊息設定中的問題。 瞭解這些錯誤代碼可以大幅減少疑難排解時間，並幫助您維持最佳行銷活動效能。

## 瞭解錯誤代碼結構 {#error-code-structure}

Adobe Journey Optimizer錯誤代碼遵循一致的命名模式，這有助於識別元件和問題型別：

* **服務首碼**：指出產生錯誤的Adobe Journey Optimizer服務（例如，推播/傳輸服務的CJMPTS、歷程執行階段的CJMRT、訊息編寫服務的CJMMAS）
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
| **CJMPTS-1510-500** | 推播頻道傳送時出現內部伺服器錯誤 | 後端推播/傳輸故障；提供者或基礎結構錯誤 | 1.檢查頻道布建設定<br/>2。 確認推送認證有效<br/>3。 請重試操作<br/>4。 若為持續性，請連絡Adobe支援並提供請求ID <br/><br/>**相關檔案**： [推播設定](../push/push-configuration.md) |
| **CJMPTS-1023-500** | 推播傳送/處理期間發生內部伺服器錯誤（協力廠商閘道） | 暫時性雲端故障或未知的服務錯誤 | 1.驗證提供者/通道組態<br/>2。 檢查第三方閘道狀態<br/>3。 請在幾分鐘後重試<br/>4。 檢視其他內容&#x200B;<br/><br/>**相關檔案的記錄檔**： [推播通知](../push/create-push.md) |
| **CJMPTS-1310-500** | 來自轉譯服務的內部錯誤（預覽或即時傳送） | 下游範本轉譯器失敗，通常是由於JSON/範本語法問題 | 1.驗證範本語法和結構<br/>2。 檢查所有個人化變數是否有效<br/>3。 使用測試裝載來識別問題<br/>4。 視需要簡化範本複雜度&#x200B;<br/><br/>**相關檔案**： [訊息範本](../content-management/content-templates.md)，[Personalization語法](../personalization/personalization-syntax.md) |

### CJMRT：Journey Runtime和API錯誤 {#cjmrt-errors}

這些錯誤會在歷程執行、事件處理和API作業期間發生。

| 錯誤碼 | 說明 | 根本原因 | 解決方法 |
|------------|-------------|-----------|-----------|
| **CJMRT-030012-422** | 無法處理的實體 — 動作失敗、事件無效或裝載錯誤 | 無效的輸入資料（例如，不存在的對象、事件或屬性） | 1.仔細檢查輸入/事件裝載結構<br/>2。 驗證參考的物件（對象、資料集）存在且作用中<br/>3。 驗證所有必要欄位是否存在<br/>4。 使用已知良好的承載進行測試&#x200B;<br/><br/>**相關檔案**： [歷程疑難排解](troubleshooting.md)，[事件組態](../event/about-events.md) |
| **CJMRT-130004-400** | 錯誤請求 — 歷程節點或頻道設定中的輸入格式錯誤 | 歷程裝載或設定參考已移除/無效的資源 | 1.檢閱歷程節點組態<br/>2。 驗證所有參考的資源（訊息、對象、動作）是否存在<br/>3。 修正或更新中斷的參照<br/>4。 必要時重新建置歷程設定&#x200B;<br/><br/>**相關檔案**： [歷程建立](journey-gs.md)，[自訂動作](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | 衝突 — 資源已存在 | 嘗試建立具有重複ID或名稱的資源 | 1.對所有資源使用唯一識別碼和名稱<br/>2。 檢查具有相同識別碼<br/>3的現有資源。 刪除或重新命名衝突的物件<br/>4。 檢閱命名慣例&#x200B;<br/><br/>**相關檔案**： [歷程版本](journey-gs.md#journey-versions) |
| **CJMRT-170016-400** | 歷程設定/預覽期間發生錯誤請求 | 承載缺少必要的相依性或損壞的範本連結 | 1.驗證所有必要資源是否為使用中<br/>2。 請確定範本和內容區塊已發佈<br/>3。 檢查所有相依性已正確連結<br/>4。 檢閱歷程測試模式結果&#x200B;<br/><br/>**相關檔案**： [測試歷程](testing-the-journey.md)，[歷程相依性](journey-gs.md) |
| **CJMRT-080608-400** | 網域/頻道/委派中的錯誤請求 | 缺少必要的DNS記錄或電子郵件/簡訊設定 | 1.完成電子郵件網域<br/>2的DNS設定。 確認子網域委派已完成<br/>3。 再次執行組態精靈<br/>4。 允許DNS傳播的時間（最長72小時）<br/><br/>**相關檔案**： [頻道介面](../configuration/channel-surfaces.md)，[子網域委派](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | 承載上的內部錯誤 | 後端資料/設定錯誤或不支援的設定 | 1.重試操作<br/>2。 若使用進階功能，則簡化設定<br/>3。 使用請求ID和確切的承載<br/>4向上呈報至Adobe支援。 檢視發行說明&#x200B;<br/><br/>**相關檔案**&#x200B;中的已知問題： [歷程疑難排解](troubleshooting.md) |

### CJMAS：訊息編寫服務錯誤 {#cjmmas-errors}

建立、編輯或發佈訊息、預設集和內容時，就會發生這些錯誤。

| 錯誤碼 | 說明 | 根本原因 | 解決方法 |
|------------|-------------|-----------|-----------|
| **CJMMAS-1149-400** | 儲存訊息、預設集或變體時發生錯誤請求 | 訊息中缺少必填欄位或設定錯誤 | 1.完成所有必要欄位（標示星號）<br/>2。 驗證訊息/預設集組態<br/>3。 檢查欄位值格式和限制<br/>4。 檢閱UI <br/><br/>**相關檔案**&#x200B;中的驗證訊息： [電子郵件頻道](../email/get-started-email.md)，[頻道介面](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | 訊息預設集編輯中無法處理的實體 | 驗證錯誤、不支援的欄位或不正確的語法 | 1.更正語法/欄位錯誤，如指示所示<br/>2。 與已知良好組態比較<br/>3。 在儲存<br/>4之前使用訊息UI驗證。 檢閱檔案&#x200B;<br/><br/>**相關檔案**&#x200B;中的欄位需求： [訊息預設集](../configuration/channel-surfaces.md)，[電子郵件設定](../email/email-settings.md) |
| **CJMMAS-1300-500** | 訊息製作發生內部錯誤 | 因基礎建設問題、大型內容或服務停機造成後端當機 | 1.簡化範本/內容（減少大小/複雜性）<br/>2。 請重試操作<br/>3。 逐步儲存工作<br/>4。 若為持續性，請升級至Adobe支援&#x200B;<br/><br/>**相關檔案**： [內容範本](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | 成功狀態但錯誤橫幅：選擇退出連結遺失 | 電子郵件變體缺少必要的取消訂閱連結 | 1.將選擇退出/取消訂閱連結新增至所有電子郵件變體<br/>2。 確定每個語言版本<br/>3都有連結。 使用個人化協助程式插入選擇退出連結<br/>4。 請先測試所有變體，再發佈&#x200B;<br/><br/>**相關檔案**： [選擇退出管理](../privacy/opt-out.md)，[電子郵件設計](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | 更新/發佈範本或預設集時禁止 | 使用者缺少必要的許可權/角色，或目前狀態不允許動作 | 1.確認使用者具有適當許可權（訊息管理員、作者等）<br/>2. 檢查預設集/範本狀態（草稿、已發佈、已封存）<br/>3。 如有需要，請要求系統管理員提供存取權<br/>4。 檢閱產品設定檔指派&#x200B;<br/><br/>**相關檔案**： [許可權](../administration/permissions.md)，[存取控制](../administration/permissions-overview.md) |

### CJMCMP：行銷活動錯誤 {#cjmcmp-errors}

這些錯誤會在行銷活動建立、設定和啟動期間發生。

| 錯誤碼 | 說明 | 根本原因 | 解決方法 |
|------------|-------------|-----------|-----------|
| **CJMCMP-2050-400** | 行銷活動啟動或核准中的錯誤請求 | 行銷活動參考無效/缺少原則或區段 | 1.稽核所有行銷活動節點設定<br/>2。 確認原則/區段連結為最新且有效<br/>3。 以正確的組態更新<br/>4。 在啟用之前重新測試行銷活動&#x200B;<br/><br/>**相關檔案**： [行銷活動建立](../campaigns/create-campaign.md)，[行銷活動核准](../test-approve/gs-approval.md) |

## 一般疑難排解方法 {#troubleshooting-approach}

遇到錯誤碼時，請遵循此系統化方法：

1. **識別錯誤**：請注意完整的錯誤碼、HTTP狀態以及任何隨附的訊息或要求識別碼。

2. **尋找服務**：使用服務首碼(CJMPTS、CJMRT、CJMMAS、CJMCMP)來識別受影響的元件。

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

* **驗證所有資源**：確認所有參考的對象、資料來源和自訂動作都有效
* **徹底測試**：使用測試模式在發佈之前識別問題（[瞭解更多](testing-the-journey.md)）
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

