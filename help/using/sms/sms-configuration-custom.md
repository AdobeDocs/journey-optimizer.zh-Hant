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
source-git-commit: 201d7d367540f7b36f27ca4a09b6f0ce12e3e22f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 27%

---

# 設定自訂提供者 {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="提供者 URL"
>abstract="指定您計劃連線之外部 API 的 URL。此 URL 會做為存取 API 功能的端點。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="驗證類型"
>abstract="指定存取 API 所需的驗證方法，例如 OAuth 或 Bearer 權杖。這能確保與外部服務的通訊是安全且獲得授權的。"

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
>
>請注意，此Beta不支援選擇加入/選擇退出同意管理和傳遞報告的傳入訊息。

若要在Journey Optimizer中使用Adobe未提供的現成可用自訂提供者（例如Sinch、Infobip、Twilio）傳送訊息，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。

1. 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

   ![](assets/sms_byo_1.png)

1. 設定您的SMS API認證，如下所述：

   * **[!UICONTROL SMS供應商]**：自訂。

   * **[!UICONTROL 名稱]**：輸入您的API認證名稱。

   * **[!UICONTROL 提供者AppId]**：輸入您的SMS提供者提供的應用程式ID。

   * **[!UICONTROL 提供者名稱]**：輸入您的SMS提供者的名稱。

   * **[!UICONTROL 提供者URL]**：輸入簡訊提供者的URL。

   * **[!UICONTROL 驗證型別{&#x200B;1}：選取您的授權型別。]**&#x200B;支援的授權型別為&#x200B;**持有者應用程式**&#x200B;或&#x200B;**基本**。

   * **[!UICONTROL API Token]**：輸入您的SMS提供者提供的API Token。

   * **[!UICONTROL 提供者承載]**：新增您的提供者承載，例如`{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`。

     確定承載包含`{{toNumber}}`、`{{fromNumber}}`、`{{message}}`。

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API認證]**&#x200B;功能表中，按一下bin圖示以刪除您的API認證。

1. 若要修改現有認證，請找到所需的API認證，然後按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;選項以進行必要的變更。

建立和設定API認證後，您現在需要建立SMS訊息的頻道介面。 [了解更多](sms-configuration-surface.md)

設定後，您就可以運用所有立即可用的頻道功能，例如訊息製作、個人化、連結追蹤和報告。

## 作法影片 {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
