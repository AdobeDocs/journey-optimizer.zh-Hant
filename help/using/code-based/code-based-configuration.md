---
title: 程式碼型設定
description: 建立程式碼型設定
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: f715fb9135c446d569a4384ce73e9e92c72cb9ff
workflow-type: tm+mt
source-wordcount: '1558'
ht-degree: 39%

---

# 設定您基於程式碼的體驗 {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="定義基於程式碼的體驗設定"
>abstract="基於程式碼的設定會定義您應用程式中的路徑和位置，由應用程式實作中的 URI 唯一識別，且內容將在其中傳遞和使用。"

在[建置您的體驗](create-code-based.md)之前，您需要建立程式碼型體驗設定，在其中定義內容將在您的應用程式內傳遞和使用的位置。

程式碼型體驗設定必須參考曲面，這基本上是您要呈現變更的位置。 根據所選的平台，您需要輸入位置/路徑，或完整表面URI。 [了解更多](#surface-definition)

## 建立基於程式碼的體驗設定 {#create-code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="表示頁面或應用程式內的特定位置"
>abstract="此欄位會指定您希望使用者存取之頁面或應用程式內的確切目標。它可以是網頁內的特定區段，也可以是應用程式導覽結構深處的頁面。"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="定義內容建立和預覽 URL"
>abstract="此欄位可確保根據規則產生或符合的頁面具有指定的 URL，這對於有效建立和預覽內容至關重要。"

若要建立程式碼型體驗通道設定，請遵循下列步驟：

1. 存取&#x200B;**[!UICONTROL 頻道]** > **[!UICONTROL 一般設定]** > **[!UICONTROL 頻道設定]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 建立頻道設定]**。

   ![](assets/code_config_1.png)

1. 輸入設定的名稱和說明（選擇性）。

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線`_`、點`.`和連字型大小`-`字元。

1. 若要將自訂或核心資料使用標籤指派給組態，您可以選取&#x200B;**[!UICONTROL 管理存取權]**。 [進一步瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md)

1. 選取&#x200B;**[!UICONTROL 行銷動作]**，以使用此設定將同意原則與訊息相關聯。 系統會運用與行銷動作相關的所有同意政策，以尊重客戶的偏好設定。 [了解更多](../action/consent.md#surface-marketing-actions)

1. 選取&#x200B;**程式碼型體驗**&#x200B;管道。

   ![](assets/code_config_2.png)

1. 選取將套用程式碼庫體驗的平台：

   * [Web](#web)
   * [iOS和/或Android](#mobile)
   * [其他](#other)

   >[!NOTE]
   >
   >您可以選取數個平台。 選擇多個平台時，內容會傳遞至所有選取的頁面或應用程式。

1. 為此特定位置選擇應用程式預期的格式。 這將用於編寫行銷活動和歷程中的程式碼型體驗。

   ![](assets/code_config_4.png)

1. 按一下&#x200B;**[!UICONTROL 提交]**&#x200B;以儲存變更。

現在當您在行銷活動和歷程中[建立程式碼型體驗](create-code-based.md)時，可以選取此設定。

>[!NOTE]
>
>您的應用程式實作團隊負責發出明確API或SDK呼叫，以擷取所選程式碼型體驗設定中定義之表面的內容。 在[本節](code-based-implementation-samples.md)中瞭解不同客戶實作的詳細資訊。

### Web 平台 {#web}

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="定義內容製作和預覽 URL"
>abstract="此欄位可確保根據規則產生或符合的頁面具有指定的 URL，這對於有效建立和預覽內容至關重要。"

若要定義Web平台的程式碼型體驗組態設定，請遵循下列步驟。

1. 選取下列其中一個選項：

   * **[!UICONTROL 單頁]** — 如果您只想將變更套用至單頁，請輸入&#x200B;**[!UICONTROL 頁URL]**。

     ![](assets/code_config_single_page.png)

   * **[!UICONTROL 頁面符合規則]** — 若要鎖定多個符合相同規則的URL，請建置一或多個規則。 [了解更多](../web/web-configuration.md#web-page-matching-rule)

     <!--This could be used to apply changes universally across a website, such as updating a hero banner across all pages or adding a top image to display on every product page.-->

     例如，如果您想要編輯顯示在Luma網站所有女性產品頁面上的元素，請選取&#x200B;**[!UICONTROL 網域]** > **[!UICONTROL 開頭為]** > `luma`和&#x200B;**[!UICONTROL 頁面]** > **[!UICONTROL 包含]** > `women`。

     ![](assets/code_config_matching_rules.png)

1. 下列專案適用於預覽URL：

   * 如果輸入單一頁面URL，該URL將用於預覽 — 不需要輸入其他URL。
   * 如果選取了符合規則](../web/web-configuration.md#web-page-matching-rule)的[頁面，您必須輸入預設的撰寫和預覽URL ]**，以便在瀏覽器中預覽體驗。**[!UICONTROL [了解更多](../code-based/create-code-based.md#preview-on-device)

     ![](assets/code_config_matching_rules_preview.png)

1. **[!UICONTROL 頁面]**&#x200B;上的位置欄位會指定您要使用者存取之頁面內的確切目的地。 它可以是網站導覽結構內頁面上的特定區段，例如「hero-banner」或「product-rail」。

   ![](assets/code_config_location_on_page.png)

### 行動平台 (iOS 和 Android) {#mobile}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="提供您的應用程式 ID"
>abstract="輸入應用程式 ID，以便在應用程式的操作環境中進行準確的識別和設定，確保緊密整合和功能。"

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="輸入內容預覽 URL"
>abstract="此欄位對於直接在裝置的應用程式中模擬和預覽內容至關重要。"

若要定義行動平台的程式碼型體驗組態設定，請遵循下列步驟。

1. 輸入您的&#x200B;**[!UICONTROL 應用程式識別碼]**。 這可在應用程式的作業環境中進行準確的識別和設定，並確保順暢的整合和功能。

1. 提供應用程式&#x200B;]**內的**[!UICONTROL &#x200B;位置或路徑。 此欄位會指定您想讓使用者存取的應用程式內的確切目的地。 它可以是應用程式導覽結構中的特定區段或頁面，例如「hero-banner」或「product-rail」。

   ![](assets/code_config_3.png)

1. 填寫&#x200B;**[!UICONTROL 預覽URL]**&#x200B;欄位以啟用裝置上預覽。 此URL會通知預覽服務在裝置上觸發預覽時要使用的特定URL。 [了解更多](../code-based/create-code-based.md#preview-on-device)

   預覽URL是應用程式開發人員在您應用程式內設定的深層連結。 這可確保任何符合深層連結配置的URL都會在應用程式中開啟，而不是在行動網站瀏覽器中開啟。 請聯絡您的應用程式開發人員，取得為您的應用程式設定的深層連結配置。

+++  下列資源可協助您為應用程式實作設定深層連結

   * 若為Android：

      * [建立應用程式內容的深度連結](https://developer.android.com/training/app-links/deep-linking)

   * 若為iOS：

      * [定義您的應用程式的自訂 URL 綱要](https://developer.apple.com/documentation/xcode/defining-a-custom-url-scheme-for-your-app)

      * [支援您的應用程式中的通用連結](https://developer.apple.com/documentation/xcode/supporting-universal-links-in-your-app)

+++

   >[!NOTE]
   >
   >如果您在預覽體驗時遇到問題，請參閱[本檔案](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/troubleshooting#app-does-not-open-link)。

### 其他平台 {#other}

若要定義其他平台（例如視訊主控台、電視連線裝置、智慧型電視、資訊站、ATM、語音助理、物聯網裝置等）的程式碼型體驗組態設定，請遵循下列步驟。

1. 如果您的實作不適用於Web、iOS或Android，或需要鎖定特定的URI，請選取&#x200B;**[!UICONTROL 其他]**&#x200B;作為平台。

1. 輸入&#x200B;**[!UICONTROL 表面URI]**。 表面URI是與您要傳送體驗的實體對應的唯一識別碼。 [了解更多](#surface-definition)

   ![](assets/code_config_5.png)

   >[!CAUTION]
   >
   >請務必輸入與您自己的實施中所使用之URI相符的表面URI。 否則，將無法傳送變更。

1. **[!UICONTROL 視需要新增另一個表面URI]**。 您可以新增最多10個URI。

   >[!NOTE]
   >
   >新增多個URI時，內容會傳遞至所有列出的元件。

## 什麼是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="新增元件的表面 URI"
>abstract="如果您的實作不是針對 Web、iOS 或 Android，或如果您需要以特定 URI 為目標，請輸入表面 URI，它是唯一識別碼，指向您想要提供體驗的實體。確保您輸入的表面 URI 符合您自己的實作中使用的 URI。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/communication-channels/code-based-experience/code-based-configuration#other" text="為其他平台建立基於程式碼的體驗設定"

程式碼型體驗&#x200B;**surface**&#x200B;是任何專為使用者或系統互動而設計的實體，可由&#x200B;**URI**&#x200B;唯一識別。 介面會在應用程式實作中指定，且必須符合程式碼型體驗通道設定中參照的介面。

在任何階層層級中，只要有實體（接觸點）存在，即可將表面視為容器。

* 其可以是網頁、行動應用程式、桌面應用程式，或大型實體內的特定內容位置 (例如`div`) 或非標準顯示模式 (例如，資訊站或桌面應用程式橫幅)。<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 其也可以延伸至內容容器的特定片段，用於非顯示或抽象顯示目的 (例如，傳遞至服務的 JSON Blob)。

* 其也可以是符合各種用戶端介面定義的萬用字元表面 (例如，網站每個頁面上的主圖影像位置可翻譯為表面URI，例如：web://mydomain.com/*#hero_image)。

建立程式碼型Experience Channel設定時，您有兩種方式可根據選取的平台指定表面：

* 針對&#x200B;**[!UICONTROL Web]**、**[!UICONTROL iOS]**&#x200B;和&#x200B;**[!UICONTROL Android]**&#x200B;平台，您必須輸入&#x200B;**位置或路徑**&#x200B;來構成介面。

* 如果平台是&#x200B;**[!UICONTROL Other]**，您必須輸入完整的&#x200B;**表面URI**，如下例所示。

表面URI可作為指向應用程式中不同使用者介面元素或元件的精確識別碼。 表面URI基本上由多個區段組成：

1. **類型**：網頁、行動應用程式、ATM、資訊站、tvcd、服務等
1. **屬性**：頁面 URL 或應用程式套裝
1. **容器**：頁面/應用程式活動上的位置

下表列出各種裝置的一些表面 URI 定義範例。

**網頁與行動裝置**

| 類型 | URI | 說明 |
| --------- | ----------- | ------- | 
| Web | `web://domain.com/path/page.html#element` | 代表特定網域之特定頁面中的個別元素，其中元素可以是標籤，如下列範例中的標籤：hero_banner、top_nav、menu、footer 等。 |
| iOS 應用程式 | `mobileapp://com.vendor.bundle/activity#element` | 代表原生應用程式活動中的特定元素，例如按鈕或其他檢視元素。 |
| Android 應用程式 | `mobileapp://com.vendor.bundle/#element` | 代表原生應用程式中的特定元素。 |

**其他裝置型別**

| 類型 | URI | 說明 |
| --------- | ----------- | ------- | 
| 桌面 | `desktop://com.vendor.bundle/#element` | 代表應用程式中的特定元素，例如按鈕、功能表、主圖橫幅等。 |
| 電視應用程式 | `tvcd://com.vendor.bundle/#element` | 代表智慧型電視或電視連結裝置應用程式的特定元素 - 套裝 ID。 |
| 服務 | `service://servicename/#element` | 代表伺服器端程序或其他手動實體。 |
| 資訊站 | `kiosk://location/screen#element` | 潛在可輕鬆新增的其他表面類型範例。 |
| ATM | `atm://location/screen#element` | 潛在可輕鬆新增的其他表面類型範例。 |

**萬用字元表面**

| 類型 | URI | 說明 |
| --------- | ----------- | ------- | 
| 萬用字元網頁 | `wildcard:web://domain.com/*#element` | 萬用字元表面 - 代表特定網域下每個頁面中的個別元素。 |
| 萬用字元網頁 | `wildcard:web://*domain.com/*#element` | 萬用字元表面 - 代表所有以「domain.com」結尾的網域下每個頁面中的個別元素。 |
