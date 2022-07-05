---
title: 建立 SMS 訊息
description: 瞭解如何在Journey Optimizer建立SMS消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 630b8ef5a140709161b24256083b2104be5b6121
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 15%

---

# 建立 SMS 訊息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="SMS建立"
>abstract="添加文本消息，然後使用表達式編輯器開始個性化它。"

一旦 [已建立消息](get-started-content.md)，使用 **[!UICONTROL SMS]** 頁籤，定義SMS消息的設定和內容。


>[!AVAILABILITY]
>
>簡訊管道目前僅可用於一組組織（可用性限制）。 如需詳細資訊，請聯絡您的 Adobe 代表。

![](assets/sms_1.png)

如果這是您首次建立SMS消息，請確保已配置SMS通道。 [了解更多](../configuration/sms-configuration.md)。

## 定義SMS內容{#sms-content}

要開始個性化您的SMS消息，請執行以下步驟：

1. 按一下 **[!UICONTROL Add text message]** 欄位以開啟表達式編輯器。

   ![](assets/sms_3.png)

1. 使用表達式編輯器定義內容。 您可以使用任何屬性對內容進行個性化設定，如配置檔案名稱或城市。 在中的表達式編輯器中瞭解有關個性化的詳細資訊 [此部分](../personalization/personalize.md)

   >[!NOTE]
   >
   > SMS消息最多可包含160個字元，包括空格和換行符。

   ![](assets/sms_2.png)

1. 按一下 **[!UICONTROL Save]** 當您的留言準備好時。

## 驗證您的SMS{#sms-preview}

定義消息內容後，可以使用test配置檔案預覽和test它。 如果插入 [個性化內容](../personalization/personalize.md)，您可以利用test配置檔案資料檢查此內容在消息中的顯示方式。

要直觀顯示移動設備上的SMS消息顯示方式，請瀏覽至 **[!UICONTROL Preview]** 頁籤。

如需詳細資訊，請參閱[本章節](../design/preview.md)。

## 發佈您的SMS {#sms-publish}

一旦您的消息準備就緒，您就可以發佈它，使其可以與 **[!UICONTROL Publish]** 按鈕 此操作將發佈消息的新版本，該新版本將用於您的行程中的下一個執行。

您的SMS消息現在可以在旅途中使用。 [瞭解如何建立旅程](../building-journeys/journey-gs.md)。

## 選擇加入和選擇退出{#sms-opt-in-out}

對於所有營銷消息，SMS必須包含一種方法，讓收件人能夠輕鬆取消訂閱。 一旦取消訂閱，這些配置檔案將自動從未來營銷消息的受眾中刪除。 對於事務性消息，不必添加未訂閱連結。

SMS收件人可以使用選擇加入和選擇退出關鍵字進行回復。 根據行業標準和法規，Adobe Journey Optimizer自動處理傳入消息中的以下關鍵字：開始、停止和停止。 這些關鍵字觸發來自簡訊提供者的自動標準回覆。

要瞭解SMS的本機入站關鍵字支援（啟動、停止和取消停止）的工作原理的詳細資訊，請參閱以下視頻。

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

## How-to視頻

瞭解如何配置、編寫和將SMS消息包括到您的客戶旅程中。

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)

**相關主題**

* [設定簡訊頻道](../configuration/sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)
* [建立新訊息。](get-started-content.md)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
