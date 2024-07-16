---
solution: Journey Optimizer
product: journey optimizer
title: 設定簡訊表面
description: 瞭解如何設定您的SMS/MMS介面，以使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: 080928d14a9d6ec116286386748b77a6a25e76f8
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 10%

---

# 建立 SMS/MMS 表面 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定義訊息類別。"
>abstract="選取使用此表面的文字簡訊類型：需要使用者同意的促銷簡訊的行銷訊息，或非商業簡訊的交易型訊息，例如密碼重設。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=zh-Hant#sms-opt-out-management" text="選擇不接收行銷文字簡訊"

設定您的SMS/MMS頻道之後，您必須建立頻道介面，才能從&#x200B;**[!DNL Journey Optimizer]**&#x200B;傳送SMS和MMS訊息。

若要建立管道曲面，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL 品牌]** > **[!UICONTROL 管道表面]**。 按一下&#x200B;**[!UICONTROL 建立管道表面]**&#x200B;按鈕。

   ![](assets/preset-create.png)

1. 輸入表面的名稱和說明（選擇性），然後選取SMS通道。

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線`_`、點`.`和連字型大小`-`字元。

1. 定義&#x200B;**簡訊設定**。

   ![](assets/sms-surface-settings.png)

   首先，選取將與介面一併傳送的&#x200B;**[!UICONTROL 簡訊型別]**： **[!UICONTROL 異動]**&#x200B;或&#x200B;**[!UICONTROL 行銷]**。

   * 選擇促銷文字訊息的&#x200B;**行銷**：這些訊息需要使用者同意。
   * 針對非商業性訊息，例如訂單確認、密碼重設通知或傳遞資訊，請選擇&#x200B;**異動**。

   建立SMS/MMS時，您必須選擇與您為訊息選取的類別相符的有效頻道介面。

   >[!CAUTION]
   >
   >**異動**&#x200B;訊息可傳送給取消訂閱行銷通訊的設定檔。 這些訊息只能在特定內容中傳送。

1. 選取&#x200B;**[!UICONTROL SMS設定]**&#x200B;以關聯至表面。

   有關如何設定環境以傳送SMS訊息的詳細資訊，請參閱[本節](#create-api)。

1. 輸入&#x200B;您要用於通訊的&#x200B;**[!UICONTROL 寄件者號碼]**。

1. 選取您的&#x200B;**[!UICONTROL 簡訊執行欄位]**&#x200B;以選取與設定檔電話號碼相關聯的&#x200B;**[!UICONTROL 設定檔屬性]**。

1. 如果您想要在SMS訊息中使用URL縮短功能，請從&#x200B;**[!UICONTROL 子網域]**&#x200B;清單中選取專案。

   >[!NOTE]
   >
   >若要能夠選取子網域，請確定您先前已設定至少一個SMS/MMS子網域。 [了解作法](sms-subdomains.md)

1. 設定完所有引數後，按一下&#x200B;**[!UICONTROL 提交]**&#x200B;確認。 您也可以將管路曲面儲存為草繪，並稍後恢復其組態。

   ![](assets/sms-submit-surface.png)

1. 建立管道表面後，它會顯示在&#x200B;**[!UICONTROL 處理中]**&#x200B;狀態的清單中。

   >[!NOTE]
   >
   >如果檢查不成功，請在[本節](#monitor-channel-surfaces)中進一步瞭解可能的失敗原因。

1. 檢查成功後，管道表面會取得&#x200B;**[!UICONTROL 作用中]**&#x200B;狀態。 已準備好用於傳遞訊息。

   ![](assets/preset-active.png)

您現在可以使用Journey Optimizer傳送簡訊。
