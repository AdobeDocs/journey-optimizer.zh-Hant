---
solution: Journey Optimizer
product: journey optimizer
title: 歷程全域報告
description: 瞭解如何使用歷程全域報告中的資料
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 5671f510d8be80b53d57b1ff90a101e500773243
workflow-type: tm+mt
source-wordcount: '4368'
ht-degree: 11%

---

# 歷程全域報告 {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="歷程全域報告"
>abstract="歷程全域報告可讓您測量您的歷程在選取時段內的影響。您的報告會分為不同的介面工具，詳細說明您的歷程的成功和錯誤。每個報告儀表板都可以透過調整大小或移除介面工具來修改。"

全域報告可從「所有時間」標籤存取，它會顯示至少兩小時前發生的事件，以及所選時段內的封面事件。 相較之下，即時報表著重於過去24小時內發生的事件，最短間隔為事件發生後的2分鐘。

歷程全域報告可透過以下直接從您的歷程存取： **[!UICONTROL 檢視報告]** 按鈕。

![](assets/report_journey.png)

歷程 **[!UICONTROL 全域報告]** 頁面會顯示以下索引標籤：

* [歷程](#journey-global)
* [電子郵件](#email-global)
* [推播](#push-global)
* [簡訊](#sms-global)
* [應用程式內](#in-app-global)

歷程 **[!UICONTROL 全域報告]** 會分成不同的Widget，詳述您歷程的成功和錯誤。 如有需要，可以調整每個Widget的大小並將其刪除。 如需詳細資訊，請參閱此 [區段](global-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [此頁面](global-report.md#list-of-components-global).

## 歷程索引標籤 {#journey-global}

從您的歷程 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 歷程]** 標籤可讓您清楚檢視歷程最重要的追蹤資料。

### 歷程績效 {#journey-perfomance}

>[!CONTEXTUALHELP]
>id="ajo_journey_performance"
>title="歷程績效"
>abstract="歷程績效Widget可讓您在目標設定檔進行歷程時，以視覺化方式追蹤其路徑。"

![](assets/journey_performance.png)

此 **[!UICONTROL 歷程績效]** widget可讓您在目標設定檔導覽您的歷程時，以視覺化方式追蹤其軌跡。

### 歷程統計資料 {#journey-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_statistics"
>title="歷程統計資料"
>abstract="歷程統計關鍵績效指標(KPI)是功能完整的儀表板，提供與您的歷程相關之基本量度的深入分析。"

![](assets/journey_statistics.png)

此 **[!UICONTROL 歷程統計資料]** 關鍵績效指標(KPI)作為全方位的控制面板，提供與您的歷程相關聯的基本量度分析。 這包含已輸入設定檔計數和失敗個別歷程例項等詳細資訊，提供歷程成效和參與層級的全面深入分析。

+++ 進一步瞭解歷程統計量度

* **[!UICONTROL 輸入的設定檔]**：到達歷程進入事件的個人總數。

* **[!UICONTROL 已退出的設定檔]**：已退出歷程的個人總數。

* **[!UICONTROL 失敗的個人歷程]**：未成功執行的個別歷程總數。

+++

### 動作績效 {#action-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_performance"
>title="動作績效"
>abstract="動作效能Widget會說明在起始動作時最成功的動作。"

![](assets/journey_action_performance.png)

此 **[!UICONTROL 動作績效]** Widget代表當您執行 **[!UICONTROL 動作]** 已觸發。

### 熱門動作 {#top-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_actions"
>title="熱門動作"
>abstract="「排名在前的動作」表格可整合有關動作的重要資訊，並提供每個動作的頻率和效能的精簡觀察。"

![](assets/journey_top_actions.png)

此 **[!UICONTROL 熱門動作]** 表格會編譯您電腦上的基本資料 **[!UICONTROL 動作]**. 它提供每個動作頻率和效能的簡單深入分析。

+++ 深入了解熱門動作量度

* **[!UICONTROL 動作已成功執行]**：總數 **[!UICONTROL 動作]** 已成功為歷程執行。

* **[!UICONTROL 動作中的錯誤]**：已發生的錯誤總數 **[!UICONTROL 動作]**.

+++

### 動作錯誤原因 {#action-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_actions_error_reasons"
>title="動作錯誤原因"
>abstract="「動作」錯誤原因表格和圖表提供執行動作期間所遭遇錯誤的完整摘要，以及可能已發生問題的全面概觀。"

![](assets/journey_action_error.png)

此 **[!UICONTROL 動作錯誤原因]** 表格和圖表提供執行期間發生錯誤的全面概觀 **[!UICONTROL 動作]**.

### 依據來源的事件 {#events-origin}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_origin"
>title="依據來源的事件"
>abstract="「依來源的事件」表格和圖形可提供成功接收事件的檢視。 這些視覺呈現方式可讓您精確識別有效接收的事件，針對歷程中每個事件的效能和影響提供有價值的深入分析。"

![](assets/journey_events_origin.png)

此 **[!UICONTROL 依據來源的事件]** 表格和圖表可讓您從詳細角度瞭解成功接收您的 **[!UICONTROL 事件]**. 透過這些視覺化表示法，您可以精確地辨識 **[!UICONTROL 事件]** 獲得有效接收，針對歷程中個別事件的效能和影響提供寶貴見解。

### 依事件收到的事件 {#events-received}

>[!CONTEXTUALHELP]
>id="ajo_journey_events_received"
>title="依事件收到的事件"
>abstract="「依事件收到的事件」圖表可讓您識別和分析歷程中有效執行的特定事件，針對個別事件的效能和成功率提供有價值的深入分析。"

![](assets/journey_event_received.png)

此 **[!UICONTROL 依事件收到的事件]** 圖表可讓您識別及分析哪些特定的 **[!UICONTROL 事件]** 在您的歷程中有效地執行，提供個別事件效能和成功率的寶貴見解。

### 熱門事件 {#top-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_top_events"
>title="熱門事件"
>abstract="「常用事件」表格可整合事件的基本資料，並提供每個個別事件頻率和效能的精簡觀察資料。"

![](assets/journey_top_events.png)

此 **[!UICONTROL 熱門事件]** 表格會編譯您電腦上的基本資料 **[!UICONTROL 活動]**. 它提供每個專案的頻率和效能的簡單深入分析 **[!UICONTROL 事件]**.

### 同意原則 {#consent-policies}

>[!CONTEXTUALHELP]
>id="ajo_journey_consent_policies"
>title="同意原則"
>abstract="「同意原則」表格和圖形會顯示在自訂動作中，從每個原則排除的設定檔數量。 此簡報提供對各個同意原則對設定檔排除之影響的清晰分析。"

![](assets/journey_consent.png)

此 **[!UICONTROL 同意原則]** 表格和圖表會顯示在自訂動作中從每個原則排除的設定檔數量。 這可提供每個同意原則對設定檔排除之影響的明確見解。

如需自訂動作的詳細資訊，請參閱 [詳細檔案](../action/about-custom-action-configuration.md).

請注意，若要讓這些Widget出現在您的歷程報告中，您需要重設儀表板。 若要這麼做，請按一下 **[!UICONTROL 修改]** 則 **[!UICONTROL 重設]** 在報表頂端。

## 電子郵件標籤 {#email-global}

從您的歷程 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 電子郵件]** 索引標籤會詳細說明歷程中傳送之電子郵件相關的主要資訊。

### 電子郵件 — 傳送統計資料 {#email-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_statistics"
>title="電子郵件 — 傳送統計資料"
>abstract="「電子郵件 - 發送統計資料」表格總結你的電子郵件的基本資料，例如「指定對象」或「已送達」。"

![](assets/journey_email_statistics.png)

此 **[!UICONTROL 電子郵件傳送統計資料]** 表格提供有關您歷程中電子郵件之基本資料的完整摘要。 它會詳細說明關鍵量度，例如目標對象的大小和成功傳送的電子郵件數量，提供對電子郵件和歷程的成效和觸及範圍的寶貴見解。

+++ 進一步瞭解電子郵件傳送統計量度

* **[!UICONTROL 執行時間]**：如果為週期性歷程，則為每次歷程執行的開始時間。 若要只鎖定一或多個遞回，請從 **[!UICONTROL 執行時間]** 下拉式清單。

* **[!UICONTROL 已鎖定目標]**：任何動作（例如傳送電子郵件或簡訊）的目標設定檔數。

* **[!UICONTROL 已傳送]**：為歷程傳送的電子郵件總數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數，與已傳送電子郵件總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的電子郵件百分比。

* **[!UICONTROL 跳出數]**：與已傳送電子郵件總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 跳出率]**：與已傳送電子郵件相比跳出的電子郵件百分比。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的電子郵件相比，在傳送過程中發生而無法傳送的錯誤百分比。

* **[!UICONTROL 重試]**：重試佇列中的電子郵件數。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的設定檔數。

+++

### 電子郵件 - 追蹤統計資料 {#email-tracking}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_tracking_statistics"
>title="電子郵件 - 追蹤統計資料"
>abstract="「電子郵件 - 追蹤統計資料」表格提供你的電子郵件設定檔活動的資料。"

![](assets/journey_email_tracking.png)

此 **[!UICONTROL 電子郵件 — 追蹤統計資料]** 表格提供與歷程中所包含電子郵件相關的設定檔活動的詳細帳戶。 其中包括開啟次數、點按次數和其他相關的參與指標，以提供設定檔與電子郵件內容互動方式的完整檢視。

+++ 進一步瞭解電子郵件 — 追蹤統計量度

* **[!UICONTROL 執行時間]**：歷程中每次執行週期性電子郵件的開始時間。 若要只鎖定一或多個週期性電子郵件，請從 **[!UICONTROL 執行時間]** 下拉式清單。

* **[!UICONTROL 開啟次數]**：您的電子郵件在歷程中開啟的次數。

* **[!UICONTROL 不重複開啟次數]**：已開啟電子郵件的百分比。

* **[!UICONTROL 不重複開啟率]**：與已傳遞電子郵件數量相比較的已開啟電子郵件總數。

* **[!UICONTROL 點按次數]**：內容在您的電子郵件中被點按的次數。

* **[!UICONTROL 不重複點按]**：點按您電子郵件中內容的收件者人數。

* **[!UICONTROL 點進率]**：與歷程互動的使用者百分比。

* **[!UICONTROL 取消訂閱]**：對取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾郵件投訴數]**：您的電子郵件被宣告為垃圾郵件或垃圾郵件的次數。

+++

### 電子郵件 - 傳送效能 {#email-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sending_performance"
>title="電子郵件 - 傳送效能"
>abstract="電子郵件 — 傳送績效圖表顯示有關已傳送電子郵件的全面資料，提供關鍵量度（例如傳送和跳出）的深入分析，允許電子郵件傳送過程的詳細分析。"

![](assets/journey_email_performance.png)

此 **[!UICONTROL 電子郵件 — 傳送績效]** graph提供與您歷程中傳送之電子郵件相關的完整資料檢視，提供關鍵量度的深入分析，例如傳送和跳出。 這可啟用電子郵件傳送流程的詳細分析，提供關於歷程效率和效能的寶貴資訊。

+++ 進一步瞭解電子郵件 — 傳送績效量度

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數，與已傳送電子郵件總數相關。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 重試]**：重試佇列中的電子郵件數。

* **[!UICONTROL 錯誤]**：傳送程式期間發生且無法傳送至設定檔的錯誤總數。

+++

### 電子郵件 — 退回類別和原因 {#email-bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces"
>title="電子郵件 — 退回類別和原因"
>abstract="電子郵件 — 跳出類別和原因Widget會彙總有關跳出訊息的資料，針對造成電子郵件跳出的特定原因和類別提供深入分析"

![](assets/journey_email_bounce_categories.png)

此 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 退信類別]** Widget會編譯與退回訊息相關的可用資料，提供電子郵件退回背後的特定原因和類別的詳細深入分析。

有關退信的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 頁面。

+++ 進一步瞭解電子郵件 — 退回類別量度

* **[!UICONTROL 硬退信]**：永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。

* **[!UICONTROL 軟退信]**：暫時性錯誤的總數，例如完整的收件匣。

* **[!UICONTROL 已忽略]**：暫時性總數，例如「不在辦公室」或技術錯誤，例如，如果傳送者型別是郵遞員。

+++

### 電子郵件 - 錯誤原因 {#email-errors}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_error_reasons"
>title="電子郵件 - 錯誤原因"
>abstract="「電子郵件 - 錯誤原因」圖表和表格讓你能夠識別傳送過程中發生的特定錯誤。"

![](assets/journey_email_error.png)

此 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視傳送過程中發生的特定錯誤，提供有關錯誤性質和發生次數的寶貴資訊。

### 電子郵件 - 排除原因 {#email-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_excluded_reasons"
>title="電子郵件 - 排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

![](assets/journey_email_excluded.png)

此 **[!UICONTROL 排除的原因]** 圖表和表格可全面檢視導致從目標對象中排除使用者設定檔，從而導致未收到訊息的不同因素。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 依網域劃分的已傳送和已送達郵件 {#sent-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_sent_delivered_domains"
>title="依網域劃分的已傳送和已送達郵件"
>abstract="「依網域傳送和傳遞」表格和圖表提供依網域分類的電子郵件劃分，呈現對電子郵件通訊整體績效的深入分析。"

![](assets/journey_email_sent_domains.png)

此 **[!UICONTROL 依網域傳送和傳遞]** 表格和圖表提供網域層級的電子郵件詳細劃分，提供電子郵件效能的完整深入分析。

+++ 進一步瞭解依網域進行之傳送和傳遞的量度

* **[!UICONTROL 已傳送]**：您的電子郵件傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數，與已傳送電子郵件總數相關。

+++

### 依網域劃分的開啟和點選動作 {#open-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_open_clicks_domains"
>title="依網域劃分的開啟和點選動作"
>abstract="「依網域區分的開啟與點按」圖表和表格提供網域層級的詳細劃分，呈現受眾如何與您的電子郵件互動的完整檢視。"

![](assets/journey_email_open_domains.png)

此 **[!UICONTROL 依網域開啟和點按]** 圖形和表格會顯示設定檔與電子郵件互動的網域層級劃分，提供不同網域與內容互動方式的寶貴見解。

+++ 進一步瞭解依網域量度的開啟和點按次數

* **[!UICONTROL 開啟次數]**：電子郵件開啟的次數。

* **[!UICONTROL 點按次數]**：內容在電子郵件中的點按次數。

+++

### 依網域劃分的退回情形與錯誤 {#bounces-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_errors_domains"
>title="依網域劃分的退回情形與錯誤"
>abstract="「依網域區分的跳出和錯誤」圖表和表格提供網域層級的詳細劃分，深入分析電子郵件傳送過程中所遇到的特定錯誤。"

![](assets/journey_email_bounce_domains.png)

此 **[!UICONTROL 依網域區分的退回和錯誤]** 圖表和表格提供傳送程式期間所遇到特定錯誤的網域層級劃分，針對所發生的問題提供詳細分析。

+++ 進一步瞭解依網域量度的跳出和錯誤

* **[!UICONTROL 跳出數]**：與已傳送電子郵件總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

+++

### 依網域劃分的退回原因 {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_bounces_reasons_domains"
>title="依網域列出的退回原因"
>abstract="「依網域區分的跳出原因」圖表和表格提供網域層級的劃分，提供暫時和永久錯誤的全面深入分析。 這項詳細分析可為您提供退回訊息背後特定原因的重要資訊。"

![](assets/journey_email_bounce_reasons_domain.png)

此 **[!UICONTROL 依網域區分的退回原因]** 圖表和表格提供有關暫時和永久錯誤的網域層級資料劃分，提供退回訊息背後原因的詳細深入分析。

### 電子郵件 - 熱門 URL {#email-top}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_top_url"
>title="電子郵件 - 熱門 URL"
>abstract="「電子郵件 - 熱門 URL」圖表和表格提供電子郵件中訪客流量最高的 URL 的綜合概觀，讓你能夠確認最受歡迎的連結。"

![](assets/journey_email_top.png)

此 **[!UICONTROL 電子郵件 — 熱門URL]** 圖表和表格提供電子郵件中吸引最高訪客流量之URL的完整概觀。 這可讓您識別最熱門的連結並排定其優先順序，進而更瞭解電子郵件中特定內容的設定檔參與情形。

### 電子郵件 — 最佳化 {#email-sto}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_optimization"
>title="電子郵件 — 最佳化"
>abstract="傳送時間最佳化及已最佳化與未最佳化的Widget提供關於您訊息的詳細資訊，並醒目提示訊息是否已最佳化。"

![](assets/journey_email_sto.png)

>[!NOTE]
>
>此 **[!UICONTROL 傳送時間最佳化]** 和 **[!UICONTROL 已最佳化與未最佳化]** 只有為您的傳送啟用「傳送時間最佳化」選項時，才可使用Widget。 如需傳送時間最佳化的詳細資訊，請參閱 [此頁面](../building-journeys/journeys-message.md#send-time-optimization).

此 **[!UICONTROL 傳送時間最佳化]** 和 **[!UICONTROL 已最佳化與未最佳化]** Widget會根據傳送方法（最佳化或正常），詳細描述您電子郵件的成功與否。

+++ 進一步瞭解傳送時間最佳化及已最佳化與非最佳化量度的比較

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。
* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 已傳送]**：為歷程傳送的電子郵件總數。

* **[!UICONTROL 開啟次數]**：您的電子郵件在歷程中開啟的次數。

* **[!UICONTROL 點按次數]**：內容在電子郵件中的點按次數。

+++

### 電子郵件 — 優惠方案 {#email-offers}

>[!CONTEXTUALHELP]
>id="ajo_journey_email_offers"
>title="電子郵件 — 優惠方案"
>abstract="優惠統計和優惠詳細統計Widget提供優惠效能的全面深入分析，提供一段時間影響的詳細分析，並提供詳細統計資料，以便更深入地瞭解。"

>[!NOTE]
>
>優惠方案Widget和量度僅在決定已插入電子郵件中時才能使用。 有關決定管理的詳細資訊，請參閱此 [頁面](../offers/get-started/starting-offer-decisioning.md).

此 **[!UICONTROL 優惠統計資料]** 和 **[!UICONTROL 優惠詳細統計資料]** 一段時間後，Widget會衡量您選件的成功及對目標對象的影響。 它會使用KPI詳細說明與您的訊息相關的主要資訊。

+++ 進一步瞭解電子郵件 — 優惠方案量度

* **[!UICONTROL 已傳送的優惠]**：選件的傳送總數。

* **[!UICONTROL 優惠印象]**：在您的電子郵件中開啟選件的次數。

* **[!UICONTROL 優惠點選次數]**：在您的電子郵件中點按優惠的次數。

* **[!UICONTROL 位置名稱]**：用來顯示優惠方案的位置名稱。 如需位置的詳細資訊，請參閱此 [頁面](../offers/offer-library/creating-placements.md).

* **[!UICONTROL 選件名稱]**：在您的電子郵件中新增的優惠方案名稱。 如需位置的詳細資訊，請參閱此 [頁面](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL 已傳送的優惠]**：選件的傳送總數。

* **[!UICONTROL 優惠曝光率]**：已開啟選件相對於已傳送選件數量的百分比。

* **[!UICONTROL 優惠點按率]**：與選件互動的使用者百分比。

+++

## 推播通知標籤 {#push-global}

從您的歷程 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 推播通知]** 索引標籤會詳細說明歷程中傳送之推播通知的相關主要資訊。

### 推播通知 - 傳送統計資料 {#push-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_statistics"
>title="推播通知 - 傳送統計資料"
>abstract="「推播通知傳送統計資料」表格總結有關推播通知的基本資料，例如指定對象或已送達的訊息。"

![](assets/journey_push_sending.png)

此 **[!UICONTROL 推播通知 — 傳送統計資料]** 此表格提供與推播通知相關之基本資料的簡要摘要，包括關鍵量度，例如目標訊息數目以及成功傳送的訊息數目。

+++ 進一步瞭解推播通知 — 傳送統計量度

* **[!UICONTROL 執行時間]**：如果為週期性歷程，則為每次歷程執行的開始時間。 若要只鎖定一或多個遞回，請從 **[!UICONTROL 執行時間]** 下拉式清單。

* **[!UICONTROL 已鎖定目標]**：任何動作（例如傳送電子郵件或簡訊）的目標設定檔數。

* **[!UICONTROL 已傳送]**：已傳送的推播通知總數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數，與已傳送推播通知總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的推播通知百分比。

* **[!UICONTROL 跳出數]**：與已傳送推播通知總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 跳出率]**：與已傳送的推播通知相比退回的推播通知百分比。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與推播通知傳送相比，在傳送過程中發生而無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的設定檔數。

+++

### 推播通知 - 追蹤統計資料 {#push-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_tracking_statistics"
>title="推播通知 - 追蹤統計資料"
>abstract="「推播追蹤統計資料」提供有關推播通知的設定檔活動的資料。"

此 **[!UICONTROL 推播 — 追蹤統計資料]** widget提供與您的推播通知相連結的個人資料活動的詳細快照，提供參與和推播通知有效性的基本深入分析。

+++ 進一步瞭解推播通知 — 追蹤統計量度

* **[!UICONTROL 執行時間]**：如果為週期性歷程，則為每次歷程執行的開始時間。 若要只鎖定一或多個遞回，請從 **[!UICONTROL 執行時間]** 下拉式清單。

* **[!UICONTROL 開啟次數]**：您的推播通知在歷程中開啟的次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

+++

### 推播通知 - 傳送摘要 {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_sending_summary"
>title="推播通知 - 傳送摘要"
>abstract="「推播通知傳送摘要」圖表顯示已傳送的推播通知的可用資料。"

![](assets/journey_push_summary.png)

此 **[!UICONTROL 推播通知 — 傳送摘要]** 圖表提供動態表示，顯示推播通知活動的分析。 此圖形表示提供已傳送推播通知的完整劃分。

+++ 進一步瞭解推播通知 — 傳送摘要量度

* **[!UICONTROL 開啟次數]**：您的推播通知在歷程中開啟的次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 跳出數]**：與已傳送推播通知總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數，與已傳送推播通知總數相關。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

+++

### 推播通知 - 錯誤原因 {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_error_reasons"
>title="推播通知 - 錯誤原因"
>abstract="「錯誤原因」圖表和表格可讓您識別在傳送過程中發生的特定錯誤"

![](assets/journey_push_error.png)

此 **[!UICONTROL 錯誤原因]** 表格和圖表可讓您識別在傳送推播通知的過程中發生的特定錯誤，針對過程中遇到的任何問題提供詳細分析。

### 推播通知 - 排除原因 {#push-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_excluded_reasons"
>title="推播通知 - 排除原因"
>abstract="「排除的原因」圖表和表格說明了從目標對象排除的使用者設定檔無法接收訊息的各種因素。"

![](assets/journey_push_excluded.png)

此 **[!UICONTROL 排除的原因]** 圖表和表格會顯示從目標設定檔中排除的使用者設定檔無法接收推播通知的不同原因。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 推播通知 - 依平台劃分 {#push-breakdown}

>[!CONTEXTUALHELP]
>id="ajo_journey_push_breakdown_platform"
>title="推播通知 - 依平台劃分"
>abstract="推播通知 — 依平台劃分圖表和表格會根據設定檔的作業系統，提供推播通知成功劃分資訊。"

![](assets/journey_push_breakdown.png)

此 **[!UICONTROL 依平台劃分]** 圖表和表格提供推送通知成功的詳細分析，根據您的設定檔作業系統提供深入分析。 此劃分可讓您更瞭解推播通知在不同平台上的執行情形。

### 推播通知 — 最佳化 {#push-sto}

>[!NOTE]
>
>此 **[!UICONTROL 已最佳化與未最佳化]** 和 **[!UICONTROL 傳送時間最佳化]** 只有為您的傳送啟用「傳送時間最佳化」選項時，才可使用Widget。 如需傳送時間最佳化的詳細資訊，請參閱 [此頁面](../building-journeys/journeys-message.md#send-time-optimization).

此 **[!UICONTROL 已最佳化與未最佳化]** 和 **[!UICONTROL 傳送時間最佳化]** Widget會詳細說明與訊息相關的主要資訊，無論是否已最佳化。

+++ 進一步瞭解推播通知 — 最佳化量度

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 開啟次數]**：您的推播通知在歷程中開啟的次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

+++

## 簡訊標籤 {#sms-global}

### 簡訊 - 傳送統計資料 {#sms-sending-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_sending_statistics"
>title="簡訊 - 傳送統計資料"
>abstract="SMS — 傳送統計資料表格會摘要有關SMS訊息的基本資料，例如已鎖定或已傳送的訊息。"

![](assets/journey_sms_sending.png)

此 **[!UICONTROL 簡訊 — 傳送統計資料]** 表格提供與您的SMS訊息相關之基本資料的簡要摘要，包含關鍵量度，例如目標訊息數目和成功傳送訊息的計數。

+++ 進一步瞭解簡訊 — 傳送統計量度

* **[!UICONTROL 執行時間]**：如果為週期性歷程，則為每次歷程執行的開始時間。 若要只鎖定一或多個遞回，請從 **[!UICONTROL 執行時間]** 下拉式清單。

* **[!UICONTROL 已鎖定目標]**：符合簡訊訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已排除]**：未接收SMS訊息的目標設定檔中排除的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：為歷程傳送的SMS訊息總數。

* **[!UICONTROL 跳出數]**：與已傳送SMS訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

+++

### 簡訊 — 追蹤統計資料 {#sms-tracking-stat}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_tracking_statistics"
>title="簡訊 — 追蹤統計資料"
>abstract="SMS — 追蹤統計Widget提供與訪客與您URL互動相關之基本資訊的完整概觀。"

![](assets/journey_sms_tracking.png)

此 **[!UICONTROL 簡訊 — 追蹤統計資料]** Widget提供與訪客與您URL互動相關之關鍵資訊的詳細概觀，提供您SMS訊息有效性的深入分析。

* **[!UICONTROL 執行時間]**：您每次執行週期性SMS的開始時間。 若要只定位一或多個循環的SMS，請從 **[!UICONTROL 執行時間]** 下拉式清單。

* **[!UICONTROL 點按次數]**：內容在簡訊訊息中的點按次數。

### 簡訊 - 依日期劃分的效能 {#sms-performance-date}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_perfomance_date"
>title="簡訊 - 依日期劃分的效能"
>abstract="SMS — 按日期效能Widget可透過圖形化呈現方式提供有關訊息的重要資訊。"

![](assets/journey_sms_performance.png)

此 **[!UICONTROL 簡訊 — 依據日期的績效]** widget提供與訊息相關之關鍵資訊的詳細概觀，透過圖表呈現，提供特定時段內績效趨勢的深入分析。

+++ 進一步瞭解簡訊 — 依據日期量度的績效

* **[!UICONTROL 已傳送]**：為歷程傳送的SMS訊息總數

* **[!UICONTROL 跳出數]**：與已傳送SMS訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

+++

### 簡訊 - 退回原因 {#sms-bounce}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_bounces_reasons"
>title="簡訊 - 退回原因"
>abstract="「退回原因」圖表和表格包含與退回郵件相關的可用資料。"

![](assets/journey_sms_bounce_reasons.png)

此 **[!UICONTROL 退回原因]** 圖表和表格提供與彈回SMS訊息相關的完整資料概觀，針對SMS訊息彈回例項背後的特定原因提供有價值的深入分析。

### 簡訊 - 錯誤原因 {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_error_reasons"
>title="簡訊 - 錯誤原因"
>abstract="「簡訊 - 錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

![](assets/journey_sms_error.png)

此 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您識別SMS訊息傳送過程中發生的特定錯誤，促進對所遇到的任何問題進行徹底分析。

### 簡訊 - 排除原因 {#sms-excluded}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_excluded_reasons"
>title="簡訊 - 排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

![](assets/journey_sms_excluded.png)

此 **[!UICONTROL 排除的原因]** 圖表和表格會以視覺化方式呈現導致目標對象中排除使用者設定檔的各種因素，以防止他們接收您的SMS訊息。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 簡訊 - 點選次數依連結劃分 {#sms-clicks}

>[!CONTEXTUALHELP]
>id="ajo_journey_sms_clicks"
>title="簡訊 - 點選次數依連結劃分"
>abstract="SMS — 連結點按次數Widget提供訪客與訊息中URL互動的基本深入分析。"

![](assets/journey_sms_clicks.png)

此 **[!UICONTROL 簡訊 — 依據連結的點按]** Widget提供訪客與訊息中URL互動的基本深入分析，提供關於哪些連結吸引最多互動的寶貴資訊。

## 應用程式內標籤 {#in-app-global}

從您的歷程 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 應用程式內]** 索引標籤會詳細說明歷程中傳送之應用程式內訊息的相關主要資訊。

### 應用程式內效能 {#inapp-performance}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_performance"
>title="應用程式內效能"
>abstract="應用程式內效能 KPI 提供有關訪客參與應用程式內訊息的重要深入分析。"

![](assets/journey_inapp_performance.png)

此 **[!UICONTROL 應用程式內績效]** KPI可讓您深入瞭解設定檔與應用程式內訊息的互動情形，提供基本量度，以評估歷程中包含的應用程式內訊息效能和影響。

+++ 深入瞭解應用程式內 — 依據日期量度的績效

* **[!UICONTROL 不重複曝光次數]**：顯示應用程式內訊息的不重複使用者人數。

* **[!UICONTROL 曝光數]**：向所有使用者顯示的應用程式內訊息總數。

  >[!NOTE]
  >
  >為確保計算曝光次數，使用者必須符合兩個條件：
  >* 應用程式內體驗中的資格，可透過存取其歷程中的特定應用程式內活動來達成。
  >* 符合觸發程式規則中指定的條件。
  > 
  >由於第二個標準，目標設定檔數量與不重複曝光數量之間可能會有顯著差異。

* **[!UICONTROL 互動]**：應用程式內訊息的參與次數。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。
+++

### 應用程式內摘要 {#inapp-summary}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_summary"
>title="應用程式內摘要"
>abstract="應用程式內摘要圖表顯示指定時間內應用程式內曝光與互動的進展。"

![](assets/journey_inapp_summary.png)

此 **[!UICONTROL 應用程式內摘要]** 圖表會說明應用程式內曝光次數和互動在指定期間內的進度，提供應用程式內訊息效能的完整概覽。

### 依類型劃分的互動 {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_journey_inapp_interactions"
>title="依類型劃分的互動"
>abstract="「依類型劃分的互動」圖表和表格透過追蹤任何點選、關閉或互動，詳細說明使用者如何與應用程式內訊息互動。"

![](assets/journey_inapp_interactions.png)

此 **[!UICONTROL 依型別的互動]** 圖表和表格詳細說明設定檔如何與您的應用程式內訊息、追蹤動作（例如點選、解僱或任何其他形式的參與）互動。
