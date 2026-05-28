---
solution: Journey Optimizer
product: journey optimizer
title: 設定忠誠度挑戰
description: 瞭解如何在Adobe [!DNL Journey Optimizer]中設定忠誠度挑戰的獎勵提供者、事件定義、產品詳細目錄、排除和組織層級設定。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人測試版" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
feature_v2: []
subfeature_v2: []
source-git-commit: 2e01cd1880b8527911376d94188d0204f7649541
workflow-type: tm+mt
source-wordcount: 1642
ht-degree: 1%

---

# 設定忠誠度挑戰 {#loyalty-admin}

<!-- Unpublished draft: Loyalty Admin UI documentation is not validated for Experience League. This page uses hide: true until review. -->

>[!BEGINSHADEBOX]

**目錄**

[開始應對忠誠度挑戰](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**建立和管理挑戰**

* [存取及管理挑戰與工作](access-loyalty-challenges.md)
* [創造挑戰](create-challenges.md)
* [建立任務](create-tasks.md)
* [監視忠誠度挑戰績效](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**設定並整合**

* **設定忠誠度挑戰** ◀︎ **您在這裡**
* [熟客資料與資料集](loyalty-data-and-datasets.md)
* [忠誠度挑戰API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中。 如需[!DNL Journey Optimizer]中發行週期與可用性階段的完整詳細資訊，請參閱[發行週期](../rn/releases.md)。

## 概觀 {#access-loyalty-admin}

「忠誠度挑戰」設定會透過在行銷人員撰寫挑戰之前設定獎勵履行、事件對應、產品詳細目錄和排除，將[!DNL Journey Optimizer]連線到您的外部忠誠度系統。

>[!NOTE]
>
>除了忠誠度挑戰所需的許可權之外，忠誠度挑戰設定需要管理員存取您的[!DNL Journey Optimizer]執行個體。 請聯絡您的Adobe管理員以取得存取權。

若要開啟設定介面，請從左側導覽選取&#x200B;**[!UICONTROL 忠誠度管理員]**&#x200B;功能表。 介面會整理為標籤：

* **全域設定** — 選取您程式的Experience Platform身分名稱空間。 [瞭解如何設定全域設定](#global-settings)
* **獎勵提供者** — 連線完成客戶進度或完成挑戰時獎勵的API。 [瞭解如何設定獎勵提供者](#reward-providers)
* **事件定義** — 將傳入體驗事件對應至&#x200B;**[!UICONTROL 自訂事件]**&#x200B;工作中所使用的活動。 [瞭解如何設定事件定義](#event-definitions)
* **產品詳細目錄** — 上傳專案對群組的對應，以用於工作適用性規則。 [瞭解如何設定產品詳細目錄](#product-inventory)
* **排除專案** — 上傳整個組織的專案和群組排除專案以進行任務設定。 [瞭解如何設定排除專案](#exclusions)

## 全域設定 {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="全域設定"
>abstract="全域設定可定義忠誠度挑戰的組織層級設定，包括用於識別事件和挑戰中成員的身分名稱空間。"

開啟&#x200B;**[!UICONTROL 全域設定]**&#x200B;標籤，並在&#x200B;**[!UICONTROL 名稱空間]**&#x200B;下拉式清單中選取Adobe Experience Platform [身分識別名稱空間](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/namespaces)以利忠誠度挑戰。 此名稱空間必須符合在您的資料中識別成員設定檔的方式。

![](assets/admin-global-settings.png)

➡️ [瞭解如何使用身分識別名稱空間](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/namespaces){target="_blank"}

## 獎勵提供者 {#reward-providers}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers"
>title="獎勵提供者"
>abstract="獎勵提供者定義外部系統，當客戶完成挑戰時，[!DNL Journey Optimizer]會呼叫此外部系統以履行獎勵。 設定每個整合的提供者端點、獎勵定義、Proxy設定和驗證。"

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers_connection"
>title="獎勵提供者連線"
>abstract="設定[!DNL Journey Optimizer]如何連線至您的獎勵API：提供者名稱、說明、端點URL，以及履行呼叫所需的HTTP標頭。"

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers_details"
>title="獎勵定義"
>abstract="獎勵定義會指定此提供者可以發行的每個獎勵型別（例如，點數或星號），以及完成獎勵時傳送的裝載[!DNL Journey Optimizer]。"

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers_proxy"
>title="獎勵Proxy"
>abstract="可選擇透過Proxy伺服器路由履行呼叫，而非直接傳送至您的獎勵API端點。 設定主機、連線埠、證明資料，以及是否已啟用Proxy。 認證值通常看起來像： `{ "userName": "test", "password": "xxxx" }`"

**獎勵提供者**&#x200B;會通知[!DNL Journey Optimizer]當記錄挑戰進度或完成挑戰時，要將履行呼叫傳送到何處。 例如，將忠誠度點數或起點數歸於成員帳戶的API。

若要建立獎勵提供者，請遵循下列步驟：

1. 開啟&#x200B;**[!UICONTROL 獎勵提供者]**&#x200B;索引標籤，然後選取&#x200B;**[!UICONTROL 建立獎勵提供者]**。

   ![](assets/admin-reward.png)

1. 輸入&#x200B;**[!UICONTROL 名稱]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 在&#x200B;**[!UICONTROL URL]**&#x200B;欄位中，輸入接收履行請求的API端點。

1. 視需要為您的API新增&#x200B;**[!UICONTROL 標題]** （例如API金鑰或內容型別）。

1. 設定與您的獎勵提供者相關聯的資源。 展開下列每個區段以取得欄位詳細資訊：

   +++獎勵定義

   針對您的提供者支援的獎勵型別（例如方案點數、星級或貨幣信用），新增一個專案。 對於每個定義：

   * 輸入&#x200B;**[!UICONTROL 名稱]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。
   * 指定定義是否為&#x200B;**[!UICONTROL 已啟用]**。
   * 切換&#x200B;**[!UICONTROL 預設]**，將一個定義標示為此提供者的預設。
   * 定義隨履行呼叫傳送的&#x200B;**裝載**。

   ![](assets/admin-reward-definition.png)

   +++

   +++獎勵Proxy

   透過中繼伺服器路由履行呼叫，而非直接傳送至您的端點。 在獎勵提供者和&#x200B;**[!UICONTROL 建立Proxy]**&#x200B;畫面上，使用&#x200B;**[!UICONTROL 認證]**&#x200B;欄位進行Proxy驗證。

   * 輸入&#x200B;**[!UICONTROL 名稱]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。
   * 輸入&#x200B;**[!UICONTROL 主機]**&#x200B;和&#x200B;**[!UICONTROL 連線埠]**。
   * 指定代理伺服器是否為&#x200B;**[!UICONTROL 已啟用]**。
   * 在&#x200B;**[!UICONTROL 認證]**&#x200B;中，以JSON格式輸入Proxy使用者名稱和密碼。 認證值通常看起來像：

     ```json
     { "userName": "test", "password": "xxxx" }
     ```

   ![](assets/admin-reward-proxies.png)

   +++

   +++驗證權杖產生器

   當您的API需要持有人權杖或類似驗證時使用。

   * 輸入&#x200B;**[!UICONTROL 名稱]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。
   * 在&#x200B;**[!UICONTROL 驗證型別]**&#x200B;中，輸入驗證型別（例如，持有人）。
   * 選取HTTP方法（例如POST）。
   * 輸入權杖端點URL和回應中的&#x200B;**[!UICONTROL 權杖金鑰]** （例如`access_token`）。
   * 指定驗證權杖產生器是否為&#x200B;**[!UICONTROL 已啟用]**。
   * 新增您的權杖端點所需的任何標頭。

   [!DNL Journey Optimizer]會使用此設定，在每次呼叫您的獎勵API之前取得新的Token。

   ![](assets/admin-reward-auth.png)

   +++

1. 選取&#x200B;**[!UICONTROL 建立獎勵提供者]**。 提供者和所有已設定的資源會一起儲存。

儲存後，提供者會出現在獎勵提供者清單中。 行銷人員在設定挑戰獎勵時可加以選取。 [瞭解如何設定挑戰獎勵](create-challenges.md#rewards)

若要編輯獎勵提供者，請開啟&#x200B;**[!UICONTROL 獎勵提供者]**&#x200B;標籤、選取提供者，並更新適當的欄位。 獎勵定義、代理和驗證權杖產生器的變更會在您更新時自動儲存。

>[!NOTE]
>
>**[!UICONTROL 攜帶您自己的資料]**&#x200B;挑戰透過您自己的資料整合完成獎勵。 在此設定的獎勵提供者不適用於這些挑戰。 [瞭解如何建立您自己的資料挑戰](create-challenges.md#create-the-challenge)

## 事件定義 {#event-definitions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_event_definitions"
>title="事件定義"
>abstract="事件定義會告知[!DNL Journey Optimizer]如何識別和解譯來自您外部來源的傳入事件資料。 每個定義都會對應特定事件型別（例如購買或簽到），以便系統可追蹤客戶完成挑戰任務的進度。"

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_event_schema"
>title="事件結構描述和轉換器"
>abstract="當您的組織以自訂JSON格式傳送事件時，請使用&#x200B;**[!UICONTROL 結構描述]**&#x200B;來驗證裝載，並使用&#x200B;**[!UICONTROL 轉換器]** （例如JSONata運算式）將欄位對應到忠誠度挑戰期望的格式。"

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_event_identification"
>title="事件識別"
>abstract="指定[!DNL Journey Optimizer]如何使用識別碼路徑、識別碼值、XDM結構描述ID或這些欄位的組合，來辨識傳入裝載中的事件。"

**[!UICONTROL 事件定義]**&#x200B;告知[!DNL Journey Optimizer]要處理哪些傳入的Adobe Experience Platform體驗事件。 例如，購買或飯店簽到。 行銷人員在任務產生器中建立&#x200B;**[!UICONTROL 自訂事件]**&#x200B;任務時，會參考這些定義。 不符合任何定義的事件會被忽略。

當您的組織以自己的JSON格式傳送事件時，**[!UICONTROL 結構描述]**&#x200B;和&#x200B;**[!UICONTROL 轉換器]**&#x200B;會協助[!DNL Journey Optimizer]驗證承載、剖析該承載，並決定是否追蹤活動。

若要建立事件定義，請遵循下列步驟：

1. 開啟&#x200B;**[!UICONTROL 事件定義]**&#x200B;標籤，並建立新定義。

   ![](assets/admin-event-definition.png)

1. 輸入事件的&#x200B;**[!UICONTROL 名稱]** （例如，`Coffee purchase`）。 行銷人員在設定&#x200B;**[!UICONTROL 自訂事件]**&#x200B;任務時看到此名稱。

1. 指定[!DNL Journey Optimizer]如何辨識傳入裝載中的事件。 提供&#x200B;**[!UICONTROL 識別碼路徑]**、**[!UICONTROL XDM結構描述識別碼]**，或兩者皆提供：

   * **[!UICONTROL 識別碼路徑]** — 裝載中欄位的路徑（例如，`data.memberId`）。 依承載中的值比對事件時，請使用此選項。
   * **[!UICONTROL 識別碼值]** — 識別碼路徑上的值必須存在，才能符合此定義。
   * **[!UICONTROL XDM結構描述ID]** — 此事件型別的Experience Platform XDM結構描述識別碼。 在根據已知結構描述擷取事件時，請使用此選項。

1. 如有需要，請將字串貼到&#x200B;**[!UICONTROL 結構描述]**&#x200B;和&#x200B;**[!UICONTROL 轉換器]**&#x200B;中：

   * **[!UICONTROL 結構描述]** — 傳入承載的驗證字串。
   * **[!UICONTROL Transformer]** — 轉換運算式（例如JSONata），可將您的裝載對應至「忠誠度挑戰」所預期的格式。

1. 儲存事件定義。 它出現在&#x200B;**[!UICONTROL 事件定義]**&#x200B;清單中，可在行銷人員建立&#x200B;**[!UICONTROL 自訂事件]**&#x200B;任務時取得。 [瞭解如何建立任務](create-tasks.md#choose-activity)

## 產品詳細目錄 {#product-inventory}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_product_inventory"
>title="產品詳細目錄"
>abstract="上傳將專案識別碼對應至產品群組的CSV檔案。 行銷人員在設定購買和支出任務的合格專案時，無需輸入每個專案ID，即可參考這些群組。"

**[!UICONTROL 產品詳細目錄]**&#x200B;索引標籤會將目錄專案分組，讓行銷人員不必輸入每個專案ID，就能在工作中鎖定這些專案。 上傳將每個專案識別碼對應至一或多個&#x200B;**產品群組**&#x200B;的&#x200B;**CSV檔案** （相同的專案可屬於數個群組）。 設定任務適用性時，可使用匯入的群組。 [瞭解如何建立任務](create-tasks.md)

若要上傳產品詳細目錄檔案，請遵循下列步驟：

1. 準備CSV檔案，將每個專案識別碼對應至一或多個產品群組。 展開以下區段以檢視範例。

   +++產品詳細目錄CSV範例

   ![](assets/admin-inventory-csv.png)

   +++

1. 開啟&#x200B;**[!UICONTROL 產品詳細目錄]**&#x200B;標籤。

1. 選取&#x200B;**[!UICONTROL 上傳]**&#x200B;並選擇您的CSV檔案。

   ![](assets/admin-inventory-upload.png)

1. 檢閱詳細目錄清單中的匯入資料。 清單會為每個專案顯示一列。 包含在&#x200B;**欄中的**&#x200B;群組會將該專案的每個產品群組顯示為藥丸，或當專案屬於多個群組時顯示數個藥丸。

   ![](assets/admin-inventory-imported.png)

1. 若要檢視產品群組中的所有專案，請在任一列的&#x200B;**欄中所包含的**&#x200B;群組中，選取該群組的藥丸。 群組詳細資訊檢視會列出群組中的每個專案。

   ![](assets/admin-inventory-group.png)

1. 開啟&#x200B;**[!UICONTROL 上傳記錄]**&#x200B;以檢視先前的CSV上傳。

## 排除 {#exclusions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_exclusions"
>title="排除"
>abstract="上傳CSV檔案，該檔案定義整個方案已排除的目錄專案和群組。 行銷人員在任務上設定符合資格的專案和排除專案時，匯入的排除群組就會顯示。"

**[!UICONTROL 排除專案]**&#x200B;索引標籤會定義整個方案中排除的目錄專案和群組，因此行銷人員不必在每個任務上列出相同的排除專案。 上傳將每個專案識別碼對應至一或多個&#x200B;**排除群組**&#x200B;的&#x200B;**CSV檔案** （相同的專案可以屬於數個群組）。

匯入後，當行銷人員設定&#x200B;**[!UICONTROL 合格的專案和排除專案]**&#x200B;時，排除的專案和群組會出現在任務產生器中。 [瞭解如何定義任務上的合格專案和排除專案](create-tasks.md#eligible-items-exclusions)

若要上傳排除專案，請執行下列步驟：

1. 準備CSV檔案，將每個專案識別碼對應至一或多個排除群組。 展開以下區段以檢視範例。

   +++排除專案CSV範例

   ![](assets/admin-exclusions-csv.png)

   +++

1. 開啟&#x200B;**[!UICONTROL 排除專案]**&#x200B;標籤。

1. 選取&#x200B;**[!UICONTROL 上傳]**&#x200B;並選擇您的CSV檔案。

   ![](assets/admin-exclusions-upload.png)

1. 檢閱排除專案清單中的匯入資料。 清單會為每個專案顯示一列。 包含在&#x200B;**欄中的**&#x200B;群組會將該專案的每個排除群組顯示為藥丸，或當專案屬於多個群組時顯示數個藥丸。

<!-- SCREENSHOT: Exclusions list after CSV upload -->

1. 若要檢視排除群組中的所有專案，請在任何列的&#x200B;**欄中所包含的**&#x200B;群組中，選取該群組的藥丸。 群組詳細資訊檢視會列出群組中的每個專案。

<!-- SCREENSHOT: Exclusion group details -->

1. 開啟&#x200B;**[!UICONTROL 上傳記錄]**&#x200B;以檢視先前的CSV上傳。
