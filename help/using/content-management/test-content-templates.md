---
solution: Journey Optimizer
product: journey optimizer
title: 測試內容範本
description: 瞭解如何測試部分電子郵件內容範本的轉譯
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 4%

---

# 測試電子郵件內容範本 {#test-template}

您可以測試部分電子郵件範本的轉譯，無論是從草稿建立還是從現有內容建立。 若要執行此操作，請遵循下列步驟。

1. 透過存取內容範本清單 **[!UICONTROL 內容管理]** > **[!UICONTROL 內容範本]** 功能表並選取任何電子郵件範本。

1. 按一下 **[!UICONTROL 編輯內容]** 從 **[!UICONTROL 範本屬性]**.

1. 按一下 **[!UICONTROL 模擬內容]** 並選取測試設定檔以檢查您的演算。 [了解更多](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. 您可以傳送校樣以測試您的內容，並在將其用於歷程或行銷活動之前，先由內部使用者核准。

   * 若要這麼做，請按一下 **[!UICONTROL 傳送證明]** 按鈕並遵循中所述的步驟 [本節](../content-management/proofs.md).

   * 在傳送校樣之前，您必須選取 [電子郵件表面](../configuration/channel-surfaces.md) 這些將用於測試您的內容。

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>測試電子郵件內容範本時目前不支援追蹤，這表示追蹤事件、UTM引數和登入頁面連結將在從範本傳送的校樣中無效。 若要測試追蹤， [使用內容範本](../email/use-email-templates.md) 在電子郵件和 [傳送證明](../content-management/preview-test.md#send-proofs).
