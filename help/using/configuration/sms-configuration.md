---
title: SMS設定
description: 了解如何設定您的環境，使用Journey Optimizer傳送SMS訊息
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: e4125d3e1f0c382c1f2ca13ad080aba830c5df46
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 設定簡訊頻道 {#sms-configuration}

>[!CAUTION]
>
> 目前，僅特定使用者可提早存取SMS通道。 如果您想要運用此功能，請連絡您的Adobe客戶主管。

[!DNL Journey Optimizer] 可讓您建立歷程並傳送訊息給目標對象。

## 建立新的API憑證 {#create-api}

若要使用Journey Optimizer設定您的SMS廠商，請遵循下列步驟：

1. 存取 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** ，然後按一下 **[!UICONTROL Create API credential]**.

   ![](../assets/sms_4.png)

1. 選取Sinch作為 **[!UICONTROL SMS vendor]**.

1. 輸入 **[!UICONTROL Name]** 來取得API憑證。

1. 輸入 **[!UICONTROL Service ID]** 和 **[!UICONTROL API Token]**.

   >[!NOTE]
   >
   > Sinch需要特殊API憑證。 若要尋找 **[!UICONTROL Service ID]** 和 **[!UICONTROL API Token]**，從您的Sinch帳戶存取SMS > API功能表，

   ![](../assets/sms_5.png)

1. 按一下 **[!UICONTROL Submit]** 完成API憑證的設定時。

建立和設定API憑證後，您現在需要建立SMS訊息的訊息預設集。

## 建立SMS訊息的訊息預設集 {#message-preset-sms}

設定SMS通道後，您需要建立訊息預設集，才能傳送來自 **[!DNL Journey Optimizer]**.

若要建立訊息預設集，請依照下列步驟操作：

1. 存取 **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** ，然後按一下 **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. 輸入預設集的名稱和說明（選用），然後選取SMS通道。

   ![](../assets/sms_preset.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 連字型大小 `-` 字元。

1. 設定 **簡訊** 設定。

   ![](../assets/preset-sms.png)

   * 選取 **[!UICONTROL SMS Type]** 會與預設集一併傳送： **[!UICONTROL Transactional]** 或 **[!UICONTROL Marketing]**.

   * 選取 **[!UICONTROL SMS configuration]** 來關聯預設集。

      如需如何設定環境以傳送SMS訊息的詳細資訊，請參閱 [本節](sms-configuration.md).

   * 輸入 **[!UICONTROL Sender number]** &#x200B;你想用於溝通。

1. 完成所有參數設定後，按一下 **[!UICONTROL Submit]** 確認。 您也可以將訊息預設集儲存為草稿，稍後繼續其設定。

   ![](../assets/sms_preset_2.png)

1. 建立訊息預設集後，訊息預設集會顯示在清單中，並搭配 **[!UICONTROL Processing]** 狀態。

   >[!NOTE]
   >
   >如果檢查未成功，請進一步了解中可能的失敗原因。 [本節](#monitor-message-presets).

1. 檢查成功後，訊息預設集會取得 **[!UICONTROL Active]** 狀態。 它已準備好用於傳送訊息。

   ![](../assets/preset-active.png)

若要了解如何設定推播通知和電子郵件的訊息預設集，請參閱 [本節](message-presets.md).

您現在已準備好使用Journey Optimizer傳送SMS訊息。

**相關主題**

* [建立SMS訊息](../create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
