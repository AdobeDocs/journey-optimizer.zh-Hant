---
solution: Journey Optimizer
product: journey optimizer
title: Define the API triggered campaign audience
description: Learn how to define the API triggered campaign audience.
topic: Content Management
role: Developer
level: Experienced
keywords: campaigns, API-triggered, REST, optimizer, messages
exl-id: 6dda5687-3742-4e88-be7c-c4969b183161
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 3%

---

# Define the API triggered campaign audience {#api-audience}

Use the **[!UICONTROL Audience]** tab to define the campaign audience.

![](assets/campaign-audience.png)

## 選取客群

**For Marketing API triggered campaigns**, click the **[!UICONTROL Select audience]** button to display the list of available Adobe Experience Platform audiences. [Learn more about audiences](../audience/about-audiences.md).

>[!IMPORTANT]
>
>The use of audiences and attributes from [audience composition](../audience/get-started-audience-orchestration.md) is currently unavailable for use with Healthcare Shield or Privacy and Security Shield.

**For Transactional API triggered campaigns**, the targeted profiles need to be defined in the API call. A single API call supports up to 20 unique recipients. Each recipient must have a unique user ID, duplicate user IDs are not permitted. Learn more in the [Interactive Message Execution API documentation](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMUnitaryMessageExecution){target="_blank"}

## 選取身分識別類型

In the **[!UICONTROL Identity type]** field, choose the type of key to use to identify the individuals from the selected audience. You can either use an existing identity type or create a new one using the Adobe Experience Platform Identity Service. Standard Identity namespaces are listed on [this page](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

Only one identity type is allowed per campaign. Individuals belonging to a segment that does not have the selected identity type among their different identities cannot be targeted by the campaign. Learn more about identity types and namespaces in the [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hant){target="_blank"}.

## Activate profile creation at campaign execution

In some cases, you may need to send transactional messages to profiles that do not exist in the system. For example if an unknown user tries to reset password on your website. When a profile does not exist in the database, Journey Optimizer allows you to automatically create it when executing the campaign to allow sending the message to this profile.

To activate profile creation at campaign execution, toggle the **[!UICONTROL Create new profiles]** option on. 如果停用此選項，則會拒絕任何傳送的未知設定檔，且API呼叫將失敗。

![](assets/api-triggered-create-profile.png)

>[!IMPORTANT]
>
>在大量交易式傳送使用案例中，提供此選項是為了建立&#x200B;**極小的磁碟區設定檔**，其中大量的設定檔已存在於平台中。
>
>在&#x200B;**AJO互動式訊息設定檔資料集**&#x200B;資料集中，針對每個傳出頻道（電子郵件、簡訊和推播）分別使用三個預設名稱空間（電子郵件、電話和ECID）建立未知的設定檔。 不過，如果您使用自訂名稱空間，則會使用相同的自訂名稱空間建立身分。
>
>[高輸送量行銷活動](../campaigns/api-triggered-high-throughput.md)無法在執行時建立設定檔，因為此模式不依賴Adobe設定檔。 系統不會檢查設定檔是否存在。

## 啟用 Webhook {#webhook}

對於異動API觸發的行銷活動，您可以啟用Webhook以接收對訊息執行狀態的即時回饋。 若要這麼做，請切換&#x200B;**[!UICONTROL 啟用Webhook]**&#x200B;選項，將傳遞狀態事件傳送至已設定的Webhook。

![](assets/api-triggered-webhook.png)

Webhook設定是在&#x200B;**[!UICONTROL 管理]** / **[!UICONTROL 管道]** / **[!UICONTROL 意見Webhook]**&#x200B;功能表中集中管理。 管理員可從該處建立和編輯webhook端點。 [瞭解如何建立意見回饋Webhook](../configuration/feedback-webhooks.md)

## 後續步驟 {#next}

準備好行銷活動設定和內容後，您就可以排程其執行。 [了解更多](api-triggered-campaign-schedule.md)
