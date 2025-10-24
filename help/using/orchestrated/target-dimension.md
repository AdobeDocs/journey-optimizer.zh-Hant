---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的目標維度
description: 瞭解如何將關聯式結構描述對應到客戶設定檔
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: ac80d1cec351a3029c8b2bf862275ffe7fd5c86d
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

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

➡️ [在Adobe Experience Platform檔案中進一步瞭解關聯式結構描述](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/relational#how-relational-schemas-differ-from-standard-xdm-schemas)

## 建立您的目標維度 {#targeting-dimension}

首先，將關聯式結構描述對應至客戶設定檔，以設定行銷活動協調流程。

1. 從&#x200B;**[!UICONTROL 管理]**，存取&#x200B;**[!UICONTROL 組態]**&#x200B;功能表並選取&#x200B;**[!UICONTROL Campaign Target Dimension]**。

   ![](assets/target-dimension-1.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**&#x200B;以開始建立您的&#x200B;**[!UICONTROL 目標維度]**。

1. 從下拉式清單中選擇您先前設定的[結構描述](gs-schemas.md)&#x200B;。

   雖然所有關聯式結構描述都可見，但只有與&#x200B;**設定檔**&#x200B;有直接身分關聯的結構描述才符合選取的條件。

1. 選取代表您要鎖定之實體的&#x200B;**[!UICONTROL 身分值]**。

   在此範例中，客戶設定檔連結到多個訂閱，每個訂閱在`crmID`結構描述中由唯一的`Recipient`表示。 透過設定&#x200B;**[!UICONTROL Target Dimension]**&#x200B;使用`Recipient`結構描述及其`crmID`身分，您可以在訂閱層級傳送訊息，而非傳送至主要客戶設定檔，確保每個合約或服務內容都能收到自己的個人化訊息。

   [請到 Adobe Experience Platform 文件](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition#identity)那邊，了解更多相關資訊。

   ![](assets/target-dimension-2.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;以完成設定。 請注意，一旦建立，**[!UICONTROL Target維度]**&#x200B;便無法移除或編輯。

設定&#x200B;**[!UICONTROL 目標Dimension]**&#x200B;後，繼續建立和設定您的&#x200B;**[!UICONTROL 通道設定]**，並定義對應的&#x200B;**[!UICONTROL 執行詳細資料]**。