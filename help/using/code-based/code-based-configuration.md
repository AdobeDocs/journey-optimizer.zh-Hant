---
title: 程式碼型設定
description: 建立程式碼型設定
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: 77e2892dc188ebdd79031792434b4f55913ee811
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 50%

---

# 設定您基於程式碼的體驗 {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="應用程式 ID"
>abstract="提供應用程式 ID，以便在應用程式的操作環境中進行準確的識別和設定，確保緊密整合和功能。"

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="頁面上的位置"
>abstract="應用程式欄位內的位置或路徑會指定您希望使用者存取應用程式內的確切目標。這可能是應用程式導覽結構深處的特定區段或頁面。"

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="表面 URI"
>abstract="表面 URI 是作為精確的識別碼使用，會指向應用程式內的不同使用者介面元素或元件。"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="預設製作和預覽 URL"
>abstract="此欄位可確保根據規則產生或符合的頁面具有指定的 URL，這對於有效建立和預覽內容至關重要。"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="預設製作和預覽 URL"
>abstract="此欄位可確保根據規則產生或符合的頁面具有指定的 URL，這對於有效建立和預覽內容至關重要。"

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="預覽 URL"
>abstract="此欄位對於直接在裝置的應用程式中模擬和預覽內容至關重要。"

## 建立管道設定 {#reatte-code-based-configuration}

若要建立通道設定，請遵循下列步驟：

1. 存取&#x200B;**[!UICONTROL 頻道]** > **[!UICONTROL 一般設定]** > **[!UICONTROL 頻道設定]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 建立頻道設定]**。

   ![](assets/code_config_1.png)

1. 輸入設定的名稱和說明（選擇性）。

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線`_`、點`.`和連字型大小`-`字元。

1. 若要將自訂或核心資料使用標籤指派給組態，您可以選取&#x200B;**[!UICONTROL 管理存取權]**。 [進一步瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md)。

1. 選取&#x200B;**[!UICONTROL 行銷動作]**，以使用此設定將同意原則與訊息相關聯。 系統會運用與行銷動作相關的所有同意政策，以尊重客戶的偏好設定。 [了解更多](../action/consent.md#surface-marketing-actions)

1. 選取&#x200B;**程式碼型體驗**&#x200B;管道。

   ![](assets/code_config_2.png)

1. 選取將套用程式碼庫體驗的平台。

1. 針對Web：

   * 指定&#x200B;**[!UICONTROL 頁面URL]**，將變更僅套用至單一頁面。

   * 或是建立符合規則&#x200B;]**的**[!UICONTROL &#x200B;頁面，以鎖定多個符合指定規則的URL。 例如，這可用來在網站上通用套用變更，例如更新所有頁面的主圖橫幅，或新增頂端影像以顯示於每個產品頁面上。 [了解更多](../web/web-configuration.md)

1. 對於iOS和Android：

   * 輸入您的&#x200B;**[!UICONTROL 應用程式ID]**&#x200B;和&#x200B;**[!UICONTROL 應用程式]**&#x200B;內的位置或路徑。

     ![](assets/code_config_3.png){width="500"}

1. 如果您的實作不適用於Web、iOS或Android，或您需要鎖定特定URI，請選取「其他」作為平台。 選擇多個平台或新增多個URI時，內容將會傳送至所有選取的頁面或應用程式。

   * 輸入&#x200B;**[!UICONTROL 表面URI]**。

   >[!CAUTION]
   >
   >請確定您的程式碼型行銷活動中使用的表面URI與您自己的實施中使用的表面URI相符。 否則，將不會傳送變更。

1. 填寫&#x200B;**[!UICONTROL 預覽URL]**&#x200B;欄位以啟用裝置上預覽。 此URL會通知預覽服務在觸發預覽時要使用的特定URL。

   * 針對Web：

      * 如果輸入單一頁面URL，該URL將用於預覽。
      * 如果選取了頁面比對規則，您必須輸入預設預覽URL，此URL將用於預覽瀏覽器中的體驗。

   * 針對行動平台(iOS / Android)：

      * 預覽URL是應用程式開發人員在您的應用程式中設定的深層連結。 這可確保任何符合深層連結配置的URL都將在應用程式中開啟，而不是在行動網頁瀏覽器中開啟。 請連絡您的應用程式開發人員，取得為您的應用程式設定的深層連結配置。

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

1. 選擇應用程式在該特定位置所預期的格式。 這將用於編寫行銷活動和歷程中的程式碼型體驗。

1. 提交變更。

您現在可以在建立程式碼型體驗時選取設定。


## 什麼是表面？ {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="定義以程式碼為主的體驗設定"
>abstract="以程式碼為主的設定會定義您應用程式中的路徑和位置，由應用程式實作中的 URI 唯一識別，且內容將在其中傳遞和使用。"

**程式碼型體驗介面**&#x200B;是任何專為使用者或系統互動而設計的實體，可由URI唯一識別。 介面會在應用程式實作中指定，且應該與程式碼型體驗通道設定中的介面相對應。

建立程式碼型體驗管道設定時 — 針對Web、iOS和Android平台，您需要輸入路徑和位置來撰寫表面，而如果平台為「其他」，則需要輸入完整的URI，如下例所示。

換言之，可將表面視為位於任何有實體 (接觸點) 存在之階層層級的容器。<!--good idea to illustrate how it can be seen, but to clarify-->

* 其可以是網頁、行動應用程式、桌面應用程式，或大型實體內的特定內容位置 (例如`div`) 或非標準顯示模式 (例如，資訊站或桌面應用程式橫幅)。<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* 其也可以延伸至內容容器的特定片段，用於非顯示或抽象顯示目的 (例如，傳遞至服務的 JSON Blob)。

* 其也可以是符合各種用戶端介面定義的萬用字元表面 (例如，網站每個頁面上的主圖影像位置可翻譯為表面URI，例如：web://mydomain.com/*#hero_image)。

基本上，表面 URI 由多個區段組成：
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
