---
title: 預覽訊息並傳送校樣
description: 瞭解如何預覽和測試您的訊息
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 2%

---

# 預覽並測試您的訊息{#preview-and-proof}

![](assets/do-not-localize/badge.png)

在您的訊息內容定義完成後，您可以使用測試描述檔來預覽和測試。 如果您插入[個人化內容](personalization/personalize.md)，您將能夠利用測試配置檔案資料檢查該內容在消息中的顯示方式。

若要偵測電子郵件內容或個人化設定中的可能錯誤，請傳送校樣以測試個人檔案。 每次進行變更時，都應傳送證明，以驗證最新內容。

>[!CAUTION]
>
>您必須有測試設定檔才能預覽訊息並傳送校樣。 [了解更多](building-journeys/testing-the-journey.md#create-test-profile)。

若要測試您的訊息內容，您必須：

* [選擇測試設定檔](#select-test-profiles)
* [檢查訊息預覽](#preview-your-messages)

然後，您就可以將校樣[傳送至測試設定檔。](#send-proofs)

此外，還可將您的&#x200B;**Litmus**&#x200B;帳戶運用在[!DNL Journey Optimizer]中，在常用的電子郵件客戶端中立即預覽您的&#x200B;**電子郵件轉換**。 然後，您可以確保電子郵件內容在每個收件匣中看起來都完美無暇，而且正常運作。 瞭解如何在[本節](#email-rendering)中解除鎖定「Litmus電子郵件預覽」

## 選擇測試配置檔案{#select-test-profiles}

測試設定檔可讓您鎖定不符合已定義定位準則的其他收件者。

若要選取測試設定檔，請遵循下列步驟：

1. 在訊息介面或電子郵件設計器中，按一下&#x200B;**[!UICONTROL Preview]**&#x200B;按鈕以存取測試描述檔選擇。

   ![](assets/email-preview-button.png)

1. 按一下&#x200B;**[!UICONTROL Identity namespace]**&#x200B;選擇圖示，選取用來識別測試描述檔的命名空間。

   ![](assets/previewselect-namespace.png)

   在本節](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=en#getting-started)中進一步瞭解Adobe Experience Platform身份名稱空間[。

   在以下範例中，我們將使用&#x200B;**Email**&#x200B;命名空間。

1. 使用搜索欄位查找命名空間，選擇它並按一下&#x200B;**[!UICONTROL Select]**

   ![](assets/preview-email-namespace.png)

1. 輸入值以識別測試配置檔案，然後按一下&#x200B;**[!UICONTROL Find test profile]**。

   ![](assets/preview-identity-value.png)

1. 如果您在訊息中新增個人化，請新增其他描述檔，以便根據描述檔資料測試不同的訊息變體。 新增後，描述檔會列在選取欄位下。

   ![](assets/preview-profile-list.png)

   此清單會根據訊息個人化元素，在相關欄中顯示每個測試描述檔的資料。

## 預覽消息{#preview-your-messages}

在選取[測試描述檔](#select-test-profiles)後，您就可以預覽訊息並檢查內容。

1. 按一下&#x200B;**[!UICONTROL Preview]**&#x200B;標籤以測試您的訊息。

1. 選取測試設定檔。 您可以檢查欄中的可用值。 使用向右／向左鍵瀏覽資料。

   ![](assets/preview-tab-select-profile.png)

1. 按一下清單上方的&#x200B;**[!UICONTROL Select data]**&#x200B;表徵圖以添加或刪除列。

   ![](assets/preview-select-data.png)

   您可以在清單的結尾看到目前訊息專屬的個人化欄位。 在此範例中，描述檔城市、名字和姓氏。 選取這些欄位，並確定這些值已填入您的測試設定檔中。

1. 在消息預覽中，個性化元素被選擇的測試配置檔案資料替換。

   例如，對於此訊息，電子郵件內容和電子郵件主旨都是個人化的：

   ![](assets/preview-test-profile.png)

1. 選取其他測試設定檔，以預覽每個訊息變體的電子郵件轉譯。

針對推播通知預覽：

1. 從&#x200B;**[!UICONTROL Preview]**&#x200B;畫面左上角的&#x200B;**[!UICONTROL Channels]**&#x200B;下拉式清單切換至&#x200B;**[!UICONTROL Push]**&#x200B;頻道。

   ![](assets/preview-select-channel.png)

1. 套用與上述相同的步驟來選取測試描述檔，並選取要預覽內容的裝置類型：**[!UICONTROL iOS]**&#x200B;或&#x200B;**[!UICONTROL Android]**

   ![](assets/preview-iOS.png)

1. 在推播預覽中，測試描述檔資料會運用在訊息內容中。

   例如，對於此推播通知，標題和內文都是個人化的：

   ![](assets/preview-android.png)

## 傳送校樣{#send-proofs}

證明是特定訊息，可讓您在傳送訊息給主要觀眾之前先測試訊息。 證明的收件者負責核准訊息：演算、內容、個人化設定、設定。

在選取[測試描述檔](#select-test-profiles)後，您就可以傳送校樣。

1. 在&#x200B;**[!UICONTROL Preview]**&#x200B;畫面中，按一下&#x200B;**[!UICONTROL Send proof]**&#x200B;按鈕。

   ![](assets/send-proof-button.png)

1. 選擇將收到證明的測試配置檔案，然後按一下&#x200B;**[!UICONTROL Send proof]**。 如有需要，您可以在證明的主旨行中新增前置詞。

   ![](assets/send-proof-select.png)

1. 回到&#x200B;**[!UICONTROL Preview]**&#x200B;畫面中，按一下&#x200B;**[!UICONTROL View proofs]**&#x200B;按鈕以檢查狀態。

   ![](assets/send-proof-view.png)

在對訊息內容進行任何修改後，您必須傳送校樣。

## 電子郵件呈現{#email-rendering}

您可以將&#x200B;**Litmus**&#x200B;帳戶運用在[!DNL Journey Optimizer]中，在常用的電子郵件客戶端中立即預覽&#x200B;**電子郵件轉換**。

若要存取「電子郵件」轉換功能，您必須：

* 擁有Litmus帳戶
* [選擇測試設定檔](#select-test-profiles)

然後，請依照下列步驟進行：

1. 在「電子郵件設計器」中，按一下&#x200B;**[!UICONTROL Preview]**&#x200B;按鈕並選擇&#x200B;**[!UICONTROL Email rendering]**&#x200B;頁籤。

1. 按一下右上方區段的「連接您的Litmus帳戶&#x200B;**」。**

   ![](assets/email-rendering-litmus.png)

1. 輸入您的認證並登入。

   ![](assets/email-rendering-credentials.png)

1. 按一下「執行test **」按鈕，產生電子郵件預覽。**

1. 在熱門的案頭、行動裝置和網路用戶端中檢查您的電子郵件內容。

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>將&#x200B;**Litmus**&#x200B;帳戶與[!DNL Journey Optimizer]連接時，您同意將測試消息發送到Litmus:一旦傳送，這些電子郵件就不再由Adobe管理。 因此，Litmus資料保留電子郵件政策適用於這些電子郵件，包括可能包含在這些測試訊息中的個人化資料。

