---
solution: Journey Optimizer
product: journey optimizer
title: 電子郵件選擇退出管理
description: 了解如何使用電子郵件管理選擇退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 85%

---

# 電子郵件選擇退出管理 {#email-opt-out}

為了讓收件者能夠取消訂閱收件者的電子郵件通訊，您必須一律包含 **取消訂閱連結** 寄送給收件者的每封電子郵件。 [深入了解隱私權和選擇退出管理](../privacy/opt-out.md)

若要這麼做，您可以：

* 插入 **連結至外部登錄頁面** 封電子郵件，讓使用者得以取消訂閱，而無法接收您品牌的通訊。 [了解如何新增外部選擇退出連結](#opt-out-external-lp)

* 新增 **一鍵式選擇退出連結** 填入您的電子郵件內容。 此連結可讓您的收件者快速取消訂閱您的通訊內容，無需重新導向至需要確認選擇退出的登陸頁面，加速取消訂閱的流程。 [了解如何新增一鍵式選擇退出連結](#one-click-opt-out)

此外，若 **[!UICONTROL 清單 — 取消訂閱]** 選項，則隨Journey Optimizer傳送的對應電子郵件會在電子郵件標題中包含取消訂閱連結。 [進一步了解電子郵件標題中的選擇退出](#unsubscribe-header)

>[!NOTE]
>
>行銷類電子郵件務必要加入選擇退出連結，管理異動類的訊息則非必要。 訊息類別(**[!UICONTROL 行銷]** 或 **[!UICONTROL 交易]**)是在 [通道表面](../configuration/channel-surfaces.md#email-type) （即訊息預設集）層級和建立訊息時)。

## 外部選擇退出 {#opt-out-external-lp}

### 新增取消訂閱連結 {#add-unsubscribe-link}

您首先需要在訊息中加入取消訂閱連結。 請依照下列步驟執行此操作：

1. 建立您的取消訂閱登陸頁面。

1. 在選擇的協力廠商系統進行託管。

1. 在歷程中新增訊息。

1. 選擇內容中的文字，並使用內容相關工具列[插入連結](../email/message-tracking.md#insert-links)。

   ![](assets/opt-out-insert-link.png)

1. 從&#x200B;**[!UICONTROL 連結類型]**&#x200B;下拉式清單中選擇 **[!UICONTROL 外部選擇退出/取消訂閱]** 。

   ![](assets/opt-out-link-type.png)

1. 在&#x200B;**[!UICONTROL 連結]**&#x200B;欄位貼上第三方登陸頁面的連結。

   ![](assets/opt-out-link-url.png)

1. 按一下「**[!UICONTROL 儲存]**」。

### 實施選擇退出的 API 呼叫 {#opt-out-api}

要在收件者從登陸頁面提交選擇時選擇退出，您必須實施 **Subscription API** 呼叫，透過 [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;} 更新對應設定檔的偏好設定。

此 POST 呼叫如下：

端點：platform.adobe.io/journey/imp/consent/preferences

查詢參數：

* **params**：包含加密的裝載
* **sig**：簽名
* **pid**：加密的設定檔 ID

這三個參數將包括在傳送給收件者的第三方登陸頁面 URL 中：

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

透過 [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;} API 呼叫，[!DNL Journey Optimizer] 會利用這些參數更新對應設定檔的選擇。

### 傳送包含取消訂閱連結的訊息 {#send-message-unsubscribe-link}

設定好取消訂閱的登陸頁面連結並實施 API 呼叫後，您便可傳送訊息。

1. 透過[歷程](../building-journeys/journey.md)傳送包含連結的訊息。

1. 收到訊息後，如果收件者按一下取消訂閱連結，就會顯示您的登陸頁面。

   ![](assets/opt-out-lp-example.png)

1. 收件者一旦提交表單 (在此按一下登陸頁面中的&#x200B;**取消訂閱**&#x200B;按鈕)，則會透過 [API 呼叫](#opt-out-api)更新設定檔資料。

1. 然後，選擇退出的收件者會被重新導向至確認訊息畫面，表示成功選擇退出。

   ![](assets/opt-out-confirmation-example.png)

   因此，除非再次訂閱，否則此使用者將不會收到您品牌的通訊。

1. 若要檢查對應的設定檔選擇是否已更新，請前往 Experience Platform，並透過選取識別名稱空間和對應的識別值來存取設定檔。 在 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}中進一步瞭解。

   ![](assets/opt-out-profile-choice.png)

   在&#x200B;**[!UICONTROL 屬性]**&#x200B;標籤中，您可以看到&#x200B;**[!UICONTROL 選擇]**&#x200B;的值已變更為&#x200B;**[!UICONTROL 否]**。

## 一鍵選擇退出 {#one-click-opt-out}

要在電子郵件加入選擇退出連結，請遵照以下步驟。

1. [插入連結](../email/message-tracking.md#insert-links)並選擇&#x200B;**[!UICONTROL 按一下退出]**&#x200B;作為連結類型。

   ![](assets/message-tracking-opt-out.png)

1. 選擇要如何套用選擇退出：在頻道、身分或訂閱項目層級。

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL 頻道]**：選擇退出適用於未來的訊息，傳送到目前頻道的設定檔目標 (即電子郵件地址)。 如果設定檔連結數個目標，選擇退出將套用於該頻道設定檔的所有目標 (即電子郵件地址)。
   * **[!UICONTROL 識別]**：選擇退出適用於未來的訊息，傳送給目前郵件使用的特定目標 (即電子郵件地址)。
   * **[!UICONTROL 訂閱]**：選擇退出適用於未來的訊息，連結特定訂閱項目清單。 僅當目前的訊息連結訂閱項目清單時，才能選擇此選項。

1. 輸入登陸頁面 URL，一旦取消訂閱，將重新導向使用者。 此頁僅用於確認選擇退出成功。

   >[!NOTE]
   >
   >如果在頻道介面層級啟用 **List-Unsubscribe** 選項，當使用者按一下電子郵件標頭的取消訂閱連結時，也將使用此 URL。 [了解更多](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   您可以個人化連結。 進一步瞭解[本章節](../personalization/personalization-syntax.md)的個人化 URL。

1. 儲存您的變更。

經由[歷程](../building-journeys/journey.md)傳送您的訊息後，如果收件者按一下選擇退出的連結，則會立即選擇退出其設定檔。

## 電子郵件標頭的取消訂閱連結 {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="在電子郵件標題新增取消訂閱連結"
>abstract="啟用 List-Unsubscribe 向電子郵件標題新增取消訂閱連結。 若要設定取消訂閱 URL，請在電子郵件內容插入一鍵式選擇退出連結。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=zh-Hant#one-click-opt-out" text="一鍵選擇退出"

如果在頻道介面層級啟用 [List-Unsubscribe 選項](../configuration/channel-surfaces.md#list-unsubscribe)，透過[!DNL Journey Optimizer]傳送的相應電子郵件將在電子郵件標頭包含取消訂閱連結。

例如，取消訂閱連結在 Gmail 中顯示如下：

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>若要在電子郵件標題中顯示取消訂閱連結，收件者的電子郵件用戶端必須支援此功能。

取消訂閱地址是預設的&#x200B;**[!UICONTROL Mailto (取消訂閱)]**&#x200B;地址顯示在相應的頻道介面。 [了解更多](../configuration/channel-surfaces.md#list-unsubscribe)。

若要設定個人化取消訂閱 URL，請在電子郵件內容中插入一鍵退出連結，然後輸入您選擇的 URL。 [了解更多](#one-click-opt-out)

根據電子郵件用戶端，在標題按一下取消訂閱連結將產生下列其中一項影響：

* 取消訂閱請求將傳送到預設取消訂閱位址。

* 收件人將被導向在訊息中新增退出連結時指定的登陸頁面 URL。

   >[!NOTE]
   >
   >如果您未在訊息內容中新增一鍵退出連結，則不會顯示登陸頁面。

* 對應的設定檔會立即退出，而此選項會在 Experience Platform 中更新。 在 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}中進一步瞭解 。
