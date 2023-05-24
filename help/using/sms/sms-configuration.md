---
solution: Journey Optimizer
product: journey optimizer
title: 配置SMS通道
description: 瞭解如何配置環境以向Journey Optimizer發送簡訊
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 33dccf32b60a6afb58931823016821fc1effcbd8
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 19%

---

# 設定簡訊頻道 {#sms-configuration}

[!DNL Journey Optimizer] 允許您建立行程並向目標受眾發送消息。

在發送SMS之前，請配置實例。 你需要 [整合提供程式設定](#create-api) 和Journey Optimizer [建立SMS曲面](#message-preset-sms) （即SMS預設）。 這些步驟必須由 [Adobe Journey Optimizer 系統管理員](../start/path/administrator.md)執行。

## 先決條件{#sms-prerequisites}

Adobe Journey Optimizer目前與Sinch和Twilio等第三方提供商進行整合，後者提供獨立於Adobe Journey Optimizer的簡訊服務。

在SMS配置之前，必須使用這些SMS提供程式之一建立帳戶以接收API令牌和服務ID，這使您能夠在Adobe Journey Optimizer和適用的SMS提供程式之間建立連接。

您使用SMS服務將受適用SMS提供商的附加條款和條件的約束。 由於Sinch和Twilio是通過整合提供給Adobe Journey Optimizer用戶的第三方產品，因此對於任何與SMS服務相關的問題或查詢，Sinch或Twilio的用戶需要聯繫適用的SMS提供商以獲得幫助。 Adobe不控制第三方產品，也不負責。

>[!CAUTION]
>
>要訪問和編輯SMS子域，您必須具有 **[!UICONTROL 管理SMS子域]** 在生產沙盒上的權限。

## 建立新API憑據 {#create-api}

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

要使用Journey Optimizer配置您的SMS供應商，請執行以下步驟：

1. 在左欄中，瀏覽到 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 的 **[!UICONTROL API憑據]** 的子菜單。 按一下 **[!UICONTROL 建立新API憑據]** 按鈕

   ![](assets/sms_6.png)

1. 選擇 **[!UICONTROL SMS供應商]**:

   * **[!DNL Sinch]**

      查找 **[!UICONTROL 服務ID]** 和 **[!UICONTROL API令牌]**，從您的Sinch帳戶訪問SMS > APIs菜單。

   * **[!DNL Twilio]**

      查找 **[!UICONTROL 服務ID]** 和 **[!UICONTROL API令牌]**，訪問「控制台儀表板」頁的「帳戶資訊」窗格。


1. 輸入 **[!UICONTROL 名稱]** API憑據。

1. 輸入 **[!UICONTROL 服務ID]** 和 **[!UICONTROL API令牌]**。

   ![](assets/sms_7.png)

1. 按一下 **[!UICONTROL 提交]** 完成API憑據的配置。

建立和配置API憑據後，您現在需要為SMS消息建立通道表面（即消息預設）。

## 建立SMS曲面 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定義簡訊類別"
>abstract="選取使用此表面的簡訊訊息類型：需要使用者同意的促銷簡訊的行銷訊息，或非商業簡訊的異動訊息，例如密碼重設。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="選擇不接收行銷簡訊訊息"

配置SMS通道後，必須建立通道表才能從中發送SMS消息 **[!DNL Journey Optimizer]**。

要建立通道曲面，請執行以下步驟：

1. 在左欄中，瀏覽到 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 選擇 **[!UICONTROL 品牌]** > **[!UICONTROL 通道曲面]**。 按一下 **[!UICONTROL 建立通道曲面]** 按鈕

   ![](assets/preset-create.png)

1. 輸入曲面的名稱和說明（可選），然後選擇SMS通道。

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含字母數字字元。 您還可以使用下划線 `_`，點`.` 連字元 `-` 字元。

1. 定義 **SMS設定**。

   ![](assets/preset-sms.png)

   * 選擇 **[!UICONTROL SMS類型]** 將與表面一起發送： **[!UICONTROL 事務性]** 或 **[!UICONTROL 營銷]**。

      * 選擇 **營銷** 促銷簡訊：這些消息需要用戶同意。
      * 選擇 **事務性** 非商業消息（例如，訂單確認、密碼重置通知或傳遞資訊）。

      >[!CAUTION]
      >
      >**事務性** SMS消息可以發送到從營銷通信中取消訂閱的配置檔案。 這些消息只能在特定上下文中發送。

      建立SMS消息時，必須選擇與您為消息選擇的類別匹配的有效通道表面。

   * 選擇 **[!UICONTROL SMS配置]** 與曲面相關。

      有關如何配置環境以發送SMS消息的詳細資訊，請參閱 [此部分](#create-api)。

   * 輸入 **[!UICONTROL 發件人編號]** 你&#x200B;想用來溝通。

   * 選擇 **[!UICONTROL SMS執行欄位]** 的 **[!UICONTROL 配置檔案屬性]** 與配置檔案的電話號碼關聯。


1. 如果要在SMS消息中使用URL縮短功能，請從 **[!UICONTROL 子域]** 清單框。

   >[!NOTE]
   >
   >要能夠選擇子域，請確保您以前至少配置了一個SMS子域。 [了解作法](sms-subdomains.md)

1. 配置完所有參數後，按一下 **[!UICONTROL 提交]** 確認。 也可將通道曲面另存為拔模，並稍後恢復其配置。

   ![](assets/sms_preset_2.png)

1. 建立通道曲面後，它將顯示在清單中 **[!UICONTROL 處理]** 狀態。

   >[!NOTE]
   >
   >如果檢查不成功，請詳細瞭解中可能的失敗原因 [此部分](#monitor-channel-surfaces)。

1. 檢查成功後，通道曲面將 **[!UICONTROL 活動]** 狀態。 它已準備好用於傳遞消息。

   ![](assets/preset-active.png)

您現在已準備好向Journey Optimizer發送SMS消息。

**相關主題**

* [建立簡訊訊息](create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [在市場活動中添加消息](../campaigns/create-campaign.md)

