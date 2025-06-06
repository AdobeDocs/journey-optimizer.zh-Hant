---
solution: Journey Optimizer
product: journey optimizer
title: 建立內容範本
description: 瞭解如何測試部分電子郵件內容範本的轉譯
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 01726ab6-f581-4d19-aedd-2541bc0f27c6
source-git-commit: 22a8742bf9000ed1cc8437d7ac89747276284dbf
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 4%

---

# 測試電子郵件內容範本 {#test-template}

您可以測試部分電子郵件範本的轉譯，無論是從草稿建立還是從現有內容建立。 若要執行此操作，請遵循下列步驟。

1. 透過&#x200B;**[!UICONTROL 內容管理]** > **[!UICONTROL 內容範本]**&#x200B;功能表存取內容範本清單，並選取任何電子郵件範本。

1. 按一下&#x200B;**[!UICONTROL 範本屬性]**&#x200B;中的&#x200B;**[!UICONTROL 編輯內容]**。

1. 按一下&#x200B;**[!UICONTROL 模擬內容]**&#x200B;並選取測試設定檔以檢查您的演算。 [了解更多](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

   >[!NOTE]
   >
   >[!DNL Journey optimizer]也可讓您使用從CSV / JSON檔案上傳或手動新增的範例輸入資料，透過預覽和傳送校樣來測試內容範本的不同變體。 [瞭解如何模擬內容變化](../test-approve/simulate-sample-input.md)

1. 您可以傳送校樣以測試您的內容，並在將其用於歷程或行銷活動之前，先由內部使用者核准。

   * 若要這麼做，請按一下&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;按鈕，並遵循[本節](../content-management/proofs.md)中所述的步驟。

   * 在傳送校樣之前，您必須選取要用來測試內容的[電子郵件組態](../configuration/channel-surfaces.md)。

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>測試電子郵件內容範本時目前不支援追蹤，這表示追蹤事件、UTM引數和登入頁面連結將在從範本傳送的校樣中無效。 若要測試追蹤，[在電子郵件中使用內容範本](../email/use-email-templates.md)，並使用測試設定檔或從CSV / JSON檔案上傳的範例輸入資料，或手動新增來傳送校樣。 [瞭解如何預覽和測試您的內容](../content-management/preview-test.md)
