---
title: 設定資料來源
description: 瞭解如何設定資料來源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 10%

---

# 設定資料來源 {#configure-data-source}

以下是主要的資料來源設定步驟：

>[!NOTE]
>
>資料來源設定一律會由&#x200B;**技術使用者**&#x200B;執行。

1. 在「管理」(ADMINISTRATION)菜單部分，選擇 **[!UICONTROL Configurations]**。 In the  **[!UICONTROL Data Sources]** section, click **[!UICONTROL Manage]**. 畫面隨即顯示資料來源。請參閱 [此頁](../start/user-interface.md) 的上界。

   ![](../assets/journey18.png)

1. 然後，您可以將欄位組添加到內置資料源(請參見 [此頁](../datasource/adobe-experience-platform-data-source.md))或建立新的外部資料源(請參見 [此頁](../datasource/external-data-sources.md))和關聯的欄位組(請參見 [此頁](../datasource/configure-data-sources.md#define-field-groups))。

   ![](../assets/journey23.png)

1. 按一下「**[!UICONTROL Save]**」。

   資料來源現在已設定完畢，且可供您在歷程中使用。

## Define field groups {#define-field-groups}

Field groups are sets of fields that you can retrieve from a data source and use in a journey.

對於每個資料源，可以定義多個欄位組。

For example, you can create a field group with the telephone number, the email, the first name and the address of the profile. You will then be able to use this data in your journey to create conditions. 例如，只有在配置檔案的電話號碼不為空時，您才可以決定發送SMS。 如果為空，則可以發送電子郵件。

即使自動添加預設名稱，我們建議您為欄位組指定名稱。 實際上，欄位組名稱將對中的其他用戶可見 [!DNL Journey Optimizer]。 Giving a relevant name to field groups is a best practice.

在行程中使用資料源欄位時，系統將檢索為該欄位組定義的所有欄位。 因此，只選擇您的行程所需的欄位是最佳做法。 這將減少您的行程中的請求延遲，從而提高效能。 請注意，以後可以在欄位組中輕鬆添加更多欄位。

使用欄位組的行程次數顯示在 **[!UICONTROL Used in]** 的子菜單。 You can click the **[!UICONTROL View journeys]** button to display the list of journeys using this field group.

>[!NOTE]
>
>請注意，如果欄位組沒有欄位，則表達式編輯器中將不顯示該欄位。

![](../assets/journey3bis.png)

## 欄位組生命週期 {#field-group-lifecycle}

您可以從任何草稿或即時行程中未使用的欄位組中添加或刪除欄位。

You can add but you cannot remove a field from a field group used in one or more draft or live journeys. This will avoid breaking journeys.

要從一個或多個行程中使用的欄位組中刪除欄位，請執行以下步驟。 讓我們使用名為「欄位組A」的欄位組的示例。

1. 在欄位組清單中，將游標置於「欄位組A」上，然後按一下 **[!UICONTROL Duplicate]** 表徵圖。 例如，將重複欄位組命名為「欄位組B」。
1. 在「欄位組B」中，刪除不再需要的欄位。
1. 在「欄位組A」中，檢查此欄位組的使用位置。 此資訊顯示在 **[!UICONTROL Used in]** 的子菜單。
1. Open all the journeys which use &quot;Field Group A”.
1. 建立這些行程的新版本。 使用「欄位組A」編輯所有活動，然後選擇「欄位組B」。
1. 停止使用「欄位組A」的舊版本的旅程。 然後，您不應使用「欄位組A」進行任何旅程。
1. Remove &quot;Field Group A” as is it not used anymore.
