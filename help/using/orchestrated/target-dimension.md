---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的目標維度
description: 瞭解如何將關聯式結構描述對應到客戶設定檔
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---


# 設定目標維度 {#configuration}

透過&#x200B;**[!UICONTROL 協調的行銷活動]**，您可以運用Adobe Experience Platform的關聯式結構描述功能，在實體層級設計並傳遞目標通訊。 Experience Platform使用結構描述，以一致且可重複使用的方式說明資料結構。 將資料擷取至Experience Platform時，會根據XDM結構描述進行架構。

雖然&#x200B;**[!UICONTROL 協調的行銷活動]**&#x200B;的區段主要在關聯式結構描述上運作，但實際的訊息傳送一律發生在&#x200B;**設定檔**&#x200B;層級。

設定鎖定目標時，您可定義兩個關鍵面向：

* **可定位的結構描述**

  您可以指定適合定位的關聯式結構描述。 預設會使用名為`Recipient`的結構描述，但您可以設定替代方案，例如`Visitors`、`Customers`等。

  >[!IMPORTANT]
  >
  > 目標結構描述必須與:1結構描述有1`Profile`關係。 例如，您無法使用`Purchases`作為目標結構描述，因為它通常代表一對多關係。

* **設定檔連結**

  系統必須瞭解目標結構描述如何對應到`Profile`結構描述。 這是透過共用身分欄位來達成，該欄位存在於目標結構描述和`Profile`結構描述中，並且已設定為身分名稱空間。

## 建立您的目標維度 {#targeting-dimension}

首先，將關聯式結構描述對應至客戶設定檔，以設定行銷活動協調流程。

1. 從&#x200B;**[!UICONTROL 管理]**，存取&#x200B;**[!UICONTROL 組態]**&#x200B;功能表並選取&#x200B;**[!UICONTROL Campaign Target Dimension]**。

   ![](assets/target-dimension-1.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**&#x200B;以開始建立您的&#x200B;**[!UICONTROL 目標維度]**。

1. 從下拉式清單中選擇您先前設定的[結構描述](gs-schemas.md)&#x200B;。

   雖然所有關聯式結構描述都可見，但只有與&#x200B;**設定檔**&#x200B;有直接身分關聯的結構描述才符合選取的條件。

1. 選取代表您要鎖定之實體的&#x200B;**[!UICONTROL 身分值]**。

   在此範例中，客戶設定檔連結到多個訂閱，每個訂閱在`crmID`結構描述中由唯一的`Recipient`表示。 透過設定&#x200B;**[!UICONTROL Target Dimension]**&#x200B;使用`Recipient`結構描述及其`crmID`身分，您可以在訂閱層級傳送訊息，而非傳送至主要客戶設定檔，確保每個合約或服務內容都能收到自己的個人化訊息。

   [請到 Adobe Experience Platform 文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/schema/composition#identity)那邊，了解更多相關資訊。

   ![](assets/target-dimension-2.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;以完成設定。 請注意，一旦建立，**[!UICONTROL Target維度]**&#x200B;便無法移除或編輯。

設定&#x200B;**[!UICONTROL 目標Dimension]**&#x200B;後，繼續建立和設定您的&#x200B;**[!UICONTROL 通道設定]**，並定義對應的&#x200B;**[!UICONTROL 執行詳細資料]**。

## 設定您的頻道設定 {#channel-configuration}

設定&#x200B;**[!UICONTROL 目標Dimension]**&#x200B;後，您需要設定電子郵件或簡訊&#x200B;**[!UICONTROL 頻道設定]**，並定義適當的&#x200B;**[!UICONTROL 執行詳細資料]**。 這可讓您定義：

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
