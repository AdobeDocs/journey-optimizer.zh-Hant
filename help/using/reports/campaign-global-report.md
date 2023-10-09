---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動全域報告
description: 瞭解如何使用Campaign全域報告的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 6bceccc561daac594f5c84d3d3250d887a349b7b
workflow-type: tm+mt
source-wordcount: '3181'
ht-degree: 3%

---

# 行銷活動全域報告 {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="行銷活動全域報告"
>abstract="行銷活動全域報告可測量您的行銷活動在選取時段內的影響。您的報表會分為不同的介面工具，詳述促銷活動的成功和錯誤。每個報告儀表板都可以透過調整大小或移除介面工具來修改。"

全域報告，可從存取 **所有時間** 標籤，顯示至少兩小時前發生的事件，以及所選時段內的封面事件。 相較之下，即時報表著重於過去24小時內發生的事件，最短間隔為事件發生後的2分鐘。

行銷活動全域報告可透過以下直接從行銷活動存取： **[!UICONTROL 檢視報告]** 按鈕。

![](assets/campaign_report_global_5.png)

行銷活動 **[!UICONTROL 全域報告]** 頁面會顯示以下索引標籤：

* [Campaign](#campaign-global)
* [電子郵件](#email-global)
* [應用程式內](#inapp-global)
* [推播](#push-global)
* [簡訊](#sms-global)
* [Web](#web-tab)
* [直接郵件](#direct-mail-global)

行銷活動 **[!UICONTROL 全域報告]** 分成不同的Widget，詳細說明行銷活動的成功和錯誤。 如有需要，可以調整每個Widget的大小並將其刪除。 如需詳細資訊，請參閱此 [區段](../reports/global-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [此頁面](global-report.md#list-of-components-global.md)

## 行銷活動標籤 {#campaign-global}

### 傳送 {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="行銷活動的統計資料"
>abstract="行銷活動的統計介面工具集會詳細說明與行銷活動相關的主要資訊，例如，已輸入的設定檔和已傳送的動作。"

![](assets/campaign_report_global_1.png)

此 **[!UICONTROL 行銷活動的統計資料]** widget會詳細說明與行銷活動相關的主要資訊：

* **[!UICONTROL 輸入的設定檔]**：開始歷程的設定檔數。

* **[!UICONTROL 動作已傳送]**：歷程中動作已傳送的不重複總次數。

* **[!UICONTROL 動作失敗百分比]**：與動作已傳送的不重複次數總數相比，歷程中動作失敗的不重複次數。

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.
-->

### 實驗報告 {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="成功量度"
>abstract="先前在建立實驗時選取的成功量度的總值除以設定檔的數量。"

![](assets/experimentation_report_3.png)

此 **[!UICONTROL 實驗]** Tab提供每個變體績效的關鍵分析，並識別最成功的變體。

請注意，定義績效最佳者可能需要一些時間，其將以此圖示表示 ![](assets/experimentation_report_1.png).

+++進一步瞭解Experimentation報表中可用的不同量度和Widget。

此 **[!UICONTROL 實驗結果]** widget詳細說明每個變體的效能。 您可以透過以下方式選取處理方式之一來變更基準線： **[!UICONTROL 基線]** 下拉式清單。 最佳處理方式會以星形圖示表示。

此表格會顯示下列量度：

* **[!UICONTROL 提升度超過基準線]**：測量指定處理的轉換率相對於基線的增進百分比。

* **[!UICONTROL 信賴度]**：指定處理與基線處理相同的證據。 [了解更多](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL 不重複傳出點按]**：跨傳出頻道的點按總數。

* **[!UICONTROL 設定檔]**：針對此處理的設定檔數。

* **[!UICONTROL 不重複傳出點按次數/設定檔]**：建立實驗時先前選取的成功量度總值除以設定檔數量。

此 **[!UICONTROL 信賴區間]** 圖表會測量改善的不確定性。 它詳細說明基準線和最佳執行處理之間的效能百分比差異。 [了解更多](../campaigns/experiment-calculations.md#confidence-intervals)。

![](assets/experimentation_report_4.png)

最後一個Widget提供的資料與 **[!UICONTROL 成功量度]** 您先前已為「處理」選取。 您可以選擇從中選擇不同的目標量度 **[!UICONTROL 量度]** 用於追蹤替代資料的下拉式功能表。

>[!CAUTION]
>
>使用實驗中的篩選量度時，請注意，從實驗比較頁面上的下拉式清單中變更量度選取範圍時，不會保留篩選值。 例如，從「點按」切換至「不重複點按」會導致套用的篩選器遺失，導致比較不準確或無效。

+++

如需這些結果的深入瞭解以及如何解讀，請參閱 [此頁面](../campaigns/get-started-experiment.md#interpret-results).

## 電子郵件索引標籤 {#email-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="電子郵件 — 傳送統計資料"
>abstract="電子郵件 — 傳送統計資料表會概述有關電子郵件的基本資料，例如「已鎖定目標」或「已傳送」。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="電子郵件 — 追蹤統計資料"
>abstract="「電子郵件 — 追蹤」統計資料表格提供有關您電子郵件之設定檔活動的資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="電子郵件 — 傳送績效"
>abstract="電子郵件 — 傳送績效圖表顯示有關已傳送電子郵件的全面資料，提供傳遞和退回等關鍵量度的深入分析，允許電子郵件傳遞流程的詳細分析。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="電子郵件 — 退回類別"
>abstract="電子郵件 — 退回類別圖表和表格會提供暫時和永久錯誤的相關資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="電子郵件 — 退回原因"
>abstract="「電子郵件 — 退信原因」圖表和表格包含與退信相關的可用資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="電子郵件 — 錯誤原因"
>abstract="「電子郵件 — 錯誤原因」圖表和表格可讓您識別在傳送過程中發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="電子郵件 — 排除的原因"
>abstract="「排除的原因」圖表和表格說明導致使用者設定檔從目標對象中排除而不接收訊息的各種因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="電子郵件 — 熱門URL"
>abstract="電子郵件 — 熱門URL圖表和表格提供電子郵件中，接收最高訪客流量的URL的完整概觀，讓您識別最受歡迎的連結。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="電子郵件 — 最佳收件者網域"
>abstract="「電子郵件 — 最佳收件者網域」圖表和表格提供收件者最常用來開啟電子郵件的網域詳細劃分，為收件者行為提供有價值的深入分析。"

![](assets/campaign_report_global_2.png)

從您的行銷活動 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 電子郵件]** 索引標籤詳細說明與在您的Campaign中傳送的電子郵件傳遞相關的主要資訊。

+++進一步瞭解可用於電子郵件報告的不同量度和Widget。

此 **[!UICONTROL 電子郵件傳送統計資料]** 圖表會詳細說明您的電子郵件是否成功：

* **[!UICONTROL 已鎖定目標]**：傳送過程中處理的訊息總數。

* **[!UICONTROL 已傳送]**：電子郵件的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的訊息百分比。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 跳出率]**：與已傳送電子郵件相比跳出的電子郵件百分比。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的電子郵件相比，在傳送過程中發生而無法傳送的錯誤百分比。

* **[!UICONTROL 重試]**：重試佇列中的電子郵件數。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的設定檔數。

此 **[!UICONTROL 電子郵件 — 追蹤統計資料]** Widget包含您電子郵件之設定檔活動的可用資料：

* **[!UICONTROL 開啟次數]**：電子郵件開啟的次數。

* **[!UICONTROL 不重複開啟次數]**：已開啟電子郵件的百分比。

* **[!UICONTROL 開啟率]**：與已傳遞電子郵件數量相比較的已開啟電子郵件總數。

* **[!UICONTROL 點按次數]**：內容在電子郵件中的點按次數。

* **[!UICONTROL 不重複點按]**：在電子郵件中點按內容的設定檔數。

* **[!UICONTROL 不重複點按率]**：與您的電子郵件互動的使用者百分比。

* **[!UICONTROL 取消訂閱]**：對取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾郵件投訴數]**：訊息被宣告為垃圾郵件或垃圾郵件的次數。

此 **[!UICONTROL 傳送績效]** 圖表包含可用於已傳送電子郵件的資料，例如：

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 重試]**：重試佇列中的電子郵件數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 退信類別]** Widget包含與退信相關的可用資料，例如：

* **[!UICONTROL 硬退信]**：永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。

* **[!UICONTROL 軟退信]**：暫時性錯誤的總數，例如完整的收件匣。

* **[!UICONTROL 已忽略]**：暫時性總數，例如「不在辦公室」或技術錯誤，例如，如果傳送者型別是郵遞員。

有關退信的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 頁面。

此 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視傳送程式期間發生哪些錯誤。

此 **[!UICONTROL 排除的原因]** 圖表和表格會顯示從目標設定檔中排除的使用者設定檔無法接收訊息的不同原因。

此 **[!UICONTROL 電子郵件 — 熱門URL]** 圖表和表格詳細說明您電子郵件中哪些的URL的造訪次數最多。

此 **[!UICONTROL 電子郵件 — 熱門收件者網域]** 圖表和表格詳細說明設定檔最常用來開啟電子郵件的網域。

>[!NOTE]
>
>此 **[!UICONTROL 已最佳化與未最佳化]** 和 **[!UICONTROL 傳送時間最佳化]**  只有當您的電子郵件已啟用傳送時間最佳化選項時，才可使用Widget。 如需傳送時間最佳化的詳細資訊，請參閱 [此頁面](../building-journeys/journeys-message.md#send-time-optimization).

此 **[!UICONTROL 已最佳化與未最佳化]** 圖表詳細說明與訊息相關的主要資訊，無論是否已最佳化：

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

* **[!UICONTROL 點按次數]**：內容在電子郵件中的點按次數。

此 **[!UICONTROL 傳送時間最佳化]** 根據傳送方式詳細說明您的電子郵件是否成功：已最佳化或正常。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。
+++

## 應用程式內標籤 {#inapp-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="應用程式內績效"
>abstract="應用程式內績效KPI可讓您深入瞭解訪客與應用程式內訊息的互動程度。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="依型別的互動"
>abstract="「依型別的互動」圖表和表格會追蹤任何點按、解除或互動，以詳細說明使用者如何與您的應用程式內訊息互動。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="應用程式內摘要"
>abstract="應用程式內摘要圖表會說明應用程式內曝光次數和互動在指定期間內的進度。"

從您的行銷活動 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 應用程式內]** 索引標籤會詳細說明與行銷活動中傳送之應用程式內傳遞相關的主要資訊。

![](assets/campaign_report_global_6.png)

+++進一步瞭解應用程式內報表可用的不同量度和Widget。

此 **[!UICONTROL 應用程式內績效]** KPI會詳細說明與訪客與您應用程式內訊息的參與度相關的主要資訊，例如：

* **[!UICONTROL 不重複曝光次數]**：應用程式內訊息已傳送給的不重複使用者人數。

* **[!UICONTROL 曝光數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 互動率]**：應用程式內訊息的參與百分比。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。

此 **[!UICONTROL 依型別的互動]** 圖表和表格會詳細說明使用者如何透過追蹤任何點選、解除或互動來與您的應用程式內訊息互動。

此 **[!UICONTROL 應用程式內摘要]** 圖表會顯示相關期間應用程式內曝光次數和互動的演變。
+++

## 推播通知標籤 {#push-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="推播通知 — 傳送統計資料"
>abstract="「推播通知傳送統計資料」表格會摘要推播通知的相關基本資料，例如「已鎖定目標」或「已傳送的訊息」。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="推播通知 — 追蹤統計資料"
>abstract="「推播追蹤統計資料」可提供推播通知之設定檔活動的資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="推播通知 — 傳送摘要"
>abstract="「推播通知傳送摘要」圖表會顯示已傳送推播通知的可用資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="推播通知 — 排除的原因"
>abstract="「排除的原因」圖表和表格說明導致使用者設定檔從目標對象中排除而不接收訊息的各種因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="推播通知 — 錯誤原因"
>abstract="「錯誤原因」圖表和表格可讓您識別傳送程式期間發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="推播通知 — 依據平台的劃分"
>abstract="「依平台劃分」圖表和表格會根據設定檔的作業系統，提供推播通知成功與否的劃分資訊。"

從您的行銷活動 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 推播通知]** 索引標籤會詳細說明與行銷活動中傳送之推播傳遞相關的主要資訊。

![](assets/campaign_report_global_3.png)應用程式內績效KPI會詳細說明與訪客與應用程式內訊息互動相關的主要資訊。

+++進一步瞭解推送報表可用的不同量度和Widget。

此 **[!UICONTROL 推播通知 — 傳送統計資料]** 表格詳細說明與推播通知相關的主要資訊

* **[!UICONTROL 已鎖定目標]**：分析期間處理的訊息總數。

* **[!UICONTROL 已傳送]**：推播通知的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的訊息百分比。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 跳出率]**：與已傳送的推播通知相比退回的推播通知百分比。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的推播通知相比，無法傳送期間發生的錯誤百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的設定檔數。

此 **[!UICONTROL 推播 — 追蹤統計資料]** 包含推播通知之設定檔活動的可用資料：

* **[!UICONTROL 開啟次數]**：您的推播通知開啟次數。

* **[!UICONTROL 開啟率]**：已開啟推播通知的百分比。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 參與]**：此推播通知的開啟和動作總數，也就是設定檔是否已開啟推播，或按鈕是否已點按。

* **[!UICONTROL 參與率]**：此推播通知的開啟和動作百分比，亦即，設定檔是否已開啟推播，或按鈕是否已點按。

此 **[!UICONTROL 推播通知摘要]** 圖表包含可用於已傳送推播通知的資料，例如：

* **[!UICONTROL 開啟次數]**：您的推播通知開啟次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的累計錯誤數和自動傳回處理總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

>[!NOTE]
>
>此 **[!UICONTROL 已最佳化與未最佳化]** 和 **[!UICONTROL 傳送時間最佳化]**  只有為您的推播通知啟動傳送時間最佳化選項時，才可使用Widget。 如需傳送時間最佳化的詳細資訊，請參閱 [此頁面](../building-journeys/journeys-message.md#send-time-optimization).

此 **[!UICONTROL 已最佳化與未最佳化]** 圖表詳細說明與訊息相關的主要資訊，無論是否已最佳化：

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 開啟次數]**：您的推播通知開啟次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

此 **[!UICONTROL 傳送時間最佳化]** 根據傳送方式詳細說明推播通知是否成功：已最佳化或正常。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

此 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視發生的錯誤。

此 **[!UICONTROL 排除的原因]** 圖形和表格會顯示從目標設定檔中排除的使用者設定檔無法接收訊息的不同原因。

此 **[!UICONTROL 依平台劃分]** 圖形和表格會根據您的設定檔作業系統詳細描述推播通知的成功情況。
+++

## 簡訊索引標籤 {#sms-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="簡訊 — 傳送統計資料"
>abstract="「SMS傳送統計資料」表格會摘要有關SMS訊息的基本資料，例如「已鎖定目標」或「已傳送」訊息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="簡訊 — 錯誤原因"
>abstract="SMS — 錯誤原因圖表和表格可讓您識別傳送程式期間發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="簡訊 — 依據日期的績效"
>abstract="依日期的SMS效能Widget可透過圖形化呈現方式，提供您訊息的重要相關資訊。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="簡訊 — 排除的原因"
>abstract="「排除的原因」圖表和表格說明導致使用者設定檔從目標對象中排除而不接收訊息的各種因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="簡訊 — 退回原因"
>abstract="「退信原因」圖表和表格包含與退信相關的可用資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="簡訊 — 依據連結的點按"
>abstract="SMS — 連結點按次數Widget提供訪客與訊息中URL互動的基本深入分析"

從您的行銷活動 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 簡訊]** 索引標籤會詳細說明與行銷活動中傳送之SMS傳遞相關的主要資訊。

![](assets/campaign_report_global_4.png)

+++進一步瞭解SMS報表可用的不同量度和Widget。

此 **[!UICONTROL 簡訊 — 傳送統計資料]** 表格詳細說明您的SMS訊息是否成功：

* **[!UICONTROL 已鎖定目標]**：符合目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 已傳送]**：您的SMS訊息傳送總數。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 依日期的SMS效能]** Widget會以圖表詳細列出與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**：您的SMS訊息傳送總數。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 排除原因]** 和 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視傳送程式期間發生哪些錯誤和排除。

此 **[!UICONTROL 簡訊 — 依據連結的點按]** Widget會詳細說明與訪客與您URL互動相關的主要資訊。

+++

## 網頁標籤 {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="網頁效能"
>abstract="網站績效KPI提供關於訪客與網站體驗互動情況的完整資訊。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="網頁摘要"
>abstract="「Web摘要」圖表可說明您的Web體驗在指定期間內的進度，包括曝光數、不重複曝光數和互動數。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="依元素的互動"
>abstract="「依元素的互動」表格提供有關訪客與網頁上不同元素互動的關鍵資訊。"

從您的行銷活動 **[!UICONTROL 全域報告]**，則 **[!UICONTROL Web]** 標籤會詳細說明與網頁相關的主要資訊。

![](assets/web-report.png)

+++進一步瞭解可用於網頁報表的不同量度和Widget。

此 **[!UICONTROL 網頁效能]** KPI會詳細說明與訪客對您網站體驗的參與度相關的主要資訊，例如：

* **[!UICONTROL 不重複曝光次數]**：提供網頁體驗的不重複使用者人數。

* **[!UICONTROL 曝光數]**：傳送給所有使用者的網站體驗總數。

* **[!UICONTROL 互動率]**：與您的網頁互動的百分比。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

此 **[!UICONTROL 網頁摘要]** 圖表會顯示相關期間您網站體驗（曝光數、不重複曝光數和互動數）的演變。

此 **[!UICONTROL 依元素的互動]** 此表格詳細說明與您的訪客與您網頁上各種元素的參與度相關的主要資訊。
+++

## 直接郵件索引標籤 {#direct-mail-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="直接郵件 — 傳送統計資料"
>abstract="「直接郵件傳送統計資料」表格會摘要有關直接郵件訊息的基本資料，例如「已鎖定目標」或「已傳遞」訊息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="直接郵件 — 錯誤原因"
>abstract="「直接郵件 — 錯誤原因」圖表和表格可讓您識別在傳送過程中發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="直接郵件 — 排除的原因"
>abstract="「直接郵件排除的原因」圖表和表格說明了導致使用者設定檔從目標對象中排除而不接收訊息的各種因素。"

從您的行銷活動 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 直接郵件]** 索引標籤會詳細說明與直接郵件傳送相關的主要資訊。

![](assets/direct-mail-report_1.png)

+++進一步瞭解直接郵件報表可用的不同量度和Widget。

此 **[!UICONTROL 直接郵件 — 傳送統計資料]** 下表詳細說明直接郵件的成功率：

* **[!UICONTROL 已鎖定目標]**：符合此直接郵件目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：此直接郵件的傳送總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到直接郵件的使用者設定檔數。

此 **[!UICONTROL 直接郵件 — 排除的原因]** 和 **[!UICONTROL 直接郵件 — 錯誤原因]** 圖表和表格可讓您檢視傳送程式期間發生哪些錯誤和排除。
+++

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [建立API觸發的行銷活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止行銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動即時報告](campaign-live-report.md)
