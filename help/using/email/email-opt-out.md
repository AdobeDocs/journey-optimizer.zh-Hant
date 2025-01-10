---
solution: Journey Optimizer
product: journey optimizer
title: 電子郵件選擇退出管理
description: 瞭解如何透過電子郵件管理選擇退出
feature: Email Design, Privacy
topic: Content Management
role: User
level: Intermediate
keywords: 選擇退出，電子郵件，連結，取消訂閱
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: fb14db58f9facac87e83a85e8f163ea31732a374
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 27%

---

# 電子郵件選擇退出管理 {#email-opt-out}

從歷程或行銷活動傳送訊息時，您必須一律確保客戶可取消訂閱未來的通訊。 取消訂閱後，設定檔會自動從未來行銷訊息的對象中移除。  [進一步瞭解隱私權與選擇退出管理](../privacy/opt-out.md)

>[!NOTE]
>
>您的所有行銷訊息都必須包含選擇退出連結。 異動訊息不需要此屬性。 訊息類別 — **[!UICONTROL 行銷]**&#x200B;或&#x200B;**[!UICONTROL 異動]** — 是在[頻道設定](../configuration/channel-surfaces.md#email-type)層級及建立訊息時定義。

若要在電子郵件內容中插入取消訂閱連結，您可以：

* 在電子郵件標題中新增一鍵取消訂閱URL。 頻道設定層級的&#x200B;**[!UICONTROL 啟用List-Unsubscribe]**&#x200B;選項會將選擇退出連結新增至電子郵件標題。 [進一步瞭解電子郵件標頭中的選擇退出](#unsubscribe-header)

* 為您的電子郵件啟用&#x200B;**一鍵退出連結**。  [瞭解如何新增一鍵退出連結](#one-click-opt-out)

* 插入登陸頁面&#x200B;**的**&#x200B;連結。 [瞭解如何新增選擇退出的登陸頁面](#opt-out-external-lp)


## 一步選擇退出 {#opt-out-one-step}

### 電子郵件標頭中的一鍵取消訂閱 URL {#unsubscribe-header}

<!--Do not modify - Legal Review Done -->

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="將取消訂閱 URL 新增至電子郵件標頭"
>abstract="啟用清單取消訂閱，將取消訂閱 URL 新增至電子郵件標頭。若要在訊息中設定取消訂閱 URL，請在電子郵件內容中插入一鍵式選擇退出連結。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/channels/email/email-opt-out#one-click-opt-out" text="一鍵式選擇退出電子郵件內容"

一鍵式清單取消訂閱URL是電子郵件寄件者資訊旁邊顯示的取消訂閱連結或按鈕，可讓收件者只要按一下即可立即選擇退出您的郵寄清單。 在Adobe Journey Optimizer中，當&#x200B;**啟用List-Unsubscribe**&#x200B;選項切換時，電子郵件標題預設會包含收件者可用於取消訂閱郵寄清單的郵件和/或URL。

[啟用List-Unsubscribe](email-settings.md#list-unsubscribe)切換必須在頻道設定層級啟動，以便使用此設定的電子郵件在電子郵件標題中包含一鍵取消訂閱URL。

>[!NOTE]
>
>若要在電子郵件標題中顯示一鍵式取消訂閱URL，收件者的電子郵件使用者端必須支援此功能。


例如，按一下取消訂閱URL會在Gmail中顯示取消訂閱連結，如下所示：

![](assets/unsubscribe-header.png)


透過Adobe Journey Optimizer，您可以透過自動產生的一鍵式取消訂閱URL和電子郵件標題中的mailto地址來設定電子郵件組態設定，或在您的電子郵件內文中包含一鍵式選擇退出URL：當收件者按一下一鍵式選擇退出連結時，收件者的取消訂閱請求會據此處理。

<!--
>[!AVAILABILITY]
>
>One-click Unsubscribe URL Header will be available in Adobe Journey Optimizer starting June 3, 2024.
>
-->

根據電子郵件使用者端及[電子郵件組態取消訂閱設定](email-settings.md#list-unsubscribe)，按一下電子郵件標頭中的取消訂閱連結可能會產生下列影響：

* 當您啟用&#x200B;**Mailto （取消訂閱）**&#x200B;功能時，系統會根據您建立的子網域，將取消訂閱請求傳送至預設的取消訂閱位址。
* 當您啟用&#x200B;**一鍵取消訂閱URL**&#x200B;功能時，或如果您在電子郵件內文內容中插入取消訂閱URL，當收件者按一下一鍵取消訂閱URL （根據同意的設定）時，收件者會直接在頻道層級或ID層級（視您建立的子網域而定）選擇退出。

在這兩種情況下，收件者的對應設定檔會立即退出，而此選項會在Experience Platform中更新。 在[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hant){target="_blank"}中進一步瞭解。

若您已針對List Unsubscribe標頭切換到&#x200B;**[!UICONTROL 啟用List-Unsubscribe]**&#x200B;選項，我們建議您啟用這兩種方法 — **Mailto （取消訂閱）**&#x200B;和&#x200B;**一鍵取消訂閱URL**。 並非所有電子郵件使用者端都支援HTTP方法。 透過提供Mailto清單 — 取消訂閱功能，您可選取替代方案，更能保護您的寄件者信譽，且您的所有收件者都能夠存取取消訂閱功能。 [了解更多](email-settings.md#list-unsubscribe)


### 一鍵式選擇退出電子郵件內容 {#one-click-opt-out}

若要設定個人化取消訂閱URL，請在電子郵件內容中插入一鍵退出連結，然後輸入您選擇的URL，如下所述：

1. 存取您的電子郵件內容，並[插入連結](../email/message-tracking.md#insert-links)。
1. 選取&#x200B;**[!UICONTROL 按一下退出]**&#x200B;作為連結型別。

   ![](assets/message-tracking-opt-out.png)

1. 輸入登陸頁面的URL，一旦取消訂閱，就會將使用者重新導向。 此頁用於確認選擇退出成功。

   >[!NOTE]
   >
   >如果您在[通道組態層級](email-settings.md#list-unsubscribe)啟用&#x200B;**[!UICONTROL List-Unsubscribe]**&#x200B;選項，並且取消核取預設的一鍵選擇退出URL選項，則當使用者按一下電子郵件標頭的取消訂閱連結時，會使用此URL。 [了解更多](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   您可以個人化連結。 進一步瞭解[本章節](../personalization/personalization-syntax.md)的個人化 URL。

1. 選擇要如何套用選擇退出：在頻道、身分識別或訂閱項目層級。

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL 頻道]**：選擇退出適用於未來的訊息，傳送到目前頻道的輪廓目標 (即電子郵件地址)。 如果輪廓連結數個目標，選擇退出將套用於該頻道輪廓的所有目標 (即電子郵件地址)。
   * **[!UICONTROL 身分識別]**：選擇退出適用於未來的訊息，傳送給目前郵件使用的特定目標 (即電子郵件地址)。
     <!--* **[!UICONTROL Subscription]**: The opt-out applies to future messages associated with a specific subscription list. This option can only be selected if the current message is associated with a subscription list.-->

1. 儲存您的變更。


## 兩步驟選擇退出 {#opt-out-external-lp}

標準的選擇退出機制取決於兩個步驟：訂閱者按一下電子郵件中的選擇退出連結，然後被重新導向至選擇退出登陸頁面，以確認取消訂閱。

若要實作此取消訂閱模式，您必須建立並發佈選擇退出登陸頁面，並在電子郵件訊息中新增取消訂閱連結，連同登陸頁面的連結。 這些步驟概述如下。


### 先決條件 {#prereq-lp}

若要設定兩步驟選擇退出機制，您必須建立自己的取消訂閱登入頁面。 第一個登入頁面將會從您的訊息連結，而且必須包含行動號召按鈕。 當使用者按一下按鈕時，應顯示確認訊息。

瞭解如何在Adobe Journey Optimizer中建立登陸頁面，以便在[此頁面](../landing-pages/lp-use-cases.md#opt-out)中管理取消訂閱。

您也可以使用外部登入頁面。 在此情況下，請設定API以在收件者取消訂閱時將資訊傳送至Adobe Journey Optimizer。

+++ 瞭解如何實作選擇退出API呼叫

要在收件者從登陸頁面提交選擇時選擇退出，您必須實施&#x200B;**訂閱API呼叫** (透過[Adobe Developer](https://developer.adobe.com){target="_blank"})以更新對應設定檔的偏好設定。

此 POST 呼叫如下：

端點：https://platform.adobe.io/journey/imp/consent/preferences

查詢參數：

* **params**：包含加密的裝載
* **pid**：加密的輪廓 ID

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

[!DNL Journey Optimizer]會透過[Adobe Developer](https://developer.adobe.com){target="_blank"} API呼叫，使用這些引數更新對應設定檔的選擇。

+++


### 新增取消訂閱連結 {#add-unsubscribe-link}

您首先需要在訊息中加入取消訂閱連結。 請依照下列步驟執行此操作：

1. 使用內容工具列建立訊息並[插入連結](../email/message-tracking.md#insert-links)。

   ![](assets/opt-out-insert-link.png)

1. 從&#x200B;**[!UICONTROL 型別]**&#x200B;下拉式清單中選取&#x200B;**[!UICONTROL 登陸頁面]**，然後在&#x200B;**[!UICONTROL 登陸頁面]**&#x200B;欄位中選取您的選擇退出登陸頁面。

   如果您使用外部登陸頁面，請從&#x200B;**[!UICONTROL 型別]**&#x200B;下拉式清單中選取&#x200B;**[!UICONTROL 外部選擇退出/取消訂閱]**。

   ![](assets/opt-out-link-type.png)

   在&#x200B;**[!UICONTROL 連結]**&#x200B;欄位貼上第三方登陸頁面的連結。

   ![](assets/opt-out-link-url.png)

1. 按一下「**[!UICONTROL 儲存]**」。


### 傳送包含取消訂閱連結的訊息 {#send-message-unsubscribe-link}

設定好取消訂閱的登陸頁面連結後，您就可以建立並傳送訊息。

1. 使用取消訂閱連結設定您的訊息，並將其傳送給訂閱者。

1. 收到訊息後，如果收件者按一下取消訂閱連結，就會顯示您的登陸頁面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件者提交表單 — 在此按一下登陸頁面中的&#x200B;**[!UICONTROL 取消訂閱]**&#x200B;按鈕 — 會透過API呼叫更新設定檔資料。

1. 然後，選擇退出的收件者會被重新導向至確認訊息畫面，表示成功選擇退出。

   ![](assets/opt-out-confirmation-example.png)

   因此，除非再次訂閱，否則此使用者將不會收到您品牌的通訊。

1. 若要檢查對應的輪廓選擇是否已更新，請前往 Experience Platform，並透過選取身分識別名稱空間和對應的身分識別值來存取輪廓。 在[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hant){target="_blank"}中進一步瞭解。

   ![](assets/opt-out-profile-choice.png)

   在&#x200B;**[!UICONTROL 屬性]**&#x200B;標籤中，您可以看到&#x200B;**[!UICONTROL 選擇]**&#x200B;的值已變更為&#x200B;**[!UICONTROL 否]**。

