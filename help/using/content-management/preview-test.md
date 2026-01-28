---
title: 預覽並測試您的內容
description: 了解如何預覽並測試您的內容。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: 3f363a006ed25c07f3ea5b516f5fc306b230d029
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 90%

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

一旦定義內容，您就可以在傳送訊息之前，先預覽內容。 這個重要步驟能確保內容屬實，但內容與個人化設定中的資料也不得有誤。

您也可以將電子郵件訊息的測試傳遞傳送給特定收件者或訂閱者，以進行測試和驗證，並檢查它們在熱門的案頭、行動裝置和網頁型使用者端中的轉譯。 此外，您也可以評估一般內容品質方面，例如可讀性和有效性。 [進一步瞭解內容品質驗證](brands-score.md#validate-quality)

所有這些動作都可以使用&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕來執行，可以從訊息的編輯內容畫面，或透過電子郵件、網頁頻道的電子郵件和網頁設計工具，存取此按鈕。

![](../email/assets/email-preview-button.png)

## 使用測試設定檔資料，或是範例輸入資料進行測試 {#methods}

Journey Optimizer 有提供兩種體驗，測試您的內容：

* **使用測試設定檔資料測試內容**

  使用測試設定檔，預覽內容，傳送電子郵件校樣，同時檢查電子郵件轉譯。 如果您已新增個人化欄位，就可以使用測試設定檔資料，檢查資料的顯示方式。如需詳細資訊，請參閱以下區段：

  ➡️ [選取測試設定檔](test-profiles.md)
➡️ [使用測試設定檔來預覽](preview.md)
➡️ [傳送電子郵件校樣](proofs.md)
➡️ [檢查電子郵件轉譯](rendering.md)
➡️ [預覽並校訂電子郵件（影片）](#video-preview)

* **使用範例輸入資料來測試內容變化版本**

  [!DNL Journey optimizer]可讓您使用從 CSV / JSON 檔案上傳的範例輸入資料，或是手動新增來預覽內容的不同變化版本。 

  系統會自動偵測您在內容中使用到的所有設定檔屬性，以便進行個人化，以上屬性可應用到測試上，即可建立多個變體。

  ➡️ [模擬內容變化版本](../test-approve/simulate-sample-input.md)

## 必讀

* **必要使用權限** - 您必須將&#x200B;**[!DNL Manage Simulate Content]**&#x200B;產品設定檔&#x200B;**[!DNL Content Library Manager]**&#x200B;加入權限才行。[了解更多](../administration/ootb-product-profiles.md#content-library-manager)。

  若想傳送校樣，您必須擁有&#x200B;**核准和發佈**&#x200B;權限，可應用於電子郵件相關的特定資源（行銷活動或歷程）。 此外，若想在歷程中傳送校樣，還需要&#x200B;**發佈歷程**&#x200B;權限才行。 [深入了解權限](../administration/ootb-permissions.md)。

* **使用內容資料執行個人化** - 當預覽訊息或傳送校樣時，只會顯示出設定檔個人化資料。 根據內容資料，例如事件資訊等個人化資料，只能在歷程的內容中測試。 可到[此使用案例](../personalization/personalization-use-case.md)，了解使用方法。

* **使用多重條件變因來預覽內容** - 當出現許多條件變體的電子郵件模擬，或是轉譯校樣時，Journey Optimizer 可能需要更多時間來處理資料。 如果您遇到逾時或錯誤訊息，請考慮減少變體總數或簡化條件規則。 請在[此頁面](../personalization/dynamic-content.md)深入了解相關內容。

## 作法影片 {#video-preview}

了解如何使用測試輪廓來測試各個收件匣裡的電子郵件轉譯，根據測試輪廓預覽您的個人化電子郵件，同時傳送校樣。

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
