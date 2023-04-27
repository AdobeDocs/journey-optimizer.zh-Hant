---
solution: Journey Optimizer
product: journey optimizer
title: 建立電子郵件
description: 了解如何在 Journey Optimizer 中建立電子郵件
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 建立，電子郵件，開始，歷程，行銷活動
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 9%

---

# 建立電子郵件 {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="電子郵件建立"
>abstract="僅需三個簡單的步驟即可定義您的電子郵件參數。"

在中建立電子郵件 [!DNL Journey Optimizer]，請遵循下列步驟。

## 在歷程或行銷活動中建立電子郵件 {#create-email-journey-campaign}

新增 **[!UICONTROL 電子郵件]** 動作至歷程或行銷活動，並根據您的案例遵循下列步驟。

>[!BEGINTABS]

>[!TAB 新增電子郵件至歷程]

1. 開啟您的歷程，然後拖放 **[!UICONTROL 電子郵件]** 活動 **[!UICONTROL 動作]** 區段。

1. 提供訊息的基本資訊（標籤、說明、類別）。

1. 選擇 [電子郵件表面](email-settings.md) 來使用。

   ![](assets/email_journey.png)

   依預設，欄位會預填，使用者用於該管道的最後一個曲面。

>[!NOTE]
>
>如果您要從歷程傳送電子郵件，您可以運用Adobe Journey Optimizer的「傳送時間最佳化」功能，根據歷史開啟率和點按率預測傳送訊息的最佳時機，以最大化參與。 [了解如何使用傳送時間最佳化](../building-journeys/journeys-message.md#send-time-optimization)

如需如何設定歷程的詳細資訊，請參閱 [本頁](../building-journeys/journey-gs.md).

>[!TAB 新增電子郵件至行銷活動]

1. 建立新的排程或API觸發促銷活動，然後選取 **[!UICONTROL 電子郵件]** 作為您的動作。

1. 選擇 [電子郵件表面](email-settings.md) 來使用。

   ![](assets/email_campaign.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 完成建立電子郵件促銷活動的步驟，例如促銷活動屬性、 [對象](../segment/about-segments.md)，和 [排程](../campaigns/create-campaign.md#schedule).

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

如需如何設定促銷活動的詳細資訊，請參閱 [本頁](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## 定義您的電子郵件內容 {#define-email-content}

<!-- update the quarry component with right ID value-->

>[!CONTEXTUALHELP]
>id="test_id"
>title="設定電子郵件內容"
>abstract="建立您的電子郵件內容。定義其主旨，然後利用電子郵件設計工具建置和個人化電子郵件內文。"

1. 在歷程或行銷活動設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕來設定電子郵件內容。 [了解更多](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. 在 **[!UICONTROL 標題]** 區段 **[!UICONTROL 編輯內容]** 螢幕， **[!UICONTROL 從名稱]**, **[!UICONTROL 從電子郵件]** 和 **[!UICONTROL 密件副本]** 欄位來自您選取的電子郵件表面。 [了解更多](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. 您可以新增主旨行。 直接在對應欄位中輸入純文字，或使用 [運算式編輯器](../personalization/personalization-build-expressions.md) 個人化您的主旨行。

1. 按一下 **[!UICONTROL 編輯電子郵件內文]** 按鈕，開始使用 [!DNL Journey Optimizer] 電子郵件設計工具。 [了解更多](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. 如果您在促銷活動中，也可以按一下 **[!UICONTROL 代碼編輯器]** 按鈕，使用顯示的彈出窗口以純HTML編寫您自己的內容。

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >如果您已透過電子郵件設計工具建立或匯入內容，此內容將以HTML顯示。

## 檢查警報 {#check-email-alerts}

當您設計訊息時，當遺失金鑰設定時，警示會顯示在介面中（位於畫面右上方）。

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>如果未看到此按鈕，則未檢測到任何警報。

下面列出了系統檢查的設定和元素。 您也會找到如何調整設定以解決對應問題的相關資訊。

可能會發生兩種警報：

* **警告** 請參閱建議和最佳實務，例如：

   * **[!UICONTROL 電子郵件內文中沒有選擇退出連結]**:將取消訂閱連結新增至電子郵件內文是最佳作法。 了解如何在 [本節](../privacy/opt-out.md#opt-out-management).

      >[!NOTE]
      >
      >行銷類電子郵件務必要加入選擇退出連結，管理異動類的訊息則非必要。 訊息類別(**[!UICONTROL 行銷]** 或 **[!UICONTROL 交易]**)是在 [通道表面](email-settings.md#email-type) 級別和時間 [建立訊息](#create-email-journey-campaign) 從歷程或行銷活動。

   * **[!UICONTROL HTML的文本版本為空]**:別忘了定義電子郵件內文的文字版本，因為當無法顯示HTML內容時，會使用它。 了解如何在 [本節](text-version-email.md).

   * **[!UICONTROL 電子郵件內文中存在空連結]**:檢查電子郵件中的所有連結是否正確。 了解如何管理 [本節](content-from-scratch.md).

   * **[!UICONTROL 電子郵件大小已超過100KB的限制]**:為獲得最佳傳送，請確定您的電子郵件大小不超過100KB。 了解如何在 [本節](content-from-scratch.md).

* **錯誤** 只要未解決歷程/行銷活動，就會阻止您測試或啟動這些活動，例如：

   * **[!UICONTROL 主題行缺失]**:電子郵件主旨行是必填欄位。 了解如何在 [本節](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL 郵件的電子郵件版本為空]**:未設定電子郵件內容時，會顯示此錯誤。 了解如何在 [本節](get-started-email-design.md).

   * **[!UICONTROL 曲面不存在]**:如果在建立消息後刪除了所選曲面，則無法使用消息。 如果發生此錯誤，請在消息中選取另一個曲面 **[!UICONTROL 屬性]**. 進一步了解 [本節](../configuration/channel-surfaces.md).


>[!CAUTION]
>
>若要使用電子郵件測試或啟動歷程/行銷活動，您必須解析 **錯誤** 警報。

## 預覽並傳送您的電子郵件

定義訊息內容後，您可以預覽訊息內容以控制電子郵件的呈現，並使用測試設定檔檢查個人化設定。 [了解更多](preview.md)

![](assets/email_designer_edit_simulate.png)

當您的電子郵件準備就緒時，請完成 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md)，然後啟用它以傳送訊息。

>[!NOTE]
>
>若要透過電子郵件開啟和/或互動來追蹤收件者的行為，請確定 **[!UICONTROL 追蹤]** 區段會在歷程的 [電子郵件活動](../building-journeys/journeys-message.md) 或在電子郵件中 [行銷活動](../campaigns/create-campaign.md).<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] Expression editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

