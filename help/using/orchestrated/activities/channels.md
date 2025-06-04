---
solution: Journey Optimizer
product: journey optimizer
title: 在多步驟行銷活動中新增管道活動
description: 瞭解如何在多步驟行銷活動中新增管道活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 2935e611bb9682256a324485b28e7dd2552e1dd2
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 44%

---

# 管道活動 {#channel}

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調的行銷活動活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](configuration-steps.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立協調的行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[使用協調的行銷活動傳送訊息](send-messages.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用查詢Modeler](orchestrated-query-modeler.md)<br/><br/>[建置您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建置對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

Adobe Journey Optimizer可讓您跨傳入和傳出頻道自動執行行銷活動。 您可以將頻道活動結合到協調的行銷活動畫布中，以建立跨頻道協調的行銷活動，其可根據客戶行為和資料觸發動作。 支援的管道列於[此頁面](../../channels/gs-channels.md)。

例如，您可以建立歡迎電子郵件行銷活動，其中包括跨不同頻道的一系列訊息，例如電子郵件、簡訊、推播和直接郵件。 您還可以在客戶完成購買後傳送後續追蹤電子郵件，或透過簡訊向客戶傳送個人化的生日祝賀訊息。

使用管道活動，您即可建立全面性和個人化的行銷活動，從多個接觸點和客戶互動並提升轉換率。

## 先決條件 {#channel-activity-prereq}

開始使用相關活動建置您的協調行銷活動：

* 插入管道活動之前，您必須定義對象。 對象是您傳送的主要目標：接收訊息的設定檔。

* 若要傳送循環傳遞，請使用&#x200B;**排程器**&#x200B;活動來開始您的協調行銷活動。 您也可以針對單次傳送使用&#x200B;**排程器**&#x200B;活動，以設定該傳送的聯絡日期。 您也可以在傳送設定中設定聯絡日期。

## 設定管道活動 {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="電子郵件活動"
>abstract="電子郵件活動讓您可以在多步驟行銷活動中傳送電子郵件，單次訊息和定期訊息兩者均適用。此活動可用來自動化在相同多步驟行銷活動內傳送電子郵件至所計算之目標的流程。您可以將管道活動結合至多步驟行銷活動畫布中，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="簡訊活動"
>abstract="簡訊活動讓您可以在多步驟行銷活動中傳送簡訊，單次訊息和定期訊息兩者均適用。此活動可用來自動化在相同多步驟行銷活動內傳送簡訊至所計算之目標的流程。您可以將管道活動結合至多步驟行銷活動畫布中，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="推播 iOS 活動"
>abstract="推播 iOS 活動可讓您傳送 iOS 推播通知作為多步驟行銷活動的一部分。此活動可以傳送單次和定期的多步驟行銷活動，自動將 iOS 推播通知傳送至相同工作流程中的預先定義目標。您可以將管道活動組合到工作流程畫布中，建立可根據客戶行為和資料觸發動作的跨管道工作流程。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="推播 Android 活動"
>abstract="推播 Android 活動可讓您傳送 Android 推播通知作為多步驟行銷活動的一部分。此活動可以傳送單次和定期的訊息，自動將 Android 推播通知傳送到相同多步驟行銷活動中的預先定義目標。您可以將管道活動結合至多步驟行銷活動畫布中，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="直接郵件活動"
>abstract="直接郵件活動有助於在多步驟行銷活動中傳送直接郵件，單次訊息和定期訊息兩者均適用。此類活動可用於將直接郵件提供者所需之摘取檔案產生流程自動化。您可以將管道活動結合至多步驟行銷活動畫布中，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"

若要在協調的行銷活動內容中設定傳送，請遵循下列步驟：

1. 新增頻道活動： **[!UICONTROL 電子郵件]**、**[!UICONTROL 簡訊]**、**[!UICONTROL 推播通知(Android)]**、**[!UICONTROL 推播通知(iOS)]**&#x200B;或&#x200B;**[!UICONTROL 直接郵件]**。

1. 選取&#x200B;**傳遞型別**：單一或循環。

   * **單一傳遞**&#x200B;為單次傳遞，僅傳送一次，例如「黑色星期五」電子郵件。
   * 根據其執行頻率，**循環傳遞**&#x200B;會傳送多次。 每次執行協調的行銷活動時，都會重新計算對象，並將傳送內容傳送給更新後的對象，其中包含更新的內容。 例如，這可以是每週電子報或循環生日電子郵件。

1. 選取傳遞&#x200B;**範本**。範本是預先設定的傳遞設定 (特定於管道)。每個管道都有內建範本可用，預設會預先填入。

   ![](../assets/delivery-activity-in-wf.png)

   您可以從管道活動設定左窗格中選取範本。 如果之前選取的客群和管道不相容，則無法選取範本。若要解決此問題，請更新&#x200B;**建立對象**&#x200B;活動，以選取具有正確目標對應的對象。

1. 按一下「**建立傳遞**」。然後，您可以像建立獨立傳送一樣定義訊息設定和內容。 您也可以測試和模擬內容。

1. 導覽回您的工作流程。 如果要繼續工作流程，請切換&#x200B;**產生出站轉變**&#x200B;選項，以在頻道活動後新增轉變。

1. 按一下&#x200B;**開始**&#x200B;以啟動您的協調行銷活動。

   依預設，啟動協調的行銷活動會觸發訊息準備階段，而不會立即傳送訊息。

1. 開啟您的頻道活動，以確認從&#x200B;**檢閱並傳送**&#x200B;按鈕進行傳送。

1. 在您的傳遞儀表板中，按一下「**傳送**」。

## 範例 {#cross-channel-workflow-sample}

以下是跨頻道協調的行銷活動範例，包含細分和兩個傳送。 這項精心策劃的行銷活動目標鎖定所有居住在巴黎並對咖啡機感興趣的客戶。 針對此群體，會傳送電子郵件給普通客戶，並傳送簡訊給 VIP 用戶端。

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

您也可以建立循環協調的行銷活動，於每月第一天晚上8點傳送個人化簡訊給住在巴黎的所有客戶。

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
