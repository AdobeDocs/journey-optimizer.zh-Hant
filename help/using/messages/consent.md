---
title: 管理選擇退出
description: 瞭解如何管理選擇退出與隱私權
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 5d1dc2d1711ba43b8270423acb1a5ca0ab862230
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 52%

---

# 管理同意 {#consent}

使用 [!DNL Journey Optimizer] 追蹤收件者的通訊同意，並透過管理其偏好和訂閱來瞭解他們想要如何與您的品牌互動。

GDPR 等法規規定，您必須符合特定要求，才能使用資料主體的資訊。 此外，資料主體應能隨時修改其同意書。

**為什麼這很重要？**

* 若未遵守這些法規，您的品牌將面臨法律風險。
* 它可協助您避免傳送未經請求的通訊給您的收件者，這可能會使他們將您的訊息標示為垃圾訊息，並損害您的聲譽。

在 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant){target=&quot;_blank&quot;} 中進一步瞭解隱私權管理和相關法規。

>[!NOTE]
>
>在 [!DNL Journey Optimizer]，同意由Experience Platform處理 [同意架構](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}。 預設情況下，「同意」欄位的值為空，並被視為接受通信的同意。 您可以在載入到列出的一個可能值時修改此預設值 [這裡](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}。

## 電子郵件選擇退出管理 {#opt-out-management}

法律規定必須讓收件者提供能夠取消訂閱來自品牌的通訊。 進一步了解 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=zh-Hant){target=&quot;_blank&quot;} 中的適用法規。

因此，您必須在每封寄送給收件者的電子郵件中一律包含&#x200B;**取消訂閱連結**：

* 按一下此連結後，收件人將被引導至登錄頁以確認退出。
* 在確認其選擇後，將使用此資訊更新配置檔案的資料。

### 外部選擇退出 {#opt-out-external-lp}

為此，您可以將指向外部登錄頁的連結插入電子郵件中，以便用戶可以取消訂閱從您的品牌接收通信。

#### 新增取消訂閱連結 {#add-unsubscribe-link}

您首先需要在消息中添加取消訂閱連結。 為此，請執行以下步驟：

1. 生成您自己的未訂閱登錄頁。

1. 在選擇的協力廠商系統進行託管。

1. 於[!DNL Journey Optimizer][建立訊息](create-message.md)。

1. 選擇內容中的文本， [插入連結](message-tracking.md#insert-links) 使用上下文工具欄。

   ![](assets/opt-out-insert-link.png)

1. 從&#x200B;**[!UICONTROL Link type]**&#x200B;下拉式清單中選取 **[!UICONTROL External Opt-out/Unsubscription]**。

   ![](assets/opt-out-link-type.png)

1. 在 **[!UICONTROL Link]** 欄位，貼上指向第三方登錄頁的連結。

   ![](assets/opt-out-link-url.png)

1. 按一下「**[!UICONTROL Save]**」。

1. 儲存您的內容並[發佈您的訊息](publish-manage-message.md)。

#### 實現API調用以選擇退出 {#opt-out-api}

要在收件人從登錄頁提交其選擇時選擇退出，您必須實施 **訂閱API調用** 通過Adobe I/O更新相應配置檔案的首選項。

此 Adobe I/OPOST 呼叫如下：

端點：platform.adobe.io/journey/imp/consent/preferences

查詢參數：

* **params**：包含加密的裝載
* **sig**：簽名
* **pid**：加密的設定檔 ID

這三個參數將包括在發送給您的收件人的第三方登錄頁URL中：

![](assets/opt-out-parameters.png)

頁首需求：

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* 授權 (來自您技術帳戶的使用者權杖)

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

[!DNL Journey Optimizer] 將使用這些參數通過Adobe I/O調用更新相應配置檔案的選擇。

#### 使用取消訂閱連結發送郵件 {#send-message-unsubscribe-link}

配置到登錄頁的取消訂閱連結並實現API調用後，您的消息就可以發送了。

1. 通過 [旅程](../building-journeys/journey.md)。

1. 收到訊息後，如果收件者按一下取消訂閱連結，就會顯示您的登陸頁面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件人提交表單(此處，按 **取消訂閱** 按鈕)，通過 [Adobe I/O呼叫](#opt-out-api)。

1. 然後，選擇退出的收件者會被重新導向至確認訊息畫面，表示成功選擇退出。

   ![](assets/opt-out-confirmation-example.png)

   因此，除非再次訂閱，否則此使用者將不會收到您品牌的通訊。

1. 若要檢查對應的設定檔選擇是否已更新，請前往 Experience Platform，並透過選取識別名稱空間和對應的識別值來存取設定檔。 在 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}中進一步瞭解。

   ![](assets/opt-out-profile-choice.png)

   在 **[!UICONTROL Attributes]** 標籤中，您可以看到 **[!UICONTROL choice]** 的值已變更為 **[!UICONTROL no]**。

### 一鍵選擇退出 {#one-click-opt-out}

由於許多客戶都在尋找更輕鬆的取消訂閱流程，您也可以在電子郵件內容中加入一鍵選擇退出的連結。 此連結將使您的收件人能夠快速取消訂閱您的通信，而無需重定向到需要確認其選擇的登錄頁，從而加快取消訂閱過程。

要在電子郵件中添加選擇退出連結，請執行以下步驟。

1. [插入連結](message-tracking.md#insert-links) 選擇 **[!UICONTROL One click Opt-out]** 作為連結的類型。

   ![](assets/message-tracking-opt-out.png)

1. 選擇要如何應用選擇退出：在通道、標識或訂閱級別。

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**:選擇退出適用於將來發送到當前渠道的配置檔案目標（即電子郵件地址）的郵件。 如果幾個目標與一個配置檔案關聯，則選擇退出將應用於該渠道配置檔案中的所有目標（即電子郵件地址）。
   * **[!UICONTROL Identity]**:選擇退出適用於將來發送給當前郵件使用的特定目標（即電子郵件地址）的郵件。
   * **[!UICONTROL Subscription]**:選擇退出適用於與特定訂閱清單關聯的將來消息。 僅當當前消息與訂閱清單關聯時，才能選擇此選項。

1. 輸入登錄頁的URL，一旦取消訂閱，將重定向用戶。 此頁僅用於確認選擇退出成功。

   ![](assets/message-tracking-opt-out-confirmation.png)

   您可以個性化連結。 瞭解有關中的個性化URL的詳細資訊 [此部分](../personalization/personalization-syntax.md)。

1. 儲存您的變更。

一旦經由[歷程](../building-journeys/journey.md)傳送您的訊息後，如果收件者按一下選擇退出的連結，則會立即選擇退出其設定檔。

### 取消訂閱消息標頭中的連結 {#unsubscribe-email}

如果收件者的電子郵件用戶端支援在電子郵件標題中顯示取消訂閱連結，則隨 [!DNL Journey Optimizer] 傳送的電子郵件會自動包含此連結。

例如，取消訂閱連結在 Gmail 中顯示如下：

![](assets/unsubscribe-email.png)

根據電子郵件用戶端，從標題按一下取消訂閱連結將產生下列其中一項影響：

* 對應的設定檔會立即退出，而此選項會在 Experience Platform 中更新。 在 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}中進一步瞭解 。

* 其效果與從電子郵件內容按一下取消訂閱連結相同：收件者會重新導向至包含按鈕的登陸頁面，以確認選擇退出。 進一步瞭解[本章節](#opt-out-management)中的選擇退出管理。

## 推播選擇退出管理 {#push-opt-out-management}

推播收件者可以透過裝置本身取消訂閱。

例如，在下載或使用您的應用程式時，他們可以選擇停止通知。 同樣地，他們也可以透過行動裝置作業系統變更通知設定。
