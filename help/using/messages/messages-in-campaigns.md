---
title: 在市場活動中添加消息
description: 瞭解如何在市場活動中添加消息
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 87f9a4661b64cf24a8cd62bb9c70d5f1c9fcaddf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 80%

---


# 在市場活動中添加消息{#messages-in- campaigns}

在市場活動中，選擇要設計並個性化發送給受眾的消息的渠道。 當您添加電子郵件、簡訊或「推送」到您的市場活動時，您可以立即發送它或安排消息。

>[!NOTE]
>您還可以建立行程以發送觸發消息。 請參閱[本節](messages-in-journeys.md).

瞭解如何在市場活動中添加和配置郵件 [此部分](../campaigns/create-campaign.md)

若要瞭解建立訊息內容的詳細步驟，請至以下頁面：

* [建立電子郵件](create-email.md)
* [建立推播通知](create-push.md)
* [建立 SMS 訊息](create-sms.md)

## 啟用傳送時間最佳化{#sto-in-journeys}

針對電子郵件與推播通知，您可以啟用&#x200B;**[!UICONTROL Send-time optimization]**。

利用&#x200B;**[!UICONTROL Send-time optimization]**&#x200B;為每位使用者安排個人化的傳送時間，以提高您訊息的開啟及點閱率。 [了解更多](../messages/send-time-optimization.md)。

## 進階參數{#adv-settings}

進階參數預設為唯讀並隱藏。

若要存取進階參數，請按一下訊息窗格頂端的&#x200B;**[!UICONTROL Show read-only fields]**&#x200B;圖示。

![](assets/show-read-only.png)

進階參數會顯示在訊息窗格的底部。 這些參數在與訊息相關的[頻道介面](../configuration/channel-surfaces.md)，由[系統管理員](../start/path/administrator.md)定義。

針對推播通知，您可以顯示以下參數：代號、AppID、AppPlatform。

![](assets/push-adv-parameters.png)

針對電子郵件，您可以顯示主要電子郵件地址。

針對特定用途，您可以在特定內容覆寫這些值。 若要強制執行值，請按一下欄位右側的&#x200B;**啟用參數覆寫**&#x200B;圖示。此選項可能對如下項目非常有用：

* 測試電子郵件，您可以新增電子郵件地址。 在您發佈了此歷程後，會向您寄送電子郵件。
* 請參閱訂閱者清單的電子郵件地址。 在[此使用案例](../building-journeys/message-to-subscribers-uc.md)中了解更多。

按一下同一表徵圖隱藏高級設定。

## 瀏覽訊息{#browse-message}

當在歷程中使用多個訊息時，您可以從 **編輯內容** 畫面切換到另一個畫面。

![](assets/inline-messages-multi-content.png)

你可以在單一檢視中 [檢查警報](alerts.md) 和 [模擬](../design/preview.md) 每個內容。

## 複製訊息 {#duplicate-message}

你可以從歷程畫布複製現有訊息。

請依照下列步驟執行：

1. 選取要複製的訊息。

1. 使用窗格的 **[!UICONTROL Copy]** 按鈕 **[!UICONTROL Action]** 。

   ![](assets/message-duplicate.png)

1. 輸入 **crtl+V** 貼上訊息。

   該訊息將新增到歷程畫布。 所有設定與組態都將複製到新訊息中。

   ![](assets/message-duplicated.png)

1. 將訊息重新命名以便能夠區分初始訊息與副本，例如，在編輯訊息時，如下所示：

   ![](assets/multi-message.png)


>[!NOTE]
>
>對於電子郵件，您還可以將現有訊息轉換為範本。 [了解更多](../design/email-templates.md)。

## 刪除訊息{#delete-message}

若要刪除訊息，請使用頻道活動窗格頂部的垃圾筒圖示。

![](assets/delete-message.png)

使用 **[!UICONTROL Confirm]** 按鈕來驗證。
