---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動即時報告
description: 瞭解如何使用Campaign即時報告的資料
feature: Reporting, Campaigns
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 5671f510d8be80b53d57b1ff90a101e500773243
workflow-type: tm+mt
source-wordcount: '3484'
ht-degree: 27%

---

# 行銷活動即時報告 {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="行銷活動即時報告"
>abstract="行銷活動即時報告可讓您僅在過去 24 小時內對行銷活動的影響和效能進行即時測量和視覺化。您的報表會分為不同的介面工具，詳述促銷活動的成功和錯誤。每個報告儀表板都可以透過調整大小或移除介面工具來修改。"

從「最近24小時」索引標籤存取的即時報告，會顯示過去24小時內發生的事件，從事件發生起的最短時間間隔為兩分鐘。 相較之下，全域報表著重於至少兩小時前發生的事件，並涵蓋選定時段內的事件。

行銷活動即時報告可直接從您的行銷活動存取，使用 **[!UICONTROL 即時檢視]** 按鈕。

行銷活動 **[!UICONTROL 即時報告]** 頁面會顯示以下索引標籤：

* [Campaign](#campaign-live)
* [電子郵件](#email-live)
* [應用程式內](#inapp-live)
* [推播](#push-live)
* [簡訊](#sms-live)
* [Web](#web-tab)
* [直接郵件](#direct-mail-tab)

行銷活動 **[!UICONTROL 即時報告]** 分成不同的Widget，詳細說明行銷活動的成功和錯誤。 如有需要，可以調整每個Widget的大小並將其刪除。 如需詳細資訊，請參閱此 [區段](../reports/live-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [此頁面](live-report.md#list-of-components-live).

## 行銷活動標籤 {#campaign-live}

### 傳遞 {#delivery-live}

![](assets/campaign_live_statistics.png)

此 **[!UICONTROL 行銷活動的統計資料]** KPI可做為完整的儀表板，提供與行銷活動相關之過去24小時關鍵量度的詳細劃分。 這包括基本資訊，例如已傳送的設定檔數和動作，讓您透徹瞭解行銷活動的績效和參與。

+++ 進一步瞭解Campaign的統計量度

* **[!UICONTROL 對象]**：目標設定檔數目。

* **[!UICONTROL 動作已傳送]**：動作已傳送的不重複總次數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

+++

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## 電子郵件標籤 {#email-live}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 電子郵件]** 索引標籤會詳細說明與行銷活動中傳送之電子郵件相關的主要資訊。

### 電子郵件 - 傳送效能 {#email-sending-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_sending_statistics"
>title="電子郵件 - 傳送統計資料"
>abstract="「電子郵件 - 傳送統計資料」圖表總結有關你的電子郵件的基本資料，例如過去 24 小時內的指定對象或已送達的郵件。"

![](assets/campaign_email_live_sending.png)

此 **[!UICONTROL 電子郵件 — 傳送績效]** 提供過去24小時內傳送之電子郵件相關資料的完整概觀。 它提供基本量度的深入分析，例如傳送和跳出，以便詳細檢查電子郵件傳送過程。

+++ 進一步瞭解電子郵件傳送效能量度

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 重試]**：重試佇列中的電子郵件數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。
+++

### 電子郵件 - 統計資料

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_statistics"
>title="電子郵件 - 統計資料"
>abstract="「電子郵件 - 統計資料」表格提供過去 24 小時內你的電子郵件的設定檔活動資料。"

![](assets/campaign_email_live_statistics.png)

此 **[!UICONTROL 依電子郵件傳送量度]** 表格提供過去24小時資料的完整摘要。 它概述基本量度，包括目標對象人數和成功傳送電子郵件的計數。 這可提供針對電子郵件行銷活動之成效和觸及範圍的寶貴見解。

+++ 進一步瞭解電子郵件 — 統計量度

* **[!UICONTROL 執行時間]**：您週期性電子郵件每次執行的開始時間。 若要只鎖定一或多個週期性電子郵件，請從 **[!UICONTROL 執行時間]** 下拉式清單。

* **[!UICONTROL 已鎖定目標]**：傳送過程中處理的訊息總數。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

* **[!UICONTROL 點按次數]**：內容被點按的次數。

* **[!UICONTROL 取消訂閱]**：對取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾郵件投訴數]**：訊息被宣告為垃圾郵件或垃圾郵件的次數。

* **[!UICONTROL 重試]**：重試佇列中的電子郵件數。
+++

### 電子郵件 - 退回郵件的類別和原因 {#bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_categories"
>title="電子郵件 - 退回類別"
>abstract="「電子郵件 - 退回類別」圖表和表格提供有關過去 24 小時內暫時性和永久錯誤的資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_reasons"
>title="電子郵件 - 退回原因"
>abstract="「電子郵件 - 退回原因」圖表和表格包含與過去 24 小時內退回郵件相關的可用資料。"

![](assets/campaign_live_email_bounce_categories.png)

此 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 退信類別]** Widget會編譯與退信相關的過去24小時可用資料，提供電子郵件退信的特定原因和類別的詳細深入分析。

有關退信的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 頁面。

+++ 進一步瞭解電子郵件 — 退回類別和原因量度

* **[!UICONTROL 硬退信]**：永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。

* **[!UICONTROL 軟退信]**：暫時性錯誤的總數，例如完整的收件匣。

* **[!UICONTROL 已忽略]**：暫時性總數，例如「不在辦公室」或技術錯誤，例如，如果傳送者型別是郵遞員。

+++

### 電子郵件 - 依日期劃分的效能 {#email-performance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_performance_bydate"
>title="電子郵件 - 依日期劃分的效能"
>abstract="「電子郵件 - 依日期劃分的效能」圖表顯示過去 24 小時內有關已傳送電子郵件的綜合資料，提供關鍵量度例如送出和退回郵件的深入分析，進而對電子郵件傳送過程進行詳細分析。"

![](assets/campaign_email_live_performance.png)

此 **[!UICONTROL 電子郵件 — 依據日期的績效]** widget提供與訊息相關之關鍵資訊的詳細總覽，透過圖表呈現，提供過去24小時內效能趨勢的深入分析。

+++ 進一步瞭解電子郵件 — 依據日期和原因量度的績效

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

* **[!UICONTROL 點按次數]**：內容被點按的次數。

* **[!UICONTROL 取消訂閱]**：對取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾郵件投訴數]**：訊息被宣告為垃圾郵件或垃圾郵件的次數。

+++

### 錯誤原因 {#email-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_error_reasons"
>title="電子郵件 - 錯誤原因"
>abstract="「電子郵件 - 錯誤原因」圖表和表格讓你能夠確認過去 24 小時內發送過程中發生的特定錯誤。"

![](assets/campaign_email_live_error.png)

此 **[!UICONTROL 錯誤原因]** 圖形和表格可讓您深入瞭解在過去24小時內傳送程式期間發生的特定錯誤。 此資訊對於瞭解錯誤的性質和頻率非常有用。

### 排除原因 {#email-exclude-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_excluded_reasons"
>title="電子郵件 - 排除原因"
>abstract="「排除原因」圖表和表格說明在過去 24 小時內導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

![](assets/campaign_email_live_excluded.png)

此 **[!UICONTROL 排除的原因]** 圖表和表格提供過去24小時內導致從目標對象中排除使用者設定檔的各種因素的完整觀點。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 電子郵件 - 最佳收件者網域 {#email-best-recipient}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_best_recipient"
>title="電子郵件 - 最佳收件者網域"
>abstract="「電子郵件 - 最佳收件者」網域圖表和表格提供收件者開啟電子郵件時最常使用網域的詳細劃分，針對過去 24 小時內的收件者行為提供重要的深入分析。"

![](assets/campaign_email_live_recipient.png)

此 **[!UICONTROL 電子郵件 — 最佳收件者網域]** 圖表和表格提供過去24小時內設定檔最常用來開啟電子郵件之網域的完整劃分。 這可提供描述檔行為的寶貴見解，可幫助您瞭解偏好的平台。

### 電子郵件 — 優惠方案 {#email-offers}

>[!NOTE]
>
>優惠方案Widget和量度僅在決定已插入電子郵件中時才能使用。 有關決定管理的詳細資訊，請參閱此 [頁面](../offers/get-started/starting-offer-decisioning.md).

此 **[!UICONTROL 優惠統計資料]** 和 **[!UICONTROL 一段時間內的優惠統計資料]** Widget可測量您選件的成功程度以及對目標受眾的影響。 它會使用KPI詳細說明與您的訊息相關的主要資訊。

+++ 進一步瞭解電子郵件 — 優惠方案量度

* **[!UICONTROL 已傳送的優惠]**：選件的傳送總數。

* **[!UICONTROL 優惠印象]**：在您的電子郵件中開啟選件的次數。

* **[!UICONTROL 優惠點選次數]**：在您的電子郵件中點按優惠的次數。

+++

## 應用程式內標籤 {#inapp-live}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 應用程式內]** 索引標籤詳細說明與在您的行銷活動中傳送的應用程式內訊息相關的主要資訊。

### 應用程式內效能 {#inapp-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="應用程式內效能"
>abstract="應用程式內效能 KPI 提供有關訪客在過去 24 小時內參與應用程式內訊息的互動情況的重要分析。"

此 **[!UICONTROL 應用程式內績效]** KPI可讓您深入瞭解設定檔在過去24小時內與應用程式內訊息的互動情形，並提供基本量度，以評估應用程式內行銷活動的效益和影響。

+++ 進一步瞭解應用程式內績效量度

* **[!UICONTROL 曝光數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 互動]**：應用程式內訊息的參與總數。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。

+++

### 應用程式內摘要 {#inapp-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="應用程式內摘要"
>abstract="應用程式內摘要圖表顯示過去 24 小時內應用程式內曝光與互動的進展。"

此 **[!UICONTROL 應用程式內摘要]** 圖表會說明應用程式內曝光次數和互動在過去24小時內的進度，提供應用程式內訊息效能的完整概覽。

+++ 進一步瞭解應用程式內摘要量度

* **[!UICONTROL 曝光數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 互動]**：應用程式內訊息的參與總數。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。

+++

### 依類型劃分的互動 {#inapp-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="依類型劃分的互動"
>abstract="「依類型劃分的互動」圖表和表格透過追蹤過去 24 小時內的任何點選、關閉或互動，詳細說明使用者如何與應用程式內訊息進行互動。"

此 **[!UICONTROL 依型別的互動]** 圖表和表格詳細說明個人檔案在過去24小時內如何與您的應用程式內訊息、追蹤動作（例如點選、解僱或任何其他形式的參與）互動。

## 推播通知標籤 {#push-live}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 推播通知]** 索引標籤會詳細說明與行銷活動中傳送之推播通知相關的主要資訊。

### 推播通知 - 傳送效能 {#push-sending-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="推播通知 - 傳送效能"
>abstract="「推播通知傳送效能」圖表總結有關推播通知的基本資料，例如過去 24 小時內的錯誤或已送達的訊息。"

![](assets/campain_push_live_sending_performance.png)

此 **[!UICONTROL 推播通知傳送績效]** graph針對過去24小時內傳送之推播通知的相關資料提供完整概觀。 它提供基本量度的深入分析，例如傳送和跳出，以便詳細檢查推播通知傳送流程。

+++ 進一步瞭解推播通知 — 傳送效能量度

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

+++

### 推播通知 - 統計資料 {#push-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="推播通知 - 統計資料"
>abstract="「推播統計資料」表格提供過去 24 小時內推播通知的收件者活動相關資料。"

![](assets/campaign_push_live_statistics.png)

此 **[!UICONTROL 推播通知 — 統計資料]** 表格提供與過去24小時內推播通知相關的基本資料摘要，包括關鍵量度，例如目標訊息數量和成功傳送訊息數量。

+++ 進一步瞭解推播通知 — 統計量度

* **[!UICONTROL 執行時間]**：您每次執行循環推播通知的開始時間。 若要僅定位一或多個循環推播通知，請從 **[!UICONTROL 執行時間]** 下拉式清單。

* **[!UICONTROL 已鎖定目標]**：傳送過程中處理的訊息總數。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

+++

### 推播通知 - 傳送摘要 {#push-sending-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="推播通知 - 傳送摘要"
>abstract="「推播通知發送摘要」圖表顯示過去 24 小時內已發送的推播通知的可用資料。"

此 **[!UICONTROL 推播通知 — 統計資料]** 圖表提供動態顯示，顯示過去24小時內推播通知活動的分析。 此圖形表示提供已傳送推播通知的完整劃分。

+++ 進一步瞭解推播通知 — 傳送摘要量度

* **[!UICONTROL 開啟次數]**：您的推播通知開啟次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的累計錯誤數和自動傳回處理總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

+++

### 推播通知 - 排除原因 {#push-excluded}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="推播通知 - 排除原因"
>abstract="「排除原因」圖表和表格說明在過去 24 小時內導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

此 **[!UICONTROL 排除的原因]** 圖形和表格會顯示從目標設定檔中排除的使用者設定檔在最近24小時內無法接收推播通知的不同原因。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 推播通知 - 錯誤原因 {#push-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="推播通知 - 錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認過去 24 小時內傳送過程中發生的特定錯誤。"

此 **[!UICONTROL 錯誤原因]** 表格和圖表可讓您識別過去24小時內推播通知傳送流程期間發生的特定錯誤，針對過程中遇到的任何問題提供詳細分析。

### 推播通知 - 依平台劃分 {#push-breakdown-platform}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="推播通知 - 依平台劃分"
>abstract="「依平台劃分」圖表和表格根據收件人的作業系統提供過去 24 小時內成功傳送的推播通知的劃分資料。"

此 **[!UICONTROL 推播通知 — 依據平台的劃分]** 圖表和表格提供過去24小時推播通知成功的詳細分析，根據您的設定檔作業系統提供深入分析。 此劃分可讓您更瞭解推播通知在不同平台上的執行情形。

+++ 進一步瞭解推播通知 — 依平台量度劃分

* **[!UICONTROL 已鎖定目標]**：分析期間處理的訊息總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 開啟次數]**：您的推播通知開啟次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的累計錯誤數和自動傳回處理總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的設定檔數。

+++

## 簡訊標籤 {#sms-live}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 簡訊]** 索引標籤會詳細說明與行銷活動中傳送之SMS訊息相關的主要資訊。

### 簡訊 - 統計資料 {#sms-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="簡訊 - 統計資料"
>abstract="「簡訊傳送統計資料」表格總結有關簡訊的基本資料，例如過去 24 小時內指定對象或已送達的郵件。"

![](assets/campaign_live_sms_statistics.png)

此 **[!UICONTROL 簡訊 — 統計資料]** 表格提供過去24小時內與SMS訊息相關之基本資料的簡要摘要，包含關鍵量度，例如目標訊息數目和成功傳送訊息的數目。

+++ 進一步瞭解簡訊 — 統計量度

* **[!UICONTROL 執行時間]**：您每次執行循環SMS訊息的開始時間。 若要僅定位一或多個循環的SMS訊息，請從 **[!UICONTROL 執行時間]** 下拉式清單。

* **[!UICONTROL 已鎖定目標]**：符合目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 點按次數]**：URL造訪總數。

+++

### 簡訊 - 依日期劃分的效能 {#sms-perfomance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="簡訊 - 依日期劃分的效能"
>abstract="「依日期劃分的簡訊效能」介面工具透過圖形呈現方式提供過去 24 小時內有關你的簡訊的重要資訊。"

![](assets/campaign_live_sms_performance_date.png)

此 **[!UICONTROL 依日期的SMS效能]** widget提供與訊息相關之關鍵資訊的詳細總覽，透過圖表呈現，提供過去24小時內效能趨勢的深入分析。

+++ 進一步瞭解簡訊 — 依據日期量度的績效

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

+++

### 簡訊 - 錯誤原因 {#sms-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="簡訊 - 錯誤原因"
>abstract="「簡訊 - 錯誤原因」圖表和表格讓你能夠確認過去 24 小時內傳送過程中發生的特定錯誤。"

此 **[!UICONTROL 排除的原因]** 圖表和表格可讓您識別過去24小時內SMS訊息傳送流程期間發生的特定錯誤，以便深入分析遇到的任何問題。

### 簡訊 - 排除原因 {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="簡訊 - 排除原因"
>abstract="「排除原因」圖表和表格說明在過去 24 小時內導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

![](assets/campaign_live_sms_excluded.png)

此 **[!UICONTROL 排除的原因]** 圖表和表格會以視覺化方式呈現導致目標對象中排除使用者設定檔的各種因素，以防止他們在過去24小時內收到您的SMS訊息。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 簡訊 - 退回原因 {#sms-bounces-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="簡訊 - 退回原因"
>abstract="「退回原因」圖表和表格包含過去 24 小時內與退回郵件相關的可用資料。"

此 **[!UICONTROL 退回原因]** 圖表和表格提供與彈回SMS訊息相關的完整資料概觀，針對過去24小時內SMS訊息彈回例項背後的特定原因，提供有價值的深入分析。

## 網頁標籤 {#web-tab}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL Web]** 標籤會詳細說明與網頁相關的主要資訊。

### 網頁效能 {#web-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="網頁效能"
>abstract="Web 效能 KPI 提供有關過去 24 小時內訪客參與 Web 體驗相關情形的綜合資訊。"

![](assets/campaign_live_web_performance.png)

此 **[!UICONTROL 網頁效能]** KPI可提供過去24小時內訪客與您的網頁互動情況的全方位深入分析，包含曝光數和互動數等關鍵量度。

+++ 進一步瞭解網站績效計量

* **[!UICONTROL 曝光數]**：傳送給所有使用者的網站體驗總數。

* **[!UICONTROL 互動]**：與您的網頁互動的總次數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

+++

### 網頁摘要 {#web-summary}

![](assets/campaign_live_web_summary.png)

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="網頁摘要"
>abstract="「網頁摘要」圖表說明過去 24 小時內你的 Web 體驗的進展情況，包括曝光、唯一曝光和互動次數。"

此 **[!UICONTROL 網頁摘要]** 圖表顯示您網站體驗在過去24小時中的演變（曝光數、不重複曝光數和互動數）。

+++ 進一步瞭解網頁摘要量度

* **[!UICONTROL 曝光數]**：傳送給所有使用者的網站體驗總數。

* **[!UICONTROL 互動]**：與您的網頁互動的總次數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

+++

### 依元素劃分的互動 {#web-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="依元素劃分的互動"
>abstract="「依元素劃分的互動」表格提供過去 24 小時內訪客參與網頁上不同元素之互動的重要資訊。"

此 **[!UICONTROL 依元素的互動]** 表格提供訪客過去24小時內與您的網頁上各種元素互動的完整資訊，提供使用者互動和偏好設定的寶貴見解。

## 直接郵件標籤 {#direct-mail-tab}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 直接郵件]** 標籤詳細說明與直接郵件相關的主要資訊。

### 直接郵件 - 傳送統計資料 {#direct-mail-sending}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="直接郵件 - 傳送統計資料"
>abstract="「直接郵件傳送統計資料」表格總結過去 24 小時內有關直接郵件的基本資料，例如指定對象或已送達的郵件。"

![](assets/campaign_live_directmail_statistics.png)

此 **[!UICONTROL 直接郵件 — 傳送統計資料]** 表格提供與直接郵件訊息相關之基本資料的簡要摘要，包含關鍵量度，例如目標訊息數量和過去24小時內成功傳遞的訊息計數。

+++ 深入瞭解直接郵件 — 傳送統計量度

* **[!UICONTROL 已鎖定目標]**：符合目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到直接郵件的使用者設定檔數。

+++

### 直接郵件 - 錯誤原因 {#direct-mail-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="直接郵件 - 錯誤原因"
>abstract="「直接郵件 - 錯誤原因」圖表和表格讓你確認過去 24 小時內發生的特定錯誤。"

![](assets/campaign_live_error_reasons.png)

此 **[!UICONTROL 直接郵件 — 錯誤原因]** 圖表和表格提供方法，可識別直接郵件訊息傳送過程中發生的特定錯誤，允許詳細分析過去24小時內遇到的任何問題。

### 直接郵件 - 排除原因 {#direct-mail-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="直接郵件 - 排除原因"
>abstract="「直接郵件排除原因」圖表和表格說明在過去 24 小時內導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

![](assets/campaign_live_directmail_excluded.png)

此 **[!UICONTROL 直接郵件 — 排除的原因]** 圖表和表格以視覺化方式說明導致目標對象中排除使用者設定檔的各種因素，以防止他們在過去24小時內收到您的直接郵件訊息。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [建立API觸發的行銷活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止行銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動全域報告](campaign-global-report.md)
