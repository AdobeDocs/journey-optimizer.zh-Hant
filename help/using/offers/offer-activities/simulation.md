---
title: 建立模擬
description: 瞭解如何模擬將在指定位置傳遞哪些優惠，以驗證您的決策邏輯
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 4d196e6485b55fe63bd8da2c7cdfc454a26f80f3
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 13%

---

# 建立模擬 {#create-simulations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation"
>title="模擬報價決策"
>abstract="模擬功能可讓您模擬出特定位置有哪些報價會傳送至測試設定檔。這讓您能夠在不影響目標收件者的情況下，測試和改善各種版本的報價。"

## 關於模擬 {#about-simulation}

若要驗證您的決定邏輯，您可以模擬將哪些優惠傳遞至指定位置的測試設定檔。

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

這讓您能夠在不影響目標收件者的情況下，測試和改善各種版本的報價。

>[!NOTE]
>
>此功能可模擬對 [!DNL Decisioning] API。 進一步瞭解 [使用Decisioning API傳遞優惠方案](../api-reference/offer-delivery-api/decisioning-api.md).

若要存取此功能，請選取 **[!UICONTROL 模擬]** 標籤從 **[!UICONTROL 決定管理]** > **[!UICONTROL 選件]** 功能表。

![](../assets/offers_simulation-tab.png)

>[!NOTE]
>
>由於模擬不會產生任何決定事件，因此 [上限](../offer-library/creating-personalized-offers.md#capping) 計數不受影響。

<!--
➡️ [Discover this feature in video](#video)
-->

## 選取測試設定檔 {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation_test_profile"
>title="新增測試設定檔"
>abstract="您可以透過選取身分識別命名空間和相對應的身分識別值來新增測試設定檔。您必須擁有已可供使用的測試設定檔才能將它們用於模擬。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/profiles/creating-test-profiles.html" text="建立測試設定檔"

首先，您需要選取要用於模擬的測試設定檔。

>[!CAUTION]
>
>您必須有可用的測試設定檔，以模擬將傳送給他們的優惠。 瞭解如何 [建立測試設定檔](../../audience/creating-test-profiles.md).

1. 按一下 **[!UICONTROL 管理設定檔]**.

   ![](../assets/offers_simulation-manage-profile.png)

1. 選取您要用來識別測試設定檔的身分名稱空間。 在此範例中，我們將使用 **電子郵件** 名稱空間。

   >[!NOTE]
   >
   >身分名稱空間會定義識別碼的內容，例如電子郵件地址或CRM ID。 進一步瞭解Adobe Experience Platform身分識別名稱空間 [在本節中](../../audience/get-started-identity.md){target="_blank"}.

1. 輸入身分值並按一下 **[!UICONTROL 檢視]** 以列出可用的設定檔。

   ![](../assets/offers_simulation-add-profile.png)

1. 如果您想要測試不同的設定檔資料，請新增其他設定檔，並儲存您的選取專案。

   ![](../assets/offers_simulation-save-profiles.png)

1. 新增後，所有設定檔都會列在下的下拉式清單中 **[!UICONTROL 測試設定檔]**. 您可以在儲存的測試設定檔之間切換，以顯示每個所選設定檔的結果。

   ![](../assets/offers_simulation-saved-profiles.png)

   >[!NOTE]
   >
   >選取的設定檔仍會列為測試設定檔在 **[!UICONTROL 模擬]** 以標籤從一個工作階段移至另一個工作階段，直到使用將其移除 **[!UICONTROL 管理設定檔]**.

1. 您可以按一下 **[!UICONTROL 設定檔詳細資料]** 顯示所選設定檔資料的連結。

<!--Learn more on [selecting test profiles](messages/preview.md#select-test-profiles)-->

## 新增決定範圍 {#add-decision-scopes}

現在選取您要在測試設定檔上模擬的優惠決定。

1. 選取 **[!UICONTROL 新增決定範圍]**.

   ![](../assets/offers_simulation-add-decision.png)

1. 從清單中選取位置。

   ![](../assets/offers_simulation-add-decision-scope.png)

1. 將顯示可用的決策。

   * 您可以使用搜尋欄位來縮小選取範圍。
   * 您可以按一下 **[!UICONTROL 開啟優惠決定]** 連結以開啟您建立的所有決定清單。 進一步瞭解 [決定](create-offer-activities.md).

   選取您選擇的決定並按一下 **[!UICONTROL 新增]**.

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

1. 按一下 **[!UICONTROL 設定]**.

   ![](../assets/offers_simulation-settings.png)

1. 在 **[!UICONTROL 重複資料刪除]** 區段，您可以選擇允許跨決定和/或版位重複的優惠。 這表示可能會將相同優惠指派給多個決定/位置。

   ![](../assets/offers_simulation-settings-deduplication.png)

   >[!NOTE]
   >
   >依預設，會啟用所有重複資料刪除旗標以進行模擬，這表示決定引擎允許重複專案，因此可以在多個決定/版位中提出相同的主張。 進一步瞭解 [!DNL Decisioning] 中的API要求屬性 [本節](../api-reference/offer-delivery-api/decisioning-api.md).

1. 在 **[!UICONTROL 回應格式]** 區段，您可以選擇在程式碼檢視中包含中繼資料。 核取對應的選項，然後選取您選擇的中繼資料。 選擇時，它們會顯示在請求和回應裝載中 **[!UICONTROL 檢視程式碼]**. 進一步瞭解 [檢視模擬結果](#simulation-results) 區段。

   ![](../assets/offers_simulation-settings-response-format.png)

   >[!NOTE]
   >
   >開啟選項時，預設會選取所有專案。

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

>[!NOTE]
>
>目前對於模擬資料，您只能使用 **[!UICONTROL 中心]** API。

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

1. 按一下 **[!UICONTROL 檢視結果]**.

   ![](../assets/offers_simulation-view-results.png)

1. 系統會根據針對每個決定選取的設定檔，顯示最佳可用優惠方案。

   選取要顯示其詳細資料的選件。

   ![](../assets/offers_simulation-offer-details.png)

1. 按一下 **[!UICONTROL 檢視程式碼]** 顯示請求和回應裝載。 [了解更多](#view-code)

1. 從清單中選取另一個設定檔，以顯示不同測試設定檔的優惠決定結果。

1. 您可以視需要多次新增、移除或更新決定範圍。

>[!NOTE]
>
>每次您變更設定檔或更新決定範圍時，都需要使用重新整理結果 **[!UICONTROL 檢視結果]** 按鈕。

## 檢視程式碼 {#view-code}

1. 使用 **[!UICONTROL 檢視程式碼]** 按鈕來顯示請求和回應裝載。

   ![](../assets/offers_simulation-view-code.png)

   程式碼檢視會顯示目前使用者的開發人員資訊。 根據預設， **[!UICONTROL 回應裝載]** 隨即顯示。

   ![](../assets/offers_simulation-request-payload.png)

1. 按一下 **[!UICONTROL 回應裝載]** 或 **[!UICONTROL 請求承載]** 以在這兩個標籤之間瀏覽。

   ![](../assets/offers_simulation-response-payload.png)

1. 若要在外部使用請求裝載 [!DNL Journey Optimizer]  — 如需疑難排解，例如，使用 **[!UICONTROL 複製到剪貼簿]** 「程式碼檢視」頂端的按鈕。

   ![](../assets/offers_simulation-copy-payload.png)

   <!--You cannot copy the response payload. ACTUALLY YES YOU CAN > to confirm with PM/dev? -->

   >[!NOTE]
   >
   >將請求或回應裝載複製到您自己的程式碼時，請務必取代 {USER_TOKEN} 和 {API_KEY} ，則為有效值。 瞭解如何在中擷取這些值 [ADOBE EXPERIENCE PLATFORM API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target="_blank"} 檔案。

