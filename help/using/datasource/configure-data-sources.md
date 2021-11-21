---
title: 設定資料來源
description: 瞭解如何設定資料來源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 10%

---

# 設定資料來源 {#configure-data-source}

以下是主要的資料來源設定步驟：

>[!NOTE]
>
>資料來源設定一律會由&#x200B;**技術使用者**&#x200B;執行。

1. 在「管理」(ADMINISTRATION)菜單部分中，選擇 **[!UICONTROL Configurations]**. 在  **[!UICONTROL Data Sources]** ，按一下 **[!UICONTROL Manage]**. 畫面隨即顯示資料來源。請參閱 [本頁](../user-interface.md) 以取得介面的詳細資訊。

   ![](../assets/journey18.png)

1. 然後，您可以將欄位群組新增至內建的資料來源(請參閱 [本頁](../datasource/adobe-experience-platform-data-source.md))或建立新的外部資料來源(請參閱 [本頁](../datasource/external-data-sources.md))和關聯的欄位群組(請參閱 [本頁](../datasource/configure-data-sources.md#define-field-groups))。

   ![](../assets/journey23.png)

1. 按一下「**[!UICONTROL Save]**」。

   資料來源現在已設定完畢，且可供您在歷程中使用。

## 定義欄位群組 {#define-field-groups}

欄位群組是一組欄位，您可從資料來源擷取，並用於歷程中。

對於每個資料來源，您可以定義數個欄位群組。

例如，您可以建立一個欄位群組，其中包含電話號碼、電子郵件、設定檔的名字和地址。 然後，您就能在歷程中使用此資料來建立條件。 例如，您只能在設定檔的電話號碼不為空時，才可決定傳送簡訊。 如果空白，您可以傳送電子郵件。

即使自動新增預設名稱，我們仍建議您為欄位群組命名。 事實上，欄位群組名稱將會顯示給 [!DNL Journey Optimizer]. 為欄位群組命名是最佳作法。

在歷程中使用資料來源欄位時，系統會擷取為該欄位群組定義的所有欄位。 因此，只選取您歷程所需的欄位是最佳作法。 這會減少您歷程中的要求延遲，進而提升效能。 請注意，您稍後可以輕鬆在欄位群組中新增更多欄位。

使用欄位群組的歷程次數會顯示在 **[!UICONTROL Used in]** 欄位。 您可以按一下 **[!UICONTROL View journeys]** 按鈕以顯示使用此欄位群組的歷程清單。

>[!NOTE]
>
>請注意，如果欄位群組沒有欄位，則運算式編輯器中不會顯示該欄位。

![](../assets/journey3bis.png)

## 欄位群組生命週期 {#field-group-lifecycle}

您可以從任何草稿或即時歷程中未使用的欄位群組新增或移除欄位。

您可以新增欄位，但無法從一或多個草稿或即時歷程中使用的欄位群組中移除欄位。 這樣可避免中斷歷程。

若要從一或多個歷程中使用的欄位群組中刪除欄位，請遵循下列步驟。 讓我們舉一個名為「欄位群組A」的欄位群組範例。

1. 在欄位組清單中，將游標置於「欄位組A」上，然後按一下 **[!UICONTROL Duplicate]** 表徵圖。 例如，將重複的欄位群組命名為「欄位群組B」。
1. 在「欄位群組B」中，移除您不再需要的欄位。
1. 在「欄位群組A」中，檢查此欄位群組的使用位置。 此資訊會顯示在 **[!UICONTROL Used in]** 欄位。
1. 開啟使用「欄位群組A」的所有歷程。
1. 建立這些歷程的每個新版本。 使用「欄位群組A」編輯所有活動，並選取「欄位群組B」。
1. 停止使用「欄位群組A」的舊版歷程。 之後，您應該沒有使用「欄位群組A」的歷程。
1. 移除「欄位群組A」，因為它不再使用。
