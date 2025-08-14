---
solution: Journey Optimizer
product: journey optimizer
title: 設定電子郵件標頭引數
description: 瞭解如何在通道設定層級設定您的電子郵件標頭引數
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: 設定、電子郵件、設定
exl-id: e1556c25-9c79-4362-a5a9-0a46425fa8d9
source-git-commit: 1b4ab451ed9e2315ffe4850c6ab4b8ad20223ac3
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 90%

---

# 標頭參數 {#email-header}

設定新的[電子郵件通道設定](email-settings.md)時，在&#x200B;**[!UICONTROL 標頭引數]**&#x200B;區段中，輸入與該設定所傳送電子郵件型別相關的寄件者名稱和電子郵件地址。

>[!NOTE]
>
>為了增強對電子郵件設定的控制，您可以個人化標頭參數。[了解更多](../email/surface-personalization.md#personalize-header)

* **[!UICONTROL 寄件者姓名]**：寄件者姓名，例如您的品牌名稱。
* **[!UICONTROL 寄件者電子郵件前置詞]**：您想要用於通訊的電子郵件地址。
* **[!UICONTROL 回覆姓名]**：收件者在其電子郵件用戶端軟體中按一下&#x200B;**回覆**&#x200B;按鈕時將使用的名稱。
* **[!UICONTROL 回覆電子郵件]**：收件者在其電子郵件用戶端軟體中按一下&#x200B;**回覆**&#x200B;按鈕時將使用的電子郵件地址。[了解更多](#reply-to-email)
* **[!UICONTROL 錯誤電子郵件前置詞]**：在傳送郵件幾天後，ISP 產生的所有錯誤（非同步退件）都會在此位址接收到。此位址也會接收休假通知及質詢回應。

  如果您想要在未委派給 Adobe 的特定電子郵件地址上接收休假通知和質詢回應，您需要設定[轉寄流程](#forward-email)。在此情況下，請確定您有手動或自動化解決方案來處理傳入此收件匣的電子郵件。

>[!NOTE]
>
>**[!UICONTROL 寄件者電子郵件前置詞]**&#x200B;與&#x200B;**[!UICONTROL 錯誤電子郵件前置詞]**&#x200B;位址使用目前選取的[委派子網域](../configuration/about-subdomain-delegation.md)來傳送電子郵件。例如，如果委派的子網域是 *marketing.luma.com*：
>* 輸入 *contact* 作為&#x200B;**[!UICONTROL 寄件者電子郵件前置詞]** — 寄件者電子郵件為 *contact@marketing.luma.com*。
>* 輸入 *error* 作為&#x200B;**[!UICONTROL 錯誤電子郵件前置詞]** — 錯誤位址為 *error@marketing.luma.com*。

![](assets/preset-header.png){width="80%"}

>[!NOTE]
>
>位址必須以字母 (A-Z) 開頭，並且只能包含英數字元。您也可以使用底線 `_`、點 `.` 和連字號 `-` 字元。

## 回覆電子郵件 {#reply-to-email}

定義&#x200B;**[!UICONTROL 回覆電子郵件]**&#x200B;地址時，只要電子郵件地址是有效、格式正確且不含任何拼寫錯誤，您就可以指定任何電子郵件地址。

用於回覆的收件匣將將收到所有回覆電子郵件，但休假通知和質詢回覆除外，這些郵件將在 **錯誤電子郵件**&#x200B;地址收到。

若要確保正確管理回覆，請遵循下列建議：

* 確保專用收件匣有足夠的接收容量，可接收使用電子郵件設定傳送的所有回覆電子郵件。如果收件匣出現退信，您可能無法收到客戶的一些回覆。

* 處理回覆時必須牢記隱私權與合規義務，因為回覆可能包含個人識別資訊 (PII)。

* 請勿在回覆收件匣中將郵件標示為垃圾訊息，因為這會影響傳送至此地址的所有其他回覆。

此外，在定義&#x200B;**[!UICONTROL 回覆電子郵件]**&#x200B;地址時，請務必使用具有有效 MX 記錄設定的子網域，否則電子郵件設定處理將會失敗。

如果在提交電子郵件設定時發生錯誤，表示您輸入之位址的子網域尚未設定 MX 記錄。請連絡您的管理員以設定對應的 MX 記錄，或使用其他具有有效 MX 記錄設定的位址。

>[!NOTE]
>
>如果您輸入之位址的子網域是[已完全委派給Adobe](../configuration/delegate-subdomain.md#full-subdomain-delegation)的網域，請聯絡您的Adobe代表。

## 轉寄電子郵件 {#forward-email}

若要將 [!DNL Journey Optimizer] 收到的委派子網域的所有電子郵件轉寄至特定電子郵件地址，請聯絡 Adobe 客戶服務部門。

>[!NOTE]
>
>如果用於&#x200B;**[!UICONTROL 回覆電子郵件]**&#x200B;地址的子網域未委派給 Adobe，則該地址無法進行轉寄。

您需要提供：

* 您選擇的轉寄電子郵件地址。請注意，轉寄電子郵件地址網域無法與委派給 Adobe 的任何子網域相符。
* 您的沙箱名稱。
* 將使用轉寄電子郵件地址的設定名稱或子網域。
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel configuration level.-->

>[!NOTE]
>
>每個子網域只能有一個轉寄電子郵件地址。因此，如果多個設定使用相同的子網域，則必須對所有設定使用相同的轉寄電子郵件地址。

轉寄電子郵件地址由 Adobe 設定。這需要 3 至 4 天的時間。

完成後，**[!UICONTROL 回覆電子郵件]**&#x200B;和&#x200B;**錯誤電子郵件**&#x200B;地址收到的所有郵件，以及傳送至&#x200B;**寄件者電子郵件**&#x200B;地址的所有電子郵件，都會轉寄至您提供的特定電子郵件地址。

>[!NOTE]
>
>根據預設，如果未啟用轉寄，則會捨棄直接傳送至&#x200B;**寄件者**&#x200B;地址的電子郵件。
