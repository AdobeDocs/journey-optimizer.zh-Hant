---
solution: Journey Optimizer
product: journey optimizer
title: 設定您的自訂提供者
description: 瞭解如何設定環境，以透過自訂提供者使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
badge: label="Beta" type="Informative"
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: fc78fcfb0f2ce3616cb8b1df44dda2cfd66262fe
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 設定自訂簡訊提供者 {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="提供者 URL"
>abstract="指定您計劃連線之外部 API 的 URL。此 URL 會做為存取 API 功能的端點。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="標頭參數"
>abstract="指定附加標頭的標籤、類型和值，以啟用正確的驗證、內容格式和有效的 API 通訊。 "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="提供者承載"
>abstract="提供要求承載，確保能發送用於進行處理和產生回應的正確資料。"

>[!AVAILABILITY]
>
>自訂提供者目前僅供選定使用者使用，做為Beta版。 請洽詢您的Adobe代表，以便納入Beta。
>請注意，此Beta不支援選擇加入/選擇退出同意管理和傳遞報告的傳入訊息。


此功能可讓您整合及設定自己的簡訊提供者，提供預設提供者（Sinch、Twilio和Infobip）以外的彈性。 這可讓您順暢地編寫、傳送SMS、製作報表及管理同意。

透過簡訊的自訂提供者設定，您可以：

* 直接在Journey Optimizer中設定自訂SMS提供者。
* 對動態訊息使用進階裝載自訂。
* 管理同意偏好設定（選擇加入/選擇退出）以確保法規遵循。

## 建立您的API認證 {#api-credential}

若要在Journey Optimizer中使用Adobe未提供的現成可用自訂提供者（例如Sinch、Infobip、Twilio）傳送訊息，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 管道]**，選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

   ![](assets/sms_byo_1.png)

1. 設定您的SMS API認證，如下所述：

   * **[!UICONTROL SMS供應商]**：自訂。

   * **[!UICONTROL 名稱]**：輸入您的API認證名稱。

   * **[!UICONTROL 提供者AppId]**：輸入您的SMS提供者提供的應用程式ID。

   * **[!UICONTROL 提供者名稱]**：輸入您的SMS提供者的名稱。

   * **[!UICONTROL 提供者URL]**：輸入簡訊提供者的URL。

   * **[!UICONTROL 驗證型別&#x200B;]**：選取您的授權型別，並根據選取的驗證方法[完成對應的欄位](#auth-options)。

     ![](assets/sms-byop.png)

1. 在&#x200B;**[!UICONTROL 標頭]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 新增引數]**&#x200B;以指定將傳送給外部服務的要求訊息的HTTP標頭。

   **Content-Type**&#x200B;和&#x200B;**Charset**&#x200B;標頭欄位已預設設定，無法刪除。

   ![](assets/sms_byo_2.png)

1. 新增您的&#x200B;**[!UICONTROL 提供者裝載]**，以驗證及自訂您的要求裝載。

   您可以使用設定檔屬性來動態個人化您的裝載，並透過內建的協助程式函式，確保傳送準確資料以供處理和產生回應。
<!--
1. Add your **Inbound settings** to determine how your system handles incoming messages and subscriber preferences: 

    * **[!UICONTROL Inbound Webhook URL]**: Specify the endpoint URL where inbound messages (e.g. replies or new messages from users) are sent.
    * **[!UICONTROL Opt-in Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-In Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-in Message]**: Enter the custom response that is automatically sent as your Opt-In Message.
    * **[!UICONTROL Opt-out Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-Out Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-out Message]**: Enter the custom response that is automatically sent as your Opt-Out Message.
-->

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API認證]**&#x200B;功能表中，按一下bin圖示以刪除您的API認證。

   ![](assets/sms_byo_3.png)

1. 若要修改現有認證，請找到所需的API認證，然後按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;選項以進行必要的變更。

   ![](assets/sms_byo_4.png)

建立和設定API認證後，您現在需要建立SMS訊息的頻道介面。 [了解更多](sms-configuration-surface.md)

設定後，您就可以運用所有立即可用的頻道功能，例如訊息製作、個人化、連結追蹤和報告。

### 自訂SMS提供者的驗證選項 {#auth-options}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="驗證類型"
>abstract="指定存取API所需的驗證方法，以確保與外部服務的安全且授權通訊。"

>[!BEGINTABS]

>[!TAB API金鑰]

建立API認證後，請完成API金鑰驗證所需的欄位：

* **[!UICONTROL 名稱]**&#x200B;：輸入API金鑰組態的名稱。
* **[!UICONTROL API Token]**&#x200B;：輸入您的SMS提供者提供的API Token。

![](assets/sms-byop-api-key.png)

>[!TAB MAC驗證]

建立API認證後，請完成MAC驗證所需的欄位：

* **[!UICONTROL 名稱]**&#x200B;：輸入MAC驗證組態的名稱。
* **[!UICONTROL API Token]**&#x200B;：輸入您的SMS提供者提供的API Token。
* **[!UICONTROL API秘密金鑰]**：輸入您的SMS提供者提供的API秘密金鑰。 此金鑰用於產生MAC （訊息驗證代碼），以進行安全通訊。
* **[!UICONTROL Mac授權雜湊格式]**：選擇MAC驗證的雜湊格式。

![](assets/sms-byop-mac.png)

>[!TAB OAuth驗證]

建立API認證後，請完成OAuth驗證所需的欄位：

* **[!UICONTROL 名稱]**&#x200B;：輸入您OAuth驗證組態的名稱。

* **[!UICONTROL API Token]**&#x200B;：輸入您的SMS提供者提供的API Token。

* **[!UICONTROL OAuth URL]**&#x200B;：輸入用於取得OAuth權杖的URL。

* **[!UICONTROL OAuth內文]**&#x200B;：提供JSON格式的OAuth要求內文，包括`grant_type`、`client_id`和`client_secret`等引數。

![](assets/sms-byop-oauth.png)

>[!TAB JWT驗證]

建立API認證後，請完成JWT驗證所需的欄位：

* **[!UICONTROL 名稱]**&#x200B;：輸入JWT驗證組態的名稱。

* **[!UICONTROL API Token]**&#x200B;：輸入您的SMS提供者提供的API Token。

* **[!UICONTROL JWT裝載]**&#x200B;：輸入包含JWT所需宣告的JSON裝載，例如簽發者、主體、對象和到期日。

![](assets/sms-byop-jwt.png)

>[!ENDTABS]

## 作法影片 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
