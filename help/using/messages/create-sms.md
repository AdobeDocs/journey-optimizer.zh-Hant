---
title: 建立 SMS 訊息
description: 了解如何在Journey Optimizer中建立SMS訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 32c69ef268c78ba834612d16b2ac1c721fb5df56
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 7%

---

# 建立 SMS 訊息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="簡訊建立"
>abstract="新增文字訊息，並開始使用運算式編輯器進行個人化。"

使用 [!DNL Journey Optimizer] 在客戶的行動裝置上傳送簡訊給客戶。 您可以從SMS編輯器建立、個人化及預覽文字格式的訊息。

>[!NOTE]
>
>根據業界標準和法規，所有SMS行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 若要這麼做，SMS收件者可以使用選擇加入和選擇退出關鍵字回覆。 [了解如何管理選擇退出](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

可建立SMS傳遞：

* 在 **歷程**:在歷程中新增SMS活動並定義基本設定後，請使用 **[!UICONTROL 動作：簡訊]** 右窗格，以建立SMS訊息的內容。

   如需如何設定歷程的詳細資訊，請參閱 [頁面](../building-journeys/journey-gs.md).

* 在 **行銷活動**:建立促銷活動後，請選取SMS作為動作並定義基本設定。

   如需如何設定促銷活動的詳細資訊，請參閱 [頁面](../campaigns/create-campaign.md#configure).

如果這是您第一次建立SMS訊息，請確定已設定SMS通道。 [了解更多](../configuration/sms-configuration.md)。

## 定義您的SMS內容{#sms-content}

若要開始個人化SMS訊息，請遵循下列步驟：

1. 按一下 **[!UICONTROL 訊息]** 欄位來開啟運算式編輯器。

   ![](assets/sms-content.png)

1. 使用運算式編輯器來定義內容並新增動態內容。 您可以使用任何屬性，例如設定檔名稱或城市。 深入了解 [個人化](../personalization/personalize.md) 和 [動態內容](../personalization/get-started-dynamic-content.md) 在運算式編輯器中。

1. 按一下 **[!UICONTROL 儲存]** 並在預覽中檢查您的訊息。

   ![](assets/sms-content-preview.png)

## 驗證您的簡訊{#sms-preview}

>[!NOTE]
>
> 為了獲得更好的傳遞能力，您應始終使用提供商支援的格式的電話號碼。 例如， Twilio和Sinch僅支援E.164格式的電話號碼。

定義訊息內容後，您就可以使用測試設定檔來預覽和測試。 如果您已插入 [個人化內容](../personalization/personalize.md)，您可以運用測試設定檔資料，檢查訊息中此內容的顯示方式。

若要視覺化您的SMS訊息在行動裝置上的顯示方式，請按一下 **[!UICONTROL 模擬內容]** 標籤。 深入了解內容模擬，位於 [本節](../design/preview.md).

您也必須檢查編輯器上方區段的警報。  其中有些是簡單警告，但有些警告可能會阻止您使用訊息。 請參閱[此章節](alerts.md)深入瞭解。

![](assets/sms-alert-button.png)

<!--
## How-to video

Learn how to configure, author, and include SMS messaging into your customer journeys.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)
-->
**相關主題**

* [設定簡訊頻道](../configuration/sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)
* [建立新訊息。](get-started-content.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
