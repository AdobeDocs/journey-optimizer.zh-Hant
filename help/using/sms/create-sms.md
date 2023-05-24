---
solution: Journey Optimizer
product: journey optimizer
title: 建立簡訊訊息
description: 瞭解如何在Journey Optimizer建立SMS消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 33dccf32b60a6afb58931823016821fc1effcbd8
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 13%

---

# 建立簡訊訊息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="建立簡訊訊息"
>abstract="新增您的簡訊訊息並開始使用運算式編輯器對其進行個人化。"

## 添加SMS消息 {#create-sms-journey-campaign}

瀏覽下面的頁籤，瞭解如何在市場活動或行程中添加SMS消息。

>[!BEGINTABS]

>[!TAB 將SMS消息添加到旅程]

1. 開啟您的旅程，然後從 **操作** 的子菜單。

   ![](assets/sms_create_1.png)

1. 提供有關消息的基本資訊（標籤、說明、類別），然後選擇要使用的消息面。

   ![](assets/sms_create_2.png)

   有關如何配置行程的詳細資訊，請參閱 [此頁](../building-journeys/journey-gs.md)

   的 **[!UICONTROL 曲面]** 預設情況下，欄位是預填充的，用戶使用該通道的最後一個曲面。

現在，您可以開始設計來自 **[!UICONTROL 編輯內容]** 按鈕 [定義SMS內容](#sms-content)

>[!TAB 向市場活動添加SMS消息]

1. 建立新的計畫市場活動或API觸發的市場活動，選擇 **[!UICONTROL 簡訊]** 選擇 **[!UICONTROL 應用表面]** 的下界。 [瞭解有關SMS配置的詳細資訊](sms-configuration.md)。

   ![](assets/sms_create_3.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 屬性]** 編輯活動 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]**。

   ![](assets/sms_create_4.png)

1. 在 **[!UICONTROL 動作跟蹤]** 部分，指定是否要跟蹤SMS消息中連結的按一下。

1. 按一下 **[!UICONTROL 選擇受眾]** 按鈕，來定義可用Adobe Experience Platform段清單中的目標受眾。 [了解更多](../segment/about-segments.md)。

1. 在 **[!UICONTROL 標識命名空間]** 欄位中，選擇要用於標識選定段中的個體的命名空間。 [了解更多](../event/about-creating.md#select-the-namespace)。

   ![](assets/sms_create_5.png)

1. 市場活動旨在在特定日期或循環頻率上執行。 瞭解如何配置 **[!UICONTROL 計畫]** 你的競選團隊 [此部分](../campaigns/create-campaign.md#schedule)。

1. 從 **[!UICONTROL 操作觸發器]** 的子菜單。 **[!UICONTROL 頻率]** 您的SMS消息：

   * 一次
   * 每日
   * 每週
   * 月

現在，您可以開始設計來自 **[!UICONTROL 編輯內容]** 按鈕 [設計您的SMS內容](#sms-content)

>[!ENDTABS]

## 定義SMS內容{#sms-content}

1. 在行程或市場活動配置螢幕中，按一下 **[!UICONTROL 編輯內容]** 按鈕來配置SMS內容。

1. 按一下 **[!UICONTROL 消息]** 欄位以開啟表達式編輯器。

   ![](assets/sms-content.png)

1. 使用表達式編輯器定義內容並添加動態內容。 可以使用任何屬性，如配置檔案名稱或城市。 瞭解有關 [個性化](../personalization/personalize.md) 和 [動態內容](../personalization/get-started-dynamic-content.md) 的子菜單。

1. 定義內容後，可以將跟蹤URL添加到郵件中。 為此，請訪問 **[!UICONTROL 幫助程式函式]** 的 **[!UICONTROL 幫手]**。

   請注意，要使用URL縮短功能，必須先配置子域，然後該子域將連結到您的曲面。 [了解更多](sms-subdomains.md)

   >[!CAUTION]
   >
   > 要訪問和編輯SMS子域，您必須具有 **[!UICONTROL 管理SMS子域]** 在生產沙盒上的權限。

   ![](assets/sms_tracking_1.png)

1. 在 **[!UICONTROL 幫助程式函式]** 菜單，按一下 **[!UICONTROL URL函式]** ，然後選擇 **[!UICONTROL 添加URL]**。

   ![](assets/sms_tracking_2.png)

1. 在 `originalUrl` 欄位，貼上要縮短的URL。

1. 按一下 **[!UICONTROL 保存]** 並在預覽中查看您的留言。 您可以使用 **[!UICONTROL 模擬內容]** 預覽縮短的URL或個性化內容。

   ![](assets/sms-content-preview.png)

您現在可以test並將您的SMS消息發送給您的受眾。 [瞭解更多資訊](send-sms.md)
發送後，您可以在「促銷活動」或「行程」報告中衡量SMS的影響。 如需報告的詳細資訊，請參閱[本區段](../reports/campaign-global-report.md#sms-tab)。

>[!NOTE]
>
>根據行業標準及法規，所有簡訊行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 為此，SMS收件人可以使用選擇加入和選擇退出關鍵字進行回復。 [瞭解如何管理退出選項](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**相關主題**

* [預覽、test和發送SMS消息](send-sms.md)
* [設定簡訊頻道](sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [在市場活動中添加消息](../campaigns/create-campaign.md)
