---
product: Journey Optimizer
audience: end-user
user-guide-title: Journey Optimizer 指南
user-guide-description: 使用 Journey Optimizer 向客戶建立與傳遞連結、情境式和個人化的體驗
type: Documentation
solution: Journey Optimizer
source-git-commit: a5057c3ce699a972c22cc125dd963d545a113b0b
workflow-type: tm+mt
source-wordcount: '2328'
ht-degree: 90%

---

# Adobe Journey Optimizer 說明 {#using}

+ [Journey Optimizer 文件](ajo-home.md)
+ 新增功能？ {#whats-new}
   + [早期發行說明](using/rn/e-release-notes.md)
   + [最新發行說明](using/rn/release-notes.md)
   + 上一個發行說明 {#previous-rn-new}
      + [2025](using/rn/release-notes-2025.md)
      + [2024 年](using/rn/release-notes-2024.md)
      + [2023 版](using/rn/release-notes-2023.md)
      + [2022 版](using/rn/release-notes-2022.md)
      + [2021 版](using/rn/release-notes-2021.md)
   + [文件更新](using/rn/documentation-updates.md)
   + [改善的歷程畫布](using/rn/new-canvas.md)
+ 快速入門{#get-started}
   + [什麼是 Journey Optimizer](using/start/get-started.md)
   + 快速開始指南{#quick-start}
      + [總覽](using/start/quick-start.md)
      + [行銷人員快速入門](using/start/path/marketer.md)
      + [資料工程師快速入門](using/start/path/data-engineer.md)
      + [管理員快速入門](using/start/path/administrator.md)
      + [開發人員快速入門](using/start/path/developer.md)
   + [使用者介面](using/start/user-interface.md)
   + [搜尋、篩選、分類](using/start/search-filter-categorize.md)
   + [協助工具](using/start/accessibility.md)
   + [使用案例教戰手冊](using/start/playbooks.md)
   + [使用 AI 助理](using/start/ai-assistant.md)
   + [護欄](using/start/guardrails.md)
   + [最佳作法](using/start/best-practices.md)
+ 歷程 {#orchestrate-journeys}
   + [開始使用歷程](using/building-journeys/journey.md)
   + 建立歷程{#create-journey}
      + [建立您的第一個歷程](using/building-journeys/journey-gs.md)
      + [設定您的歷程屬性](using/building-journeys/journey-properties.md)
      + [設定並追蹤您的歷程量度](using/building-journeys/success-metrics.md)
      + [設計您的歷程](using/building-journeys/using-the-journey-designer.md)
      + [測試您的歷程](using/building-journeys/testing-the-journey.md)
      + [模擬您的歷程](using/building-journeys/journey-simulation.md)
      + [發佈您的歷程](using/building-journeys/publishing-the-journey.md)
      + [歷程中的即時報告](using/building-journeys/report-journey.md)
   + 管理您的旅程{#manage-journey}
      + [瀏覽及篩選您的歷程](using/building-journeys/journey-ui.md)
      + [輪廓入口管理](using/building-journeys/entry-management.md)
      + [時區管理](using/building-journeys/timezone-management.md)
      + [傳送時間最佳化](using/building-journeys/send-time-optimization.md)
      + [結束您的歷程](using/building-journeys/end-journey.md)
      + [將歷程複製到另一個沙箱](using/building-journeys/copy-to-sandbox.md)
      + [疑難排解您的歷程](using/building-journeys/troubleshooting.md)
      + [與 Intelligent Services 整合](using/building-journeys/ai-services-overview.md)
   + 活動 {#about-journey-building}
      + [開始使用歷程活動](using/building-journeys/about-journey-activities.md)
      + [一般事件](using/building-journeys/general-events.md)
      + [反應](using/building-journeys/reaction-events.md)
      + [客群資格篩選](using/building-journeys/audience-qualification-events.md)
      + [條件](using/building-journeys/condition-activity.md)
      + [等待](using/building-journeys/wait-activity.md)
      + [讀取客群](using/building-journeys/read-audience.md)
      + [內建管道動作](using/building-journeys/journeys-message.md)
      + [自訂動作](using/building-journeys/using-custom-actions.md)
      + [Adobe Campaign Standard 動作](using/building-journeys/using-adobe-campaign-standard.md)
      + [Adobe Campaign v7/v8 動作](using/building-journeys/using-adobe-campaign-v7-v8.md)
      + [跳轉](using/building-journeys/jump.md)
      + [更新輪廓](using/building-journeys/update-profiles.md)
   + 建立表達式 {#building-advanced-conditions-journeys}
      + [使用進階運算式編輯器](using/building-journeys/expression/expressionadvanced.md)
      + 語法 {#syntax}
         + [進階運算式編輯器語法](using/building-journeys/expression/generalities.md)
         + [條件指令](using/building-journeys/expression/conditional-instruction.md)
         + [資料類型](using/building-journeys/expression/data-types.md)
         + [欄位參考](using/building-journeys/expression/field-references.md)
         + [集合管理功能](using/building-journeys/expression/collection-management-functions.md)
         + [操作者](using/building-journeys/expression/operators.md)
         + [歷程屬性](using/building-journeys/expression/journey-properties.md)
         + [範例](using/building-journeys/expression/advanced-editor-use-cases.md)
      + 函數 {#main-functions-journey}
         + [主要功能](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inAudience](using/building-journeys/functions/functioninaudience.md)
         + 彙總 {#aggregation}
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
            + [currentTime&#x200B;InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
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
            + [distinct](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [篩選](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [在 ](using/building-journeys/functions/functionin.md)
            + [相交](using/building-journeys/functions/functionintersect.md)
            + [limit](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + 數學 {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + 字串 {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [contain](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [IsEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [長度](using/building-journeys/functions/functionlength.md)
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
            + [upper](using/building-journeys/functions/functionupper.md)
            + [UUID](using/building-journeys/functions/functionuuid.md)
   + 使用案例 {#journey-use-cases}
      + 企業用例 {#business-use-cases}
         + [傳送多頻道訊息](using/building-journeys/journeys-uc.md)
         + [使用 Campaign v7/v8 傳送訊息](using/building-journeys/ajo-ac.md)
         + [傳送訊息給訂閱者](using/building-journeys/message-to-subscribers-uc.md)
      + 技術使用案例 {#technical-use-cases}
         + [使用自訂動作動態傳遞集合](using/building-journeys/collections.md)
         + [加快傳遞速度](using/building-journeys/ramp-up-deliveries-uc.md)
         + [使用外部資料來源和自訂動作限制輸送量](using/building-journeys/limit-throughput.md)
         + [使用自訂動作在 Experience Platform 中編寫歷程事件](using/building-journeys/custom-action-aep.md)
+ 協調的行銷活動 {#ms-campaigns}
   + [開始使用精心策劃的營銷活動](using/ms/gs-ms-campaigns.md)
   + [主要原則](using/ms/gs-campaign-creation.md)
   + 設定 {#ms-config}
      + [結構描述](using/ms/ms-schemas.md)
      + [使用事件變數](using/ms/event-variables.md)
   + 建立您的第一個編排行銷活動 {#create-ms-campaign}
      + [建立協調行銷活動](using/ms/create-ms-campaign.md)
      + [協調活動](using/ms/orchestrate-activities.md)
      + [設定行銷活動設定](using/ms/ms-campaign-settings.md)
      + [開始並監控行銷活動](using/ms/start-monitor-campaigns.md)
      + [管理個人化](using/ms/ms-personalization.md)
   + 精心規劃的行銷活動活動 {#design-campaigns}
      + [關於精心規劃的行銷活動活動](using/ms/activities/about-activities.md)
      + [合併連結](using/ms/activities/and-join.md)
      + [建置客群](using/ms/activities/build-audience.md)
      + [變更維度](using/ms/activities/change-dimension.md)
      + [合併](using/ms/activities/combine.md)
      + [重複資料刪除](using/ms/activities/deduplication.md)
      + [頻道動作](using/ms/activities/channels.md)
      + [擴充](using/ms/activities/enrichment.md)
      + [分支](using/ms/activities/fork.md)
      + [載入檔案](using/ms/activities/load-file.md)
      + [調和](using/ms/activities/reconciliation.md)
      + [儲存客群](using/ms/activities/save-audience.md)
      + [排程器](using/ms/activities/scheduler.md)
      + [分割](using/ms/activities/split.md)
      + [測試](using/ms/activities/test.md)
      + [更新資料](using/ms/activities/update-data.md)
      + [等待](using/ms/activities/wait.md)
+ 行銷活動 {#campaigns}
   + [開始使用行銷活動](using/campaigns/get-started-with-campaigns.md)
   + [建立行銷活動](using/campaigns/create-campaign.md)
   + [檢閱及啟動行銷活動](using/campaigns/review-activate-campaign.md)
   + [管理行銷活動](using/campaigns/modify-stop-campaign.md)
   + [利用 API 觸發行銷活動](using/campaigns/api-triggered-campaigns.md)
+ 衝突管理與優先順序 {#conflict-prioritization}
   + [開始使用衝突管理和優先順序](using/conflict-prioritization/gs-conflict-prioritization.md)
   + [識別潛在衝突](using/conflict-prioritization/conflicts.md)
   + [指派優先順序分數](using/conflict-prioritization/priority-scores.md)
   + [歷程上限與仲裁](using/conflict-prioritization/journey-capping.md)
+ 測試與批准 {#test}
   + 預覽 &amp; 測試 內容 {#preview-test}
      + [開始預覽和測試](using/content-management/preview-test.md)
      + [選取測試輪廓](using/content-management/test-profiles.md)
      + [預覽您的內容](using/content-management/preview.md)
      + [傳送電子郵件校樣](using/content-management/proofs.md)
      + [測試電子郵件轉譯](using/content-management/rendering.md)
      + [使用範例輸入資料 (測試版) 來測試內容](using/test-approve/simulate-sample-input.md)
      + [電子郵件垃圾郵件報告](using/content-management/spam-report.md)
   + 核准歷程與營銷活動 {#approve}
      + [開始使用核准](using/test-approve/gs-approval.md)
      + [建立和管理核准原則](using/test-approve/approval-policies.md)
      + [請求核准](using/test-approve/request-approval.md)
      + [核准請求](using/test-approve/review-approve-request.md)
+ 通訊通道 {#channels}
   + [開始使用通訊頻道](using/channels/gs-channels.md)
   + 電子郵件頻道 {#email}
      + [開始使用電子郵件](using/email/get-started-email.md)
      + [建立電子郵件](using/email/create-email.md)
      + 設計您的電子郵件內容 {#design-email}
         + [開始使用電子郵件設計](using/email/get-started-email-design.md)
         + 開始建立內容 {#start-creating-content}
            + [從頭開始設計內容](using/email/content-from-scratch.md)
            + [匯入內容](using/email/existing-content.md)
            + [為您自己的內容撰寫程式碼](using/email/code-content.md)
            + [使用電子郵件範本](using/email/use-email-templates.md)
         + 設計您的內容 {#add-content}
            + [使用內容元件](using/email/content-components.md)
            + [運用視覺片段](using/email/use-visual-fragments.md)
            + [新增連結及追蹤訊息](using/email/message-tracking.md)
            + [插入個人化產品建議](using/email/add-offers-email.md)
            + [產生文字版本](using/email/text-version-email.md)
            + [新增中繼資料](using/email/email-metadata.md)
         + 編輯樣式 {#edit-style}
            + [開始使用電子郵件樣式](using/email/get-started-email-style.md)
            + [編輯背景設定](using/email/backgrounds.md)
            + [調整垂直對齊與邊框間距](using/email/alignment-and-padding.md)
            + [加入內嵌樣式屬性](using/email/inline-styling.md)
      + [管理電子郵件選擇退出](using/email/email-opt-out.md)
      + 設定電子郵件通道 {#configure-email}
         + [開始使用電子郵件設定](using/email/get-started-email-config.md)
         + [定義電子郵件組態設定](using/email/email-settings.md)
         + [啟用清單取消訂閱](using/email/list-unsubscribe.md)
         + [標頭參數](using/email/header-parameters.md)
         + [URL 追蹤](using/email/url-tracking.md)
         + [個人化電子郵件組態](using/email/surface-personalization.md)
   + 應用程式內頻道{#in-app}
      + [開始使用應用程式內頻道](using/in-app/get-started-in-app.md)
      + [應用程式內頻道先決條件](using/in-app/inapp-configuration.md)
      + [建立行動裝置應用程式內訊息](using/in-app/create-in-app.md)
      + [建立網頁應用程式內訊息](using/in-app/create-in-app-web.md)
      + [設計您的應用程式內內容](using/in-app/design-in-app.md)
      + [檢查並傳送應用程式內通知](using/in-app/send-in-app.md)
   + 推播通知頻道{#push}
      + [開始使用推播通知](using/push/get-started-push.md)
      + [建立推播通知](using/push/create-push.md)
      + [設計推播通知](using/push/design-push.md)
      + [檢查並傳送推播通知](using/push/send-push.md)
      + 設定推送通知{#push-config}
         + [推播通知流量](using/push/push-gs.md)
         + [設定推播通知頻道](using/push/push-configuration.md)
         + [Mobile 上線快速入門工作流程](using/push/mobile-onboarding-wf.md)
   + 短信/彩信通道{#sms}
      + [開始使用文字訊息](using/sms/get-started-sms.md)
      + [建立文字簡訊 (SMS/MMS)](using/sms/create-sms.md)
      + [檢查並傳送文字訊息](using/sms/send-sms.md)
      + [管理文字訊息的選擇退出](using/sms/sms-opt-out.md)
      + [設定簡訊子網域](using/sms/sms-subdomains.md)
      + 設定短訊/彩信通道{#configure-sms}
         + [開始使用簡訊設定](using/sms/sms-configuration.md)
         + [設定 Sinch 提供者](using/sms/sms-configuration-sinch.md)
         + [設定 Infobip 提供者](using/sms/sms-configuration-infobip.md)
         + [設定 Twilio 提供者](using/sms/sms-configuration-twilio.md)
         + [設定自訂提供者 (Beta)](using/sms/sms-configuration-custom.md)
         + [建立簡訊設定](using/sms/sms-configuration-surface.md)
   + 直接郵件 {#direct-mail}
      + [開始使用直接郵件](using/direct-mail/get-started-direct-mail.md)
      + [建立直接郵件](using/direct-mail/create-direct-mail.md)
      + [檢查並傳送直接郵件訊息](using/direct-mail/test-send-direct-mail.md)
      + [設定直接郵件](using/direct-mail/direct-mail-configuration.md)
   + 網頁管道 {#web}
      + [開始使用網路頻道](using/web/get-started-web.md)
      + 設定網站通道 {#configure-web-channel}
         + [網路頻道先決條件](using/web/web-prerequisites.md)
         + [設定網頁子網域](using/web/web-delegated-subdomains.md)
         + [建立網頁管道設定](using/web/web-configuration.md)
      + [建立網站體驗](using/web/create-web.md)
      + 製作網頁 {#author-web-pages}
         + [使用網頁設計工具](using/web/web-visual-editor.md)
         + [使用非視覺化編輯器](using/web/web-non-visual-editor.md)
         + [管理修改](using/web/manage-web-modifications.md)
         + [監視網站體驗](using/web/monitor-web-experiences.md)
         + [編寫單頁應用程式](using/web/web-spa.md)
   + 基於程式碼的體驗 {#code-based-experience}
      + [開始使用程式碼型頻道](using/code-based/get-started-code-based.md)
      + 設定程式代碼型通道 {#configure-code-based-channel}
         + [護欄和限制](using/code-based/code-based-prerequisites.md)
         + [程式碼型體驗表面](using/code-based/code-based-surface.md)
         + [實施方法範例](using/code-based/code-based-implementation-samples.md)
         + [建立程式碼型體驗設定](using/code-based/code-based-configuration.md)
      + 建立程式碼型體驗 {#create-code-based-experiences}
         + [建立並撰寫程式碼型體驗](using/code-based/create-code-based.md)
         + [測試程式碼型體驗](using/code-based/test-code-based.md)
         + [管理程式碼型體驗](using/code-based/publish-code-based.md)
   + 內容卡{#content-card}
      + [開始使用內容卡](using/content-card/get-started-content-card.md)
      + 設定內容卡片通道 {#configure}
         + [內容卡的先決條件](using/content-card/content-card-configuration-prereq.md)
         + [在 Journey Optimizer 中設定內容卡頻道](using/content-card/content-card-configuration.md)
         + [在 Mobile SDK 中設定內容卡支援](using/content-card/content-card-lp.md)
         + [在 Web SDK 中設定內容卡支援](using/content-card/content-card-configuration-sdk.md)
      + [建立內容卡](using/content-card/create-content-card.md)
      + [設計內容卡](using/content-card/design-content-card.md)
   + WhatsApp{#whatsapp}
      + [開始使用 WhatsApp 訊息](using/whatsapp/get-started-whatsapp.md)
      + [在 Journey Optimizer 設定 WhatsApp 頻道](using/whatsapp/whatsapp-configuration.md)
      + [建立 WhatsApp 訊息](using/whatsapp/create-whatsapp.md)
      + [檢查並傳送 WhatsApp 訊息](using/whatsapp/send-whatsapp.md)
+ 登陸頁面 {#landing-pages}
   + [開始使用登陸頁面](using/landing-pages/get-started-lp.md)
   + [建立登陸頁面](using/landing-pages/create-lp.md)
   + 設計內容 {#landing-pages-design}
      + [關於登陸頁面設計](using/landing-pages/design-lp.md)
      + [建立登陸頁面內容](using/landing-pages/lp-content.md)
      + [建立範本](using/landing-pages/lp-templates.md)
      + [新增自訂 JavaScript](using/landing-pages/lp-custom-js.md)
   + [建立訂閱清單](using/landing-pages/subscription-list.md)
   + [透過使用案例了解](using/landing-pages/lp-use-cases.md)
   + 設定登陸頁面 {#lp-configuration}
      + [設定登陸頁面子網域](using/landing-pages/lp-subdomains.md)
      + [定義登陸頁面預設集](using/landing-pages/lp-presets.md)
+ 內容管理 {#content-management}
   + 用於內容產生的 AI 助理{#ai-assistant}
      + [開始使用 AI 助理](using/content-management/gs-generative.md)
      + [使用 AI 來產生電子郵件](using/content-management/generative-email.md)
      + [使用 AI 來產生推播](using/content-management/generative-push.md)
      + [使用 AI 來產生簡訊](using/content-management/generative-sms.md)
      + [使用 AI 來產生網頁](using/content-management/generative-web.md)
      + [使用 AI 的內容實驗](using/content-management/generative-experimentation.md)
      + [使用 AI 登陸頁面](using/content-management/generative-lp.md)
      + [AI 助理使用案例](using/content-management/generative-uc.md)
      + [建立及管理您的品牌 (Beta)](using/content-management/brands.md)
   + 使用多語言內容{#content-multilingual}
      + [開始使用多語言內容](using/content-management/multilingual-gs.md)
      + [建立地區](using/content-management/multilingual-locale.md)
      + [建立語言提供者](using/content-management/multilingual-provider.md)
      + [使用手動翻譯建立多語言內容](using/content-management/multilingual-manual.md)
      + [使用自動化翻譯建立多語言內容](using/content-management/multilingual-automated.md)
   + 使用內容實驗 {#content-experiment}
      + [開始使用內容實驗](using/content-management/get-started-experiment.md)
      + [建立內容實驗](using/content-management/content-experiment.md)
      + 技術說明 {#technotes}
         + [了解統計計算](using/content-management/experiment-calculations.md)
         + [了解實驗報告中的統計計算](using/content-management/experiment-report-calculations.md)
   + 個人化 {#personalization}
      + [開始使用個人化](using/personalization/personalize.md)
      + [新增個人化](using/personalization/personalization-build-expressions.md)
      + [個人化語法](using/personalization/personalization-syntax.md)
      + [重複使用運算式片段](using/personalization/use-expression-fragments.md)
      + [使用 Adobe Experience Platform 資料進行個人化 (Beta)](using/personalization/lookup-aep-data.md)
      + 輔助函數清單 {#functions}
         + [開始使用輔助函式](using/personalization/functions/functions.md)
         + [聚合函式](using/personalization/functions/aggregation.md)
         + [算術函式](using/personalization/functions/arithmetic-functions.md)
         + [陣列和清單功能](using/personalization/functions/arrays-list.md)
         + [日期函式](using/personalization/functions/dates.md)
         + [布林值和比較函式](using/personalization/functions/operators.md)
         + [輔助程式](using/personalization/functions/helpers.md)
         + [地圖函式](using/personalization/functions/maps.md)
         + [數學函式](using/personalization/functions/math.md)
         + [物件函式](using/personalization/functions/objects.md)
         + [字串函式](using/personalization/functions/string.md)
      + 個人化使用案例{#personalization-use-cases}
         + [訂單狀態通知](using/personalization/personalization-use-case.md)
         + [放棄購物車電子郵件](using/personalization/personalization-use-case-helper-functions.md)
         + [健康計劃處方電子郵件](using/personalization/perso-uc-plan-prescriptions.md)
   + 內容範本 {#content-templates}
      + [開始使用內容範本](using/content-management/content-templates.md)
      + [存取並管理範本](using/content-management/access-content-templates.md)
      + [建立內容範本](using/content-management/create-content-templates.md)
      + [鎖定電子郵件範本中的內容](using/content-management/content-locking.md)
      + [建立內容範本](using/content-management/test-content-templates.md)
      + [使用內容範本](using/content-management/use-content-templates.md)
   + 可重複使用的內容片段 {#fragments}
      + [開始使用片段](using/content-management/fragments.md)
      + [建立片段](using/content-management/create-fragments.md)
      + [將現有內容另存為片段](using/content-management/save-fragments.md)
      + [可自訂的片段](using/content-management/customizable-fragments.md)
      + [管理片段](using/content-management/manage-fragments.md)
   + 動態內容 {#dynamic}
      + [開始使用動態內容](using/personalization/get-started-dynamic-content.md)
      + [建立條件式規則](using/personalization/create-conditions.md)
      + [建立動態內容](using/personalization/dynamic-content.md)
+ Audiences、個人資料和身份{#audiences-profiles-identities}
   + 客群 {#audiences}
      + [開始使用 Audiences](using/audience/about-audiences.md)
      + 建立對象 {#create}
         + [區段定義](using/audience/creating-a-segment-definition.md)
         + [客群構成](using/audience/get-started-audience-orchestration.md)
         + [自訂上傳](using/audience/custom-upload.md)
         + [聯合客群構成](using/audience/federated-audience-composition.md)
      + [行銷活動和歷程中的對象啟用](using/audience/target-audiences.md)
      + [善用擴充屬性](using/audience/enrichment-attributes.md)
   + 輪廓{#profiles}
      + [開始使用輪廓](using/audience/get-started-profiles.md)
      + [建立測試輪廓](using/audience/creating-test-profiles.md)
      + [使用計算屬性](using/audience/computed-attributes.md)
   + [身分識別](using/audience/get-started-identity.md)
   + [授權使用情況](using/audience/license-usage.md)
+ 整合{#integrations}
   + [與其他解決方案整合](using/integrations/ajo-integrations.md)
   + [使用 Experience Manager Assets](using/integrations/assets.md)
   + [使用 Adobe Stock](using/integrations/stock.md)
   + [使用 Adobe Express 工作](using/integrations/express.md)
   + [使用 Experience Manager 範本工作](using/integrations/aem-templates.md)
   + [使用 Experience Manager 內容片段工作](using/integrations/aem-fragments.md)
   + [使用 Dynamic Media 工作](using/integrations/aem-dynamic.md)
   + [使用 GenStudio 工作](using/integrations/genstudio.md)
+ 追蹤與監視 {#reporting}
   + 即時報告 {#live-report}
      + [開始使用即時報告](using/reports/live-report.md)
      + [指標清單](using/reports/live-report-components.md)
      + [歷程即時報告](using/reports/journey-live-report.md)
      + [行銷活動即時報告](using/reports/campaign-live-report.md)
      + [登陸頁面即時報告](using/reports/lp-report-live.md)
      + [訂閱清單即時報告](using/reports/subscription-report-live.md)
   + 所有時程報表{#channel-report}
      + [開始使用所有時間報告](using/reports/report-gs-cja.md)
      + [指標清單](using/reports/global-report-components-cja.md)
      + [手動設定客戶歷程分析](using/reports/cja-ajo.md)
      + [管理您的報告](using/reports/report-cja-manage.md)
      + [報告與實驗先決條件](using/reports/reporting-configuration.md)
      + 行銷活動報告{#reporting}
         + [行銷活動報告](using/reports/campaign-global-report-cja.md)
         + [程式碼型行銷活動報告](using/reports/campaign-global-report-cja-code.md)
         + [內容卡行銷活動報告](using/reports/campaign-global-report-cja-content.md)
         + [直接郵件行銷活動報告](using/reports/campaign-global-report-cja-direct.md)
         + [電子郵件行銷活動報告](using/reports/campaign-global-report-cja-email.md)
         + [實驗行銷活動報告](using/reports/campaign-global-report-cja-experimentation.md)
         + [應用程式內行銷活動報告](using/reports/campaign-global-report-cja-inapp.md)
         + [推播通知行銷活動報告](using/reports/campaign-global-report-cja-push.md)
         + [簡訊行銷活動報告](using/reports/campaign-global-report-cja-sms.md)
         + [網頁行銷活動報告](using/reports/campaign-global-report-cja-web.md)
      + 歷程報告{#reporting}
         + [歷程報告](using/reports/journey-global-report-cja.md)
         + [程式碼型歷程報告](using/reports/journey-global-report-cja-code.md)
         + [內容卡歷程報告](using/reports/journey-global-report-cja-content.md)
         + [直接郵件歷程報告](using/reports/journey-global-report-cja-direct.md)
         + [電子郵件歷程報告](using/reports/journey-global-report-cja-email.md)
         + [應用程式內歷程報告](using/reports/journey-global-report-cja-inapp.md)
         + [推播歷程報告](using/reports/journey-global-report-cja-push.md)
         + [簡訊歷程報告](using/reports/journey-global-report-cja-sms.md)
         + [網頁歷程報告](using/reports/journey-global-report-cja-web.md)
      + [概述報表](using/reports/channel-report-cja.md)
      + [登陸頁面報告](using/reports/lp-report-global-cja.md)
      + [訂閱清單報告](using/reports/subscription-report-global-cja.md)
   + 歷程報告 {#reports}
      + [建立歷程報告](using/reports/sharing-overview.md)
      + [步驟事件欄位清單](using/reports/sharing-field-list.md)
      + 舊版步驟事件欄位 {#legacy-step-event-fields}
         + [關於舊版欄位](using/reports/sharing-legacy-fields.md)
         + [歷程欄位](using/reports/sharing-journey-fields.md)
         + [常用欄位](using/reports/sharing-common-fields.md)
         + [動作執行欄位](using/reports/sharing-execution-fields.md)
         + [資料擷取欄位](using/reports/sharing-fetch-fields.md)
         + [身分識別欄位](using/reports/sharing-identity-fields.md)
      + [查詢範例](using/reports/query-examples.md)
   + 傳遞能力 {#deliverability}
      + [開始使用傳遞能力](using/reports/deliverability.md)
      + [瞭解禁止名單](using/reports/suppression-list.md)
      + [新的 DMARC 需求](using/configuration/dmarc-record-update.md)
   + [警示](using/reports/alerts.md)
   + [排除原因](using/reports/exclusion-list.md)
+ 決策能力 {#decisioning}
   + [開始使用決定功能](using/experience-decisioning/gs-decision.md)
   + 決策 {#experience-decisioning}
      + [開始使用 Decisioning](using/experience-decisioning/gs-experience-decisioning.md)
      + [決策護欄與限制](using/experience-decisioning/decisioning-guardrails.md)
      + API 參考{#api-reference}
         + 建立和管理優惠方案專案 {#create-manage}
            + 決定項目{#decision-items}
               + [建立決定項目](using/experience-decisioning/api-reference/decisions-items/create.md)
               + [決定項目清單](using/experience-decisioning/api-reference/decisions-items/decision-items-list.md)
               + [刪除決定項目](using/experience-decisioning/api-reference/decisions-items/delete.md)
               + [查找決定項目](using/experience-decisioning/api-reference/decisions-items/lookup.md)
               + [更新決定項目](using/experience-decisioning/api-reference/decisions-items/update.md)
            + 專案集合{#items-collections}
               + [建立項目集合](using/experience-decisioning/api-reference/items-collections/create.md)
               + [刪除項目集合](using/experience-decisioning/api-reference/items-collections/delete.md)
               + [項目集合清單](using/experience-decisioning/api-reference/items-collections/items-collections-list.md)
               + [查找項目集合](using/experience-decisioning/api-reference/items-collections/lookup.md)
               + [更新項目集合](using/experience-decisioning/api-reference/items-collections/update.md)
            + 選擇策略{#selection-strategies}
               + [建立選擇策略](using/experience-decisioning/api-reference/selection-strategies/create.md)
               + [刪除選擇策略](using/experience-decisioning/api-reference/selection-strategies/delete.md)
               + [查找選擇策略](using/experience-decisioning/api-reference/selection-strategies/lookup.md)
               + [選擇策略清單](using/experience-decisioning/api-reference/selection-strategies/selection-strategies-list.md)
               + [更新選擇策略](using/experience-decisioning/api-reference/selection-strategies/update.md)
            + 排名公式{#ranking-formulas}
               + [建立排名公式](using/experience-decisioning/api-reference/ranking-formulas/create.md)
               + [刪除排名公式](using/experience-decisioning/api-reference/ranking-formulas/delete.md)
               + [查詢排名公式](using/experience-decisioning/api-reference/ranking-formulas/lookup.md)
               + [選擇排名公式](using/experience-decisioning/api-reference/ranking-formulas/ranking-formulas-list.md)
               + [更新排名公式](using/experience-decisioning/api-reference/ranking-formulas/update.md)
            + 適用性規則{#eligibility-rules}
               + [建立適用性規則](using/experience-decisioning/api-reference/eligibility-rules/create.md)
               + [刪除適用性規則](using/experience-decisioning/api-reference/eligibility-rules/delete.md)
               + [查詢適用性規則](using/experience-decisioning/api-reference/eligibility-rules/lookup.md)
               + [適用性規則清單](using/experience-decisioning/api-reference/eligibility-rules/eligibility-rules-list.md)
               + [更新適用性規則](using/experience-decisioning/api-reference/eligibility-rules/update.md)
         + [使用程式碼型體驗頻道提供優惠方案](using/experience-decisioning/api-reference/deliver.md)
      + 管理決定項目 {#decision-items}
         + [設定項目目錄](using/experience-decisioning/catalogs.md)
         + [建立決定項目](using/experience-decisioning/items.md)
         + [管理項目集合](using/experience-decisioning/collections.md)
      + 設定項目選擇 {#selection}
         + [建立決定規則](using/experience-decisioning/rules.md)
         + [建立排名方法](using/experience-decisioning/ranking.md)
         + [善用內容資料](using/experience-decisioning/context-data.md)
      + [建立選擇策略](using/experience-decisioning/selection-strategies.md)
      + [建立決定原則](using/experience-decisioning/create-decision.md)
      + [Decisioning 上的報告](using/experience-decisioning/cja-reporting.md)
      + [Decisioning 使用案例](using/experience-decisioning/experience-decisioning-uc.md)
   + 決策管理 {#offer-decisioning}
      + 決策管理入門 {#get-started-decision}
         + [關於決定管理](using/offers/get-started/starting-offer-decisioning.md)
         + [決策管理護欄與限制](using/offers/decision-management-guardrails.md)
         + [使用者介面](using/offers/get-started/user-interface.md)
         + [建立和管理優惠的重要步驟](using/offers/offer-library/key-steps.md)
         + [善用自訂上傳對象，以便做決策](using/offers/custom-upload-decisioning.md)
         + [使用案例：在電子郵件中插入產品建議](using/offers/offers-e2e.md)
      + 建立元件 {#create-components}
         + [建立位置](using/offers/offer-library/creating-placements.md)
         + [建立決定規則](using/offers/offer-library/creating-decision-rules.md)
         + [建立集合限定詞](using/offers/offer-library/creating-tags.md)
      + 建立排名 {#rankings}
         + [開始使用排名](using/offers/ranking/get-started-rankings.md)
         + [排名公式](using/offers/ranking/create-ranking-formulas.md)
         + AI 模型 {#ai-models}
            + [關於 AI 模型](using/offers/ranking/ai-models.md)
            + AI 模式類型 {#ai-model-types}
            + [自動最佳化模型](using/offers/ranking/auto-optimization-model.md)
            + [個人化最佳化模型](using/offers/ranking/personalized-optimization-model.md)
            + [建立 AI 模型](using/offers/ranking/create-ranking-strategies.md)
      + 建立 &amp; 管理 優惠 {#managing-offers-in-the-offer-library}
         + 設定選件 {#configure-offers}
            + [建立個人化產品建議](using/offers/offer-library/creating-personalized-offers.md)
            + [新增代表](using/offers/offer-library/add-representations.md)
            + [新增限制](using/offers/offer-library/add-constraints.md)
         + [建立後備產品建議](using/offers/offer-library/creating-fallback-offers.md)
         + [建立集合](using/offers/offer-library/creating-collections.md)
      + 建立和管理決策 {#create-manage-activities}
         + [建立決定](using/offers/offer-activities/create-offer-activities.md)
         + [設定決定中的產品建議選擇](using/offers/offer-activities/configure-offer-selection.md)
         + [建立模擬](using/offers/offer-activities/simulation.md)
      + [使用批次決策](using/offers/batch-delivery.md)
      + 收集事件資料 {#collect-event-data}
         + [開始使用資料收集](using/offers/data-collection/data-collection.md)
         + [建立資料集以收集事件](using/offers/data-collection/create-dataset.md)
         + [設定事件擷取](using/offers/data-collection/schema-requirement.md)
      + 善用內容資料 {#context-data}
         + [開始使用內容資料](using/offers/context-data.md)
         + [內容資料與邊緣決策請求](using/offers/context-data-edge.md)
         + [內容資料與決策請求](using/offers/context-data-decisioning.md)
      + 建立決策管理報表 {#create-reports}
         + [使用決策管理事件](using/offers/reports/get-started-events.md)
         + [存取事件 XDM 欄位](using/offers/reports/xdm-fields.md)
      + 導出優惠方案目錄 {#export-catalog}
         + [開始使用產品建議目錄匯出  ](using/offers/export-catalog/get-started-export.md)
         + [存取匯出的產品建議目錄](using/offers/export-catalog/access-dataset.md)
         + [個人化產品建議資料集](using/offers/export-catalog/export-offers.md)
         + [決定資料集](using/offers/export-catalog/export-decisions.md)
         + [位置資料集](using/offers/export-catalog/export-placements.md)
         + [遞補資料集](using/offers/export-catalog/export-fallback.md)
      + API 參考 {#api-reference}
         + [快速入門](using/offers/api-reference/getting-started.md)
         + 使用 API 的 建立 &amp; 管理 選件 {#offers-api}
            + 版位 {#placements}
               + [清單位置](using/offers/api-reference/offers-api/placements/placements-list.md)
               + [查詢位置](using/offers/api-reference/offers-api/placements/lookup.md)
               + [建立位置](using/offers/api-reference/offers-api/placements/create.md)
               + [更新位置](using/offers/api-reference/offers-api/placements/update.md)
               + [刪除位置](using/offers/api-reference/offers-api/placements/delete.md)
            + 決定規則 {#decision-rules}
               + [清單決定規則](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
               + [查詢決定規則](using/offers/api-reference/offers-api/decision-rules/lookup.md)
               + [建立決定規則](using/offers/api-reference/offers-api/decision-rules/create.md)
               + [更新決定規則](using/offers/api-reference/offers-api/decision-rules/update.md)
               + [刪除決定規則](using/offers/api-reference/offers-api/decision-rules/delete.md)
            + 集合限定詞 {#tags}
               + [列出集合限定詞](using/offers/api-reference/offers-api/tags/tags-list.md)
               + [查詢集合限定詞](using/offers/api-reference/offers-api/tags/lookup.md)
               + [建立集合限定詞](using/offers/api-reference/offers-api/tags/create.md)
               + [更新集合限定詞](using/offers/api-reference/offers-api/tags/update.md)
               + [刪除集合限定詞](using/offers/api-reference/offers-api/tags/delete.md)
            + 個人化產品建議 {#personalized-offers}
               + [列出個人化產品建議](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
               + [查詢個人化產品建議](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
               + [建立個人化產品建議](using/offers/api-reference/offers-api/personalized-offers/create.md)
               + [更新個人化產品建議](using/offers/api-reference/offers-api/personalized-offers/update.md)
               + [刪除個人化產品建議](using/offers/api-reference/offers-api/personalized-offers/delete.md)
            + 集合 {#collections}
               + [清單集合](using/offers/api-reference/offers-api/collections/collections-list.md)
               + [查詢集合](using/offers/api-reference/offers-api/collections/lookup.md)
               + [建立集合](using/offers/api-reference/offers-api/collections/create.md)
               + [更新集合](using/offers/api-reference/offers-api/collections/update.md)
               + [刪除集合](using/offers/api-reference/offers-api/collections/delete.md)
            + 後備產品建議 {#fallback-offers}
               + [列出後備產品建議](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
               + [查詢後備產品建議](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
               + [建立後備產品建議](using/offers/api-reference/offers-api/fallback-offers/create.md)
               + [更新後備產品建議](using/offers/api-reference/offers-api/fallback-offers/update.md)
               + [刪除後備產品建議](using/offers/api-reference/offers-api/fallback-offers/delete.md)
            + 決策 {#decisions-api}
               + [列舉決定](using/offers/api-reference/activities-api/activities/activities-list.md)
               + [查詢決定](using/offers/api-reference/activities-api/activities/lookup.md)
               + [建立決定](using/offers/api-reference/activities-api/activities/create.md)
               + [更新決定](using/offers/api-reference/activities-api/activities/update.md)
               + [刪除決定](using/offers/api-reference/activities-api/activities/delete.md)
            + 舊版 API {#legacy-api}
               + [關於舊版 API](using/offers/api-reference/offers-api/legacy-apis/about-legacy-apis.md)
               + 版位 {#placements}
                  + [清單位置](using/offers/api-reference/offers-api/legacy-apis/placements/placements-list.md)
                  + [查詢位置](using/offers/api-reference/offers-api/legacy-apis/placements/lookup.md)
                  + [建立位置](using/offers/api-reference/offers-api/legacy-apis/placements/create.md)
                  + [更新位置](using/offers/api-reference/offers-api/legacy-apis/placements/update.md)
                  + [刪除位置](using/offers/api-reference/offers-api/legacy-apis/placements/delete.md)
               + 決定規則 {#decision-rules}
                  + [清單決定規則](using/offers/api-reference/offers-api/legacy-apis/decision-rules/rules-list.md)
                  + [查詢決定規則](using/offers/api-reference/offers-api/legacy-apis/decision-rules/lookup.md)
                  + [建立決定規則](using/offers/api-reference/offers-api/legacy-apis/decision-rules/create.md)
                  + [更新決定規則](using/offers/api-reference/offers-api/legacy-apis/decision-rules/update.md)
                  + [刪除決定規則](using/offers/api-reference/offers-api/legacy-apis/decision-rules/delete.md)
               + 集合限定詞 {#tags}
                  + [列出集合限定詞](using/offers/api-reference/offers-api/legacy-apis/tags/tags-list.md)
                  + [查詢集合限定詞](using/offers/api-reference/offers-api/legacy-apis/tags/lookup.md)
                  + [建立集合限定詞](using/offers/api-reference/offers-api/legacy-apis/tags/create.md)
                  + [更新集合限定詞](using/offers/api-reference/offers-api/legacy-apis/tags/update.md)
                  + [刪除集合限定詞](using/offers/api-reference/offers-api/legacy-apis/tags/delete.md)
               + 個人化產品建議 {#personalized-offers}
                  + [列出個人化產品建議](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/offers-list.md)
                  + [查詢個人化產品建議](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/lookup.md)
                  + [建立個人化產品建議](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/create.md)
                  + [更新個人化產品建議](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/update.md)
                  + [刪除個人化產品建議](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/delete.md)
               + 後備產品建議 {#fallback-offers}
                  + [列出後備產品建議](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/fallback-list.md)
                  + [查詢後備產品建議](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/lookup.md)
                  + [建立後備產品建議](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/create.md)
                  + [更新後備產品建議](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/update.md)
                  + [刪除後備產品建議](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/delete.md)
               + 集合 {#collections}
                  + [清單集合](using/offers/api-reference/offers-api/legacy-apis/collections/collections-list.md)
                  + [查詢集合](using/offers/api-reference/offers-api/legacy-apis/collections/lookup.md)
                  + [建立集合](using/offers/api-reference/offers-api/legacy-apis/collections/create.md)
                  + [更新集合](using/offers/api-reference/offers-api/legacy-apis/collections/update.md)
                  + [刪除集合](using/offers/api-reference/offers-api/legacy-apis/collections/delete.md)
               + 決策 {#decisions-api}
                  + [列舉決定](using/offers/api-reference/offers-api/legacy-apis/activities-api/activities-list.md)
                  + [查詢決定](using/offers/api-reference/offers-api/legacy-apis/activities-api/lookup.md)
                  + [建立決定](using/offers/api-reference/offers-api/legacy-apis/activities-api/create.md)
                  + [更新決定](using/offers/api-reference/offers-api/legacy-apis/activities-api/update.md)
                  + [刪除決定](using/offers/api-reference/offers-api/legacy-apis/activities-api/delete.md)
         + 使用 API 傳送選件 {#offer-delivery-api}
            + [開始使用傳遞產品建議 API](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
            + [決策 API](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
            + [邊緣決策 API](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
            + [批次決策 API](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ 資料管理 {#data-management}
   + [開始使用資料管理](using/data/gs-data.md)
   + [使用結構描述](using/data/get-started-schemas.md)
   + Journey Optimizer 數據集 {#datasets}
      + [開始使用資料集](using/data/get-started-datasets.md)
      + [資料集存留時間 (TTL) 護欄](using/data/datasets-ttl.md)
      + [匯出 Journey Optimizer 資料集](using/data/export-datasets.md)
      + [查詢範例](using/data/datasets-query-examples.md)
      + [內建結構 >](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=zh-Hant)
   + [查詢](using/data/get-started-queries.md)
+ 管道設定 {#configuration}
   + [配置您的頻道](using/configuration/get-started-configuration.md)
   + [設定管道設定](using/configuration/channel-surfaces.md)
   + 引導式通道設定 {#guided-setup}
      + [開始使用引導式管道設定](using/configuration/set-mobile-config.md)
      + [建立管道設定](using/configuration/create-channel-set-up.md)
   + 委派電子郵件子域 {#delegate-subdomains}
      + [開始使用子網域委派](using/configuration/about-subdomain-delegation.md)
      + [委派子網域](using/configuration/delegate-subdomain.md)
      + [設定 DMARC 記錄](using/configuration/dmarc-record.md)
      + [新增 Google TXT 記錄](using/configuration/google-txt.md)
      + [存取和編輯 PTR 記錄](using/configuration/ptr-records.md)
      + [建立 IP 集區](using/configuration/ip-pools.md)
   + 實施IP預熱計劃 {#implement-ip-warmup-plan}
      + [開始使用 IP 暖身計劃](using/configuration/ip-warmup-gs.md)
      + [建立 IP 暖身行銷活動](using/configuration/ip-warmup-campaign.md)
      + [建立 IP 暖身計劃](using/configuration/ip-warmup-plan.md)
      + [執行 IP 暖身計劃](using/configuration/ip-warmup-execution.md)
      + [IP 暖身計劃檔案](using/configuration/ip-warmup-plan-files.md)
   + 監控電子郵件位址 {#monitor-reputation}
      + [禁止名單](using/configuration/manage-suppression-list.md)
      + [重試次數](using/configuration/retries.md)
      + [允許清單](using/configuration/allow-list.md)
   + [使用種子清單](using/configuration/seed-lists.md)
   + [支援封存](using/configuration/archiving-support.md)
   + [變更執行地址](using/configuration/primary-email-addresses.md)
   + [設定業務規則](using/configuration/frequency-rules.md)
   + [使用規則集](using/configuration/rule-sets.md)
+ 歷程設定 {#configure-journeys}
   + [設定資料來源、事件和動作](using/configuration/about-data-sources-events-actions.md)
   + 事件設定 {#events-journeys}
      + [使用歷程事件](using/event/about-events.md)
      + [設定單一事件](using/event/about-creating.md)
      + [關於 ExperienceEvent 結構描述](using/event/experience-event-schema.md)
      + [使用Adobe Analytics數據](using/event/about-analytics.md)
      + [設定業務事件](using/event/about-creating-business.md)
      + [傳送事件的其他步驟](using/event/additional-steps-to-send-events-to-journey.md)
   + 數據源組態{#data-source-journeys}
      + [開始使用資料來源](using/datasource/about-data-sources.md)
      + [設定資料來源](using/datasource/configure-data-sources.md)
      + [Adobe Experience Platform 資料來源](using/datasource/adobe-experience-platform-data-source.md)
      + [外部資料來源](using/datasource/external-data-sources.md)
   + 動作設定 {#action-journeys}
      + [開始使用自訂動作](using/action/action.md)
      + [設定自訂動作](using/action/about-custom-action-configuration.md)
      + [設定自訂動作](using/action/troubleshoot-custom-action.md)
      + [在自訂動作中使用 API 呼叫回應](using/action/action-response.md)
+ 連接您的系統 {#connect-systems}
   + 與外部系統整合 {#external-systems}
      + [與外部系統整合的歷程](using/configuration/external-systems.md)
      + [設定 API 上限](using/configuration/capping.md)
      + [節流 API](using/configuration/throttling.md)
   + 傳送Adobe Systems解決方案 {#adobe-solutions}
      + [歷程與 Adobe Campaign Standard 整合](using/action/acs-action.md)
      + [歷程與 Adobe Campaign v7/v8 整合](using/action/acc-action.md)
      + [歷程與 Marketo Engage 整合](using/action/marketo-engage.md)
   + [配置源連接器](using/start/get-started-sources.md)
   + [將物件匯出至另一個沙箱](using/configuration/copy-objects-to-sandbox.md)
   + [使用 Journey Optimizer API](using/configuration/ajo-apis.md)
+ 存取控制 {#access-control}
   + 存取控制概覽 {#privacy}
      + [開始使用使用者管理](using/administration/permissions-overview.md)
      + [內建角色](using/administration/ootb-product-profiles.md)
      + [內建權限](using/administration/ootb-permissions.md)
      + [權限層級](using/administration/high-low-permissions.md)
   + [管理使用者和角色](using/administration/permissions.md)
   + [以屬性為基礎的存取控制](using/administration/attribute-based-access.md)
   + [物件等級存取控制](using/administration/object-based-access.md)
   + [沙箱管理](using/administration/sandboxes.md)
+ 隱私權 {#privacy}
   + [開始使用隱私權](using/privacy/get-started-privacy.md)
   + [隱私權請求](using/privacy/requests.md)
   + [針對資源的稽核動作](using/privacy/audit-logs.md)
   + [執行資料生命週期作業](using/privacy/data-hygiene.md)
   + 管理同意 {#consent}
      + [管理選擇退出](using/privacy/opt-out.md)
      + [使用同意原則](using/action/consent.md)
   + [資料治理](using/action/action-privacy.md)
   + [設定和管理客戶託管金鑰](using/privacy/cmk.md)
