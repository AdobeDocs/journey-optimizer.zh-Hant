---
title: 建立電子郵件
description: 瞭解如何在Journey Optimizer建立電子郵件
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 9%

---

# 建立電子郵件 {#configure-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="電子郵件建立"
>abstract="只需三個簡單步驟即可定義電子郵件參數。"

可以建立電子郵件：

* 在 **旅程**:在您的旅途中添加電子郵件活動並定義基本設定後，使用 **[!UICONTROL Actions: Email]** 右窗格，為推送通知建立內容。

   有關如何配置行程的詳細資訊，請參閱此 [頁](../building-journeys/journey-gs.md)。

   ![](assets/email-edit-content.png)

* 在 **活動**:建立市場活動後，選擇「電子郵件」作為活動並定義基本設定。

   有關如何配置市場活動的詳細資訊，請參閱此 [頁](../campaigns/create-campaign.md#configure)。

   ![](assets/email_campaign.png)

## 定義您的電子郵件內容{#email-content}

使用 [!DNL Journey Optimizer] 電子郵件設計器 [從頭開始設計電子郵件](../design/create-email-content.md)。 如果您有現有內容，則 [在電子郵件設計器中導入它](../design/existing-content.md)或 [對自己的內容進行編碼](../design/code-content.md) 在 [!DNL Journey Optimizer]。

[!DNL Journey Optimizer] 有一套 [內置模板](../design/email-templates.md) 來幫助你。 任何電子郵件也可以另存為模板。

使用 [!DNL Journey Optimizer] Expression編輯器，使用配置檔案的資料個性化您的消息。 如需個人化的詳細資訊，請參閱[此章節](../personalization/personalize.md)。

## 電子郵件跟蹤{#email-tracking}

如果要通過開啟和/或按一下連結來跟蹤收件人的行為，請啟用以下選項： **[!UICONTROL Email opens]** 和 **[!UICONTROL Click on email]**。

瞭解有關跟蹤的詳細資訊 [此部分](../design/message-tracking.md)。

## 驗證您的電子郵件內容{#email-content-validate}

使用左側的預覽部分控制電子郵件的呈現，並使用test配置檔案檢查個性化設定。 如需詳細資訊，請參閱[本章節](../design/preview.md)。

![](assets/messages-simple-preview.png)


您還必須檢查編輯器上半部分的警報。  其中一些是簡單的警告，但其他警告可能會阻止您使用該消息。 請參閱[此章節](alerts.md)深入瞭解。


>[!NOTE]
>
>的 **[!UICONTROL From email]** 和 **[!UICONTROL From name]** 由 **[!UICONTROL Surface]** 在 [建立消息](get-started-content.md)。

