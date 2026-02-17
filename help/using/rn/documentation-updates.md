---
solution: Journey Optimizer
product: journey optimizer
title: 文件更新
description: 瞭解最新的文件更新
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 7cfeabc85b9645be9d61ed6458e57e42ea319619
workflow-type: tm+mt
source-wordcount: '3330'
ht-degree: 84%

---

# 文件更新 {#latest-updates}

此頁面列出 [!DNL Journey Optimizer] 文件中的所有最新變更，以及與每月發行功能和改進相關的更新。

## 2026 年 2 月 {#february-2026}

* 「外部系統整合」頁面已更新自訂資料來源和自訂動作的連結，並澄清輸出Proxy為從&#x200B;**自訂動作**&#x200B;到外部系統的輸出呼叫提供靜態IP。 [閱讀全文](../configuration/external-systems.md)

* 歷程試用檔案已釐清：步驟事件屬性`inDryRun`和`dryRunID`現在會記錄他們在試用模式時傳回`true`/執行個體ID，並在測試或即時歷程中傳回`null`。 已更新報告查詢中排除練習步驟事件的指引。 [閱讀全文](../building-journeys/journey-dry-run.md)

* **網頁推播**&#x200B;現已正式可用。 推播通知檔案已重組並據此更新（開始、設計、傳送、建立）。 [閱讀全文](../push/get-started-push.md)

* 網頁推播設定頁面現在可在檔案中取得。 [閱讀全文](../push/push-configuration-web.md)

* 更新有關在決策中使用片段的檔案：「片段」及「決策」區段中已新增附註，且「決策」政策頁面中的「片段」已更新。 [閱讀全文](../experience-decisioning/fragments-decision-policies.md)

* SMS webhook檔案已更新： Twilio webhook內容已移除。 [閱讀全文](../sms/sms-webhook.md)

* 更新Decisioning移轉API檔案。 [閱讀全文](../experience-decisioning/decisioning-migration-api.md)

* **內容決定**&#x200B;活動現已正式可用。 內容決定活動頁面已更新，其中包含步驟事件中可用的決定資料區段。 [閱讀全文](../building-journeys/content-decision.md)

* 「忠誠度挑戰」章節新增了忠誠度挑戰API檔案的連結（開始使用、建立挑戰、建立任務、存取忠誠度挑戰）。 [閱讀全文](../loyalty-challenges/get-started.md)

* 行銷活動建立精靈檔案中的支援管道資訊已更正。 「開始使用管道」和「協調的行銷活動常見問題集」頁面已更新相應內容。 [閱讀全文](../campaigns/get-started-with-campaigns.md)

* 已更正&#x200B;**歷程管理**&#x200B;和&#x200B;**核准**&#x200B;許可權的許可權檔案。 [閱讀全文](../administration/ootb-permissions.md)

* 更新AEM (Adobe Experience Manager)整合檔案，其中包含修訂命名(AEM動態內容和AEM片段)。 [閱讀全文](../integrations/aem-fragments.md)

* 排除清單中已新增排除原因： **UnsubscribeLinkNotValid** (錯誤碼050081)。 當List-Unsubscribe mailTo主旨長度大於RFC的998個字元限制時，會產生此排除。 [閱讀全文](../reports/exclusion-list.md)

* formatDate協助程式函式檔案已增強，其中指出該函式需要日期時間欄位型別（而非字串），並且提供多個範例：格式化日期時間欄位、將字串轉換為日期優先、具有日期名稱的完整日期、來自系統時間的動態日期，以及包含小寫輸出的星期幾格式。 [閱讀全文](../personalization/functions/dates.md#format-date)

* 文字版本的電子郵件檔案已增強，並具備完整的使用案例指引，包括何時使用自訂純文字與自動同步的決定標準、真實案例的實用範例，以及包含常見問題的常見問題集區段。 [閱讀全文](../email/text-version-email.md#when-to-use)

* 「執行中繼資料協助程式」檔案新增了一項限制，明確說明不會為動作中排除的設定檔擷取中繼資料。 [閱讀全文](../personalization/functions/helpers.md#execution-metadata)

* 更新程式碼型實施範例檔案，在propositionAction中加入Token欄位，以便在Decisioning中準確追蹤和歸因。 [閱讀全文](../code-based/code-based-implementation-samples.md#client-side-how)

* 已在URL追蹤和清單取消訂閱檔案中新增附註，以澄清URL附加至URL的追蹤引數順序是隨機且無法控制。 [閱讀全文](../email/url-tracking.md)

* 電子郵件Designer主題檔案已更新，其中包含有關網頁字型支援限制和備援字型重要性的資訊。 [閱讀全文](../email/apply-email-themes.md#themes-guardrails)

## 2026 年 1 月 {#january-2026}

* 授權使用儀表板檔案已用有關&#x200B;**可參與設定檔**&#x200B;的更新指南澄清，包括定義詳細資訊和疑難排解指南。 [閱讀全文](../audience/license-usage.md#what-is-engageable-profile)

* 已在電子郵件Designer主題檔案中新增附註，以釐清Web字型支援限制。 [閱讀全文](../email/apply-email-themes.md#themes-guardrails)

* 已在文件歷程承載大小驗證中新增護欄區段，包括警告和錯誤臨界值，以及如何最佳化歷程的指引。[閱讀全文](../start/guardrails.md#journey-payload-size)

* 已更新決策護欄文件，以新增決策項目大小限制 (對於包含最多 30 個屬性的項目，為 1KB)。[閱讀全文](../experience-decisioning/decisioning-guardrails.md)

* 已在決策原則建立文件中新增附註，以告知使用者一旦建立決策原則，任何變更最多可能需要 15 分鐘傳播至所有資料區域，而加拿大最多可能需要 30 分鐘。[閱讀全文](../experience-decisioning/create-decision-policy.md#review)

* 片段文件中已新增附註，以警告當片段中的按鈕標籤和 URL 都可編輯時，追蹤資料集會記錄 URL 值，而非標籤值。[閱讀全文](../content-management/customizable-fragments.md#visual)

* 推出新的頁面，說明從決策管理移轉至決策的好處，包括即將推出的移轉工具 API 的相關資訊。[閱讀全文](../experience-decisioning/migrate-to-decisioning.md)

* 新增護欄，說明查詢資料集僅適用於資料集沙箱所在區域的傳入邊緣型啟用。[閱讀全文](../data/lookup-aep-data.md#guidelines)

* 協調的行銷活動管道設定文件已新增區段，說明如何在 URL 追蹤參數中使用內容屬性 (例如行銷活動 ID、名稱和動作詳細資訊)，以用於分析和報告用途。[閱讀全文](../orchestrated/channel-config.md#url-tracking)

* 內容最佳化文件已重新建構，以提高清晰度。主要最佳化頁面已分割成四個重點子頁面：快速入門頁面、目標定位的專屬頁面、實驗頁面，以及結合兩種方法的頁面。[閱讀全文](../content-management/gs-message-optimization.md)

* 已從三個歷程警示 (已發佈歷程、歷程已完成和已觸發自訂動作上限) 中移除有限可用性附註，因為這些功能現在已普遍可用。[閱讀全文](../reports/alerts.md)

* 測試、驗證及核准登陸頁面已新增區段，包括測試功能概觀、常見問題集、含導覽連結的決策樹，以及含文件連結的增強術語。[閱讀全文](../../rp_landing_pages/test-landing-page.md)

* 個人化語法文件中已新增區段，以釐清如何在個人化運算式中使用保留關鍵字。在 XDM 結構描述中作為欄位名稱使用時，某些 PQL 關鍵字 (例如 `next`、`last` 和 `this`) 必須使用反引號逸出。[閱讀全文](../personalization/personalization-syntax.md#reserved-keywords)

* [行銷活動快速入門](../campaigns/get-started-with-campaigns.md)和[管理行銷活動](../campaigns/manage-campaigns.md)頁面已重新建構，資訊架構已改進，包括包含特定類型指南的全面工作流程、增強型行銷活動類型比較，以及整合狀態表格。

* Journeys 登陸頁面已重新設計，以協助上線新的 6 步驟工作流程、增強歷程類型比較，以及經改進的整個文件導覽。[閱讀全文](../building-journeys/journey.md)

* 新增了詳細區段，協助使用者在設定直接郵件的檔案路由時，產生 SFTP 驗證的 Base64 編碼 OpenSSH 私密金鑰，以避免連線錯誤。[閱讀全文](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* 已在子網域委派文件中新增附註，以告知使用者在嘗試委派至 Adobe 之前允許 24 到 48 小時的 DNS 傳播。[閱讀全文](../configuration/delegate-subdomain.md#set-up-subdomain)

## 2025 年 12 月 {#december-2025}

* 決策文件的自訂上傳客群已更新，以包含擷取擴充資料所需的 API 標幟。在產品建議決策中使用 CSV 上傳的客群時，您必須在 API 請求承載中包含 `"xdm:enrichedAudience": true`，以在產品建議決策回應中擷取擴充屬性。[閱讀全文](../offers/custom-upload-decisioning.md#must-read)

* 已在校樣傳送文件中新增附註，以釐清頻率上限規則適用於校樣。頁面現在包含「必須閱讀」區段，其中包含有關頻率上限行為、鏡像頁面限制和資產可存取性規則的重要考量。[閱讀全文](../content-management/proofs.md)

* 「管道快速入門」頁面已新增新的通訊管道可用性表格，顯示哪些管道在歷程和行銷活動 (動作行銷活動、API 觸發的行銷活動以及協調的行銷活動) 中受到支援。[閱讀全文](../channels/gs-channels.md#channels)

* 已建立新的全面追蹤登陸頁面，以協助使用者探索及存取 Journey Optimizer 中提供的所有追蹤與監視功能。[閱讀全文](../start/get-started-tracking.md)

* 已增強「電子郵件選擇退出管理」頁面，其中包含有關取消訂閱流程的詳細資訊，說明登陸頁面選擇退出的預期事件順序。[閱讀全文](../email/email-opt-out.md#send-message-unsubscribe-link)

* 已更新訂閱清單文件，新增串流區段適用性標準的相關資訊。[閱讀全文](../landing-pages/subscription-list.md#define-subscription-list)

* 推出新的 IP 暖身傳遞能力指南，提供信譽基礎知識、投放前準備、監視量度的全面指引，以及從零信譽過渡至成功收件匣刊登位置的最佳做法。[閱讀全文](../configuration/ip-warmup-deliverability-guide.md)

* 登陸頁面及電子郵件選擇退出區段已新增警告，以澄清按一下取消訂閱連結只會開啟登陸頁面，但使用者必須提交表單才能完成選擇退出流程。[閱讀全文](../landing-pages/lp-use-cases.md#configure-opt-out)

* 推出新的歷程使用案例資料庫，整理實用使用案例集合，包括戰術模式 (禁止邏輯、個人化技術、歷程退出策略) 和涵蓋行銷和技術工作流程的完整端到端案例。[閱讀全文](../building-journeys/jo-use-cases.md)

* 推出新使用案例，示範如何設定歷程以僅在工作日 (星期一至星期五) 傳送電子郵件，以及在星期一指定時間自動整理週末項目佇列。[閱讀全文](../building-journeys/weekday-email-uc.md)

* 推出新頁面，說明 Journey Optimizer 的決策功能，包括新一代決策框架與現有的決策管理解決方案之間的差異，以及跨管道提供個人化產品建議的主要優點。[閱讀全文](../experience-decisioning/gs-decision.md)

* 客群啟用文件已新增一個區段，說明如何在 [!DNL Journey Optimizer] 中啟用不支援的客群類型 (例如 Customer Journey Analytics 客群)，方法是在客群入口網站中以新的區段定義來包裝這些客群。[閱讀全文](../audience/target-audiences.md#activation-non-supported)

* 等待活動文件中已新增一個區段，說明停留在讀取客群歷程的等待活動中的輪廓如何自動從統一輪廓服務 (UPS) 重新整理其屬性。這說明了輪廓資料可能會在等待節點後的歷程執行期間發生變更，如果您想要在整個歷程中保持一致的快照資料，這可能會產生非預期的結果。[閱讀全文](../building-journeys/wait-activity.md#profile-refresh)

* 「路徑實驗」區段中已新增警告說明，警告使用者不要編輯發佈後的路徑實驗中繼資料，因為這會中斷實驗結果的計算和報告。[閱讀全文](../building-journeys/optimize.md#experimentation)

* 「建立表單預設集」區段已新增附註，以指定串流連線在選取範圍下拉式清單中顯示的要求。[閱讀全文](../landing-pages/lp-forms.md#create-form-preset)

* 「決策」區段已推出新頁面，說明如何設定資料收集以追蹤曝光次數、點按數和自訂事件。[閱讀全文](../experience-decisioning/data-collection/schema-requirement.md)

* 已重新整理使用 AI 助理產生內容的文件，以提高清晰度和可用性。前五個管道特定頁面 (電子郵件、推播、簡訊、網頁和登陸頁面) 已合併為三個產生類型頁面：[產生完整內容](../content-management/generative-full-content.md)、[產生文字](../content-management/generative-text.md)和[產生影像](../content-management/generative-image.md)。

## 2025 年 11 月 {#november-2025}

* 推出新的決策常見問題集頁面，涵蓋上限規則、AI 模型設定、流量需求和產品建議最佳化策略等主題。[閱讀全文](../experience-decisioning/decisioning-faq.md)

* 「開始使用電子郵件設計」頁面已更新，以釐清如何存取電子郵件設計工具。[閱讀全文](../email/get-started-email-design.md)

* 「DMARC 記錄」頁面已新增疑難排解區段，以解決 DNS 傳播延遲的問題。[閱讀全文](../configuration/dmarc-record.md#troubleshooting)

* 「使用 GenStudio for Performance Marketing」頁面已更新區段，包括主要功能、常見使用案例、先決條件和常見問題。[閱讀全文](../integrations/genstudio.md)

* 「護欄和限制」頁面已新增針對使用傳入管道定位目標假名輪廓的護欄：鎖定未經驗證的訪客會增加您的可互動輪廓總數，因此 Adobe 建議設定自動刪除輪廓的存留時間 (TTL) 以管理相關成本。[閱讀全文](../start/guardrails.md#profile-management-inbound)

* 現在，「程式碼型實作方法範例」頁面上有兩個關於為決策和程式碼型體驗設定 Web SDK 的教學課程。[閱讀全文](../code-based/code-based-decisioning-implementations.md#tutorials)

* 已新增附註，以指定從首次發佈起最多 2 年 (730 天) 仍可存取資產和影像，並在到期後需要重新發佈。[閱讀全文](../content-management/proofs.md)

* 全面的 AI 助理內容提示指南現已推出。本指南會教導您如何製作有效的提示，以建立高轉換率、符合品牌的行銷內容。了解撰寫行銷目標、使用品牌資產和針對不同管道最佳化內容的最佳做法。[閱讀全文](../content-management/ai-assistant-prompting-guide.md)

* 區段定義文件已新增附註，以澄清 `frequencyMap` 屬性不支援用於區段定義，且無法用作客群細分條件的一部分。對於以頻率為基礎的目標定位，請考慮在商業規則下使用頻率上限規則。[閱讀全文](../audience/creating-a-segment-definition.md)
* API 呼叫回應文件中已新增一個範例，說明如何在原生管道中使用自訂動作回應。此範例示範如何在電子郵件、推播和簡訊中使用 Handlebars 語法，從自訂動作回應中反覆處理巢狀陣列。[閱讀全文](../action/action-response.md#response-in-channels)

* Campaign v7/v8 整合文件中已新增章節，說明在即時 (RT) 端點變更時如何更新現有的自訂動作。該章節包含更新端點 URL、測試連線以及在儲存前驗證變更的逐步指示。[閱讀全文](../action/acc-action.md#update-action)

* 已在視覺片段文件中新增限制和最佳做法章節，以警告使用者不支援在包含動態內容的其他已解鎖片段中內嵌包含動態內容的片段。該指南包括相容性模式問題的疑難排解步驟，以及正確電子郵件結構設計的建議。[閱讀全文](../email/use-visual-fragments.md#fragment-dynamic-content)

* 歷程即時報告文件中已新增疑難排解章節，以協助使用者解決遺漏的報告資料問題。該章節涵蓋與報告資料集的歷程名稱同步、資料重新整理時間、存取權限驗證和歷程狀態需求。[閱讀全文](../building-journeys/report-journey.md#troubleshooting-missing-data)

* 資產文件新增了三個新的常見問題，說明資產過期和生命週期管理。涵蓋的主題包括 AEM Assets 的存留時間 (TTL) 原則 (730 天)、如何解決由於資產過期而損壞的影像，以及有關即將改善資產過期邏輯的資訊。[閱讀全文](../integrations/assets.md#faq-assets)

* 讀取對象活動文件新增了全面的疑難排解章節，以解決進入歷程的估計和實際輪廓之間的客群計數不相符問題。該章節涵蓋時間與資料傳播問題、資料驗證與監視技巧，以及最佳做法，包括使用「批次客群評估後觸發」選項。[閱讀全文](../building-journeys/read-audience.md#audience-count-mismatch)

* 已在客群資格事件文件中新增附註，以釐清串流細分延遲 (最長 2 小時)，並建議為時效性歷程新增等待活動或緩衝時間。[閱讀全文](../building-journeys/audience-qualification-events.md#streamed-speed-segment-qualification)

* 在電子郵件護欄中新增了章節，記錄歷程發佈的 2MB 訊息內容大小限制，包括將編寫內容保持在 1MB 以下的最佳做法，以允許後端處理額外負荷。[閱讀全文](../start/guardrails.md#message-content-size)

* 改善有關讀取客群活動中增量讀取選項的文件，以釐清快照計時相依性和 24 小時回顧限制，包括防止遺失輪廓的建議。[閱讀全文](../building-journeys/read-audience.md)

* 已在資料集查詢護欄中新增附註，以指定查詢無法鏈結在一起。[閱讀全文](../data/lookup-aep-data.md#guidelines)

* WhatsApp 和 LINE 管道現在可用於動作行銷活動。[閱讀全文](../campaigns/campaign-content.md)

* 登入管理文件中已新增有關歷程處理速率的完整新區段，涵蓋輪廓進入率、歷程中的事件和客群資格、等待活動影響以及動作活動影響。[閱讀全文](../building-journeys/entry-management.md#journey-processing-rate)

* 在設計電子郵件訊息時，系統現在會檢查關鍵設定並顯示警告和錯誤的警示。「護欄」頁面已新增有關電子郵件警示和驗證要求的資訊。[閱讀全文](../email/create-email.md#check-email-alerts)

* 表示無法為先前建立之產品建議啟用或停用的頻率上限的警告說明，已從「將限制新增至產品建議」頁面中移除。[閱讀全文](../offers/offer-library/add-constraints.md#capping)

* 現在提供有關如何使用歷程步驟事件的文件。[閱讀全文](../reports/journey-step-events-overview.md)

* 推出有關歷程進入和退出條件的全新全面指南，其中包含最佳做法、真實範例，以及在 Adobe Journey Optimizer 中管理輪廓進入和退出歷程時機的實用指引。[閱讀全文](../building-journeys/entry-exit-criteria-guide.md)

* 推出新頁面，說明如何反覆處理訊息中的內容資料。本指南說明如何使用 Handlebars 語法，以顯示個人化中事件、自訂動作回應、資料集查詢和其他內容來源的動態清單。[閱讀全文](../personalization/iterate-contextual-data.md)

* 有關識別歷程中捨棄事件的查詢已更正，以包括區段匯出工作錯誤、Dispatcher 捨棄和狀態機器捨棄的適當篩選器。[閱讀全文](../reports/query-examples.md#common-queries)

* 已在查詢範例文件中的所有 37 個查詢範例中新增介紹性句子，以提供更好的背景資訊並解釋每個查詢在呈現 SQL 程式碼之前的用途。這可幫助使用者了解，並提供更清楚的指引，說明何時應使用每個查詢。[閱讀全文](../reports/query-examples.md)

## 2025 年 10 月 {#october-2025}

* 您現在可以使用影像至 HTML 轉換工具，將影像轉換為 HTML 範本。[閱讀全文](../content-management/image-to-html.md)

* 現在提供 Adobe Journey Optimizer 發行週期的相關資訊。[閱讀全文](releases.md)

* 全新歷程常見問題頁面已推出。[閱讀全文](../building-journeys/journey-faq.md)

* 監視您的自訂動作功能現已推出。[閱讀全文](../action/reporting.md)

* API 觸發的行銷活動現在可使用高輸送量模式。[閱讀全文](../campaigns/api-triggered-high-throughput.md)

* 現在提供歷程的錯誤代碼參考。[閱讀全文](../building-journeys/error-codes-reference.md)

* Journey Optimizer Experimentation Accelerator 文件現已推出。[閱讀全文](../content-management/experiment-accelerator-gs.md)

* 已將新區段新增至 **formatDate** 協助程式函式文件。本節說明關鍵模式符號 (例如 y、Y、M、d 和 D) 的含義。[閱讀全文](../personalization/functions/dates.md#pattern-characters)

* 決策排名公式區段已新增 PQL 範例，說明如何根據輪廓的郵遞區號和年收入提升產品建議。[閱讀全文](../experience-decisioning/ranking/ranking-formulas.md#ranking-formula-examples)

* 歷程測試模式區段已新增限制，以提及測試模式不支援自訂上傳客群屬性擴充。[閱讀全文](../building-journeys/testing-the-journey.md#important_notes)

* 已在[決策管理護欄和限制](../offers/decision-management-guardrails.md#configurations)及[決策護欄和限制](../experience-decisioning/decisioning-guardrails.md#configurations)頁面中新增區段，以指定支援的組態數上限 (20,000)，此數目對應於您沙箱中存在的上限規則總數。

* 已在歷程的條件活動區段中新增附註，以記錄包含兩個以上跨裝置身分的輪廓的條件評估將會失敗。[閱讀全文](../building-journeys/condition-activity.md)

* 已新增一個頁面，說明如何使用同意原則，根據客戶的選擇尊重其偏好，同時尊重其同意。[閱讀全文](../action/preference-center.md)

* 「輪廓快速入門」和「護欄」頁面已新增附註，以指定在擷取資料時，電子郵件會區分大小寫，這意味著在定位對應的收件者時，可能會建立並使用重複的輪廓。[閱讀全文](../audience/get-started-profiles.md)

* 已在個人化編輯器中引進新的 `render` 屬性。將其設定為 `false`，以隱藏運算式片段的內容。[閱讀全文](../personalization/use-expression-fragments.md#use-expression-fragment)

* 在區段中新增了護欄清單，說明如何在決策原則中善用附加到決策項目的片段。[閱讀全文](../experience-decisioning/use-decision-policy.md#fragments)

* 新增資料集查詢的最佳做法：隨時切換以避免索引問題，並了解批次刪除如何影響查詢資料。[閱讀全文](../data/lookup-aep-data.md#guidelines)

* 新增了限制，以說明搭配補充識別碼使用讀取客群歷程時，僅支援統一輪廓服務客群。[閱讀全文](../building-journeys/supplemental-identifier.md#guardrails)

* Experimentation Accelerator 的文件已重新放置到另一個集合。[閱讀全文](https://experienceleague.adobe.com/zh-hant/docs/experimentation-accelerator/using/overview)

## 2025 年 9 月 {#september-2025}

* 「護欄和限制」頁面已新增傳入管道區段，以收集套用至網頁、應用程式內、程式碼型體驗和內容卡管道的所有限制。其中包括所有傳入請求的尖峰量限制 (每秒 5,000 個傳入請求)，以及最多 500 個作用中的傳入動作。[閱讀全文](../start/guardrails.md#inbound-guardrails)

* 已針對協調行銷活動發行「常見問題集」頁面。[閱讀全文](../orchestrated/orchestrated-campaigns-faq.md)

* 已在歷程步驟事件文件中新增疑難排解章節，其中包含最常捨棄事件類型的定義、常見原因和疑難排解步驟。[閱讀全文](../reports/sharing-field-list.md#discarded-events)

* 有關如何在歷程中使用補充識別碼的文件現在包含一個表格，詳細說明當使用補充識別碼在歷程中套用退出條件時，輪廓的行為方式。[閱讀全文](../building-journeys/supplemental-identifier.md#exit-criteria)

* 疑難排解章節已新增到暫停歷程中了解的輪廓捨棄。[閱讀全文](../building-journeys/journey-pause.md#discards-troubleshoot)

* 結構描述概觀文件中已新增資訊，以區分用於協調行銷活動的標準和關聯式結構描述。[閱讀全文](../data/gs-data.md)

* 已在決策和決策管理文件中新增有關成功訓練[自動最佳化](../experience-decisioning/ranking/auto-optimization-model.md)和[個人化最佳化](../experience-decisioning/ranking/personalized-optimization-model.md)模型的需求的資訊。

* 已澄清互動式訊息執行 REST API 呼叫具有 60 秒的逾時時間，且內部會重試以確保傳送。[閱讀全文](../campaigns/trigger-campaigns.md)

* 已更新「決策項目集合」頁面，以釐清定義規則時 **CONTAINS** 運算子的行為。[閱讀全文](../experience-decisioning/collections.md)

* 已更新「指派優先順序分數」頁面，其中包含在&#x200B;**動作**&#x200B;活動中定義傳入頻道動作的優先順序分數的特定步驟。[閱讀全文](../conflict-prioritization/priority-scores.md#priority-action)

<!--
## August 2025 {#august-2025}

* A new page listing the best practices for designing accessible email and landing page content with [!DNL Journey Optimizer] was added. [Read more](../email/accessible-content.md)

* The documentation for supplemental identifiers in journeys has been updated with the following clarifications:

    * After adding a supplemental identifier to a schema, a new event (for event-triggered journeys) or a new field group (for Read audience journeys) must be created. Existing entities do not refresh automatically and will not recognize the new identifier.

    * Supplemental identifiers are not validated against Data Usage Labeling & Enforcement (DULE) policies and are not considered during data governance checks in journeys.

        [Read more](../building-journeys/supplemental-identifier.md)

* The Optimization in campaigns page was updated to reflect the fact that optimization is now also available in journeys. [Read more](../content-management/gs-message-optimization.md)

* A link to the tutorial video describing how to leverage message optimization in a campaign was added. [Read more](../content-management/gs-message-optimization.md)

## July 2025 {#july-2025}

* The campaigns interface now features two separate tabs: **Action** and **API Triggered**. The documentation has been updated accordingly, with information for each campaign type organized into dedicated sections to improve clarity and usability. [Read more](../campaigns/get-started-with-campaigns.md)

* The [Get started with subdomain delegation](../configuration/about-subdomain-delegation.md) and [Delegate a subdomain](../configuration/delegate-subdomain.md) pages have been updated to better present the different delegation methods and the steps to set them up.

* A note has been added to the Fragments section, specifying that when tracking is enabled in a journey or a campaign, if links are present in a fragment and if this fragment is used in a message, these links are tracked such as all other links included in the message. [Learn more](../content-management/create-fragments.md#content)

* The guardrails and limitations applying to subdomain delegation in Journey Optimizer have been enriched and consolidated into one dedicated section. [Read more](../configuration/delegate-subdomain.md#guardrails)

* A note has been added to the Create fallback offers and Create decision pages to mention that fallback offers should contain all representations used within a decision. [Read more](../offers/offer-library/creating-fallback-offers.md)

* The guardrails applying to fragments have been enriched. [Read more](../start/guardrails.md#fragments-guardrails).

* A note has been added to specify that links added to messages expire after 25 months and links to mirror pages after 90 days. [Read more](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

<!--
## June 2025 {#june-2025}

* Added a new section on how to add and use rich text such as line breaks, bold, italics etc., to customizable fragments by using HTML components. [Read more](../content-management/customizable-fragments.md#rich-text)

* The Decisioning part has been updated with a specific section dedicated to building AI models. [Read more](../experience-decisioning/ranking/ai-models.md)

* Added a recommendation about the usage of the `actionExecutionTime` field in the journeyStep events action. [Read more](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* Added a note about the `messageID` which may not be unique for each individual delivery. [Read more](../data/datasets-query-examples.md)

* Added a recommendation about historical events management in data hygiene operations. [Read more](../privacy/data-hygiene.md#data-hygiene-recommendations)

* Added a guardrail about landing pages not being supported for migration between sandboxes. [Read more](../configuration/copy-objects-to-sandbox.md#global)

* Added a caution note about nested JSON objects not supported in custom authentication for custom actions. [Read more](../datasource/external-data-sources.md)

* Added a caution note about conditional content variant naming in the Email designer. [Read more](../personalization/create-conditions.md)

* Updated the "Undelegate a landing page subdomain" section. [Read more](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Clarified journey reentrance rules when using supplemental identifiers. [Read more](../building-journeys/supplemental-identifier.md#guardrails)

* Added a new note to clarify that you must use the expression editor in Advanced mode when selecting the supplemental identifier attribute during event configuration. [Learn more](../building-journeys/supplemental-identifier.md#add)

* Added clarification on how journey reentrance works with supplemental identifiers. [Learn more](../building-journeys/supplemental-identifier.md#guardrails)

## May 2025 {#may-2025}

* Adobe integrations available with Journey Optimizer are now listed in the "Connect your systems and environments" section. [Read more](../integrations/ajo-integrations.md)

* The content integrations are now grouped in the Content Management section. [Read more](../integrations/content-integrations.md)

* Architecture diagrams for Adobe Experience Platform and Journey Optimizer have been updated. [Read more](../start/get-started.md#architecture)

* Added a video about the personalization editor playground to help you learn how to write and test personalization code using sample data. [Read more](../personalization/personalize.md#video-perso)

* The maximum number of addresses in a seed list has been increased from 50 to 300. [Read more](../configuration/seed-lists.md#create-seed-list)

* A new step detailing how to wrap code when using decision policies in the code-based experience editor has been added to the Create decision policies page. [Read more](../experience-decisioning/create-decision.md#create-decision)

* A note has been added to the Code-based experiences documentation to specify that when you have multiple code-based experience actions running on the same surface, the campaign or journey's priority score determines what is delivered to the end-user if they qualify for more than one action. [Read more](../code-based/code-based-surface.md#surface-definition)

* A new page on troubleshooting inbound actions in journeys provides a step-by-step guide to identify and resolve issues independently before reaching out to support. [Read more](../building-journeys/troubleshooting-inbound.md)

* A new [page](../code-based/code-based-decisioning-implementations.md) has been added to describe how to add the following flags to your client implementation when using decisioning in code-based experiences:

    * Adding the `dryRun` flag to test decisioning in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

    * Apply deduplication to decisioning requests in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## April 2025 {#apr-2025}

* The Configuration chapter is now split into three chapters: [Channel configuration](../configuration/get-started-configuration.md), [Journey configuration](../configuration/about-data-sources-events-actions.md), and [Connect your systems](../configuration/ajo-apis.md).
* Added a caution note about using experience events in journey expressions and conditions. [Read more](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* Added a note on the Direct mail configuration page about temporary storage of the output file. [Read more](../direct-mail/direct-mail-configuration.md)
* Added a tip in the journey advanced expression editor section about the condition format guidelines. [Read more](../building-journeys/expression/expressionadvanced.md)
* Added a caution note in the `inAudience` function section about impacts and best practices when renaming an audience. [Read more](../building-journeys/functions/functioninaudience.md)
* Added a recommendation about the native keywords usage when using two-way SMS. [Read more](../sms/sms-opt-out.md)
* Updated the journey test page with a note about the need for including an identity namespace in the event used. [Read more](../building-journeys/testing-the-journey.md)
* Currently, you cannot undelegate subdomains through the [!UICONTROL Journey Optimizer] user interface - you must reach out to your Adobe representative. Steps to undelegate a subdomain are now detailed for [Emails](../configuration/delegate-subdomain.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain), [Web experiences](../web/web-delegated-subdomains.md#undelegate-subdomain), and [Landing pages](../landing-pages/lp-subdomains.md#undelegate-subdomain).<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
<!--
* Added clarification about the optional `maxHttpConnections` parameter in the journeys Capping API, including guidance on how to use it alongside throttling configurations for the same endpoint. [Read more](../configuration/throttling.md)
* In the Decisioning section, added guidance explaining that approved offer items cannot be deleted if they are used in a collection or a decision. Included steps to change their status to "Draft" using the **[!UICONTROL Undo approve]** option. [Read more](../experience-decisioning/items.md#manage)
* Information on sandboxes have been grouped together into a new "Sandboxes management" section. This new section provides information on how to use and assign sandboxes, and how to use package export and import capabilitie to copy objects such as journeys, content templates, or fragments, across multiple sandboxes. [Read more](../administration/sandboxes.md)

## March 2025 {#mar-2025}

* The page about Audience Qualification events has been updated with new recommendations. [Read more](../building-journeys/audience-qualification-events.md)
* Custom action troubleshooting capability is now available to all customers (GA). [Read more](../action/troubleshoot-custom-action.md)
* Data Hygiene is now Data Lifecycle in the product user interface. The documentation has been updated to reflect this change. [Read more](../privacy/data-hygiene.md)
* The missing Landing Page built-in permissions have been added to the documentation. [Read more](../administration/ootb-permissions.md)
* A note has been added about scheduling recurring campaigns. [Read more](../campaigns/create-campaign.md)
* The section about inserting links and enabling tracking in an email message has been updated and reorganized. [Read more](../email/message-tracking.md)
* The section about personalization capabilities into Adobe Journey Optimizer has been reorganized and improved. [Read more](../personalization/personalize.md)
* Decision management API to list personalized offers has been updated with a sample to perform pagination if multiple personalized offers are missing from the response. [Read more](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* A new page gathering all information regarding the List unsubscribe feature has been created for improved clarity. [Read more](../email/list-unsubscribe.md)
* The Frequency capping section has been updated with information on how the frequency capping counter is updated for the Decisioning and Batch Decisioning APIs, in addition to the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)

## February 2025 {#feb-2025}

* The Read Audience activity guardrails have been updated to specify that only one activity can be used in a journey and that it can target only one audience. [Read more](../building-journeys/read-audience.md)
* Journey guardrails when using Adobe Campaign activities have been updated. [Read more](../start/guardrails.md#ac-g)
* Steps to create your first journeys have been detailed, and links to documentation section have been added. [Read more](../building-journeys/journey-gs.md)
* A new page is now available to detail the journey dashboard and filtering user interface. [Read more](../building-journeys/journey-ui.md)
* Documentation for **[!UICONTROL Send-Time optimization]** and its related FAQ have been updated, improved and moved to a new dedicated page. [Read more](../building-journeys/send-time-optimization.md)
* New guardrails have been added for journey events. [Read more](../start/guardrails.md#events-g)
* The built-in channel actions page has been reorganized. [Read more](../building-journeys/journeys-message.md)
* Guardrails & limitations have been added in the Decisioning and Decision management sections.
    * [Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md)
    * [Decision management guardrails & limitations](../offers/decision-management-guardrails.md)
* A new section on context data has been added in the Decision management documentation. It provides information on how to leverage context data in the decisioning engine, for example to design a decision rule that requires the current weather to be ≥80 degrees at the time the decision request is made. [Read more](../offers/context-data.md)

## January 2025 {#jan-2025}

* A new section on the **[!UICONTROL Execution address]** option in the email configuration has been added. The primary address is defined at the sandbox level, but the default setting can be overidden for a specific email configuration. [Read more](../email/email-settings.md#execution-address)

* The **Get started with deliverability** page has been updated with the possibility to create IP warmup workflows directly from the user interface. [Read more](../reports/deliverability.md#reputation)

* The **Header parameters** section has been updated to reflect the new labels and changes in the user interface. [Read more](../email/email-settings.md#email-header)

* The **Forward email** section has been updated to specify that all emails sent to the **From email** address are forwarded to the forward email address. If no forward email is specified, these emails are discarded. [Read more](../email/email-settings.md#email-settings)

* The maximum size of contextual attributes passed into an API-triggered campaign request has been updated to 200kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)

* A new section has been added to the **Manage fragments** page to describe how to add new attributes to a live fragment. The whole page has also been improved. [Read more](../content-management/manage-fragments.md#adding-new-attributes)

* A "Guardrails & limitations" section has been added to the conflict management & prioritizations tools documentation. [Read more](../conflict-prioritization/gs-conflict-prioritization.md)

* A new end-to-end use case has been added to present all the steps needed to use Decisioning in content experiments with the [!DNL Journey Optimizer] code-based experience channel. [Read more](../experience-decisioning/experience-decisioning-uc.md)

* The **Configure email settings** page has been divided into several sub-pages for improved readability, including new standalone pages dedicated to [List unsubscribe](../email/list-unsubscribe.md), [Header parameters](../email/header-parameters.md) and [URL tracking](../email/url-tracking.md).

## December 2024 {#nov-2024}

* A note has been added to help troubleshoot a potential error message when making an API call to enable datasets for personalization using Adobe Experience Platform data. [Read more](../personalization/aep-data-perso.md)

## October 2024 {#oct-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] October '24 release have been detailed in the documentation. [Read more](release-notes.md)
* All communication channels available in [!DNL Journey Optimizer] are now grouped in a dedicated section of the documentation. [Read more](../channels/gs-channels.md)
* The **Configure your code-based experience** page has been improved to make the process clearer, including the section explaining what a surface URI is. [Read more](../code-based/code-based-configuration.md)
* The **Create web channel configuration** page has been updated to clarify the steps when creating a pages matching rule, which also apply to Code-based experience configuration. [Read more](../web/web-configuration.md#web-page-matching-rule)
* A note about the upcoming time-to-live (TTL) guardrail for system-generated datasets has been added. [Read more](../data/get-started-datasets.md)
* A new section has been added to describe how to preview your code-based personalized experiences right on your browser or on your mobile devices, using the **Preview on device** option when simulating content in a journey or a campaign. [Read more](../code-based/test-code-based.md#preview-on-device)
* A new page has been added on how to leverage Custom upload audiences for decisioning. [Read more](../offers/custom-upload-decisioning.md)
* A new page has been added to introduce the decision capabilities available in Journey Optimizer. [Read more](../experience-decisioning/gs-decision.md)
* Guardrails and limitations have been added to the Decisioning documentation. [Read more](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## September 2024 {#sept-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] Sept '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a section about journey retry management. [Read more](../building-journeys/read-audience.md#read-audience-retry)
* The FAQ about Capping/throttling rule for custom actions has been updated to mention the default capping rule. [Read more](../configuration/external-systems.md#faq)
* The Control access section has been updated with permissions related to AI Assistant Content Generator. [Read more](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* A video about AI Assistant Content Generator for email generation has been added. [Read more](../content-management/generative-full-content.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
* Journey guardrails have been updated. [Read more](../start/guardrails.md#journeys-guardrails-journeys)


## July 2024 {#july-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] July '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A personalization use case has been added on how to personalize an email with information related health plans and prescriptions. [Read more](../personalization/perso-uc-plan-prescriptions.md)

## June 2024 {#june-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] June '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A note about the usage of merge policies in journeys has been added on [this page](../building-journeys/journey-properties.md#merge-policies).
* The page about how to configure a **Wait** activity in a journey has been reorganized and improved. [Read more](../building-journeys/wait-activity.md)
* A new page has been created to detail journey's properties. [Read more](../building-journeys/journey-properties.md)

## May 2024 {#may-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] May '24 release have been detailed in the documentation. [Read more](release-notes.md)
* The section on seed lists has been updated regarding recurring journeys. [Read more](../configuration/seed-lists.md#use-seed-list)
* The setion on external data sources has been updated. [Read more](../datasource/external-data-sources.md#custom-authentication-access-token)
* The global journey timeout of 30 days has been added to the Guardrail and limitation page. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* The section on the Adobe Campaign v7/v8 integration has been updated with information on provisionning. [Read more](../action/acc-action.md#access)
* The expression editor used to personalize content has been renamed in the documentation to "personalization editor" to clearly differenciate it from the [Journey expression editor](../building-journeys/expression/expressionadvanced.md). [Read more](../personalization/personalization-build-expressions.md)

## April 2024 {#april-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] April '24 release have been detailed in the documentation. [Read more](release-notes.md#apr-2024)
* Configuration steps for In-app messaging have been detailed. [Read more](../in-app/inapp-configuration.md)
* Documentation for [Offer decisioning APIs](../offers/api-reference/offer-delivery-api/decisioning-api.md) and [Batch decisioning APIs](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md) have been updated.
* Information has been added in the Decision management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-profile-error-rate)
* Information on the Wait activity has been added to the page on journey reports. [Read more](../reports/sharing-overview.md)
* For Journeys in test mode, following shortcuts have been disabled:
    * T: Shortcut to toggle the test mode on or off.
    * E: Shortcut used to trigger an event in an event-based journey.
    * P: Shortcut to trigger an event in an audience-based journey for which the Single profile at a time option is turned on.
    * L: Shortcut designated to display the test logs.
* The Message frequency rules page has been updated with a new subsection on daily frequency cap, which is available on demand in addition to weekly or monthly capping.
* The Work with consent policies page has been improved and updated with useful links to the Experience Platform documentation. [Read more](../action/consent.md)
* A new section has been added to reflect the fact that you can display HTML email content templates as thumbnails with the Grid view mode (Limited Availability). [Read more](../content-management/content-templates.md#template-thumbnails)
* A new section has been added to the Deliverability page to explain what feedback loops are and how to leverage them. [Read more](../reports/deliverability.md#feedback-loops)
* A note has been added to the Create personalized offers section to specify that the size of an offer including all its representations cannot exceed 300KB. [Read more](../offers/offer-library/creating-personalized-offers.md#create-offer)

## February 2024 {#feb-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] February '24 release have been detailed in the documentation. [Read more](release-notes.md#feb-2024)
* The Journey Optimizer + Workfront integration has been added to the integrations page. [Read more](../integrations/ajo-integrations.md)
* Information has been added on how to personalize offers' representations based on context data. [Read more](../offers/offer-library/add-representations.md#context-data)
* The guardrails page has ben updated with a note on custom actions which support JSON format only when using request or response payloads. [Read more](../start/guardrails.md#custom-actions-g)
* Additional information has been added about the basic authentication type in external datasources. [Read more](../datasource/external-data-sources.md)
* A note has been added to clearly differenciate the [Journey expression editor](../building-journeys/expression/expressionadvanced.md) from the [personalization editor](../personalization/functions/functions.md).
* The list of functions available in the advanced expression editor has been updated. [Read more](../building-journeys/expression/functions.md)
* The page on the Split function has been updated. [Read more](../building-journeys/functions/functioninaudience.md)
* Information has been added regarding the impact of the opt-in or opt-out of push notifications on In-app messages. [Read more](../in-app/create-in-app.md)
* The Message frequency rules page has been updated to reflect the Duration options available in the user interface (weekly or monthly).
* The Edit a PTR record section has been updated to clarify the fact that PTR records cannot be created manually and that you need to edit PTR records to assign them new subdomains. [Read more](../configuration/ptr-records.md#edit-ptr-record)

## January 2024 {#jan-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] January '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A guardrail about the journey size has been added. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* Journey timeout management has been detailed [in the following section](../building-journeys/journey-properties.md#global_timeout).
* Journey Optimizer [documentation home](../../ajo-home.md) page has been redesigned.
* Recommendations about the Update Profiles activity have been added. [Read more](../building-journeys/update-profiles.md) 
* Information has been added regarding the behavior of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `listObject` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/conversion-functions.md#toString)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#modify-an-action-campaign)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the Decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#batch-speed-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the Decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behavior. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#content-templates)
* Several warnings have been added in the **Create and publish landing pages** section to specify that you cannot access your landing page by simply copy-pasting into a web browser the URL defined when creating the page, even if published. Instead you can test it using the preview function. [Read more](../landing-pages/create-lp.md)
* A new section has been added on how to **manage consent** for the direct mail channel. [Read more](../direct-mail/test-send-direct-mail.md)

## July 2023 {#july-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] July '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The wait activity documentation page has been improved with additional information and best practices related to the global timeout and reentrance usage. [Read more](../building-journeys/wait-activity.md)
* The page on entry management has been improved. [Read more](../building-journeys/entry-management.md)
* Additional information has been added about the throttling rate in the Read audience activity documentation. [Read more](../building-journeys/read-audience.md)
* Additional information has been added about retries. [Read more](../start/guardrails.md#general-actions-g)
* The **Implement personalization consent** section has been updated to describe how to manually enforce personalization consent in campaigns: you can use the segment rule builder to create an audience containing opt-out profiles or add a split activity to a composition workflow. [Read more](../privacy/opt-out.md#opt-out-expression-editor)

## June 2023 {#june-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] June '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the discard rate ratio in the Journeys overview screen. [Read more](../building-journeys/journey-gs.md#journey-access)
* A note has been added with the steps to follow if you modify your schema with new enumeration values after creating an event [Read more](../event/about-creating.md)
* A recommendation has been added to use journeyVersionID instead of journeyVersionName when querying journeys. [Read more](../reports/sharing-common-fields.md#journeyversionid-field)
* Additional examples on the evaluation criteria order have been added to the **Create decisions** section to illustrate cases where multiple criteria and multiple decision scopes are used. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Decision management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publish-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the Decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#override-execution-address-journey)
* The **URL tracking** section now provides the list and description of all contextual attributes that can be set for URL tracking in an email channel configuration. [Read more](../email/email-settings.md#url-tracking)

## March 2023 {#march-2023}

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html)
* All new features and improvements coming with [!DNL Journey Optimizer] March '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a step to enable Adobe Analytics events in your journeys. [Read more](../event/about-analytics.md)
* A new section has been created in the Decision management guide on how to collect offer decisioning feedback in Adobe Experience Platform, including which offers are displayed and how users interact with them. [Read more](../offers/data-collection/data-collection.md)
* A new subsection has been added to the **Create decision** section to explain the difference between evaluating criteria in a sequential order or at the same time. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A guardrail has been added for read audience journeys with incremental read. You cannot create a new version, you need to duplicate the journey. [Read more](../start/guardrails.md#journey-versions-g)
* The use case on how to limit throughput put has been updated with information on throttling capabilities. [Read more](../building-journeys/limit-throughput.md)
* A note has been added to specify that scalar arrays are not supported in response payload definition. [Read more](../datasource/external-data-sources.md)
* The section on profile cap conditions has been updated. [Read more](../building-journeys/condition-activity.md#profile_cap)

## February 2023 {#feb-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the canvas toolbar. [Read more](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Information has been added to state that internal Adobe addresses are not allowed in URLs and APIs. [Read more](../start/guardrails.md)
* A note has been added in the API-triggered campaigns documentation to specify that contextual attributes passed into the request cannot exceed 50kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)
* Information was added on how opt-out information is stored in the **Consent Service Dataset** after recipients are unsubscribed through a landing page. [Read more](../landing-pages/lp-use-cases.md#configure-opt-out)

## January 2023 {#jan-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added on custom authentication endpoints in the capping documentation. [Read more](../configuration/external-systems.md)
* A new custom authentication example has been added in the external datasources section. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* A note has been added about Data Collection Core Service (DCCS) for event-triggered journeys. [Read more](../start/guardrails.md#events-g)
* A note on identity namespace retrieval has been added in the [Read audience](../building-journeys/read-audience.md), [Audience qualification](../building-journeys/audience-qualification-events.md) and [Event creation](../event/about-creating.md) sections.
* Accessibility features in [!DNL Journey Optimizer] are now grouped in a dedicated page. [Read more](../start/accessibility.md)
* The examples have been updated in the Operators section of the advanced expression editor documentation. [Read more](../building-journeys/expression/operators.md)
* A note has been added about the limitation on lookup with array of objects. [Read more](../event/experience-event-schema.md#relationships_limitations)
* Added a new page about data management in [!DNL Journey Optimizer]. [Read more](../data/gs-data.md)
* Added a table listing all codes that can be returned in the response when delivering offers using the Decisioning API. [Read more](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++

+++ 2022

## December 2022 {#december-2022}

* The Messages guide has been reorganized and split into dedicated guides for each channel:

    * [Email channel](../email/get-started-email.md)
    * [Push notification channel](../../rp_landing_pages/push-landing-page.md)
    * [SMS channel](../sms/get-started-sms.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#send-to-suppressed-email-addresses)
* Added a section on how to modify the content of a message in a live journey. [Read more](../building-journeys/journeys-message.md#update-live-content)

## October 2022 {#october-2022}

* Added a journey use case on how to limit throughput using External Data Sources and Custom Actions. [Read more](../building-journeys/limit-throughput.md)
* The journey use case section has been reorganized into two categories: [Business use cases](../building-journeys/journeys-uc.md) and [Technical use cases](../building-journeys/collections.md).
* The **Entity Dataset** section has been updated with more details. [Read more](../data/datasets-query-examples.md#entity-dataset)
* The opt-out management and consent policies sections have been reorganized. [Read more](../privacy/opt-out.md)
* The section on advanced parameters in journey messages has been clarified and now specifies that email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. 
* Added a note to the **Configure landing page subdomains** section to specify that capital letters are not allowed in landing page subdomains. [Read more](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] September '22 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a best practice related to the use of wait activities in recurring read audience journeys. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added new step event query examples as well as information on the difference between id, instanceid and profileid. [Read more](../reports/query-examples.md).
* Updated the pages related to the [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly) and [toString](../building-journeys/functions/conversion-functions.md#toString) functions.
* Added details on the time condition parameters. [Read more](../building-journeys/condition-activity.md#time_condition)
* Added information on built-in datasets. [Read more](../data/get-started-datasets.md#access-datasets)
* The Global report and Live report sections have been improved and reorganized. [Read more](../reports/report-gs-cja.md)
* A list of every reporting metric available in Adobe Journey Optimizer has been added.
[Read more](../reports/report-gs-cja.md#email-and-sms-metrics)
* The BCC email section has been moved to the new Support for archiving page. [Read more](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] August '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The Frequency rules section has been updated to reflect the new in-line messaging flow.
* A video showing how to configure subscriptions and create landing pages is now referenced in the Get started with landing pages section. [Read more](../landing-pages/get-started-lp.md#video)
* A limitation has been added for journeys using Read Audience activities. [Read more](../building-journeys/read-audience.md)
* The expression editor operators page has been improved. [Read more](../building-journeys/expression/operators.md)
* A section on how to schedule a campaign has been added. [Read more](../campaigns/create-campaign.md)
* General syntax rules section for expression editor has been updated to take into account the new rule regarding the backslash symbol escaping in literal functions. The existing published messages are not impacted by this change. Only the new or draft messages must be updated. [Read more](../personalization/personalization-syntax.md#general-rules)

## July 2022 {#july-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] July '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Set up channel configurations** section has been clarified and updated with links to the page describing how to configure the SMS channel. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* In the journey properties, the **Profile Time zone** option is now disabled by default. [Read more](../building-journeys/timezone-management.md#timezone-from-profiles)
* In the **Wait** activity, the **Fixed date** option is no longer available. [Read more](../building-journeys/wait-activity.md)
* Added more information on the **Incremental read** option in the **Read audience** activity. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added recommendations on the **Profile cap** condition type. [Read more](../building-journeys/condition-activity.md#profile_cap)
* Added a limitation on business events. [Read more](../start/guardrails.md#events-g)

## June 2022 {#june-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] June '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new section about Privacy requests has been added to the documentation. [Read more](../privacy/requests.md)
* A new section about Audit logs on resources has been added to the documentation. [Read more](../privacy/audit-logs.md)
* A new section about how to add HTML or JSON content coming from Adobe Experience Cloud Asset library to an offer representation has been added to the documentation. [Read more](../offers/offer-library/add-representations.md#html-json)
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md)
* Updated the Wait activity page. [Read more](../building-journeys/wait-activity.md)
* Added the list of Adobe Journey Optimizer datasets with query examples. [Read more](../data/datasets-query-examples.md)
* The Allowed list page has been moved to the Configuration section. [Read more](../configuration/allow-list.md)
* The Suppression list page has been updated to clarify some information, including the fact that all ASCII characters comprised between 32 and 126 are allowed in the reason for suppression field. [Read more](../configuration/manage-suppression-list.md)
* The link to guardrails and static limits for Decision management has been added. [Read more](../start/guardrails.md)
* Send-Time Optimization is now available for all customers. The beta mention has been removed. [Read more](../building-journeys/send-time-optimization.md)
* The Batch Decisioning API has been added to the list of available APIs to delivery personalized offers. [Read more](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## May 2022 {#may-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] May '22 release have been detailed in the documentation. [Read more](release-notes.md)
* New query examples related to [audience qualification](../reports/query-examples.md#segment-qualification-queries) and [events](../reports/query-examples.md#event-based-queries) have been added.
* The email design section now mentions new built-in templates available to start content with. Related screenshots have been updated. [Read more](../email/get-started-email-design.md)
* Links to key resources have been updated in Journey Optimizer documentation home page.
* Screenshots for landing page and subscription reporting have been updated. [Read more](../reports/live-report.md)
* A note has been added stating that the Delete method is not supported in custom actions. [Read more](../action/about-custom-action-configuration.md)
* Links to how-to videos have been updated.
* The [Email configuration](../configuration/about-subdomain-delegation.md), [Message presets](../configuration/channel-surfaces.md) and [Configure landing pages](../landing-pages/lp-subdomains.md) sections have been reorganized for improved readability.
* The URL tracking section has been updated and improved with examples. [Read more](../email/email-settings.md#url-tracking)
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#email-settings)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
* The **Get Started with Datasets** section has been improved to detail how to access and create datasets. [Read more](../data/get-started-datasets.md)
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* The **Create message presets** section now specifies that you cannot proceed with preset creation while the selected IP pool is under edition (**[!UICONTROL Processing]** status) and has never been associated with the selected subdomain. [Read more](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* The message presets **URL tracking** section has been updated to reflect minor changes in the user interface. [Read more](../configuration/channel-surfaces.md#url-tracking)

## March 2022 {#march-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] March '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page on getting started with AI models has been added to the **Offer decisioning** section, including a thorough description of the [auto-optimization model](../offers/ranking/auto-optimization-model.md), the algorithm it uses and more technical details. [Read more](../offers/ranking/ai-models.md)
* The test profile creation page has been moved to the  **Audience, profiles and identity** section. [Read more](../audience/creating-test-profiles.md)
* Added an example on how to add an expression as a default value in the expression editor. [Read more](../building-journeys/expression/field-references.md#default-value)
* The **Create personalized offers** section has been reorganized for improved readability. [Read more](../offers/offer-library/creating-personalized-offers.md)
* A new section has been added to describe the impacts that changing an offer's start and/or end dates may have on this offer's frequency capping. [Read more](../offers/offer-library/add-constraints.md#capping-change-date)
* The **Change the primary email addresses** section has been updated to reflect the user interface changes. [Read more](../configuration/primary-email-addresses.md)

## February 2022 {#feb-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The [replace](../building-journeys/functions/string-functions.md#replace) and [replaceAll](../building-journeys/functions/string-functions.md#replaceAll) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-decision-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-setup)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/date-functions.md#setHours), [getListItem](../building-journeys/functions/list-functions.md#getListItem), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/list-functions.md#filter), [intersect](../building-journeys/functions/list-functions.md#intersect), [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#decision-list)

* Added specific ranking formula examples to illustrate some real-life use cases. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Added a subsection on how to edit IP pools. [Read more](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] August '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Updated Decision management permissions. [Read more](../administration/ootb-product-profiles.md)
* Updated Email Designer screenshots with latest UI.
* Updated the configuration procedure for custom actions with dynamic URL paths and dynamic headers. [Read more](../action/about-custom-action-configuration.md#url-configuration)
* Added a section about accessibility features and shortcuts. [Read more](../start/user-interface.md#accessibility)
* Added a section about audience evaluation methods. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Added notes to the Suppression list, Allowed list and Email global/live report sections to specify that profiles with Suppressed and Not allowed statuses are excluded from the Email report Sent metrics. [Read more](../reports/report-gs-cja.md)
* Added a new section to describe how to retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [Read more](../configuration/allow-list.md#reporting)
* Updated the Enable the allow list section. [Learn more](../configuration/allow-list.md#enable-allow-list)
* Updated the Monitor message presets section with the possible preset creation failure reasons and details on such errors. [Read more](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Updated and renamed the Retry time period section to reflect the fact that you can now adjust the email retry setting in the message presets. [Read more](../configuration/retries.md#retry-duration)
* Updated the Delegate a subdomain section with more detailed information on the validation process performed by Adobe. [Read more](../configuration/delegate-subdomain.md#subdomain-validation)
* Added a section to describe how to manually add email addresses and domains to the suppression list. [Read more](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Updated the [Access the suppression list](../configuration/manage-suppression-list.md#access-suppression-list) section and [Retries](../configuration/retries.md) sections to reflect the new user interface.
* The new flow to add and configure representations when creating an offer has been documented. [Read more](../offers/offer-library/creating-personalized-offers.md#representations)

## July 2021 {#july-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] July '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added direct links to Experience Platform services documentation in [!DNL Journey Optimizer] home page and table of contents
* New landing pages for Experience Platform services available in [!DNL Journey Optimizer] 
* Added links to [!DNL Journey Optimizer] product description in the home page
* Added tutorial videos in multiple pages
* Optimized home page imagery
* Moved, improved and renamed 'Message tracking' section to 'Add links and track messages'. [Read more](../email/message-tracking.md)
* Added a subsection on mirror pages. [Read more](../email/message-tracking.md#mirror-page)
* Renamed 'offer activities' as 'decisions' and 'decisions' as 'decision scopes' in documentation and screens. [Read more](../offers/get-started/starting-offer-decisioning.md)
* New use case: [personalize a message with helper functions](../personalization/personalization-use-case-helper-functions.md)
* Updated the Read audience documentation to reflect materialized segment impacts. [Read more](../building-journeys/read-audience.md)
* Updated the Journey limitations. [Read more](../start/guardrails.md)
* Updated the Configure offers selection in decisions section. [Read more](../offers/offer-activities/configure-offer-selection.md)
* Added a warning to mention that event-based offers are not currently supported. [Read more](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documented the Decision management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
