---
title: 建立程式碼型體驗
description: 瞭解如何在Journey Optimizer中建立程式碼型體驗
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 3f7d71eecf282b21eb09423378008c3b9ccd7edc
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 10%

---

# 建立程式碼型體驗 {#create-code-based}

目前在[!DNL Journey Optimizer]中，您只能在&#x200B;**行銷活動**&#x200B;中建立程式碼型體驗。

有關程式碼型體驗的特定護欄和建議，請參閱[此頁面](code-based-prerequisites.md)。

## 建立程式碼型行銷活動 {#create-code-based-campaign}

若要透過行銷活動開始建立程式碼型體驗，請遵循下列步驟。

1. 建立行銷活動。 [了解更多](../campaigns/create-campaign.md)

1. 選取&#x200B;**[!UICONTROL 程式碼型體驗]**&#x200B;動作。

1. 輸入程式碼型體驗介面。 [了解更多](#surface-definition)

   ![](assets/code-based-campaign-surface.png)

   >[!CAUTION]
   >
   >請確定您的程式碼型行銷活動中使用的表面URI與您自己的實施中使用的表面URI相符。 否則，將不會傳送變更。

1. 選取「**[!UICONTROL 建立]**」。

1. 完成步驟以建立行銷活動，例如行銷活動屬性、[對象](../audience/about-audiences.md)和[排程](../campaigns/create-campaign.md#schedule)。 如需如何設定行銷活動的詳細資訊，請參閱[此頁面](../campaigns/get-started-with-campaigns.md)。

1. 使用個人化編輯器，視需要編輯您的內容。 [了解更多](#edit-code)

   ![](assets/code-based-campaign-edit-content.png)

## 編輯程式碼內容 {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="使用個人化編輯器"
>abstract="插入並編輯您想要作為此基於程式碼之體驗動作的一部分的程式碼。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html?lang=zh-Hant" text="開始使用個人化編輯器"

1. 在行銷活動版本畫面中，選取&#x200B;**[!UICONTROL 編輯代碼]**。

   ![](assets/code-based-campaign-edit-code.png)

1. [個人化編輯器](../personalization/personalization-build-expressions.md)開啟。 這是非視覺化體驗建立介面，可讓您編寫程式碼。

1. 您可以將編寫模式從HTML切換為JSON，反之亦然。

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >變更編寫模式將會遺失您目前的所有程式碼，因此在開始編寫之前，請務必切換模式。

1. 視需要輸入您的程式碼。 您可以善用[!DNL Journey Optimizer]個人化編輯器及其所有個人化和編寫功能。 [了解更多](../personalization/personalization-build-expressions.md)

1. 您可以視需要新增HTML或JSON運算式片段。 [了解作法](../personalization/use-expression-fragments.md)

   您也可以將部分程式碼內容儲存為片段。 [了解作法](../content-management/fragments.md#save-as-expression-fragment)

1. 在程式碼型行銷活動中，您可以使用體驗決策功能。 從左側列選取&#x200B;**[!UICONTROL 決定]**&#x200B;圖示，然後按一下&#x200B;**[!UICONTROL 建立決定]**。 [了解更多](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >體驗決策目前僅可適用於一組組織 (可用性限制)。 若要取得存取權，請和您的 Adobe 代表聯絡。


1. 按一下&#x200B;**[!UICONTROL 儲存並關閉]**&#x200B;以確認您的變更。

現在，當您的開發人員進行API或SDK呼叫以擷取所選表面的內容時，變更就會套用至您的網頁或應用程式。

## 測試基於程式碼的行銷活動 {#test-code-based-campaign}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="預覽您的基於程式碼的體驗"
>abstract="模擬基於程式碼的體驗。"

若要顯示已修改程式碼型體驗的預覽，請遵循下列步驟。 有關如何選取測試設定檔和預覽內容的詳細資訊，請參閱[預覽和測試內容頁面](../content-management/preview-test.md)。

>[!CAUTION]
>
>您必須有可用的測試設定檔，以模擬將傳送給他們的優惠。 瞭解如何[建立測試設定檔](../audience/creating-test-profiles.md)。

1. 從個人化編輯器或編輯內容畫面中，選取&#x200B;**[!UICONTROL 模擬內容]**。

   ![](assets/code-based-campaign-simulate.png)

1. 按一下&#x200B;**[!UICONTROL 管理測試設定檔]**&#x200B;以選取一或多個測試設定檔。

1. 畫面上會顯示已修改程式碼式體驗的預覽。

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## 啟用程式碼型行銷活動 {#activate-code-based-campaign}

定義程式碼型行銷活動並使用[程式碼型編輯器](#edit-code)視需要編輯內容後，您就可以檢閱並啟用它。 請遵循下列步驟。

>[!NOTE]
>
>您也可以在啟用行銷活動內容之前先預覽該內容。 [了解更多](#test-code-based-campaign)

1. 從您的程式碼型行銷活動中，選取&#x200B;**[!UICONTROL 檢閱以啟動]**。

   ![](assets/code-based-campaign-review.png)

1. 視需要檢查並編輯內容、屬性、表面、對象和排程。

1. 選取&#x200B;**[!UICONTROL 啟動]**。

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >按一下&#x200B;**[!UICONTROL 啟用]**&#x200B;後，最多可能需要1分鐘才能將程式碼型行銷活動變更即時顯示在您的位置。

您的程式碼型行銷活動會採用&#x200B;**[!UICONTROL 即時]**&#x200B;狀態，且現在對選取的對象可見。 行銷活動的每位收件者都能看到您的修改。

>[!NOTE]
>
>如果您為程式碼型行銷活動定義排程，在到達開始日期和時間之前，其狀態為&#x200B;**[!UICONTROL 已排程]**。
>
>如果您啟用程式碼型行銷活動，其影響的位置與另一個已上線的行銷活動相同，則所有變更將會套用至您的位置。

在[本節](../campaigns/review-activate-campaign.md)中進一步瞭解啟用行銷活動。

## 停止程式碼型行銷活動 {#stop-code-based-campaign}

程式碼型行銷活動上線時，您可以停止該活動，以防止對象看到您的修改。 請遵循下列步驟。

1. 從清單中選取即時行銷活動。

1. 從頂端功能表選取&#x200B;**[!UICONTROL 停止行銷活動]**。

   ![](assets/code-based-campaign-stop.png)

1. 您所定義的對象將看不到您所新增的修改。

>[!NOTE]
>
>程式碼型行銷活動停止後，您就無法再編輯或啟動它。 您只能複製該檔案並啟動複製的促銷活動。

## 程式碼型行銷活動報表

您可以從行銷活動摘要畫面存取程式碼型行銷活動報告。

全域報告會顯示至少兩小時前發生的事件，並涵蓋選定時段內的事件。 相較之下，即時報表著重於過去24小時內發生的事件，最短間隔為事件發生後的2分鐘。

### 程式碼型即時報告 {#live-report-code-based}

從您的行銷活動&#x200B;**[!UICONTROL 即時報告]**，**[!UICONTROL 程式碼型體驗]**&#x200B;索引標籤會詳細說明與您的應用程式或網頁相關的主要資訊。 [進一步瞭解即時報告](../reports/campaign-live-report.md)

+++進一步瞭解程式碼型體驗報表中可用的不同量度和Widget。

**[!UICONTROL 程式碼型體驗效能]** KPI詳細列出與訪客參與程式碼型體驗相關的主要資訊，例如：

* **[!UICONTROL 曝光次數]**：傳送給所有使用者的體驗總數。

* **[!UICONTROL 互動]**：與應用程式/頁面的互動總數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

**[!UICONTROL 程式碼型體驗摘要]**&#x200B;圖表顯示您過去24小時體驗（曝光數、不重複曝光數和互動數）的演變。

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.-->
+++

### 程式碼型全域報表 {#global-report-code-based}

您可以使用&#x200B;**[!UICONTROL 檢視報告]**&#x200B;按鈕，直接從行銷活動存取程式碼型行銷活動全域報告。 [進一步瞭解全域報告](../reports/campaign-global-report.md)

從您的行銷活動&#x200B;**[!UICONTROL 全域報告]**，**[!UICONTROL 程式碼型體驗]**&#x200B;索引標籤會詳細說明與您的應用程式或網頁相關的主要資訊。

![](assets/code-based-campaign-global-report.png)

<!--image-->

+++進一步瞭解程式碼型體驗報表中可用的不同量度和Widget。

**[!UICONTROL 程式碼型體驗效能]** KPI會詳細說明與訪客與您的體驗互動相關的主要資訊，例如：

* **[!UICONTROL 不重複曝光次數]**：提供體驗的不重複使用者人數。

* **[!UICONTROL 曝光次數]**：傳送給所有使用者的體驗總數。

* **[!UICONTROL 互動]**：與您的應用程式/頁面互動的百分比。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

**[!UICONTROL 程式碼型體驗摘要]**&#x200B;圖表會顯示您在此期間體驗（不重複曝光次數、曝光次數和互動）的演變。

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.-->
+++

<!--
## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
