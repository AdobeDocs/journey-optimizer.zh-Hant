---
title: 建立 SMS 訊息
description: 瞭解如何在Journey Optimizer建立SMS消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 067453ee3c19c7f269b4b1791ead8b5421adf95b
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 12%

---

# 建立 SMS 訊息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS建立"
>abstract="添加文本消息，然後使用表達式編輯器開始個性化它。"

>[!NOTE]
>
>SMS通道當前僅可用於一組組織（有限可用性）。 有關詳細資訊，請與Adobe代表聯繫。

一旦 [已建立消息](get-started-content.md)，使用 **[!UICONTROL SMS]** 的子菜單。

![](assets/sms_1.png)

要開始個性化您的SMS消息，請執行以下步驟：

1. 按一下 **[!UICONTROL Add text message]** 欄位以開啟表達式編輯器。

   ![](assets/sms_3.png)

1. 使用表達式編輯器定義內容和個性化資料。 在中的表達式編輯器中瞭解有關個性化的詳細資訊 [此部分](../personalization/personalize.md)

   >[!NOTE]
   >
   > SMS消息的長度限制為160個字元。

   ![](assets/sms_2.png)

1. 按一下 **[!UICONTROL Save]** 當您的個性化郵件準備就緒時。

1. 按一下 **[!UICONTROL Preview]** 顯示移動設備上的SMS消息顯示方式。 如需詳細資訊，請參閱[本章節](../design/preview.md)。

1. 一旦您的消息準備就緒，您就可以發佈它，使其可以與 **[!UICONTROL Publish]** 按鈕 此操作將發佈消息的新版本，該新版本將用於您的旅途中的下一次執行。

您的SMS消息現在可以在旅途中使用。 [瞭解如何建立旅程](../building-journeys/journey-gs.md)。

## 選擇加入和選擇退出{#sms-opt-in-out}

SMS收件人可以使用選擇加入和選擇退出關鍵字進行回復。 根據行業標準和法規，Adobe Journey Optimizer自動處理傳入消息中的以下關鍵字：開始、停止和停止。 這些關鍵字觸發來自SMS提供程式的自動標準答復。

**相關主題**

* [設定簡訊頻道](../configuration/sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)
* [建立新訊息。](get-started-content.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
