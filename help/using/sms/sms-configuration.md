---
solution: Journey Optimizer
product: journey optimizer
title: 設定簡訊頻道
description: 瞭解如何設定您的環境，以使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: f275820c3f79bb4c9aca8593c2c761ccd4283795
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 13%

---

# 設定簡訊頻道 {#sms-configuration}

傳送SMS前，您必須設定Adobe Journey Optimizer環境。 若要執行這項作業：

* [整合提供者設定](#create-api) 使用Journey Optimizer
* [建立簡訊表面](#message-preset-sms) （即簡訊預設集）

這些步驟必須由Adobe Journey Optimizer執行 [系統管理員](../start/path/administrator.md).

## 先決條件{#sms-prerequisites}

Adobe Journey Optimizer目前與獨立於Adobe Journey Optimizer提供文字訊息服務的第三方提供者整合。 支援的文字訊息提供者包括： **Sinch**， **Twilio** 和 **Infobip**.

在設定SMS頻道之前，您必須與以下其中一個提供者建立帳戶，以取得 **API Token** 和 **服務ID**，您需要設定Adobe Journey Optimizer與適用提供者之間的連線。

您對簡訊服務的使用受限於適用提供者的其他條款與條件。 作為協力廠商解決方案，Adobe Journey Optimizer使用者可透過整合使用Sinch、Twilio和Infobip。 Adobe不會控制，且對協力廠商產品不負任何責任。 如有任何與簡訊服務相關的問題或需要協助的要求，請連絡您的提供者。

>[!CAUTION]
>
>若要存取及編輯SMS子網域，您必須擁有 **[!UICONTROL 管理SMS子網域]** 生產沙箱的許可權。 進一步瞭解中的許可權 [此頁面](../administration/high-low-permissions.md#administration-permissions).
>

## 建立新的 API 認證 {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="使用 Journey Optimizer 設定您的 SMS 服務提供者"
>abstract="Adobe Journey Optimizer 會透過 SMS 服務提供者發送文字簡訊。選取您的服務提供者並填寫您的 API 認證。"

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="使用 Journey Optimizer 設定您的 MMS 服務提供者"
>abstract="Adobe Journey Optimizer 會透過 MMS 服務提供者發送媒體內容。選取您的服務提供者並填寫您的 API 認證。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="使用 Journey Optimizer 設定您的 SMS 服務提供者"
>abstract="在傳送文字訊息之前，您必須整合提供者設定與Journey Optimizer。 完成後，您需要建立SMS表面。 這些步驟必須由 Adobe Journey Optimizer 系統管理員執行。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=zh-Hant#message-preset-sms" text="建立簡訊管道表面"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="選取簡訊供應商設定"
>abstract="選取為您的簡訊供應商設定的 API 憑證。"

若要使用Journey Optimizer設定簡訊提供者，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL API認證]** 功能表。 按一下 **[!UICONTROL 建立新的API認證]** 按鈕。

   ![](assets/sms_6.png)

1. 設定您的SMS API認證，如下所述。

   ![](assets/sms_7.png)

   * +++ 的 **[!DNL Sinch]**

      * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

      * **[!UICONTROL 服務ID]** 和 **[!UICONTROL API Token]**：存取API頁面，您可以在SMS標籤下找到您的認證。 進一步瞭解 [Sinch檔案](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

      * **[!UICONTROL 選擇加入訊息]**：輸入自訂回應，此回應會作為 **[!UICONTROL 選擇加入訊息]**.

      * **[!UICONTROL 選擇退出訊息]**：輸入自訂回應，此回應會作為 **[!UICONTROL 選擇退出訊息]**.

      * **[!UICONTROL 說明訊息]**：輸入自訂回應，此回應會作為 **說明訊息**.

      * **[!UICONTROL 雙重選擇加入關鍵字]**：輸入觸發雙重加入流程的關鍵字。 如果使用者設定檔不存在，則會在成功確認時加以建立。對於多個關鍵字，請使用逗號分隔值。 [進一步瞭解簡訊雙重選擇加入](https://video.tv.adobe.com/v/3427129/?learn=on).

      * **[!UICONTROL 雙重選擇加入訊息]**：輸入自動傳送以回應雙重選擇加入確認的自訂回應。
+++

   * +++ 的 **[!DNL Twilio]**

      * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

      * **[!UICONTROL 帳戶SID]** 和 **[!UICONTROL 驗證權杖]**：存取Twilio主控台控制面板頁面的「帳戶資訊」窗格，以尋找您的認證。

      * **[!UICONTROL 訊息SID]**：輸入指派給Twilio API所建立每則訊息的唯一識別碼。 進一步瞭解 [Twilio檔案](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

+++

   * +++ 的 **[!DNL Infobip]**

      * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

      * **[!UICONTROL API基底URL]** 和 **[!UICONTROL API權杖]**：存取您的網頁介面首頁或API金鑰管理頁面以尋找您的認證。 進一步瞭解 [Infobip檔案](https://www.infobip.com/docs/api){target="_blank"}.

      * **[!UICONTROL 雙重選擇加入關鍵字]**：輸入觸發雙重加入流程的關鍵字。 如果使用者設定檔不存在，則會在成功確認時加以建立。對於多個關鍵字，請使用逗號分隔值。

      * **[!UICONTROL 雙重選擇加入訊息]**：輸入自動傳送以回應雙重選擇加入確認的自訂回應。

      * **[!UICONTROL 主體實體ID]**：輸入您指派的DLT主要實體識別碼。

      * **[!UICONTROL 內容範本ID]**：輸入您註冊的DLT內容範本ID。

      * **[!UICONTROL 有效期]**：輸入訊息有效期（小時）。 如果在此時間範圍內無法傳遞訊息，系統會再次嘗試重新傳送訊息。 預設有效期設定為48小時。

      * **[!UICONTROL 回呼資料]**：輸入要在通知URL上傳送的其他使用者端資料。
+++

<!--
    * +++ For **[!DNL Sinch MMS]**

        * **[!UICONTROL Name]**: choose a name for your API Credential.

        * **[!UICONTROL Project ID]**, **[!UICONTROL App ID]** and **[!UICONTROL API Token]**: from the Conversation API menu, you can find your credentials in the App menu. Learn more in [Sinch Documentation](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html){target="_blank"}.

        +++ 
-->
1. 按一下 **[!UICONTROL 提交]** 完成API認證的設定時。

建立和設定API認證後，您現在需要建立SMS訊息的頻道介面（即訊息預設集）。

## 建立簡訊表面 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定義訊息類別。"
>abstract="選取使用此表面的文字簡訊類型：需要使用者同意的促銷簡訊的行銷訊息，或非商業簡訊的交易型訊息，例如密碼重設。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=zh-Hant#sms-opt-out-management" text="選擇不接收行銷文字簡訊"

設定您的SMS頻道後，您必須建立頻道介面才能從傳送SMS訊息 **[!DNL Journey Optimizer]**.

若要建立管道曲面，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL 品牌化]** > **[!UICONTROL 管道表面]**. 按一下 **[!UICONTROL 建立管道表面]** 按鈕。

   ![](assets/preset-create.png)

1. 輸入表面的名稱和說明（選擇性），然後選取SMS通道。

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 和連字型大小 `-` 個字元。

1. 定義 **簡訊設定**.

   ![](assets/sms-surface-settings.png)

   首先，選取 **[!UICONTROL 簡訊型別]** 將與介面一併傳送的郵件： **[!UICONTROL 異動]** 或 **[!UICONTROL 行銷]**.

   * 選擇 **行銷** 促銷文字訊息：這些訊息需要使用者同意。
   * 選擇 **異動** 非商業訊息，例如訂單確認、密碼重設通知或傳遞資訊。

   建立SMS訊息時，您必須選擇與您為訊息選取的類別相符的有效頻道介面。

   >[!CAUTION]
   >
   >**異動** 可將訊息傳送給取消訂閱行銷通訊的設定檔。 這些訊息只能在特定內容中傳送。

1. 選取 **[!UICONTROL 簡訊設定]** 以與曲面相關聯。

   有關如何設定環境以傳送SMS訊息的詳細資訊，請參閱 [本節](#create-api).

1. 輸入 **[!UICONTROL 寄件者號碼]** 您&#x200B;要用於通訊。

1. 選取您的 **[!UICONTROL 簡訊執行欄位]** 以選取 **[!UICONTROL 設定檔屬性]** 與設定檔的電話號碼相關聯。

1. 如果您想要在SMS訊息中使用URL縮短功能，請從 **[!UICONTROL 子網域]** 清單。

   >[!NOTE]
   >
   >若要能夠選取子網域，請確定您先前已設定至少一個SMS子網域。 [了解作法](sms-subdomains.md)

1. 輸入 **[!UICONTROL 選擇退出號碼]** 您要用於此曲面。 當設定檔選擇退出此號碼時，您仍然可以從其他號碼傳送訊息給設定檔，您可能會使用其他號碼傳送文字訊息： [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >在 [!DNL Journey Optimizer]，頻道層級不再管理選擇退出簡訊。 它現在特定於數字。

1. 設定好所有引數後，按一下 **[!UICONTROL 提交]** 以確認。 您也可以將管路曲面儲存為草繪，並稍後恢復其組態。

   ![](assets/sms-submit-surface.png)

1. 建立管道曲面後，它會顯示於清單中，其中包含 **[!UICONTROL 處理中]** 狀態。

   >[!NOTE]
   >
   >如果檢查不成功，請在中進一步瞭解可能的失敗原因 [本節](#monitor-channel-surfaces).

1. 檢查成功後，管道表面會取得 **[!UICONTROL 作用中]** 狀態。 已準備好用於傳遞訊息。

   ![](assets/preset-active.png)

您現在可以使用Journey Optimizer傳送簡訊。

**相關主題**

* [建立文字訊息](create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [在行銷活動中新增訊息](../campaigns/create-campaign.md)

