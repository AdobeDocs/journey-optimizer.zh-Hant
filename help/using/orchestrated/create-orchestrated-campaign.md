---
solution: Journey Optimizer
product: journey optimizer
title: 使用Journey Optimizer建立及排程協調的行銷活動
description: 瞭解如何使用Adobe Journey Optimizer建立協調的行銷活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 435b4a7eee9428c7f0efeb62c72b39c0e2aaabba
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 19%

---


# 建立並安排協調式行銷活動 {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="協調式行銷活動清單"
>abstract="「**協調**」索引標籤列出所有協調式行銷活動。按一下協調的行銷活動的名稱即可編輯。使用「**建立協調的行銷活動**」按鈕新增新的協調的行銷活動。"

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](configuration-steps.md)<br/><br/>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](gs-campaign-creation.md)<br/><br/><b>[建立並排程行銷活動](create-orchestrated-campaign.md)</b><br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[傳送包含協調行銷活動的訊息](send-messages.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建置對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

檔案處理中

>[!ENDSHADEBOX]

## 建立行銷活動 {#create}

若要建立協調的行銷活動，請遵循下列步驟：

1. 瀏覽至&#x200B;**[!UICONTROL 行銷活動]**&#x200B;功能表，選取&#x200B;**[!UICONTROL 協調流程]**&#x200B;索引標籤，然後選取&#x200B;**[!UICONTROL 建立行銷活動]**。

   ![](assets/inventory-create.png)

1. 輸入已協調行銷活動的名稱。 此外，我們強烈建議您在專用欄位中新增說明。

1. （選用）使用&#x200B;**標籤**&#x200B;欄位將Adobe Experience Platform統一標籤指派給您協調的行銷活動。 這可讓您輕鬆分類，並改進行銷活動清單的搜尋。 [瞭解如何使用標籤](../start/search-filter-categorize.md#tags)。

1. 按一下「**[!UICONTROL 建立]**」按鈕確認。


您協調的行銷活動現在已建立，並可在行銷活動清單中使用。 您可以按一下行銷活動畫布中的![行銷活動設定圖示](assets/do-not-localize/campaign-settings.svg)圖示，隨時變更這些屬性。


## 排程行銷活動 {#schedule}

根據預設，協調的行銷活動會在手動啟動後開始，並在執行活動後立即結束。

如果您不想在協調行銷活動啟動後立即執行，您可以指定應執行的日期和時間。 您也可以根據各種條件，以固定頻率執行行銷活動。

若要設定行銷活動的排程，請開啟協調的行銷活動，然後按一下&#x200B;**[!UICONTROL 儘快]**&#x200B;按鈕。

![](assets/create-schedule.png)

<!--In the Execution frequency field, select 

time zone

daily, weekly, monthly
several times a day based on specific hours or periodically

recurring frequencies (all except as soon and once)
preview launch times
validity period

>[!NOTE]
>
>When scheduling campaigns in [!DNL Adobe Journey Optimizer], ensure your start date/time aligns with the desired first delivery. For recurring campaigns, if the initial scheduled time has already passed, the campaigns will roll over to the next available time slot according to their recurrence rules.

## Work with orchestrated campaign templates {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Orchestrated campaign templates"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaign."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Orchestrated campaign properties"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. In this screen, enter the label of the orchestrated campaign template and configure its settings such as its internal name, folder and execution folders, timezone, and supervisor group."

Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. You can select the template of your orchestrated campaign from the orchestrated campaign properties, when creating an orchestrated campaign. An empty template is provided by default.

You can create a template from an existing orchestrated campaign, or create a new template from scratch. Both methods are detailed below.

>[!BEGINTABS]

>[!TAB Create a template from an existing orchestrated campaign]

To create an orchestrated campaign template from an existing orchestrated campaign, follow these steps:

1. Open to the **Campaign** menu and browse to the orchestrated campaign to save as a template.
1. Click the three dots on the right of the name of the orchestrated campaign, and choose **Copy as template**.
1. In the popup window, confirm the template creation.
1. In the orchestrated campaign template canvas, check, add, and configure the activities as needed.
1. Browse to the settings, from the **Settings** button, to change the name of the orchestrated campaign template, and enter a description.
1. Select the **folder** and **execution folder** of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.


>[!TAB Create a template from scratch]


To create an orchestrated campaign template from scratch, follow these steps:

1. Open to the **Campaign** menu and browse to the **Templates** tab. You can see the list of available orchestrated campaign templates.
1. Click the **[!UICONTROL Create template]** button in the upper-right corner of the screen.
1. Enter the label and open the additional options to enter a description of your orchestrated campaign template.
1. Select the folder and execution folder of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Click the **Create** button to confirm your settings.
1. In the orchestrated campaign template canvas, add and configure the activities as needed.

     ![](assets/wf-template-activities.png){zoomable="yes"}

1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.

>[!ENDTABS]






## Next steps {#next}

Once your campaign configuration and content are ready, you can review and activate it. [Learn more](review-activate-campaign.md)

-->