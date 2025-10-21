---
solution: Journey Optimizer
product: journey optimizer
title: 設定單一事件
description: 瞭解如何設定單一事件
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: 事件，單一，建立，歷程
exl-id: e22e2bc7-0c15-457a-8980-97bea5da7784
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '1693'
ht-degree: 13%

---

# 設定單一事件 {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="單一事件"
>abstract="事件設定可讓您定義 Journey Optimizer 會接收為事件的資訊。您可以使用多個事件 (在歷程的不同步驟中)，而好幾個歷程可以使用同一個事件。單一事件會連結到特定的設定檔。它們可能是以規則為基礎或由系統產生。"

>[!CONTEXTUALHELP]
>id="ajo_journey_event_parameters"
>title="參數"
>abstract="定義事件的參數，例如結構描述和承載欄位。對於規則型事件，請使用「**[!UICONTROL 事件 ID 條件]**」欄位來定義系統要用哪些條件來確認將會觸發您的歷程的事件。新增用於事件的身份識別類型和輪廓識別碼。"

單一事件會連結到特定的設定檔。可以是規則型或系統產生。  閱讀有關單一事件[本節](../event/about-events.md)的詳細資訊。

以下是設定新事件的第一個步驟：

1. 在[管理]功能表區段中，瀏覽至&#x200B;**[!UICONTROL 組態]**，在&#x200B;**[!UICONTROL 事件]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 管理]**。 畫面隨即顯示事件清單。

   ![](assets/jo-event1.png)

1. 按一下&#x200B;**[!UICONTROL 建立事件]**&#x200B;以建立新事件。 事件設定窗格會在畫面右側開啟。

   ![](assets/jo-event2.png)

1. 輸入事件的名稱。 您也可以新增說明。

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >只允許使用英數字元和底線。 長度上限為30個字元。

1. 在&#x200B;**[!UICONTROL 型別]**&#x200B;欄位中，選擇&#x200B;**單一**。

   ![](assets/jo-event3bis.png)

1. 在&#x200B;**[!UICONTROL 事件識別碼型別]**&#x200B;欄位中，選取您要使用的事件識別碼型別： **規則型**&#x200B;或&#x200B;**系統產生**。 閱讀有關[本節](../event/about-events.md#event-id-type)中事件ID型別的詳細資訊。

   ![](assets/jo-event4.png)

1. 使用此事件的歷程次數會顯示在&#x200B;**[!UICONTROL 用於]**&#x200B;欄位中。 您可以按一下&#x200B;**[!UICONTROL 檢視歷程]**&#x200B;圖示，以顯示使用此事件的歷程清單。

1. 定義結構和裝載欄位：您可以在此處選取歷程預期會收到的事件資訊（通常稱為裝載）。 接著，您就可以在歷程中使用這項資訊。請參閱[本節](../event/about-creating.md#define-the-payload-fields)。

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >當您選取&#x200B;**[!UICONTROL 系統產生的]**&#x200B;型別時，只有具有eventID型別欄位的結構描述才可用。 當您選取&#x200B;**[!UICONTROL 規則型]**&#x200B;型別時，所有體驗事件結構描述都可供使用。

1. 對於規則型事件，請在&#x200B;**[!UICONTROL 事件識別碼條件]**&#x200B;欄位內按一下。 使用簡單或進階運算式編輯器，定義系統將使用的條件，以識別將觸發您歷程的事件。

   ![](assets/jo-event6.png)

   在我們的範例中，我們根據設定檔的城市來撰寫條件。 這表示每當系統收到符合此條件（**[!UICONTROL 城市]**&#x200B;欄位和&#x200B;**[!UICONTROL 巴黎]**&#x200B;值）的事件時，就會將其傳遞給歷程。

   >[!NOTE]
   >
   >在簡單運算式編輯器中，並非所有運運算元都可使用，它們取決於資料型別。 例如，對於欄位的字串型別，您可以使用「包含」或「等於」。
   >
   >如果您在建立事件後，使用新的列舉值修改綱要，則需要按照以下步驟將變更套用至現有事件：從事件欄位中取消選取列舉欄位，確認選擇，然後再次選取列舉欄位。 現在會顯示新的分項清單。

1. 新增身分型別。 此步驟為選填，但建議您新增身分型別，以便運用儲存在「即時客戶個人檔案服務」的資訊。 它會定義事件具備的金鑰類型。請參閱[此章節](../event/about-creating.md#select-the-namespace)深入瞭解。

1. 定義設定檔識別碼：從您的裝載欄位選擇一個欄位，或定義一個公式以識別與事件相關聯的人員。 如果您選取身分型別，此金鑰會自動設定（但仍可編輯）。 事實上，歷程會挑選應該與身分型別對應的金鑰（例如，如果您選取電子郵件身分型別，則會選取電子郵件金鑰）。 請參閱[此章節](../event/about-creating.md#define-the-event-key)深入瞭解。

   ![](assets/jo-event7.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

   條件現在已設定完畢，且準備好放入歷程中。若要接收事件，則需要完成其他設定步驟。請參閱[此頁面](../event/additional-steps-to-send-events-to-journey.md)。

## 定義裝載欄位 {#define-the-payload-fields}

裝載定義可讓您選擇系統預期從歷程中的事件接收的資訊，以及識別與事件相關聯之人員的金鑰。 裝載是根據Experience Cloud XDM欄位定義。 如需XDM的詳細資訊，請參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}。

1. 從清單中選取XDM結構描述，然後按一下&#x200B;**[!UICONTROL 欄位]**&#x200B;欄位或&#x200B;**[!UICONTROL 編輯]**&#x200B;圖示。

   ![](assets/journey8.png)

   結構描述中定義的所有欄位都會顯示。 欄位清單會因結構描述而異。 您可以搜尋特定欄位，或使用篩選器來顯示所有節點和欄位，或僅顯示選定的欄位。 根據結構描述定義，某些欄位可能是必填欄位並預先選取。 您無法取消選取它們。 依預設，系統會選取歷程正確接收事件所必須的所有欄位。

   >[!NOTE]
   >
   >對於系統產生的事件，請確定您已將「協調流程」欄位群組新增至XDM結構描述。 這將確保您的結構描述包含使用[!DNL Journey Optimizer]所需的所有資訊。

   ![](assets/journey9.png)

1. 選取您預期會從事件接收的欄位。 這些是業務使用者將在歷程中善用的欄位。 它們也必須包含用來識別與事件相關聯之人員的金鑰（請參閱[本區段](../event/about-creating.md#define-the-event-key)）。

   >[!NOTE]
   >
   >對於系統產生的事件，**[!UICONTROL eventID]**&#x200B;欄位會自動新增到選取的欄位清單中，以便[!DNL Journey Optimizer]可以識別事件。 推播事件的系統不應產生ID，而應使用裝載預覽中可用的ID。 請參閱[本節](../event/about-creating.md#preview-the-payload)。

1. 選取完所需的欄位後，按一下&#x200B;**[!UICONTROL 確定]**&#x200B;或按&#x200B;**[!UICONTROL Enter]**。

   選取的欄位數目會出現在&#x200B;**[!UICONTROL 欄位]**&#x200B;欄位中。

   ![](assets/journey12.png)

## 選取身分識別類型 {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="身分識別類型"
>abstract="選取索引鍵以識別和事件相關聯的客戶輪廓。"

身分型別（先前稱為「名稱空間」）可讓您定義用來識別與事件相關聯之人員的金鑰型別。 其設定是選用的。 如果您想要在歷程中擷取來自[即時客戶個人檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}的其他資訊，則需要此專案。 如果您僅使用來自協力廠商系統的資料，透過自訂資料來源，則不需要身分型別定義。

您可以使用現有的身分型別，或使用Adobe Experience Platform Identity Service建立新的身分型別。 在[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hant){target="_blank"}中進一步瞭解。

如果您選取具有主要身分的結構描述，則會預先填入&#x200B;**[!UICONTROL 效能評測器識別碼]**&#x200B;和&#x200B;**[!UICONTROL 身分型別]**&#x200B;欄位。 如果未定義任何身分，我們選取&#x200B;_identityMap > id_&#x200B;作為主索引鍵。 然後您必須選取身分型別，而且會使用&#x200B;**[!UICONTROL identityMap > id]**&#x200B;預先填入金鑰（_身分型別_&#x200B;欄位下方）。

選取欄位時，會標籤主要身分欄位。

![](assets/primary-identity.png)

從下拉式清單中選取身分型別。

![](assets/journey17.png)

每個歷程只允許一個身分型別。 如果您在同一個歷程中使用數個事件，則需要使用相同的身分型別。 請參閱[此頁面](../building-journeys/journey.md)。

>[!NOTE]
>
>您只能選取以人物為基礎的身分型別。 如果您已定義查閱表格的身分型別（例如：產品查閱的ProductID身分型別），將無法在&#x200B;**身分型別**&#x200B;下拉式清單中找到它。

## 定義設定檔識別碼 {#define-the-event-key}

索引鍵是欄位或欄位組合，這是事件裝載資料的一部分，可讓系統識別與事件相關聯的人員。 例如，索引鍵可以是Experience Cloud ID、CRM ID或電子郵件地址。

若要使用儲存在Adobe即時客戶設定檔資料庫中的資料，事件索引鍵必須是您在[即時客戶設定檔服務](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}中定義為設定檔身分的資訊。

設定檔識別碼可讓系統在事件和個人設定檔之間執行調解。 如果您選取具有主要身分的結構描述，則會預先填入&#x200B;**[!UICONTROL 設定檔識別碼]**&#x200B;和&#x200B;**[!UICONTROL 身分型別]**&#x200B;欄位。 如果未定義任何身分，則&#x200B;_identityMap > id_&#x200B;是主索引鍵。 然後您必須選取身分型別，而且金鑰會使用&#x200B;_identityMap > id_&#x200B;自動預先填入。

選取欄位時，會標籤主要身分欄位。

![](assets/primary-identity.png)

如果您需要使用不同的金鑰，例如CRM ID或電子郵件地址，您需要手動新增，如下所述：

1. 在&#x200B;**[!UICONTROL 設定檔識別碼]**&#x200B;欄位內或鉛筆圖示上按一下。

   ![](assets/journey16.png)

1. 選取在裝載欄位清單中選為索引鍵的欄位。

收到事件時，機碼的值可讓系統識別與事件相關聯的人員。 金鑰與[身分型別](../event/about-creating.md#select-the-namespace)相關聯，可用來在Adobe Experience Platform上執行查詢。 請參閱[此頁面](../building-journeys/about-journey-activities.md#orchestration-activities)。
金鑰也可用來檢查個人是否在歷程中。 事實上，一個人在同一歷程中不能位於兩個不同的位置。 因此，系統不允許相同的金鑰（例如金鑰CRMID=3224）位於相同歷程中的不同位置。

## 進階運算式編輯器 {#adv-exp-editor}

定義事件ID條件或設定檔識別碼時，您可以切換至進階運算式編輯器，以建立更複雜的索引鍵（例如兩個事件欄位的串連）。

![](assets/journey20.png)

若要執行其他操作，您可以從&#x200B;**[!UICONTROL 進階模式]**&#x200B;按鈕存取進階運算式函式。 這些函式可讓您控制用於執行特定查詢的值，例如變更格式、執行欄位串連，僅考慮欄位的一部分（例如10個第一個字元）。 請參閱此[頁面](../building-journeys/expression/expressionadvanced.md)。


## 預覽裝載 {#preview-the-payload}

裝載預覽可讓您驗證裝載定義。

>[!NOTE]
>
>對於系統產生的事件，當您建立事件時，在檢視裝載預覽之前，請儲存事件並重新開啟。 在裝載中產生事件ID時，需要執行此步驟。

1. 按一下&#x200B;**[!UICONTROL 檢視裝載]**&#x200B;圖示以預覽系統預期的裝載。

   ![](assets/journey13.png)

   您可以注意到已選取的欄位已顯示。

   ![](assets/journey14.png)

1. 檢查預覽以驗證裝載定義。

1. 然後，您可以將裝載預覽與共用給負責事件傳送的人員。 此承載可協助他們設計推送至[!DNL Journey Optimizer]之事件的設定。 請參閱[此頁面](../event/additional-steps-to-send-events-to-journey.md)。
