---
title: 訊息中的警報
description: 了解如何檢查訊息內容驗證和疑難排解
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# 訊息上的警報 {#publish-manage-messages}

## 發佈前檢查 {#message-alerting}

建立訊息時，當您在發佈訊息前需要採取重要動作時，會發出警告。

警報會顯示在畫面右上方，如下所示：

![](assets/message-alerts.png)

>[!NOTE]
>
>如果未看到此按鈕，則未檢測到任何警報。

可能會發生兩種警報：

* **警告** 請參閱建議和最佳實務。 例如，如果缺少選擇退出連結，則會顯示訊息。

* **錯誤** 只要訊息未解決，就無法發佈訊息。 例如，訊息會警告您主題行已遺失。

會詳細說明所有可能的警告和錯誤 [low](#alerts-and-warnings).

>[!CAUTION]
>
> 你需要解決所有 **錯誤** 發佈前發出警報。

## 警告和錯誤清單 {#alerts-and-warnings}

下面列出了系統檢查的設定和元素。 您也會找到如何調整設定以解決對應問題的相關資訊。

**警告**:

* **[!UICONTROL Opt out link not present in the email body]**:將取消訂閱連結新增至電子郵件內文是最佳作法。 了解如何在 [本節](consent.md).

* **[!UICONTROL Text version of html is empty]**:別忘了定義電子郵件內文的文字版本，因為當無法顯示HTML內容時，會使用它。 了解如何在 [本節](create-email-content.md#generate-text-version).

* **[!UICONTROL Empty link is present in email body]**:檢查電子郵件中的所有連結是否正確。 了解如何管理 [本節](create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB]**:為獲得最佳傳送，請確定您的電子郵件大小不超過100KB。 了解如何在 [本節](create-email-content.md).

**錯誤**:

* **[!UICONTROL Subject Line Not Present]**:電子郵件主旨行是必填欄位。 了解如何在 [本節](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Push Variant is empty]**:遺失推播通知內文或標題時，會顯示此錯誤。 了解如何在中定義推播通知內容 [本節](create-push.md).

* **[!UICONTROL Email Variant is empty]**:未設定電子郵件內容時，會顯示此錯誤。 了解如何在 [本節](design-emails.md).

* **[!UICONTROL Preset doesn’t exist]**:如果您選取的預設集在訊息建立後刪除，則無法發佈訊息。 如果發生此錯誤，請在訊息中選取其他預設集 **[!UICONTROL Properties]**. 進一步了解品牌推廣 [本節](configuration/about-subdomain-delegation.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**:推播通知大小不能超過4KB。 若要遵守此限制，請嘗試減少使用影像或表情符號。 了解如何在 [本節](create-push.md).

>[!CAUTION]
>
> 若要發佈訊息，您必須解析 **錯誤** 警報。

<!--Other issues can stop publication such as:
* The push notification title is empty-->
