---
solution: Journey Optimizer
product: journey optimizer
title: 建立忠誠度挑戰
description: 瞭解如何在Adobe Journey Optimizer中建立和設定忠誠度挑戰。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人測試版" type="Informative"
mini-toc-levels: 1
exl-id: c950bee8-4ea9-4b64-810d-91371e8b3e4c
source-git-commit: 89e1348a98596b8ecefabab571d2c1af299f1ed8
workflow-type: tm+mt
source-wordcount: '1807'
ht-degree: 1%

---

# 創造挑戰 {#create-challenges}

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* [開始應對忠誠度挑戰](get-started.md)
* [存取及管理挑戰與工作](access-loyalty-challenges.md)
* **建立挑戰** ◀︎**您在這裡**
* [建立任務](create-tasks.md)
* [忠誠度挑戰API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges/){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](../rn/releases.md)。

本頁涵蓋建立忠誠度挑戰的完整流程，從選取挑戰型別和設定其屬性，到產生和發佈將為客戶提供挑戰的歷程。

## 建立挑戰 {#create-the-challenge}

1. 在Journey Optimizer中導覽至&#x200B;**[!UICONTROL 忠誠度挑戰(Beta)]**。

1. 選取&#x200B;**[!UICONTROL 挑戰]**&#x200B;標籤，並選取&#x200B;**[!UICONTROL 建立挑戰]**。

   ![](assets/challenge-create.png)

1. 選擇挑戰型別：

   * **[!UICONTROL 標準]**：客戶以任何順序完成任何指定數量的工作\
     *範例：完成5個可用工作中的3個*

   * **[!UICONTROL 連續執行]**：客戶連續多次完成相同的工作\
     *範例：連續7天購買*

   * **[!UICONTROL 循序]**：客戶以定義的順序完成工作\
     *範例： Purchase → Review → Share （必須依此順序完成）*

   選擇挑戰型別後，挑戰建立介面會開啟，其中包含多個設定標籤。 從設定挑戰結構開始。

## 設定挑戰結構 {#structure}

在&#x200B;**[!UICONTROL 結構]**&#x200B;索引標籤中，定義挑戰的組織方式：其屬性、排程、要完成的任務以及要傳送的獎勵。

### 定義挑戰屬性並使用自訂中繼資料 {#properties}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_properties"
>title="挑戰屬性"
>abstract="在「挑戰屬性」窗格中，設定挑戰名稱和說明，並新增自訂索引鍵/值中繼資料以追蹤或外部整合。"

1. 在&#x200B;**[!UICONTROL 挑戰內容]**&#x200B;窗格中，定義挑戰的全域設定：

   * **[!UICONTROL 名稱]**：輸入質詢的描述性名稱。 此名稱會出現在挑戰清單中。
   * **[!UICONTROL 說明]**：輸入說明挑戰目的和目標的說明。

1. 使用&#x200B;**[!UICONTROL 自訂中繼資料]**&#x200B;區段，以使用索引鍵/值配對來新增自訂中繼資料。 此中繼資料可用於追蹤或與外部系統整合。

   ![](assets/challenge-create-properties.png)

### 排程挑戰 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_schedule"
>title="挑戰排程"
>abstract="使用排程來定義挑戰何時上線：設定客戶可以使用挑戰的開始日期和時間，以及停止接受完工的結束日期和時間。 請挑選時區，並選擇客戶何時可以在&#x200B;**[!UICONTROL 任務完成視窗區段]**&#x200B;中完成任務。"

設定您的挑戰執行時間：

1. 選取&#x200B;**[!UICONTROL 開啟排程]**&#x200B;圖示：

   ![](assets/challenge-create-schedule.png)

1. 設定下列排程選項：

   * **[!UICONTROL 開始日期和時間]**：設定客戶何時可提出挑戰。
   * **[!UICONTROL 結束日期和時間]**：設定質詢過期且不再接受新完成的時間。
   * **[!UICONTROL 時區]**：挑戰預設使用收件者的當地時區。
   * **[!UICONTROL 任務必須完成]**：選擇客戶何時可以完成任務：

      * **[!UICONTROL 在挑戰期間的任何時間]**：客戶可以在挑戰開始與結束日期之間的任何時間完成任務。
      * **[!UICONTROL 在一天中的特定小時內]**：設定&#x200B;**[!UICONTROL 開始時間]**&#x200B;和&#x200B;**[!UICONTROL 結束時間]**，將工作完成限制在特定每日小時內。

挑戰排程現在已設定。 接下來，新增客戶需要完成的工作。

### 新增任務 {#add-tasks}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_tasks"
>title="任務"
>abstract="選取要執行的工作以完成挑戰。 接下來，設定完成挑戰的方式 — 可用選項取決於您的挑戰型別（標準、連續或循序）。"

任務定義客戶要獲得獎勵必須完成的特定操作。 您可以設定任務型別（購買、支出）、數量、產品篩選器和其他屬性。

若要新增任務至您的挑戰，請遵循下列步驟：

1. 在&#x200B;**[!UICONTROL 工作]**&#x200B;區段中，選取&#x200B;**[!UICONTROL 新增工作]**。

   ![](assets/challenge-create-add-task.png)

1. **[!UICONTROL 任務詳細目錄]**&#x200B;已開啟。 從清單中選取一或多個工作，然後選取&#x200B;**[!UICONTROL 新增]**。 若要建立新工作，請選取&#x200B;**[!UICONTROL 新增]**。 [瞭解如何建立及設定工作](create-tasks.md)。

1. 指定將挑戰視為已完成的時間。 可用的設定取決於挑戰型別：

   +++標準挑戰

   在&#x200B;**[!UICONTROL 工作完成需求]**&#x200B;下拉式清單中，選擇下列專案：

   * **[!UICONTROL 客戶選擇1項工作完成]** - *客戶可以選擇並完成任何單一工作以獲得獎勵*
   * **[!UICONTROL 客戶完成特定數量的工作]** - *客戶必須完成已定義的數量工作。 指定要完成的工作所需數目。*

   +++

   +++Streak挑戰

   在&#x200B;**[!UICONTROL Streak型別]**&#x200B;下拉式清單中，選擇下列專案：

   * **連續**：客戶必須在連續幾天不間斷地完成工作。 *範例：星期一、星期二、星期三的購買 — 錯過一天就中斷連線。*

   * **非連續**：客戶可以在完成之間有間隔的情況下完成工作。 *範例：在30天內完成7次購買，允許中斷。*

   在&#x200B;**[!UICONTROL 條紋長度]**&#x200B;欄位中，指定任務必須完成的次數。 *範例：針對「7天購買連結」設定為7。*

   +++

   +++循序挑戰

   在&#x200B;**[!UICONTROL 工作完成需求]**&#x200B;下拉式清單中，選擇下列專案：

   * **[!UICONTROL 客戶選擇1項工作完成]** - *客戶可以選擇並完成任何單一工作以獲得獎勵*
   * **[!UICONTROL 客戶完成特定數量的工作]** - *客戶必須依照您定義的確切順序完成已定義數量的工作。 遺失或略過任務會中斷順序。 指定要完成的工作所需數目*

   +++

1. 依預設，標準和循序挑戰可讓客戶跨多個交易完成任務。 若要在單一交易中要求完成所有工作，請選取&#x200B;**[!UICONTROL 設定]**&#x200B;圖示並開啟下方的選項。

   ![](assets/challenge-create-single-transaction.png)

將任務新增至挑戰後，請設定客戶完成任務即可獲得的獎勵。

### 設定獎勵 {#rewards}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_rewards"
>title="獎勵"
>abstract="選擇客戶獲得點數的時間：完成整個挑戰的時間，或是在任務里程碑進行時。 選取您的獎勵提供者（管理點數和獎勵的忠誠度解決方案），然後設定金額：完整完成的單一總計，或里程碑的每一項任務值，僅針對您要支付的任務啟用獎勵。"

獎勵是客戶在完成挑戰時獲得的忠誠度點數或權益。

若要設定何時及如何提供獎勵：

1. 在&#x200B;**[!UICONTROL 獎勵傳遞]**&#x200B;下拉式功能表中，選擇何時傳遞獎勵：

   * **[!UICONTROL 當挑戰完成時提供獎勵]**：當客戶完成整個挑戰時提供獎勵\
     *範例：完成全部5項工作後獲得100分*

   * **[!UICONTROL 當挑戰進度完成時，在任務完成里程碑提供獎勵]**：當客戶完成個別任務時，獎勵會遞增（僅適用於需要多個任務的挑戰）\
     *範例：在任務1後獎勵10分，在任務2後獎勵20分，在任務3後獎勵50分*

1. 選取您的獎勵提供者。 這是管理客戶點數和獎勵的忠誠度解決方案。

   ![](assets/challenge-create-reward-type.png)

1. 根據您選取的傳送方式設定獎勵金額：

   +++完成挑戰時提供獎勵

   指定當客戶完成整個挑戰時所要給予的總獎勵金額。

   *在下列範例中，完成挑戰時，客戶會獲得100分。*

   ![](assets/challenge-create-reward-total.png)

   +++

   +++在任務完成里程碑時傳遞獎勵

   指定任務完成里程碑的獎勵金額。 此選項可讓您建立漸進式獎勵，當客戶完成挑戰時提高他們的積極性。

   對於您想要提供獎勵的任何工作，請切換獎勵選項，並指定當客戶完成該特定工作時要獎勵多少分。 您可以選擇僅獎勵特定任務完成 — 例如，如果您有10個任務，則可能僅獎勵任務1、5和10。

   *在下列範例中，客戶完成第一個任務時會獲得10分，完成第二個任務後會再獲得50分。*

   ![](assets/challenge-create-reward-milestones.png)

   +++

在設定包含任務和獎勵的挑戰結構後，設計內容卡以向客戶顯示挑戰。

## 設定內容卡片 {#configure-content-cards}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_content"
>title="內容"
>abstract="設定內容卡，代表您在客戶裝置上的挑戰，並顯示挑戰資訊、進度和獎勵。 輸入卡片名稱，選取通道設定，讓傳送使用正確的技術設定（例如標題、子網域或行動應用程式），然後選取「編輯內容」以設計和個人化卡片體驗。"

內容卡以視覺化方式呈現您在客戶裝置上的挑戰，顯示挑戰資訊、進度和獎勵。 [進一步瞭解內容卡](../content-card/create-content-card.md)。

若要設定挑戰的內容卡：

1. 導覽至&#x200B;**[!UICONTROL Content]**&#x200B;標籤，然後輸入內容卡的&#x200B;**[!UICONTROL 名稱]**。

1. 選取&#x200B;**[!UICONTROL 通道設定]**。 管道設定包含所有用於傳送訊息的技術引數，例如標頭引數、子網域、行動應用程式等。 [進一步瞭解通道設定](../configuration/channel-surfaces.md)。

1. 選取&#x200B;**[!UICONTROL 編輯內容]**&#x200B;以設計您的內容卡。 [瞭解如何設計和個人化內容卡](../content-card/design-content-card.md)。

   ![](assets/challenge-create-content.png)

設定內容卡後，設定訊息以在挑戰生命週期中吸引客戶。

### 設定傳訊 {#configure-messaging}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_messaging"
>title="傳訊"
>abstract="傳送訊息有助於在挑戰生命週期中進行參與。 在「訊息」標籤上，為每個階段新增訊息：啟動（挑戰開始時）、進行中（提醒和進度更新）以及完成（慶祝成功並確認獎勵）。 對於每個階段，新增訊息、選擇頻道、選取頻道設定，然後選取「編輯」以設計訊息內容。"

設定多管道訊息，在挑戰生命週期的關鍵階段與客戶互動。 傳訊功能為選用，但建議儘量擴大客戶參與度。

1. 導覽至&#x200B;**[!UICONTROL 傳訊]**&#x200B;標籤，並為每個生命週期階段設定訊息：

   * **啟動**&#x200B;訊息：當挑戰開始時通知客戶
   * **進行中**&#x200B;訊息：讓客戶持續參與提醒和進度更新
   * **完成**&#x200B;訊息：慶祝成功並確認獎勵配置

1. 對於每個階段，按一下新增訊息按鈕，以建立該階段的訊息。

1. 選擇您想要的頻道： **[!UICONTROL 應用程式內]**、**[!UICONTROL 電子郵件]**&#x200B;或&#x200B;**[!UICONTROL 推播通知]**，並選取相關的頻道設定。

1. 選取![](assets/do-not-localize/Smock_More_18_N.svg)圖示並選擇&#x200B;**[!UICONTROL 編輯]**&#x200B;來設計您的訊息內容。

   ![](assets/challenge-create-messaging.png)

在以下章節中瞭解如何建立特定頻道的訊息： [應用程式內訊息](../in-app/get-started-in-app.md) - [電子郵件訊息](../email/get-started-email.md) - [推播通知](../push/get-started-push.md)

完成訊息設定後，請定義哪些客戶有資格參與挑戰。

## 選取挑戰對象 {#audience}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenge_audience"
>title="客群"
>abstract="在「對象」標籤上，從可用的Adobe Experience Platform對象中選擇可以參與挑戰的對象。"

定義哪些客戶可參與您的忠誠度挑戰。

1. 導覽至&#x200B;**[!UICONTROL 對象]**&#x200B;標籤，然後按一下&#x200B;**[!UICONTROL 選取對象]**&#x200B;按鈕。

   ![](assets/challenge-create-audience.png)

1. 在對象選取對話方塊中，從可用的Adobe Experience Platform對象清單中選取您的目標對象，然後選取&#x200B;**[!UICONTROL 新增對象]**。 [瞭解如何使用對象](../audience/about-audiences.md)。

您的挑戰現在已完整設定結構、內容、訊息和目標對象。 若要啟動它，您必須發佈挑戰及其相關歷程。

## 發起挑戰 {#launch}

啟動挑戰需要&#x200B;**三個步驟**： (1)發佈挑戰、(2)產生歷程、(3)發佈歷程。 必須完成全部三個步驟，才能將挑戰傳遞給客戶。

1. 請檢閱您的挑戰設定，以確保所有必填欄位都已完成。

1. 按一下![](assets/do-not-localize/Smock_More_18_N.svg)圖示並選取&#x200B;**[!UICONTROL 發佈]**。

   ![](assets/challenge-create-publish.png)

1. 選取&#x200B;**[!UICONTROL 產生歷程]**&#x200B;以建立將協調您的挑戰傳遞的歷程。

   ![](assets/challenge-create-generate-journey.png)

1. Journey Optimizer會自動建立狀態為「草稿」的歷程。 歷程會以名稱格式&#x200B;*「歷程： [挑戰名稱]」*&#x200B;出現在您的歷程詳細目錄中。 [進一步瞭解歷程詳細目錄](../building-journeys/journey-ui.md)。

   ![](assets/challenge-create-journey.png)

1. 開啟歷程並發佈。 歷程將在您指定的挑戰開始日期自動開始，並根據您的設定傳送內容和訊息。 [瞭解如何發佈歷程](../building-journeys/publish-journey.md)。

1. 一旦您的挑戰上線，請在[歷程報告](../reports/journey-global-report-cja.md)中監視效能和訊息傳送。

>[!NOTE]
>
>可以自訂自動產生的歷程，以新增其他邏輯或訊息。 不過，直接對歷程進行的變更不會同步回挑戰設定。 如果您稍後編輯挑戰，則重新產生歷程時，所有歷程自訂都將遺失。
