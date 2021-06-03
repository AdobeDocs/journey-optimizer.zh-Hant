---
title: 管理選擇退出
description: 了解如何管理選擇退出與隱私權
source-git-commit: 738d72e8f3ba204219086f19252220ff833369cb
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 1%

---

# 管理選擇退出 {#consent}

![](assets/do-not-localize/badge.png)

使用[!DNL Journey Optimizer]追蹤收件者對通訊的同意，並管理其偏好設定和訂閱，以了解他們想如何與您的品牌互動。<!--Their preferences and subscriptions are handled through Consent management.-->

GDPR等法規規定，您必須先符合特定要求，才能使用資料主體的資訊。 此外，資料主體應可隨時修改其同意。

**為什麼這很重要？**

* 未遵守這些法規會為您的品牌帶來法律風險。
* 它可協助您避免傳送未經請求的通訊給收件者，這可能會使他們將您的訊息標示為垃圾訊息，並損害您的名譽。

[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant)中，深入了解管理隱私權和適用法規。

<!--* Recipients should be able to opt-in/opt-out from receiving electronic communication through one or more channel
* Recipients expect the brand to offer preference centre capability that controls how brand should engage with them (example: channel of communication, invasive and non-invasive tracking etc). This helps to fulfil regulatory obligations and also facilitates quality engagement with recipient. 
* The third category is the capability to offer subscription to recipients (newsletter, etc)-->

## 退出管理{#opt-out-management}

向收件者提供取消訂閱從品牌接收通訊的能力是一項法律規定。 [Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=en#regulations)中可適用法規的詳細資訊。

因此，您必須在每封寄送給收件者的電子郵件中一律包含&#x200B;**取消訂閱連結**:
* 按一下此連結時，收件者會被導向至登陸頁面，其中包含用於確認選擇退出的按鈕。
* 按一下退出按鈕後，會發出Adobe I/O呼叫，以使用此資訊更新設定檔資料。 [深入了解](#consent-service-api)。

若要新增取消訂閱連結，請遵循下列步驟：

1. 建立您的取消訂閱登錄頁面。
1. 在您選擇的協力廠商系統上托管您的登錄頁面。
1. [建立訊](../../help/using/create-message.md) 息 [!DNL Journey Optimizer]。

   <!--The link to your landing page should contain a static URL and the profile ID.-->

1. 選取內容中的文字，並使用內容工具列插入連結。

   ![](assets/opt-out-insert-link.png)

1. 從&#x200B;**[!UICONTROL Link type]**&#x200B;下拉清單中選擇&#x200B;**[!UICONTROL Unsubscription link]**。

   ![](assets/opt-out-link-type.png)

1. 在&#x200B;**[!UICONTROL Unsubscription page URL]**&#x200B;影格中，將連結複製至您的登錄頁面。

   ![](assets/opt-out-link-url.png)

1. 按一下「**[!UICONTROL Save]**」。

1. 儲存內容並[發佈訊息](../../help/using/publish-manage-message.md)。

   >[!NOTE]
   >
   >您的第三方登錄頁面URL將包含三個參數，這些參數將用來透過Adobe I/O呼叫更新設定檔的偏好設&#x200B;定。 [了解更多資訊](#consent-service-api)。

1. 透過[journey](building-journeys/journey.md)傳送含有登錄頁面連結的訊息。

1. 收到訊息後，如果收件者按一下取消訂閱連結，便會顯示您的登錄頁面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件者按一下登錄頁面中的選擇退出按鈕（此處為&#x200B;**取消訂閱**&#x200B;按鈕），則會透過[Adobe I/O呼叫](#opt-out-api)更新設定檔資料。

   接著，退出收件者會重新導向至確認訊息畫面，指出退出是否成功。

   ![](assets/opt-out-confirmation-example.png)

   因此，除非再次訂閱，否則此使用者將不會收到您品牌的通訊。

若要檢查對應設定檔的選項是否已更新，請前往Experience Platform，並選取身分命名空間和對應的身分值來存取設定檔。 請參閱[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=en#getting-started)以了解更多資訊。

![](assets/opt-out-profile-choice.png)

在&#x200B;**[!UICONTROL Attributes]**&#x200B;標籤中，您可以看到&#x200B;**[!UICONTROL choice]**&#x200B;的值已變更為&#x200B;**[!UICONTROL no]**。

<!--The opt-out URL is resolved upon each recipient receiving the message. It is then personalized with the relevant encrypted parameters (profile ID, profile name, journey ID, sandbox ID, and message execution ID).-->

## 退出API呼叫{#opt-out-api}

一旦收件者按一下取消訂閱連結而選擇退出後，就會呼叫Adobe I/OAPI <!--Consent service API to capture the encrypted data and-->以更新對應設定檔的偏好設定。

此Adobe I/OPOST呼叫如下：

端點：cjm.adobe.io/imp/consent/preferences

查詢參數：
* **參數**:包含加密的裝載
* **sig**:簽名  <!--which signature?-->
* **pid**:加密的配置檔案ID

這些參數可從傳送給收件者的取消訂閱連結中取得，亦即將為指定收件者開啟您第三方登陸頁面的URL:

![](assets/opt-out-parameters.png)

<!--QUESTION: How do you get the URL built for each recipient? Do you have to wait until each targeted recipient receives the unsubscribe link or can you deduce it in advance? Is it done automatically upon the API call or do you have to do something manually for each profile? In other words will the LP automatically include the 3 parameters or do you have to insert something manually? Still not completely clear-->

標題要求：
* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* 授權（來自您技術帳戶的使用者代號）<!--How do you find this information? And other header elements?-->

要求內文：

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

<!--The Consent service /-->[!DNL Journey Optimizer] will <!--decrypt and-->use these parameters to update the corresponding profile's choice. <!--and provide an answer back to the landing page.-->

## 推送選擇退出管理{#push-opt-out-management}

推送收件者可以透過其裝置本身取消訂閱。

例如，在下載或使用您的應用程式時，使用者可以選取停止通知。 同樣地，他們可以透過行動作業系統變更通知設定。
