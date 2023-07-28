---
title: 測試並傳送直接郵件訊息
description: 瞭解如何在Journey Optimizer中測試和傳送直接郵件訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
source-git-commit: 246205d13c1dd30b4f4769780f69e5acdd388e66
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 2%

---

# 測試並傳送直接郵件訊息 {#direct-mail-test-send}

## 預覽解壓縮檔案 {#preview-dm}

定義解壓縮檔案的內容後，您就可以使用測試設定檔來預覽。 如果您已插入個人化內容，您可以使用測試設定檔資料檢查此內容在訊息中的顯示方式。

1. 在擷取檔案內容設定畫面中，按一下 **[!UICONTROL 模擬內容]**.

   ![](assets/direct-mail-simulate-button.png){width="800" align="center"}

1. 按一下 **[!UICONTROL 管理測試設定檔]** 以新增測試設定檔。

1. 使用尋找您的測試設定檔 **[!UICONTROL 身分名稱空間]** 和 **[!UICONTROL 身分值]** 欄位。 然後，按一下 **[!UICONTROL 新增設定檔]**.

   ![](assets/direct-mail-test-profile.png){width="800" align="center"}

1. 選取測試設定檔後，您可以關閉 **[!UICONTROL 新增測試設定檔]** 視窗。

1. 從 **預覽和測試** 視窗中，測試設定檔資料會新增至擷取檔案內容，讓您預覽檔案的呈現方式。

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

一旦檔案內容準備好要傳送，請關閉模擬畫面，然後按一下 **[!UICONTROL 檢閱以啟動]** 按鈕。

## 驗證並啟用直接郵件行銷活動 {#dm-validate}

在啟用直接郵件行銷活動之前，請確定已正確設定行銷活動和擷取檔案。 若要這麼做，請檢查編輯器上半區段的警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

* **警告** 請參閱建議和最佳實務。 例如，如果SMS訊息為空，則會顯示警告訊息。

* **錯誤** 防止您發佈行銷活動，前提是行銷活動尚未解決。 例如，當主旨行遺失時，錯誤訊息會警告您。

![](assets/direct-mail-review.png){width="800" align="center"}

當您的直接郵件行銷活動準備就緒時，請按一下 **[!UICONTROL 啟動]** 按鈕。 行銷活動開始時，擷取檔案會自動產生，並匯出至中指定的伺服器。 [檔案路由設定](../direct-mail/direct-mail-configuration.md).

傳送後，您可以在行銷活動報表中測量直接郵件行銷活動的影響。 如需報告的詳細資訊，請參閱本區段。
