---
solution: Journey Optimizer
product: journey optimizer
title: 設定簡訊頻道
description: 瞭解如何設定環境，以使用Journey Optimizer傳送簡訊
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: b657f4380026988ac324ee87c96375734a9b3961
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 17%

---

# 設定簡訊頻道 {#sms-configuration}

[!DNL Journey Optimizer] 可讓您建立歷程並傳送訊息給目標對象。

傳送SMS前，請設定您的執行個體。 您需要 [整合提供者設定](#create-api) 使用Journey Optimizer和 [建立簡訊表面](#message-preset-sms) （即簡訊預設集）。 這些步驟必須由 [Adobe Journey Optimizer 系統管理員](../start/path/administrator.md)執行。

## 先決條件{#sms-prerequisites}

Adobe Journey Optimizer目前與Sinch、Twilio和Infobip等協力廠商整合，這些廠商獨立於Adobe Journey Optimizer提供簡訊服務。

在SMS設定之前，您必須與其中一個SMS提供者建立帳戶，以接收API權杖和服務ID，這可讓您在Adobe Journey Optimizer和適用的SMS提供者之間建立連線。

您對簡訊服務的使用將受限於適用簡訊提供者的其他條款與條件。 鑑於Sinch和Twilio是透過整合可供Adobe Journey Optimizer使用者使用的協力廠商產品，如有任何與SMS服務相關的問題或查詢，Sinch或Twilio的使用者需要聯絡適用的SMS提供者以尋求協助。 Adobe無法控制且對協力廠商產品不承擔任何責任。

>[!CAUTION]
>
>若要存取及編輯SMS子網域，您必須擁有 **[!UICONTROL 管理SMS子網域]** 生產沙箱的許可權。

## 建立新的API認證 {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="使用 Journey Optimizer 設定您的簡訊供應商"
>abstract="選取您的供應商並填寫您的簡訊 API 憑證。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="使用 Journey Optimizer 設定您的簡訊供應商"
>abstract="在傳送簡訊之前，您必須將提供者設定和 Journey Optimizer 整合。完成後，您將需要建立一個簡訊表面。這些步驟必須由 Adobe Journey Optimizer 系統管理員執行。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=zh-Hant#message-preset-sms" text="建立簡訊管道表面"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="選取簡訊供應商設定"
>abstract="選取為您的簡訊供應商設定的 API 憑證。"

若要使用Journey Optimizer設定簡訊供應商，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL API認證]** 功能表。 按一下 **[!UICONTROL 建立新的API認證]** 按鈕。

   ![](assets/sms_6.png)

1. 設定您的SMS API認證：

   * 的 **[!DNL Sinch]**：

      * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

      * **[!UICONTROL 服務ID]** 和 **[!UICONTROL API Token]**：存取API頁面，您可以在SMS標籤下找到您的認證。  [了解更多](https://developers.sinch.com/docs/sms/getting-started/)

      * **[!UICONTROL 選擇加入訊息]**：輸入自訂回應，此回應會隨著您的網站自動傳送。 **[!UICONTROL 選擇加入訊息]**.

      * **[!UICONTROL 說明訊息]**：輸入自訂回應，此回應會隨著您的網站自動傳送。 **[!UICONTROL 說明訊息]**.

   * 的 **[!DNL Twilio]**：

      * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

      * **[!UICONTROL 帳戶SID]** 和 **[!UICONTROL 驗證權杖]**：存取Twilio主控台控制面板頁面的「帳戶資訊」窗格，以尋找您的認證。

      * **[!UICONTROL 訊息SID]**：輸入指派給Twilio API所建立每則訊息的唯一識別碼。 [了解更多](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-)

   * 的 **[!DNL Infobip]**：

      * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

      * **[!UICONTROL API基底URL]** 和 **[!UICONTROL API權杖]**：存取您的網頁介面首頁或API金鑰管理頁面以尋找您的認證。 [了解更多](https://www.infobip.com/docs/api)

   ![](assets/sms_7.png)

1. 按一下 **[!UICONTROL 提交]** 完成API認證的設定時。

建立和設定API認證後，您現在需要建立SMS訊息的頻道介面（即訊息預設集）。

## 建立簡訊表面 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定義簡訊類別"
>abstract="選取使用此表面的簡訊類型：需要使用者同意的促銷簡訊的行銷訊息，或非商業簡訊的異動訊息，例如密碼重設。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=zh-Hant#sms-opt-out-management" text="選擇不接收行銷簡訊"

設定您的SMS頻道後，您必須建立頻道介面才能從傳送SMS訊息 **[!DNL Journey Optimizer]**.

若要建立管道曲面，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL 品牌化]** > **[!UICONTROL 管道表面]**. 按一下 **[!UICONTROL 建立管道表面]** 按鈕。

   ![](assets/preset-create.png)

1. 輸入表面的名稱和說明（選擇性），然後選取SMS通道。

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 和連字型大小 `-` 個字元。

1. 定義 **簡訊設定**.

   ![](assets/preset-sms.png)

   * 選取 **[!UICONTROL 簡訊型別]** 將與介面一併傳送的郵件： **[!UICONTROL 異動]** 或 **[!UICONTROL 行銷]**.

      * 選擇 **行銷** 促銷簡訊：這些訊息需要使用者同意。
      * 選擇 **異動** 非商業訊息，例如訂單確認、密碼重設通知或傳遞資訊。

     >[!CAUTION]
     >
     >**異動** SMS訊息可傳送給取消訂閱行銷通訊的設定檔。 這些訊息只能在特定內容中傳送。

     建立SMS訊息時，您必須選擇與您為訊息選取的類別相符的有效頻道介面。

   * 選取 **[!UICONTROL 簡訊設定]** 以與曲面相關聯。

     有關如何設定環境以傳送SMS訊息的詳細資訊，請參閱 [本節](#create-api).

   * 輸入 **[!UICONTROL 寄件者號碼]** 您&#x200B;要用於通訊。

   * 選取您的 **[!UICONTROL 簡訊執行欄位]** 以選取 **[!UICONTROL 設定檔屬性]** 與設定檔的電話號碼相關聯。

1. 如果您想要在SMS訊息中使用URL縮短功能，請從 **[!UICONTROL 子網域]** 清單。

   >[!NOTE]
   >
   >若要能夠選取子網域，請確定您先前已設定至少一個SMS子網域。 [了解作法](sms-subdomains.md)

1. 設定好所有引數後，按一下 **[!UICONTROL 提交]** 以確認。 您也可以將管路曲面儲存為草繪，並稍後恢復其組態。

   ![](assets/sms_preset_2.png)
<!--
1. **[!UICONTROL Opt-out number]** But what we need to call out is that the opt-out is no longer at a channel level. Previously on receiving the opt-out keyword we used to opt-out the profile at the channel level. Now, we have made it short code specific. So if the customer is using multiple short codes within AJO to send out SMSs, they can continue to send messages to users from other shortcodes if the end user unsubscribes from 1.-->

1. 建立管道曲面後，它會顯示於清單中，其中包含 **[!UICONTROL 處理中]** 狀態。

   >[!NOTE]
   >
   >如果檢查不成功，請在中進一步瞭解可能的失敗原因 [本節](#monitor-channel-surfaces).

1. 檢查成功後，管道表面會取得 **[!UICONTROL 作用中]** 狀態。 已準備好用於傳遞訊息。

   ![](assets/preset-active.png)

您現在可以使用Journey Optimizer傳送SMS訊息。

**相關主題**

* [建立簡訊訊息](create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [在行銷活動中新增訊息](../campaigns/create-campaign.md)

