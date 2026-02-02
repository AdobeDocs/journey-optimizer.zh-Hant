---
title: 建立決定原則
description: 瞭解如何建立決定原則
feature: Decisioning
topic: Integrations
role: User
level: Experienced
version: Journey Orchestration
source-git-commit: 2dfc9c2db5af1b9b74f7405a68e85563f633a54f
workflow-type: tm+mt
source-wordcount: '2108'
ht-degree: 6%

---


# 建立決定原則 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="定義要傳回的項目數量"
>abstract="選取您想要傳回的決定項目數量。例如，如果您選取 2，則目前設定將顯示最佳的 2 個符合資格的產品建議。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="選取遞補"
>abstract="當為該決定原則定義的所有選擇策略都不合格時，會向使用者顯示遞補項目。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="什麼是策略？"
>abstract="選擇策略的順序決定了先評估哪個策略。至少需要一個策略。組合策略中的決定項目將一起評估。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="建立策略"

若要向客戶呈現最佳的動態優惠和體驗，請將決定原則新增至行銷活動或歷程中的內容，然後設定要傳回的專案及要使用的選擇策略。 要執行此操作，請遵循下列步驟：

1. [新增決定原則](#add)
1. [設定決定原則](#configure) — 新增名稱並指定電子郵件通道要傳回的專案數。
1. [設定策略順序](#strategy) — 選取要連同決定原則一起傳回的專案。
1. [選取遞補優惠](#fallback) （選擇性） — 選取若無合格專案或選取策略，要顯示的專案。
1. [檢閱並儲存](#review)選取策略
1. [指派位置](#placement) （電子郵件頻道）

>[!AVAILABILITY]
>
>決定原則適用於&#x200B;**程式碼型體驗**、**推播通知**&#x200B;和SMS頻道的所有客戶。
>
>電子郵件通道的決策功能在「有限可用性」中提供。 若要要求存取權，請聯絡您的Adobe代表。 深入瞭解[可用性標籤](../rn/releases.md#availability-labels)。

## 新增決定原則 {#add}

若要在您的訊息中新增決定原則，請開啟歷程或行銷活動，然後選取[頻道動作](../building-journeys/journeys-message.md)。

編輯訊息內容並瀏覽以下標籤，瞭解如何根據所選頻道新增決定原則的更多資訊。

>[!BEGINTABS]

>[!TAB 程式碼型體驗]

針對程式碼型體驗，您可以使用&#x200B;**程式碼編輯器**&#x200B;或屬性窗格中可用的&#x200B;**決策**&#x200B;功能表來新增決定原則。

+++從程式碼編輯器新增決定原則

1. 使用&#x200B;**[!UICONTROL 編輯程式碼]**&#x200B;按鈕開啟程式碼編輯器。

1. 瀏覽至&#x200B;**[!UICONTROL 決定原則]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 新增決定原則]**&#x200B;按鈕。

   ![](assets/decision-policy-add-code-editor.png)

+++

+++從決定功能表新增決定原則

1. 按一下屬性窗格中的![](assets/do-no-localize/decisioning-icon.png)圖示以存取&#x200B;**[!UICONTROL 決策]**&#x200B;功能表。

1. 按一下&#x200B;**[!UICONTROL 新增決定原則]**&#x200B;按鈕。

   ![](assets/decision-policy-add-code.png)

+++

>[!TAB 電子郵件]

1. 切換&#x200B;**[!UICONTROL 啟用決策]**&#x200B;選項。

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >啟用決策功能會清除現有的電子郵件內容。 如果您已設計電子郵件，請務必預先將內容儲存為範本。

1. 使用電子郵件設計工具中可用的&#x200B;**個人化編輯器**&#x200B;或&#x200B;**決策**&#x200B;功能表，新增新的決定原則。

   +++從Personalization編輯器新增決定原則

   1. 使用主旨行欄位或電子郵件內文中可新增個人化的任何欄位中可用的![](assets/do-no-localize/editor-icon.svg)圖示，開啟個人化編輯器。

   1. 瀏覽至&#x200B;**[!UICONTROL 決定原則]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 新增決定原則]**&#x200B;按鈕。

      ![](assets/decision-policy-add-email-editor.png)

   +++

   +++從決定功能表新增決定原則

   1. 開啟電子郵件Designer並選取電子郵件結構中的任何元件。

   1. 按一下屬性窗格中的![](assets/do-no-localize/decisioning-icon.png)圖示以存取&#x200B;**[!UICONTROL 決策]**&#x200B;功能表。

   1. 按一下&#x200B;**[!UICONTROL 新增原則]**&#x200B;按鈕。

      ![](assets/decision-policy-add-email-add.png)

   >[!NOTE]
   >
   >**[!UICONTROL 重複使用決定輸出]**&#x200B;可讓您重複使用已在此電子郵件中建立的決定原則。

>[!TAB 簡訊]

對於SMS，您可以使用&#x200B;**個人化編輯器**&#x200B;或屬性窗格中可用的&#x200B;**決策**&#x200B;選單來新增決定原則。

+++從個人化編輯器新增決定原則

1. 使用![](assets/do-no-localize/editor-icon.svg)圖示開啟個人化編輯器。
1. 瀏覽至&#x200B;**[!UICONTROL 決定原則]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 新增決定原則]**&#x200B;按鈕。

   ![](assets/decision-policy-add-sms-editor.png)

+++

+++從決定功能表新增決定原則

1. 按一下屬性窗格中的![](assets/do-no-localize/decisioning-icon.png)圖示以存取&#x200B;**[!UICONTROL 決策]**&#x200B;功能表。

1. 按一下&#x200B;**[!UICONTROL 新增決定原則]**&#x200B;按鈕。

   ![](assets/decision-policy-add-sms.png)

>[!TAB 推播通知]

對於推播通知，您可以使用&#x200B;**個人化編輯器**&#x200B;或屬性窗格中可用的&#x200B;**決策**&#x200B;選單來新增決定原則。

+++從個人化編輯器新增決定原則

1. 使用![](assets/do-no-localize/editor-icon.svg)圖示開啟個人化編輯器。
1. 瀏覽至&#x200B;**[!UICONTROL 決定原則]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 新增決定原則]**&#x200B;按鈕。

   ![](assets/decision-policy-add-push.png)

+++

+++從決定功能表新增決定原則

1. 按一下屬性窗格中的![](assets/do-no-localize/decisioning-icon.png)圖示以存取&#x200B;**[!UICONTROL 決策]**&#x200B;功能表。

1. 按一下&#x200B;**[!UICONTROL 新增決定原則]**&#x200B;按鈕。

   ![](assets/decision-policy-add-push-menu.png)

>[!IMPORTANT]
>
>具有推播通知的Experience Decisioning需要特定版本的Mobile SDK。 在實作此功能之前，請檢查[發行說明](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}以識別所需的版本，並確定您已相應地升級。 您也可以在[本節](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}中檢視您平台的所有可用SDK版本。

>[!ENDTABS]

## 設定決定原則 {#configure}

將新的決定原則新增至內容後，決定原則設定畫面會隨即開啟。 請依照以下步驟設定決定原則：

1. 提供決定原則的名稱，並選取目錄（目前僅限於預設的&#x200B;**[!UICONTROL 優惠]**&#x200B;目錄）。

   ![](assets/decision-code-based-details.png)

1. **[!UICONTROL 專案數]**&#x200B;欄位可讓您定義要連同決定原則一起傳回的決定專案數。 例如，如果您選取 2，則目前設定將顯示最佳的 2 個符合資格的產品建議。

   >[!NOTE]
   >
   >此選項僅適用於電子郵件和程式碼型體驗管道。 對於所有其他管道，每個動作只能傳回1個決定專案。

   若要傳回電子郵件通道的多個專案，您必須在&#x200B;**[!UICONTROL 重複網格]**&#x200B;元件中新增決定原則。 展開下列區段以取得詳細資訊：

   +++在電子郵件中傳回多個決定專案

   1. 拖曳電子郵件中的&#x200B;**[!UICONTROL 重複網格]**&#x200B;元件，並使用&#x200B;**[!UICONTROL 設定]**&#x200B;窗格視需要加以設定。

      ![](assets/decision-policy-repeat.png)

   1. 按一下畫布工具列中的&#x200B;**[!UICONTROL 決策]**&#x200B;圖示，或開啟&#x200B;**[!UICONTROL 決策]**&#x200B;窗格並選取&#x200B;**[!UICONTROL 新增決策原則]**。

   1. 在&#x200B;**[!UICONTROL 專案數]**&#x200B;欄位中指定要傳回的專案數，然後設定決定原則，如下所述。 您可以選取的專案數目上限受&#x200B;**[!UICONTROL 重複網格]**&#x200B;元件中定義的圖磚數目限制。

   ![](assets/decision-policy-repeat-number.png)

   +++

1. 按一下&#x200B;**[!UICONTROL 下一步]**。

## 設定策略順序 {#strategy}

**[!UICONTROL 策略順序]**&#x200B;區段可讓您選取決定專案，並設定要與決定原則一起呈現的選擇策略。

1. 按一下&#x200B;**[!UICONTROL 新增]**，然後選擇要包含在原則中的物件型別：

   ![](assets/decision-code-based-strategy-sequence.png)

   * **[!UICONTROL 選擇策略]** — 決定策略會運用與適用性限制和排名方法相關的集合來決定要顯示的專案。 您可以選取一或多個現有的選取策略，或使用&#x200B;**[!UICONTROL 建立選取策略]**&#x200B;按鈕建立新的選取策略。 [瞭解如何建立選擇策略](selection-strategies.md)

   * **[!UICONTROL 決定專案]** — 選取單一決定專案，而不需執行選取策略。 您一次只能選取一個決定專案。 任何針對專案設定的適用性限制都會套用。

   >[!NOTE]
   >
   >決策原則可支援最多10個合併的選擇策略和決策專案。 [進一步瞭解Decisioning護欄和限制](gs-experience-decisioning.md#guardrails)

1. 新增多個決定專案和/或策略時，將會以特定順序評估它們。 將先評估新增至序列的第一個物件，依此類推。 若要變更預設順序，請拖放物件和/或群組以視需要重新排序。 展開下列區段以取得詳細資訊。

   +++管理決定原則中的評估順序

   將決定專案和選取策略新增到原則之後，您可以安排它們的順序以決定它們的評估順序，並將選取策略組合在一起以一起評估。

   每個物件或物件群組左邊會以數字表示要評估專案與策略的&#x200B;**循序順序**。 若要在序列中移動選取策略（或一組策略）的位置，請將其拖放到另一個位置。

   ![](assets/decision-code-based-strategy-groups.png)

   >[!NOTE]
   >
   >在序列中只能拖放選取策略。 若要變更決定專案的位置，您必須移除它，並在新增您之前要評估的其他專案之後，使用&#x200B;**[!UICONTROL 新增]**&#x200B;按鈕將其重新新增。

   您也可以&#x200B;**將**&#x200B;多個選取策略組合成群組，以便一起評估而不是分別評估。 若要這麼做，請按一下選取策略下方的&#x200B;**`+`**&#x200B;按鈕，將其與另一個策略結合。 您也可以將選取策略拖放至另一個策略上，將兩個策略組成群組。

   >[!NOTE]
   >
   >決策專案無法與其他專案或選取策略一起分組。

   多個策略及其分組決定策略的優先順序以及合格優惠的排名。 第一個策略具有最高優先順序，且在相同群組內合併的策略具有相同優先順序。

   例如，您有兩個集合，一個在策略A中，另一個在策略B中。此請求是為了傳回兩個決定專案。 假設有兩個來自策略A的合格優惠方案和三個來自策略B的合格優惠方案。

   * 如果兩個策略&#x200B;**未合併**&#x200B;或依序順序（1和2），則第一列中會傳回第一個策略中前兩個符合資格的優惠。 如果第一個策略沒有兩個符合資格的優惠，決定引擎會依序移至下一個策略，以找出仍需要多少優惠方案，最終在需要時傳回遞補。

     ![](assets/decision-code-based-consecutive-strategies.png)

   * 如果兩個集合約時進行&#x200B;**評估**，因為有來自策略A的兩個合格優惠和來自策略B的三個合格優惠，這五個優惠都將根據各自排名方法決定的值棧疊在一起。 已要求兩個優惠方案，因此將傳回這五個優惠方案中的前兩個合格優惠方案。

     ![](assets/decision-code-based-combined-strategies.png)

   具有多個策略的&#x200B;**範例**

   現在，讓我們舉一個例子，您有劃分為不同群組的多個策略。 您定義了三種策略。 策略1和策略2在群組1中結合，而策略3是獨立的（群組2）。 每個策略的合格優惠方案及其優先順序（用於排名函式評估）如下：

   * 群組1：
      * 策略1 - （選件1、選件2、選件3） — 優先順序1
      * 策略2 - （選件3、選件4、選件5） — 優先順序1

   * 群組2：
      * 策略3 - （選件5、選件6） — 優先順序0

   系統會先評估最高優先順序的策略選件，並將其新增至排名選件清單。

   * **反複專案1：**

     策略1和策略2選件會一起評估（選件1、選件2、選件3、選件4、選件5）。 假設結果為：

     選件1 - 10
選件2 - 20
策略1的優惠3 - 30，策略2的優惠45。 兩者中的最高會納入考量，因此會考慮45。
選件4 - 40
選件5 - 50

     排名優惠方案現在如下：優惠方案5、優惠方案3、優惠方案4、優惠方案2、優惠方案1。

   * **反複專案2：**

     已評估策略3選件（選件5、選件6）。 假設結果為：

      * 選件5 — 將不進行評估，因為它已存在於上述結果中。
      * 選件6 - 60

     排名優惠方案現在如下：優惠方案5 、優惠方案3、優惠方案4、優惠方案2、優惠方案1、優惠方案6。

   +++

1. 當您的選取策略準備就緒時，請按一下[下一步] **&#x200B;**。

## 新增遞補優惠 {#fallback}

選取決定專案和/或選取策略後，如果上述專案或選取策略皆不合格，您可以新增遞補優惠以顯示。

您可以從清單中選取任何專案，這會顯示在目前沙箱上建立的所有決定專案。 如果沒有合格的選取策略，則無論套用至所選專案<!--nor frequency capping when available - TO CLARIFY-->的日期和適用性限制，都會對使用者顯示遞補。

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> 遞補內容為選用。 最多可以選取請求的專案數。 如果沒有符合資格且未設定遞補內容，則不會顯示任何內容。

## 檢閱並儲存決定原則 {#review}

設定選擇策略並新增遞補優惠後，按一下[下一步] **[!UICONTROL 以檢閱並儲存您的決定原則，然後按一下[建立]]**&#x200B;以確認建立原則。**&#x200B;**

>[!IMPORTANT]
>
>建立決定原則後，對其所做的任何變更最多可能需要15分鐘才能傳播到所有資料區域，而加拿大最多可能需要30分鐘。 這包括變更，例如將新的決定專案新增至集合、變更專案中的規則、變更專案內容或更新公式。

您可以隨時使用個人化編輯器中的省略符號按鈕，或元件屬性窗格中的&#x200B;**[!UICONTROL 決策]**&#x200B;選單來編輯或刪除決定原則。

>[!BEGINTABS]

>[!TAB 從個人化編輯器編輯或刪除原則]

![](assets/decision-policy-edit.png)

>[!TAB 從決策功能表編輯或刪除原則]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## 指派位置（電子郵件） {#placement}

對於電子郵件，您需要定義與決定原則相關元件的位置。 若要這麼做，請按一下元件屬性窗格中的&#x200B;**[!UICONTROL 決策]**&#x200B;按鈕，然後選取&#x200B;**[!UICONTROL 指派位置]**。 [瞭解如何使用版位](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

## 後續步驟 {#next-steps}

現在您已瞭解如何建立決定原則，您已準備好將其用於[!DNL Journey Optimizer]管道以傳遞優惠方案。

➡️ [瞭解如何在訊息中使用決定原則](../experience-decisioning/use-decision-policy.md)
