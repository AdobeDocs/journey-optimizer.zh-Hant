---
title: 開始使用訊息
description: 了解如何在 Journey Optimizer 中建立和傳遞個人化訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 7%

---

# 開始使用訊息 {#get-started-messages}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="渠道操作"
>abstract="使用通道操作發送推送、SMS或電子郵件。"

使用 [!DNL Journey Optimizer] 建立和傳遞個性化推送通知、SMS和電子郵件。 所有郵件都可以在行內編輯，作為Journey Canvas上操作的一部分。  使用「另存為模板」功能可輕鬆重用內容。 您可以：

* 使用 [!DNL Journey Optimizer] **電子郵件設計功能** 建立或導入響應電子郵件。

* 利用 **Adobe Experience Manager Assets Essentials** 豐富您的電子郵件，構建和管理您自己的資產資料庫。

* 查找 **Adobe Stock照片** 構建內容並改進電子郵件設計。

* 通過建立個性化的客戶體驗 **推送通知、簡訊和電子郵件** 基於其配置檔案屬性。

* **發送交貨** 並跟蹤客戶行為。

>[!NOTE]
>
>用戶可以根據其產品配置檔案訪問、建立、編輯和/或發佈行程。 [在此章節](../administration/permissions.md)瞭解有關使用者權限的詳細資訊。


## 在您的行程中添加消息{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="消息類別"
>abstract="為商業消息選擇「市場營銷」，或為非商業消息選擇「事務處理」，如訂單確認、密碼重置通知或交貨資訊"

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="通道表面"
>abstract="渠道曲面是該渠道的一個實例，它具有通過市場活動或行程成功傳遞行動的所有設定。 它由系統管理員定義。"

要在您的行程中添加消息，只需在行程卡中添加推送、簡訊或電子郵件活動即可。

1. 開始您的旅程 [事件](../building-journeys/general-events.md) 或 [讀取段](../building-journeys/read-segment.md) 的子菜單。

1. 從 **操作** ，拖放 **電子郵件**&#x200B;的 **簡訊** 或 **推** 的下界。

   ![](assets/add-a-message.png)

1. 輸入標籤和說明。

1. 選擇消息 **[!UICONTROL Category]**:選擇 **營銷** 用於商業消息，或 **事務性** 非商業消息（如訂單確認、密碼重置通知或傳遞資訊）。

   >[!CAUTION]
   >
   >如果您定義 [頻率規則](../configuration/frequency-rules.md) 對於特定的頻道和類別，在選擇該頻道和類別後，這些頻道和類別將自動應用到消息。 當前僅 **[!UICONTROL Marketing]** 類別可用於頻率規則。

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >市場營銷類型消息必須包括 [選擇退出連結](../messages/consent.md#opt-out-management)。 對於事務性消息，不需要這樣做，因為這些消息可以發送到從市場營銷通信中取消訂閱的配置檔案。

1. 選擇頻道 **[!UICONTROL Surface]** （即消息預設），用於發送您的消息。

   曲面是由 [系統管理員](../start/path/administrator.md)。 它包含所有用於發送消息的技術參數，如報頭參數、子域、移動應用等。 [了解更多](../configuration/channel-surfaces.md)。

   >[!CAUTION]
   >
   >必須為所選消息類別和通道選擇有效的通道曲面。

   您可以隨時使用 **[!UICONTROL Properties]** 按鈕。

1. 建立消息內容。

   瞭解在以下頁面中建立消息內容的詳細步驟：

   * [建立電子郵件](create-email.md)
   * [建立推播通知](create-push.md)
   * [建立 SMS 訊息](create-sms.md)

## 啟用發送時優化{#sto-in-journeys}

對於電子郵件和推送通知，您可以啟用 **[!UICONTROL Send-time optimization]**。

使用 **[!UICONTROL Send-time optimization]** 為每個用戶安排個性化發送時間以增加開啟時間並按一下消息的速率。 [了解更多](../messages/send-time-optimization.md)。


## 高級參數{#adv-settings}

預設情況下，高級參數為只讀和隱藏。

要訪問高級參數，請按一下 **[!UICONTROL Show read-only fields]** 表徵圖。

![](assets/show-read-only.png)

高級參數顯示在消息窗格的底部。 這些參數由 [系統管理員](../start/path/administrator.md) 的 [通道表面](../configuration/channel-surfaces.md) （即消息預設）與消息關聯。

對於推式通知，您可以顯示以下參數：令牌、AppID、AppPlatform。

![](assets/push-adv-parameters.png)

對於電子郵件，可以顯示主電子郵件地址。

對於特定用途，可以在特定上下文中覆蓋這些值。 要強制值，請按一下 **啟用參數覆蓋** 表徵圖 此選項可能對以下項目非常有用：

* Test電子郵件，您可以添加電子郵件地址。 在您發佈了此旅程後，會向您發送電子郵件。
* 請參閱清單訂閱者的電子郵件地址。 瞭解詳情 [此使用案例](../building-journeys/message-to-subscribers-uc.md)。

按一下同一表徵圖以重置為預設參數。


## 瀏覽消息{#browse-message}

當在旅途中使用多條消息時，您可以從 **編輯內容** 的上界。

![](assets/inline-messages-multi-content.png)

你可以 [檢查警報](alerts.md) 和 [模擬](../design/preview.md) 每個內容都來自一個視圖。

## 複製訊息 {#duplicate-message}

可以從行程畫布複製現有郵件。

要執行此操作，請執行以下步驟：

1. 選擇要複製的消息。

1. 使用 **[!UICONTROL Copy]** 按鈕 **[!UICONTROL Action]** 的子菜單。

   ![](assets/message-duplicate.png)

1. 輸入 **crtl+V** 按鈕。

   該消息將添加到行程中。 所有設定與組態都將複製到新訊息中。

   ![](assets/message-duplicated.png)

1. 將消息更名為能夠將初始消息與副本區分，例如，在編輯消息時，如下所示：

   ![](assets/multi-message.png)


>[!NOTE]
>
>對於電子郵件，您還可以將現有郵件轉換為模板。 [了解更多](../design/email-templates.md)。

## 刪除消息{#delete-message}

要刪除消息，請使用渠道操作活動窗格頂部的資源回收筒表徵圖。

![](assets/delete-message.png)

使用 **[!UICONTROL Confirm]** 按鈕來驗證。
