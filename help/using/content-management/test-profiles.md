---
title: 選取測試輪廓
description: 瞭解如何選取測試設定檔以預覽和測試內容。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: c51e4089-7f51-437d-a5ed-de10bab46cf8
source-git-commit: 95a6d032808bc735a27a98dcb61efefa93cf5047
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 16%

---

# 選取測試輪廓 {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="使用測試設定檔檢查您的內容"
>abstract="使用測試設定檔預覽和測試您的內容。 若您已新增個人化欄位，便能使用測試設定檔資料確認其顯示方式。"

測試設定檔是不符合已定義定位准則的其他收件者。 [瞭解如何建立測試設定檔](../audience/creating-test-profiles.md)

使用測試設定檔測試內容之前，您必須先選取設定檔。 要執行此操作，請依照下列步驟執行：

1. 從訊息的編輯內容畫面或電子郵件Designer中，按一下&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕，然後選取&#x200B;**[!UICONTROL 模擬內容]**。

1. 按一下&#x200B;**[!UICONTROL 管理測試設定檔]**&#x200B;按鈕，然後按一下&#x200B;**[!UICONTROL 身分識別名稱空間]**&#x200B;選取圖示，選取要用來識別測試設定檔的名稱空間。 [進一步瞭解Adobe Experience Platform身分識別名稱空間](../audience/get-started-identity.md)。

   在下列範例中，我們使用&#x200B;**電子郵件**&#x200B;名稱空間。

   ![](../email/assets/previewselect-namespace.png)

1. 使用搜尋欄位來尋找名稱空間，選取並按一下&#x200B;**[!UICONTROL 選取]**

   ![](../email/assets/preview-email-namespace.png)

1. 在&#x200B;**[!UICONTROL 身分值]**&#x200B;欄位中，輸入值（此處為電子郵件地址）以識別測試設定檔，然後按一下&#x200B;**[!UICONTROL 新增設定檔]**。

   <!--![](assets/preview-identity-value.png)-->

1. 如果您將個人化新增至訊息，請新增其他設定檔，以便您根據設定檔資料測試訊息的不同變體。 新增後，設定檔會列在選取的欄位下。

   ![](../email/assets/preview-profile-list.png)

   此清單會根據訊息個人化元素，在相關欄中顯示每個測試設定檔的資料。

>[!NOTE]
>
>除了測試設定檔之外，[!DNL Journey optimizer]也可讓您使用從CSV / JSON檔案上傳或手動新增的範例輸入資料，透過預覽和傳送校樣來測試內容的不同變體。 [瞭解如何模擬內容變化](../test-approve/simulate-sample-input.md)
