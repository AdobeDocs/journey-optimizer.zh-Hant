---
solution: Journey Optimizer
product: journey optimizer
title: 設定您的頻道設定
description: 瞭解如何設定您的頻道設定
version: Campaign Orchestration
source-git-commit: 0b92d0e806c47b0d87ba53b7c7f1d56ee4453abb
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 設定您的頻道設定 {#channel-configuration}

設定[目標Dimension](target-dimension.md)後，您需要設定&#x200B;**[!UICONTROL 通道設定]**&#x200B;並定義適當的&#x200B;**[!UICONTROL 執行詳細資料]**。 這可讓您定義：

* **郵件傳遞的層級**：例如，每個收件者傳送一封郵件，例如每個個人傳送一封電子郵件。

* **執行地址**：用於傳送的特定連絡人欄位，例如電子郵件地址或電話號碼。

若要設定通道組態：

1. 從建立和設定您的&#x200B;**[!UICONTROL 頻道設定]**&#x200B;開始。

   您也可以更新現有的&#x200B;**[!UICONTROL 頻道設定]**。

   ➡️ [請依照此頁面中詳述的步驟操作](../email/surface-personalization.md)

1. 從&#x200B;**[!UICONTROL 通道設定]**&#x200B;的&#x200B;**[!UICONTROL 執行詳細資料]**&#x200B;區段，存取&#x200B;**[!UICONTROL 協調的行銷活動]**&#x200B;標籤。

   ![](assets/target-dimension-3.png)

1. 按一下&#x200B;**[!UICONTROL 已啟用]**，使其與協調的行銷活動相容。

1. 選擇您的傳送方式：

   * **[!UICONTROL 目標Dimension]**：傳送給主要實體，例如，收件者。

   * **[!UICONTROL 目標+次要Dimension]**：使用主要和次要實體來傳送，例如，收件者+合約。

1. 從下拉式清單中選取您先前建立的[目標Dimension](#targeting-dimension)。

   ![](assets/target-dimension-4.png)

1. 如果您選取&#x200B;**[!UICONTROL Target +次要Dimension]**&#x200B;作為傳遞方法，請選擇&#x200B;**[!UICONTROL 次要Dimension]**&#x200B;來定義訊息傳遞的內容。

1. 在&#x200B;**[!UICONTROL 執行地址]**&#x200B;區段下，選擇應該使用哪個&#x200B;**[!UICONTROL Source]**&#x200B;來擷取傳遞地址，例如電子郵件地址或電話號碼：

   * **[!UICONTROL 設定檔]**：如果傳遞地址（例如電子郵件）直接儲存在主要客戶設定檔中，請選取此選項。

     在向主要客戶傳送訊息（而非特定的關聯實體）時非常有用。

   * **[!UICONTROL 目標Dimension]**：如果傳遞地址儲存在主要實體（例如收件者）中，請選擇此專案。

     當每個收件者都有自己的傳遞地址（例如不同的電子郵件或電話號碼）時，這非常有用。

   * **[!UICONTROL 次要Dimension]**：使用&#x200B;**[!UICONTROL Target +次要Dimension]**&#x200B;作為傳遞方式時，請選取您先前設定的相關&#x200B;**[!UICONTROL 次要Dimension]**。

     例如，如果次要維度代表預訂或訂閱，則可以從該層級取得執行地址，例如電子郵件。 若在預訂或訂閱服務時，設定檔使用不同的聯絡人詳細資訊，則此功能會很有用。

1. 從&#x200B;**[!UICONTROL 傳遞地址]**&#x200B;欄位中，按一下![編輯圖示](assets/do-not-localize/edit.svg)以選擇要用於訊息傳遞的特定欄位。

   ![](assets/target-dimension-4.png)

1. 設定之後，按一下&#x200B;**[!UICONTROL 提交]**。

您的頻道現在已準備好搭配&#x200B;**協調的行銷活動**&#x200B;使用，將會根據選取的目標維度傳遞訊息。
