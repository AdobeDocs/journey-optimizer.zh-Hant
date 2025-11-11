---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 建立模擬
description: 瞭解如何模擬將在指定位置傳遞哪些優惠，以驗證您的決策邏輯
badge: label="舊版" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 12%

---

# 建立模擬 {#create-simulations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation"
>title="模擬報價決策"
>abstract="模擬功能可讓您模擬出特定產品建議放置環境有哪些產品建議會傳送至測試設定檔。這讓您能夠在不影響目標收件者的情況下，測試和改善各種版本的報價。"

## 關於模擬 {#about-simulation}

若要驗證您的決定邏輯，您可以模擬將哪些優惠傳遞至指定位置的測試設定檔。

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

這讓您能夠在不影響目標收件者的情況下，測試和改善各種版本的報價。

>[!NOTE]
>
>此功能會模擬對[!DNL Decisioning] API的單一要求。 深入瞭解[使用Decisioning API傳遞優惠方案](../api-reference/offer-delivery-api/decisioning-api.md)。

若要存取此功能，請從&#x200B;**[!UICONTROL 決定管理]** > **[!UICONTROL 優惠]**&#x200B;選單中選取&#x200B;**[!UICONTROL 模擬]**&#x200B;標籤。

![](../assets/offers_simulation-tab.png)

>[!NOTE]
>
>由於模擬不會產生任何決定事件，因此[上限](../offer-library/add-constraints.md#capping)計數不會受到影響。

<!--
➡️ [Discover this feature in video](#video)
-->

## 選取測試輪廓 {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation_test_profile"
>title="新增測試設定檔"
>abstract="您可以透過選取身分識別命名空間和相對應的身分識別值來新增測試設定檔。您必須擁有已可供使用的測試設定檔才能將它們用於模擬。"

首先，您需要選取要用於模擬的測試設定檔。

>[!CAUTION]
>
>您必須有可用的測試設定檔，以模擬將傳送給他們的優惠。 瞭解如何[建立測試設定檔](../../audience/creating-test-profiles.md)。

1. 按一下&#x200B;**[!UICONTROL 管理設定檔]**。

   ![](../assets/offers_simulation-manage-profile.png)

1. 選取您要用來識別測試設定檔的身分名稱空間。 在此範例中，我們將使用&#x200B;**電子郵件**&#x200B;名稱空間。

   >[!NOTE]
   >
   >身分名稱空間會定義識別碼的內容，例如電子郵件地址或CRM ID。 在本節[中進一步瞭解Adobe Experience Platform識別名稱空間](../../audience/get-started-identity.md){target="_blank"}。

1. 輸入身分值並按一下&#x200B;**[!UICONTROL 檢視]**&#x200B;列出可用的設定檔。

   ![](../assets/offers_simulation-add-profile.png)

1. 如果您想要測試不同的設定檔資料，請新增其他設定檔，並儲存您的選取專案。

   ![](../assets/offers_simulation-save-profiles.png)

1. 新增後，所有設定檔都會列在&#x200B;**[!UICONTROL 測試設定檔]**&#x200B;下的下拉式清單中。 您可以在儲存的測試設定檔之間切換，以顯示每個所選設定檔的結果。

   ![](../assets/offers_simulation-saved-profiles.png)

   >[!NOTE]
   >
   >選取的設定檔將保留在&#x200B;**[!UICONTROL Simulation]**&#x200B;分頁中，以測試設定檔形式列在不同工作階段中，直到使用&#x200B;**[!UICONTROL 管理設定檔]**&#x200B;移除這些設定檔為止。

1. 您可以按一下&#x200B;**[!UICONTROL 設定檔詳細資料]**&#x200B;連結，以顯示選取的設定檔資料。

## 新增決定範圍 {#add-decision-scopes}

現在選取您要在測試設定檔上模擬的優惠決定。

1. 選取&#x200B;**[!UICONTROL 新增決定範圍]**。

   ![](../assets/offers_simulation-add-decision.png)

1. 從清單中選取位置。

   ![](../assets/offers_simulation-add-decision-scope.png)

1. 將顯示可用的決策。

   * 您可以使用搜尋欄位來縮小選取範圍。
   * 您可以按一下&#x200B;**[!UICONTROL 開啟優惠決定]**&#x200B;連結，開啟您建立的所有決定清單。 深入瞭解[決定](create-offer-activities.md)。

   選取您選擇的決定並按一下[新增]。**&#x200B;**

   ![](../assets/offers_simulation-add-decision-scope-add.png)

1. 您剛才定義的決定範圍會顯示在主要工作區中。

   您可以調整想要請求的優惠方案數量。 例如，如果您選取2，則會針對此決定範圍顯示最佳的2個優惠方案。

   ![](../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >您最多可以請求30個優惠方案。

1. 重複上述步驟，視需要新增更多決策。

   ![](../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >即使您定義了數個決定範圍，也只會模擬一個API請求。

## 定義模擬設定 {#define-simulation-settings}

若要編輯模擬的預設設定，請遵循下列步驟。

1. 按一下&#x200B;**[!UICONTROL 設定]**。

   ![](../assets/offers_simulation-settings.png)

1. 在&#x200B;**[!UICONTROL 重複資料刪除]**&#x200B;區段中，您可以選擇允許跨決定和/或刊登版位重複優惠。 這表示可能會將相同優惠指派給多個決定/位置。

   ![](../assets/offers_simulation-settings-deduplication.png)

   >[!NOTE]
   >
   >依預設，會啟用所有重複資料刪除旗標以進行模擬，這表示決定引擎允許重複專案，因此可以跨多個決定/位置提出相同的主張。 在[!DNL Decisioning]本節[中進一步瞭解](../api-reference/offer-delivery-api/decisioning-api.md) API要求屬性。

1. 在&#x200B;**[!UICONTROL 回應格式]**&#x200B;區段中，您可以選擇在程式碼檢視中包含中繼資料。 核取對應的選項，然後選取您選擇的中繼資料。 選取&#x200B;**[!UICONTROL 檢視代碼]**&#x200B;時，它們會顯示在請求和回應裝載中。 在[檢視模擬結果](#simulation-results)區段中瞭解更多。

   ![](../assets/offers_simulation-settings-response-format.png)

   >[!NOTE]
   >
   >開啟選項時，預設會選取所有專案。

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

>[!NOTE]
>
>目前對於模擬資料，您只能使用&#x200B;**[!UICONTROL 中心]** API。

<!--
In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## 檢視模擬結果 {#simulation-results}

新增決定範圍並選取測試設定檔後，您就可以檢視結果。

1. 按一下&#x200B;**[!UICONTROL 檢視結果]**。

   ![](../assets/offers_simulation-view-results.png)

1. 系統會根據針對每個決定選取的設定檔，顯示最佳可用優惠方案。

   選取要顯示其詳細資料的選件。

   ![](../assets/offers_simulation-offer-details.png)

1. 按一下&#x200B;**[!UICONTROL 檢視代碼]**&#x200B;以顯示請求和回應裝載。 [了解更多](#view-code)

1. 從清單中選取另一個設定檔，以顯示不同測試設定檔的優惠決定結果。

1. 您可以視需要多次新增、移除或更新決定範圍。

>[!NOTE]
>
>每次變更設定檔或更新決定範圍時，都需要使用&#x200B;**[!UICONTROL 檢視結果]**&#x200B;按鈕重新整理結果。

## 檢視程式碼 {#view-code}

1. 使用&#x200B;**[!UICONTROL 檢視代碼]**&#x200B;按鈕來顯示請求和回應裝載。

   ![](../assets/offers_simulation-view-code.png)

   程式碼檢視會顯示目前使用者的開發人員資訊。 預設會顯示&#x200B;**[!UICONTROL 回應承載]**。

   ![](../assets/offers_simulation-request-payload.png)

1. 按一下&#x200B;**[!UICONTROL 回應承載]**&#x200B;或&#x200B;**[!UICONTROL 請求承載]**，在兩個標籤之間導覽。

   ![](../assets/offers_simulation-response-payload.png)

1. 若要在[!DNL Journey Optimizer]外部使用請求承載，例如，為了疑難排解之用，請使用程式碼檢視上方的&#x200B;**[!UICONTROL 複製到剪貼簿]**&#x200B;按鈕來複製它。

   ![](../assets/offers_simulation-copy-payload.png)

   <!--You cannot copy the response payload. ACTUALLY YES YOU CAN > to confirm with PM/dev? -->

   >[!NOTE]
   >
   >將請求或回應裝載複製到您自己的程式碼時，請確定您將{USER_TOKEN}和{API_KEY}取代為有效值。 在[Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=zh-Hant){target="_blank"}檔案中瞭解如何擷取這些值。

