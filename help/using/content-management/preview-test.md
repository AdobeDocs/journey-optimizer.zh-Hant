---
title: 預覽和測試您的內容
description: 瞭解如何預覽和測試您的內容。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: 03cb3298c905766bc059e82c58969a2111379345
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 28%

---

# 預覽和測試您的內容 {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="檢查您的內容的呈現方式"
>abstract="定義內容後，您可以使用測試輪廓進行預覽，並根據您使用的管道檢查呈現是否正確。"

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="檢查您的內容的呈現方式"
>abstract="定義內容後，您可以進行預覽並根據您使用的頻道檢查轉譯是否正確。"

## 關於預覽和測試 {#about}

定義內容後，您可以在傳送訊息之前預覽其內容。 這是確保正確性的重要步驟，但內容與個人化設定中也不會有錯誤。

您也可以將電子郵件訊息的測試傳遞傳送給特定收件者或訂閱者，以進行測試和驗證，並檢查它們在熱門的案頭、行動裝置和網頁型使用者端中的轉譯。

>[!CAUTION]
>
>預覽訊息或傳送校樣時，僅會顯示設定檔個人化資料。 根據內容資料（例如事件資訊）的Personalization只能在歷程的內容中測試。 瞭解如何在[此使用案例](../personalization/personalization-use-case.md)中測試個人化。

所有這些動作都可以使用&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕來執行，您可從訊息的編輯內容畫面或電子郵件與網頁通道的電子郵件與網頁設計工具存取該按鈕。

![](../email/assets/email-preview-button.png)

請注意，您需要在&#x200B;**[!DNL Content Library Manager]**&#x200B;產品設定檔中加入&#x200B;**[!DNL Manage Simulate Content]**&#x200B;許可權。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)。

## 使用測試設定檔或範例輸入資料進行測試 {#methods}

您可以使用以下工具預覽和測試您的內容：

* **測試輪廓**

  使用測試設定檔來預覽您的內容、傳送電子郵件校樣並檢查電子郵件呈現。 如果您新增了個人化欄位，可以使用測試輪廓資料檢查它們的顯示方式。

  ➡️[選取測試設定檔](test-profiles.md)

  ➡️[使用測試設定檔預覽您的內容](preview.md)

  ➡️[傳送電子郵件校樣](proofs.md)

  ➡️[檢查電子郵件轉譯](rendering.md)

  ➡️[在此影片中瞭解如何預覽和校訂您的電子郵件](#video-preview)

* **範例輸入資料**

  [!DNL Journey optimizer]可讓您使用從CSV / JSON檔案上傳或手動新增的範例輸入資料，預覽內容並傳送校樣，以測試內容的不同變體。

  系統會自動偵測您在內容中使用到的所有設定檔屬性，以便進行個人化，以上屬性可應用到測試上，即可建立多個變體。

  ➡️[瞭解如何使用範例輸入資料測試您的內容](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >此功能目前僅供所有客戶作為電子郵件、簡訊和推播通知頻道的公開測試版使用。

## 操作說明影片 {#video-preview}

瞭解如何使用測試設定檔來測試各收件匣間的電子郵件呈現、根據測試設定檔預覽您的個人化電子郵件，以及傳送校樣。

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
