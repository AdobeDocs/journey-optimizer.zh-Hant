---
title: 管理選擇退出
description: 瞭解如何管理選擇退出與隱私權
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: a174944bb8efcb67d758d4fe215674c1b8bbee13
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 80%

---

# 管理選擇退出 {#consent}

使用 [!DNL Journey Optimizer] 追蹤收件者的通訊同意，並透過管理其偏好和訂閱來瞭解他們想要如何與您的品牌互動。<!--Their preferences and subscriptions are handled through Consent management.-->

GDPR 等法規規定，您必須符合特定要求，才能使用資料主體的資訊。 此外，資料主體應能隨時修改其同意書。

**為什麼這很重要？**

* 若未遵守這些法規，您的品牌將面臨法律風險。
* 它可協助您避免傳送未經請求的通訊給您的收件者，這可能會使他們將您的訊息標示為垃圾訊息，並損害您的聲譽。

[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant){target=&quot;_blank&quot;}中有關管理隱私權和適用法規的詳細資訊。

<!--* Recipients should be able to opt-in/opt-out from receiving electronic communication through one or more channel
* Recipients expect the brand to offer preference centre capability that controls how brand should engage with them (example: channel of communication, invasive and non-invasive tracking etc). This helps to fulfil regulatory obligations and also facilitates quality engagement with recipient. 
* The third category is the capability to offer subscription to recipients (newsletter, etc)-->

## 選擇退出管理 {#opt-out-management}

為接收者提供取消訂閱來自品牌之通訊的能力為法律所規定。 進一步了解[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}中的適用法規。

因此，您必須在每封寄送給收件者的電子郵件中一律包含&#x200B;**取消訂閱連結**：
* 按一下此連結後，收件者會被導向至包含確認選擇退出按鈕的登陸頁面。
* 按一下選擇退出按鈕後，將會發出 Adobe I/O 呼叫，以使用此資訊更新設定檔資料。 [進一步瞭解此功能](#consent-service-api)。

### 新增取消訂閱連結 {#add-unsubscribe-link}

若要新增取消訂閱連結，請遵循下列步驟：

1. 建立您的取消訂閱登陸頁面。
1. 在您選擇的協力廠商系統上代管您的登陸頁面。
1. 於[!DNL Journey Optimizer][建立訊息](../../help/using/create-message.md)。

   <!--The link to your landing page should contain a static URL and the profile ID.-->

1. 選擇內容中的文字，並使用內容相關工具列插入連結。

   ![](assets/opt-out-insert-link.png)

1. 從&#x200B;**[!UICONTROL Link type]**&#x200B;下拉式清單中選取 **[!UICONTROL Unsubscription link]**。

   ![](assets/opt-out-link-type.png)

1. 在&#x200B;**[!UICONTROL Unsubscription page URL]**&#x200B;框架中，複製登陸頁面的連結。

   ![](assets/opt-out-link-url.png)

1. 按一下「**[!UICONTROL Save]**」。

1. 儲存您的內容並[發佈您的訊息](../../help/using/publish-manage-message.md)。

   >[!NOTE]
   >
   >您的協力廠商登陸頁面 URL 將包含三個參數，這些參數將用來透過 Adobe I/O 呼叫更新設定檔的偏好設定。 [在本節中瞭解更多](#consent-service-api)。

1. 透過[歷程](building-journeys/journey.md)傳送含有登陸頁面連結的訊息。

1. 收到訊息後，如果收件者按一下取消訂閱連結，就會顯示您的登陸頁面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件者按一下登陸頁面中的選擇退出按鈕 (這裡是&#x200B;**取消訂閱**&#x200B;按鈕)，則透過 [Adobe I/O 呼叫](#opt-out-api)更新設定檔資料。

   然後，選擇退出的收件者會被重新導向至確認訊息畫面，表示成功選擇退出。

   ![](assets/opt-out-confirmation-example.png)

   因此，除非再次訂閱，否則此使用者將不會收到您品牌的通訊。

若要檢查對應的設定檔選擇是否已更新，請前往 Experience Platform，並透過選取識別名稱空間和對應的識別值來存取設定檔。 請參閱[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}了解更多資訊。

![](assets/opt-out-profile-choice.png)

在 **[!UICONTROL Attributes]** 標籤中，您可以看到 **[!UICONTROL choice]** 的值已變更為 **[!UICONTROL no]**。

<!--The opt-out URL is resolved upon each recipient receiving the message. It is then personalized with the relevant encrypted parameters (profile ID, profile name, journey ID, sandbox ID, and message execution ID).-->

### 選擇退出 API 呼叫 {#opt-out-api}

當收件者按一下取消訂閱連結選擇退出後，就會呼叫 Adobe I/OAPI <!--Consent service API to capture the encrypted data and-->以更新對應的設定檔偏好設定。

此 Adobe I/OPOST 呼叫如下：

端點：cjm.adobe.io/imp/consent/preferences

查詢參數：
* **params**：包含加密的裝載
* **sig**：簽名 <!--which signature?-->
* **pid**：加密的設定檔 ID

這些參數可從傳送給收件者的取消訂閱連結取得，亦即將為指定收件者開啟您第三方登陸頁面的 URL：

![](assets/opt-out-parameters.png)

<!--QUESTION: How do you get the URL built for each recipient? Do you have to wait until each targeted recipient receives the unsubscribe link or can you deduce it in advance? Is it done automatically upon the API call or do you have to do something manually for each profile? In other words will the LP automatically include the 3 parameters or do you have to insert something manually? Still not completely clear-->

頁首需求：
* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* 授權 (來自您技術帳戶的使用者權杖) <!--How do you find this information? And other header elements?-->

請求內文：

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

<!--The Consent service /-->[!DNL Journey Optimizer] will <!--decrypt and-->use these parameters to update the corresponding profile's choice.
<!--and provide an answer back to the landing page.-->

## 按一下選擇退出 {#one-click-opt-out}

由於許多客戶都在尋找更輕鬆的取消訂閱程式，您也可以在電子郵件內容中新增一鍵式選擇退出連結。 此連結可讓您的收件者快速取消訂閱您的通訊內容，而無需重新導向至需要確認選擇退出的登錄頁面。

了解如何在[本區段](message-tracking.md#one-click-opt-out-link)中，將選擇退出連結新增至您的訊息內容。

透過[journey](building-journeys/journey.md)傳送訊息後，如果收件者按一下選擇退出連結，則會立即選擇退出其設定檔。

## 標題中的取消訂閱連結 {#unsubscribe-email}

如果收件者的電子郵件用戶端支援在電子郵件標題中顯示取消訂閱連結，則隨 [!DNL Journey Optimizer] 傳送的電子郵件會自動包含此連結。

例如，取消訂閱連結在 Gmail 中顯示如下：

![](assets/unsubscribe-email.png)

根據電子郵件用戶端，從標題按一下取消訂閱連結將產生下列其中一項影響：

* 對應的設定檔會立即退出，而此選項會在 Experience Platform 中更新。 請參閱[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}了解更多資訊。

* 其效果與從電子郵件內容按一下取消訂閱連結相同：收件者會重新導向至包含按鈕的登陸頁面，以確認選擇退出。 進一步瞭解[本章節](#opt-out-management)中的選擇退出管理。

## 推播選擇退出管理 {#push-opt-out-management}

推播收件者可以透過裝置本身取消訂閱。

例如，在下載或使用您的應用程式時，他們可以選擇停止通知。 同樣地，他們也可以透過行動裝置作業系統變更通知設定。
