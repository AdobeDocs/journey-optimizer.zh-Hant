---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的第一個歷程
description: 使用 Adobe Journey Optimizer 建置您的第一個歷程的關鍵步驟
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，第一，開始，快速入門，對象，事件，動作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 23%

---

# 建立您的第一個歷程 {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="建立歷程"
>abstract="使用 **Adobe Journey Optimizer** 可讓您善用儲存在事件或資料來源中的內容關聯式資料，建置即時協調流程使用案例。"

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="歷程"
>abstract="設計客戶歷程提供個人化的內容關聯式體驗。Journey Optimizer 可讓您利用儲存在事件或資料來源中的內容關聯式資料，建立即時協調流程使用案例。**概觀&#x200B;**&#x200B;索引標籤會顯示儀表板，其中包含與您的歷程相關的關鍵量度。**瀏覽&#x200B;**&#x200B;索引標籤會顯示現有歷程的清單。"

Adobe Journey Optimizer 包含全頻道協調流程畫布，可讓行銷人員協調行銷外聯活動與一對一客戶參與。 使用者介面可讓您輕鬆將活動從浮動視窗拖放至畫布，以建立您的歷程。 歷程使用者介面在[此頁面](journey-ui.md)上詳細說明。

![歷程畫布範例](assets/journey38.png)


建立歷程的主要步驟將於本頁詳細說明。 其簡化如下：

![歷程建立步驟：建立、設計、測試和發佈](assets/journey-creation-process.png)


建立多步驟客戶歷程可跨管道即時起始一系列互動、優惠方案和訊息。 此方法可確保根據客戶的動作和相關業務訊號，在最佳時刻與客戶互動。 可以根據行為、情境資料和業務事件來定義Target對象。 先決條件取決於您的使用案例，以及您正在建置的[歷程型別](entry-management.md#types-of-journeys)。

在開始建立您的歷程之前，請檢查相關的設定步驟已完成：

* 如果您想要在收到事件時統一觸發您的歷程，您需要&#x200B;**設定事件**。 您可以定義預期的資訊及其處理方式。 [閱讀全文](../event/about-events.md)。

<!--   ![](assets/jo-event7bis.png)  -->

* 您的歷程也可以監聽Adobe Experience Platform對象，以批次傳送訊息至指定的設定檔集。 為此，您需要&#x200B;**建立對象**。 [閱讀全文](../audience/about-audiences.md)。

<!--   ![](assets/segment2.png)  -->

* 您可以定義系統連線，以擷取將用於歷程的其他資訊，例如在您的條件中。 此連線依賴&#x200B;**資料來源**。 [閱讀全文](../datasource/about-data-sources.md)

<!--   ![](assets/jo-datasource.png)  -->

* Journey Optimizer隨附[內建訊息](../building-journeys/journeys-message.md)功能。 如果您使用協力廠商系統來傳送訊息，您可以&#x200B;**建立自訂動作**。 在此[節](../action/action.md)中瞭解更多。

<!--    ![](assets/custom2.png)  -->


對於資料工程師，設定歷程的步驟 (包括資料來源、事件和動作) 已詳細說明，請參閱[本節](../configuration/about-data-sources-events-actions.md)。


>[!NOTE]
>
>在[此頁面](../start/guardrails.md)上詳細描述歷程護欄和限制

## 建立歷程 {#jo-build}

若要建立多步驟歷程，請遵循下列步驟：

1. 在「歷程管理」功能表區段中，按一下&#x200B;**[!UICONTROL 歷程]**。

1. 按一下&#x200B;**[!UICONTROL 建立歷程]**&#x200B;按鈕以建立新歷程。

1. 編輯歷程的設定窗格以定義歷程的名稱並設定其屬性。 瞭解如何在[此頁面](journey-properties.md)上設定您的歷程屬性。

   ![](assets/jo-properties.png)

接著，您就可以開始設計您的歷程。

## 設計歷程 {#jo-design}

全頻道歷程設計器可協助您使用直覺式的拖放介面，透過目標客群建立多步驟歷程、根據即時客戶或業務互動進行更新以及全頻道訊息。

![](assets/journey38.png)

1. 首先，從浮動視窗拖放事件或&#x200B;**讀取對象**&#x200B;活動到畫布。 若要進一步瞭解歷程設計，請參閱[本節](using-the-journey-designer.md)。

   ![](assets/read-segment.png)

1. 拖放個人會遵循的後續步驟。 例如，您可以新增條件，然後新增管道動作。 若要進一步瞭解活動，請參閱[本節](about-journey-activities.md)。

## 測試歷程 {#jo-test}

一旦您建立了您的歷程，您就可以在發佈之前先測試它。 Journey Optimizer提供「測試模式」，以便在測試設定檔歷程中移動時檢視測試設定檔，並在啟用之前偵測潛在錯誤。 執行快速測試可讓您檢查歷程是否正確運作，以便您能夠放心發佈。

在此[小節](testing-the-journey.md)中瞭解更多

## 發佈此歷程 {#jo-pub}

您必須發佈歷程才能啟用它，並讓新設定檔可以進入它。 發佈歷程之前，請確認其有效且沒有錯誤。 您無法發佈含有錯誤的歷程。 在此[區段](publishing-the-journey.md)中進一步瞭解歷程發佈。

![](assets/jo-journeyuc2_32bis.png)

發佈後，您可以使用專用的報告工具監控您的歷程，以評估歷程的成效。

![](assets/jo-dynamic_report_journey_12.png)

在此[區段](../reports/live-report.md)中進一步瞭解歷程報告。

>[!NOTE]
>
>如果您需要修改為&#x200B;**即時**&#x200B;歷程，請[建立歷程的新版本](journey-ui.md#journey-versions)。
