---
solution: Journey Optimizer
product: journey optimizer
title: 設定單一事件
description: 了解如何設定單一事件
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: 事件，統一，建立，歷程
exl-id: e22e2bc7-0c15-457a-8980-97bea5da7784
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '1573'
ht-degree: 11%

---

# 設定單一事件 {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="單一事件"
>abstract="事件設定可讓您定義Journey Optimizer將接收做為事件的資訊。 您可以使用多個事件（在歷程的不同步驟中），而數個歷程可以使用相同的事件。 單一事件會連結至特定設定檔。 可由規則型或系統產生。"

單一事件會連結至特定設定檔。 可由規則型或系統產生。  深入了解單一事件 [本節](../event/about-events.md).

以下是設定新事件的前幾個步驟：

1. 在「管理」(ADMINISTRATION)菜單部分中，選擇 **[!UICONTROL 配置]**. 在  **[!UICONTROL 事件]** ，按一下 **[!UICONTROL 管理]**. 畫面隨即顯示事件清單。

   ![](assets/jo-event1.png)

1. 按一下 **[!UICONTROL 建立事件]** 來建立新事件。 事件設定窗格會在畫面右側開啟。

   ![](assets/jo-event2.png)

1. 輸入事件名稱。 您也可以新增說明。

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >請勿使用空格或特殊字元。請勿使用超過 30 個字元。

1. 在 **[!UICONTROL 類型]** 欄位，選擇 **單一**.

   ![](assets/jo-event3bis.png)

1. 在 **[!UICONTROL 事件ID類型]** 欄位中，選取您要使用的事件ID類型： **規則型** 或 **系統生成**. 請參閱 [本節](../event/about-events.md#event-id-type).

   ![](assets/jo-event4.png)

1. 使用此事件的歷程次數會顯示在 **[!UICONTROL 用於]** 欄位。 您可以按一下 **[!UICONTROL 檢視歷程]** 圖示以顯示使用此事件的歷程清單。

1. 定義結構和裝載欄位：這是您選取歷程預期會收到的事件資訊（通常稱為裝載）的位置。 接著，您就可以在歷程中使用這項資訊。請參閱[本節](../event/about-creating.md#define-the-payload-fields)。

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >選取 **[!UICONTROL 系統生成]** 類型，只有具有eventID type欄位的結構才可供使用。 選取 **[!UICONTROL 規則型]** 類型，所有體驗事件結構皆可使用。

1. 若為規則型事件，請按一下 **[!UICONTROL 事件ID條件]** 欄位。 使用簡單運算式編輯器，定義系統將使用的條件，以識別將觸發您歷程的事件。
   ![](assets/jo-event6.png)

   在範例中，我們根據設定檔的城市寫了條件。 這表示每當系統收到符合此條件的事件時(**[!UICONTROL 城市]** 欄位與 **[!UICONTROL 巴黎]** 值)，則會傳遞至歷程。

   >[!NOTE]
   >
   >定義 **[!UICONTROL 事件ID條件]**. 在簡單運算式編輯器中，並非所有運算子都可用，它們取決於資料類型。 例如，對於欄位的字串類型，您可以使用「包含」或「等於」。

1. 新增命名空間。此步驟為選填，但建議您新增命名空間，以便運用儲存在「即時客戶個人檔案服務」的資訊。它會定義事件具備的金鑰類型。請參閱[本節](../event/about-creating.md#select-the-namespace)。

1. 定義設定檔識別碼：從您的裝載欄位中選擇欄位，或定義公式以識別與事件相關聯的人員。 如果您選取命名空間，系統便會自動設定此金鑰（但您仍可加以編輯）。事實上，歷程會挑選應該與命名空間對應的金鑰（例如，如果您選取電子郵件命名空間，系統便會選取電子郵件金鑰）。 請參閱[本節](../event/about-creating.md#define-the-event-key)。

   ![](assets/jo-event7.png)

1. 按一下「**[!UICONTROL 儲存]**」。

   條件現在已設定完畢，且準備好放入歷程中。若要接收事件，則需要完成其他設定步驟。請參閱[此頁面](../event/additional-steps-to-send-events-to-journey.md)。

## 定義裝載欄位 {#define-the-payload-fields}

有效負載定義可讓您選擇系統預期從歷程中的事件接收的資訊，以及識別與事件相關聯之人員的金鑰。 裝載以Experience CloudXDM欄位定義為基礎。 如需XDM的詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.

1. 從清單中選取XDM架構，然後按一下 **[!UICONTROL 欄位]** 欄位或 **[!UICONTROL 編輯]** 表徵圖。

   ![](assets/journey8.png)

   架構中定義的所有欄位都會顯示。 欄位清單因結構而異。 您可以搜尋特定欄位，或使用篩選器來顯示所有節點和欄位，或僅顯示選取的欄位。 根據架構定義，某些欄位可能是必填欄位，且已預先選取。 您無法取消選取它們。 依預設，會選取所有對於歷程正確接收事件而言為必要的欄位。

   >[!NOTE]
   >
   >針對系統產生的事件，請確定您已將「協調」欄位群組新增至XDM架構。 這可確保您的架構包含所有要使用的必要資訊 [!DNL Journey Optimizer].

   ![](assets/journey9.png)

1. 選取您要從事件接收的欄位。 這些是業務使用者在歷程中將利用的欄位。 也必須包含用來識別與事件相關聯之人員的金鑰(請參閱 [本節](../event/about-creating.md#define-the-event-key))。

   >[!NOTE]
   >
   >若為系統產生的事件， **[!UICONTROL eventID]** 欄位會自動新增至選取的欄位清單中，以便 [!DNL Journey Optimizer] 可識別事件。 推送事件的系統不應產生ID，而應使用有效負載預覽中可用的ID。 請參閱[本節](../event/about-creating.md#preview-the-payload)。

1. 選取完所需欄位後，按一下 **[!UICONTROL 確定]** 或按下 **[!UICONTROL 輸入]**.

   選取的欄位數會顯示在 **[!UICONTROL 欄位]** 欄位。

   ![](assets/journey12.png)

## 選取命名空間 {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="身分識別命名空間"
>abstract="選取用於識別與事件相關聯的客戶設定檔的金鑰。"

命名空間可讓您定義用於識別與事件相關聯之人員的索引鍵類型。 其設定為選用。 如果您想在歷程中擷取來自 [即時客戶個人檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}. 如果您只使用來自協力廠商系統的資料（透過自訂資料來源），則不需要命名空間定義。

您可以使用其中一個預先定義的命名空間，或使用身分命名空間服務建立新的一個。 請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hant){target="_blank"}.

如果您選取的架構具有主要身分，則 **[!UICONTROL 探查器標識符]** 和 **[!UICONTROL 命名空間]** 欄位已預填。 如果沒有定義標識，則我們選擇 _identityMap > id_ 作為主要金鑰。 然後，您必須選取命名空間，系統就會預先填入索引鍵(位於 **[!UICONTROL 命名空間]** 欄位)使用 _identityMap > id_.

選取欄位時，會標籤主要身分欄位。

![](assets/primary-identity.png)

從下拉式清單中選取命名空間。

![](assets/journey17.png)

每個歷程僅允許一個命名空間。 如果您在相同歷程中使用數個事件，則這些事件需要使用相同的命名空間。 請參閱[此頁面](../building-journeys/journey.md)。

>[!NOTE]
>
>您只能選取以人物為基礎的身分命名空間。 如果您已為查詢表格定義命名空間(例如：產品查閱的ProductID命名空間)，將無法使用於 **命名空間** 下拉式清單。

## 定義設定檔識別碼 {#define-the-event-key}

金鑰是欄位或欄位組合，欄位是事件有效負載資料的一部分，可讓系統識別與事件相關聯的人員。 金鑰可以是Experience CloudID、CRM ID或電子郵件地址。

若要使用儲存在Adobe即時客戶設定檔資料庫中的資料，事件索引鍵必須是您在 [即時客戶個人檔案服務](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant){target="_blank"}.

設定檔識別碼可讓系統執行事件與個人設定檔之間的調解。 如果您選取的架構具有主要身分，則 **[!UICONTROL 設定檔識別碼]** 和 **[!UICONTROL 命名空間]** 欄位已預填。 若未定義身分，則 _identityMap > id_ 是主要金鑰。 然後，您必須選取命名空間，系統會使用 _identityMap > id_.

選取欄位時，會標籤主要身分欄位。

![](assets/primary-identity.png)

如果您需要使用不同的金鑰（例如CRM ID或電子郵件地址），則需要手動新增，如下所述：

1. 按一下內部 **[!UICONTROL 設定檔識別碼]** 欄位或鉛筆圖示上。

   ![](assets/journey16.png)

1. 在有效負載欄位清單中選取作為索引鍵的欄位。 您也可以切換至進階運算式編輯器，以建立更複雜的索引鍵（例如，事件的兩個欄位串連）。

   ![](assets/journey20.png)

收到事件時，鍵值允許系統識別與事件相關聯的人。 與命名空間相關聯(請參閱 [本節](../event/about-creating.md#select-the-namespace))，則可使用索引鍵來對Adobe Experience Platform執行查詢。 請參閱[此頁面](../building-journeys/about-journey-activities.md#orchestration-activities)。金鑰也可用來檢查人員是否在歷程中。 事實上，一個人不可能在同一個旅程中處於兩個不同的位置。 因此，系統不允許相同的索引鍵（例如CRMID=3224）位於相同歷程中的不同位置。

您也可以存取進階運算式函式(**[!UICONTROL 進階模式]**)。 這些函式可讓您操控用於執行特定查詢的值，例如更改格式、執行欄位串連，而僅考慮欄位的一部分（例如10個前字元）。 請參閱此[頁面](../building-journeys/expression/expressionadvanced.md)。

## 預覽裝載 {#preview-the-payload}

有效負載預覽可讓您驗證有效負載定義。

>[!NOTE]
>
>對於系統產生的事件，當您建立事件時，在檢視裝載預覽之前，請先儲存事件並重新開啟它。 需要執行此步驟，才能在裝載中產生事件ID。

1. 按一下 **[!UICONTROL 檢視裝載]** 圖示來預覽系統預期的裝載。

   ![](assets/journey13.png)

   您可以注意到已顯示選取的欄位。

   ![](assets/journey14.png)

1. 檢查預覽以驗證有效負載定義。

1. 接著，您可以將裝載預覽與事件傳送的負責人共用。 此裝載可協助他們設計推送至的事件設定 [!DNL Journey Optimizer]. 請參閱[此頁面](../event/additional-steps-to-send-events-to-journey.md)。
