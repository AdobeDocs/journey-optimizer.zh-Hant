---
solution: Journey Optimizer
product: journey optimizer
title: 設定熟客方案
description: 瞭解如何在Adobe Journey Optimizer中設定忠誠計畫的獎勵提供者、事件定義和組織設定。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人測試版" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: e66628ab1d9df497226ab625947aa18a2a3b6f48
workflow-type: tm+mt
source-wordcount: '1221'
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

**[!UICONTROL 忠誠度管理員]**&#x200B;區段是管理員設定Journey Optimizer如何連線至忠誠度計畫後端的地方。 行銷人員使用&#x200B;**[!UICONTROL 忠誠度挑戰(Beta)]**&#x200B;來設計挑戰、工作、內容和訊息；忠誠度管理員是獎勵履行和事件對應的獨立一次性設定。

當客戶完成挑戰（或達到獎勵里程碑）時，Journey Optimizer會呼叫您在此處設定的獎勵提供者，以提供點數或其他獎勵。 挑戰&#x200B;**[!UICONTROL 內容]**、**[!UICONTROL 訊息]**&#x200B;和&#x200B;**[!UICONTROL 對象]**&#x200B;設定不受忠誠度管理員組態的影響。

## 存取忠誠度管理員 {#access-loyalty-admin}

若要開啟「忠誠度管理員」，請登入Journey Optimizer，然後在左側導覽中選取「**[!UICONTROL 忠誠度管理員]**」。

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

管理員介面會整理成標籤。 視您的組織而定，您可能會看到&#x200B;**[!UICONTROL 全域設定]**、**[!UICONTROL 獎勵提供者]**、**[!UICONTROL 事件定義]**&#x200B;以及&#x200B;**[!UICONTROL 產品詳細目錄]**。

## 全域設定 {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="全域設定"
>abstract="選取忠誠度計畫的Adobe Experience Platform身分名稱空間，並複製設定ID。 必須先進行這些組織層級設定，獎勵提供者才能正確履行獎勵。"

使用&#x200B;**[!UICONTROL 全域設定]**&#x200B;來設定忠誠度挑戰的組織範圍選項。

1. 開啟&#x200B;**[!UICONTROL 全域設定]**&#x200B;標籤。

1. 在&#x200B;**[!UICONTROL 名稱空間]**&#x200B;下拉式清單中，從Adobe Experience Platform選取您的熟客方案所使用的[身分名稱空間](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/namespaces)。 選取&#x200B;**[!UICONTROL 儲存]**&#x200B;以更新您組織的「忠誠度挑戰」組態上的名稱空間。

1. 如果您需要與實作團隊或外部系統共用&#x200B;**[!UICONTROL 組態ID]**，請加以複製。

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## 獎勵提供者 {#reward-providers}

**獎勵提供者**&#x200B;會通知Journey Optimizer在記錄挑戰進度或完成挑戰時，將履行呼叫傳送至何處，例如，將忠誠點數或開始點數加到會員帳戶的API。

獎勵提供者包括：

* 基本連線詳細資料（名稱、說明、API URL、標題）
* **[!UICONTROL 獎勵定義]** — 此提供者可以發行的獎勵型別（例如星星或英里）
* **[!UICONTROL 獎賞代理]** （選擇性） — 將呼叫路由透過Proxy，而非直接路由至您的端點
* **[!UICONTROL 驗證權杖產生器]** — Journey Optimizer在呼叫您的API之前如何取得存取權杖

### 建立獎勵提供者 {#create-reward-provider}

請依照下列步驟，註冊新的獎勵提供者及其相關資源。

1. 開啟&#x200B;**[!UICONTROL 獎勵提供者]**&#x200B;標籤，並開始建立提供者。

1. 輸入&#x200B;**[!UICONTROL Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**，然後輸入傳送履行請求的&#x200B;**[!UICONTROL API URL]**。

1. 視需要為您的API新增&#x200B;**[!UICONTROL 標題]** （例如API金鑰或內容型別）。 您可以在UI中新增或移除標題列。

1. 設定&#x200B;**[!UICONTROL 獎勵定義]**：

   * 定義提供者支援的每種獎勵型別（例如方案點數或星星）。
   * 可選擇將某個定義標示為該提供者的&#x200B;**預設**。
   * 指定每個定義隨履行呼叫傳送的&#x200B;**裝載**。

1. 選擇性地設定&#x200B;**[!UICONTROL 獎勵Proxy]**：

   * **[!UICONTROL 主機]**、**[!UICONTROL 連線埠]**&#x200B;和認證
   * **[!UICONTROL 名稱]**、**[!UICONTROL 描述]**，以及Proxy是否已啟用&#x200B;**&#x200B;**

1. 若您的API在每次呼叫前都需要權杖，請設定&#x200B;**[!UICONTROL 驗證權杖產生器]**：

   * 權杖端點URL和HTTP方法（例如，OAuth樣式流程的&#x200B;**POST**）
   * 回應中的&#x200B;**[!UICONTROL Token金鑰]** （例如`access_token`）
   * 您的權杖端點所需的標頭

   Journey Optimizer會在呼叫您的獎勵API之前，要求此設定的Token，讓呼叫使用目前的認證。

1. 選取&#x200B;**[!UICONTROL 建立獎勵提供者]**。 提供者及其子資源（定義、Proxy和權杖產生器）會一起建立。

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

建立後，提供者會出現在獎勵提供者清單中。 行銷人員在[設定挑戰獎勵](create-challenges.md#rewards)時選取此提供者。

### 編輯獎勵提供者 {#edit-reward-provider}

1. 開啟&#x200B;**[!UICONTROL 獎勵提供者]**&#x200B;標籤，然後選取提供者。

1. 視需要更新提供者的名稱、說明、URL或標頭。

1. 若要變更&#x200B;**[!UICONTROL 獎勵定義]**、**[!UICONTROL 獎勵代理]**&#x200B;或&#x200B;**[!UICONTROL 驗證權杖產生器]**，請開啟對應的區段並編輯欄位。 當您就地更新這些子資源時，會儲存對這些子資源的變更。

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>針對&#x200B;**[!UICONTROL 自備資料]**&#x200B;挑戰，若工作與獎勵完全來自資料整合，則此處設定的獎勵提供者可能不適用。 [進一步瞭解如何應對資料挑戰](create-challenges.md#create-the-challenge)。

## 事件定義 {#event-definitions}

**[!UICONTROL 事件定義]**&#x200B;將您品牌格式的傳入體驗事件對應至忠誠度挑戰可以使用的活動，特別是&#x200B;**[!UICONTROL 自訂事件]**&#x200B;工作。 當資料從您的管道抵達時，Journey Optimizer會使用這些定義來判斷某個事件是否相關以及如何解譯。 不符合任何定義的事件會被忽略。

### 建立事件定義 {#create-event-definition}

1. 開啟&#x200B;**[!UICONTROL 事件定義]**&#x200B;標籤，並建立新定義。

1. 輸入事件的&#x200B;**[!UICONTROL 名稱]** （例如，`Coffee purchase`）。 這是行銷人員在設定&#x200B;**[!UICONTROL 自訂事件]**&#x200B;任務時選取的名稱。

1. 指定如何識別傳入裝載中的事件：

   * **[!UICONTROL 識別碼路徑]** — 識別事件或成員的欄位的JSON路徑（例如，`data.memberId`）
   * **[!UICONTROL 識別碼值]** — 必須存在值才能符合此定義

1. 選擇性地指定&#x200B;**[!UICONTROL XDM結構描述識別碼]**&#x200B;和/或使用&#x200B;**[!UICONTROL 結構描述]**&#x200B;和&#x200B;**[!UICONTROL 轉換器]**&#x200B;欄位，貼上您的團隊在處理之前用來剖析和驗證傳入JSON的結構描述和轉換字串。

   您可以提供XDM結構描述ID和/或識別碼路徑，端視您的事件結構而定。

1. 儲存事件定義。

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

大多陣列織會建立多個事件定義 — 每個要追蹤的活動各一個（例如購買、入庫或網站造訪）。 [瞭解如何在挑戰中使用自訂事件工作](create-tasks.md#choose-activity)。

## 產品詳細目錄 {#product-inventory}

**[!UICONTROL 產品詳細目錄]**&#x200B;索引標籤可讓您上傳CSV檔案，以將產品或專案識別碼（例如MPG ID）對應到用於工作資格的產品群組。 這支援任務參考分組產品而不是手動輸入的個別SKU的情況。

1. 開啟&#x200B;**[!UICONTROL 產品詳細目錄]**&#x200B;標籤。

1. 將對應檔案拖曳至上傳區域或瀏覽以選取它，即可上傳對應檔案。

1. 檢閱詳細目錄清單中匯入的對應。 選取產品群組以檢視該群組中的所有專案。 使用搜尋來依名稱或ID尋找專案。

1. 使用&#x200B;**[!UICONTROL 上傳記錄]**&#x200B;檢視先前的上傳。

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>針對產品詳細目錄的&#x200B;**[!UICONTROL 全域排除]**&#x200B;計畫於未來版本推出，此處並未記錄。

## 忠誠度管理如何與挑戰相關 {#how-admin-relates-to-challenges}

| 區域圖 | 在熟客方案管理員中設定 | 在忠誠度挑戰中設定 |
|------|----------------------------|----------------------------------|
| 獎勵履行API | 是 — 獎勵提供者 | 否 — 僅選取提供者和金額 |
| 自訂活動的事件對應 | 是 — 事件定義 | 否 — 在自訂事件工作上選取事件名稱 |
| 產品群組對應 | 是 — 產品詳細目錄 | 否 — 在編寫購買/支出任務時使用群組 |
| 挑戰結構、內容、對象 | 無 | 是 |

一般設定順序：

1. 在熟客管理中設定&#x200B;**[!UICONTROL 全域設定]**&#x200B;以及至少一個&#x200B;**[!UICONTROL 獎勵提供者]**。
1. 如果您的程式使用自訂事件或CSV型產品群組，可選擇新增&#x200B;**[!UICONTROL 事件定義]**&#x200B;和&#x200B;**[!UICONTROL 產品詳細目錄]**。
1. 在&#x200B;**[!UICONTROL 忠誠度挑戰(Beta)]**&#x200B;中建立[工作](create-tasks.md)和[挑戰](create-challenges.md)，選取您設定的獎勵提供者和定義。

當客戶獲得獎勵時，Adobe Journey Optimizer會傳送履行呼叫給您的提供者；您的忠誠度平台擁有會員帳戶的退款。

## 先決條件 {#prerequisites}

忠誠度管理適用於貴組織中的少數管理員。 除了[忠誠度挑戰](get-started.md#prerequisites)所需的許可權之外，您還需要存取權來設定組織層級的忠誠度設定。

如果&#x200B;**[!UICONTROL 忠誠度管理員]**&#x200B;未出現在左側導覽中，或您無法儲存全域設定或獎勵提供者，請聯絡您的管理員。
