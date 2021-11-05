---
title: 預覽訊息並傳送校樣
description: 了解如何預覽和測試您的訊息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: f2c2a360-a4b2-4416-bbd0-e27dd014e4ac
source-git-commit: 9ef56c69e875c68bfbd9f08348bb45387f4bb32c
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 3%

---

# 預覽和測試您的訊息{#preview-and-proof}

定義訊息內容後，您就可以使用測試設定檔來預覽和測試。 如果您已插入 [個人化內容](personalization/personalize.md)，您將可以運用測試設定檔資料，檢查訊息中此內容的顯示方式。

若要偵測電子郵件內容或個人化設定中可能的錯誤，請傳送校樣至測試設定檔。 每次進行變更時都應傳送校樣，以驗證最新內容。

>[!CAUTION]
>
>您必須有可用的測試設定檔，才能預覽訊息並傳送校樣。
>
>了解如何在 [本頁](building-journeys/creating-test-profiles.md).

若要測試訊息內容，您必須：

* [選取測試設定檔](#select-test-profiles)
* [檢查訊息預覽](#preview-your-messages)

然後，您就能 [傳送校樣](#send-proofs) 至測試設定檔。

此外，還要利用 **利特穆斯** 帳戶 [!DNL Journey Optimizer] 立即預覽 **電子郵件呈現** 常見電子郵件用戶端。 然後，您可以確保您的電子郵件內容看起來很棒，並且在每個收件匣中都正常運作。 了解如何在中解鎖Litmus電子郵件預覽 [本節](#email-rendering)

>[!CAUTION]
>
>預覽訊息或傳送校樣時，只會顯示設定檔個人化資料。 根據內容資料的個人化（例如事件資訊）只能在歷程的內容中測試。 了解如何在中測試個人化 [此使用案例](personalization/personalization-use-case.md).

➡️ [了解如何在此影片中預覽、校樣和發佈您的電子郵件](#video-preview)

## 選取測試設定檔{#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="預覽和測試您的訊息"
>abstract="定義訊息內容後，您就可以使用測試設定檔來預覽和測試。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/create-messages/create-message/preview.html?lang=en#email-rendering" text="電子郵件轉譯"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/create-messages/create-message/preview.html?lang=en#preview-your-messages" text="預覽"



使用 [測試設定檔](building-journeys/creating-test-profiles.md) 來鎖定不符合已定義定位准則的其他收件者。

若要選取測試設定檔，請遵循下列步驟：

1. 在訊息介面或電子郵件設計工具中，按一下 **[!UICONTROL Show preview]** 按鈕來存取測試設定檔選取項目。

   ![](assets/email-preview-button.png)

1. 按一下 **[!UICONTROL Identity namespace]** 選項。

   ![](assets/previewselect-namespace.png)

   深入了解Adobe Experience Platform身分識別命名空間 [在本節](get-started-identity.md){target=&quot;_blank&quot;}。

   在以下範例中，我們將使用 **電子郵件** 命名空間。

1. 使用搜尋欄位來尋找命名空間，選取命名空間，然後按一下 **[!UICONTROL Select]**

   ![](assets/preview-email-namespace.png)

1. 輸入值以識別測試設定檔，然後按一下 **[!UICONTROL Find test profile]**.

   ![](assets/preview-identity-value.png)

1. 如果您在訊息中新增個人化，請新增其他設定檔，這樣您就能根據設定檔資料測試訊息的不同變體。 新增後，設定檔會列在選取欄位下。

   ![](assets/preview-profile-list.png)

   此清單會根據訊息個人化元素，顯示相關欄中每個測試設定檔的資料。

## 預覽訊息{#preview-your-messages}

一次 [測試設定檔](#select-test-profiles) ，您可以預覽訊息並檢查內容。

1. 按一下 **[!UICONTROL Preview]** 標籤來測試訊息。

1. 選取測試設定檔。 您可以檢查欄中可用的值。 使用向右/向左箭頭來瀏覽資料。

   ![](assets/preview-tab-select-profile.png)

1. 按一下 **[!UICONTROL Select data]** 表徵圖以添加或刪除列。

   ![](assets/preview-select-data.png)

   您可以在清單的結尾處看到目前訊息專屬的個人化欄位。 在此範例中，設定檔城市、名字和姓氏。 選取這些欄位，並確定這些值已填入您的測試設定檔中。

1. 在訊息預覽中，個人化元素會由選取的測試設定檔資料取代。

   例如，對於此訊息，電子郵件內容和電子郵件主旨都會個人化：

   ![](assets/preview-test-profile.png)

1. 選取其他測試設定檔，以針對訊息的每個變體預覽電子郵件呈現。

推播通知預覽：

1. 切換至 **[!UICONTROL Push]** 頻道 **[!UICONTROL Channels]** 下拉式清單 **[!UICONTROL Preview]** 螢幕。

   ![](assets/preview-select-channel.png)

1. 套用與上述步驟相同的步驟，以選取測試設定檔，並選取要預覽內容的裝置類型： **[!UICONTROL iOS]** 或 **[!UICONTROL Android]**.

   ![](assets/preview-iOS.png)

1. 在推播預覽中，測試設定檔資料會運用在訊息內容中。

   例如，對於此推播通知，標題和內文都會個人化：

   ![](assets/preview-android.png)

## 傳送校樣{#send-proofs}

校樣是特定訊息，可讓您在將訊息傳送給主要對象之前先測試訊息。 校樣的收件者負責核准訊息：轉譯、內容、個人化設定、設定。

一次 [測試設定檔](#select-test-profiles) ，您可以傳送校樣。

1. 在 **[!UICONTROL Preview]** 螢幕上，按一下 **[!UICONTROL Send proof]** 按鈕。

   ![](assets/send-proof-button.png)

1. 從 **[!UICONTROL Send proof]** 視窗中，輸入收件者的電子郵件，然後按一下 **[!UICONTROL Add]** 將校樣傳送給您自己或組織的成員。

   請注意，您最多可為校樣傳送新增10個收件者。

   ![](assets/send-proof-button_2.png)

1. 然後，選取 **測試設定檔** 將用於個人化訊息內容。

   校樣的每個收件者會收到與所選測試設定檔數目相同的訊息。 例如，如果您新增了5封收件者電子郵件，並選取10個測試設定檔，則您會傳送50封校樣訊息，而每位收件者都會收到10封。

1. 您可以視需要在校樣的主旨行新增首碼。 僅限英數字元和特殊字元，例如。 - _() [ ]，可做為主旨行的前置詞。

1. 按一下「**[!UICONTROL Send proof]**」。

   ![](assets/send-proof-select.png)

1. 回到  **[!UICONTROL Preview]** 螢幕上，按一下  **[!UICONTROL View proofs]** 按鈕，檢查狀態。

   ![](assets/send-proof-view.png)

建議在每次修改後傳送校樣至訊息內容。

>[!NOTE]
>
>在傳送至測試設定檔的校樣中，鏡像頁面的連結未啟用。 它只會在最終訊息中啟動。

## 電子郵件轉譯{#email-rendering}

您可以運用 **利特穆斯** 帳戶 [!DNL Journey Optimizer] 立即預覽 **電子郵件呈現** 常見電子郵件用戶端。

若要存取電子郵件呈現功能，您需要：

* 有Litmus賬戶
* [選取測試設定檔](#select-test-profiles)

接著，請依照下列步驟操作：

1. 在電子郵件設計工具中，按一下 **[!UICONTROL Preview]** 按鈕並選取 **[!UICONTROL Email rendering]** 標籤。

1. 按一下 **連接您的Litmus帳戶** 在右上角。

   ![](assets/email-rendering-litmus.png)

1. 輸入您的憑證並登入。

   ![](assets/email-rendering-credentials.png)

1. 按一下 **運行測試** 按鈕來產生電子郵件預覽。

1. 在熱門的案頭、行動裝置和網頁型用戶端中查看您的電子郵件內容。

   ![](assets/email-rendering-previews.png)

>[!CAUTION]
>
>連接 **利特穆斯** 帳戶 [!DNL Journey Optimizer]，您同意將測試訊息傳送至Litmus:傳送後，這些電子郵件便不再由Adobe管理。 因此，Litmus資料保留電子郵件原則會套用至這些電子郵件，包括可能包含在這些測試訊息中的個人化資料。

## 作法影片{#video-preview}

瞭解如何測試各收件匣間的電子郵件呈現、如何根據測試設定檔預覽您的個人化電子郵件、傳送校樣及發佈您的電子郵件。

>[!VIDEO](https://video.tv.adobe.com/v/334239?quality=12)
