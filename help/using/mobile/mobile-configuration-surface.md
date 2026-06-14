---
solution: Journey Optimizer
product: journey optimizer
title: 設定簡訊設定
description: 瞭解如何設定您的SMS/RCS/MMS設定，以使用Journey Optimizer傳送行動訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
TQID: https://experienceleague.adobe.com/J5h64ccVVJUTCIk7FMMolKfEZy6rjEn-jwj1dEntnRM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 4c82775044b5a0a3a48920f59b0afb8a3c6a6d80
workflow-type: tm+mt
source-wordcount: 558
ht-degree: 12%

---

# 建立行動訊息設定 {#message-preset-sms}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何在Adobe Journey Optimizer中建立行動訊息通道設定，方法是設定訊息型別、行動設定、寄件者號碼、子網域和執行欄位，以傳送SMS、RCS和MMS訊息。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定義訊息類別"
>abstract="選取使用此設定的行動訊息類型：用於促銷訊息的行銷型訊息 (需要使用者同意)，或非商務訊息的交易型訊息 (例如密碼重設)。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="選擇退出行銷行動訊息"

設定行動訊息通道後，您必須建立通道設定，才能從&#x200B;**[!DNL Journey Optimizer]**&#x200B;傳送SMS、RCS和MMS訊息。

若要建立通道設定，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL 一般設定]** > **[!UICONTROL 管道設定]**。 按一下&#x200B;**[!UICONTROL 建立通道組態]**&#x200B;按鈕。

   ![](assets/preset-create.png)

1. 輸入設定的名稱和說明（選用），然後選取行動裝置頻道。

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`、點 `.` 和連字號 `-` 字元。

1. 選取此設定的&#x200B;**[!UICONTROL 簡訊型別]**：

   * **[!UICONTROL 行銷]**：針對需要使用者同意的促銷訊息。
   * **[!UICONTROL 異動]**：針對非商業訊息，例如訂單確認、密碼重設或傳遞更新。

   >[!CAUTION]
   >
   >**異動**&#x200B;訊息可傳送給已取消訂閱行銷通訊的設定檔，但僅限於特定內容。

   ![](assets/sms-surface-settings.png){width=80%}

1. 選取&#x200B;**[!UICONTROL 行動組態]**&#x200B;以與組態關聯。

   有關如何設定環境以傳送行動訊息的詳細資訊，請參閱[本節](#create-api)。

1. 輸入&#x200B;您要用於通訊的&#x200B;**[!UICONTROL 寄件者號碼]**。

1. 若要在行動裝置訊息中使用URL縮短功能，請從&#x200B;**[!UICONTROL 子網域]**&#x200B;清單中選取專案。

   >[!NOTE]
   >
   >若要能夠選取子網域，請確定您先前已設定至少一個SMS/RCS/MMS子網域。 [了解作法](mobile-subdomains.md)

1. 在&#x200B;**[!UICONTROL 執行維度]**&#x200B;區段中，使用&#x200B;**[!UICONTROL 簡訊執行欄位]**&#x200B;在設定檔屬性中選取您想要優先使用的電話號碼（如果資料庫中有數個號碼可用）。 [了解更多](../configuration/primary-email-addresses.md#override-execution-address-channel-config)

   >[!NOTE]
   >
   >依預設，[!DNL Journey Optimizer]在沙箱層級使用[一般設定](../configuration/primary-email-addresses.md)中指定的電話號碼。 更新此欄位會覆寫使用此設定的歷程和行銷活動的預設值。

1. 選取&#x200B;**[!UICONTROL 使用傳入的自訂資料集]**，將此認證的傳入SMS路由至您從下拉式清單中選擇的預先建立資料集。 [進一步瞭解如何使用傳入關鍵字的自訂資料集](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >資料集結構描述必須是&#x200B;**[!UICONTROL XDM ExperienceEvent]**，而且至少包含下列欄位群組：
   >* Adobe CJM ExperienceEvent — 訊息互動細節
   >* Adobe CJM ExperienceEvent — 訊息執行詳細資料
   >* Adobe CJM ExperienceEvent — 訊息設定檔詳細資料
   >
   >必須為設定檔啟用結構描述和資料集。

1. 設定完所有引數後，按一下&#x200B;**[!UICONTROL 提交]**&#x200B;確認。 您也可以將頻道設定儲存為草稿，並稍後繼續其設定。

   ![](assets/sms-submit-surface.png)

1. 建立管道設定後，它就會顯示在狀態為&#x200B;**[!UICONTROL 處理中]**&#x200B;的清單中。

   >[!NOTE]
   >
   >如果檢查不成功，請在[本節](../configuration/channel-surfaces.md)中進一步瞭解可能的失敗原因。

1. 檢查成功後，通道設定會取得&#x200B;**[!UICONTROL 作用中]**&#x200B;狀態。 已準備好用於傳遞訊息。

   ![](assets/preset-active.png)

您現在可以使用Journey Optimizer傳送行動裝置訊息。
