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
source-git-commit: c910664b343f8143579e4a22ff101d38476c4585
workflow-type: tm+mt
source-wordcount: '2841'
ht-degree: 85%

---

# 文件更新 {#latest-updates}

此頁面列出[!DNL Journey Optimizer]檔案中的所有最新變更，以及與每月發行功能和改進相關的更新。

## 2025 年 11 月 {#november-2025}

* 已在資料集查詢護欄中新增附註，以指定查詢無法鏈結在一起。 [閱讀全文](../data/lookup-aep-data.md#guidelines)

* WhatsApp和LINE頻道現在可用於「動作」行銷活動。 [閱讀全文](../campaigns/campaign-content.md)

* 登入管理檔案中已新增有關歷程處理速率的完整新區段，涵蓋設定檔進入率、事件和歷程中的對象資格、等待活動影響以及動作活動影響。 [閱讀全文](../building-journeys/entry-management.md#journey-processing-rate)

* 在設計電子郵件訊息時，系統現在會檢查金鑰設定並顯示警告和錯誤的警報。 「護欄」頁面已新增有關電子郵件警示和驗證要求的資訊。 [閱讀全文](../email/create-email.md#check-email-alerts)

* 先前建立之優惠方案的頻率上限無法啟用或停用的警告說明，已從「將限制新增至優惠方案」頁面中移除。 [閱讀全文](../offers/offer-library/add-constraints.md#capping)

* 現在提供有關如何使用歷程步驟事件的檔案。 [閱讀全文](../reports/journey-step-events-overview.md)

* 提供三個新的歷程警報：歷程已發佈、歷程已完成，以及自訂動作上限已觸發。 [閱讀全文](../reports/alerts.md#journey-alerts)

## 2025 年 10 月 {#october-2025}

* 您現在可以使用影像轉換為HTML轉換工具，將影像轉換為HTML範本。 [閱讀全文](../email/image-to-html.md)

* 現在提供Adobe Journey Optimizer發行週期的相關資訊。 [閱讀全文](releases.md)

* 全新歷程常見問題頁面已推出。 [閱讀全文](../building-journeys/journey-faq.md)

* 監視您的自訂動作功能現已可用。 [閱讀全文](../action/reporting.md)

* API觸發的行銷活動現在可使用高輸送量模式。 [閱讀全文](../campaigns/api-triggered-high-throughput.md)

* 現在提供歷程的錯誤代碼參考。 [閱讀全文](../building-journeys/error-codes-reference.md)

* Journey Optimizer Experimentation Accelerator檔案已可供參考。 [閱讀全文](../content-management/experiment-accelerator-gs.md)

* **formatDate**&#x200B;協助程式函式檔案已新增新區段。 本節說明關鍵模式符號（例如y、Y、M、d和D）的意義。[瞭解詳情](../personalization/functions/dates.md#pattern-characters)

* 決策排名公式區段已新增PQL範例，說明如何根據設定檔的郵遞區號和年收入提升優惠方案。 [閱讀全文](../experience-decisioning/ranking/ranking-formulas.md#ranking-formula-examples)

* 歷程測試模式區段已新增限制，以提及測試模式不支援自訂上傳對象屬性擴充。 [閱讀全文](../building-journeys/testing-the-journey.md#important_notes)

* 已在[決定管理護欄和限制](../offers/decision-management-guardrails.md#configurations)及[決定護欄和限制](../experience-decisioning/decisioning-guardrails.md#configurations)頁面中新增區段，以指定支援的組態數上限(20,000)，此數目對應於您沙箱中存在的上限規則總數。

* 在歷程的「條件」活動區段中新增附註，以記錄包含兩個以上跨裝置身分的設定檔的條件評估將會失敗。 [閱讀全文](../building-journeys/condition-activity.md)

* 已新增一個頁面，說明如何使用同意政策，根據客戶的選擇尊重其偏好，同時尊重其同意。 [閱讀全文](../action/preference-center.md)

* 「輪廓快速入門」和「護欄」頁面已新增附註，以指定在擷取資料時，電子郵件會區分大小寫，這意味著在定位對應的收件者時，可能會建立並使用重複的輪廓。[閱讀全文](../audience/get-started-profiles.md)

* 已在個人化編輯器中引進新的 `render` 屬性。將其設定為 `false`，以隱藏運算式片段的內容。[閱讀全文](../personalization/use-expression-fragments.md#use-expression-fragment)

* 在區段中新增了護欄清單，說明如何在決策原則中善用附加到決策項目的片段。[閱讀全文](../experience-decisioning/create-decision.md#fragments-guardrails)

* 新增資料集查詢的最佳做法：隨時切換以避免索引問題，並了解批次刪除如何影響查詢資料。[閱讀全文](../data/lookup-aep-data.md#guardrails--guidelines-guidelines)

* 新增了限制，以說明搭配補充識別碼使用讀取客群歷程時，僅支援統一輪廓服務客群。[閱讀全文](../building-journeys/supplemental-identifier.md#guardrails--limitations-guardrails)

* Experimentation Accelerator 的文件已重新放置到另一個集合。[閱讀全文](https://experienceleague.adobe.com/zh-hant/docs/experimentation-accelerator/using/overview)

## 2025 年 9 月 {#september-2025}

* 「護欄和限制」頁面已新增傳入管道區段，以收集套用至網頁、應用程式內、程式碼型體驗和內容卡管道的所有限制。其中包括所有傳入請求的尖峰量限制 (每秒 5,000 個傳入請求)，以及最多 500 個作用中的傳入動作。[閱讀全文](../start/guardrails.md#inbound-guardrails)

* 已針對協調行銷活動發行「常見問題集」頁面。[閱讀全文](../orchestrated/orchestrated-campaigns-faq.md)

* 已在歷程步驟事件文件中新增疑難排解章節，其中包含最常捨棄事件類型的定義、常見原因和疑難排解步驟。[閱讀全文](../reports/sharing-field-list.md#troubleshoot-discarded-event-types-in-journey_step_events)

* 有關如何在歷程中使用補充識別碼的文件現在包含一個表格，詳細說明當使用補充識別碼在歷程中套用退出條件時，輪廓的行為方式。[閱讀全文](../building-journeys/supplemental-identifier.md#exit-criteria)

* 疑難排解章節已新增到暫停歷程中了解的輪廓捨棄。[閱讀全文](../building-journeys/journey-pause.md#troubleshoot-profile-discards-in-paused-journeys)

* 結構描述概觀文件中已新增資訊，以區分用於協調行銷活動的標準和關聯式結構描述。[閱讀全文](../data/gs-data.md)

* 已在決策和決策管理文件中新增有關成功訓練[自動最佳化](../experience-decisioning/ranking/auto-optimization-model.md)和[個人化最佳化](../experience-decisioning/ranking/personalized-optimization-model.md)模型的需求的資訊。

* 已澄清互動式訊息執行 REST API 呼叫具有 60 秒的逾時時間，且內部會重試以確保傳送。[閱讀全文](../campaigns/trigger-campaigns.md)

* 已更新「決策項目集合」頁面，以釐清定義規則時 **CONTAINS** 運算子的行為。[閱讀全文](../experience-decisioning/collections.md)

* 已更新「指派優先順序分數」頁面，其中包含在&#x200B;**動作**&#x200B;活動中定義傳入頻道動作的優先順序分數的特定步驟。[閱讀全文](../conflict-prioritization/priority-scores.md#priority-action)

## 2025 年 8 月 {#august-2025}

* 新增了一個頁面，其中列出使用 [!DNL Journey Optimizer] 設計無障礙電子郵件和登陸頁面內容的最佳做法。[閱讀全文](../email/accessible-content.md)

* 已更新歷程中的補充識別碼文件，其說明如下：

   * 將補充識別碼新增到結構描述後，必須建立新事件 (適用於事件觸發的歷程) 或新欄位群組 (適用於讀取客群歷程)。現有實體不會自動重新整理，且將無法識別新識別碼。

   * 補充識別碼不會根據資料使用標籤和實作 (DULE) 原則驗證，並且在歷程中的資料治理檢查期間不予考慮。

[閱讀全文](../building-journeys/supplemental-identifier.md)

* 行銷活動中的最佳化頁面已更新，以反映最佳化，現在也可用於歷程的事實。[閱讀全文](../campaigns/campaigns-message-optimization.md)

* 已新增教學課程影片的連結，說明如何在行銷活動中運用訊息最佳化。[閱讀全文](../campaigns/campaigns-message-optimization.md)

## 2025 年 7 月 {#july-2025}

* 行銷活動介面目前提供兩種個別分頁： **動作**&#x200B;和&#x200B;**觸發的 API**。 據此已更新說明文件，已將每種行銷活動類型的資訊整理到專屬章節，以便改善清晰度和易用性。 [閱讀全文](../campaigns/get-started-with-campaigns.md)

* [開始使用子網域委派](../configuration/about-subdomain-delegation.md)和[委派子網域](../configuration/delegate-subdomain.md)頁面已更新，以便更清楚地呈現不同的委派方法以及設定它們的步驟。

* 「片段」區段已新增附註，指定在歷程或行銷活動中啟用追蹤時，如果連結存在於片段中，且此片段用於訊息中，則會追蹤這些連結，例如訊息中包含的所有其他連結。[了解更多](../content-management/create-fragments.md#content)

* 在 Journey Optimizer 中套用至子網域委派的護欄和限制已擴充並整合至一個專用區段。[閱讀全文](../configuration/delegate-subdomain.md#guardrails)

* 「建立遞補優惠」和「建立決定」頁面已新增附註，其中提及遞補優惠應包含決定內使用的所有代表。[閱讀全文](../offers/offer-library/creating-fallback-offers.md)

* 已擴充套用至片段的護欄。[閱讀全文](../start/guardrails.md#fragments-guardrails)。

* 已新增附註，以指定新增至訊息的連結在 25 個月後到期，而鏡像頁面的連結在 90 天後到期。[閱讀全文](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

## 2025 年 6 月 {#june-2025}

* 新增章節，說明如何使用 HTML 元件，在可自訂的片段中新增及使用富文字 (例如分行符號、粗體、斜體等)。[閱讀全文](../content-management/customizable-fragments.md#rich-text)

* 決策部分已更新，其中包含專用於建立 AI 模型的特定區段。[閱讀全文](../experience-decisioning/ranking/ai-models.md)

* 新增在 journeyStep 事件動作中使用 `actionExecutionTime` 欄位的建議。[閱讀全文](../reports/sharing-execution-fields.md#actionexecutiontime-actionexecutiontime-field)

* 已新增關於 `messageID` 的備註，該備註可能不會對於每個個別傳遞都是唯一的。[閱讀全文](../data/datasets-query-examples.md)

* 新增有關資料衛生操作中歷史事件管理的建議。[閱讀全文](../privacy/data-hygiene.md#recommendations-data-hygiene-recommendations)

* 新增不支援在沙箱之間移轉之登陸頁面的護欄。[閱讀全文](../configuration/copy-objects-to-sandbox.md#general-best-practices-global)

* 針對自訂動作的自訂驗證不支援巢狀 JSON 物件，新增警示說明。[閱讀全文](../datasource/external-data-sources.md)

* 在電子郵件設計工具中新增條件式內容變體命名的警告說明。[閱讀全文](../personalization/create-conditions.md)

* 更新「取消委派登陸頁面子網域」區段。[閱讀全文](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* 釐清使用補充性識別碼時的歷程重新進入規則。[閱讀全文](../building-journeys/supplemental-identifier.md#guardrails--limitations)

* 新增附註，說明在事件設定期間選取補充性識別碼屬性時，必須在進階模式中使用運算式編輯器。[了解更多](../building-journeys/supplemental-identifier.md#add)

* 已新增歷程重新進入如何處理補充性識別碼的說明。[了解更多](../building-journeys/supplemental-identifier.md#guardrails)

## 2025 年 5 月 {#may-2025}

* 目前已經可以到「連線系統和環境」區段那邊，使用 Journey Optimizer 提供的 Adobe 整合功能。[閱讀全文](../integrations/ajo-integrations.md)

* 目前已將內容整合社為群組，歸類到 [內容管理] 區段。[閱讀全文](../integrations/content-integrations.md)

* 已更新 Adobe Experience Platform 和 Journey Optimizer 的架構圖。 [閱讀全文](../start/get-started.md#architecture-architecture)

* 新增有關個人化編輯器遊樂場的影片，以便幫助您瞭解如何使用樣本資料，編寫並測試個人化程式碼。 [閱讀全文](../personalization/personalize.md#how-to-videosvideo-perso)

* 種子清單上允許的頁數上限已從 50 頁提高至 300 頁。[閱讀全文](../configuration/seed-lists.md#create-seed-list)

* [建立決定原則] 頁面已加入新步驟，會詳細說明當使用程式碼型體驗編輯器中的決定原則時，該如何繞排程式碼。 [閱讀全文](../experience-decisioning/create-decision.md#use-decision-policy)

* 已在程式碼型體驗檔案中新增備註，如此一來，當您在同一個表面上執行多個程式碼型體驗動作時，如果使用者符合多重動作的資格，行銷活動或歷程的優先順序分數就會決定要傳遞哪些內容給他們參考。[閱讀全文](../code-based/code-based-surface.md#surface-definition)

* 有關在歷程中的疑難排解傳入動作新頁面上，提供逐步指南這件事，讓您可以在聯絡支援之前，先獨立找出問題所在，及時解決問題。[閱讀全文](../building-journeys/troubleshooting-inbound.md)

* 已新增[頁面](../code-based/code-based-decisioning-implementations.md)，以便說明如何在程式碼型體驗中使用決策功能時，將下列標幟新增至用戶端實作：

   * 正在新增 `dryRun` 標幟，以便測試程式碼型體驗中的決策。[閱讀全文](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

   * 請將重複資料刪除套用至程式碼型體驗中的決策請求。[閱讀全文](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## 2025 年 4 月 {#apr-2025}

* 設定章節現在分成三個章節： [頻道設定](../configuration/get-started-configuration.md)、[歷程設定](../configuration/about-data-sources-events-actions.md)以及[連線您的系統](../configuration/ajo-apis.md)。
* 新增在歷程運算式和條件中使用體驗事件的警告備註。 [閱讀全文](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* 在直接郵件設定頁面新增了關於輸出檔案暫時儲存的備註。 [閱讀全文](../direct-mail/direct-mail-configuration.md)
* 在歷程進階運算式編輯器章節新增條件格式指南的相關提示。 [閱讀全文](../building-journeys/expression/expressionadvanced.md)
* 在 `inAudience` 函式區段新增重新命名對象時影響和最佳實務的警告注意事項。 [閱讀全文](../building-journeys/functions/functioninaudience.md)
* 新增了使用雙向 SMS 時原生關鍵字用法的建議。 [閱讀全文](../sms/sms-opt-out.md)
* 已更新歷程測試頁面，其中備註說明必須在使用的事件中包含身分命名空間。 [閱讀全文](../building-journeys/testing-the-journey.md)
* 目前您無法透過 [!UICONTROL Journey Optimizer] 使用者介面取消委派子網域，請洽詢您的 Adobe 代表。 已詳細說明立即取消委託子網域的步驟，包括[電子郵件](../configuration/delegate-subdomain.md#undelegate-subdomain)、[簡訊](../sms/sms-subdomains.md#undelegate-a-subdomain-undelegate-subdomain)、[網頁體驗](../web/web-delegated-subdomains.md#undelegate-a-subdomain-undelegate-subdomain)和[登陸頁面](../landing-pages/lp-subdomains.md#undelegate-subdomain)。 <!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
* 已新增有關歷程上限 API 選用的 `maxHttpConnections` 參數說明，包括如何將其與相同端點的節流設定一起使用的指引。 [閱讀全文](../configuration/throttling.md)
* 在「體驗決策」區段新增指引，如果已核准的優惠項目用於集合或決策，則無法刪除。 包含使用&#x200B;**[!UICONTROL 復原核准]**&#x200B;選項將其狀態變更為「草稿」的步驟。 [閱讀全文](../experience-decisioning/items.md#manage)
* 有關沙箱的資訊已歸類至新的「沙箱管理」區段。 這個新的區段提供如何使用和指派沙箱的相關資訊，以及如何使用套件匯出與匯入功能，在多個沙箱中複製物件，例如歷程、內容範本或片段。 [閱讀全文](../administration/sandboxes.md)

## 2025 年 3 月 {#mar-2025}

* 已更新「客群資格篩選」事件的相關頁面，並新增建議。[閱讀全文](../building-journeys/audience-qualification-events.md)
* 所有客戶現在都能使用自訂動作疑難排解功能 (GA)。[閱讀全文](../action/troubleshoot-custom-action.md)
* 資料衛生現在是產品使用者介面的資料生命週期。 說明文件已更新，以反映此變更。 [閱讀全文](../privacy/data-hygiene.md)
* 檔案已新增缺少的登陸頁面內建權限。 [閱讀全文](../administration/ootb-permissions.md)
* 已新增有關排程定期性行銷活動的附註。 [閱讀全文](../campaigns/create-campaign.md)
* 有關在電子郵件訊息中插入連結及啟用追蹤的區段已更新並重新組織。 [閱讀全文](../email/message-tracking.md)
* Adobe Journey Optimizer 個人化功能的相關區段已重新整理並改善。 [閱讀全文](../personalization/personalize.md)
* 用於列出個人化優惠的決策管理 API 已更新，如果回應中缺少多個個人化優惠，則使用範例來執行分頁。 [閱讀全文](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* 已建立新頁面，收集有關清單取消訂閱功能的所有資訊，以提高清晰度。 [閱讀全文](../email/list-unsubscribe.md)
* 已更新「頻率限定」章節，其中包含如何在 Edge Decisioning API 之外更新「決策」和「批次決策」API 的頻率限定計數器。 [閱讀全文](../offers/offer-library/add-constraints.md#frequency-capping)

## 2025 年 2 月 {#feb-2025}

* 已更新「讀取客群」活動護欄，以指定歷程中只能使用一個活動，並只能鎖定一個客群。[閱讀全文](../building-journeys/read-audience.md)
* 使用 Adobe Campaign 行銷活動時的歷程護欄已更新。 [閱讀全文](../start/guardrails.md#ac-g)
* 已詳細說明建立第一個歷程的步驟，並新增檔案區段的連結。 [閱讀全文](../building-journeys/journey-gs.md)
* 新頁面現在已可用，以詳細說明歷程控制面板和篩選使用者介面。 [閱讀全文](../building-journeys/journey-ui.md)
*  **[!UICONTROL 傳送時間最佳化]** 的文件及其相關常見問題集已更新、改進並移至新的專用頁面。 [閱讀全文](../building-journeys/send-time-optimization.md)
* 已新增歷程事件護欄。 [閱讀全文](../start/guardrails.md#events-g)
* 內建頻道動作頁面已重新整理。 [閱讀全文](../building-journeys/journeys-message.md)
* 決策和決策管理區段新增了護欄與限制。
   * [決策護欄與限制](../experience-decisioning/decisioning-guardrails.md)
   * [決策管理護欄與限制](../offers/decision-management-guardrails.md)
* 已在決策管理檔案中新增內容資料的新區段。 它提供如何在決策引擎中運用內容資料的資訊，例如，設計決策規則，要求作出決策請求時當下天氣為 ≥ 80 度。 [閱讀全文](../offers/context-data.md)

## 2025 年 1 月 {#jan-2025}

* 已新增有關電子郵件設定中&#x200B;**[!UICONTROL 執行地址]**&#x200B;選項的新區段。主要地址是在沙箱層級定義，但預設設定可針對特定電子郵件設定覆寫。[閱讀全文](../email/email-settings.md#execution-address)

* **開始使用傳遞能力**&#x200B;頁面已更新，可以直接從使用者介面建立 IP 熱身工作流程。[閱讀全文](../reports/deliverability.md#reputation)

* **標頭參數**&#x200B;區段已更新，以反映使用者介面的新標籤和變更。[閱讀全文](../email/email-settings.md#email-header)

* **轉寄電子郵件**&#x200B;區段已更新，以指定所有傳送至&#x200B;**寄件者電子郵件**&#x200B;地址的電子郵件都會轉寄至這個轉寄電子郵件地址。如果未指定轉寄電子郵件，這些電子郵件將被捨棄。[閱讀全文](../email/email-settings.md#forward-email)

* 傳遞至 API 觸發之行銷活動要求中的內容屬性大小上限已更新為 200kb。 [閱讀全文](../campaigns/api-triggered-campaigns.md#contextual)

* 已對&#x200B;**管理章節**&#x200B;頁面新增一個區段，以說明如何將新屬性新增至即時片段中。 整個頁面也得到了改善。 [閱讀全文](../content-management/manage-fragments.md#adding-new-attributes)

* 「護欄和限制」區段已新增至衝突管理與優先順序工具文件之中。 [閱讀全文](../conflict-prioritization/gs-conflict-prioritization.md)

* 已新增端對端使用案例，以呈現 [!DNL Journey Optimizer] 程式碼型體驗管道的內容實驗中使用決策所需的所有步驟。 [閱讀全文](../experience-decisioning/experience-decisioning-uc.md)

*  **設定電子郵件設定** 頁面已分割成數個子頁面，以改善可讀性，包括專用於[清單取消訂閱](../email/list-unsubscribe.md)、[標頭參數](../email/header-parameters.md) 以及 [URL 追蹤](../email/url-tracking.md)的新獨立頁面。

## 2024 年 12 月  {#nov-2024}

* 已新增備註，以便協助處理疑難排解，當使用 Adobe Experience Platform 資料來啟用個人化資料集的 API 呼叫時，很可能傳出錯誤訊息。 [閱讀全文](../personalization/aep-data-perso.md)

## 2024 年 10 月 {#oct-2024}

* 有關 [!DNL Journey Optimizer]2024 年 10 月發布內容所有新功能，還有改良功能之詳情，請參閱本文件。 [閱讀全文](release-notes.md)
* [!DNL Journey Optimizer] 中可用的所有通訊頻道，目前都已完成分組，會列入文件的專用區段中。 [閱讀全文](../channels/gs-channels.md)
* 已改善&#x200B;**設定程式碼型體驗**&#x200B;分頁，讓程序更清楚，包括說明什麼是表面 URI 的區段。[閱讀全文](../code-based/code-based-configuration.md)
* 已更新&#x200B;**建立網頁管道設定**&#x200B;頁面，以便釐清建立頁面比對規則的步驟，此規則也適用於程式碼型體驗設定。[閱讀全文](../web/web-configuration.md#web-page-matching-rule)
* 已新增有關系統產生資料集的近期存留時間 (TTL) 護欄的備註。[閱讀全文](../data/get-started-datasets.md)
* 已新增新區段，方便說明如何操作，當要在歷程或行銷活動中模擬內容時，就能透過瀏覽器，或是在行動裝置上，使用&#x200B;**在裝置上預覽**&#x200B;的選項，直接預覽程式碼型個人化體驗。[閱讀全文](../code-based/test-code-based.md#preview-on-device)
* 已新增頁面，說明如何善用自訂上傳對象做決策。[閱讀全文](../offers/custom-upload-decisioning.md)
* 已新增新頁面，以便介紹 Journey Optimizer 中可用的決定功能。[閱讀全文](../experience-decisioning/gs-decision.md)
* Decisioning 文件已新增護欄和限制。 [閱讀全文](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## 2024 年 9 月 {#sept-2024}

* 有關 [!DNL Journey Optimizer] 2024 年 9 月發行版本的新功能和改進項目的詳情，請參閱本文件。 [閱讀全文](release-notes.md)
* 新增歷程重試管理的相關章節。[閱讀全文](../building-journeys/read-audience.md#read-audience-retry)
* 已更新自訂動作的上限/節流規則相關常見問題，以提及預設上限規則。[閱讀全文](../configuration/external-systems.md#faq)
* 已更新「控制存取權」章節，其中包含與 AI 助理內容產生器相關的權限。[閱讀全文](../administration/high-low-permissions.md#ai-permission)
* 已新增有關 AI 助理內容產生器影片，可用於電子郵件產生。[閱讀全文](../content-management/generative-email.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision Management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
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
* Information has been added in the Decision Management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-troubleshooting)
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
* Information has been added regarding the behaviour of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important-notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `<listObject>` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/conversion-functions.md#toString)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#campaign-statuses-and-alerts-statuses)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision Management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#important-notes-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behaviour. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#test-template)
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
* Decision Management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision Management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publish-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#journey-parameters)
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
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#reply-to-email)
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
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md#journey-versions)
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
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#forward-email)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision Management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
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
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-management)
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
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
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

* Now all the Decision Management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

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
* Documented the Decision Management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
