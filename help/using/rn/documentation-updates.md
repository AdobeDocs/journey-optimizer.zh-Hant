---
solution: Journey Optimizer
product: journey optimizer
title: 文件更新
description: 瞭解 Adobe Journey Optimizer 的最新文件更新，包括新增頁面、結構調整和補充說明。
keywords: 文件更新、發行說明、Journey Optimizer、變更記錄
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 9c6142de31dfd7e1ce42b0bf0c7fc0be1743312d
workflow-type: tm+mt
source-wordcount: '7217'
ht-degree: 82%
---

# 文件更新 {#latest-updates}

此頁面列出 [!DNL Journey Optimizer] 文件中的所有最新變更，以及與每月發行功能和改進相關的更新。

## 2026年9月 {#september-2026}

* `inAudience`護欄現在包含超過5,000個受眾的沙箱的因應措施，在歷程編寫期間可能會拒絕較舊的受眾，因為驗證只會檢查5,000個最近更新的受眾。 [閱讀更多](../building-journeys/functions/functioninaudience.md#guardrails)

* 電子郵件映象頁面的指引已擴展：本檔案現在說明無法透過公用API或資料集擷取映象頁面URL、建議訊息匯出或密件副本封存以保留已傳送的內容，並澄清映象頁面連結在校訂和模擬中為非作用中。 [閱讀更多](../email/message-tracking.md#mirror-page)

* 新的&#x200B;**互動式示範**&#x200B;頁面現在可用於忠誠度挑戰，連結至自我引導的可點選示範，其中涵蓋行銷人員的挑戰建立流程（包括自攜資料和見解儀表板）、最終客戶體驗，以及CX Coworker中的忠誠度挑戰管理。 [閱讀更多](../loyalty-challenges/loyalty-challenges-demo.md)

* **個人化您的電子郵件背景**&#x200B;頁面已展開並改良。 它現在會記錄背景影像的完整&#x200B;**影像位置**&#x200B;下拉式清單，並新增背景色彩和影像的最佳實務，包括建議在實際的電子郵件使用者端中測試背景影像，而非僅仰賴電子郵件Designer預覽。 [閱讀更多](../email/backgrounds.md)

* 已重新整理並釐清&#x200B;**使用電子郵件Designer**&#x200B;頁面從頭開始設計內容：它將&#x200B;**[!UICONTROL n:n欄]**&#x200B;結構與固定的預設結構區分開來、可增加結構的欄數而不遺失現有內容的檔案、說明行動裝置上的欄棧疊行為，以及新增使用&#x200B;**[!UICONTROL 模組]**&#x200B;以快速開始建立電子郵件的步驟。 [閱讀更多](../email/content-from-scratch.md)

* **設計您的歷程**&#x200B;頁面現在包含有關新畫布體驗的完整教學課程區段，涵蓋如何新增活動、使用工具列圖示、選取多個活動以進行大量動作、複製和貼上活動，以及加入或分離分支。 [閱讀更多](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

* 已新增驗證自訂動作傳送的指南： **資料集查詢範例**&#x200B;頁面現在說明如何根據動作型別在訊息回饋事件、電子郵件追蹤和歷程步驟事件資料集之間進行選擇，以及說明如何解決「資料集未布建的表格」錯誤的檔案。 **歷程步驟事件總覽**&#x200B;和&#x200B;**疑難排解您的即時歷程執行**&#x200B;頁面已據此更新，澄清成功的自訂動作呼叫只會確認Journey Optimizer已執行動作，不會確認外部系統已傳送訊息。 [閱讀更多](../data/datasets-query-examples.md#choose-the-correct-dataset)

* 有關CX Coworker的資訊已新增至&#x200B;**使用AI**&#x200B;頁面，內容涵蓋CX Coworker是什麼、它與AI助理的關係，以及官方同事檔案的參考資料。 每個功能指南中也新增了專屬的技能頁面 — [歷程的CX Coworker技能](../building-journeys/journeys-coworker-skills.md)、[忠誠度的CX Coworker技能](../loyalty-challenges/loyalty-coworker-skills.md)和[CX Coworker內容管理工具](../content-management/content-management-coworker-skills.md)。 [閱讀更多](../start/ai-features.md#cx-coworker)

* 已在CX Coworker頁面的&#x200B;**歷程分析**&#x200B;下記錄新的&#x200B;**分析歷程異常**&#x200B;技能。 它會根據歷史基準偵測歷程的進入、退出或傳送計數中意外的尖峰、下降或平線，並執行唯讀診斷以找出可能的根本原因。 [閱讀更多](../building-journeys/journeys-coworker-skills.md#journey-analyze)

* 已更新&#x200B;**護欄和限制**&#x200B;和&#x200B;**歷程屬性**&#x200B;頁面，以將預設歷程裝載限制記錄為&#x200B;**2 MB （2,000,000位元組）**，澄清值反映序列化歷程定義而非僅活動計數，並說明90%警告和100%封鎖臨界值。 [閱讀更多資訊](../start/guardrails.md#journey-payload-size)和[瞭解更多資訊](../building-journeys/journey-properties.md#journey-payload-size)

* **護欄和限制**&#x200B;頁面已更正，以反映超過100 KB的視覺片段或超過200 KB的運算式片段不會再造成電子郵件傳送的截斷問題：現在單一700 KB片段大小護欄適用。 [閱讀更多](../start/guardrails.md#fragments-guardrails)

* **建立即時活動**&#x200B;頁面已更正： `executionMetadata`欄位僅適用於&#x200B;**API觸發的交易式**&#x200B;行銷活動，不適用於先前所述的API觸發的行銷活動。 [閱讀更多](../mobile-live/create-mobile-live.md#metadata)

* **AJO訊息回饋事件資料集**&#x200B;檔案已擴充，以澄清其涵蓋所有管道（電子郵件、SMS/RCS/MMS、直接郵件）的訊息傳遞回饋，而不只是電子郵件和推播，現在包含&#x200B;**將測試和非測試執行分類**&#x200B;區段，說明如何解譯`isTestExecution`欄位，包括`NULL`或缺少的值。 [閱讀更多](../data/datasets-query-examples.md#classify-test-executions)

* 已針對CX Coworker記錄新的&#x200B;**內容管理**&#x200B;功能，由15個讀取/寫入MCP工具提供支援，可讓您使用自然語言提示探索、建立、更新、複製及發佈內容範本、片段、登陸頁面及歷程/行銷活動內嵌訊息內容。 [閱讀更多](../content-management/content-management-coworker-skills.md#content-management)

* **將內容新增至您的登入頁面**&#x200B;檔案現在說明&#x200B;**將表單欄位設為同意核取方塊的必要欄位**&#x200B;選項：啟用時，除非選取核取方塊，且檢查在使用者端和伺服器端強制執行，否則無法提交表單。 [閱讀更多](../landing-pages/lp-content.md#use-form-component)

* **開始使用歷程模擬**&#x200B;頁面已更新，以記錄模擬現在支援內容決定節點和&#x200B;**最佳化**&#x200B;活動的目標定位規則方法（先前列為封鎖），以及新的&#x200B;**決定行為**&#x200B;表格，詳細說明在模擬執行期間如何評估優惠資格、適用規則和對象，以及排名方法。 [閱讀更多](../building-journeys/simulate-journey-gs.md#limitations)

* 已更正&#x200B;**將影像轉換為電子郵件內容範本**&#x200B;頁面，移除不正確的許可權要求：存取和建立包含影像到HTML轉換器的範本不需要&#x200B;**管理內容範本**&#x200B;許可權，而只需要&#x200B;**產生內容**&#x200B;許可權。 [閱讀更多](../content-management/image-to-html.md#access-image-to-html)

* **外部系統（自訂動作）**&#x200B;頁面已更正：當超過20%的呼叫在120秒的視窗中超過&#x200B;**5秒** （先前記錄為10秒）時，將會啟用慢速自訂動作端點的斷路器。 [閱讀更多](../configuration/external-systems.md#response-time)

* **設定您的管道組態**&#x200B;頁面現在包含澄清用於次要維度的結構描述必須具有主索引鍵，並且不支援複合主索引鍵的備註。 [閱讀更多](../orchestrated/channel-config.md)

* **忠誠度資料和資料集**&#x200B;和&#x200B;**開始使用來源**&#x200B;頁面已更新，將LAVA作為支援的忠誠度和獎勵聯結器，以及Talon.One、Capillary和Kobie。 [閱讀更多](../loyalty-challenges/loyalty-data-and-datasets.md)

## 2026 年 8 月 {#august-2026}

* **將視覺片段新增至您的電子郵件**&#x200B;頁面現在會釐清「電子郵件Designer」中具有動態內容和空白預設狀態的片段會顯示為空白 — 以相符的設定檔進行模擬以預覽內容。 [閱讀更多](../email/use-visual-fragments.md#fragment-dynamic-content)

* **追蹤您的訊息**&#x200B;頁面已更新，以釐清不支援的URL字元（例如單引號）必須以百分比編碼，而且若不加以編碼，可能會中斷追蹤的連結和URL追蹤引數。 [閱讀更多](../email/message-tracking.md#insert-links)

* 已更新「使用波段傳送」**&#x200B;**&#x200B;頁面，以記錄讀取對象歷程中的最後一個波段必須排程在歷程開始的&#x200B;**6天及18小時**&#x200B;內。 超過此視窗會觸發驗證錯誤，並防止歷程進入測試模式或上線。 [閱讀更多](../delivery/send-using-waves.md#limitations-guardrails)

* 新的&#x200B;**抑制意見事件**&#x200B;區段已新增至&#x200B;**決定管理資料集合**&#x200B;頁面，記錄如何在測試期間使用`dryRun`旗標抑制決定事件，以及防止擷取意見以用於報告和頻率上限計數器。 [閱讀更多](../offers/data-collection/data-collection.md#suppress-feedback)

* 新的&#x200B;**選擇驗證方法**&#x200B;頁面現已可用。 它會比較歷程模擬、測試模式和歷程練習，每個都會使用資料、是否傳送真正的訊息、要避免的常見錯誤，以及在建立歷程的每個階段選擇正確方法的決策指南。 [閱讀更多](../building-journeys/choose-validation-method.md)

* **護欄和限制**&#x200B;頁面已更新，以釐清「客群鑑定」活動和「事件」護欄：措辭現在一致統稱為「客群鑑定」**活動** (而非節點)，包括用作退出條件時，且兩個護欄現在都明確涵蓋&#x200B;**即時、已關閉、已暫停、測試模式和試運行**&#x200B;歷程。 [閱讀更多](../start/guardrails.md#audience-qualif-g)

* **測試 HTML 大小最佳化**&#x200B;區段中已新增備註，釐清校樣大小僅反映 HTML 範本大小 (Handlebars 處於最小值)，而非最終傳送的電子郵件大小，在傳送時解析動態運算式後，實際傳送的電子郵件大小可能會更大。 [閱讀更多](../email/create-email.md#optimize-html-proof)

* 新的&#x200B;**行動網站瀏覽器限制**&#x200B;區段已新增至&#x200B;**開始使用電子郵件設計**&#x200B;頁面，說明透過行動瀏覽器存取時，電子郵件在 Gmail 或 Outlook 中呈現方式不同的原因，並提供因應措施。 [閱讀更多](../email/get-started-email-design.md#mobile-web-limitations)

* 新的 **Outlook 轉譯考量事項**&#x200B;區段已新增至&#x200B;**開始使用電子郵件設計**&#x200B;頁面，其中列出設計時要注意的常見 Outlook 特殊行為：內距和寬度使用偶數、以像素為基礎的表格寬度、HTML 影像寬度屬性、替代文字、表格儲存格上的框線以及圓角。 [閱讀更多](../email/get-started-email-design.md#outlook-tips)

* **資料集存留時間 (TTL) 護欄**&#x200B;頁面已更新，包含大幅擴充的&#x200B;**受影響的資料集**&#x200B;表格，現在已涵蓋所有Journey Optimizer 系統產生的資料集 (包括數個先前未列出的資料集，例如 AJO 同意服務、互動式訊息設定檔、推播設定檔及訊息匯出資料集)，以及新增的&#x200B;**可用性**&#x200B;欄，標示每個資料集是否依預設包含，或是需要特定附加元件或授權。 **護欄和限制**&#x200B;頁面也已更新，以反映此護欄的確認執行日期：此變更將從 **2026 年10月1日**&#x200B;開始，在&#x200B;**現有客戶沙箱**&#x200B;中強制執行。 [閱讀更多](../data/datasets-ttl.md#datasets)

* 新的&#x200B;**使用影像設定模式**&#x200B;區段已新增至生成式內容文件中。 它說明了&#x200B;**[!UICONTROL 影像設定]**&#x200B;下可用的&#x200B;**平衡**、**DAM** 和&#x200B;**創意**&#x200B;模式，這些模式可控制 AI 產生的內容影像來源是來自您的數位資產管理程式庫、由 AI 產生，還是兩者混合使用。 [閱讀更多](../content-management/generative-uc.md#image-mode)

* **左側導覽>主要區段**&#x200B;底下的&#x200B;**目的地**&#x200B;說明已更新，以備註具有[!DNL Real-Time CDP]或[!DNL Adobe Journey Optimizer]的組織也可以從Experience Platform目的地目錄啟用受眾至合格的個人化目的地，例如[!DNL Adobe Target]。 [閱讀更多](../start/user-interface.md#main-sections)

* 已在「忠誠度挑戰」檔案中新增操作影片，說明如何建立挑戰、設定獎勵提供者，以及監控挑戰績效。 [觀看挑戰影片](../loyalty-challenges/create-challenges.md#video)、[觀看獎勵提供者影片](../loyalty-challenges/reward-definition-guide.md#video)，以及[觀看報告影片](../loyalty-challenges/loyalty-reporting.md#video)。

## 2026 年 7 月 {#july-2026}

* 新的&#x200B;**傳遞設定**&#x200B;區段已新增至文件導覽中。 它將套用至歷程、行銷活動和協調行銷活動的傳遞相關功能分組：**使用波段傳送**、**傳送時間最佳化**&#x200B;及&#x200B;**管道最佳化**&#x200B;皆已從歷程區段移至該處。

* 歷程與動作行銷活動原本獨立的&#x200B;**使用波段傳送**&#x200B;文件頁面已合併為單一頁面，且現在也涵蓋協調的行銷活動。 [閱讀更多](../delivery/send-using-waves.md)

* **設計您的歷程**&#x200B;頁面中已新增祕訣，指向有關&#x200B;**如何在新歷程畫布中分離及重新連接節點**&#x200B;的 Experience League 社群文章。 [閱讀更多](../building-journeys/using-the-journey-designer.md)

* **網格**&#x200B;元件區段已新增到&#x200B;**電子郵件設計工具內容元件**&#x200B;頁面中。 它可讓您將內容組織到由列和欄組成的結構化網格，其中每個儲存格都可包含其他內容元件。 [閱讀更多](../email/content-components.md#grid)

* **決策移轉 API** 文件已更新，其中補充說明目標沙箱&#x200B;**可以與來源沙箱**&#x200B;相同。 移轉流程會處理此情境並確保資料完整性，無論物件是在同一個沙盒內移轉，還是移轉至不同的沙箱。 [閱讀更多](../experience-decisioning/decisioning-migration-api.md#target-sandbox-preparation)

* 加強&#x200B;**決策移轉API**&#x200B;檔案，並提供移轉決策管理物件至Decisioning的全面指引。 新區段包括：具有10個命名慣例的實體對應參考、範圍內與範圍外涵蓋範圍、詳細請求/回應模型比較、具有Cookie處理的三種實作模式（使用者端、伺服器端、混合）、包含5個事件JSON範例的事件追蹤需求、跨沙箱移轉先決條件、端對端5步驟移轉程式，以及移轉常見問題集。 [閱讀更多](../experience-decisioning/decisioning-migration-api.md)

* 全新的 **CX Co-worker 技能**&#x200B;頁面現已推出。 它提供 Journey Optimizer 中所有歷程技能的完整文件，包括歷程建立、管道內容建立、忠誠度挑戰管理及歷程分析，並隨附每種技能的使用案例、範例提示和最佳做法。 [閱讀更多](../start/ai-features.md#cx-coworker)

* **至精確度**&#x200B;函式文件已更新，釐清 `toPrecision` 的運作方式類似於 JavaScript `toFixed()`：它會傳回具有固定小數位數的字串，包括在需要時補零。 [閱讀更多](../personalization/functions/math.md#to-precision)

* **結束歷程**&#x200B;頁面已更新，已釐清非定期「讀取客群」歷程的自動停止時間：排程執行後約 **96 小時 (~4天)** 的安全緩衝時間 (24 小時閒置期間 + 72 小時非傳送時間容許值)，在此期間歷程可在緩衝結束後不久轉換為&#x200B;**已停止**&#x200B;之前維持&#x200B;**上線**&#x200B;狀態。 頁面現在也釐清以波段為基礎 (多波段) 的歷程，以及使用傳送時間最佳化的歷程，均不適用此自動停止機制，而是遵循標準 91 天歷程逾時限制。 [閱讀更多](../building-journeys/end-journey.md#auto-stop-non-recurring)

* **建立 IP 暖身行銷活動**&#x200B;頁面已更新，已釐清目標選擇規則可套用至 IP 暖身行銷活動，並記錄評估行為：客群會籍在運行啟用時固定 (每日批次細分) ，而輪廓屬性則在運行階段從最近攝取的批次資料中讀取。 [閱讀更多](../configuration/ip-warmup-campaign.md)

* **編輯 PTR 記錄**&#x200B;頁面已新增警告，以通知客戶在將新的前向 DNS 記錄新增至其平台時，必須等到移轉完成後才能移除舊子網域的前向 DNS 記錄，否則將會導致編輯失敗。 [閱讀更多](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

* **使用波段傳送**&#x200B;頁面已更新，釐清跨波段的客群重新評估行為：客群會籍在啟用時已固定 (快照) ，但輪廓屬性和同意狀態會在每個波段處理時評估。 這表示系統會遵循各波段之間發生的選擇退出。 請在[常見問題集章節](../delivery/send-using-waves.md#faq)參閱更多資訊。

* **資料治理**&#x200B;頁面已更新，已釐清 DULE 原則執行僅適用於&#x200B;**輪廓屬性欄位**。 不支援以事件為基礎的欄位 (例如歷程事件欄位等內容屬性)：套用至 UI 中這些欄位的標籤不會限制資料使用。 [閱讀更多](../action/action-privacy.md)

* **傳送時間最佳化**&#x200B;文件已更新，以反映&#x200B;**[!UICONTROL 傳送時間在未來]**&#x200B;的全新限制為 **2 至 100 小時** (先前為 1 至 168 小時)，並記錄此功能支援的 AEP Hub 區域。 [閱讀更多](../building-journeys/send-time-optimization.md#use-send-time-optimization)


* **個人化最佳化模型**&#x200B;頁面已更新，以反映最新的模型改進，包括整合模型的運作方式、資料集需求、使用案例、關鍵假設和冷啟動行為。 請在[體驗決策](../experience-decisioning/ranking/personalized-optimization-model.md)和[Offer Decisioning](../offers/ranking/personalized-optimization-model.md)章節參閱更多資訊。

* **歷程仲裁排名公式**&#x200B;頁面已新增備註，說明排名公式僅適用於已購買&#x200B;**決策**&#x200B;附加元件產品的組織。 [閱讀更多](../conflict-prioritization/journey-ranking-formulas.md)

* 全新的&#x200B;**動態片段**&#x200B;頁面現已推出。 它記錄如何在 [!DNL Journey Optimizer] 中使用動態片段解析，根據輪廓屬性、資料集查詢或傳送時傳遞的內容資料，選取要在執行階段插入至訊息中的已發佈片段。 [閱讀更多](../content-management/dynamic-fragments.md)

## 2026 年 6 月 {#june-2026}

* **檢查並傳送直接郵件訊息**&#x200B;頁面已更新，以釐清直接郵件匯出時間與批次處理行為，包括固定的 4 小時 UTC 匯出排程、為何在一天內可以產生多個檔案、何時在歷程中執行&#x200B;**[!UICONTROL 更新輪廓]**，以及針對每日單一檔案情境的建議。 [閱讀更多](../direct-mail/test-send-direct-mail.md#dm-export-timing)

* 新的&#x200B;**歷程類型：選擇正確的類型**&#x200B;頁面現已推出。 它將所有歷程進入點 (讀取客群、客群鑑定、單一事件和商業事件) 與決策指南及功能相容性矩陣比較，以協助您為使用案例選取正確的類型。 [閱讀更多](../building-journeys/journey-types-selection.md)

* 全新&#x200B;**歷程與行銷活動**&#x200B;頁面現已推出。 它就歷程、動作行銷活動及 API 觸發的行銷活動，從執行型態、資料模型和使用案例進行比較，包括低延遲邊緣個人化的傳入管道啟用、多介面傳入傳送，以及使用協調行銷活動 (臨時客群構成、同盟資料) 的時機指引。 [閱讀更多](../start/journeys-vs-campaigns.md)

* **高輸送量模式**&#x200B;頁面已更新，以反映更廣泛的地區可用性：已授權使用高輸送量交易型訊息附加元件的組織，除瑞士之外，此功能現可在所有地區使用。 [閱讀更多](../campaigns/api-triggered-high-throughput.md)

* 新的&#x200B;**可互動輪廓和授權使用情況**&#x200B;區段已新增到&#x200B;**開始使用輪廓**&#x200B;頁面，作為此概念的單一事實來源，並在客群、行銷活動及決策區段中新增對應的參考。 [閱讀更多](../audience/get-started-profiles.md#engageable-profiles)

* **分割**&#x200B;活動文件已更新，記錄了每個子集設定中可用的&#x200B;**[!UICONTROL 區段代碼]**&#x200B;欄位，這能讓您為每個客群細分群體指派唯一識別碼，以用於追蹤和報告。 [閱讀更多](../orchestrated/activities/split.md)

* **設定目標選擇維度**&#x200B;頁面已更新，以記錄協調行銷活動中可用的兩種目標維度類型：內建的&#x200B;**輪廓定向維度** (無需設定) 以及基於關聯式結構描述的&#x200B;**自訂目標維度**。 [閱讀更多](../orchestrated/target-dimension.md)

* 已釐清&#x200B;**善用片段主題**&#x200B;文件，以明確記錄 5 個主題相容性限制 (包括 Adobe 預設主題限制)，並說明當電子郵件主題不是該片段關聯的主題之一時，片段插入會被封鎖。 [閱讀更多](../email/apply-email-themes.md#leverage-themes-fragment)

* **開始使用資料集**&#x200B;與&#x200B;**開始使用結構描述**&#x200B;頁面已更新，提供了為即時客戶輪廓啟用資料集和結構描述的指引，包括關鍵考量事項、停用資料集與停用其基礎結構描述的差異，以及 Adobe Experience Platform 規劃和最佳做法文件的連結。 [深入瞭解資料集](../data/get-started-datasets.md)與[深入瞭解結構描述](../data/get-started-schemas.md)

* 新的&#x200B;**開始使用 Adobe Journey Optimizer** 入門中心現已推出。 新使用者可以依角色選擇路徑、探索基礎知識，若已經完成新手入門，也可以直接前往日常作業區域，完全無需事先知道該從何處找起。 [閱讀更多](../../rp_landing_pages/get-started-landing-page.md)

* 全新的&#x200B;**從您的目標開始**&#x200B;頁面讓您從想要達成的目標開始操作，而不是從功能名稱開始。 這會將業務目標對應至設定、歷程、行銷活動、個人化、決策和報告中的推薦 [!DNL Journey Optimizer] 功能。 [閱讀更多](../start/ajo-use-case-guide.md)

* **開發人員快速入門**&#x200B;角色指南已更新，除了為每個區段提供更清晰的簡介，也改善了參考歷程並連結至關鍵實施頁面的&#x200B;**跨角色共同作業**&#x200B;標籤。 [閱讀更多](../start/path/developer.md)

* 已在&#x200B;**路徑實驗**&#x200B;文件中新增全新的&#x200B;**重新進入歷程時的路徑指派**&#x200B;子區段。 這釐清了同一輪廓多次進入同一個歷程版本，路徑指派都會保持永久性，但僅限於該歷程版本。 當發佈新歷程版本時，指派會重設，且歷程中的每個路徑實驗活動會套用獨立的隨機指派。 [閱讀更多](../building-journeys/path-experimentation.md#path-assignment)
* 在 [!DNL Journey Optimizer] 文件中對 **Adobe Experience Cloud** 的參考內容，已與 **[!DNL Adobe CX Enterprise]** 品牌保持一致。

* **`nowWithDelta()`日期函數**&#x200B;文件已更新，以釐清月底行為：當目標月份的天數少於目前日期的日數時，結果會標準化為該月份的最後有效日期。 [閱讀更多](../building-journeys/functions/date-functions.md#nowWithDelta)

* **傳遞能力快速入門**&#x200B;頁面已更新為新的&#x200B;**提供者，沒有每個收件者的 FBL** 子區段。 它會列出未傳回每個收件者垃圾郵件投訴的主要信箱提供者，包括 Gmail / Google Workspace、Apple iCloud 和 Corporate Microsoft 365 / Exchange Online，並說明為何使用這些服務的收件者預期會缺少黑名單項目。 [閱讀更多](../reports/deliverability.md#providers-no-fbl)

* **體驗決策現在可用於直接郵件管道。** 全新的&#x200B;**直接郵件中的批次決策**&#x200B;頁面說明如何使用決策引擎來個人化直接郵件擷取檔案，或匯出輪廓及其決策結果以用於下游系統。 **直接郵件**&#x200B;已在決策文件中新增為支援管道 (快速入門、建立決策原則、在訊息中使用決策原則、開始使用決策原則)，包括透過&#x200B;**[!UICONTROL 項目數]**&#x200B;欄位為每個輪廓傳回多個決策項目的功能。 [閱讀更多](../experience-decisioning/batch-decisioning-direct-mail.md)

* **歷程片段**&#x200B;文件不再標記為有限可用性。 此頁面現在包含清楚說明內容&#x200B;**[!UICONTROL 片段]**&#x200B;和 **AEM 內容片段**&#x200B;中的歷程片段的附註 (從所有三個頁面交叉連結)，以及包含支援&#x200B;**沙箱工具**、**稽核記錄**&#x200B;和&#x200B;**標記**&#x200B;的文件。 歷程片段也已新增至&#x200B;**開始使用歷程**&#x200B;頁面。 [閱讀更多](../building-journeys/journey-fragments.md)

* 已針對自訂驗證更新&#x200B;**外部資料來源**&#x200B;和&#x200B;**自訂動作**&#x200B;文件。 `tokenInResponse` 欄位現在可讓您指定當端點傳回 `access_token` 或 `id_token` 時，兩者是否作為驗證認證使用。 對於憑證型自訂驗證，`subType` 與 `aud` 欄位現在為必填欄位，權杖端點 `method` 必須為 `POST`，而且對「Azure Entra ID」的參考已更正為「Microsoft Entra ID」。 [閱讀更多](../datasource/external-data-sources.md#certificate-credential)

* **開始使用決策**&#x200B;頁面已更新，其中包含流程圖，其摘要端到端決策工作流程，從管理決策項目及設定選擇策略，到將決策原則內嵌至歷程或行銷活動。 [閱讀更多](../experience-decisioning/gs-experience-decisioning.md#process)

* **寄件者標題**&#x200B;文件現在釐清&#x200B;**[!UICONTROL 寄件者名稱]**&#x200B;和&#x200B;**[!UICONTROL 寄件者電子郵件]**&#x200B;必須同時設定或兩者皆留空，否則歷程和行銷活動無法發佈。 [閱讀更多](../email/header-parameters.md#sender-header)

## 2026 年 5 月 {#may-2026}

* 在視覺片段中使用動態內容時的限制和最佳做法，已合併至單一&#x200B;**管理片段中的條件式內容**&#x200B;區段中，以改善可讀性。 [閱讀更多](../email/use-visual-fragments.md#fragment-dynamic-content)

* 新增了兩個新的高階權限：**管理金鑰登錄** (可讓使用者檢視、建立、旋轉和撤銷金鑰登錄中的金鑰) 和&#x200B;**檢視金鑰登錄** (可讓使用者檢視金鑰登錄清單和金鑰詳細資訊)。 [閱讀更多](../administration/high-low-permissions.md#administration-permissions)

* **在訊息中使用決策原則**&#x200B;文件現在說明如何從行銷活動摘要檢視決策原則的完整結構，並複製 JSON 技術摘要至剪貼簿以進行疑難排解。 [閱讀更多](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

* 舊版&#x200B;**決策管理** [自動最佳化模型](../offers/ranking/auto-optimization-model.md)頁面已重新寫入，以符合更新後的決策文件，包括增強學習概觀、需求和限制、平衡最佳化與學習，以及 Thompson 抽樣詳細資訊。 [閱讀更多](../offers/ranking/auto-optimization-model.md)

* **發行說明**&#x200B;頁面已重新建構為主題型版面配置。 變更現在會依產品區域而非變更類型分組，並新增專屬的&#x200B;**可用性改進**&#x200B;區段。 即將推出項目會在各個主題中顯示為可展開的摺疊項目。 [閱讀更多](release-notes.md)

* **協調行銷活動的護欄和限制**&#x200B;頁面現在會記錄每個協調行銷活動的&#x200B;**管道活動**&#x200B;限制。 [閱讀更多](../orchestrated/guardrails.md#activities-limitations)

* **在沙箱之間複製 Journey Optimizer 物件**&#x200B;文件現在包含&#x200B;**協調行銷活動**&#x200B;的重要注意事項：匯入後，請在目標沙箱中複製行銷活動，並使用複製的內容來執行，以確保報告可正確擷取意見回饋和追蹤資料。 [閱讀更多](../configuration/copy-objects-to-sandbox.md#copy-to-sandbox)

* **重要術語**&#x200B;頁面已改寫：新增 6 個新術語、新增&#x200B;**衝突與優先順序術語**&#x200B;區段，以及新增&#x200B;**當術語看起來相似時**&#x200B;的消除歧義指南，用於四個常混淆的術語對。 已移除 Adobe Experience Platform 特定術語，並取代為連結至 Adobe Experience Platform 詞彙表的附註。 [閱讀更多](../start/terminology.md)

* **深層連結**&#x200B;文件已新增&#x200B;**製作深層連結**&#x200B;章節，詳細說明可用於電子郵件的兩個選項 (電子郵件設計工具 UI 和個人化編輯器程式碼) 以及可用於簡訊的 URL 函式語法。 **建立簡訊**&#x200B;頁面現在在內容製作流程中包含深層連結步驟。 [閱讀更多](../email/deeplinks.md)

* **Url** 協助程式參考已在個人化文件中更新專屬章節。 [閱讀更多](../personalization/functions/helpers.md#url)

* **執行中繼資料**&#x200B;協助程式文件已新增限制：傳入管道 (網頁、程式碼型體驗、應用程式內訊息、內容卡) 不支援該函式。 [閱讀更多](../personalization/functions/helpers.md#execution-metadata)

* 已新增&#x200B;**個人化方式**&#x200B;頁面，為 [!DNL Journey Optimizer] 中最常見的使用案例提供現成的個人化模式。 它涵蓋日期和時間方式 (目前的日期格式、到期倒數、計算前的天數、僅限時間的顯示、週末與平日偵測)、字串方式 (搭配變數指派使用 `replaceAll`) 以及條件式遞補方式 (使用 `isEmpty` 的空白欄位遞補)。 [閱讀全文](../personalization/personalization-recipes.md)

* 已更新&#x200B;**個人化語法**&#x200B;文件，其中擴充了簡介，澄清 Handlebars (`{{...}}`) 與 PQL (`{%= ... %}`) 語法之間的差異，包括使用表格、跳脫字面雙引號指引，以及&#x200B;**適用於特殊屬性索引鍵的新 PQL 語法規則**&#x200B;章節，涵蓋保留關鍵字、連字屬性索引鍵及數值事件識別碼。 還更正了反引號跳脫的輔助：連字欄位名稱可以直接在 `{{...}}` 區塊中參照；只有反引號語法會失敗。 [閱讀全文](../personalization/personalization-syntax.md)

* **日期時間函式**&#x200B;文件已新增現實範例：針對 `dateDiff` 的倒計時模式、針對 `dayOfWeek` 的週末與平日條件式 (附註說明如何使用歷程條件活動來路由使用案例)，以及結合了 `extractHours` 及 `extractMinutes` 與前導零防護的純時間顯示模式。 [閱讀全文](../personalization/functions/dates.md)

* **字串函式**&#x200B;文件已更新 `replaceAll` 的新範例，說明如何將結果指派給 `{% let %}` 變數，以便在同一範本的多個運算式中重複使用。 [閱讀全文](../personalization/functions/string.md#replace-all)

* 已更新&#x200B;**陣列函式**&#x200B;文件，其中包含新的&#x200B;**反覆處理陣列**&#x200B;章節，以記錄 Handlebars `{{#each}}` 區塊協助程式，並包含備註以說明僅個人化編輯器支援 `{{#each}}`，且無法在歷程條件活動內使用。 [閱讀全文](../personalization/functions/arrays-list.md#each-loop)

* **開始使用資料集**&#x200B;頁面已在系統資料集章節中更新&#x200B;**傳入**&#x200B;項目，以記錄 _AJO 傳入活動事件資料集_。 已新增附註，用於說明輪廓必須至少從 [!DNL Journey Optimizer] 傳送一則訊息，才能在此資料集中擷取傳入的訊息。 [閱讀全文](../data/get-started-datasets.md#system-datasets)

* **匯出訊息內容**&#x200B;文件已新增&#x200B;**訊息匯出常見問題集** (個人化內容、影像和媒體、追蹤連結、PII、保留、使用案例等)，以及簡訊和電子郵件的&#x200B;**範例匯出的 JSON**&#x200B;範例。 [閱讀全文](../configuration/message-export.md)

* 新的 **AJO 訊息匯出結構描述**&#x200B;頁面會記錄 AJO 訊息匯出資料集中的每個欄位，其中包含匯出的電子郵件和簡訊承載的資料類型和階層。 [閱讀全文](../configuration/message-export-schema.md)

* 已新增&#x200B;**個人化電子郵件中的 URL** 頁面，整合動態 URL 個人化、完整/基本 URL 個人化、URL 追蹤參數個人化和關鍵護欄的相關指引。 [閱讀全文](../email/url-personalization.md)

* 新的&#x200B;**業務規則查詢**&#x200B;區段已新增到查詢範例頁面，提供資料湖查詢以檢查特定日期後特定歷程上由於歷程頻率上限排除所放棄的所有輪廓。 查詢包含 `eventCodeReason` 欄位，以識別輪廓是否因為達到上限 (`CAP_REACHED`) 或優先順序較低 (`LOWER_PRIORITY`) 而被排除。 [閱讀全文](../reports/query-examples.md#business-rules-queries)

* 已更新&#x200B;**歷程屬性**&#x200B;文件，以記錄歷程屬性面板中的新&#x200B;**目前歷程承載大小**&#x200B;指標。 此唯讀欄位顯示與設定限制 (例如 2 MB 中的 1.5 MB) 相比的目前歷程承載大小，可幫助您在發佈之前監視歷程複雜度並避免與大小相關的發佈錯誤。 [閱讀全文](../building-journeys/journey-properties.md#journey-payload-size)

## 2026 年 4 月 {#april-2026}

* **變更維度**&#x200B;活動文件已更新，以釐清當活動使用外部連接並保留維度變更步驟的所有記錄時，新目標維度中無相符輪廓的記錄會在訊息傳送時默默地排除。 [閱讀全文](../orchestrated/activities/change-dimension.md)

* **將 CC 欄位新增至電子郵件**&#x200B;文件中的護欄已增強。 它們現在已明確規定，系統不會根據同意或抑制檢查 CC 位址，而傳送至 CC 位址之電子郵件的開啟和點進次數，均會計入傳送分析的總開啟和點進次數。 [閱讀全文](../configuration/cc-email-field.md)

* **管道活動**&#x200B;文件已更新，其中包含新的&#x200B;**行銷與交易型訊息**&#x200B;區段，說明兩個管道類別之間的行為差異：選擇加入需求、業務規則應用、管道設定類型和建議的使用案例。 [閱讀全文](../orchestrated/activities/channels.md#marketing-vs-transactional)

* **分支活動**&#x200B;文件中已擴充&#x200B;**範例**&#x200B;區段，說明如何使用分支活動在單一行銷活動執行中將客群分割到兩個平行電子郵件分支 (一個行銷活動和一個交易型) 中。 [閱讀全文](../orchestrated/activities/fork.md#fork-examples)

* **建立客群活動**&#x200B;文件中已擴充新範例，說明如何使用規則產生器依訂閱方案屬性篩選輪廓。 [閱讀全文](../orchestrated/activities/build-audience.md#build-audience-examples)

* **開始使用協調的行銷活動**&#x200B;頁面會在&#x200B;**協調的行銷活動內含哪些內容？**&#x200B;中記錄入門層級&#x200B;**建立客群 → 分支 → 管道 A + 管道 B** 模式，並交叉參考分支活動以及行銷與交易型訊息頁面。 [閱讀全文](../orchestrated/gs-orchestrated-campaigns.md#gs-ms-campaign-inside)

* **使用進階 HTML 編輯器編輯電子郵件內容**&#x200B;頁面已從「內容管理」區段移至文件的&#x200B;**電子郵件**&#x200B;區段。 此頁面現在說明，進階 HTML 編輯器可在電子郵件設計工具中用於電子郵件訊息以及電子郵件內容範本。 [閱讀全文](../email/email-expert-mode.md)

* **開始和監視協調的行銷活動**&#x200B;文件已新增區段，以詳細說明內部發佈時間執行順序，以及行銷活動生命週期狀態表、發佈前檢查清單，以及非週期性行銷活動的傳送確認警告。 [閱讀全文](../orchestrated/start-monitor-campaigns.md#publication-sequence)

* **儲存客群**&#x200B;活動文件已新增附註，以釐清儲存客群活動一律在發佈時於訊息活動之前執行。 [閱讀全文](../orchestrated/activities/save-audience.md)

* 已在&#x200B;**協調的行銷活動常見問題集**&#x200B;中新增三個問答：發佈時內部會發生什麼情況、發佈後可能不會傳送訊息的 7 點原因檢查清單，以及輪廓快照查詢與即時輪廓解析的差異。 [閱讀全文](../orchestrated/orchestrated-campaigns-faq.md)

* 已在歷程疑難排解文件中新增&#x200B;**[因封鎖歷程執行個體而捨棄的事件](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)**&#x200B;區段，說明 `maxInstanceStackEventsReached` 捨棄的原因、發生時間以及如何降低其風險。 護欄和步驟事件欄位清單頁面也已相應更新。

* **利用決策原則中的片段**&#x200B;文件現在包含&#x200B;**電子郵件**&#x200B;管道的護欄附註：**[!UICONTROL 模擬內容]**&#x200B;不顯示決策項目的運算式片段，而&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;和已啟用的行銷活動則會顯示。 此頁面也指出&#x200B;**[!UICONTROL 視覺片段]**&#x200B;無法指派給決策項目，在這種情況下僅支援&#x200B;**運算式片段**。 [閱讀全文](../experience-decisioning/fragments-decision-policies.md)

## 2026年3月 {#march-2026}

* **使用體驗決策預覽程式碼型體驗**&#x200B;的文件現已釐清&#x200B;**[!UICONTROL 模擬內容]**&#x200B;僅為內容預覽。 製作預覽中不會模擬即時 Edge 請求的內容資料。 [閱讀全文](../code-based/test-code-based.md#preview-code-based)

* **使用 Adobe Experience Platform 資料**&#x200B;文件已更新：護欄不再指出資料集查詢無法鏈結，這反映了目前的產品行為。 [閱讀全文](../data/lookup-aep-data.md)

* **更新輪廓**&#x200B;活動文件已更新，以記錄在單一動作中最多更新五個輪廓屬性的支援。 [閱讀全文](../building-journeys/update-profiles.md)

* 已更新&#x200B;**讀取客群**&#x200B;活動和&#x200B;**歷程屬性**&#x200B;文件，以釐清永久性定期歷程的 91 天歷程生命週期。 排程區段現在會明確確認沒有結束日期的週期性歷程在超過 91 天後仍會維持即時狀態，而全域逾時常見問題集已擴充，以區分 91 天輪廓 TTL 和 91 天報告期間。 [閱讀全文](../building-journeys/read-audience.md#schedule)

* 已更新&#x200B;**資料集查詢**&#x200B;活動文件，以釐清必須在進階模式中設定查詢金鑰，`@datasetLookup{}` 語法才能用於下游條件活動。 已新增疑難排解章節，其中包含解決「找不到資料集查詢」錯誤的指引。 [閱讀全文](../building-journeys/dataset-lookup.md#troubleshooting)

* **日期時間函式**&#x200B;文件已更新，其中包含新範例，說明如何從內容事件屬性格式化時間戳記，包括 `toDateTime()` 需求、數值事件 ID 的反引號語法，以及 PQL「不相符輸入」錯誤的常見錯誤圖說文字。 [閱讀全文](../personalization/functions/dates.md#format-date)

* 已更新&#x200B;**協調的行銷活動護欄和限制**&#x200B;以及&#x200B;**開始使用來源連接器**&#x200B;文件，以釐清針對檔案型變更資料擷取，`_change_request_type` 欄位為必填項，其值必須為小寫 `u` (更新插入) 或 `d` (刪除)，而非大寫。 [閱讀全文](../orchestrated/guardrails.md)

* **新增連結與追蹤訊息**&#x200B;文件已更新，其中包含如何產生追蹤識別碼 (urlID) 的指引：唯有 URL 和標籤皆為唯一時，才會指派唯一的 urlID。 若要在多個電子郵件中追蹤同一個 URL (或在一封電子郵件中追蹤多次)，使用者必須針對每個類似的 URL 使用唯一標籤；否則，[!DNL Journey Optimizer] 無法判斷所點按的連結。 [閱讀全文](../email/message-tracking.md#track-across-multiple-emails)

* **建立測試輪廓**&#x200B;文件已更新，其中包含有關身分識別描述項需求的重要附註：刪除並重新建立資料集時，結構描述必須在主要身分識別欄位上保留正確的身分識別描述項。 如果沒有它，即使擷取成功完成，擷取的輪廓也不會標記為 `testProfile = true`。 已新增疑難排解檢查清單。 [閱讀全文](../audience/creating-test-profiles.md)

* 已更新&#x200B;**讀取客群**&#x200B;活動文件，以釐清&#x200B;**商業事件**&#x200B;活動是讀取客群必須是歷程中第一個活動這一規則的例外狀況。 也新增了參照&#x200B;**最佳化**&#x200B;活動的附註，作為控制客群目標定位的進階替代方案。 [閱讀全文](../building-journeys/read-audience.md)

* 在歷程中&#x200B;**使用波段傳送**&#x200B;功能現在通常可用。 已從文件中移除「有限可用性」標幟。 [閱讀全文](../delivery/send-using-waves.md)

* **跳轉**&#x200B;活動文件已擴充新的設計策略區段 (**小型子歷程**)，說明如何將複雜的端到端流程分解為透過跳轉活動連線的較小且重點突出的子歷程。 [閱讀全文](../building-journeys/jump.md#jump-strategy)

* **標記**&#x200B;文件已更新，其中包含使用標記類別作為複雜命名慣例的替代方法的指引。 新章節說明如何為可擴充的歷程管理設定標記類別。 [閱讀全文](../building-journeys/tags.md)

* **關於資料來源**&#x200B;文件現在包含新章節，可協助從業人員在三種資料存取策略之間進行選擇：透過自訂動作存取外部資料、使用未針對輪廓啟用的資料集，或使用已啟用輪廓的資料集。 每個選項都說明利弊權衡和建議的使用案例。 [閱讀全文](../datasource/about-data-sources.md#data-access-strategy)

* **推播通知設計**&#x200B;文件已更新，其中包含釐清 iOS 上通用連結行為的附註：如果通知 URL 註冊為通用連結，則無論所選的網頁 URL 動作為何，都會開啟關聯的應用程式。 已新增如何強制開啟瀏覽器的指引。 [閱讀全文](../push/design-push.md)

* Decisioning 文件現在提供新的&#x200B;**監視您的 AI 模型**&#x200B;頁面。 說明如何直接在 [!DNL Journey Optimizer] 中追蹤個人化最佳化模型的健康情況、訓練狀態和效能。 [閱讀全文](../experience-decisioning/ranking/ai-model-observability.md)

* 電子郵件範本的&#x200B;**進階 HTML 編輯器** (專家模式) 現在可在「有限可用性」中取得。 文件頁面現可公開存取。 此功能可讓您直接從電子郵件設計工具檢視及編輯電子郵件內容範本的原始 HTML 來源。 [閱讀全文](../email/email-expert-mode.md)

* 已更新 **URL 追蹤**&#x200B;和&#x200B;**歷程疑難排解**&#x200B;文件，以記錄 `context.system.source.actionId` 在已關閉歷程中的行為。 已關閉或未重新發佈的歷程可能會在追蹤 URL 時產生空白的 `{}` 預留位置。 已新增指引，說明如何透過重新發佈歷程或移除受影響參數來解決問題。 [閱讀全文](../email/url-tracking.md)

* **Adobe Experience Platform 資料來源**&#x200B;文件已更新附註：資料來源設定中僅支援 XDM 個別輪廓型結構描述。 [閱讀全文](../datasource/adobe-experience-platform-data-source.md)

* **資料集存留時間 (TTL) 護欄**&#x200B;文件已增強，並新增常見問題集項目，以清楚識別哪些資料集須遵守 TTL。 TTL 僅適用於時間序列資料集；記錄類型資料集，例如實體資料集、分類資料集和決策物件存放庫，不受 TTL 約束，也不會受到護欄推出的影響。 [閱讀全文](../data/datasets-ttl.md)

* 已更新&#x200B;**歷程屬性**&#x200B;和&#x200B;**暫停歷程**&#x200B;文件，以記錄歷程技術詳細資料中現在可用的新暫停和恢復欄位。 除了現有的 `pausedJourneySettings` 區塊之外，**複製技術詳細資料**&#x200B;按鈕現在還包含 `lastPausedAt`、`lastPausedBy`、`lastPausedById`、`lastResumedAt`、`lastResumedBy` 和 `lastResumedById`。 **暫停歷程**&#x200B;頁面也新增了一個區段，說明如何直接從歷程屬性檢視暫停和繼續時間戳記。 [閱讀全文](../building-journeys/journey-properties.md)

## 2026 年 2 月 {#february-2026}

* 決策管理現在提供新頁面。 其中列出使用個人化編輯器個人化產品建議內容 (呈現) 時支援的所有運算子、協助程式和函式。 使用此清單可避免執行階段錯誤。 在產品建議決策中個人化內容時，僅支援已記錄的函式。 [閱讀全文](../offers/offer-library/personalization-editor-supported-functions.md)

* 已更新電子郵件的&#x200B;**建立決策原則**&#x200B;和&#x200B;**在訊息中使用決策原則**&#x200B;文件：附註說明當電子郵件正文中的多個決策原則可以選取相同產品建議時，引擎會刪除重複產品建議 (每個版位都會收到不同的產品建議)。 若要在多個版位 (例如頁首和頁尾) 顯示相同產品建議，請使用&#x200B;**重複使用決策輸出**。 [閱讀全文](../experience-decisioning/create-decision-policy.md)

* 已更新決策項目頁面，其中包含推播管道和自訂事件上限的相關資訊。 [閱讀全文](../experience-decisioning/items.md#capping)

* **歷程中的體驗事件查詢**&#x200B;文件已新增棄用時間表：自 2026 年 4 月 1 日起，過去 90 天內未曾在歷程運算式中使用體驗事件屬性的組織將無法再存取此功能。 常見問題集現在聚焦於淘汰時間表及受影響人群，而體驗事件結構描述頁面已同步更新替代方法的直接連結。 [閱讀全文](../building-journeys/exp-event-lookup.md)

* 已使用 Adobe Experience Platform 資料更新&#x200B;**決策**&#x200B;文件中的&#x200B;**資料集查詢**：支援的管道護欄現在指出資料集查詢適用於所有可使用決策功能的管道 (歷程中的程式碼型體驗、電子郵件、推播、簡訊和內容決策活動)。 已從決策規則、排名公式和決策項目頁面中移除有限可用性和公開 Beta 版附註。 [閱讀全文](../experience-decisioning/aep-data-exd.md)

* 外部系統整合頁面已更新自訂資料來源和自訂動作的連結，並釐清輸出 Proxy 為從&#x200B;**自訂動作**&#x200B;到外部系統的傳出呼叫提供靜態 IP。 [閱讀全文](../configuration/external-systems.md)

* 歷程試運行文件已釐清：步驟事件屬性 `inDryRun` 和 `dryRunID` 現已記錄它們在試運行模式中傳回 `true`/執行個體 ID，並在測試或即時歷程中傳回 `null`。 已相應地更新報告查詢中排除試運行步驟事件的指引。 [閱讀全文](../building-journeys/journey-dry-run.md)

* **網頁推播**&#x200B;現已正式推出。 推播通知文件已重新建構並據此更新 (快速入門、設計、傳送、建立)。 [閱讀全文](../push/get-started-push.md)

* 網頁推播設定頁面現已在文件中提供。 [閱讀全文](../push/push-configuration-web.md)

* 已更新有關在決策中使用片段的文件：「片段」及「決策」區段中已新增附註，且決策原則頁面中的片段已更新。 [閱讀全文](../experience-decisioning/fragments-decision-policies.md)

* 簡訊 Webhook 文件已更新：Twilio Webhook 內容已移除。 [閱讀全文](../mobile/mobile-webhook.md)

* **將影像轉換為內容範本**&#x200B;文件已增強，並包含擴充的護欄和推薦、常見使用案例，以及關於將影像設計轉換為可編輯的 HTML 內容範本的更清楚指引。 它還提到您現在可以使用主題作為轉換的輸入。 [閱讀全文](../content-management/image-to-html.md)

* 已更新決策移轉 API 文件。 [閱讀全文](../experience-decisioning/decisioning-migration-api.md)

* **內容決策**&#x200B;活動現已正式推出。 內容決策活動頁面已更新，其中包含步驟事件中可用的決策資料區段。 [閱讀全文](../building-journeys/content-decision.md)

* 「忠誠度挑戰」章節新增了忠誠度挑戰 API 文件的連結 (快速入門、建立挑戰、建立任務、存取忠誠度挑戰)。 [閱讀全文](../loyalty-challenges/get-started.md)

* 行銷活動建立精靈文件中的支援管道資訊已更正。 「開始使用管道」和「協調的行銷活動常見問題集」頁面已更新相應內容。 [閱讀全文](../campaigns/get-started-with-campaigns.md)

* 已更正權限文件中有關&#x200B;**歷程管理**&#x200B;和&#x200B;**核准**&#x200B;權限的內容。 [閱讀全文](../administration/ootb-permissions.md)

* 已更新 AEM (Adobe Experience Manager) 整合文件，並修訂名稱 (AEM 動態內容和 AEM 片段)。 [閱讀全文](../integrations/aem-fragments.md)

* 排除清單中已新增排除原因：**UnsubscribeLinkNotValid** (錯誤碼 050081)。 當 List-Unsubscribe mailTo 主旨長度大於 RFC 的 998 個字元限制時，會產生此排除。 [閱讀全文](../reports/exclusion-list.md)

* formatDate 協助程式函式文件已增強，其中指出該函式需要日期時間欄位類型 (而非字串)，並且提供多個範例：格式化日期時間欄位、將字串轉換為日期優先、具有日期名稱的完整日期、來自系統時間的動態日期，以及包含小寫輸出的星期幾格式。 [閱讀全文](../personalization/functions/dates.md#format-date)

* 文字版本的電子郵件文件已增強，並提供完整的使用案例指引，包括何時使用自訂純文字與自動同步的決策標準、真實案例的實用範例，以及包含常見問題的常見問題集章節。 [閱讀全文](../email/text-version-email.md#when-to-use)

* 電子郵件設計工具主題文件已更新，其中包含有關網頁字型支援限制和遞補字型重要性的資訊。 [閱讀全文](../email/apply-email-themes.md#themes-guardrails)

* 執行中繼資料協助程式文件新增了一項限制，明確說明不會為動作中排除的輪廓擷取中繼資料。 [閱讀全文](../personalization/functions/helpers.md#execution-metadata)

* 已更新程式碼型實施範例文件，並在 propositionAction 中新增權杖欄位，以便在 Decisioning 中準確追蹤和歸因。 [閱讀全文](../code-based/code-based-implementation-samples.md#client-side-how)

* 已在 URL 追蹤和取消清單訂閱文件中新增附註，以釐清附加至 URL 的 URL 追蹤參數順序是隨機的且無法控制。 [閱讀全文](../email/url-tracking.md)

## 2026 年 1 月 {#january-2026}

* 授權使用儀表板文件已進行釐清，並更新有關&#x200B;**可互動輪廓**&#x200B;的指南，包括定義詳細資訊和疑難排解指南。 [閱讀全文](../audience/license-usage.md#what-is-engageable-profile)

* 已在電子郵件設計工具主題文件中新增附註，以釐清網頁字型支援限制。 [閱讀全文](../email/apply-email-themes.md#themes-guardrails)

* 已新增護欄區段，以記錄歷程承載大小驗證，包括警告和錯誤臨界值，以及如何最佳化歷程的指引。 [閱讀全文](../start/guardrails.md#journey-payload-size)

* 已更新決策護欄文件，以新增決策項目大小限制 (對於包含最多 30 個屬性的項目，為 1KB)。 [閱讀全文](../experience-decisioning/decisioning-guardrails.md)

* 已在決策原則建立文件中新增附註，以告知使用者一旦建立決策原則，任何變更最多可能需要 15 分鐘傳播至所有資料區域，而加拿大最多可能需要 30 分鐘。 [閱讀全文](../experience-decisioning/create-decision-policy.md#review)

* 片段文件中已新增附註，以警告當片段中的按鈕標籤和 URL 都可編輯時，追蹤資料集會記錄 URL 值，而非標籤值。 [閱讀全文](../content-management/customizable-fragments.md#visual)

* 推出新的頁面，說明從決策管理移轉至決策的好處，包括即將推出的移轉工具 API 的相關資訊。 [閱讀全文](../experience-decisioning/migrate-to-decisioning.md)

* 新增護欄，說明查詢資料集僅適用於資料集沙箱所在區域的傳入邊緣型啟用。 [閱讀全文](../data/lookup-aep-data.md#guidelines)

* 協調的行銷活動管道設定文件已新增區段，說明如何在 URL 追蹤參數中使用內容屬性 (例如行銷活動 ID、名稱和動作詳細資訊)，以用於分析和報告用途。 [閱讀全文](../orchestrated/channel-config.md#url-tracking)

* 內容最佳化文件已重新建構，以提高清晰度。 主要最佳化頁面已分割成四個重點子頁面：快速入門頁面、目標定位的專屬頁面、實驗頁面，以及結合兩種方法的頁面。 [閱讀全文](../content-management/gs-message-optimization.md)

* 已從三個歷程警示 (已發佈歷程、歷程已完成和已觸發自訂動作頻率上限) 中移除有限可用性附註，因為這些功能現在已普遍可用。 [閱讀全文](../reports/alerts.md)

* 測試、驗證及核准登陸頁面已新增區段，包括測試功能概觀、常見問題集、含導覽連結的決策樹，以及含文件連結的增強術語。 [閱讀全文](../../rp_landing_pages/test-landing-page.md)

* 個人化語法文件中已新增區段，以釐清如何在個人化運算式中使用保留關鍵字。 在 XDM 結構描述中作為欄位名稱使用時，某些 PQL 關鍵字 (例如 `next`、`last` 和 `this`) 必須使用反引號逸出。 [閱讀全文](../personalization/personalization-syntax.md#reserved-keywords)

* [行銷活動快速入門](../campaigns/get-started-with-campaigns.md)和[管理行銷活動](../campaigns/manage-campaigns.md)頁面已重新建構，資訊架構已改進，包括包含特定類型指南的全面工作流程、增強型行銷活動類型比較，以及整合狀態表格。

* Journeys 登陸頁面已重新設計，以協助上線新的 6 步驟工作流程、增強歷程類型比較，以及經改進的整個文件導覽。 [閱讀全文](../building-journeys/journey.md)

* 新增了詳細區段，協助使用者在設定直接郵件的檔案路由時，產生 SFTP 驗證的 Base64 編碼 OpenSSH 私密金鑰，以避免連線錯誤。 [閱讀全文](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* 已在子網域委派文件中新增附註，告知使用者在嘗試委派給 Adobe 之前，需等待 24 到 48 小時讓 DNS 傳播完成。 [閱讀全文](../configuration/delegate-subdomain.md#set-up-subdomain)
