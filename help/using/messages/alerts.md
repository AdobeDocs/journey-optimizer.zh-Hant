---
title: 郵件中的警報
description: 瞭解如何檢查郵件內容驗證和故障排除
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 3%

---

# 檢查郵件的警報 {#messages-alerts}

## 發送前檢查 {#message-alerting}

在設計消息時，當缺少鍵設定時，會在介面中顯示警報。

編輯消息內容時，警報顯示在螢幕右上方。

![](assets/alerts-details.png)

>[!NOTE]
>
>如果未看到此按鈕，則未檢測到任何警報。

可以發生兩種類型的警報：

* **警告** 請參閱建議和最佳做法。 例如，如果缺少opt-out連結，則將顯示一條消息。

* **錯誤** 只要未解決，就阻止您測試或激活行程。 例如，一條消息將警告您主題行丟失。

所有可能的警告和錯誤都已詳細列出 [下](#alerts-and-warnings)。

>[!CAUTION]
>
> 你需要解決所有 **錯誤** 使用消息測試或激活行程之前發出警報。

## 警告和錯誤清單 {#alerts-and-warnings}

下面列出了系統檢查的設定和元素。 您還將找到有關如何調整配置以解決相應問題的資訊。

**警告**:

* **[!UICONTROL The opt-out link is not present in the email body]**:將未訂閱連結添加到電子郵件正文是最佳做法。 瞭解如何在 [此部分](consent.md#opt-out-management)。

   >[!NOTE]
   >
   >行銷類電子郵件務必要加入選擇退出連結，管理異動類的訊息則非必要。 消息類別(**[!UICONTROL Marketing]** 或 **[!UICONTROL Transactional]**) [通道表面](../configuration/message-presets.md#email-type) （即消息預設）級別和時間 [建立消息](get-started-content.md#create-new-message)。

* **[!UICONTROL Text version of HTML is empty]**:不要忘記定義電子郵件正文的文本版本，因為當無法顯示HTML內容時，將使用它。 瞭解如何在中建立文本版本 [此部分](../design/text-version-email.md)。

* **[!UICONTROL Empty link is present in email body]**:檢查電子郵件中的所有連結是否正確。 瞭解如何管理中的內容和連結 [此部分](../design/create-email-content.md)。

* **[!UICONTROL Email size has exceeded the limit of 100KB]**:要獲得最佳傳送，請確保電子郵件大小不超過100KB。 瞭解如何在中編輯電子郵件內容 [此部分](../design/create-email-content.md)。

**錯誤**:

* **[!UICONTROL The subject line is missing]**:電子郵件主題行是必填項。 瞭解如何在中定義和個性化它 [此部分](create-email.md)。

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL The push version of the message is empty]**:當缺少推送通知正文或標題時，將顯示此錯誤。 瞭解如何在中定義推送通知內容 [此部分](create-push.md)。

* **[!UICONTROL The email version of the message is empty]**:未配置電子郵件內容時，將顯示此錯誤。 瞭解如何在 [此部分](../design/design-emails.md)。

* **[!UICONTROL Surface doesn’t exist]**:如果在建立消息後刪除了所選曲面，則不能使用消息。 如果出現此錯誤，請在消息中選擇另一個曲面 **[!UICONTROL Properties]**。 瞭解有關中的通道曲面的詳細資訊 [此部分](../configuration/message-presets.md)。

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**:推送通知大小不能超過4KB。 要尊重此限制，請嘗試減少使用影像或表情符號。 瞭解如何在中管理推送通知內容 [此部分](create-push.md)。

>[!CAUTION]
>
> 要能夠使用您的消息，您需要解決所有 **錯誤** 警報。

<!--Other issues can stop publication such as:
* The push notification title is empty-->
