---
title: 訊息中的警報
description: 了解如何檢查訊息內容驗證和疑難排解
feature: Journeys
topic: 內容管理
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 1%

---

# 訊息的警報{#publish-manage-messages}

## 發佈前檢查{#message-alerting}

建立訊息時，當您在發佈訊息前需要採取重要動作時，會發出警告。

警報會顯示在畫面右上方，如下所示：

![](assets/message-alerts.png)

>[!NOTE]
>
>如果未看到此按鈕，則未檢測到任何警報。

可能會發生兩種警報：

* **** 警告請參閱建議和最佳實務。例如，如果缺少選擇退出連結，則會顯示訊息。

* **** 錯誤只要訊息未解決，便無法發佈訊息。例如，訊息會警告您主題行已遺失。

所有可能的警告和錯誤都在[下面詳細說明。](#alerts-and-warnings)

>[!CAUTION]
>
> 發佈前，您需要解決所有&#x200B;**error**&#x200B;警報。

## 警告和錯誤清單{#alerts-and-warnings}

下面列出了系統檢查的設定和元素。 您也會找到如何調整設定以解決對應問題的相關資訊。

**警告**:

* **[!UICONTROL Opt out link not present in the email body]**:將取消訂閱連結新增至電子郵件內文是最佳作法。了解如何在[本小節](consent.md)中進行配置。

* **[!UICONTROL Text version of html is empty]**:別忘了定義電子郵件內文的文字版本，因為當無法顯示HTML內容時，會使用它。了解如何在[本區段](create-email-content.md#generate-text-version)中建立文字版本。

* **[!UICONTROL Empty link is present in email body]**:檢查電子郵件中的所有連結是否正確。了解如何管理[此小節](create-email-content.md)中的內容和連結。

* **[!UICONTROL Email size has exceeded the limit of 100KB]**:為獲得最佳傳送，請確定您的電子郵件大小不超過100KB。了解如何在[此區段](create-email-content.md)中編輯電子郵件內容。

**錯誤**:

* **[!UICONTROL Subject Line Not Present]**:電子郵件主旨行是必填欄位。在[此小節](create-email.md)中了解如何定義並個人化該小節。

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Push Variant is empty]**:遺失推播通知內文或標題時，會顯示此錯誤。了解如何在[此區段](create-push.md)中定義推播通知內容。

* **[!UICONTROL Email Variant is empty]**:未設定電子郵件內容時，會顯示此錯誤。了解如何在[此小節](design-emails.md)中設計電子郵件內容。

* **[!UICONTROL Preset doesn’t exist]**:如果您選取的預設集在訊息建立後刪除，則無法發佈訊息。如果發生此錯誤，請在消息&#x200B;**[!UICONTROL Properties]**&#x200B;中選擇其他預設集。 進一步了解[本小節](configuration/about-subdomain-delegation.md)中的品牌推廣。

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**:推播通知大小不能超過4KB。若要遵守此限制，請嘗試減少使用影像或表情符號。 了解如何在[此區段](create-push.md)中管理推播通知內容。

>[!CAUTION]
>
> 若要發佈訊息，您必須解決所有&#x200B;**error**&#x200B;警報。

<!--Other issues can stop publication such as:
* The push notification title is empty-->
