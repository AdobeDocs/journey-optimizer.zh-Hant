---
product: Journey Optimizer
audience: end-user
user-guide-title: Journey Optimizer指南
user-guide-description: 使用Journey Optimizer來建立並提供連結、情境式和個人化的體驗給客戶
type: Documentation
solution: Journey Optimizer
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 0%

---

# Adobe Journey Optimizer說明 {#using}

+ [Journey Optimizer檔案](ajo-home.md)
+ 新增功能 {#whats-new}
   + [最新發行說明](using/rn/release-notes.md)
   + 舊版發行說明 {#previous-rn-new}
      + [2022年發行說明](using/rn/release-notes-2022.md)
      + [2021年發行說明](using/rn/release-notes-2021.md)
   + [檔案更新](using/rn/documentation-updates.md)
+ 開始使用{#get-started}
   + [什麼是Journey Optimizer](using/start/get-started.md)
   + 快速入門手冊{#quick-start}
      + [概述](using/start/quick-start.md)
      + [行銷人員入門](using/start/path/marketer.md)
      + [資料工程師入門](using/start/path/data-engineer.md)
      + [以管理員身分開始使用](using/start/path/administrator.md)
      + [以開發人員身分開始使用](using/start/path/developer.md)
   + [使用者介面](using/start/user-interface.md)
   + [整合](using/start/ajo-integrations.md)
   + [護欄](using/start/guardrails.md)
+ 歷程 {#orchestrate-journeys}
   + [開始使用歷程](using/building-journeys/journey.md)
   + 建立歷程{#create-journey}
      + [建立您的第一個歷程](using/building-journeys/journey-gs.md)
      + [設計您的歷程](using/building-journeys/using-the-journey-designer.md)
      + [測試您的歷程](using/building-journeys/testing-the-journey.md)
      + [發佈您的歷程](using/building-journeys/publishing-the-journey.md)
   + 管理您的歷程{#mannage-journey}
      + [結束您的歷程](using/building-journeys/end-journey.md)
      + [時區管理](using/building-journeys/timezone-management.md)
      + [設定檔入口管理](using/building-journeys/entry-management.md)
      + [將歷程複製至其他沙箱](using/building-journeys/copy-to-sandbox.md)
      + [疑難排解您的歷程](using/building-journeys/troubleshooting.md)
      + [與Intelligent Services整合](using/building-journeys/ai-services-overview.md)
   + 活動 {#about-journey-building}
      + [開始使用歷程活動](using/building-journeys/about-journey-activities.md)
      + [一般事件](using/building-journeys/general-events.md)
      + [反應](using/building-journeys/reaction-events.md)
      + [區段資格](using/building-journeys/segment-qualification-events.md)
      + [條件](using/building-journeys/condition-activity.md)
      + [等待](using/building-journeys/wait-activity.md)
      + [讀取區段](using/building-journeys/read-segment.md)
      + [電子郵件、簡訊、推播](using/building-journeys/journeys-message.md)
      + [自訂動作](using/building-journeys/using-custom-actions.md)
      + [Adobe Campaign Standard動作](using/building-journeys/using-adobe-campaign-standard.md)
      + [Adobe Campaign v7/v8動作](using/building-journeys/using-adobe-campaign-classic.md)
      + [跳](using/building-journeys/jump.md)
      + [更新設定檔](using/building-journeys/update-profiles.md)
   + 建立運算式 {#building-advanced-conditions-journeys}
      + [概述](using/building-journeys/expression/expressionadvanced.md)
      + 語法 {#syntax}
         + [一般性](using/building-journeys/expression/generalities.md)
         + [條件式指令](using/building-journeys/expression/conditional-instruction.md)
         + [資料類型](using/building-journeys/expression/data-types.md)
         + [欄位參考](using/building-journeys/expression/field-references.md)
         + [集合管理函式](using/building-journeys/expression/collection-management-functions.md)
         + [運算子](using/building-journeys/expression/operators.md)
         + [歷程屬性](using/building-journeys/expression/journey-properties.md)
         + [範例](using/building-journeys/expression/advanced-editor-use-cases.md)
      + 函式 {#main-functions-journey}
         + [主要函式](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inSegment](using/building-journeys/functions/functioninsegment.md)
         + 匯總 {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [計數](using/building-journeys/functions/functioncount.md)
            + [countOnlyNull](using/building-journeys/functions/functioncountonlynull.md)
            + [countWithNull](using/building-journeys/functions/functioncountwithnull.md)
            + [distinctCount](using/building-journeys/functions/functiondistinctcount.md)
            + [distinctCountWithNull](using/building-journeys/functions/functiondistinctcountwithnull.md)
            + [max](using/building-journeys/functions/functionmax.md)
            + [min](using/building-journeys/functions/functionmin.md)
            + [sum](using/building-journeys/functions/functionsum.md)
         + 轉換 {#conversion}
            + [toBool](using/building-journeys/functions/functiontobool.md)
            + [toDateOnly](using/building-journeys/functions/functiontodateonly.md)
            + [toDateTime](using/building-journeys/functions/functiontodatetime.md)
            + [toDateTimeOnly](using/building-journeys/functions/functiontodatetimeonly.md)
            + [toDecimal](using/building-journeys/functions/functiontodecimal.md)
            + [toDuration](using/building-journeys/functions/functiontoduration.md)
            + [toInteger](using/building-journeys/functions/functiontointeger.md)
            + [toString](using/building-journeys/functions/functiontostring.md)
         + 日期 {#date}
            + [currentTime &#x200B; InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
            + [inLastDays](using/building-journeys/functions/functioninlastdays.md)
            + [inLastHours](using/building-journeys/functions/functioninlasthours.md)
            + [inLastMonths](using/building-journeys/functions/functioninlastmonths.md)
            + [inLastYears](using/building-journeys/functions/functioninlastyears.md)
            + [inNextDays](using/building-journeys/functions/functioninnextdays.md)
            + [inNextHours](using/building-journeys/functions/functioninnexthours.md)
            + [inNextMonths](using/building-journeys/functions/functioninnextmonths.md)
            + [inNextYears](using/building-journeys/functions/functioninnextyears.md)
            + [now](using/building-journeys/functions/functionnow.md)
            + [nowWithDelta](using/building-journeys/functions/functionnowwithdelta.md)
            + [setHours](using/building-journeys/functions/functionsethours.md)
            + [setDays](using/building-journeys/functions/functionsetdays.md)
            + [updateTimeZone](using/building-journeys/functions/functionupdatetimezone.md)
         + 清單 {#list}
            + [不重複](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [篩選](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [in](using/building-journeys/functions/functionin.md)
            + [相交](using/building-journeys/functions/functionintersect.md)
            + [限制](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [排序](using/building-journeys/functions/functionsort.md)
         + 數學 {#math}
            + [隨機](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + 字串 {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [cont](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [isEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [length](using/building-journeys/functions/functionlength.md)
            + [lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [notequalIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [split](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [uper](using/building-journeys/functions/functionupper.md)
            + [uid](using/building-journeys/functions/functionuuid.md)
   + 使用案例 {#journey-use-cases}
      + 業務使用案例 {#business-use-cases}
         + [傳送多通道訊息](using/building-journeys/journeys-uc.md)
         + [使用Campaign v7/v8傳送訊息](using/building-journeys/ajo-ac.md)
         + [傳送訊息給訂閱者](using/building-journeys/message-to-subscribers-uc.md)
      + 技術使用案例 {#technical-use-cases}
         + [使用自訂動作以動態方式傳遞集合](using/building-journeys/collections.md)
         + [加速傳遞](using/building-journeys/ramp-up-deliveries-uc.md)
         + [使用外部資料來源和自訂動作限制輸送量](using/building-journeys/limit-throughput.md)
+ 行銷活動{#campaigns}
   + [開始使用行銷活動](using/campaigns/get-started-with-campaigns.md)
   + [建立促銷活動](using/campaigns/create-campaign.md)
   + [檢閱及啟動行銷活動](using/campaigns/review-activate-campaign.md)
   + [管理行銷活動](using/campaigns/modify-stop-campaign.md)
   + 內容實驗 {#content-experiment}
      + [開始進行內容實驗](using/campaigns/get-started-experiment.md)
      + [建立內容實驗](using/campaigns/content-experiment.md)
      + [了解統計計算](using/campaigns/experiment-calculations.md)
      + [設定實驗報表](using/campaigns/reporting-configuration.md)
   + [使用API觸發促銷活動](using/campaigns/api-triggered-campaigns.md)
+ 電子郵件通道 {#email}
   + [開始使用電子郵件](using/email/get-started-email.md)
   + [建立電子郵件](using/email/create-email.md)
   + 設計您的電子郵件內容 {#design-email}
      + [開始使用電子郵件設計](using/email/get-started-email-design.md)
      + 開始建立內容 {#start-creating-content}
         + [從頭開始](using/email/content-from-scratch.md)
         + [匯入您的電子郵件內容](using/email/existing-content.md)
         + [編寫您自己的內容](using/email/code-content.md)
         + [使用範本](using/email/email-templates.md)
      + 設計您的內容 {#add-content}
         + [使用內容元件](using/email/content-components.md)
         + [新增連結及追蹤訊息](using/email/message-tracking.md)
         + 管理資產 {#manage-asset}
            + [使用Assets Essentials](using/email/assets-essentials.md)
            + [使用Adobe Stock](using/email/stock.md)
         + [插入個人化優惠方案](using/email/add-offers-email.md)
         + [生成文本版本](using/email/text-version-email.md)
         + [新增前置詞](using/email/preheader.md)
      + 編輯樣式 {#edit-style}
         + [開始使用電子郵件樣式](using/email/get-started-email-style.md)
         + [編輯背景設定](using/email/backgrounds.md)
         + [調整垂直對齊和邊框間距](using/email/alignment-and-padding.md)
         + [定義連結的樣式](using/email/styling-links.md)
         + [新增內嵌樣式屬性](using/email/inline-styling.md)
   + [預覽和測試您的電子郵件](using/email/preview.md)
   + [管理電子郵件選擇退出](using/email/email-opt-out.md)
   + 設定電子郵件通道 {#configure-email}
      + [開始使用電子郵件設定](using/email/get-started-email-config.md)
      + [配置電子郵件表面設定](using/email/email-settings.md)
+ 應用程式內管道{#in-app}
   + [開始使用應用程式內管道](using/in-app/get-started-in-app.md)
   + [設定應用程式內通道](using/in-app/inapp-configuration.md)
   + [建立應用程式內訊息](using/in-app/create-in-app.md)
   + [設計您的應用程式內內容](using/in-app/design-in-app.md)
   + [應用程式內報表](using/in-app/inapp-report.md)
+ 推播通知通道{#push}
   + [推播通知快速入門](using/push/get-started-push.md)
   + [建立推播通知](using/push/create-push.md)
   + [設計推播通知](using/push/design-push.md)
   + [傳送推播通知](using/push/send-push.md)
   + 設定推播通知{#push-config}
      + [推播通知與Adobe Journey Optimizer](using/push/push-gs.md)
      + [設定推播通知通道](using/push/push-configuration.md)
+ SMS通道{#sms}
   + [開始使用SMS](using/sms/get-started-sms.md)
   + [建立SMS訊息](using/sms/create-sms.md)
   + [傳送SMS訊息](using/sms/send-sms.md)
   + [管理SMS選擇退出](using/sms/sms-opt-out.md)
   + [設定SMS通道](using/sms/sms-configuration.md)
+ 直接郵件 {#direct-mail}
   + [建立直接郵件](using/direct-mail/create-direct-mail.md)
   + [配置直接郵件](using/direct-mail/direct-mail-configuration.md)
+ 網頁頻道{#web}
   + [開始使用網頁頻道](using/web/get-started-web.md)
   + [建立網路體驗](using/web/create-web.md)
   + [製作網頁](using/web/author-web.md)
   + [Visual Editing Helper擴充功能](using/web/visual-editing-helper.md)
   + [網站報告](using/web/web-report.md)
+ 登錄頁面 {#landing-pages}
   + [開始使用登錄頁面](using/landing-pages/get-started-lp.md)
   + [建立登錄頁面](using/landing-pages/create-lp.md)
   + 設計內容 {#landing-pages-design}
      + [關於登錄頁面設計](using/landing-pages/design-lp.md)
      + [建立登錄頁面內容](using/landing-pages/lp-content.md)
      + [建立範本](using/landing-pages/lp-templates.md)
      + [新增自訂JavaScript](using/landing-pages/lp-custom-js.md)
   + [建立訂閱清單](using/landing-pages/subscription-list.md)
   + [透過使用案例了解](using/landing-pages/lp-use-cases.md)
   + 設定登錄頁面 {#lp-configuration}
      + [設定登錄頁面子網域](using/landing-pages/lp-subdomains.md)
      + [定義登錄頁面預設集](using/landing-pages/lp-presets.md)
+ 個人化和動態內容 {#personalized-dynamic-content}
   + 個人化 {#personalization}
      + [開始使用個人化](using/personalization/personalize.md)
      + [個人化內容](using/personalization/personalization-contexts.md)
      + 建立運算式 {#build-expressions}
         + [個人化語法](using/personalization/personalization-syntax.md)
         + 使用運算式編輯器 {#expression-editor}
            + [關於運算式編輯器](using/personalization/personalization-build-expressions.md)
            + [將屬性添加到收藏夾](using/personalization/personalization-favorites.md)
            + [使用已儲存的運算式](using/personalization/personalization-library.md)
            + [個人化驗證](using/personalization/personalization-validation.md)
         + 輔助函式{#functions}
            + [開始使用協助程式函式](using/personalization/functions/functions.md)
            + [聚合函式](using/personalization/functions/aggregation.md)
            + [算術函式](using/personalization/functions/arithmetic-functions.md)
            + [陣列和清單函式](using/personalization/functions/arrays-list.md)
            + [日期函式](using/personalization/functions/dates.md)
            + [布林值和比較函式](using/personalization/functions/operators.md)
            + [Helpers](using/personalization/functions/helpers.md)
            + [地圖函式](using/personalization/functions/maps.md)
            + [物件函式](using/personalization/functions/objects.md)
            + [字串函式](using/personalization/functions/string.md)
      + 使用案例{#personalization-use-cases}
         + [訂單狀態通知](using/personalization/personalization-use-case.md)
         + [購物車放棄電子郵件](using/personalization/personalization-use-case-helper-functions.md)
   + 動態內容 {#dynamic}
      + [開始使用動態內容](using/personalization/get-started-dynamic-content.md)
      + [建立條件式規則](using/personalization/create-conditions.md)
      + [建立動態內容](using/personalization/dynamic-content.md)
+ 區段、設定檔與身分{#segment}
   + 區段 {#segments}
      + [開始使用區段](using/segment/about-segments.md)
      + [建立區段](using/segment/creating-a-segment.md)
   + 設定檔{#profiles}
      + [開始使用設定檔](using/segment/get-started-profiles.md)
      + [建立測試設定檔](using/segment/creating-test-profiles.md)
   + [身分](using/segment/get-started-identity.md)
   + 撰寫對象 {#audience-orchestration}
      + [開始使用受眾構成](using/segment/get-started-audience-orchestration.md)
      + [建立合成工作流程](using/segment/create-compositions.md)
      + [使用合成畫布](using/segment/composition-canvas.md)
      + [存取及管理對象](using/segment/access-audiences.md)
   + [授權使用](using/segment/license-usage.md)
+ 追蹤和監視 {#reporting}
   + 即時報表 {#live-report}
      + [開始使用即時報表](using/reports/live-report.md)
      + [歷程即時報表](using/reports/journey-live-report.md)
      + [行銷活動上線報表](using/reports/campaign-live-report.md)
      + [登陸頁面即時報表](using/reports/lp-report-live.md)
      + [訂閱清單即時報表](using/reports/subscription-report-live.md)
   + 全域報表 {#global-report}
      + [開始使用全域報表](using/reports/global-report.md)
      + [歷程全域報表](using/reports/journey-global-report.md)
      + [行銷活動全域報表](using/reports/campaign-global-report.md)
      + [登陸頁面全域報表](using/reports/lp-report-global.md)
      + [訂閱清單全局報告](using/reports/subscription-report-global.md)
   + 歷程報表 {#reports}
      + [建立歷程報表](using/reports/sharing-overview.md)
      + [步驟事件欄位清單](using/reports/sharing-field-list.md)
      + 舊版步驟事件欄位 {#legacy-step-event-fields}
         + [關於舊版欄位](using/reports/sharing-legacy-fields.md)
         + [歷程欄位](using/reports/sharing-journey-fields.md)
         + [公用欄位](using/reports/sharing-common-fields.md)
         + [動作執行欄位](using/reports/sharing-execution-fields.md)
         + [資料擷取欄位](using/reports/sharing-fetch-fields.md)
         + [身分欄位](using/reports/sharing-identity-fields.md)
      + [查詢範例](using/reports/query-examples.md)
   + 傳遞能力 {#deliverability}
      + [開始使用傳遞能力](using/reports/deliverability.md)
      + [了解隱藏清單](using/reports/suppression-list.md)
   + [警報](using/reports/alerts.md)
   + [使用Customer Journey Analytics](using/reports/cja-ajo.md)
+ 決策管理 {#offer-decisioning}
   + 開始使用決策管理 {#get-started-decision}
      + [關於決策管理](using/offers/get-started/starting-offer-decisioning.md)
      + [使用者介面](using/offers/get-started/user-interface.md)
      + [建立和管理優惠方案的關鍵步驟](using/offers/offer-library/key-steps.md)
      + [使用案例：在電子郵件中插入優惠方案](using/offers/offers-e2e.md)
   + 建立元件 {#create-components}
      + [建立版位](using/offers/offer-library/creating-placements.md)
      + [建立決策規則](using/offers/offer-library/creating-decision-rules.md)
      + [建立標籤](using/offers/offer-library/creating-tags.md)
   + 建立排名 {#rankings}
      + [開始使用排名](using/offers/ranking/get-started-rankings.md)
      + [排名公式](using/offers/ranking/create-ranking-formulas.md)
      + AI模型 {#ai-models}
         + [關於AI模型](using/offers/ranking/ai-models.md)
         + AI模型類型 {#ai-model-types}
            + [自動優化模型](using/offers/ranking/auto-optimization-model.md)
            + [個性化優化模型](using/offers/ranking/personalized-optimization-model.md)
         + 建立AI模型 {#configure-ai-model}
            + [建立資料集以收集事件](using/offers/ranking/create-dataset.md)
            + [建立AI模型](using/offers/ranking/create-ranking-strategies.md)
            + [配置事件捕獲](using/offers/ranking/schema-requirement.md)
   + 建立和管理優惠方案 {#managing-offers-in-the-offer-library}
      + 設定優惠方案 {#configure-offers}
         + [建立個人化優惠方案](using/offers/offer-library/creating-personalized-offers.md)
         + [添加表示法](using/offers/offer-library/add-representations.md)
         + [新增限制](using/offers/offer-library/add-constraints.md)
      + [建立回退優惠方案](using/offers/offer-library/creating-fallback-offers.md)
      + [建立集合](using/offers/offer-library/creating-collections.md)
   + 建立和管理決策 {#create-manage-activities}
      + [建立決策](using/offers/offer-activities/create-offer-activities.md)
      + [在決策中設定選件選取項目](using/offers/offer-activities/configure-offer-selection.md)
      + [建立模擬](using/offers/offer-activities/simulation.md)
   + [批次決策](using/offers/batch-delivery.md)
   + 建立決策管理報表 {#create-reports}
      + [開始使用決策管理事件](using/offers/reports/get-started-events.md)
      + [決策管理事件關鍵資訊](using/offers/reports/key-information.md)
      + [存取事件XDM欄位](using/offers/reports/xdm-fields.md)
   + 匯出優惠方案目錄 {#export-catalog}
      + [開始匯出優惠方案目錄 ](using/offers/export-catalog/get-started-export.md)
      + [存取匯出的優惠方案目錄](using/offers/export-catalog/access-dataset.md)
      + [個人化優惠方案資料集](using/offers/export-catalog/export-offers.md)
      + [決策資料集](using/offers/export-catalog/export-decisions.md)
      + [版位資料集](using/offers/export-catalog/export-placements.md)
      + [備援資料集](using/offers/export-catalog/export-fallback.md)
   + API參考 {#api-reference}
      + [快速入門](using/offers/api-reference/getting-started.md)
      + 使用API建立和管理優惠方案 {#offers-api}
         + 版位 {#placements}
            + [清單位置](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [查詢投放位置](using/offers/api-reference/offers-api/placements/lookup.md)
            + [建立版位](using/offers/api-reference/offers-api/placements/create.md)
            + [更新投放位置](using/offers/api-reference/offers-api/placements/update.md)
            + [刪除投放位置](using/offers/api-reference/offers-api/placements/delete.md)
         + 決策規則 {#decision-rules}
            + [清單決策規則](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [查詢決策規則](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [建立決策規則](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [更新決策規則](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [刪除決策規則](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + 標籤 {#tags}
            + [清單標籤](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [查詢標籤](using/offers/api-reference/offers-api/tags/lookup.md)
            + [建立標籤](using/offers/api-reference/offers-api/tags/create.md)
            + [更新標籤](using/offers/api-reference/offers-api/tags/update.md)
            + [刪除標籤](using/offers/api-reference/offers-api/tags/delete.md)
         + 個人化優惠方案 {#personalized-offers}
            + [列出個人化優惠方案](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
            + [查詢個人化優惠方案](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
            + [建立個人化優惠方案](using/offers/api-reference/offers-api/personalized-offers/create.md)
            + [更新個人化優惠方案](using/offers/api-reference/offers-api/personalized-offers/update.md)
            + [刪除個人化優惠方案](using/offers/api-reference/offers-api/personalized-offers/delete.md)
         + 集合 {#collections}
            + [清單集合](using/offers/api-reference/offers-api/collections/collections-list.md)
            + [查詢集合](using/offers/api-reference/offers-api/collections/lookup.md)
            + [建立集合](using/offers/api-reference/offers-api/collections/create.md)
            + [更新集合](using/offers/api-reference/offers-api/collections/update.md)
            + [刪除集合](using/offers/api-reference/offers-api/collections/delete.md)
         + 回退優惠方案 {#fallback-offers}
            + [列出回退優惠方案](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
            + [查詢備援優惠方案](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
            + [建立回退優惠方案](using/offers/api-reference/offers-api/fallback-offers/create.md)
            + [更新回退優惠方案](using/offers/api-reference/offers-api/fallback-offers/update.md)
            + [刪除回退優惠方案](using/offers/api-reference/offers-api/fallback-offers/delete.md)
      + 使用API建立和管理決策 {#activities-api}
         + [清單決策](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [查詢決策](using/offers/api-reference/activities-api/activities/lookup.md)
         + [建立決策](using/offers/api-reference/activities-api/activities/create.md)
         + [更新決策](using/offers/api-reference/activities-api/activities/update.md)
         + [刪除決策](using/offers/api-reference/activities-api/activities/delete.md)
      + 使用API提供優惠方案 {#offer-delivery-api}
         + [開始使用選件傳送API](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [決策API](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [Edge Decisioning API](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [批次決策API](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ 資料管理 {#data-management}
   + [開始使用資料管理](using/data/gs-data.md)
   + [使用結構](using/data/get-started-schemas.md)
   + Journey Optimizer資料集 {#datasets}
      + [開始使用資料集](using/data/get-started-datasets.md)
      + [查詢範例](using/data/datasets-query-examples.md)
   + [查詢](using/data/get-started-queries.md)
+ 設定{#configuration}
   + [開始使用Journey Optimizer設定](using/configuration/get-started-configuration.md)
   + 委派電子郵件子網域 {#delegate-subdomains}
      + [開始使用子網域委派](using/configuration/about-subdomain-delegation.md)
      + [委派子網域](using/configuration/delegate-subdomain.md)
      + [新增Google TXT記錄](using/configuration/google-txt.md)
      + [訪問和編輯PTR記錄](using/configuration/ptr-records.md)
      + [建立IP池](using/configuration/ip-pools.md)
   + [設定通道曲面](using/configuration/channel-surfaces.md)
   + 監視電子郵件地址 {#monitor-reputation}
      + [隱藏清單](using/configuration/manage-suppression-list.md)
      + [重試](using/configuration/retries.md)
      + [允許的清單](using/configuration/allow-list.md)
   + [支援封存](using/configuration/archiving-support.md)
   + [設定頻率規則](using/configuration/frequency-rules.md)
   + [管理執行地址](using/configuration/primary-email-addresses.md)
   + 設定歷程 {#configure-journeys}
      + [關於資料來源、事件和動作](using/configuration/about-data-sources-events-actions.md)
      + [與外部系統整合](using/configuration/external-systems.md)
      + 事件設定 {#events-journeys}
         + [一般原則](using/event/about-events.md)
         + 設定單一事件 {#unitary-events}
            + [開始使用單一事件](using/event/about-creating.md)
            + [關於ExperienceEvent結構](using/event/experience-event-schema.md)
            + [運用Adobe Analytics](using/event/about-analytics.md)
         + [設定業務事件](using/event/about-creating-business.md)
         + [傳送事件的其他步驟](using/event/additional-steps-to-send-events-to-journey.md)
      + 資料源配置{#data-source-journeys}
         + [關於資料來源](using/datasource/about-data-sources.md)
         + [設定資料來源](using/datasource/configure-data-sources.md)
         + [Adobe Experience Platform資料來源](using/datasource/adobe-experience-platform-data-source.md)
         + [外部資料來源](using/datasource/external-data-sources.md)
      + 動作設定 {#action-journeys}
         + [關於動作](using/action/action.md)
         + [設定動作](using/action/about-custom-action-configuration.md)
         + [與Adobe Campaign Standard整合](using/action/acs-action.md)
         + [與Adobe Campaign v7/v8整合](using/action/acc-action.md)
   + [來源](using/start/get-started-sources.md)
+ 存取控制 {#access-control}
   + [存取控制概觀](using/administration/permissions-overview.md)
   + [內建的產品設定檔](using/administration/ootb-product-profiles.md)
   + [管理使用者和產品設定檔](using/administration/permissions.md)
   + [權限層級](using/administration/high-low-permissions.md)
   + [沙箱管理](using/administration/sandboxes.md)
   + [基於屬性的訪問控制](using/administration/attribute-based-access.md)
   + [對象級訪問控制](using/administration/object-based-access.md)
+ 隱私權 {#privacy}
   + [開始使用隱私權](using/privacy/get-started-privacy.md)
   + [隱私權要求](using/privacy/requests.md)
   + [對資源執行審計操作](using/privacy/audit-logs.md)
   + 管理同意 {#consent}
      + [管理選擇退出](using/privacy/opt-out.md)
      + [使用同意政策](using/action/consent.md)
   + [資料控管](using/action/action-privacy.md)
