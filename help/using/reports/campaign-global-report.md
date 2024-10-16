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
source-git-commit: 94d6ebe6e0ad5fa48eaad9d8cfa8cff584f2b819
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 行銷活動全域報告 {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="行銷活動全域報告"
>abstract="行銷活動全域報告可測量您的行銷活動在選取時段內的影響。您的報表會分為不同的介面工具，詳述促銷活動的成功和錯誤。每個報告儀表板都可以透過調整大小或移除介面工具來修改。"

>[!AVAILABILITY]
>
>目前的報告體驗將於2025年1月淘汰。 在此日期之後，新的報告體驗將成為標準體驗。建議您熟悉新功能，以確保順利轉換。 [開始使用Journey Optimizer的新報告介面。](report-gs-cja.md)

全域報告可從&#x200B;**所有時間**&#x200B;標籤存取，可顯示至少兩小時前發生的事件，並涵蓋所選時段內的事件。 相較之下，即時報表著重於過去24小時內發生的事件，最短間隔為事件發生後的2分鐘。

透過&#x200B;**[!UICONTROL 檢視報告]**&#x200B;按鈕，可以直接從您的行銷活動存取行銷活動全域報告。

![](assets/campaign_report_global_5.png)

行銷活動&#x200B;**[!UICONTROL 全域報告]**&#x200B;頁面將會顯示以下標籤：

* [Campaign](#campaign-global)
* [電子郵件](#email-global)
* [應用程式內](#inapp-global)
* [推播](#push-global)
* [簡訊](#sms-global)
* [Web](#web-tab)
* [直接郵件](#direct-mail-global)

行銷活動&#x200B;**[!UICONTROL 全域報告]**&#x200B;會分成不同的Widget，詳細說明行銷活動的成功與錯誤。 如有需要，可以調整每個Widget的大小並將其刪除。 如需詳細資訊，請參閱此[區段](../reports/global-report.md#modify-dashboard)。

如需Adobe Journey Optimizer中每個可用量度的詳細清單，請參閱[此頁面](global-report.md#list-of-components-global.md)

## 行銷活動標籤 {#campaign-global}

### 傳遞 {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="行銷活動的統計資料"
>abstract="行銷活動的統計資料介面工具詳細說明與行銷活動相關的主要資訊，例如所輸入的輪廓及已完成的動作。"

![](assets/campaign_report_global_1.png)

**[!UICONTROL 行銷活動的統計資料]** KPI可作為完整的儀表板，提供與行銷活動相關之關鍵量度的詳細劃分。 這包括基本資訊，例如已傳送的設定檔數和動作，讓您透徹瞭解行銷活動的績效和參與。

+++ 進一步瞭解Campaign的統計量度

* **[!UICONTROL 對象]**：目標設定檔數目。

* **[!UICONTROL 已傳遞的動作]**：已傳遞動作的唯一次數總計。

* **[!UICONTROL 動作在%]**&#x200B;中失敗：動作失敗的不重複次數與已傳遞動作的不重複次數總數的百分比。

+++

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../content-management/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.


### Experimentation report {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Success metric"
>abstract="The total value of the Success metric, previously selected when creating your Experiments, divided by the number of profiles."

![](assets/experimentation_report_3.png)

The **[!UICONTROL Experimentation]** tab provides key insights into the performance of each variant, and identifies the most successful one.

Note that defining the best performer might take some time, it will be represented by this icon ![](assets/experimentation_report_1.png).

+++Learn more on the different metrics and widgets available for the Experimentation report.

The **[!UICONTROL Experiment result]** widget details the performance of each variant. You can change your baseline by selecting one of the treatment from the **[!UICONTROL Baseline]** the drop-down. The best treatment will be represented with a star icon.

For a deep-dive in these results and how to interpret them, refer to [this page](../content-management/get-started-experiment.md#interpret-results).

The table presents the following metrics:

* **[!UICONTROL Lift over baseline]**: Measure of the percentage improvement in conversion rate of a given treatment over the baseline.

* **[!UICONTROL Confidence]**: Evidence that a given treatment is the same as the baseline treatment. [Learn more](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Unique outbound clicks]**: Total count of clicks across outbound channels.

* **[!UICONTROL Profiles]**: Number of profiles targeted for this treatment.

* **[!UICONTROL Unique outbound clicks/profiles]**: Total value of the Success metric, previously selected when creating your Experiments, divided by the number of profiles.

The **[!UICONTROL Confidence interval]** graph measures uncertainty around improvement. It details the percentage difference in performance between the baseline and the best performing treatment. [Learn more](../content-management/experiment-calculations.md#confidence-intervals). 

![](assets/experimentation_report_4.png)

The last widget provides data related to the **[!UICONTROL Success metric]** you previously selected for your Treatments. You have the option to select a different targeted metric from the **[!UICONTROL Metric]** drop-down menu to track alternative data.
    
>[!CAUTION]
>
>When working with experimentation filtered metrics, please note that changing the Metric selection from the drop-down on the comparison page for experimentation will not retain the filter value. For example, switching from "Clicks" to "Unique clicks" will lead to the loss of the applied filter, rendering the comparison inaccurate or invalid.

+++
-->

## 電子郵件標籤 {#email-global}

### 電子郵件 - 傳送統計資料 {#sending-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="電子郵件 - 傳送統計資料"
>abstract="「電子郵件 - 發送統計資料」表格總結你的電子郵件的基本資料，例如「指定對象」或「已送達」。"

![](assets/campaign_email_sending.png)

**[!UICONTROL 電子郵件傳送統計資料]**&#x200B;表格提供有關電子郵件促銷活動之基本資料的完整摘要。 它會詳細說明關鍵量度，例如目標對象的大小和成功傳送的電子郵件數量，為您的電子郵件提供有效性和觸及範圍的寶貴見解。

+++ 進一步瞭解電子郵件傳送統計量度

* **[!UICONTROL 已鎖定目標]**：傳送程式期間處理的電子郵件總數。

* **[!UICONTROL 已傳送]**：您電子郵件的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數目，與已傳送的訊息總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的電子郵件百分比。

* **[!UICONTROL 跳出數]**：在傳送程式期間累積的錯誤總數，以及相對於已傳送訊息總數的自動傳回處理次數。

* **[!UICONTROL 跳出率]**：與已傳送電子郵件相比跳出的電子郵件百分比。

* **[!UICONTROL 錯誤]**：在傳送過程中發生的錯誤總數，導致無法將其傳送至設定檔。

* **[!UICONTROL 錯誤率]**：傳送程式期間發生的錯誤百分比，與已傳送的電子郵件比較，無法傳送。

* **[!UICONTROL 重試]**：重試佇列中的電子郵件數目。

* **[!UICONTROL 已排除]**： Adobe Journey Optimizer已排除的設定檔數目。

+++

### 電子郵件 - 追蹤統計資料 {#tracking-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="電子郵件 - 追蹤統計資料"
>abstract="「電子郵件 - 追蹤統計資料」表格提供你的電子郵件輪廓活動的資料。"

![](assets/campaign_email_tracking.png)

**[!UICONTROL 電子郵件 — 追蹤統計資料]**&#x200B;表格提供與您的電子郵件行銷活動相關的設定檔活動詳細帳戶。 其中包括開啟次數、點按次數和其他相關的參與指標，以提供設定檔與電子郵件內容互動方式的完整檢視。

+++ 進一步瞭解電子郵件 — 追蹤統計量度

* **[!UICONTROL 開啟次數]**：電子郵件開啟的次數。

* **[!UICONTROL 不重複開啟]**：已開啟電子郵件的百分比。

* **[!UICONTROL 開啟率]**：與已傳遞電子郵件數相較的已開啟電子郵件總數。

* **[!UICONTROL 點按]**：內容在電子郵件中的點按次數。

* **[!UICONTROL 不重複點按]**：點按電子郵件中內容的設定檔數目。

* **[!UICONTROL 不重複點按率]**：與您電子郵件互動的使用者百分比。

* **[!UICONTROL 取消訂閱]**：取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾訊息申訴]**：訊息被宣告為垃圾郵件或垃圾訊息的次數。

+++

### 電子郵件 - 傳送效能 {#sending-performance-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="電子郵件 - 傳送效能"
>abstract="「電子郵件 - 傳送效能」圖表顯示有關已發送電子郵件的綜合資料，提供關鍵量度 (例如送出郵件和退回郵件) 的深入分析，以利針對電子郵件傳送過程進行詳細分析。"

![](assets/campaign_email_sending_performance.png)

**[!UICONTROL 電子郵件 — 傳送效能]**&#x200B;圖表提供與已傳送電子郵件相關的完整資料檢視，提供關鍵量度的深入分析，例如傳送和跳出。 這可啟用電子郵件傳送流程的詳細分析，提供電子郵件行銷活動的效率和效能的寶貴資訊。

+++ 進一步瞭解電子郵件 — 傳送效能量度

* **[!UICONTROL 已傳遞]**：與已傳送電子郵件總數相關的成功傳送電子郵件數目。

* **[!UICONTROL 跳出數]**：在傳送程式期間累積的錯誤總數，以及相對於已傳送電子郵件總數的自動傳回處理次數。

* **[!UICONTROL 重試]**：重試佇列中的電子郵件數目。

* **[!UICONTROL 錯誤]**：在傳送過程中發生的錯誤總數，導致無法將其傳送至設定檔。

+++

### 電子郵件 - 退回郵件的原因和類別 {#bounces-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="電子郵件 - 退回類別"
>abstract="「電子郵件 - 退回」類別圖表和表格提供有關暫時性和永久錯誤的資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="電子郵件 - 退回原因"
>abstract="「電子郵件 - 退回原因」圖表和表格包含與退回郵件相關的可用資料。"

![](assets/campaign_email_bounces.png)

**[!UICONTROL 電子郵件 — 退信原因]**&#x200B;和&#x200B;**[!UICONTROL 電子郵件 — 退信類別]** Widget會編譯與退信相關的可用資料，提供電子郵件退信背後特定原因和類別的詳細深入分析。

如需退信的詳細資訊，請參閱[隱藏清單](../reports/suppression-list.md)頁面。

+++ 進一步瞭解電子郵件 — 退回類別量度

* **[!UICONTROL 硬退信]**：永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。

* **[!UICONTROL 軟退信]**：暫時性錯誤的總數，例如完整的收件匣。

* **[!UICONTROL Ignored]**：暫時性的總數，例如「不在辦公室」，或是技術錯誤，例如，如果寄件者型別是郵遞員。

+++


### 電子郵件 - 錯誤原因 {#errors-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="電子郵件 - 錯誤原因"
>abstract="「電子郵件 - 錯誤原因」圖表和表格讓你能夠識別傳送過程中發生的特定錯誤。"

![](assets/campaign_email_error_reasons.png)

**[!UICONTROL 錯誤原因]**&#x200B;圖表和表格提供傳送過程中發生的特定錯誤的可見度，提供有關錯誤性質和發生次數的寶貴資訊。

您可以選擇從表格、長條圖或環形圖切換。

### 電子郵件 - 排除原因 {#excluded-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="電子郵件 - 排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者輪廓被排除在目標客群之外，而未能收到訊息的各項因素。"

![](assets/campaign_email_excluded.png)

**[!UICONTROL 排除的原因]**&#x200B;圖表和表格呈現不同因素的完整檢視，這些因素導致目標對象排除使用者設定檔，導致未收到訊息。

如需排除原因的完整清單，請參閱[此頁面](exclusion-list.md)。

### 依網域劃分的已傳送和已送達郵件 {#sent-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sent_domains"
>title="依網域劃分的已傳送和已送達郵件"
>abstract="「依網域劃分的已傳送和已送達郵件」表格和圖表提供依網域分類的電子郵件劃分資料，呈現對電子郵件通訊整體績效的深入解析。"

![](assets/campaign_email_sent_domains.png)

網域&#x200B;]**的**[!UICONTROL &#x200B;傳送與傳遞表格和圖表提供網域層級的電子郵件詳細劃分，提供您電子郵件效能的完整深入分析。

+++ 進一步瞭解依網域進行之傳送和傳遞的量度

* **[!UICONTROL 已傳送]**：您電子郵件的傳送總數。

* **[!UICONTROL 已傳遞]**：與已傳送電子郵件總數相關的成功傳送電子郵件數目。

+++

### 依網域劃分的退回情形與錯誤 {#bounces-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounces_domains"
>title="依網域劃分的退回情形與錯誤"
>abstract="「依網域劃分的退回情形與錯誤」圖表和表格提供網域層級的精細劃分資料，可讓您深入了解電子郵件傳送過程中遇到的特定錯誤。"

![](assets/campaign_email_bounce_domains.png)

依網域&#x200B;]**的**[!UICONTROL &#x200B;跳出和錯誤圖表和表格提供傳送程式期間遇到的特定錯誤的網域層級劃分，提供所發生問題的詳細分析。

+++ 進一步瞭解依網域量度的跳出和錯誤

* **[!UICONTROL 跳出數]**：在傳送程式期間累積的錯誤總數，以及相對於已傳送電子郵件總數的自動傳回處理次數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生的錯誤總數，使您的電子郵件無法傳送至設定檔。

+++

### 依網域劃分的開啟和點按動作 {#opens-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_open_domains"
>title="依網域劃分的開啟和點按動作"
>abstract="「依網域劃分的開啟和點按動作」圖表和表格提供網域層級的詳細劃分資料，呈現客群與您電子郵件互動方式的全面檢視。"

![](assets/campaign_email_open_domains.png)

**[!UICONTROL 依網域開啟和點按]**&#x200B;的圖表和表格會顯示設定檔與電子郵件互動的網域層級劃分，提供不同網域與內容互動方式的寶貴見解。

+++ 進一步瞭解依網域量度的開啟和點按次數

* **[!UICONTROL 開啟次數]**：電子郵件開啟的次數。

* **[!UICONTROL 點按]**：在電子郵件中點按內容的次數。

+++

### 依網域劃分的退回原因 {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounces_reasons_domains"
>title="依網域劃分的退回原因"
>abstract="「依網域劃分的退回原因」圖表和表格提供網域層級的劃分資料，讓您取得對臨時和永久錯誤的全面深入解析。此詳細分析會為您提供有關退回郵件背後具體原因的珍貴資訊。"

![](assets/campaign_email_bounce_reasons_domains.png)

依網域&#x200B;]**的**[!UICONTROL &#x200B;跳出原因圖表和表格提供與暫時和永久錯誤相關的網域層級資料劃分，提供跳出訊息背後原因的詳細分析。

+++ 進一步瞭解依網域量度的退回原因

* **[!UICONTROL 開啟次數]**：電子郵件開啟的次數。

* **[!UICONTROL 點按]**：在電子郵件中點按內容的次數。

+++

### 電子郵件 - 熱門 URL {#top-url-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="電子郵件 - 熱門 URL"
>abstract="「電子郵件 - 熱門 URL」圖表和表格提供電子郵件中訪客流量最高的 URL 的綜合概觀，讓你能夠確認最受歡迎的連結。"

![](assets/campaign_email_topurl.png)

**[!UICONTROL 電子郵件 — 熱門URL]**&#x200B;圖表和表格提供您電子郵件中吸引最高訪客流量的URL的完整概觀。 這可讓您識別最熱門的連結並排定其優先順序，進而更瞭解電子郵件中特定內容的設定檔參與情形。

### 電子郵件 - 最佳收件者網域 {#top-recipient-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="電子郵件 - 最佳收件者網域"
>abstract="「電子郵件 - 最佳收件者」網域圖表和表格提供收件者開啟電子郵件時最常使用網域的詳細劃分，針對收件者行為提供重要的深入分析。"

![](assets/campaign_email_best_recipient.png)

>[!CAUTION]
>
> **[!UICONTROL 電子郵件 — 最佳收件者網域]** Widget的正確率為99.95%。

**[!UICONTROL 電子郵件 — 最佳收件者網域]**&#x200B;圖表和表格提供設定檔最常用來開啟您的電子郵件的網域詳細劃分。 這可提供描述檔行為的寶貴見解，可幫助您瞭解偏好的平台。

+++ 進一步瞭解電子郵件 — 最佳收件者網域量度

* **[!UICONTROL 已傳遞]**：與已傳送電子郵件總數相關的成功傳送電子郵件數目。

* **[!UICONTROL 傳遞率]**：成功傳送的電子郵件百分比。

* **[!UICONTROL 跳出+錯誤率]**：與已傳送電子郵件相比跳出的電子郵件百分比。

+++

### 電子郵件 - 最佳化 {#optimized-email}

![](assets/campaign_email_optimized.png)

>[!NOTE]
>
>**[!UICONTROL 已最佳化與未最佳化]**&#x200B;和&#x200B;**[!UICONTROL 傳送時間最佳化]** Widget只有在您的電子郵件已啟用傳送時間最佳化選項時，才可使用。 如需傳送時間最佳化的詳細資訊，請參閱[此頁面](../building-journeys/journeys-message.md#send-time-optimization)。

**[!UICONTROL 已最佳化與未最佳化]**&#x200B;和&#x200B;**[!UICONTROL 傳送時間最佳化]**&#x200B;介面工具會詳細說明與您訊息相關的主要資訊（無論是否已最佳化）。

+++ 進一步瞭解傳送時間最佳化量度

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 開啟]**：訊息開啟的次數。

* **[!UICONTROL 點按次數]**：在電子郵件中點按內容的次數。

* **[!UICONTROL 已傳遞]**：與已傳送訊息總數相關的成功傳送訊息數。

* **[!UICONTROL 跳出數]**：在傳送程式期間累積的錯誤總數，以及相對於已傳送訊息總數的自動傳回處理次數。

+++

### 電子郵件 - 優惠 {#email-offers}

![](assets/campaign_email_offers.png)

**[!UICONTROL 優惠統計資料]**、**[!UICONTROL 一段時間內的優惠統計資料]**&#x200B;和&#x200B;**[!UICONTROL 優惠詳細統計資料]** Widget可測量您優惠的成功及對您目標對象的影響。

+++ 進一步瞭解電子郵件 — 優惠方案量度

* **[!UICONTROL 已傳送的優惠]**：優惠的傳送總數。

* **[!UICONTROL 優惠閱聽]**：在您的電子郵件中開啟優惠的次數。

* **[!UICONTROL 優惠點按次數]**：您的電子郵件中某個優惠的點按次數。

* **[!UICONTROL 位置名稱]**：用來顯示優惠方案的位置名稱。 如需位置的詳細資訊，請參閱此[頁面](../offers/offer-library/creating-placements.md)。

* **[!UICONTROL 選件名稱]**：傳遞中新增的選件名稱。 如需位置的詳細資訊，請參閱此[頁面](../offers/offer-library/creating-personalized-offers.md)。

* **[!UICONTROL 已傳送的優惠]**：優惠的傳送總數。

* **[!UICONTROL 優惠曝光率]**：已開啟的優惠相對於已傳送的優惠數目的百分比。

+++

## 應用程式內標籤 {#inapp-global}

從您的行銷活動&#x200B;**[!UICONTROL 全域報告]**，**[!UICONTROL 應用程式內]**&#x200B;索引標籤會詳細說明與行銷活動中傳送之應用程式內訊息相關的主要資訊。

### 應用程式內績效 {#in-app-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="應用程式內績效"
>abstract="應用程式內效能 KPI 提供有關訪客參與應用程式內訊息的重要深入分析。"

![](assets/campaign_inapp_performance.png)

**[!UICONTROL 應用程式內績效]** KPI可讓您深入瞭解訪客與應用程式內訊息的互動程度，並提供評估應用程式內行銷活動成效與影響的基本量度。

+++ 進一步瞭解應用程式內績效量度

* **[!UICONTROL 不重複曝光次數]**：應用程式內訊息已傳送給的不重複使用者人數。

* **[!UICONTROL 曝光次數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 互動]**：與應用程式內訊息互動的總數。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。

+++

### 依類型劃分的互動 {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="依類型劃分的互動"
>abstract="「依類型劃分的互動」圖表和表格透過追蹤任何點選、關閉或互動，詳細說明使用者如何與應用程式內訊息互動。"

![](assets/campaign_inapp_interactions.png)

依型別&#x200B;]**的**[!UICONTROL &#x200B;互動圖表和表格提供設定檔如何與您的應用程式內訊息、追蹤動作（例如點選、解除）或任何其他形式的參與互動的詳細描述。

### 應用程式內摘要 {#in-app-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="應用程式內摘要"
>abstract="應用程式內摘要圖表顯示指定時間內應用程式內曝光與互動的進展。"

![](assets/campaign_inapp_summary.png)

**[!UICONTROL 應用程式內摘要]**&#x200B;圖表會說明應用程式內曝光次數和互動在指定期間的進度，提供您應用程式內訊息效能的完整概觀。

+++ 進一步瞭解應用程式內摘要量度

* **[!UICONTROL 不重複曝光次數]**：應用程式內訊息已傳送給的不重複使用者人數。

* **[!UICONTROL 曝光次數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 互動]**：與應用程式內訊息互動的總數。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。

+++

## 推播通知標籤 {#push-global}

從您的行銷活動&#x200B;**[!UICONTROL 全域報告]**，**[!UICONTROL 推播通知]**&#x200B;索引標籤會詳細說明與行銷活動中傳送之推播通知相關的主要資訊。

### 推播通知 - 傳送統計資料 {#push-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="推播通知 - 傳送統計資料"
>abstract="「推播通知傳送統計資料」表格總結有關推播通知的基本資料，例如指定對象或已送達的訊息。"

![](assets/campaign_push_sending.png)

**[!UICONTROL 推播通知 — 傳送統計資料]**&#x200B;表格提供與推播通知相關之基本資料的簡要摘要，包括關鍵量度，例如目標訊息數目和成功傳送的訊息數目。

+++ 進一步瞭解推播通知 — 傳送統計量度

* **[!UICONTROL 執行時間]**：每次執行您循環推播通知的開始時間。 若要只鎖定一或多個循環推播通知，請從&#x200B;**[!UICONTROL 執行時間]**&#x200B;下拉式清單中選取該通知。

* **[!UICONTROL 已鎖定目標]**：分析期間處理的推播通知總數。

* **[!UICONTROL 已傳送]**：推播通知的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數目（與已傳送的推播通知總數相關）。

* **[!UICONTROL 傳遞率]**：成功傳送的推播通知百分比。

* **[!UICONTROL 跳出數]**：在傳送程式期間累積的錯誤總數，以及相對於推播通知總數的自動傳回處理次數。

* **[!UICONTROL 跳出率]**：與已傳送的推播通知相比跳出的推播通知百分比。

* **[!UICONTROL 錯誤]**：發生無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：無法傳送期間發生的錯誤百分比，與已傳送的推播通知比較。

* **[!UICONTROL 已排除]**： Adobe Journey Optimizer已排除的設定檔數目。

+++

### 推播通知 - 追蹤統計資料 {#push-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="推播通知 - 追蹤統計資料"
>abstract="「推播追蹤統計資料」提供有關推播通知的輪廓活動的資料。"

![](assets/campaign_push_tracking.png)

**[!UICONTROL 推播通知 — 追蹤統計資料]** Widget提供與您的推播通知連結的設定檔活動詳細快照，提供參與和推播通知有效性的基本深入分析。

+++ 進一步瞭解推播通知 — 追蹤統計量度

* **[!UICONTROL 執行時間]**：每次執行您循環推播通知的開始時間。 若要只鎖定一或多個循環推播通知，請從&#x200B;**[!UICONTROL 執行時間]**&#x200B;下拉式清單中選取該通知。

* **[!UICONTROL 開啟]**：您的推播通知開啟的次數。

* **[!UICONTROL 動作]**：已傳送推播通知上的動作總數，例如按鈕點選或解除。

+++

### 推播通知 - 傳送摘要 {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="推播通知 - 傳送摘要"
>abstract="「推播通知傳送摘要」圖表顯示已傳送的推播通知的可用資料。"

![](assets/campaign_push_sending_summary.png)

**[!UICONTROL 推播通知 — 傳送摘要]**&#x200B;圖表提供動態表示，顯示推播通知活動的分析。 此圖形表示提供已傳送推播通知的完整劃分。

+++ 進一步瞭解推播通知 — 傳送摘要量度

* **[!UICONTROL 開啟]**：您的推播通知開啟的次數。

* **[!UICONTROL 動作]**：已傳送推播通知上的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 跳出數]**：累計的錯誤總數，以及與已傳送推播通知總數相關的自動傳回處理次數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數目（與已傳送的推播通知總數相關）。

* **[!UICONTROL 錯誤]**：發生無法傳送至設定檔的錯誤總數。

+++

### 推播通知 — 最佳化 {#push-optimized}

>[!NOTE]
>
>**[!UICONTROL 已最佳化與未最佳化]**&#x200B;和&#x200B;**[!UICONTROL 傳送時間最佳化]** Widget只有在您的推播通知啟用「傳送時間最佳化」選項時，才可使用。 如需傳送時間最佳化的詳細資訊，請參閱[此頁面](../building-journeys/journeys-message.md#send-time-optimization)。

**[!UICONTROL 已最佳化與未最佳化]**&#x200B;和&#x200B;**[!UICONTROL 傳送時間最佳化]**&#x200B;介面工具會詳細說明與您訊息相關的主要資訊（無論是否已最佳化）。

+++ 進一步瞭解推播通知 — 傳送時間最佳化量度

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數目（與已傳送的推播通知總數相關）。

* **[!UICONTROL 開啟]**：您的推播通知開啟的次數。

* **[!UICONTROL 動作]**：已傳送推播通知上的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 跳出數]**：傳送程式與自動傳回處理期間，累積的錯誤總數與已傳送推播通知的總數有關。

+++

### 推播通知 - 錯誤原因 {#error-reasons-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="推播通知 - 錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

![](assets/campaign_push_error_reasons.png)

**[!UICONTROL 錯誤原因]**&#x200B;表格和圖表可讓您識別推播通知傳送過程中發生的特定錯誤，提供過程中所遇到任何問題的詳細深入分析。

### 推播通知 - 排除原因 {#excluded-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="推播通知 - 排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者輪廓被排除在目標客群之外而未能收到訊息的各項因素。"

![](assets/campaign_push_excluded.png)

**[!UICONTROL 排除的原因]**&#x200B;圖表和表格會顯示阻止從目標設定檔排除的使用者設定檔接收推播通知的不同原因。

如需排除原因的完整清單，請參閱[此頁面](exclusion-list.md)。

### 推播通知 - 依平台劃分 {#breakdown-platform-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="推播通知 - 依平台劃分"
>abstract="「推播通知 - 依平台劃分」圖表和表格，會根據輪廓的作業系統提供推播通知成功傳送的劃分資料。"

![](assets/campaign_push_breakdown.png)

**[!UICONTROL 推播通知 — 依平台]**&#x200B;劃分圖表和表格提供推播通知成功的詳細分析，根據您設定檔的作業系統提供深入分析。 此劃分可讓您更瞭解推播通知在不同平台上的執行情形。

+++ 進一步瞭解推播通知 — 依平台量度劃分

* **[!UICONTROL 已鎖定目標]**：分析期間處理的推播通知總數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數目（與已傳送的推播通知總數相關）。

* **[!UICONTROL 開啟]**：您的推播通知開啟的次數。

* **[!UICONTROL 動作]**：已傳送推播通知上的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 跳出數]**：累計的錯誤總數，以及與已傳送推播通知總數相關的自動傳回處理次數。

* **[!UICONTROL 錯誤]**：發生無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 已排除]**： Adobe Journey Optimizer已排除的設定檔數目。

+++

## 簡訊標籤 {#sms-global}

從您的行銷活動&#x200B;**[!UICONTROL 全域報告]**，**[!UICONTROL 簡訊]**&#x200B;索引標籤會詳細說明與行銷活動中傳送之簡訊訊息相關的主要資訊。

### 簡訊 - 傳送統計資料 {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="簡訊 - 傳送統計資料"
>abstract="「簡訊 - 傳送統計資料」表格會總結有關簡訊的基本資料，例如指定對象或已送達的簡訊。"

![](assets/campaign_sms_sending.png)

**[!UICONTROL SMS — 傳送統計資料]**&#x200B;表格提供與您的SMS訊息相關之基本資料的簡要摘要，包含關鍵量度，例如目標訊息數目以及成功傳送訊息的計數。

+++ 進一步瞭解簡訊 — 傳送統計量度

* **[!UICONTROL 執行時間]**：每次執行您週期性SMS訊息的開始時間。 若要只鎖定一或多個循環的SMS訊息，請從&#x200B;**[!UICONTROL 執行時間]**&#x200B;下拉式清單中選取它。

* **[!UICONTROL 目標]**：符合目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：簡訊的傳送總數。

* **[!UICONTROL 跳出數]**：在傳送程式期間累積的錯誤總數，以及相對於已傳送SMS訊息的總數的自動傳回處理次數。

* **[!UICONTROL 錯誤]**：發生無法傳送至設定檔的錯誤總數。

+++

### 簡訊 - 追蹤統計資料 {#sms-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_sms_tracking_statistics"
>title="簡訊 - 追蹤統計資料"
>abstract="「簡訊 - 追蹤統計資料」Widget 會提供訪客與您的 URL 互動相關基本資訊的全面概觀。"

![](assets/campaign_sms_tracking.png)

**[!UICONTROL SMS — 追蹤統計資料]** Widget提供與訪客與您URL互動相關之重要資訊的詳細概觀，提供您SMS訊息有效性的深入分析。

+++ 進一步瞭解簡訊 — 追蹤統計量度

* **[!UICONTROL 執行時間]**：您每一次執行週期性簡訊的開始時間。 若要只鎖定一或多個週期性簡訊，請從&#x200B;**[!UICONTROL 執行時間]**&#x200B;下拉式清單中選取它。

* **[!UICONTROL 點按]**：內容在簡訊訊息中被點按的次數。

+++

### 簡訊 - 依日期劃分的效能 {#sms-perfomance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="簡訊 - 依日期劃分的績效"
>abstract="「簡訊 - 依日期劃分的績效」Widget 透過圖形呈現方式提供有關您簡訊的重要資訊。"

![](assets/campaign_sms_performance.png)

**[!UICONTROL 依日期的SMS效能]** Widget提供訊息相關重要資訊的詳細概觀，透過圖表呈現，提供特定期間效能趨勢的深入分析。

+++ 進一步瞭解簡訊 — 依據日期量度的績效

* **[!UICONTROL 已傳送]**：簡訊的傳送總數。

* **[!UICONTROL 跳出數]**：在傳送程式期間累積的錯誤總數，以及相對於已傳送SMS訊息的總數的自動傳回處理次數。

* **[!UICONTROL 錯誤]**：發生無法傳送至設定檔的錯誤總數。

+++

### 簡訊 - 錯誤原因 {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="簡訊 - 錯誤原因"
>abstract="「簡訊 - 錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

![](assets/campaign_sms_error_reasons.png)

**[!UICONTROL 錯誤原因]**&#x200B;圖表和表格可讓您識別在傳送SMS訊息過程中發生的特定錯誤，協助徹底分析遇到的任何問題。

### 簡訊 - 排除原因 {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="簡訊 - 排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者輪廓被排除在目標客群之外，而未能收到訊息的各項因素。"

![](assets/campaign_sms_excluded.png)

**[!UICONTROL 排除原因]**&#x200B;圖表和表格會以視覺化方式描述導致目標對象中排除使用者設定檔的各種因素，以防止他們接收您的SMS訊息。

如需排除原因的完整清單，請參閱[此頁面](exclusion-list.md)。

### 簡訊 - 退回原因 {#sms-bounces-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="簡訊 - 退回原因"
>abstract="「退回原因」圖表和表格包含與退回郵件相關的可用資料。"

**[!UICONTROL 退信原因]**&#x200B;圖表和表格提供與退信SMS訊息相關的完整資料概觀，針對SMS訊息退信例項背後的特定原因提供有價值的深入分析。

### 簡訊 - 依連結劃分的點按次數 {#sms-clicks-links}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="簡訊 - 依連結劃分的點按次數"
>abstract="「簡訊 - 依連結劃分的點按次數」Widget 會提供有關訪客與您訊息中 URL 互動的重要深入解析。"

![](assets/campaign_sms_clicks.png)

**[!UICONTROL SMS — 連結點按]** Widget可讓您深入瞭解訪客對訊息中所包含URL的參與度，提供哪些連結吸引最多互動的寶貴資訊。

## 網頁標籤 {#web-tab}

從您的行銷活動&#x200B;**[!UICONTROL 全域報告]**，**[!UICONTROL 網頁]**&#x200B;索引標籤會詳細說明與您的網頁相關的主要資訊。

### 網頁績效 {#web-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="網頁效能"
>abstract="Web 效能 KPI 提供有關訪客參與 Web 體驗相關情形的綜合資訊。"

![](assets/campaign_web_performance.png)

**[!UICONTROL 網頁成效]** KPI可提供訪客與網頁互動情況的全方位分析，包含曝光次數和互動等關鍵量度。

+++ 進一步瞭解網站績效計量

* **[!UICONTROL 不重複曝光次數]**：網頁體驗傳送給的不重複使用者人數。

* **[!UICONTROL 曝光次數]**：傳送給所有使用者的網頁體驗總數。

* **[!UICONTROL 互動率]**：與網頁互動的百分比。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

+++

### 網頁摘要 {#web-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="網頁摘要"
>abstract="「網頁摘要」圖表說明指定時間內你的 Web 體驗的進展情況，包括曝光、唯一曝光和互動的次數。"

![](assets/campaign_web_summary.png)

**[!UICONTROL Web摘要]**&#x200B;圖表顯示您在此期間的Web體驗（曝光數、不重複曝光數和互動數）的演變。

+++ 進一步瞭解網頁摘要量度

* **[!UICONTROL 不重複曝光次數]**：網頁體驗傳送給的不重複使用者人數。

* **[!UICONTROL 曝光次數]**：傳送給所有使用者的網頁體驗總數。

* **[!UICONTROL 互動]**：與網頁的互動總數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

+++

### 依元素劃分的互動 {#web-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="依元素劃分的互動"
>abstract="「依元素劃分的互動」表格提供訪客與網頁上不同元素互動的重要資訊。"

![](assets/campaign_web_interactions.png)

**[!UICONTROL 依元素的互動]**&#x200B;表格提供訪客與網頁上各種元素互動的完整資訊，提供使用者互動和偏好設定的寶貴見解。

+++ 進一步瞭解依元素量度的互動

* **[!UICONTROL 互動]**：與網頁的互動總數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

* **[!UICONTROL 互動率]**：與網頁互動的百分比。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

+++

## 直接郵件標籤 {#direct-mail-global}

從您的行銷活動&#x200B;**[!UICONTROL 全域報告]**，**[!UICONTROL 直接郵件]**&#x200B;索引標籤會詳細說明與直接郵件訊息相關的主要資訊。

### 直接郵件 - 傳送統計資料 {#direct-mail-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="直接郵件 - 傳送統計資料"
>abstract="「直接郵件傳送統計資料」表格總結有關直接郵件的基本資料，例如指定對象或已送達的郵件。"

![](assets/campaign_direct_sending.png)

**[!UICONTROL 直接郵件 — 傳送統計資料]**&#x200B;表格提供與直接郵件訊息相關之基本資料的簡要摘要，包含關鍵量度，例如目標訊息數目以及成功傳遞的訊息數目。

+++ 深入瞭解直接郵件 — 傳送統計量度

* **[!UICONTROL 執行時間]**：每次執行您的週期性直接郵件的開始時間。 若要只鎖定一或多個循環的直接郵件，請從&#x200B;**[!UICONTROL 執行時間]**&#x200B;下拉式清單中選取它。

* **[!UICONTROL 目標]**：符合直接郵件訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：直接郵件訊息的傳送總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生的錯誤總數，導致無法將其傳送至設定檔。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到直接郵件訊息的使用者設定檔數目。

+++

### 直接郵件 - 錯誤原因 {#direct-mail-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="直接郵件 - 錯誤原因"
>abstract="「直接郵件 - 錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

![](assets/direct-mail-report_1.png)

**[!UICONTROL 直接郵件 — 錯誤原因]**&#x200B;圖表和表格提供了識別直接郵件訊息傳送過程中發生的特定錯誤的方法，允許對遇到的任何問題進行詳細分析。

### 直接郵件 - 排除原因 {#direct-mail-excluded}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="直接郵件 - 排除原因"
>abstract="「直接郵件排除原因」圖表和表格說明導致使用者輪廓被排除在目標客群之外而未能收到訊息的各項因素。"

![](assets/campaign_direct_excluded.png)

**[!UICONTROL 直接郵件 — 排除的原因]**&#x200B;圖表和表格以視覺化方式說明導致從目標對象中排除使用者設定檔的各種因素，以防止他們接收您的直接郵件訊息。

如需排除原因的完整清單，請參閱[此頁面](exclusion-list.md)。

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [建立API觸發的行銷活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止行銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動即時報告](campaign-live-report.md)
