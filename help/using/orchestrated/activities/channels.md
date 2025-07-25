---
solution: Journey Optimizer
product: journey optimizer
title: 請在多步驟行銷活動中新增頻道活動
description: 瞭解如何在多步驟行銷活動中，新增頻道活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 3c3ef1555c587b3e50e3b70596fbac98e87d414e
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 77%

---

# 頻道活動 {#channel}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="電子郵件活動"
>abstract="電子郵件活動讓您在協調式行銷活動中傳送電子郵件，單次訊息和定期訊息兩者均適用。此活動會自動執行傳送電子郵件至相同協調式行銷活動內計算的某個目標的流程。您可以將管道活動結合至多步驟行銷活動畫布中，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="簡訊活動"
>abstract="簡訊活動讓您在協調式行銷活動中傳送簡訊，單次訊息和定期訊息兩者均適用。此活動會自動執行傳送簡訊至相同協調式行銷活動內計算的某個目標的流程。您可以將管道活動與多步驟行銷活動版面結合，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="推播活動"
>abstract="推播活動讓您在協調式行銷活動當中傳送推播。推播活動可以傳送單次和定期的協調式行銷活動訊息，自動傳送推播至相同協調式行銷活動內預先定義的目標。您可以將管道活動與行銷活動版面結合，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"

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
>abstract="直接郵件活動讓您在協調式行銷活動中傳送直接郵件更加方便，單次訊息和定期訊息兩者均適用。此類活動會自動執行產生直接郵件提供者所需之摘取檔案的流程。您可以將管道活動與協調式行銷活動版面結合，建立可根據客戶行為和資料觸發動作的跨管道行銷活動。"


+++ 目錄

| 歡迎使用協調行銷活動 | 首次投放的協調行銷活動 | 查詢資料庫 | 協調行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[開始使用結構描述和資料集](../gs-schemas.md)</li><li>[手動結構描述](../manual-schema.md)</li><li>[檔案上傳結構描述](../file-upload-schema.md)</li><li>[擷取資料](../ingest-data.md)</li></ul>[存取及管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[同時加入](and-join.md) - [建立客群](build-audience.md) - [變更維度](change-dimension.md) - <b>[頻道活動](channels.md)</b> - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調和](reconciliation.md) - [儲存客群](save-audience.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]可讓您跨頻道，透過電子郵件、簡訊和推播通知，自動執行行銷活動。 您可以結合頻道活動與協調行銷活動版面，即可根據客戶行為和資料觸發動作，建立跨頻道行銷活動。

例如：
* 透過電子郵件、簡訊和推播等方式，傳送迎賓系列。
* 請在購買後提供後續電子郵件。
* 透過簡訊，傳送個人化生日問候。

使用管道活動，您即可建立全面性和個人化的行銷活動，從多個接觸點和客戶互動並提升轉換率。

>[!PREREQUISITES]
>
>在新增頻道活動之前，請使用[建置客群活動](build-audience.md)，定義目標客群。

## 新增頻道活動，定義屬性 {#add}

1. 請將頻道活動新增至畫布。 可用的頻道活動包括&#x200B;**[!UICONTROL 電子郵件]**、**[!UICONTROL 簡訊]**&#x200B;和&#x200B;**[!UICONTROL 推播]**。

   ![影像會顯示擁有可用活動的畫布](../assets/channel-add.png)

1. 選取活動，然後按一下 **[!UICONTROL [編輯電子郵件]]**、**[!UICONTROL [編輯簡訊]]** 或 **[!UICONTROL [編輯推播]]**，會視選取的頻道而定。

   ![影像顯示擁有電子郵件活動的畫布](../assets/channel-edit.png)

1. 請在&#x200B;**[!UICONTROL 屬性]**&#x200B;索引標籤中，輸入說明，然後切換至&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤，以便設定活動。

## 設定頻道設定和設定 {#configuration}

使用&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤，選取訊息的頻道設定，再設定其他設定，例如追蹤、內容實驗或多語言內容。

1. **選取通道設定**

   會由[系統管理員](../../start/path/administrator.md)定義設定。它包含所有用於傳送訊息的技術參數，如標頭參數、子網域、行動應用程式等等。[了解如何設定頻道設定](../../configuration/channel-surfaces.md)。

   ![顯示 [動作] 區段的影像](../assets/channel-actions.png)

1. **套用上限規則**

   在&#x200B;**[!UICONTROL 規則集]**&#x200B;下拉式清單中，選取管道規則集以將上限規則套用至行銷活動。 運用管道規則集，可讓您根據通訊型別設定頻率上限，以防止訊息相似的客戶超載。 [學習如何使用規則集](../conflict-prioritization/rule-sets.md)

1. **追蹤參與** （電子郵件和簡訊）

   使用&#x200B;**[!UICONTROL 動作追蹤]**&#x200B;區段，追蹤收件者對電子郵件或簡訊傳遞的反應。 一旦執行行銷活動完畢，即可從行銷活動報告，存取追蹤結果。 [深入瞭解行銷活動報告](../../reports/campaign-global-report-cja.md)

1. **啟用快速傳遞模式** （推播）

   快速傳送模式是[!DNL Journey Optimizer]附加元件，允許透過行銷活動，迅速傳送大量推播訊息。 當您想要在行動電話上，傳送緊急推播警報時，例如傳送重大新聞給已安裝新聞頻道應用程式的使用者參考，如果對企業來說，延後傳遞訊息很重要，就可能會使用快速傳遞功能。 如需使用快速傳遞模式時的效能詳細資訊，就請參閱 [Adobe Journey Optimizer 產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html)。

1. **建立內容實驗**

   使用&#x200B;**[!UICONTROL 內容實驗]**&#x200B;區段，您就可以定義多重訊息處理，以便測量針對目標客群，執行哪種處理方式的效果最佳。 按一下 **[!UICONTROL [建立實驗]]** 按鈕，然後依照本區段詳述的步驟完成操作：[建立內容實驗](../../content-management/content-experiment.md)。

1. **新增多語言內容**

   使用&#x200B;**[!UICONTROL 語言]**&#x200B;區段，就能在行銷活動中，使用多語言建立內容。 若想這麼做，就請按一下 **[!UICONTROL [新增語言]]** 按鈕，然後選取指定 **[!UICONTROL [語言設定]]**。 本區段有提供如何設定、使用多語言功能的詳細資訊：[開始使用多語言內容](../../content-management/multilingual-gs.md)

   ![影像會顯示內容實驗區段](../assets/channel-experiment.png)

當設定好頻道活動後，請選取 **[!UICONTROL [內容]]** 索引標籤，即可定義內容。

## 定義內容 {#content}

切換至 **[!UICONTROL [內容]]** 索引標籤，以便建立訊息。 步驟程式會因選定的頻道而有所不同。 若要瞭解建立訊息內容之詳細步驟，請前往以下頁面：

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../../email/create-email.md"><img alt="電子郵件" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../../email/create-email.md"><strong>建立電子郵件</strong></a></td>
<td><a href="../../sms/create-sms.md"><img alt="簡訊" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../../sms/create-sms.md"><strong>建立簡訊</strong></a></td>
<td><a href="../../push/create-push.md"><img alt="推播" src="../../channels/assets/do-not-localize/push.png"></a><a href="../../push/create-push.md"><strong>建立推播通知</strong></a></td>
</tr></table>

## 新增個人化

協調行銷活動中的Personalization的運作方式與其他&#x200B;**[!UICONTROL Journey Optimizer]**&#x200B;行銷活動或歷程類似，但有一些主要差異是特定於協調畫布的。

當您從協調的行銷活動存取個人化編輯器時，有兩個主要資料夾包含可用於個人化的屬性，如下所述。

* **[!UICONTROL 輪廓屬性]**

  此資料夾包含來自[!DNL Adobe Experience Platform]的所有設定檔相關資料。 這些是標準屬性，例如名稱、電子郵件地址、位置或使用者設定檔中擷取的任何其他特徵。

* **[!UICONTROL Target屬性]** （特定於協調的行銷活動）

  此資料夾是協調行銷活動的唯一資料夾。 它包含直接在行銷活動畫布中計算的屬性。 它包含兩個子資料夾：

   * **`<Targeting dimension>`** （例如「收件者」、「購買」）：包含與行銷活動所定位的維度相關的所有屬性。

   * **`Enrichment`**：包含透過畫布中的&#x200B;**[!UICONTROL 擴充]**&#x200B;活動新增的資料。 這可讓您根據外部資料集或在協調期間納入的其他邏輯來個人化訊息。 [瞭解如何使用擴充活動](../activities/enrichment.md)

如需如何使用個人化編輯器的詳細概觀，請參閱[開始使用個人化](../../personalization/personalize.md)

## 檢查並測試您的內容

一旦建立內容完畢，就請使用 **[!UICONTROL [模擬內容]]** 按鈕，以從 CSV / JSON 檔案上傳，或可透過手動新增的測試設定檔，或是範例輸入資料，預覽並測試內容。 [了解更多](../../content-management/preview-test.md)

![顯示 [模擬內容] 按鈕的影像](../assets/channel-simulate.png)

## 後續步驟 {#next}

當訊息內容已就緒時，請使用 **[!UICONTROL [上一步]]** 箭頭，返回協調行銷活動。 然後，您就可以在畫布中完成活動協調流程，然後發佈行銷活動，以便開始傳送訊息。 [瞭解如何開始並監視協調行銷活動](../start-monitor-campaigns.md)

![顯示返回按鈕的影像](../assets/channel-back.png)

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
