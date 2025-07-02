---
solution: Journey Optimizer
product: journey optimizer
title: 在多步驟行銷活動中新增管道活動
description: 瞭解如何在多步驟行銷活動中新增管道活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: cfb09467809a69516c34d52be3f41e7a1abdb7c3
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 17%

---

# 管道活動 {#channel}

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[建立協調行銷活動的重要步驟](../gs-campaign-creation.md) | [建立協調的行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用查詢Modeler](../orchestrated-rule-builder.md)<br/><br/>[建置您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建置對象](build-audience.md) - [變更維度](change-dimension.md) - **[頻道活動](channels.md)** - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[!DNL Adobe Journey Optimizer]可讓您跨管道自動執行行銷活動。 您可以將頻道活動結合到協調的行銷活動畫布中，以建立跨頻道協調的行銷活動，其可根據客戶行為和資料觸發動作。

例如，您可以建立一個歡迎電子郵件活動，其中包括跨不同管道的一系列訊息，例如電子郵件、簡訊和推播。您還可以在客戶完成購買後傳送後續追蹤電子郵件，或透過簡訊向客戶傳送個人化的生日祝賀訊息。

透過使用管道活動，您可以建立全面且個人化的行銷活動，在多個接觸點吸引客戶並促進轉換。 支援的管道包括電子郵件、簡訊和推播。

## 先決條件 {#channel-activity-prereq}

開始使用相關活動建置您的協調行銷活動：

* 插入管道活動之前，您必須定義對象。 對象是您傳送的主要目標：接收訊息的設定檔。 [瞭解如何使用建置對象活動](build-audience.md)

* 若要傳送循環傳遞，請使用&#x200B;**[!UICONTROL 排程器]**&#x200B;活動來開始您的協調行銷活動。 您也可以針對單次傳送使用&#x200B;**[!UICONTROL 排程器]**&#x200B;活動，以設定該傳送的聯絡日期。 您也可以在傳送設定中設定聯絡日期。 [LEarn如何排程協調的行銷活動](../create-orchestrated-campaign.md#schedule)

## 設定管道活動 {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="電子郵件活動"
>abstract="電子郵件活動可讓您在協調的行銷活動中傳送電子郵件，包括一次性訊息和循環訊息。 它有助於將傳送電子郵件至目標的程式自動化，並在相同協調的行銷活動中計算。 您可以將管道活動結合至多步驟行銷活動畫布中，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="簡訊活動"
>abstract="SMS活動可讓您在協調的行銷活動中針對單次和循環訊息傳送SMS。 它有助於自動處理傳送SMS至在相同協調行銷活動中計算的目標。 您可以將管道活動結合至多步驟行銷活動畫布中，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="推播活動"
>abstract="推播活動可讓您在協調的行銷活動中傳送推播通知。 它可啟用一次性與循環協調行銷活動的傳送，將傳送推播通知自動傳送到相同協調行銷活動內預先定義的目標。 您可以將頻道活動結合到行銷活動畫布中，以建立跨頻道行銷活動，其可根據客戶行為和資料觸發動作。"

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same orchestrated campaign. You can combine channel activities into the orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="直接郵件活動"
>abstract="直接郵件活動可促進在協調的行銷活動中進行直接郵件傳送，無論是單次還是循環訊息。 此類活動可用於將直接郵件提供者所需之摘取檔案產生流程自動化。您可以將頻道活動結合到協調的行銷活動畫布中，以建立跨頻道行銷活動，其可根據客戶行為和資料觸發動作。"

若要在協調的行銷活動內容中設定傳送，請遵循下列步驟。

### 新增管道活動並定義其屬性 {#add}

1. 將管道活動新增至畫布。 可用的頻道活動包括&#x200B;**[!UICONTROL 電子郵件]**、**[!UICONTROL 簡訊]**&#x200B;和&#x200B;**[!UICONTROL 推播]**。

   ![影像顯示具有可用活動的畫布](../assets/channel-add.png)

1. 選取新增的活動，然後依據所選的頻道，按一下&#x200B;**[!UICONTROL 編輯電子郵件]**、**[!UICONTROL 編輯簡訊]**&#x200B;或&#x200B;**[!UICONTROL 編輯推播]**&#x200B;按鈕。

   ![影像顯示具有電子郵件活動的畫布](../assets/channel-edit.png)

1. 在&#x200B;**[!UICONTROL 屬性]**&#x200B;索引標籤中，輸入行銷活動的說明。

### 設定管道組態和設定 {#configuration}

1. 選取&#x200B;**[!UICONTROL 動作]**&#x200B;標籤，並選擇要用於訊息的通道設定。

   設定是由[系統管理員](../../start/path/administrator.md)所定義。 它包含所有用於傳送訊息的技術參數，如標頭參數、子網域、行動應用程式等等。[瞭解如何設定頻道設定](../../configuration/channel-surfaces.md)。

1. 針對電子郵件和簡訊，使用追蹤選項來監視收件者對您的電子郵件或簡訊傳遞的反應。

   執行行銷活動後，即可從行銷活動報表存取追蹤結果。 [進一步瞭解行銷活動報告](../../reports/campaign-global-report-cja.md)

1. 對於推播通知，請使用&#x200B;**[!UICONTROL 快速傳送模式]**&#x200B;選項，在推播頻道上執行高速訊息傳送，以傳送至3000萬名以下的對象。

   快速傳遞模式是&#x200B;**[!DNL Journey Optimizer]**&#x200B;附加元件，允許以大數量快速傳送推播訊息。 [了解更多](../../push/create-push.md#rapid-delivery)

1. **[!UICONTROL 內容實驗]**&#x200B;區段可讓您定義多個傳遞處理方式，以測量哪個方式最適合您的目標對象。

   若要這麼做，請按一下&#x200B;**[!UICONTROL 建立實驗]**&#x200B;按鈕，然後依照本節詳述的步驟進行： [建立內容實驗功能](../../content-management/content-experiment.md)。

1. **[!UICONTROL 語言]**&#x200B;區段可讓您在行銷活動中建立多種語言的內容。

   若要這麼做，請按一下&#x200B;**[!UICONTROL 新增語言]**&#x200B;按鈕，然後選取所需的&#x200B;**[!UICONTROL 語言設定]**。 本節提供如何設定及使用多語言功能的詳細資訊： [開始使用多語言內容](../../content-management/multilingual-gs.md)

### 定義內容 {#content}

選取&#x200B;**[!UICONTROL Content]**&#x200B;索引標籤以定義訊息的內容。 內容建立程式取決於所選的頻道。

在以下頁面瞭解建立訊息內容的詳細步驟：

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../../email/create-email.md"><img alt="電子郵件" src="../../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../../email/create-email.md"><strong>電子郵件</strong></a></div></td>
<td><a href="../../sms/create-sms.md"><img alt="簡訊" src="../../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../../sms/create-sms.md"><strong>簡訊</strong></a></div></td>
<td><a href="../../push/create-push.md"><img alt="推播" src="../../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../../push/create-push.md"><strong>推播通知</strong></a></div></td>
</tr></table>

定義內容後，請使用&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕，以測試設定檔或從CSV / JSON檔案上傳的範例輸入資料來預覽和測試您的內容，或手動新增。 [了解更多](../../content-management/preview-test.md)

## 後續步驟 {#next}

使用&#x200B;**[!UICONTROL 上一步]**&#x200B;箭頭，導覽回您精心安排的行銷活動。

![顯示返回按鈕的影像](../assets/channel-back.png)

您現在可以在畫布中完成活動協調，並發佈行銷活動以開始傳送訊息。 [瞭解如何開始及監視協調的行銷活動](../start-monitor-campaigns.md)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel orchestrated campaign example with a segmentation and two deliveries. The orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
