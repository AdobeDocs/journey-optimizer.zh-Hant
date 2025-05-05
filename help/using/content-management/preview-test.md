---
title: 預覽並測試您的內容
description: 了解如何預覽並測試您的內容。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: ht
source-wordcount: '480'
ht-degree: 100%

---

# 預覽並測試您的內容 {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="檢查您的內容的呈現方式"
>abstract="定義內容後，您可以使用測試輪廓進行預覽，並根據您使用的管道檢查呈現是否正確。"

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="檢查您的內容的呈現方式"
>abstract="定義內容後，您可以進行預覽並根據您使用的頻道檢查轉譯是否正確。"

## 關於預覽和測試 {#about}

一旦定義內容，您就可以在傳送訊息之前，先預覽內容。 這個重要步驟能確保內容屬實，但內容與個人化設定中的資料也不得有誤。

您也可以將電子郵件訊息的測試傳遞寄給特定收件者或訂閱者，以便進行測試和驗證，同時檢查郵件內容在熱門桌面、行動裝置和網頁型用戶端中的轉譯內容。

所有這些動作都可以使用&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕來執行，可已從訊息的編輯內容畫面，或透過電子郵件、網頁頻道的電子郵件和網頁設計工具，存取此按鈕。

![](../email/assets/email-preview-button.png)

請注意，您必須產品設定檔案中加入&#x200B;**[!DNL Manage Simulate Content]**&#x200B;權限&#x200B;**[!DNL Content Library Manager]**。[了解更多](../administration/ootb-product-profiles.md#content-library-manager)。


>[!CAUTION]
>
>* 當預覽訊息或傳送校樣時，只會顯示出設定檔個人化資料。 根據內容資料，例如事件資訊等個人化資料，只能在歷程的內容中測試。 了解如何在[這個使用案例](../personalization/personalization-use-case.md)中測試個人化。
>
>* 針對包含多個條件變體的電子郵件來模擬或轉譯校樣時，Journey Optimizer 可能需要更多處理時間。 如果您遇到逾時或錯誤訊息，請考慮減少變體總數或簡化條件規則。 請在[此頁面](../personalization/dynamic-content.md)深入了解相關內容。


## 使用測試設定檔或範例輸入資料來進行測試 {#methods}

您可以使用以下工具，預覽並測試您的內容：

* **測試輪廓**

  使用測試輪廓來預覽您的內容、傳送電子郵件校樣，同時檢查電子郵件轉譯。 如果您已新增個人化欄位，就可以使用測試輪廓資料，檢查資料的顯示方式。如需詳細資訊，請參閱以下區段：

  ➡️ [選取測試輪廓](test-profiles.md)

  ➡️[使用測試輪廓來預覽您的內容](preview.md)

  ➡️ [傳送電子郵件校樣](proofs.md)

  ➡️[檢查電子郵件轉譯](rendering.md)

  ➡️ [預覽並校訂您的電子郵件 (影片)](#video-preview)

* **範例輸入資料**

  [!DNL Journey optimizer] 可讓您預覽電子郵件內容，還能從 CSV / JSON 檔案上傳，或是手動新增的範例輸入資料，傳送校樣，以便測試內容的不同變體。 

  系統會自動偵測您在內容中使用到的所有設定檔屬性，以便進行個人化，以上屬性可應用到測試上，即可建立多個變體。

  ➡️ [了解如何使用範例輸入資料來測試您的內容](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >此功能目前會透過公開測試版的形式，開放給所有客戶使用，只限用於電子郵件、簡訊和推播通知頻道。

## 作法影片 {#video-preview}

了解如何使用測試輪廓來測試各個收件匣裡的電子郵件轉譯，根據測試輪廓預覽您的個人化電子郵件，同時傳送校樣。

>[!VIDEO](https://video.tv.adobe.com/v/3430345?quality=12&captions=chi_hant)
