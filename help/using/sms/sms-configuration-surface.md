---
solution: Journey Optimizer
product: journey optimizer
title: 設定簡訊表面
description: 瞭解如何設定您的SMS/MMS介面，以使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: 82c58753b0beb1c6c60b4e1a8188725b3cb83390
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---

# 建立簡訊/多媒體簡訊表面 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定義訊息類別"
>abstract="使用此介面選取文字訊息型別：促銷訊息的行銷需要使用者同意，或非商業訊息的交易式（例如重設密碼）。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="行銷文字訊息中的選擇退出"

設定您的SMS/MMS頻道後，您必須建立頻道介面，才能從傳送SMS和MMS訊息 **[!DNL Journey Optimizer]**.

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

   建立SMS/MMS時，您必須選擇與您為訊息選取的類別相符的有效頻道介面。

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
   >若要能夠選取子網域，請確定您先前已設定至少一個SMS/MMS子網域。 [了解作法](sms-subdomains.md)

<!--
1. Enter the **[!UICONTROL Opt-out number]** you want to use for this surface. When profiles opt out from this number, you are still able to send them messages from other numbers you may be using to send out text messages with [!DNL Journey Optimizer].

    >[!NOTE]
    >
    >In [!DNL Journey Optimizer], opt-out for text messages is no longer managed at the channel level. It is now specific to a number.
-->
1. 設定好所有引數後，按一下 **[!UICONTROL 提交]** 以確認。 您也可以將管路曲面儲存為草繪，並稍後恢復其組態。

   ![](assets/sms-submit-surface.png)

1. 建立管道曲面後，它會顯示於清單中，其中包含 **[!UICONTROL 處理中]** 狀態。

   >[!NOTE]
   >
   >如果檢查不成功，請在中進一步瞭解可能的失敗原因 [本節](#monitor-channel-surfaces).

1. 檢查成功後，管道表面會取得 **[!UICONTROL 作用中]** 狀態。 已準備好用於傳遞訊息。

   ![](assets/preset-active.png)

您現在可以使用Journey Optimizer傳送簡訊。
