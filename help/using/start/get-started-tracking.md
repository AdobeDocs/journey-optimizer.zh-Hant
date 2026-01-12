---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用Journey Optimizer中的追蹤功能
description: 瞭解Journey Optimizer提供的追蹤和監控功能
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: 追蹤，監視，分析，報告，傳遞能力
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '1916'
ht-degree: 3%

---

# 開始使用Journey Optimizer中的追蹤功能 {#get-started-tracking}

追蹤可讓您評估行銷活動的成效、最佳化客戶體驗，並確保訊息送達其預期的收件者。 Journey Optimizer提供全方位追蹤功能，可擷取客戶互動、傳遞效能及系統健康狀況，協助您做出資料導向式決策，同時尊重隱私權並維護合規性。

大部分追蹤都會在您建立訊息和歷程時自動設定。 若是進階案例，您可以設定自訂量度、設定URL引數，以及與外部分析平台整合。 透過內建報告存取您的追蹤資料，或匯出資料以在Customer Journey Analytics中進行更深入的分析。

>[!BEGINSHADEBOX]

您可在Journey Optimizer中追蹤的內容：

📧 **電子郵件互動** — 開啟、點按和連結效能

🌐 **網頁行為** — 頁面檢視、點按和參與模式

🛤️ **歷程績效** — 自訂量度、步驟事件和轉換路徑

📊 **傳遞健康狀態** — 跳出率、垃圾郵件投訴和寄件者信譽

⚙️ **系統作業** — 警示、錯誤和自訂動作效能

>[!ENDSHADEBOX]

若要協助您開始使用，請探索這些基本的追蹤和監視主題：

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="量度" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong>設定成功量度</strong></a>
    </div>
    <p>
    <em>追蹤符合您業務目標的自訂KPI</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="傳遞能力" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>監視器傳遞能力</strong></a>
    </div>
    <p>
    <em>確定您的郵件已送達客戶收件匣</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="報告" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>探索報告</strong></a>
    </div>
    <p>
    <em>存取您的歷程與行銷活動的即時和歷史報告</em>
    <p>
  </td>
</tr>
</table>

## 跨頻道追蹤客戶互動 {#tracking-by-channel}

Journey Optimizer提供通道專用的追蹤功能。 以下說明如何為每個頻道設定和使用追蹤。

+++電子郵件追蹤

當您建立電子郵件訊息時，會自動啟用電子郵件追蹤。 Journey Optimizer預設會追蹤開啟、點按和取消訂閱，不需額外設定。

**設定追蹤選項：**

* **啟用/停用追蹤** — 在設計您的電子郵件時，在郵件層級控制追蹤。 您可以選擇追蹤開啟和/或點按。 [了解更多](../email/message-tracking.md)

* **設定URL追蹤引數** — 在表面層級設定追蹤引數，以自動將行銷活動識別碼（utm_campaign、utm_source等）附加至所有電子郵件連結。 這可讓您在整個數位生態系統中進行歸因追蹤。 [了解更多](../email/url-tracking.md)

* **追蹤已儲存片段中的連結** — 當您從已啟用追蹤的內容儲存片段時，當您在其他歷程或行銷活動中重複使用片段時，該片段中的連結仍會受到追蹤。 [了解更多](../content-management/save-fragments.md)

* **新增映象頁面追蹤** — 啟用映象頁面選項，以建立您電子郵件的網頁版本，並自動追蹤檢視者。 [了解更多](../email/message-tracking.md#mirror-page)

**監視效能：**&#x200B;檢視行銷活動和歷程報告中的即時量度，包括開啟、點按和連結層級的效能。 [行銷活動報告](../reports/campaign-global-report-cja-email.md) | [歷程報告](../reports/journey-global-report-cja-email.md)

+++

+++網路追蹤

網路追蹤需要明確的設定，以追蹤使用者與您的網路修改內容的互動。

**設定點選追蹤：**

製作網頁時，您可以選取要追蹤的特定元素（按鈕、影像、連結）。 如此可啟用這些元素的點選追蹤，而不需要其他程式碼。 [了解更多](../web/monitor-web-experiences.md)

* **追蹤任何可點按的元素** — 選取您網頁個人化中的按鈕、影像、連結或任何互動元素。
* **自動資料收集** — 設定後，Journey Optimizer會自動擷取點選事件並將其與設定檔建立關聯。
* **即時監視** — 在使用者互動驗證個人化有效性時追蹤使用者互動。

**檢視追蹤資料：**&#x200B;存取報表中的顯示量度、點進率及元素層級效能。 [行銷活動報告](../reports/campaign-global-report-cja-web.md) | [歷程報告](../reports/journey-global-report-cja-web.md)

+++

+++推播通知追蹤

推播追蹤會自動啟用，並擷取曝光數（已傳送）、點選次數（已點選）和開啟次數（已啟動應用程式）。 若要最大化追蹤值，請在推播內容中設定可點按的元素。

**設定追蹤的元素：**

* **內文點按行為** — 設定使用者點選通知時會發生什麼情況：開啟應用程式、導覽至深層連結，或開啟網頁URL。 系統會自動追蹤每個動作。 [了解更多](../push/design-push.md#on-click-behavior)

* **新增動作按鈕** — 包含最多3個按鈕(Android)或多個按鈕(iOS)，每個按鈕動作（開啟應用程式、深層連結、網頁URL）都有獨立的追蹤。 [了解更多](../push/design-push.md#add-buttons-push)

* **啟用追蹤** — 確認已在您的推播歷程活動或行銷活動追蹤設定中啟用追蹤。 [了解更多](../push/create-push.md#create)

>[!NOTE]
>
>推播追蹤需要行動SDK實施。 確認應用程式已正確設定Adobe Experience Platform Mobile SDK。 [了解更多](../push/push-configuration.md#integrate-mobile-app)

**分析參與：**&#x200B;檢視報告中的點進率、按鈕效能以及追蹤的連結詳細資料。 [行銷活動報告](../reports/campaign-global-report-cja-push.md) | [歷程報告](../reports/journey-global-report-cja-push.md)

+++

+++應用程式內訊息追蹤

應用程式內訊息會自動追蹤顯示畫面和使用者互動。 設定觸發器和內容以最大化追蹤有效性。

**設定追蹤：**

* **定義顯示規則** — 使用觸發器（應用程式啟動、熒幕載入）、頻率規則和對象條件，設定應用程式內訊息出現的時間和位置。 正確設定可確保準確追蹤觸發和顯示的訊息。

* **新增追蹤的元素** — 在訊息內容中包含按鈕、連結和互動式元素。 系統會自動使用詳細標籤追蹤每個互動。

* **最佳化顯示時間** — 設定一週中的某天和一天中的某時間規則，將觸發訊息實際顯示給使用者的可能性最大化。

[瞭解如何設定應用程式內訊息](../in-app/create-in-app.md)

**追蹤的內容：** Journey Optimizer會自動擷取顯示、按鈕點按、解除、觸發與顯示的量度，以及連結效能。 [行銷活動報告](../reports/campaign-global-report-cja-inapp.md) | [歷程報告](../reports/journey-global-report-cja-inapp.md)

+++

+++簡訊與多媒體簡訊追蹤

SMS追蹤只需要最少的設定 — Journey Optimizer會自動縮短並追蹤您包含在訊息中的連結。

**運作方式：**

* **自動連結追蹤** — 使用URL協助程式函式，將任何URL新增至您的SMS內容。 Journey Optimizer會自動縮短連結，並追蹤點按，不需要額外設定。 若要縮短URL長度，您必須先設定SMS子網域。 [了解更多](../sms/sms-subdomains.md)

* **傳入郵件追蹤** — 會自動擷取收件者的回覆，讓您監視雙向交談和回應模式。 [了解更多](../sms/sms-opt-out.md#sms-native-keywords)

**檢視量度：**&#x200B;存取連結點選資料、傳入訊息磁碟區以及報表中的訊息型別效能。 [行銷活動報告](../reports/campaign-global-report-cja-sms.md) | [歷程報告](../reports/journey-global-report-cja-sms.md)

+++

+++程式碼型體驗追蹤

程式碼型體驗需要實作設定，才能將追蹤資料傳送至Adobe Experience Platform。

**必要條件：**

在追蹤運作之前，您需要設定實施以傳送互動事件（顯示、點按）至Adobe Experience Platform。 此設定需要：

* 設定為Adobe Experience Platform設定的資料串流。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant)
* 使用Web SDK或Mobile SDK在程式碼中實作事件集合。
* 顯示或點選內容時傳送顯示和互動事件。

[進一步瞭解實作必要條件](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**追蹤的內容：**&#x200B;實作後，追蹤任何數位接觸點（網站、行動應用程式、IoT裝置等）的顯示、點按、點進率及元素層級效能。 [行銷活動報告](../reports/campaign-global-report-cja-code.md) | [歷程報告](../reports/journey-global-report-cja-code.md)

+++

+++內容卡追蹤

內容卡會自動追蹤使用者互動。 設定內容和顯示規則以控制追蹤行為。

**如何實作：**

* **設計追蹤的內容** — 新增按鈕和連結至您的內容卡。 系統會自動使用標籤和URL追蹤每個互動式元素。

* **設定持續性** — 內容卡會跨應用程式工作階段持續存在，可讓您追蹤長期參與模式。 設定到期規則，以控制卡片可追蹤的時長。

* **設定顯示規則** — 定義卡片出現的時間和位置，以確保顯示和互動的追蹤準確無誤。

[瞭解如何設定內容卡](../content-card/create-content-card.md)

**監視參與：**&#x200B;追蹤多個工作階段的顯示、點按、點進率及參與模式。 [行銷活動報告](../reports/campaign-global-report-cja-content.md) | [歷程報告](../reports/journey-global-report-cja-content.md)

+++

+++登陸頁面追蹤

登陸頁面隨附不需要額外設定的內建追蹤功能。 Journey Optimizer會自動擷取造訪、轉換和跳出率。

**自動追蹤的內容：**

* **次造訪** — 測量觸及範圍的造訪總數和不重複
* **轉換** — 表單提交、訂閱確認或其他已定義的動作
* **跳出率** — 未互動的訪客百分比
* **效能趨勢** — 顯示量度如何演化的時間序列資料

[瞭解如何設定登入頁面](../landing-pages/create-lp.md)

**監視效能：**&#x200B;追蹤一段時間內的造訪模式、轉換率和跳出率，以瞭解使用者如何與您的表格互動，並找出需要改善的領域。 [行銷活動報告](../reports/lp-report-global-cja.md)

+++

## 追蹤您的歷程與行銷活動活動 {#journey-campaign-tracking}

除了管道層級追蹤，設定追蹤來測量整體效能並瞭解行銷方案的客戶行為。

* **定義自訂成功量度** — 設定符合您業務目標（購買、報名、續約等）的特定KPI，超出標準參與量度。 [了解更多](../building-journeys/success-metrics.md)

* **啟用歷程步驟事件** — 啟用詳細追蹤客戶在歷程中採取的每個動作。 如此一來，入口/出口點、路徑選取和出口位置都可清楚顯示。 [了解更多](../reports/journey-step-events-overview.md)

* **設定排程** — 設定傳送時間最佳化，以追蹤不同計時策略的效能，並識別最佳傳送期間。 [了解更多](../building-journeys/send-time-optimization.md)

* **設定自訂動作監視** — 設定與外部系統整合的追蹤，以監視API呼叫、回應時間和錯誤模式。 [了解更多](../action/reporting.md)

* **建立自訂報告並匯出資料** — 建立量身打造的報告並匯出追蹤資料至外部系統，以進行更深入的分析。 [了解更多](../reports/sharing-overview.md)

* **檢視統一的效能：**&#x200B;存取行銷活動和歷程的完整報告，以比較電子郵件、推播、簡訊和其他管道的效能，並瞭解哪些組合可帶來最佳結果。 [行銷活動報告](../reports/campaign-global-report-cja.md) | [歷程報告](../reports/journey-global-report-cja.md)

## 追蹤最佳化和決策效能 {#optimization-decisioning-tracking}

Journey Optimizer會自動追蹤最佳化實驗、目標定位策略和決策效能。 設定您的設定以確保資料收集正確。

### 設定最佳化追蹤 {#optimization-tracking}

* **在您的行銷活動和歷程中最佳化**：

   * 建立實驗時，定義要追蹤的量度（轉換、點按、自訂事件）。 Journey Optimizer會自動收集每個處理的效能資料。 [了解更多](../content-management/optimization-experimentation.md)

   * 建立鎖定目標規則，將不同內容傳送至不同的受眾區段。 Journey Optimizer會自動追蹤每個目標群組的參與量度，讓您比較不同區段的效能。 [了解更多](../content-management/optimization-targeting.md)

* **歷程路徑最佳化**：新增&#x200B;**最佳化**&#x200B;活動至您的歷程並設定多個路徑。 Journey Optimizer會自動追蹤設定檔採取哪些路徑並測量效能。 [了解更多](../building-journeys/optimize.md)

若要分析結果：在實驗報告中檢視轉換率、統計顯著性和治療之間的提升度，或比較目標區段之間的參與量度。 [實驗行銷活動報告](../reports/campaign-global-report-cja-experimentation.md) | [實驗歷程報告](../reports/journey-global-report-cja-experimentation.md) | [歷程目標定位報告](../reports/journey-global-report-cja.md#targeting)

### 追蹤決策效能 {#decisioning-tracking}

使用決策來個人化內容時，Journey Optimizer會自動追蹤決策事件、曝光次數和點按次數，而不需要其他設定。

* **自動事件擷取** — 每當為設定檔選取決策專案時，Journey Optimizer就會自動擷取決策事件。
* **閱聽追蹤** — 對於電子郵件，閱聽會被自動追蹤。 針對程式碼型體驗，您必須在程式碼中實作主張顯示事件。 [了解更多](../code-based/code-based-implementation-samples.md#client-side-how)
* **點選追蹤** — 決策專案的點選會在電子郵件中自動追蹤；程式碼型體驗需要實作點選事件。

>[!NOTE]
>
>若要在&#x200B;**程式碼型體驗**&#x200B;中追蹤決策，請確保您的實作使用Web SDK或Mobile SDK將主張互動事件（顯示和點按）傳送至Adobe Experience Platform。 [了解更多](../experience-decisioning/data-collection/schema-requirement.md)

監控效能：檢視決策KPI、比較決策專案、分析選擇策略，以及在報表中監控AI模型效能。 [了解更多](../experience-decisioning/cja-reporting.md)

## 控制追蹤資料的使用情況 {#data-governance}

資料治理原則可讓您控制如何在您的組織中使用追蹤資料：

* **標籤敏感追蹤資料** — 套用治理標籤至追蹤的行為資料（例如，健康內容上的點按、金融產品互動），以將其標示為敏感或受管制。

* **限制資料使用** — 建立原則，防止標籤追蹤資料用於特定管道、匯出至協力廠商系統，或用於特定個人化案例。

* **自動強制執行** — 當您建立歷程與行銷活動時，Journey Optimizer會自動檢查治理原則，如果追蹤的資料正在違反定義的原則下使用，則會封鎖發佈。

資料控管可確保遵守GDPR和CCPA等法規，同時仍可讓您追蹤和分析在核准邊界內的客戶行為。 [了解更多](../action/action-privacy.md)

## 監視傳遞能力與系統健康狀況 {#monitoring-capabilities}

除了追蹤參與以外，請設定監控以確保訊息可到達收件匣且系統以最佳方式執行。

傳遞能力監視透過追蹤關鍵指標，幫助確保您的訊息到達收件者的收件匣，並維持健康的寄件者信譽：

* **請定期檢閱隱藏清單**，瞭解位址為何遭到封鎖，並維護清單衛生。 [了解更多](../reports/suppression-list.md)

* **分析傳遞錯誤**&#x200B;以診斷失敗並採取更正動作。 [了解更多](../configuration/email-error-types.md)

* **遵循DMARC、SPF和DKIM的最佳實務**，以最大化收件匣位置。 [了解更多](../reports/deliverability.md)

設定主動式監控，接收重大事件和系統問題的即時通知，讓您在影響客戶體驗之前快速回應：

* **設定警示** — 設定歷程錯誤、自訂動作失敗和嚴重問題的即時通知，以快速回應問題。 [了解更多](../reports/alerts.md)

* **啟用稽核記錄** — 啟用稽核記錄以追蹤資源上的所有動作，以符合法規及疑難排解。 [了解更多](../privacy/audit-logs.md)

* **監視整合** — 追蹤自訂動作效能和外部系統連線，以及早識別整合問題。 [了解更多](../action/reporting.md)

