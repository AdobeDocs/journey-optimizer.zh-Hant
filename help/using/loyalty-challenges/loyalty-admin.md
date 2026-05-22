---
solution: Journey Optimizer
product: journey optimizer
title: 設定熟客方案
description: 瞭解如何在Adobe Journey Optimizer中為您的忠誠度計畫設定獎勵提供者、事件定義和組織層級設定。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人測試版" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: a4ad533e54f3692eb0483138a8cfd1cee0e77ba1
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 2%

---

# 設定熟客方案 {#loyalty-admin}

>[!BEGINSHADEBOX]

**忠誠度挑戰檔案：**

* [開始應對忠誠度挑戰](get-started.md)
* [存取及管理挑戰與工作](access-loyalty-challenges.md)
* [創造挑戰](create-challenges.md)
* [建立任務](create-tasks.md)
* [監視忠誠度挑戰績效](loyalty-reporting.md)
* **設定熟客方案** ◀︎ **您在這裡**
* [忠誠度挑戰API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](../rn/releases.md)。

**[!UICONTROL 忠誠度管理員]**&#x200B;區段是您設定Journey Optimizer如何連線至外部忠誠度系統的位置。 行銷人員使用&#x200B;**[!UICONTROL 忠誠度挑戰(Beta)]**&#x200B;來設計挑戰、工作、內容和訊息。 **[!UICONTROL 忠誠度管理員]**&#x200B;是獨立的僅限管理員區域，用於獎勵履行、事件對應和產品詳細目錄。

當客戶完成挑戰或達到獎勵里程碑時，Journey Optimizer會呼叫您設定為提供點數或其他獎勵的獎勵提供者。 **[!UICONTROL 忠誠度管理員]**&#x200B;中的設定不會影響挑戰&#x200B;**[!UICONTROL 內容]**、**[!UICONTROL 訊息]**&#x200B;或&#x200B;**[!UICONTROL 對象]**&#x200B;設定 — 這些設定仍受行銷人員控制。

## 您在此處設定的與在忠誠度挑戰中的設定 {#scope}

| 區域圖 | 在熟客方案管理員中設定 | 在忠誠度挑戰中設定 |
|------|----------------------------|----------------------------------|
| 獎勵履行API | 是 — 獎勵提供者 | 否 — 僅選取提供者和金額 |
| 自訂活動的事件對應 | 是 — 事件定義 | 否 — 在自訂事件工作上選取事件名稱 |
| 產品群組對應 | 是 — 產品詳細目錄 | 否 — 在編寫購買/支出任務時使用群組 |
| 挑戰結構、內容、對象 | 無 | 是 |

當客戶獲得獎勵時，Adobe Journey Optimizer會傳送履行呼叫給您的獎勵提供者。 您的熟客平台負責將會員的帳戶入帳。

## 先決條件 {#prerequisites}

**[!UICONTROL 忠誠度管理員]**&#x200B;適用於每個組織的少量管理員。 除了[忠誠度挑戰](get-started.md#prerequisites)所需的許可權之外，您還需要Journey Optimizer執行個體的管理員層級存取權。 請聯絡您的Adobe管理員以請求存取權。

## 存取忠誠度管理員 {#access-loyalty-admin}

若要開啟&#x200B;**[!UICONTROL 熟客方案管理員]**，請從Journey Optimizer的左側導覽器選取它。

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

**[!UICONTROL 忠誠度管理員]**&#x200B;已組織為標籤： **[!UICONTROL 全域設定]**、**[!UICONTROL 獎勵提供者]**、**[!UICONTROL 事件定義]**&#x200B;以及&#x200B;**[!UICONTROL 產品詳細目錄]**。 您可用的標籤取決於您組織的許可權和功能設定。

## 全域設定 {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="全域設定"
>abstract="選取忠誠度計畫的Adobe Experience Platform身分名稱空間，並複製設定ID。 必須先進行這些組織層級設定，獎勵提供者才能正確履行獎勵。"

使用&#x200B;**[!UICONTROL 全域設定]**&#x200B;來設定忠誠度挑戰的組織範圍選項。

1. 開啟&#x200B;**[!UICONTROL 全域設定]**&#x200B;標籤。

1. 在&#x200B;**[!UICONTROL 名稱空間]**&#x200B;下拉式清單中，選取忠誠計畫使用的[身分名稱空間](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/namespaces)。

1. 選取&#x200B;**[!UICONTROL 儲存]**&#x200B;以將名稱空間套用至您的「忠誠度挑戰」設定。

1. 當您需要與實作團隊或外部系統共用時（例如，在設定傳入事件傳送時），請複製&#x200B;**[!UICONTROL 設定識別碼]**。

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## 獎勵提供者 {#reward-providers}

**獎勵提供者**&#x200B;會告訴Journey Optimizer在記錄挑戰進度或完成挑戰時，要傳送履行呼叫的位置，例如，將忠誠點數或起始點數加到會員帳戶的API。

獎勵提供者設定包括：

* 基本連線詳細資料（名稱、說明、API URL、標題）
* **[!UICONTROL 獎勵定義]** — 此提供者可以發行的獎勵型別（例如，星級或英里）
* **[!UICONTROL 獎賞代理]** （選擇性） — 會透過而非您的端點直接路由呼叫的中間Proxy
* **[!UICONTROL 驗證權杖產生器]** — Journey Optimizer在呼叫API之前用來取得存取權杖的機制

### 建立獎勵提供者 {#create-reward-provider}

1. 開啟&#x200B;**[!UICONTROL 獎勵提供者]**&#x200B;索引標籤，然後選取&#x200B;**[!UICONTROL 建立獎勵提供者]**。

1. 輸入&#x200B;**[!UICONTROL Name]**、**[!UICONTROL Description]**&#x200B;以及接收履行請求的&#x200B;**[!UICONTROL API URL]**。

1. 視需要為您的API新增&#x200B;**[!UICONTROL 標題]** （例如API金鑰或內容型別）。

1. 設定&#x200B;**[!UICONTROL 獎勵定義]** — 您的提供者支援的每種獎勵型別（例如方案點數或星星）各一個專案。 對於每個定義：

   * 指定隨履行呼叫傳送的&#x200B;**裝載**。
   * 可選擇將這個提供者的一個定義標示為&#x200B;**預設**。

1. 選擇性地設定&#x200B;**[!UICONTROL 獎勵Proxy]**，以透過中繼伺服器路由履行呼叫：

   * **[!UICONTROL 名稱]**、**[!UICONTROL 描述]**，以及Proxy是否已啟用&#x200B;****
   * **[!UICONTROL 主機]**、**[!UICONTROL 連線埠]**&#x200B;和認證

1. 如果您的API需要持有人權杖來進行驗證，請設定&#x200B;**[!UICONTROL 驗證權杖產生器]**：

   * 權杖端點URL和HTTP方法（例如，OAuth樣式流程的&#x200B;**POST**）
   * 回應中的&#x200B;**[!UICONTROL Token金鑰]** （例如`access_token`）
   * 您的權杖端點所需的標頭

   Journey Optimizer在呼叫您的獎勵API之前，使用此設定來取得新權杖。

1. 選取&#x200B;**[!UICONTROL 建立獎勵提供者]**。 提供者和所有已設定的子資源會一起儲存。

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

儲存後，提供者會出現在獎勵提供者清單中。 行銷人員在[設定挑戰獎勵](create-challenges.md#rewards)時選取此提供者。

若要編輯現有的獎勵提供者，請開啟&#x200B;**[!UICONTROL 獎勵提供者]**&#x200B;標籤、選取提供者，並更新適當的欄位。 更新子資源（獎勵定義、代理、驗證權杖產生器）時，會儲存這些資源的變更。

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>**[!UICONTROL 攜帶您自己的資料]**&#x200B;挑戰透過您自己的資料整合完成獎勵。 在此設定的獎勵提供者不適用於這些挑戰。 [進一步瞭解如何應對資料挑戰](create-challenges.md#create-the-challenge)。

## 事件定義（選擇性） {#event-definitions}

**[!UICONTROL 事件定義]**&#x200B;將您系統中的體驗事件（無論您的品牌使用什麼JSON或XDM格式）對應至「忠誠度挑戰」可對其採取動作的活動，最明顯的是&#x200B;**[!UICONTROL 自訂事件]**&#x200B;任務。 事件抵達時，Journey Optimizer會使用這些定義來決定是否處理事件。 不符合任何定義的事件會被忽略。

### 建立事件定義 {#create-event-definition}

1. 開啟&#x200B;**[!UICONTROL 事件定義]**&#x200B;標籤，並建立新定義。

1. 輸入事件的&#x200B;**[!UICONTROL 名稱]** （例如，`Coffee purchase`） — 這是行銷人員在設定&#x200B;**[!UICONTROL 自訂事件]**&#x200B;任務時看到的名稱。

1. 指定如何識別傳入裝載中的事件：

   * **[!UICONTROL 識別碼路徑]** — 識別事件或成員的欄位的JSON路徑（例如，`data.memberId`）
   * **[!UICONTROL 識別碼值]** — 必須存在值才能符合此定義

1. 如果您的事件裝載符合Experience Platform結構描述，可選擇指定&#x200B;**[!UICONTROL XDM結構描述識別碼]**。

1. 可選擇使用&#x200B;**[!UICONTROL 結構描述]**&#x200B;和&#x200B;**[!UICONTROL 轉換器]**&#x200B;欄位來提供自訂結構描述和轉換字串，以剖析和驗證傳入的JSON。

   您可以提供XDM結構描述ID和/或識別碼路徑，端視您的事件結構而定。

1. 儲存事件定義。

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

大多陣列織會建立多個事件定義 — 每個要追蹤的活動各一個（例如，購買、入庫或網站造訪）。 [瞭解如何在挑戰中使用自訂事件工作](create-tasks.md#choose-activity)。

## 產品詳細目錄（選擇性） {#product-inventory}

使用&#x200B;**[!UICONTROL 產品詳細目錄]**&#x200B;索引標籤來上傳將產品或專案識別碼（例如MPG ID）對應到產品群組的CSV檔案。 行銷人員隨後可在任務適用性規則中參考這些群組，而非輸入個別SKU。

1. 開啟&#x200B;**[!UICONTROL 產品詳細目錄]**&#x200B;標籤。

1. 上傳您的對應檔案。

1. 檢閱詳細目錄清單中匯入的對應。 選取產品群組以檢視該群組中的所有專案，或使用搜尋來依名稱或ID尋找專案。

1. 使用&#x200B;**[!UICONTROL 上傳記錄]**&#x200B;檢視先前的上傳。

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>針對產品詳細目錄的&#x200B;**[!UICONTROL 全域排除]**&#x200B;計畫於未來版本推出，此處並未記錄。
