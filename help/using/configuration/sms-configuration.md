---
title: SMS配置
description: 瞭解如何配置環境以向Journey Optimizer發送SMS消息
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 47b1c2832f82a5c168cd03f1d1b43a9223c945b3
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 3%

---

# 設定簡訊頻道 {#sms-configuration}

[!DNL Journey Optimizer] 允許您建立行程並向目標受眾發送消息。

在發送SMS之前，請配置實例。 你需要 [整合提供程式設定](#create-api) 和Journey Optimizer [建立SMS預設](#message-preset-sms)。 這些步驟必須由 [Adobe Journey Optimizer系統管理員](../start/path/administrator.md)。

>[!AVAILABILITY]
>
>SMS通道當前僅可用於一組組織（有限可用性）。 有關詳細資訊，請與Adobe代表聯繫。

## 建立新API憑據 {#create-api}

要使用Journey Optimizer配置您的SMS供應商，請執行以下步驟：

1. 訪問 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** 菜單，然後按一下 **[!UICONTROL Create API credential]**。

   ![](assets/sms_4.png)

1. 選擇 **[!UICONTROL SMS vendor]**:

   * [!DNL Sinch]。查找 **[!UICONTROL Service ID]** 和 **[!UICONTROL API Token]**，從您的Sinch帳戶訪問SMS > APIs菜單。
   * [!DNL Twilio]。查找 **[!UICONTROL Service ID]** 和 **[!UICONTROL API Token]**，訪問「控制台儀表板」頁的「帳戶資訊」窗格。

1. 輸入 **[!UICONTROL Name]** API憑據。

1. 輸入 **[!UICONTROL Service ID]** 和 **[!UICONTROL API Token]**。

   ![](assets/sms_5.png)

1. 按一下 **[!UICONTROL Submit]** 完成API憑據的配置。

建立和配置API憑據後，您現在需要為SMS消息建立消息預設。

## 為SMS消息建立消息預設 {#message-preset-sms}

配置SMS通道後，您需要建立消息預設，以便能夠從 **[!DNL Journey Optimizer]**。

要建立消息預設，請執行以下步驟：

1. 訪問 **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** 菜單，然後按一下 **[!UICONTROL Create Message preset]**。

   ![](assets/preset-create.png)

1. 輸入預設的名稱和說明（可選），然後選擇SMS通道。

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含字母數字字元。 您還可以使用下划線 `_`，點`.` 連字元 `-` 字元。

1. 配置 **簡訊** 的子菜單。

   ![](assets/preset-sms.png)

   * 選擇 **[!UICONTROL SMS Type]** 將隨預設發送： **[!UICONTROL Transactional]** 或 **[!UICONTROL Marketing]**。

   * 選擇 **[!UICONTROL SMS configuration]** 與預設關聯。

      有關如何配置環境以發送SMS消息的詳細資訊，請參閱 [此部分](#create-api)。

   * 輸入 **[!UICONTROL Sender number]** 你&#x200B;想用來溝通。

   * 選擇 **[!UICONTROL SMS Execution Field]** 的 **[!UICONTROL Profile attribute]** 與配置檔案的電話號碼關聯。

1. 配置完所有參數後，按一下 **[!UICONTROL Submit]** 確認。 您也可以將消息預設保存為草稿，並稍後恢復其配置。

   ![](assets/sms_preset_2.png)

1. 建立消息預設後，它將顯示在清單中 **[!UICONTROL Processing]** 狀態。

   >[!NOTE]
   >
   >如果檢查不成功，請詳細瞭解中可能的失敗原因 [此部分](#monitor-message-presets)。

1. 檢查成功後，消息預設將獲取 **[!UICONTROL Active]** 狀態。 它已準備好用於傳遞消息。

   ![](assets/preset-active.png)

您現在已準備好向Journey Optimizer發送SMS消息。

**相關主題**

* [建立 SMS 訊息](../messages/create-sms.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
