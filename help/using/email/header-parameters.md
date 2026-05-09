---
solution: Journey Optimizer
product: journey optimizer
title: 設定電子郵件標頭引數
description: 瞭解如何在通道設定層級設定您的電子郵件標頭引數
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: 設定，電子郵件，設定，寄件者標題， SMTP
exl-id: e1556c25-9c79-4362-a5a9-0a46425fa8d9
source-git-commit: 384f4e4b4c3acd9f1f1d73d4b140845870b31289
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 58%

---

# 標頭參數 {#email-header}

設定新的[電子郵件通道設定](email-settings.md)時，在&#x200B;**[!UICONTROL 標頭引數]**&#x200B;區段中，輸入與該設定所傳送電子郵件型別相關的寄件者名稱和電子郵件地址。

>[!NOTE]
>
>為了增強對電子郵件設定的控制，您可以個人化標頭參數。 [了解更多](../email/surface-personalization.md#personalize-header)
>
>當[編輯電子郵件組態](../configuration/channel-surfaces.md#edit-channel-surface)時，您無法新增新的[設定檔屬性](../personalization/personalization-build-expressions.md#sources)至標頭引數。 您必須建立新的管道設定。

* **[!UICONTROL 寄件者姓名]**：寄件者姓名，例如您的品牌名稱。

* **[!UICONTROL 寄件者電子郵件前置詞]**：您想要用於通訊的電子郵件地址。

* **[!UICONTROL 回覆姓名]**：收件者在其電子郵件用戶端軟體中按一下&#x200B;**回覆**&#x200B;按鈕時將使用的名稱。

* **[!UICONTROL 回覆電子郵件]**：收件者在其電子郵件用戶端軟體中按一下&#x200B;**回覆**&#x200B;按鈕時將使用的電子郵件地址。 [了解更多](#reply-to-email)

* **[!UICONTROL 錯誤電子郵件前置詞]**：在傳送郵件幾天後，ISP 產生的所有錯誤（非同步退件）都會在此位址接收到。 此位址也會接收休假通知及質詢回應。

  如果您想要在未委派給 Adobe 的特定電子郵件地址上接收休假通知和質詢回應，您需要設定[轉寄流程](#forward-email)。 在此情況下，請確定您有手動或自動化解決方案來處理傳入此收件匣的電子郵件。

>[!NOTE]
>
>**[!UICONTROL 寄件者電子郵件前置詞]**&#x200B;與&#x200B;**[!UICONTROL 錯誤電子郵件前置詞]**&#x200B;位址使用目前選取的[委派子網域](../configuration/about-subdomain-delegation.md)來傳送電子郵件。 例如，如果委派的子網域是 *marketing.luma.com*：
>
>* 輸入 *contact* 作為&#x200B;**[!UICONTROL 寄件者電子郵件前置詞]** — 寄件者電子郵件為 *contact@marketing.luma.com*。
>* 輸入 *error* 作為&#x200B;**[!UICONTROL 錯誤電子郵件前置詞]** — 錯誤位址為 *error@marketing.luma.com*。

![](assets/preset-header.png){width="80%"}

>[!NOTE]
>
>對於&#x200B;**[!UICONTROL 來自電子郵件前置詞]**&#x200B;和&#x200B;**[!UICONTROL 錯誤電子郵件前置詞]**，值必須以字母(A-Z)開頭，並且只能包含英數字元。 您也可以使用底線`_`、點`.`和連字型大小`-`字元。

## 寄件者標頭 {#sender-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_sender_header"
>title="寄件者標頭"
>abstract="當傳送實體 (寄件者) 與製作實體 (來源) 不同時，請使用這些選擇性欄位；例如：當上層公司為下層品牌發送訊息時，或代理商為多個客戶傳送訊息時。 支援此功能的電子郵件用戶端通常會將其轉譯為「代表來源的寄件者」或顯示「透過」指標。"

某些使用案例會要求傳輸郵件的信箱與&#x200B;**來自**&#x200B;的作者不同，例如代表子公司傳送的父級組織、多個品牌的共用行銷團隊，或為多個客戶傳送的代理商。

換句話說，**寄件者**&#x200B;是郵件的作者（電子郵件的寄件者），而&#x200B;**寄件者**&#x200B;是負責傳輸郵件的代理程式（實際傳送者）。 **Sender**&#x200B;欄位適用於傳輸實體與作者不同的情況。

在此情況下，您可以使用&#x200B;**寄件者標題**&#x200B;區段中的下列欄位，設定要新增至電子郵件標題的其他&#x200B;**寄件者**&#x200B;名稱和電子郵件地址：

* **[!UICONTROL 寄件者名稱]**：當訊息與&#x200B;**寄件者**&#x200B;作者不同時，負責傳輸訊息的一方的名稱。

* **[!UICONTROL 寄件者電子郵件]**：傳送方的電子郵件地址。

![](assets/preset-sender-header.png){width="80%"}

>[!NOTE]
>
>這些欄位為選用欄位。 您可以[個人化](surface-personalization.md#personalize-header)，就像其他標頭欄位一樣。

設定&#x200B;**[!UICONTROL 寄件者名稱]**&#x200B;和&#x200B;**[!UICONTROL 寄件者電子郵件]**&#x200B;時，[!DNL Journey Optimizer]會將&#x200B;**寄件者** SMTP標頭新增至電子郵件<!--as defined in [RFC 5322](https://datatracker.ietf.org/doc/html/rfc5322#section-3.6.2){target="_blank"}-->。 支援此功能的電子郵件使用者端可能會顯示例如&#x200B;**代表From**&#x200B;的寄件者或&#x200B;**透過**&#x200B;的指標。

>[!NOTE]
>
>如果您將&#x200B;**[!UICONTROL 寄件者名稱]**&#x200B;和&#x200B;**[!UICONTROL 寄件者電子郵件]**&#x200B;保留為空白，或是解析的&#x200B;**寄件者**&#x200B;與&#x200B;**寄件者**&#x200B;相同，則不會新增&#x200B;**寄件者**&#x200B;標頭。

附註:

* **寄件者**&#x200B;地址未用於SPF、DKIM或DMARC對齊；僅執行&#x200B;**格式**&#x200B;驗證。 SPF、DKIM和DMARC繼續依賴&#x200B;**From**&#x200B;欄位。 為組態選取的[委派子網域](../configuration/about-subdomain-delegation.md)仍舊是這些檢查所使用的傳送網域。

* 如果已設定&#x200B;**寄件者**，且個人化未解析為收件者的值，則郵件不會傳遞給該收件者。

## 回覆電子郵件 {#reply-to-email}

定義&#x200B;**[!UICONTROL 回覆電子郵件]**&#x200B;地址時，只要電子郵件地址是有效、格式正確且不含任何拼寫錯誤，您就可以指定任何電子郵件地址。

用於回覆的收件匣將將收到所有回覆電子郵件，但休假通知和質詢回覆除外，這些郵件將在 **錯誤電子郵件**&#x200B;地址收到。

若要確保正確管理回覆，請遵循下列建議：

* 確保專用收件匣有足夠的接收容量，可接收使用電子郵件設定傳送的所有回覆電子郵件。 如果收件匣出現退信，您可能無法收到客戶的一些回覆。

* 處理回覆時必須牢記隱私權與合規義務，因為回覆可能包含個人識別資訊 (PII)。

* 請勿在回覆收件匣中將郵件標示為垃圾訊息，因為這會影響傳送至此地址的所有其他回覆。

此外，在定義&#x200B;**[!UICONTROL 回覆電子郵件]**&#x200B;地址時，請務必使用具有有效 MX 記錄設定的子網域，否則電子郵件設定處理將會失敗。

如果在提交電子郵件設定時發生錯誤，表示您輸入之位址的子網域尚未設定 MX 記錄。 請連絡您的管理員以設定對應的 MX 記錄，或使用其他具有有效 MX 記錄設定的位址。

>[!NOTE]
>
>如果您輸入之位址的子網域是[已完全委派給Adobe](../configuration/delegate-subdomain.md#set-up-subdomain)的網域，請聯絡您的Adobe代表。

## 轉寄電子郵件 {#forward-email}

若要將 [!DNL Journey Optimizer] 收到的委派子網域的所有電子郵件轉寄至特定電子郵件地址，請聯絡 Adobe 客戶服務部門。

>[!NOTE]
>
>如果用於&#x200B;**[!UICONTROL 回覆電子郵件]**&#x200B;地址的子網域未委派給 Adobe，則該地址無法進行轉寄。

您需要提供：

* 您選擇的轉寄電子郵件地址。 請注意，轉寄電子郵件地址網域無法與委派給 Adobe 的任何子網域相符。
* 您的沙箱名稱。
* 將使用轉寄電子郵件地址的設定名稱或子網域。
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel configuration level.-->

>[!NOTE]
>
>* 每個子網域只能有一個轉寄電子郵件地址 — 如果多個設定使用相同的子網域，則必須對所有設定使用相同的轉寄電子郵件地址。
>* 如果未啟用轉寄，則預設會捨棄直接傳送至&#x200B;**寄件者電子郵件**&#x200B;位址的電子郵件。

轉寄電子郵件地址由 Adobe 設定。 這需要 3 至 4 天的時間。

完成後，**[!UICONTROL 回覆電子郵件]**&#x200B;和&#x200B;**錯誤電子郵件**&#x200B;地址收到的所有郵件，以及傳送至&#x200B;**寄件者電子郵件**&#x200B;地址的所有電子郵件，都會轉寄至您提供的特定電子郵件地址。

