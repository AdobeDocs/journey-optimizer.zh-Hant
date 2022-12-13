---
solution: Journey Optimizer
product: journey optimizer
title: 檔案更新
description: 了解最新檔案更新
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 3adcd750089d81e6216316dc3d39f6a7982033f4
workflow-type: tm+mt
source-wordcount: '2246'
ht-degree: 0%

---

# 檔案更新 {#latest-updates}

本頁面列出 [!DNL Journey Optimizer].

## 2022年12月 {#december-2022}

* 「訊息指南」已重新整理，並分割為每個管道的專用指南：

   * [電子郵件通道](../email/get-started-email.md)
   * [推播通知通道](../push/get-started-push.md)
   * [SMS通道](../sms/get-started-sms.md)

* 已重新整理設定指南，以改善可讀性。 [了解詳情](../configuration/get-started-configuration.md)

## 2022年11月 {#november-2022}

* 新增有關Journey Optimizer整合的頁面。 [了解詳情](../start/ajo-integrations.md)
* 新增關於鏡像頁面URL長度的建議。 [了解詳情](../email/message-tracking.md)
* 電子郵件設定設定的新小節已新增至電子郵件地址的回覆，包括確保正確回覆管理的建議。 [了解詳情](../email/email-settings.md#reply-to-email)
* 已新增如何修改即時歷程中訊息內容的區段。 [了解詳情](../building-journeys/journeys-message.md#update-live-content)

## 2022年10月 {#october-2022}

* 新增如何使用外部資料來源和自訂動作來限制輸送量的歷程使用案例。 [了解詳情](../building-journeys/limit-throughput.md)
* 歷程使用案例區段已重新組織為兩個類別： [業務使用案例](../building-journeys/journeys-uc.md) 和 [技術使用案例](../building-journeys/collections.md).
* 此 **實體資料集** 區段已更新，其中包含更多詳細資訊。 [了解詳情](../data/datasets-query-examples.md#entity-dataset)
* 已重新組織「退出管理」和「同意」政策章節。 [了解詳情](../privacy/opt-out.md)
* 歷程訊息中進階參數的區段已經釐清，現在指定電子郵件地址覆寫僅應用於特定使用案例。 在大部分時間中，定義為 **執行欄位** 才應該使用。
* 在 **設定登錄頁面子網域** 區段來指定登錄頁面子網域中不允許使用大寫字母。 [了解詳情](../landing-pages/lp-subdomains.md)

## 2022年9月 {#september-2022}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』22年9月的發行詳情請參閱本檔案。 [了解詳情](release-notes.md)
* 新增在循環讀取區段歷程中使用等待活動的相關最佳實務。 [了解詳情](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 新增新的步驟事件查詢範例，以及id、instanceid和profileid之間差異的資訊。 [了解詳情](../reports/query-examples.md).
* 更新與 [toDateOnly](../building-journeys/functions/functiontodateonly.md) 和 [toString](../building-journeys/functions/functiontostring.md) 函式。
* 已新增時間條件參數的詳細資訊。 [了解詳情](../building-journeys/condition-activity.md#time_condition)
* 已新增內建資料集的相關資訊。 [了解詳情](../data/get-started-datasets.md#access-datasets)
* 改善並重新組織「全域報表」和「即時報表」章節。 [了解詳情](../reports/global-report.md)
* 已新增Adobe Journey Optimizer中可用的每個報表量度的清單。
   [了解詳情](../reports/global-report.md#email-and-sms-metrics)
* 「密件副本」電子郵件區段已移至新的「支援封存」頁面。 [了解詳情](../configuration/archiving-support.md)

## 2022年8月 {#august-2022}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』22年8月的發行詳情請參閱本檔案。 [了解詳情](release-notes.md)
* 「頻率規則」區段已更新，以反映新的線上傳訊流程。 [了解詳情](../configuration/frequency-rules.md#apply-frequency-rule)
* 現在「開始使用登錄頁面」區段會參考有關如何設定訂閱和建立登錄頁面的影片。 [了解詳情](../landing-pages/get-started-lp.md#video)
* 已新增使用讀取區段活動之歷程的限制。 [了解詳情](../building-journeys/read-segment.md)
* 已改善運算式編輯器運算子頁面。 [了解詳情](../building-journeys/expression/operators.md)
* 已新增如何排程促銷活動的區段。 [了解詳情](../campaigns/create-campaign.md)
* 已更新運算式編輯器的一般語法規則區段，以考慮常值函式中反斜線符號逸出的新規則。 此變更不會影響現有的已發佈訊息。 只能更新新訊息或草稿訊息。 [了解詳情](../personalization/personalization-syntax.md#general-rules)

## 2022年7月 {#july-2022}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』22年7月的發行詳情載於本檔案。 [了解詳情](release-notes.md)
* 此 **設定通道曲面** 區段已釐清，並更新為說明如何設定SMS通道的頁面連結。 [了解詳情](../configuration/channel-surfaces.md#create-channel-surface)
* 在歷程屬性中， **設定檔時區** 選項現在預設為停用。 [了解詳情](../building-journeys/timezone-management.md#timezone-from-profiles)
* 在 **等待** 活動， **固定日期** 選項已無法使用。 [了解詳情](../building-journeys/wait-activity.md)
* 已新增 **增量讀取** 選項 **讀取區段** 活動。 [了解詳情](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 在 **設定檔上限** 條件類型。 [了解詳情](../building-journeys/condition-activity.md#profile_cap)
* 新增對業務事件的限制。 [了解詳情](../start/guardrails.md#events-g)

## 2022年6月 {#june-2022}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』22年6月的發行詳情請參閱本檔案。 [了解詳情](release-notes.md)
* 檔案中已新增有關隱私權要求的新章節。 [了解詳情](../privacy/requests.md)
* 檔案中已新增有關資源稽核記錄的新區段。 [了解詳情](../privacy/audit-logs.md)
* 檔案中已新增有關如何將來自Adobe Experience Cloud資產資料庫的HTML或JSON內容新增至選件表示法的新區段。 [了解詳情](../offers/offer-library/add-representations.md#html-json)
* 新增歷程生命週期的頁面。 [了解詳情](../building-journeys/journey.md#journey-versions)
* 更新「等待」活動頁面。 [了解詳情](../building-journeys/wait-activity.md)
* 新增Adobe Journey Optimizer資料集清單及查詢範例。 [了解詳情](../data/datasets-query-examples.md)
* 「允許的清單」頁面已移至「設定」區段。 [了解詳情](../configuration/allow-list.md)
* 「隱藏」清單頁已更新，以澄清一些資訊，包括在隱藏原因欄位中允許包含32到126之間的所有ASCII字元的事實。 [了解詳情](../configuration/manage-suppression-list.md)
* 已新增「決策」管理的護欄和靜態限制的連結。 [了解詳情](../start/guardrails.md)
* 「傳送時間最佳化」現在可供所有客戶使用。 已移除測試版提及。 [了解詳情](../building-journeys/journeys-message.md#send-time-optimization)
* 已將Batch Decisioning API新增至可用API清單，以傳遞個人化優惠方案。 [了解詳情](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## 2022年5月 {#may-2022}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』22年5月的發行詳情請參閱本檔案。 [了解詳情](release-notes.md)
* 相關的新查詢範例 [區段資格](../reports/query-examples.md#segment-qualification-queries) 和 [事件](../reports/query-examples.md#event-based-queries) 已新增。
* 電子郵件設計區段現在提及新的內建範本，這些範本可用來開始內容。 更新相關螢幕擷取畫面。 [了解詳情](../email/get-started-email-design.md)
* Journey Optimizer檔案首頁更新了關鍵資源的連結。
* 更新登錄頁面和訂閱報表的螢幕擷取畫面。 [了解詳情](../reports/live-report.md)
* 已新增附註，指出自訂動作不支援「刪除」方法。 [了解詳情](../action/about-custom-action-configuration.md)
* 更新操作說明影片的連結。
* 此 [電子郵件設定](../configuration/about-subdomain-delegation.md), [訊息預設集](../configuration/channel-surfaces.md) 和 [設定登錄頁面](../landing-pages/lp-subdomains.md) 已重新整理章節，以改善可讀性。
* 更新並改善「URL追蹤」章節，提供範例。 [了解詳情](../email/email-settings.md#url-tracking)
* 已新增關於設定轉寄電子郵件地址的新小節。 請注意，您無法透過使用者介面執行此作業。 [了解詳情](../email/email-settings.md#forward-email)

## 2022年4月 {#april-2022}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』22年4月的發行版本已在本檔案中詳細說明。 [了解詳情](release-notes.md)
* 此 **反應** 事件檔案頁面已更新。 [了解詳情](../building-journeys/reaction-events.md)
* 決策管理功能影片已更新，以反映Journey Optimizer使用者介面。 [了解詳情](../offers/get-started/starting-offer-decisioning.md)
* 此 **開始使用資料集** 區段已改良，以詳細說明如何存取和建立資料集。 [了解詳情](../data/get-started-datasets.md)
* 說明指南和產品發行說明的連結已新增至 **Adobe Journey Optimizer檔案** 首頁。 [了解詳情](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* 此 **建立訊息預設集** 節現在指定在所選IP池的版本下(**[!UICONTROL Processing]** 狀態)，且從未與選取的子網域相關聯。 [了解詳情](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* 訊息預設集 **URL追蹤** 區段已更新，以反映使用者介面的微幅變更。 [了解詳情](../configuration/channel-surfaces.md#url-tracking)

## 2022年3月 {#march-2022}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』22年3月發行版本已在檔案中詳細說明。 [了解詳情](release-notes.md)
* 已將AI模型快速入門的新頁面新增至 **Offer Decisioning** 小節，包括 [自動優化模型](../offers/ranking/auto-optimization-model.md)、其使用的演算法，以及更多技術詳細資訊。 [了解詳情](../offers/ranking/ai-models.md)
* 測試設定檔建立頁面已移至  **區段、設定檔與身分** 區段。 [了解詳情](../segment/creating-test-profiles.md)
* 新增如何在運算式編輯器中新增運算式作為預設值的範例。 [了解詳情](../building-journeys/expression/field-references.md#default-value)
* 此 **建立個人化優惠方案** 區段已重新整理，以改善可讀性。 [了解詳情](../offers/offer-library/creating-personalized-offers.md)
* 已新增新區段，說明變更優惠方案的開始和/或結束日期可能對此優惠方案的頻率限定產生的影響。 [了解詳情](../offers/offer-library/add-constraints.md#capping-change-date)
* 此 **變更主要電子郵件地址** 區段已更新，以反映使用者介面的變更。 [了解詳情](../configuration/primary-email-addresses.md)

## 2022年2月 {#feb-2022}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 本檔案已詳細說明』22年2月的發行版本。 [了解詳情](release-notes.md)
* 此 [replace](../building-journeys/functions/functionreplace.md#example_2) 和 [replaceAll](../building-journeys/functions/functionreplaceall.md#example) 函式檔案頁面已更新，其中包含與target參數有關的其他資訊和範例。
* 已將最佳實務新增至 [運算子](../building-journeys/expression/operators.md#important-notes) 頁面。

## 2022年1月 {#january-2022}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』22年1月發行版本已在檔案中詳細說明。 [了解詳情](release-notes.md)
* 此 **Offer decisioning AI排名** 區段已更新，其中包含自動最佳化模型的更詳細說明。 [了解詳情](../offers/ranking/auto-optimization-model.md)
* 已新增綱要需求的新區段，以便在使用排名策略時能夠傳入事件類型。 [了解詳情](../offers/ranking/schema-requirement.md)
* 與 [!DNL Journey Optimizer] 已重新整理個人化功能，以提高可讀性。 [了解詳情](../personalization/personalize.md)
* 此 **建立訊息預設集** 一節已分為幾節，以提高清晰度。 [了解詳情](../configuration/channel-surfaces.md#create-channel-surface)
* 此 **退出管理** 區段已釐清並稍微重新組織。 [了解詳情](../privacy/opt-out.md#opt-out-management)
* 此 **插入連結** 區段已更新，以反映最近使用者介面的變更。 [了解詳情](../email/message-tracking.md#insert-links)

## 2021年11月 {#november-2021}

* 的完整說明 **進階運算式編輯器** 現在可用於歷程。 [了解詳情](../building-journeys/expression/expressionadvanced.md)
* 關於 **CNAME子網域委派方法** 已新增。 [了解詳情](../configuration/delegate-subdomain.md#cname-subdomain-delegation)


## 2021年10月 {#october-2021}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 本檔案已詳細說明』21年10月發行版本。 [了解詳情](release-notes.md)
* 新增 **日期時間函式** 清單。 [了解詳情](../personalization/functions/dates.md)
* 新增 **每個使用者角色的快速入門區段**. 走自己的路，更快地達到目標！ [了解詳情](../start/quick-start.md)
* 新增 **編輯訊息預設集** 區段。 [了解詳情](../configuration/channel-surfaces.md#edit-channel-surface)
* 新增 **編輯PTR記錄** 區段。 [了解詳情](../configuration/ptr-records.md#edit-ptr-record)
* 新增 **停用訊息預設集** 區段。 [了解詳情](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* 新增限制至 **Decision Management API開發人員指南** 行動裝置不支援的選件限制 [!DNL Experience Edge] 工作流程。 [了解詳情](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* 新增 **建立模擬** 區段。 [了解詳情](../offers/offer-activities/simulation.md)
* 已更新 **添加決策範圍** 區段。 [了解詳情](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* 已更新 **定義表示的內容** 區段，包括新 [分段](../offers/offer-library/creating-personalized-offers.md#custom-text) 關於如何定義及個人化自訂文字。 [了解詳情](../offers/offer-library/creating-personalized-offers.md#content)

## 2021年9月 {#september-2021}

* 已更新下列函式頁面： [塞圖爾](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninsegment.md)

* 已新增下列函式： [篩選](../building-journeys/functions/functionfilter.md), [相交](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* 已在運算式編輯器檔案中新增dateOnly日期類型。 [了解詳情](../building-journeys/expression/data-types.md)

* 新增自訂動作快取持續時間的詳細資訊。 [了解詳情](../datasource/external-data-sources.md#custom-authentication-mode)

* 已新增自訂動作預設埠的資訊。 [了解詳情](../action/about-custom-action-configuration.md#url-configuration)

* 已新增有關多個業務事件使用案例的資訊。 [了解詳情](../event/about-creating-business.md#multiple-business-events)

* 新增在Data Lake中查詢歷程步驟事件的常用範例。 [了解詳情](../reports/query-examples.md)

* 新增 **限制** 頁面。 [了解詳情](../start/guardrails.md)

* 改善 **快速入門** 包含不同角色步驟的頁面。 [了解詳情](../start/quick-start.md)

* 現在，透過Offer Decisioning應用程式服務，專屬區段中所述的所有決策管理功能也適用於Adobe Experience Platform使用者。 [了解詳情](../offers/get-started/starting-offer-decisioning.md)

* 新增小節，釐清在套用限制以限制指定版位選擇優惠方案時，使用區段與決策規則之間的差異。 [了解詳情](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* 新增特定排名公式範例，以說明一些實際使用案例。 [了解詳情](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* 已新增如何編輯IP池的子區段。 [了解詳情](../configuration/ip-pools.md#edit-ip-pool)


## 2021年8月 {#august-2021}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』21年8月的發行詳情請參閱本檔案。 [了解詳情](release-notes.md)
* 更新決策管理權限。 [了解詳情](../administration/ootb-product-profiles.md)
* 使用最新UI更新電子郵件設計工具的螢幕擷取畫面。
* 更新具有動態URL路徑和動態標題之自訂動作的設定程式。 [了解詳情](../action/about-custom-action-configuration.md#url-configuration)
* 新增協助工具功能和捷徑的相關章節。 [了解詳情](../start/user-interface.md#accessibility)
* 新增區段評估方法的相關章節。 [了解詳情](../segment/about-segments.md#evaluation-method-in-journey-optimizer)
* 在「隱藏」清單、「允許」清單和「電子郵件全域/即時」報表區段中新增附註，以指定狀態為「隱藏」和「不允許」的設定檔會從「電子郵件報表傳送」量度中排除。 [了解詳情](../reports/global-report.md)
* 已新增新區段，說明如何擷取因未列在允許清單而從傳送排除的電子郵件地址或網域。 [了解詳情](../configuration/allow-list.md#reporting)
* 更新「啟用允許清單」區段。 [深入了解](../configuration/allow-list.md#enable-allow-list)
* 更新「監視」訊息預設集區段，其中包含可能的預設集建立失敗原因，以及這類錯誤的詳細資訊。 [了解詳情](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* 已更新並重新命名「重試時段」區段，以反映您現在可以調整訊息預設集中的電子郵件重試設定的事實。 [了解詳情](../configuration/retries.md#retry-duration)
* 已新增新區段，說明如何將一鍵式選擇退出連結插入電子郵件內容。 [了解詳情](../privacy/opt-out.md#one-click-opt-out-link)
* 更新委派子網域區段，其中包含Adobe執行之驗證程式的詳細資訊。 [了解詳情](../configuration/delegate-subdomain.md#subdomain-validation)
* 已新增區段，說明如何手動將電子郵件地址和網域新增至隱藏清單。 [了解詳情](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* 更新 [訪問隱藏清單](../configuration/manage-suppression-list.md#access-suppression-list) 區段與 [重試](../configuration/retries.md) 區段來反映新的使用者介面。
* 建立優惠方案時新增及設定表示法的新流程已記錄下來。 [了解詳情](../offers/offer-library/creating-personalized-offers.md#representations)


## 2021年7月 {#july-2021}

* 隨附的所有新功能和改善項目 [!DNL Journey Optimizer] 』21年7月的發行詳情載於本檔案。 [了解詳情](release-notes.md)
* 在 [!DNL Journey Optimizer] 首頁和目錄
* Experience Platform服務的新登錄頁面，於 [!DNL Journey Optimizer]
* 新增連結至 [!DNL Journey Optimizer] 首頁的產品說明
* 在多個頁面中新增教學課程影片
* 最佳化首頁影像
* 將「訊息追蹤」區段移動、改良及重新命名為「新增連結及追蹤訊息」。 [了解詳情](../email/message-tracking.md)
* 在鏡像頁面上新增子區段。 [了解詳情](../email/message-tracking.md#mirror-page)
* 在檔案和畫面中，將「選件活動」重新命名為「決策」，將「決策」重新命名為「決策範圍」。 [了解詳情](../offers/get-started/starting-offer-decisioning.md)
* 新使用案例： [使用協助程式功能個人化訊息](../personalization/personalization-use-case-helper-functions.md)
* 更新讀取段文檔以反映實體化段影響。 [了解詳情](../building-journeys/read-segment.md)
* 更新歷程限制。 [了解詳情](../start/guardrails.md)
* 更新「在決策中設定選件」區段。 [了解詳情](../offers/offer-activities/configure-offer-selection.md)
* 新增警告，提及目前不支援事件型選件。 [了解詳情](../offers/offer-library/creating-personalized-offers.md#eligibility)
* 記錄「決策管理」新 **[!UICONTROL Overview]** 標籤。 [了解詳情](../offers/get-started/user-interface.md#overview)
* 新增章節，說明優惠方案和決策清單中可用的動作： [選件清單](../offers/offer-library/creating-personalized-offers.md#offer-list) 和 [決策清單](../offers/offer-activities/create-offer-activities.md#decision-list).

