---
title: 建立 SMS 訊息
description: 瞭解如何在Journey Optimizer建立SMS消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 9%

---

# 建立 SMS 訊息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS建立"
>abstract="添加文本消息，然後使用表達式編輯器開始個性化它。"

使用 [!DNL Journey Optimizer] 將簡訊發送給客戶的移動設備。 您可以從SMS編輯器建立、個性化和預覽文本格式的消息。

可以建立SMS傳遞：

* 在 **旅程**:在您的行程中添加SMS活動並定義基本設定後，使用 **[!UICONTROL Actions: SMS]** 右窗格，建立SMS消息的內容。

   有關如何配置行程的詳細資訊，請參閱此 [頁](../building-journeys/journey-gs.md)。

* 在 **活動**:建立市場活動後，選擇SMS作為您的活動並定義基本設定。

   有關如何配置市場活動的詳細資訊，請參閱此 [頁](../campaigns/create-campaign.md#configure)。

如果這是您首次建立SMS消息，請確保已配置SMS通道。 [了解更多](../configuration/sms-configuration.md)。

## 定義SMS內容{#sms-content}

要開始個性化您的SMS消息，請執行以下步驟：

1. 按一下 **[!UICONTROL Message]** 欄位以開啟表達式編輯器。

   ![](assets/sms-content.png)

1. 使用表達式編輯器定義內容。 您可以使用任何屬性對內容進行個性化設定，如配置檔案名稱或城市。 在中的表達式編輯器中瞭解有關個性化的詳細資訊 [此部分](../personalization/personalize.md)。

1. 按一下 **[!UICONTROL Save]** 並在預覽中查看您的留言。

   ![](assets/sms-content-preview.png)

## 驗證您的SMS{#sms-preview}

>[!NOTE]
>
> 為了獲得更好的交付能力，您應始終使用提供商支援的格式中的電話號碼。 例如， Twilio和Sinch僅支援E.164格式的電話號碼。

定義消息內容後，可以使用test配置檔案預覽和test它。 如果插入 [個性化內容](../personalization/personalize.md)，您可以利用test配置檔案資料檢查此內容在消息中的顯示方式。

要直觀顯示移動設備上的SMS消息顯示方式，請按一下 **[!UICONTROL Simulate content]** 頁籤。 瞭解有關中內容模擬的詳細資訊 [此部分](../design/preview.md)。

您還必須檢查編輯器上半部分的警報。  其中一些是簡單的警告，但其他警告可能會阻止您使用該消息。 請參閱[此章節](alerts.md)深入瞭解。

![](assets/sms-alert-button.png)


## 選擇加入和選擇退出{#sms-opt-in-out}

對於所有營銷消息，SMS必須包含一種方法，讓收件人能夠輕鬆取消訂閱。 一旦取消訂閱，這些配置檔案將自動從未來營銷消息的受眾中刪除。 對於事務性消息，不必添加未訂閱連結。

SMS收件人可以使用選擇加入和選擇退出關鍵字進行回復。 根據行業標準和法規，Adobe Journey Optimizer自動處理傳入消息中的以下關鍵字：開始、停止和停止。 這些關鍵字觸發來自簡訊提供者的自動標準回覆。

要瞭解SMS的本機入站關鍵字支援（啟動、停止和取消停止）的工作原理的詳細資訊，請參閱以下視頻。

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

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
