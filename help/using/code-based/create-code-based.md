---
title: 建立程式碼型體驗
description: 瞭解如何在Journey Optimizer中建立程式碼型體驗
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 3c4aef3e062eb6a8b106ce00b86cd0594e94d7b0
workflow-type: tm+mt
source-wordcount: '1731'
ht-degree: 7%

---

# 建立程式碼型體驗 {#create-code-based}

在[!DNL Journey Optimizer]中，您可以在歷程或行銷活動中建立程式碼型體驗。

有關程式碼型體驗的特定護欄和建議，請參閱[此頁面](code-based-prerequisites.md)。

## 透過歷程或行銷活動新增程式碼型體驗 {#create-code-based-experience}

若要透過歷程或行銷活動開始建立程式碼型體驗，請遵循下列步驟。

>[!BEGINTABS]

>[!TAB 將程式碼型體驗新增至歷程]

若要將&#x200B;**程式碼型體驗**&#x200B;活動新增至歷程，請遵循下列步驟：

1. [建立歷程](../building-journeys/journey-gs.md)。

1. 以[事件](../building-journeys/general-events.md)或[讀取對象](../building-journeys/read-audience.md)活動來開始您的歷程。

1. 從浮動視窗的&#x200B;**[!UICONTROL 動作]**&#x200B;區段，拖放&#x200B;**[!UICONTROL 程式碼型體驗]**&#x200B;活動。

   ![](assets/code-based-activity-journey.png)

   >[!NOTE]
   >
   >由於&#x200B;**程式碼型體驗**&#x200B;是傳入訊息活動，因此會附帶3天&#x200B;**等待**&#x200B;活動。 [了解更多](../building-journeys/wait-activity.md#auto-wait-node)

1. 為您的訊息輸入&#x200B;**[!UICONTROL 標籤]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 選取或建立要使用的[程式碼型體驗組態](code-based-configuration.md)。

   ![](assets/code-based-activity-config.png)

1. 選取&#x200B;**[!UICONTROL 編輯內容]**&#x200B;按鈕，並使用個人化編輯器視需要編輯您的內容。 [了解更多](#edit-code)

1. 如有必要，請拖放其他動作或事件以完成您的歷程流程。 [了解更多](../building-journeys/about-journey-activities.md)

1. 一旦您的程式碼庫體驗準備就緒，請完成設定並發佈您的歷程以將其啟用。 [了解更多](../building-journeys/publishing-the-journey.md)

如需如何設定歷程的詳細資訊，請參閱[此頁面](../building-journeys/journey-gs.md)。

>[!TAB 建立以程式碼為主的體驗活動]

若要透過行銷活動開始建置您的&#x200B;**程式碼型體驗**，請遵循下列步驟。

1. 建立行銷活動。 [了解更多](../campaigns/create-campaign.md)

1. 選取您要執行的行銷活動型別

   * **[!UICONTROL 已排程 — 行銷]**：立即或在指定日期執行行銷活動。 已排程的行銷活動旨在傳送&#x200B;**行銷**&#x200B;訊息。 可從使用者介面設定及執行。

   * **[!UICONTROL API觸發 — 行銷/異動]**：使用API呼叫執行行銷活動。 API觸發的行銷活動旨在傳送&#x200B;**行銷**&#x200B;或&#x200B;**異動**&#x200B;訊息，即在個人執行動作後傳送的訊息：密碼重設、購物車購買等。 [瞭解如何使用API觸發行銷活動](../campaigns/api-triggered-campaigns.md)

1. 完成步驟以建立行銷活動，例如行銷活動屬性、[對象](../audience/about-audiences.md)和[排程](../campaigns/create-campaign.md#schedule)。 如需如何設定行銷活動的詳細資訊，請參閱[此頁面](../campaigns/get-started-with-campaigns.md)。

1. 選取&#x200B;**[!UICONTROL 程式碼型體驗]**&#x200B;動作。

1. 選取或建立程式碼型體驗設定。 [了解更多](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

1. 使用個人化編輯器，視需要編輯您的內容。 [了解更多](#edit-code)

   <!--![](assets/code-based-campaign-edit-content.png)-->

如需如何設定行銷活動的詳細資訊，請參閱[此頁面](../campaigns/get-started-with-campaigns.md)。

>[!ENDTABS]

## 編輯程式碼內容 {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="使用個人化編輯器"
>abstract="插入並編輯您想要作為此基於程式碼之體驗動作的一部分的程式碼。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions.html" text="開始使用個人化編輯器"

1. 在歷程活動或行銷活動版本畫面中，選取&#x200B;**[!UICONTROL 編輯代碼]**。

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

1. 使用程式碼型體驗時，您可以使用體驗決策功能。 從左側列選取&#x200B;**[!UICONTROL 決定原則]**&#x200B;圖示，然後按一下&#x200B;**[!UICONTROL 新增決定原則]**。 [了解更多](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >體驗決策目前僅可適用於一組組織 (可用性限制)。 若要取得存取權，請和您的 Adobe 代表聯絡。


1. 按一下&#x200B;**[!UICONTROL 儲存並關閉]**&#x200B;以確認您的變更。

現在，當您的開發人員進行API或SDK呼叫，擷取您管道設定中定義之表面的內容時，變更就會套用至您的網頁或應用程式。

## 測試程式碼型體驗 {#test-code-based-experience}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="預覽您的基於程式碼的體驗"
>abstract="模擬基於程式碼的體驗。"

若要顯示已修改程式碼型體驗的預覽，請遵循下列步驟。

>[!CAUTION]
>
>您必須有可用的測試設定檔，以模擬將傳送給他們的優惠。 瞭解如何[建立測試設定檔](../audience/creating-test-profiles.md)。

1. 在歷程或行銷活動中，從個人化編輯器或編輯內容畫面選取&#x200B;**[!UICONTROL 模擬內容]**。

   ![](assets/code-based-campaign-simulate.png)

1. 按一下&#x200B;**[!UICONTROL 管理測試設定檔]**&#x200B;以選取一或多個測試設定檔。

1. 畫面上會顯示已修改程式碼式體驗的預覽。

有關如何選取測試設定檔及預覽內容的詳細資訊，請參閱[本節](../content-management/preview.md)。

### 在裝置上預覽 {#preview-on-device}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device"
>title="在真實裝置上預覽您的程式碼型體驗"
>abstract="直接在您的瀏覽器或行動裝置上取得個人化體驗的預覽，以檢視它們在真實裝置上的外觀。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_web"
>title="在裝置上預覽您的程式碼式Web體驗"
>abstract="掃描QR碼或複製連結以在裝置上預覽。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_mobile"
>title="在裝置上預覽您的程式碼型行動體驗"
>abstract="掃描QR碼或複製連結以在裝置上預覽。 連線之後，請輸入裝置上的圖釘。 您可能需要重新啟動應用程式，才能在每次更新預覽連結時看到變更。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview_device_refresh"
>title="重新整理預覽連結以反映目前的檢視"
>abstract="裝置上預覽將顯示自您建立或重新整理預覽連結時起的內容。 如果您已修改內容或選取不同的測試設定檔或處理，請重新整理預覽，使其反映目前的檢視。"

為網頁或行動應用程式建立程式碼型體驗時，您可以直接在瀏覽器或行動裝置上預覽您的個人化體驗，以瞭解這些體驗在真實裝置上的外觀。

>[!WARNING]
>
>使用[決定原則](../experience-decisioning/create-decision.md)或[個人化](../personalization/personalization-build-expressions.md)內容屬性時，裝置上的預覽無法使用。

1. 在&#x200B;**[!UICONTROL 模擬]**&#x200B;畫面中，按一下&#x200B;**[!UICONTROL 開啟預覽選項]**&#x200B;按鈕。 預覽選項視您在[程式碼型組態](code-based-configuration.md#create-code-based-configuration)中選取的平台而定。

1. 如果您在程式碼型組態中使用[Web平台](code-based-configuration.md#web)，**[!UICONTROL 裝置預覽URL]**&#x200B;唯讀欄位會預先填入為目前頻道組態輸入的URL。

   ![](assets/preview-on-device-web.png)

   您可以：

   * 選取&#x200B;**[!UICONTROL 複製連結]**&#x200B;按鈕，然後將連結貼到瀏覽器索引標籤中。 您也可以與您的團隊和利害關係人共用連結，這些利害關係人可以在變更上線之前，在任何瀏覽器中預覽新體驗。

   * 按一下&#x200B;**[!UICONTROL 在新標籤中開啟]**，以在您目前的瀏覽器中開啟連結。

   * 使用行動裝置掃描二維碼，在行動瀏覽器上開啟預覽連結。

1. 如果您在程式碼型組態中使用[行動平台](code-based-configuration.md#mobile) (iOS / Android)，**[!UICONTROL Deeplink]**&#x200B;唯讀欄位會預先填入在所選平台的頻道組態中輸入的&#x200B;**[!UICONTROL 預覽URL]**&#x200B;值。

   在&#x200B;**[!UICONTROL iOS]**&#x200B;和&#x200B;**[!DNL Android]**&#x200B;標籤之間切換，以預覽您所選平台的體驗。

   ![](assets/preview-on-device-mobile.png)

   您可以：

   * 選取&#x200B;**[!UICONTROL 複製連結]**&#x200B;按鈕，並與您的團隊和利害關係人共用連結，他們可以在變更上線之前，在任何行動瀏覽器中預覽新體驗。

   * 使用行動裝置掃描二維碼，以直接在行動應用程式中開啟預覽連結。 您必須在裝置上輸入PIN，才能建立[Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/implement-assurance){target="_blank"}工作階段。

     >[!NOTE]
     >
     >**Adobe Experience Platform Assurance**&#x200B;是Adobe Experience Cloud的產品，可協助您檢查、校樣、模擬及驗證如何在行動應用程式中收集資料或提供體驗。 [了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/assurance/home){target="_blank"}

1. 已針對選取的測試設定檔產生預覽連結，如果您在歷程或行銷活動中使用[內容實驗](../content-management/content-experiment.md)，則會針對選取的處理方式產生預覽連結。

   <!--If you have modified the content or selected a different treatment or test profile, scroll down to the bottom of the **[!UICONTROL Preview on device]** pop-up and click **[!UICONTROL Refresh preview link]** to reflect the current state.

   ![](assets/preview-on-device-refresh.png)-->

   <!--When creating a content experiment, you need to select a given treatment and click the **[!UICONTROL Simulate content]** button to obtain the link corresponding to that treatment, then select another treatment, click the **[!UICONTROL Simulate content]** button to obtain a new preview link, and so on.-->

   當更新內容或選取不同的測試設定檔或處理方式時，預覽連結會自動重新整理。 您可以將連結複製到不同的瀏覽器標籤中，並比較體驗。

## 讓您的程式碼型體驗上線 {#code-based-experience-live}

>[!IMPORTANT]
>
>從9月版本開始，全新的行銷活動和歷程啟用體驗可讓您管理整個核准流程，確保行銷活動和歷程在投入使用前皆由適當的利害關係人徹底審查和核准。 此功能在「有限可用性」中提供。 [了解更多](../test-approve/gs-approval.md)

定義程式碼型體驗並使用[程式碼型編輯器](#edit-code)視需要編輯內容後，您就可以啟用歷程或行銷活動，讓您的變更對對象可見。

您也可以在讓程式碼型體驗內容上線之前，先預覽該內容。 [了解更多](#test-code-based-experience)

>[!NOTE]
>
>如果您啟用程式碼型歷程/行銷活動，將影響與另一個已上線的歷程或行銷活動相同的頁面，則所有變更將會套用至您的內容。
>
>如果有多個程式碼型歷程或行銷活動更新內容的相同元素，則會以最高優先順序的歷程/行銷活動優先。

您的程式碼型歷程或行銷活動上線後，應用程式實作團隊將負責發出明確API或SDK呼叫，以擷取所選[程式碼型體驗設定](code-based-configuration.md)中定義之表面的內容。 在[本節](code-based-implementation-samples.md)中瞭解不同客戶實作的詳細資訊。

### Publish程式碼型歷程 {#publish-code-based-journey}

若要讓您的程式碼型體驗在歷程中上線，請遵循下列步驟。

1. 確認您的歷程有效且沒有錯誤。 [了解更多](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)

1. 在歷程中，選取位於右上角下拉式功能表中的&#x200B;**[!UICONTROL Publish]**&#x200B;選項。

   ![](assets/code-based-journey-publish.png)

   >[!NOTE]
   >
   >在[本節](../building-journeys/publishing-the-journey.md)中進一步瞭解發佈歷程。

您的程式碼型歷程會採用&#x200B;**[!UICONTROL 即時]**&#x200B;狀態，現在選定對象可看見。 您歷程的每個收件者都能看到您的修改。

>[!NOTE]
>
>按一下&#x200B;**[!UICONTROL Publish]**&#x200B;後，最多可能需要15分鐘才能讓變更上線。

### 啟用程式碼型行銷活動 {#activate-code-based-campaign}

1. 從您的程式碼型行銷活動中，選取&#x200B;**[!UICONTROL 檢閱以啟動]**。

   ![](assets/code-based-campaign-review.png)

1. 視需要檢查並編輯內容、屬性、設定、對象和排程。

1. 選取&#x200B;**[!UICONTROL 啟動]**。

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >在[本節](../campaigns/review-activate-campaign.md)中進一步瞭解啟用行銷活動。

您的程式碼型行銷活動會採用&#x200B;**[!UICONTROL 即時]**&#x200B;狀態，且現在對選取的對象可見。 行銷活動的每位收件者都能看到您新增至內容的修改。

>[!NOTE]
>
>按一下[啟動&#x200B;****]後，最多可能需要15分鐘才能讓您的變更上線。
>
>如果您為程式碼型行銷活動定義排程，在到達開始日期和時間之前，其狀態為&#x200B;**[!UICONTROL 已排程]**。

## 停止程式碼型歷程或行銷活動 {#stop-code-based-experience}

程式碼式體驗上線時，您可以停止該體驗，以防止對象看到您的修改。 請遵循下列步驟。

1. 從個別清單中選取即時歷程或行銷活動。

1. 根據您的情況執行相關動作：

   * 從行銷活動頂端功能表，選取&#x200B;**[!UICONTROL 停止行銷活動]**。

     ![](assets/code-based-campaign-stop.png)

   * 從歷程頂端功能表，按一下&#x200B;**[!UICONTROL 更多]**&#x200B;按鈕，然後選取&#x200B;**[!UICONTROL 停止]**。

     ![](assets/code-based-journey-stop.png)

1. 您所定義的對象將看不到您所新增的修改。

>[!NOTE]
>
>一旦程式碼型歷程或行銷活動停止，您就無法再次編輯或啟動它。 您只能複製它並啟動複製的歷程/行銷活動。

<!--Reporting TBC

## Check the code-based experience reports {#check-code-based-reports}

Once your code-based experience is live, you can check the **[!UICONTROL Code-based]** tab of the  [Journey report](../reports/journey-global-report-cja.md#web-cja) and [Campaign report](../reports/campaign-global-report-cja.md#web) to compare elements such as the number of experiences delivered to your audience, and the number of engagements with your content.-->

<!--## Code-based reports

You can access code-based journey or campaign reports from the summary screen.

Global reports display events that occurred at least two hours ago and cover events over a selected time period. In comparison, Live reports focus on events that took place within the past 24 hours, with a minimum time interval of two minutes from the event occurrence.

### Code-based live report {#live-report-code-based}

From your campaign **[!UICONTROL Live report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages. [Learn more on live report](../reports/campaign-live-report.md)

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your code-based experiences, such as:

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**:  total number of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (impressions, unique impressions and interactions) for the last 24 hours.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.
+++

### Code-based global report {#global-report-code-based}

Code-based campaign global report can be accessed directly from your journey or campaign with the **[!UICONTROL View report]** button. [Learn more on global report](../reports/campaign-global-report.md)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages.

![](assets/code-based-campaign-global-report.png)

Add image TBC

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your experiences, such as:

* **[!UICONTROL Unique impressions]**: number of unique users to whom the experience was delivered.

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**: percentage of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (unique impressions, impressions and interactions) for the concerned period.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.
+++

TBC video if existing

## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
