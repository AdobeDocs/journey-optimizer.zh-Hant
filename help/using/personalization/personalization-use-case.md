---
solution: Journey Optimizer
product: journey optimizer
title: Personalization使用案例&colon；訂單狀態通知
description: 瞭解如何使用設定檔、優惠決定和內容資訊個人化訊息。
feature: Personalization, Use Cases
topic: Personalization
role: Developer
level: Intermediate
keywords: 運算式、編輯器、使用案例、個人化
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
TQID: https://experienceleague.adobe.com/TzGxWPRUHz4Hf-Acni4-LjNTpAYTjZBBt-GMxlNXQHM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1086
ht-degree: 1%

---

# Personalization使用案例：訂單狀態通知 {#personalization-use-case}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;遵循結合設定檔、優惠決定和內容歷程資料的訂單狀態使用案例，以在Adobe Journey Optimizer中個人化推播通知。

>[!ENDSHADEBOX]

在此使用案例中，您將會瞭解如何在單一推播通知訊息中使用多種型別的個人化。 將使用三種型別的個人化：

* **設定檔**：根據設定檔欄位的訊息個人化
* **優惠決定**：以決定管理變數為基礎的個人化
* **內容**：以歷程中的內容資料為基礎的個人化

此範例的目標是在每次更新客戶訂單時將事件推送至[!DNL Journey Optimizer]。 然後，推播通知會傳送給客戶，其中包含訂單和個人化優惠的相關資訊。

對於此使用案例，需要下列先決條件：

* 設定訂單事件，包含訂單編號、狀態及料號名稱。 請參閱本[章節](../event/about-events.md)。
* 建立決定，請參閱此[區段](../offers/offer-activities/create-offer-activities.md)。

➡️ [探索視訊中的類似使用案例](#video)

## 步驟1 — 建立歷程 {#create-journey}

1. 按一下&#x200B;**[!UICONTROL 歷程]**&#x200B;功能表並建立新歷程。

   ![](assets/perso-uc4.png)

1. 新增您的進入事件和&#x200B;**推播**&#x200B;動作活動。

   ![](assets/perso-uc5.png)

1. 設定並設計您的推播通知訊息。 請參閱本[章節](../push/create-push.md)。

## 步驟2 — 在設定檔中新增個人化 {#add-perso}

1. 在&#x200B;**推播**&#x200B;活動中，按一下&#x200B;**編輯內容**。

1. 按一下&#x200B;**標題**&#x200B;欄位。

   ![](assets/perso-uc2.png)

1. 輸入主旨並新增個人化設定檔。 使用搜尋列來尋找設定檔的名字欄位。 在主旨文字中，將游標置於要插入個人化欄位的位置，然後按一下&#x200B;**+**&#x200B;圖示。 按一下&#x200B;**儲存**。

   ![](assets/perso-uc3.png)

## 步驟3 — 在內容資料上新增個人化 {#add-perso-contextual-data}

1. 在&#x200B;**推播**&#x200B;活動中，按一下&#x200B;**編輯內容**，然後按一下&#x200B;**標題**&#x200B;欄位。

   ![](assets/perso-uc9.png)

1. 選取&#x200B;**內容屬性**&#x200B;功能表。 只有在歷程將內容資料傳遞至訊息時，內容屬性才可用。 按一下&#x200B;**Journey Orchestration**。 下列內容相關資訊隨即顯示：

   * **事件**：此類別會重新分組歷程中置於頻道動作活動之前之事件中的所有欄位。
   * **歷程屬性**：與特定設定檔之歷程相關的技術欄位，例如歷程ID或遇到的特定錯誤。 進一步瞭解[Journey Orchestration檔案](../building-journeys/expression/journey-properties.md)。

   ![](assets/perso-uc10.png)

1. 展開&#x200B;**事件**&#x200B;專案，並尋找與您的事件相關的訂單編號欄位。 您也可以使用搜尋方塊。 按一下&#x200B;**+**&#x200B;圖示，在主旨文字中插入個人化欄位。 按一下&#x200B;**儲存**。

   ![](assets/perso-uc11.png)

1. 現在按一下&#x200B;**內文**&#x200B;欄位。

   ![](assets/perso-uc12.png)

1. 輸入訊息，然後從&#x200B;**[!UICONTROL 內容屬性]**&#x200B;功能表插入訂單專案名稱和訂單進度。

   ![](assets/perso-uc13.png)

1. 從左側功能表選取&#x200B;**優惠決定**&#x200B;以插入決定變數。 選取位置，然後按一下決定旁邊的&#x200B;**+**&#x200B;圖示以將其新增到內文。

   ![](assets/perso-uc14.png)

1. 按一下驗證以確定沒有錯誤，然後按一下[儲存]。**&#x200B;**

   ![](assets/perso-uc15.png)

## 步驟4 — 測試並發佈歷程 {#test-publish}

1. 按一下&#x200B;**測試**&#x200B;按鈕，然後按一下&#x200B;**觸發事件**。

   ![](assets/perso-uc17.png)

1. 輸入測試中要傳遞的不同值。 測試模式僅適用於測試設定檔。 設定檔識別碼必須對應至測試設定檔。 按一下&#x200B;**傳送**。

   ![](assets/perso-uc18.png)

   推播通知會傳送並顯示在測試設定檔的行動電話上。

   ![](assets/perso-uc19.png)

1. 確認沒有錯誤並發佈歷程。

## 作法影片 {#video}

以下影片顯示了一個類似的使用案例，運用歷程中的內容資料來個人化電子郵件。

>[!VIDEO](https://video.tv.adobe.com/v/3425027?quality=12)

## 快速參考 {#quick-reference}

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

>[!BEGINTABS]

>[!TAB 概觀]

**TL；DR**

此頁面以單一訊息逐步解說訂單狀態推播通知使用案例，其中結合三種型別的個人化 — 設定檔欄位、優惠決定和內容相關的歷程資料。

**個意圖**

* 建立具有訂購事件和推播動作活動的歷程
* 將設定檔式個人化（客戶的名字）新增至推播標題
* 從歷程事件新增內容資料個人化（訂單編號、專案名稱、訂單進度）
* 將優惠決定個人化新增至推播內文
* 在測試模式下測試歷程並發佈

>[!TAB 字彙]

* **設定檔個人化**：根據設定檔欄位（例如名字）的Personalization，透過`profile.*`屬性存取。 *（產品特定）*
* **優惠決定**：根據決定管理變數的Personalization；從個人化編輯器中的優惠決定功能表插入。 *（產品特定）*
* **情境式個人化**：根據歷程資料的Personalization — 事件欄位（例如訂單編號、專案名稱、訂單進度）和歷程屬性（例如歷程ID、錯誤）。 僅當歷程將內容資料傳遞至訊息時可用。 *（產品特定）*
* **歷程屬性**：可在「內容屬性> Journey Orchestration」下存取與指定設定檔的歷程相關的技術欄位，例如歷程ID或發生的錯誤。 *（產品特定）*

>[!TAB 術語]

* **正式名稱：**&#x200B;內容個人化 — 變體：內容型個人化、歷程內容個人化
* **同義字：** &quot;Journey Orchestration&quot; （內容屬性功能表下的UI標籤） =內容歷程資料來源
* **請勿混淆：**&#x200B;設定檔個人化（靜態設定檔欄位值，一律可用）≠內容個人化（歷程事件和屬性資料，僅在歷程內容已傳遞至訊息後可用）≠優惠決定個人化（決定管理變數）

>[!TAB 護欄與限制]

* 只有在歷程已將內容資料傳遞至訊息時，個人化編輯器中才可使用內容屬性。
* 測試模式僅適用於測試設定檔；在事件設定中輸入的設定檔識別碼必須對應到現有的測試設定檔。

>[!TAB 常見問題集]

**問：在此使用案例中，哪三種個人化型別結合？**

個人設定檔（來自`profile.*`的客戶名字）、內容資料個人化（訂單編號、專案名稱，以及來自歷程事件的訂單進度）以及優惠決定個人化（插入內文中的決定管理優惠）。

**問：內容屬性在個人化編輯器中來自何處？**

內容屬性來自放在歷程中頻道動作活動之前的事件，以及歷程技術屬性。 它們會顯示在個人化編輯器中的內容屬性> Journey Orchestration >事件（事件欄位）或歷程屬性（歷程中繼資料）下方。

**問：此使用案例的必要條件為何？**

訂單事件必須設定訂單編號、狀態及專案名稱欄位，而且決定必須存在於決定管理中。

**問：在此使用案例中，我該如何測試推播通知？**

按一下歷程中的測試按鈕，然後按一下「觸發事件」並在事件設定視窗中輸入事件值。 測試模式僅適用於測試設定檔；設定檔識別碼必須對應至現有的測試設定檔。

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: ae5284c7 -->
