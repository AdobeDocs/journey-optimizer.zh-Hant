---
title: 消息中的警報
description: 瞭解如何檢查訊息內容驗證和疑難排解
translation-type: tm+mt
source-git-commit: 03af839084edafbc93188750db1f9f6c8b559d9e
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# 消息警報{#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## 發佈前檢查{#message-alerting}

當您建立訊息時，警報會在您發佈訊息前需要採取重要動作時發出警告。

警報顯示在畫面右上方，如下所示：

![](assets/message-alerts.png)

>[!NOTE]
>
>如果您未看到此按鈕，則未偵測到任何警報。

可能發生兩種警報：

* **警告** 請參閱建議和最佳實務。例如，如果遺失選擇退出連結，則會顯示訊息。

* **錯** 誤會阻止您發佈訊息，只要訊息未解決。例如，訊息會警告您主旨行已遺失。

所有可能的警告和錯誤都詳見[](#alerts-and-warnings)。

>[!CAUTION]
>
> 發佈前，您需要解決所有&#x200B;**error**&#x200B;警報。

## 警告與錯誤清單{#alerts-and-warnings}

系統檢查的設定和元素列在下面。 您也會找到如何調整組態以解決相關問題的資訊。

**警告**:

* **[!UICONTROL Opt out link not present in the email body]**:將取消訂閱連結新增至電子郵件內文是最佳做法。瞭解如何在[本節](consent.md)中設定它。

* **[!UICONTROL Text version of html is empty]**:不要忘記定義電子郵件內文的文字版本，因為當無法顯示HTML內容時，會使用它。瞭解如何在[本節](create-email-content.md#generate-text-version)中建立文字版本。

* **[!UICONTROL Empty link is present in email body]**:檢查您電子郵件中的所有連結是否正確。瞭解如何在[本節](create-email-content.md)中管理內容和連結。

* **[!UICONTROL Email size has exceeded the limit of 100KB]**:為獲得最佳傳送，請確定您的電子郵件大小不超過100KB。瞭解如何在[本節](create-email-content.md)中編輯電子郵件內容。

**錯誤**:

* **[!UICONTROL Subject Line Not Present]**:電子郵件主旨行是強制性的。瞭解如何在[本節](configure-email.md)中定義並個人化它。

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Push Variant is empty]**:當推播通知內文或標題遺失時，會顯示此錯誤。瞭解如何在[本節](configure-push.md)中定義推播通知內容。

* **[!UICONTROL Email Variant is empty]**:未設定電子郵件內容時，會顯示此錯誤。瞭解如何在[本節](design-emails.md)中設計電子郵件內容。

* **[!UICONTROL Preset doesn’t exist]**:如果您選取的預設集已在訊息建立後刪除，則無法發佈訊息。如果發生此錯誤，請在消息&#x200B;**[!UICONTROL Properties]**&#x200B;中選擇另一個預設。 進一步瞭解[本節](administration.md#cjm-branding)的品牌推廣。

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**:推播通知大小不能超過4KB。若要遵守此限制，請盡量減少影像或emoji的使用。 瞭解如何在[本節](configure-push.md)中管理您的推播通知內容。

>[!CAUTION]
>
> 要能夠發佈消息，您需要解決所有&#x200B;**error**&#x200B;警報。

<!--Other issues can stop publication such as:
* The push notification title is empty-->
