---
solution: Journey Optimizer
product: journey optimizer
title: 頻道層級報表
description: 瞭解如何使用管道報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ead9359b-cdab-43ed-a469-d98b0ca19a17
source-git-commit: 6bceccc561daac594f5c84d3d3250d887a349b7b
workflow-type: tm+mt
source-wordcount: '2664'
ht-degree: 32%

---

# 頻道報告 {#channel-report}

>[!CONTEXTUALHELP]
>id="ajo_channel_level_report"
>title="管道層級報告"
>abstract="管道報告提供所有管道的流量和參與量度的全面概述。您的報告會分為不同的介面工具，詳述行銷活動和歷程的成功和錯誤。每個報告儀表板都可以透過調整大小或移除介面工具來修改。"

>[!IMPORTANT]
>
> 若要存取&#x200B;**報告**&#x200B;功能表，您必須擁有&#x200B;**[!UICONTROL 檢視頻道報告]**&#x200B;權限。[了解更多](channel-report-gs.md#before-starting-manage-reports-prereq)

管道報表為使用者提供管道層級流量和參與量度的完整概觀。 這些量度會經過彙總，針對來自所選頻道的動作（橫跨各種促銷活動和歷程）呈現彙總值。

您可以導覽至「 」以存取管道報表。 **報表** 功能表中的 **歷程管理** 區段。 由於是完全可自訂的，您可以根據報表日期或動作來篩選資料。 [了解更多](channel-report-gs.md)

報表頁面會顯示以下索引標籤：

* [電子郵件](#email)
* [推播 通知](#push)
* [簡訊](#sms)
* [應用程式內](#inapp)
* [Web](#web)
* [直接郵件](#direct-mail)

➡️ [在影片中探索此功能](#channel-report-video)

## 電子郵件 {#email}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics"
>title="電子郵件 - 傳送統計資料總計"
>abstract="電子郵件 - 傳送統計資料總計 KPI 總結有關推播通知的基本資料，例如指定對象或已送達的郵件。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics"
>title="電子郵件 - 追蹤統計資料總計"
>abstract="電子郵件 - 追蹤統計資料總計 KPI 提供有關你的電子郵件的設定檔活動的資料。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics_overtime"
>title="電子郵件 - 時間區間內傳送統計資料"
>abstract="「電子郵件 - 時間區間內傳送統計資料」圖表顯示有關已傳送的電子郵件的資料，依每小時、每天、每週或每月進行劃分。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics_overtime"
>title="電子郵件 - 時間區間內追蹤統計資料"
>abstract="「電子郵件 - 時間區間內追蹤統計資料」圖表提供有關你的電子郵件的設定檔活動相關資料，依每小時、每天、每週或每月進行劃分。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_categories"
>title="退回類別"
>abstract="「退回」類別的圖表和表格提供有關暫時性和永久錯誤的資料。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons"
>title="退回原因"
>abstract="「退回原因」圖表和表格包含與退回郵件相關的可用資料。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_error_reasons"
>title="錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_excluded_reasons"
>title="排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_delivered_domains"
>title="依網域劃分的已傳送和已送達郵件"
>abstract="「依網域劃分的已傳送和已送達郵件」圖表和表格呈現依網域層級劃分的每封傳送資料的重要電子郵件。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounces_errors_domains"
>title="依網域劃分的退回情形與錯誤"
>abstract="「依網域劃分的退回情形與錯誤」圖表和表格呈現依網域層級劃分的傳送過程中發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_open_clicks_domains"
>title="依網域劃分的開啟和點選動作"
>abstract="「依網域劃分的開啟和點選動作」圖表和表格呈現依網域層級劃分的訪客參與電子郵件互動的情形。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons_domains"
>title="依網域劃分的退回原因"
>abstract="「依網域劃分的退回原因」圖表和表格呈現依網域層級劃分的暫時性錯誤和永久錯誤的資料。"

在管道報表中，電子郵件功能表會詳細說明與行銷活動和歷程中傳送之電子郵件相關的主要資訊。 量度詳情如下。

![](assets/email_channel_1.png)

+++ 進一步瞭解可用於電子郵件報告的不同量度和Widget。

此 **[!UICONTROL 電子郵件總傳送統計資料]** 圖表會詳細說明您的電子郵件是否成功：

* **[!UICONTROL 已鎖定目標]**：已處理的電子郵件總數。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數量，與已傳送訊息總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的電子郵件百分比。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的累計錯誤數和自動傳回處理總數。

* **[!UICONTROL 跳出率]**：與已傳送電子郵件相比跳出的電子郵件百分比。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的電子郵件比較無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的設定檔數。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的設定檔百分比。

此 **[!UICONTROL 電子郵件追蹤統計資料總計]** Widget包含您電子郵件中設定檔活動的可用資料：

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

* **[!UICONTROL 開啟率]**：與已傳遞電子郵件數量相比較的已開啟電子郵件總數。

* **[!UICONTROL 點按次數]**：內容在訊息中被點按的次數。

* **[!UICONTROL 點按率]**：與電子郵件互動的使用者百分比。

* **[!UICONTROL 垃圾郵件投訴數]**：訊息被宣告為垃圾郵件或垃圾郵件的次數。

* **[!UICONTROL 垃圾訊息申訴率]**：與已傳送電子郵件數量相較之下，宣告為垃圾郵件或垃圾郵件的郵件百分比。

* **[!UICONTROL 取消訂閱]**：對訂閱連結的點按次數。

* **[!UICONTROL 取消訂閱率]**：與已傳送電子郵件數目相比的取消訂閱百分比。

此 **[!UICONTROL 傳送一段時間的統計資料]** 圖表包含可用於已傳送電子郵件的資料，例如：

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數，與已傳送電子郵件總數相關。

* **[!UICONTROL 跳出數]**：與已傳送電子郵件總數相關的累積和自動傳回處理的錯誤總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 電子郵件追蹤統計資料（超時）]** 圖表包含可用於開啟和點按的資料。

此 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 退信類別]** Widget包含與退信相關的可用資料，例如：

* **[!UICONTROL 硬退信]**：永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。

* **[!UICONTROL 軟退信]**：暫時性錯誤的總數，例如完整的收件匣。

* **[!UICONTROL 已忽略]**：暫時性總數，例如「不在辦公室」或技術錯誤，例如，如果傳送者型別是郵遞員。

有關退信的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 頁面。

此 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視發生的錯誤。

此 **[!UICONTROL 排除的原因]** 圖表和表格會顯示從目標設定檔中排除的使用者設定檔無法接收訊息的不同原因。

此 **[!UICONTROL 依網域區分的退信原因]**， **[!UICONTROL 依網域傳送和傳遞]**， **[!UICONTROL 依網域區分的開啟與點按]**  和 **[!UICONTROL 依網域區分的退回和錯誤]** 表格和圖表代表每個重要電子郵件傳送和追蹤資料的網域層級劃分。
+++

## 推播通知 {#push}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics"
>title="推播通知 - 傳送統計資料總計"
>abstract="推播通知 - 傳送統計資料總計 KPI 總結有關推播通知的基本資料，例如指定對象或已送達的郵件。"

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics"
>title="推播通知 - 追蹤統計資料總計"
>abstract="「推播通知 - 追蹤統計資料總計」提供有關推播通知的設定檔活動的資料。"

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_overtime"
>title="推播通知 - 時間區間內的傳送統計資料"
>abstract="「推播通知時間區間內傳送統計資料」圖表呈有關已傳送推播通知的資料，依每小時、每天、每週或每月劃分顯示。"

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_overtime"
>title="推播通知 - 時間區間內追蹤統計資料"
>abstract="「推播通知 - 時間區間內追蹤統計資料」圖表提供有關你的推播通知的設定檔活動相關資料，依每小時、每天、每週或每月劃分顯示。"

>[!CONTEXTUALHELP]
>id="ajo_channel_push_excluded_reasons"
>title="排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

>[!CONTEXTUALHELP]
>id="ajo_channel_push_error_reasons"
>title="錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_platform"
>title="依平台劃分的追蹤統計資料"
>abstract="「依平台劃分的追蹤統計資料」圖表和表格根據你的設定檔的作業系統提供推播通知的設定檔活動相關資料。"

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_platform"
>title="依平台劃分傳送統計資料"
>abstract="「依平台劃分的傳送統計資料」圖表和表格顯示有關已傳送推播通知的資料。"

在管道報表中，推播通知功能表會詳細說明與行銷活動和歷程中傳送的推播通知相關的主要資訊。 量度詳情如下。

![](assets/push_channel_1.png)

+++  進一步瞭解推送報表可用的不同量度和Widget。

此 **[!UICONTROL 推播通知 — 傳送統計資料總數]** 表格會使用圖表和KPI詳細列出與推播通知相關的主要資訊：

* **[!UICONTROL 已鎖定目標]**：已處理的推播通知總數。

* **[!UICONTROL 已傳送]**：已傳送推播通知的總數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數，與已傳送推播通知總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的推播通知百分比。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的累計錯誤數和自動傳回處理總數。

* **[!UICONTROL 跳出率]**：與已傳送的推播通知相比退回的推播通知百分比。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的推播通知相比，無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的設定檔數。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的設定檔百分比。

此 **[!UICONTROL 推播通知 — 追蹤統計資料總數]** 包含您的推播通知之設定檔活動的可用資料：

* **[!UICONTROL 開啟次數]**：推播通知開啟的次數。

* **[!UICONTROL 開啟率]**：已開啟推播通知的百分比。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 動作率]**：已傳送推播通知的動作相對於已傳送推播通知的百分比。

* **[!UICONTROL 參與率]**：此推播通知的開啟和動作百分比，亦即，設定檔是否已開啟推播，或按鈕是否已點按。

此 **[!UICONTROL 推播通知 — 傳送一段時間內的統計資料]** 圖表包含可用於已傳送推播通知的資料，例如：

* **[!UICONTROL 已傳送]**：已傳送推播通知的總數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數，與已傳送推播通知總數相關。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的累計錯誤數和自動傳回處理總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 排除的原因]** 圖表和表格會顯示從目標設定檔中排除的使用者設定檔無法接收訊息的不同原因。

此 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視發生的錯誤。

此 **[!UICONTROL 依據平台的追蹤]** 和 **[!UICONTROL 由平台傳送]** 圖表和表格會根據設定檔的作業系統詳細描述推播通知的成功情況。
+++

## 簡訊 {#sms}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics"
>title="簡訊 - 傳送統計資料總計"
>abstract="簡訊 - 傳送統計資料總計 KPI 總結有關簡訊的基本資料，例如指定對象或已送達的簡訊。"

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics"
>title="簡訊 - 追蹤統計資料總計"
>abstract="「SMS - 追蹤統計資料總計」提供有關你的簡訊的設定檔活動相關資料。"

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics_overtime"
>title="簡訊 - 時間區間內傳送統計資料"
>abstract="「簡訊- 時間區間內傳送統計資料」圖表顯示有關已傳送簡訊的資料，依每小時、每天、每週或每月劃分顯示。"

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics_overtime"
>title="簡訊 - 時間區間內追蹤統計資料"
>abstract="「簡訊 - 時間區間內追蹤統計資料」圖表提供有關你的簡訊的設定檔活動相關資料，依每小時、每天、每週或每月劃分顯示。"

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_excluded_reasons"
>title="排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_bounce_reasons"
>title="退回原因"
>abstract="「退回原因」圖表和表格包含與退回郵件相關的可用資料。"

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_error_reasons"
>title="錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

在您的頻道報表中，簡訊功能表會詳細說明與行銷活動和歷程中傳送之簡訊有關的主要資訊。 量度詳情如下。

![](assets/sms_channel_1.png)

+++ 進一步瞭解SMS報告可用的不同量度和Widget。

此 **[!UICONTROL 簡訊 — 傳送統計資料總數]** 表格詳細說明您的SMS成功：

* **[!UICONTROL 已鎖定目標]**：符合SMS頻道目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：已傳送的SMS訊息總數。

* **[!UICONTROL 已傳遞]**：成功傳送的SMS訊息數，與已傳送的SMS訊息總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的SMS訊息百分比。

* **[!UICONTROL 跳出數]**：與已傳送SMS訊息總數相關的累積和自動傳回處理的錯誤總數。

* **[!UICONTROL 跳出率]**：與已傳送的SMS訊息相比跳出的簡訊百分比。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的SMS訊息相比，無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的設定檔百分比。

此 **[!UICONTROL 簡訊 — 追蹤統計資料總數]** Widget會詳細說明與訪客對您URL的參與度相關的主要資訊：

* **[!UICONTROL 點按次數]**：內容在SMS訊息中被點按的次數。

* **[!UICONTROL 點按率]**：與簡訊互動的使用者百分比。

此 **[!UICONTROL 簡訊 — 傳送一段時間內的統計資料]** Widget會以圖表詳細列出與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**：已傳送的SMS訊息總數。

* **[!UICONTROL 已傳遞]**：成功傳送的SMS訊息數，與已傳送的SMS訊息總數相關。

* **[!UICONTROL 跳出數]**：與已傳送SMS訊息總數相關的累積和自動傳回處理的錯誤總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 排除原因]**， **[!UICONTROL 退回原因]** 和 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視發生哪些錯誤和排除。

+++

## 直接郵件 {#direct-mail}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_sending_statistics"
>title="直接郵件 - 傳送統計資料總計"
>abstract="直接郵件 - 傳送統計資料總計 KPI 總結有關直接郵件的基本資料，例如指定對象或已送達的郵件。"

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_excluded_reasons"
>title="排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_error_reasons"
>title="錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

在管道報表中，直接郵件功能表會詳細說明與行銷活動和歷程中傳送之直接郵件訊息相關的主要資訊。 量度詳情如下。

![](assets/direct_mail_channel_1.png)

+++ 進一步瞭解直接郵件報表可用的不同量度和Widget。

此 **[!UICONTROL 直接郵件 — 總傳送統計資料]** 表格詳細說明訊息的成功情況：

* **[!UICONTROL 已鎖定目標]**：符合直接郵件訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的推播通知相比，無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的設定檔百分比。

此 **[!UICONTROL 排除原因]** 和 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視發生哪些錯誤和排除。
+++

## 應用程式內 {#in-app}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement"
>title="應用程式內 - 參與度總計"
>abstract="應用程式內 - 參與度總計 KPI 提供有關訪客參與應用程式內訊息的互動的綜合資訊，包括曝光和互動次數等量度。"

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement_overtime"
>title="應用程式 - 時間區間內參與情形"
>abstract="「應用程式內 - 時間區間內參與度」圖表追蹤應用程式內曝光和互動次數，提供依每小時、每日、每周和每月劃分的資料。"

在管道報表中，應用程式內功能表會詳細說明與促銷活動和歷程中傳送之應用程式內訊息有關的主要資訊。 量度詳情如下。

![](assets/inapp_channel_1.png)

+++  進一步瞭解可用於應用程式內報表的不同量度和Widget。

此 **[!UICONTROL 應用程式內參與總數]** KPI會詳細說明與訪客與您應用程式內訊息的參與度相關的主要資訊，例如：

* **[!UICONTROL 曝光數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 互動]**：應用程式內訊息的參與總數。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。

* **[!UICONTROL 解除]**：按一下關閉按鈕或自動關閉後，設定檔關閉的應用程式內訊息總數。

* **[!UICONTROL 解除率]**：設定檔已關閉的應用程式內訊息百分比。

此 **[!UICONTROL 應用程式內參與加班]** 圖表會透過追蹤任何曝光、關閉或互動，顯示您應用程式內曝光次數和互動在相關期間內的演變。

+++

## Web {#web}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement"
>title="網站 - 參與度總計"
>abstract="網頁 - 參與度總計 KPI 提供有關訪客參與網頁互動的綜合資訊，包括曝光和互動次數等量度。"

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement_overtime"
>title="網頁 - 時間區間內參與度總計"
>abstract="「網頁 - 時間區間內參與度」圖表追蹤你的網頁曝光和互動次數，提供依每小時、每天、每周和每月劃分的資料。"

在管道報表中，網頁功能表會詳細說明與行銷活動和歷程中所包含網頁相關的主要資訊。 量度詳情如下。

![](assets/web_channel_1.png)

+++ 進一步瞭解可用於網頁報表的不同量度和Widget。

此 **[!UICONTROL 網站參與總數]** KPI會詳細說明與訪客對您網站體驗的參與度相關的主要資訊，例如：

* **[!UICONTROL 曝光數]**：傳送給所有使用者的網頁體驗總數。

* **[!UICONTROL 互動]**：與您的網頁互動的總次數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

* **[!UICONTROL 解除]**：設定檔關閉的網頁總數。

* **[!UICONTROL 解除率]**：設定檔關閉的網頁百分比。

此 **[!UICONTROL Web參與加班]** 圖表會詳細說明與訪客對您網頁的參與度相關的主要資訊。

+++

## 管道報表（影片） {#channel-report-video}

透過此影片瞭解如何在頻道層級存取、導覽和匯出報告

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
