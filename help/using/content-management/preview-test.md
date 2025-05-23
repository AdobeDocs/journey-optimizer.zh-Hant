---
title: 預覽並測試您的內容
description: 了解如何預覽並測試您的內容。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 57%

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

您也可以將電子郵件訊息的測試傳遞寄給特定收件者或訂閱者，以便進行測試和驗證，同時檢查郵件內容在熱門桌面、行動裝置和網頁型用戶端中的轉譯內容。

所有這些動作都可以使用&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕來執行，可已從訊息的編輯內容畫面，或透過電子郵件、網頁頻道的電子郵件和網頁設計工具，存取此按鈕。

![](../email/assets/email-preview-button.png)

## 使用測試設定檔資料或範例輸入資料進行測試 {#methods}

Journey Optimizer提供兩種體驗來測試您的內容：

* **使用測試設定檔資料測試內容**

  您可以使用測試設定檔來預覽內容、傳送電子郵件校樣並檢查電子郵件呈現。 如果您已新增個人化欄位，您可以使用測試設定檔資料檢查這些欄位的顯示方式。 如需詳細資訊，請參閱以下區段：

  ➡️ [選取測試設定檔](test-profiles.md)
➡️ [使用測試設定檔預覽](preview.md)
➡️ [傳送電子郵件校樣](proofs.md)
➡️ [檢查電子郵件轉譯](rendering.md)
➡️ [預覽並校訂您的電子郵件（影片）](#video-preview)

* **使用範例輸入資料測試內容變異**

  [!DNL Journey optimizer]可讓您使用從CSV / JSON檔案上傳或手動新增的範例輸入資料，預覽和傳送您內容不同變異的校樣。

  系統會自動偵測您在內容中使用到的所有設定檔屬性，以便進行個人化，以上屬性可應用到測試上，即可建立多個變體。

  ➡️ [模擬內容變化](../test-approve/simulate-sample-input.md)

## 必讀

* **必要的許可權** — 您需要在&#x200B;**[!DNL Content Library Manager]**&#x200B;產品設定檔中包含&#x200B;**[!DNL Manage Simulate Content]**&#x200B;許可權。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)。

  若要傳送校樣，您必須對與電子郵件關聯的特定資源（行銷活動或歷程）具有&#x200B;**核准和發佈**&#x200B;許可權。 此外，若要在歷程中傳送校樣，還需要&#x200B;**發佈歷程**&#x200B;許可權。 [進一步瞭解許可權](../administration/ootb-permissions.md)。

* **包含內容資料的Personalization** — 預覽訊息或傳送校樣時，只會顯示設定檔個人化資料。 根據內容資料，例如事件資訊等個人化資料，只能在歷程的內容中測試。 在[此使用案例](../personalization/personalization-use-case.md)中瞭解如何進行。

* **預覽具有多個條件變體的內容** — 針對包含多個條件變體的電子郵件模擬或呈現校樣時，Journey Optimizer可能需要更多處理時間。 如果您遇到逾時或錯誤訊息，請考慮減少變體總數或簡化條件規則。 請在[此頁面](../personalization/dynamic-content.md)深入了解相關內容。

## 作法影片 {#video-preview}

了解如何使用測試輪廓來測試各個收件匣裡的電子郵件轉譯，根據測試輪廓預覽您的個人化電子郵件，同時傳送校樣。

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
