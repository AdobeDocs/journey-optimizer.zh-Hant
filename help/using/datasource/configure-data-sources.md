---
title: 設定資料來源
description: 瞭解如何設定資料來源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: 5596c851b70cc38cd117793d492a15fd4ce175ef
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 10%

---

# 設定資料來源 {#configure-data-source}

以下是主要的資料來源設定步驟：

>[!NOTE]
>
>資料來源設定一律會由&#x200B;**技術使用者**&#x200B;執行。

1. 在「管理」(ADMINISTRATION)菜單部分，選擇 **[!UICONTROL Configurations]**。 在  **[!UICONTROL Data Sources]** ，按一下 **[!UICONTROL Manage]**。 畫面隨即顯示資料來源。請參閱 [此頁](../start/user-interface.md) 的上界。

   ![](assets/journey18.png)

1. 然後，您可以將欄位組添加到內置資料源(請參見 [此頁](../datasource/adobe-experience-platform-data-source.md))或建立新的外部資料源(請參見 [此頁](../datasource/external-data-sources.md))和關聯的欄位組(請參見 [此頁](../datasource/configure-data-sources.md#define-field-groups))。

   ![](assets/journey23.png)

1. 按一下「**[!UICONTROL Save]**」。

   資料來源現在已設定完畢，且可供您在歷程中使用。

## 定義欄位組 {#define-field-groups}

欄位組是一組欄位，您可以從資料源中檢索這些欄位並在行程中使用。

對於每個資料源，可以定義多個欄位組。

例如，您可以建立一個欄位組，其中包含電話號碼、電子郵件、配置檔案的名字和地址。 然後，您就可以在旅途中使用此資料來建立條件。 例如，只有在客戶安裝了移動應用程式時，您才能決定發送推送通知。 如果為空，則可以發送電子郵件。

即使自動添加預設名稱，我們建議您為欄位組指定名稱。 實際上，欄位組名稱將對中的其他用戶可見 [!DNL Journey Optimizer]。 為欄位組指定相關名稱是最佳做法。

在行程中使用資料源欄位時，系統將檢索為該欄位組定義的所有欄位。 因此，只選擇您的行程所需的欄位是最佳做法。 這將減少您的行程中的請求延遲，從而提高效能。 請注意，以後可以在欄位組中輕鬆添加更多欄位。

使用欄位組的行程次數顯示在 **[!UICONTROL Used in]** 的子菜單。 您可以按一下 **[!UICONTROL View journeys]** 按鈕來顯示使用此欄位組的行程清單。

>[!NOTE]
>
>請注意，如果欄位組沒有欄位，則表達式編輯器中將不顯示該欄位。

![](assets/journey3bis.png)

## 欄位組生命週期 {#field-group-lifecycle}

您可以從任何草稿或即時行程中未使用的欄位組中添加或刪除欄位。

您可以添加欄位，但不能從一個或多個草稿或即時行程中使用的欄位組中刪除欄位。 這將避免重蹈覆轍。

要從一個或多個行程中使用的欄位組中刪除欄位，請執行以下步驟。 讓我們使用名為「欄位組A」的欄位組的示例。

1. 在欄位組清單中，將游標置於「欄位組A」上，然後按一下 **[!UICONTROL Duplicate]** 表徵圖。 例如，將重複欄位組命名為「欄位組B」。
1. 在「欄位組B」中，刪除不再需要的欄位。
1. 在「欄位組A」中，檢查此欄位組的使用位置。 此資訊顯示在 **[!UICONTROL Used in]** 的子菜單。
1. 開啟所有使用「欄位組A」的旅程。
1. 建立這些行程的新版本。 使用「欄位組A」編輯所有活動，然後選擇「欄位組B」。
1. 停止使用「欄位組A」的舊版本的旅程。 然後，您不應使用「欄位組A」進行任何旅程。
1. 刪除「欄位組A」，因為它不再使用。
