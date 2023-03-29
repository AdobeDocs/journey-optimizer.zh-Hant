---
solution: Journey Optimizer
product: journey optimizer
title: 建立簡訊訊息
description: 了解如何在Journey Optimizer中建立SMS訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 14%

---

# 建立簡訊訊息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="建立簡訊訊息"
>abstract="新增您的簡訊訊息並開始使用運算式編輯器對其進行個人化。"

## 新增SMS訊息 {#create-sms-journey-campaign}

瀏覽下方的標籤，了解如何在行銷活動或歷程中新增SMS訊息。

>[!BEGINTABS]

>[!TAB 將SMS訊息新增至歷程]

1. 開啟您的歷程，然後從 **動作** 區段。

   ![](assets/sms_create_1.png)

1. 提供訊息的基本資訊（標籤、說明、類別），然後選擇要使用的訊息表面。

   ![](assets/sms_create_2.png)

   如需如何設定歷程的詳細資訊，請參閱 [本頁](../building-journeys/journey-gs.md)

<!-- The **[!UICONTROL Surface]**field is pre-filled, by default, with the last surface used for that channel by the user. -->

您現在可以開始從 **[!UICONTROL 編輯內容]** 按鈕。 [定義您的SMS內容](#sms-content)

>[!TAB 新增SMS訊息至促銷活動]

1. 建立新的排程或API觸發促銷活動，請選取 **[!UICONTROL 簡訊]** 作為您的動作，並選取 **[!UICONTROL 應用程式表面]** 來使用。 [進一步了解SMS設定](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 屬性]** 區段，編輯您的促銷活動 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]**.

   ![](assets/sms_create_4.png)

1. 在 **[!UICONTROL 動作追蹤]** 區段，指定是否要追蹤SMS訊息中連結的點按次數。

1. 按一下 **[!UICONTROL 選取對象]** 按鈕，從可用的Adobe Experience Platform區段清單中定義要鎖定的對象。 [了解更多](../segment/about-segments.md)。

1. 在 **[!UICONTROL 身分命名空間]** 欄位中，選擇要使用的命名空間，以識別所選區段中的個人。 [了解更多](../event/about-creating.md#select-the-namespace)。

   ![](assets/sms_create_5.png)

1. 促銷活動設計為在特定日期或循環頻率上執行。 了解如何設定 **[!UICONTROL 排程]** 在 [本節](../campaigns/create-campaign.md#schedule).

1. 從 **[!UICONTROL 動作觸發器]** 菜單，選擇 **[!UICONTROL 頻率]** 簡訊：

   * 一次
   * 每日
   * 每週
   * 月

您現在可以開始從 **[!UICONTROL 編輯內容]** 按鈕。 [設計您的SMS內容](#sms-content)

>[!ENDTABS]

## 定義您的SMS內容{#sms-content}

1. 在歷程或行銷活動設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕來設定SMS內容。

1. 按一下 **[!UICONTROL 訊息]** 欄位來開啟運算式編輯器。

   ![](assets/sms-content.png)

1. 使用運算式編輯器來定義內容並新增動態內容。 您可以使用任何屬性，例如設定檔名稱或城市。 深入了解 [個人化](../personalization/personalize.md) 和 [動態內容](../personalization/get-started-dynamic-content.md) 在運算式編輯器中。

1. 定義內容後，您可以將追蹤URL新增至訊息。 若要這麼做，請存取 **[!UICONTROL 輔助函式]** 選取 **[!UICONTROL Helpers]**.

   請注意，若要使用URL縮短功能，您必須先設定子網域，然後將其連結至您的曲面。 [了解更多](sms-subdomains.md)

   ![](assets/sms_tracking_1.png)

1. 在 **[!UICONTROL 輔助函式]** 按一下 **[!UICONTROL URL函式]** 然後選取 **[!UICONTROL 新增URL]**.

   ![](assets/sms_tracking_2.png)

1. 在 `originalUrl` 欄位，貼上您要縮短的URL。

1. 按一下 **[!UICONTROL 儲存]** 並在預覽中檢查您的訊息。 您可以使用 **[!UICONTROL 模擬內容]** 預覽縮短的URL或個人化內容。

   ![](assets/sms-content-preview.png)

您現在可以測試SMS訊息並傳送給您的對象。 [深入了解](send-sms.md)
傳送後，您就可以在行銷活動或歷程報表中測量SMS的影響。 如需報告的詳細資訊，請參閱[本區段](../reports/campaign-global-report.md#sms-tab)。

>[!NOTE]
>
>根據行業標準及法規，所有簡訊行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 若要這麼做，SMS收件者可以使用選擇加入和選擇退出關鍵字回覆。 [了解如何管理選擇退出](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**相關主題**

* [預覽、測試和傳送您的SMS訊息](send-sms.md)
* [設定簡訊頻道](sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)
* [在歷程中新增訊息](../building-journeys/journeys-message.md)
* [在促銷活動中新增訊息](../campaigns/create-campaign.md)
