---
title: 以屬性為基礎的存取控制
description: 了解基於屬性的訪問控制
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 61293a2ad45d30d24e1b38d8a5df81534dc19b40
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 1%

---

# 以屬性為基礎的存取控制 {#attribute-based-access}

>[!IMPORTANT]
>
>基於屬性的訪問控制目前僅限於選定的客戶使用，並將在將來的版本中部署到所有環境。

基於屬性的訪問控制(ABAC)允許您定義授權，以管理特定團隊或用戶組的資料訪問。 其目的是保護敏感數位資產，使其免受未經授權的使用者之害，以進一步保護個人資料。

在Adobe Journey Optimizer中，ABAC可讓您保護資料，並授予特定欄位元素的特定存取權，包括Experience Data Model(XDM)結構、設定檔屬性和區段。

有關ABAC使用的術語的更詳細清單，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html).

在此範例中，我們想將標籤新增至 **國籍** 結構欄位，限制未授權的使用者使用。 為了讓此功能發揮作用，您需要執行下列步驟：

1. 建立新  **[!UICONTROL 角色]** 並指派給  **[!UICONTROL 標籤]** 供使用者存取和使用結構欄位。

1. 指派  **[!UICONTROL 標籤]** 到 **國籍** Adobe Experience Platform中的綱要欄位。

1. 使用  **[!UICONTROL 結構欄位]** 在Adobe Journey Optimizer。

請注意 **[!UICONTROL 角色]**, **[!UICONTROL 原則]** 和 **[!UICONTROL 產品]** 也可使用屬性型存取控制API來存取。 有關詳細資訊，請參閱 [檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html).

## 建立角色並指派標籤 {#assign-role}

>[!IMPORTANT]
>
>管理角色的權限之前，您首先需要建立策略。 有關詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html).

**[!UICONTROL 角色]** 是一組使用者，在您的組織內共用相同的權限、標籤和沙箱。 屬於 **[!UICONTROL 角色]** 有權使用產品中包含的Adobe應用程式和服務。
您也可以建立自己的 **[!UICONTROL 角色]** 如果您想要微調使用者對介面中特定功能或物件的存取權。

現在，我們想要將選定的使用者存取權授予 **國籍** 欄位，標籤為C2。 為此，我們需要建立新的 **[!UICONTROL 角色]** 並授予他們標籤C2，以便他們使用 **國籍** 中的詳細資料 **[!UICONTROL 歷程]**.

1. 從 [!DNL Permissions] 產品，選取 **[!UICONTROL 角色]** 按一下左窗格菜單中的 **[!UICONTROL 建立角色]**. 請注意，您也可以新增 **[!UICONTROL 標籤]** 內建角色。

   ![](assets/role_1.png)

1. 新增 **[!UICONTROL 名稱]** 和 **[!UICONTROL 說明]** 新 **[!UICONTROL 角色]**，此處：受限角色人口統計。

1. 從下拉式清單中，選取 **[!UICONTROL 沙箱]**.

   ![](assets/role_2.png)

1. 從 **[!UICONTROL 資源]** 按一下 **[!UICONTROL Adobe Experience Platform]** 來開啟不同的功能。 在此，我們選取 **[!UICONTROL 歷程]**.

   ![](assets/role_3.png)

1. 從下拉式清單中，選取 **[!UICONTROL 權限]** 連結到所選特徵，例如 **[!UICONTROL 檢視歷程]** 或 **[!UICONTROL 發佈歷程]**.

   ![](assets/role_6.png)

1. 儲存新建立的 **[!UICONTROL 角色]**，按一下 **[!UICONTROL 屬性]** 以進一步配置角色的訪問權限。

   ![](assets/role_7.png)

1. 從 **[!UICONTROL 使用者]** 按一下 **[!UICONTROL 新增使用者]**.

   ![](assets/role_8.png)

1. 從 **[!UICONTROL 標籤]** 索引標籤，選取 **[!UICONTROL 添加標籤]**.

   ![](assets/role_9.png)

1. 選取 **[!UICONTROL 標籤]** 要添加到角色中，然後按一下 **[!UICONTROL 儲存]**. 在此範例中，我們授與標籤C2，讓使用者可存取先前限制架構的欄位。

   ![](assets/role_4.png)

中的使用者 **受限角色人口** 角色現在可以存取C2標籤的物件。

## 在Adobe Experience Platform中為物件指派標籤 {#assign-label}

>[!WARNING]
>
>標籤使用不正確可能會中斷對人員的訪問，並觸發策略違規。

**[!UICONTROL 標籤]** 可使用屬性存取控制來指派特定功能區域。
在此範例中，我們想要限制 **國籍** 欄位。 此欄位將僅供具有對應之 **[!UICONTROL 標籤]** 敬  **[!UICONTROL 角色]**.

請注意，您也可以新增  **[!UICONTROL 標籤]** to  **[!UICONTROL 結構]**,  **[!UICONTROL 資料集]** 和  **[!UICONTROL 區段]**.

1. 建立 **[!UICONTROL 結構]**. 有關詳細資訊，請參閱 [本檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hant).

   ![](assets/label_1.png)

1. 在新建立的 **[!UICONTROL 結構]**，我們會先新增 **[!UICONTROL 人口統計詳細資料]** 包含的欄位群組 **國籍** 欄位。

   ![](assets/label_2.png)

1. 從 **[!UICONTROL 標籤]** 頁簽，在此處檢查限制欄位名稱 **國籍**. 然後，從右窗格菜單中，選擇 **[!UICONTROL 編輯控管標籤]**.

   ![](assets/label_3.png)

1. 選取對應的 **[!UICONTROL 標籤]**，在此情況下， C2 — 資料無法匯出至協力廠商。 如需可用標籤的詳細清單，請參閱 [本頁](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. 視需要進一步個人化您的結構，然後啟用它。 有關如何啟用架構的詳細步驟，請參閱 [頁面](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

您架構的欄位現在只會顯示，而且現在只能供C2標籤所設定角色集的一部分使用者使用。
透過套用 **[!UICONTROL 標籤]** 至 **[!UICONTROL 欄位名稱]**，請注意 **[!UICONTROL 標籤]** 會自動套用至 **國籍** 欄位。

![](assets/label_5.png)

## 存取Adobe Journey Optimizer中標示為的物件 {#attribute-access-ajo}

貼上標籤後 **國籍** 新結構和新角色中的欄位名稱，現在可以在Adobe Journey Optimizer中查看此限制的影響。
例如，具有標示為C2之物件存取權的第一個使用者X，將會建立一個包含以限制 **[!UICONTROL 欄位名稱]**. 接著，第二個使用者Y（不具備C2標籤的物件存取權）就需要發佈歷程。

1. 在Adobe Journey Optimizer中，您必須先設定 **[!UICONTROL 資料來源]** 新架構的使用者。

   ![](assets/journey_1.png)

1. 新增 **[!UICONTROL 欄位組]** 新建立 **[!UICONTROL 結構]** 內建 **[!UICONTROL 資料來源]**. 您也可以建立新的外部 **[!UICONTROLD資料來源]** 關聯 **[!UICONTROL 欄位群組]**.

   ![](assets/journey_2.png)

1. 選取您先前建立的 **[!UICONTROL 結構]**，按一下 **[!UICONTROL 編輯]** 從 **[!UICONTROL 欄位]** 類別。

   ![](assets/journey_3.png)

1. 選取 **[!UICONTROL 欄位名稱]** 您想要鎖定目標。 在此處，我們選取限制 **國籍** 欄位。

   ![](assets/journey_4.png)

1. 接著，建立歷程，此歷程會傳送電子郵件給具有特定國籍的使用者。 新增 **[!UICONTROL 事件]** 然後 **[!UICONTROL 條件]**.

   ![](assets/journey_5.png)

1. 選取受限 **國籍** 欄位，開始建立運算式。

   ![](assets/journey_6.png)

1. 編輯 **[!UICONTROL 條件]** 以限制的特定人口為目標 **國籍** 欄位。

   ![](assets/journey_7.png)

1. 視需要個人化您的歷程，此處新增 **[!UICONTROL 電子郵件]** 動作。

   ![](assets/journey_8.png)

如果無權存取標籤C2物件的使用者Y需要使用此限制欄位來存取此歷程：

* 用戶Y將無法使用受限欄位名稱，因為它將不可見。

* 在「高級」模式下，用戶Y將無法編輯具有受限欄位名稱的表達式。 會出現下列錯誤 `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* 用戶Y可以刪除表達式。

* 使用者Y將無法測試歷程。

* 使用者Y無法發佈歷程。
