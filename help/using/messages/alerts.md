---
title: 訊息中的警報
description: 了解如何檢查訊息內容驗證和疑難排解
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 32c69ef268c78ba834612d16b2ac1c721fb5df56
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 7%

---

# 檢查訊息的警報 {#messages-alerts}

## 傳送前先檢查 {#message-alerting}

當您設計訊息時，當缺少鍵值設定時，警報會顯示在介面中。

編輯訊息內容時，警報會顯示在畫面右上方。

![](assets/alerts-details.png)

>[!NOTE]
>
>如果未看到此按鈕，則未檢測到任何警報。

可能會發生兩種警報：

* **警告** 請參閱建議和最佳實務。 例如，如果缺少選擇退出連結，則會顯示訊息。

* **錯誤** 只要未解決歷程，就無法進行測試或啟動歷程。 例如，訊息會警告您主題行已遺失。

會詳細說明所有可能的警告和錯誤 [low](#alerts-and-warnings).

>[!CAUTION]
>
> 你需要解決所有 **錯誤** 使用訊息測試或啟動歷程前發出警報。

## 警告和錯誤清單 {#alerts-and-warnings}

下面列出了系統檢查的設定和元素。 您也會找到如何調整設定以解決對應問題的相關資訊。

**警告**:

* **[!UICONTROL 電子郵件內文中沒有選擇退出連結]**:將取消訂閱連結新增至電子郵件內文是最佳作法。 了解如何在 [本節](../privacy/opt-out.md#opt-out-management).

   >[!NOTE]
   >
   >行銷類電子郵件務必要加入選擇退出連結，管理異動類的訊息則非必要。 訊息類別 (**[!UICONTROL 行銷]**&#x200B;或&#x200B;**[!UICONTROL 交易]**) 會在[頻道介面](../configuration/channel-surfaces.md#email-type) (即訊息預設) 層級[建立訊息](get-started-content.md#create-new-message)時定義。

* **[!UICONTROL HTML的文本版本為空]**:別忘了定義電子郵件內文的文字版本，因為當無法顯示HTML內容時，會使用它。 了解如何在 [本節](../design/text-version-email.md).

* **[!UICONTROL 電子郵件內文中存在空連結]**:檢查電子郵件中的所有連結是否正確。 了解如何管理 [本節](../design/create-email-content.md).

* **[!UICONTROL 電子郵件大小已超過100KB的限制]**:為獲得最佳傳送，請確定您的電子郵件大小不超過100KB。 了解如何在 [本節](../design/create-email-content.md).

**錯誤**:

* **[!UICONTROL 主題行缺失]**:電子郵件主旨行是必填欄位。 了解如何在 [本節](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL 訊息的推送版本為空]**:遺失推播通知內文或標題時，會顯示此錯誤。 了解如何在中定義推播通知內容 [本節](create-push.md).

* **[!UICONTROL 郵件的電子郵件版本為空]**:未設定電子郵件內容時，會顯示此錯誤。 了解如何在 [本節](../design/design-emails.md).

* **[!UICONTROL 曲面不存在]**:如果在建立消息後刪除了所選曲面，則無法使用消息。 如果發生此錯誤，請在消息中選取另一個曲面 **[!UICONTROL 屬性]**. 進一步了解 [本節](../configuration/channel-surfaces.md).

* **[!UICONTROL 推播iOS/Android裝載已超過4KB的限制]**:推播通知大小不能超過4KB。 若要遵守此限制，請嘗試減少使用影像或表情符號。 了解如何在 [本節](create-push.md).

>[!CAUTION]
>
> 若要使用您的訊息，您必須解析 **錯誤** 警報。

<!--Other issues can stop publication such as:
* The push notification title is empty-->
