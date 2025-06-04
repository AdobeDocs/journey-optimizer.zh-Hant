---
solution: Journey Optimizer
product: journey optimizer
title: 使用Journey Optimizer建立協調的行銷活動
description: 瞭解如何使用Adobe Journey Optimizer建立協調的行銷活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 7f535b87e415ae9191199b34476adb5c977b66e9
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 17%

---


# 建立協調行銷活動 {#create-first-campaign}

+++ 目錄

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調的行銷活動活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](configuration-steps.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立協調的行銷活動](create-orchestrated-campaign.md)<br/><br/>[協調活動](orchestrate-activities.md)<br/><br/>[使用協調的行銷活動傳送訊息](send-messages.md)<br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用查詢Modeler](orchestrated-query-modeler.md)<br/><br/>[建置您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建置對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="協調的行銷活動清單"
>abstract="「**多步驟**」索引標籤列出所有協調的行銷活動。按一下協調的行銷活動的名稱即可編輯。使用「**建立協調的行銷活動**」按鈕新增新的協調的行銷活動。"

## 建立行銷活動

若要建立協調的行銷活動，請遵循下列步驟：

1. 若要建立&#x200B;**協調的行銷活動**，請瀏覽至&#x200B;**行銷活動**&#x200B;功能表。

1. 按一下畫面右上角的&#x200B;**[!UICONTROL 建立協調的行銷活動]**&#x200B;按鈕。

1. 在協調的行銷活動&#x200B;**屬性**&#x200B;對話方塊中，選取要用來建立協調行銷活動的範本（您也可以使用預設的內建範本）。 [進一步瞭解協調的行銷活動範本](#campaign-templates)。

1. 輸入已協調行銷活動的標籤。 此外，強烈建議您在畫面的&#x200B;**[!UICONTROL 其他選項]**&#x200B;區段的專屬欄位中，新增描述至您的協調行銷活動。

1. 展開&#x200B;**[!UICONTROL 其他選項]**&#x200B;區段，為協調的行銷活動設定更多設定。

1. 按一下&#x200B;**[!UICONTROL 建立協調的行銷活動]**&#x200B;按鈕，以確認建立您的協調行銷活動。

您協調的行銷活動現在已建立，並可在工作流程清單中使用。 您現在可以存取其視覺畫布，並開始新增、設定和協調其將執行的任務。 [瞭解如何協調行銷活動](orchestrate-activities.md)。

## 設定行銷活動設定

新管理員設定>結構描述、執行欄位、合併原則的概觀。 [了解更多](configuration-steps.md)

## 使用協調的行銷活動範本 {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="協調的行銷活動範本"
>abstract="協調的行銷活動範本包含預先設定的設定和活動，在建立新的協調的行銷活動時可以重複使用。"

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="協調的行銷活動屬性"
>abstract="協調的行銷活動範本包含預先設定的設定和活動，在建立新的協調的行銷活動時可以重複使用。在此畫面中，輸入協調的行銷活動範本的標籤並設定其設定，例如其內部名稱、資料夾和執行資料夾、時區和監督者群組。"

協調的行銷活動範本包含預先設定的設定和活動，在建立新的協調的行銷活動時可以重複使用。建立協調行銷活動時，您可以從協調的行銷活動屬性中選取協調行銷活動的範本。 預設會提供空白範本。

您可以從現有的協調行銷活動建立範本，或從頭開始建立新範本。 兩種方法皆詳述於下方。

>[!BEGINTABS]

>[!TAB 從現有的協調行銷活動建立範本]

若要從現有的協調行銷活動建立協調行銷活動範本，請遵循下列步驟：

1. 開啟&#x200B;**行銷活動**&#x200B;功能表，並瀏覽至協調的行銷活動以另存為範本。
1. 按一下協調行銷活動名稱右側的三個點，然後選擇&#x200B;**復製為範本**。
1. 在快顯視窗中，確認範本建立。
1. 在協調的行銷活動範本畫布中，視需要檢查、新增及設定活動。
1. 從&#x200B;**設定**&#x200B;按鈕瀏覽至設定，以變更協調行銷活動範本的名稱，並輸入說明。
1. 選取範本的&#x200B;**資料夾**&#x200B;和&#x200B;**執行資料夾**。 資料夾是儲存協調行銷活動範本的位置。 執行資料夾是指儲存根據此範本建立之協調行銷活動的資料夾。
1. 儲存您的變更。

範本清單現在提供已協調的行銷活動範本。 您可以根據此範本建立協調的行銷活動。 此協調的行銷活動將會預先設定範本中定義的設定和活動。


>[!TAB 從頭開始建立範本]


若要從頭開始建立協調的行銷活動範本，請遵循下列步驟：

1. 開啟&#x200B;**促銷活動**&#x200B;功能表，並瀏覽至&#x200B;**範本**&#x200B;標籤。 您可以檢視可用協調的行銷活動範本清單。
1. 按一下畫面右上角的&#x200B;**[!UICONTROL 建立範本]**&#x200B;按鈕。
1. 輸入標籤，然後開啟其他選項，以輸入協調行銷活動範本的說明。
1. 選取範本的資料夾和執行資料夾。 資料夾是儲存協調行銷活動範本的位置。 執行資料夾是指儲存根據此範本建立之協調行銷活動的資料夾。
1. 按一下「**建立**」按鈕以確認您的設定。
1. 在協調的行銷活動範本畫布中，視需要新增及設定活動。

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. 儲存您的變更。

範本清單現在提供已協調的行銷活動範本。 您可以根據此範本建立協調的行銷活動。 此協調的行銷活動將會預先設定範本中定義的設定和活動。

>[!ENDTABS]
