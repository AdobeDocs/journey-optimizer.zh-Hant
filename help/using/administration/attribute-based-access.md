---
title: 以屬性為基礎的存取控制
description: 瞭解基於屬性的訪問控制
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 2%

---

# 以屬性為基礎的存取控制 {#attribute-based-access}

>[!IMPORTANT]
>
>當前僅對一組組織（有限可用性）使用基於屬性的訪問控制。 如果您想利用此功能，請與Adobe客戶經理聯繫。

基於屬性的訪問控制(ABAC)允許您定義管理特定團隊或用戶組資料存取的授權。 其目的是保護敏感數字資產免受未經授權用戶的侵害，從而進一步保護個人資料。

在Adobe Journey Optimizer,ABAC允許您保護資料並授予對特定欄位元素的特定訪問權限，包括體驗資料模型(XDM)架構、配置檔案屬性和段。

有關ABAC使用的術語的更詳細清單，請參閱 [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html)。

在本示例中，我們要向 **國籍** 模式欄位，以限制未授權用戶使用它。 要使此操作正常，您需要執行以下步驟：

1. 新建  **[!UICONTROL Role]** 並賦予相應的  **[!UICONTROL Label]** 供用戶能夠訪問和使用架構欄位。

1. 分配  **[!UICONTROL Label]** 到 **國籍** 模式欄位。

1. 使用  **[!UICONTROL Schema field]** 在Adobe Journey Optimizer。

請注意 **[!UICONTROL Roles]**。 **[!UICONTROL Policies]** 和 **[!UICONTROL Products]** 也可以使用基於屬性的訪問控制API訪問。 有關此的詳細資訊，請參閱此 [文檔](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html)。

## 建立角色並分配標籤 {#assign-role}

>[!IMPORTANT]
>
>在管理角色的權限之前，首先需要建立策略。 有關此內容的詳細資訊，請參閱 [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html)。

**[!UICONTROL Roles]** 是您組織內共用相同權限、標籤和沙箱的一組用戶。 屬於 **[!UICONTROL Role]** 享有該產品中的Adobe應用和服務。
您還可以建立自己的 **[!UICONTROL Roles]** 的子菜單。

現在，我們要授予選定用戶訪問 **國籍** 欄位，標籤為C2。 為此，我們需要建立 **[!UICONTROL Role]** 為特定用戶集授予標籤C2 ，允許他們使用 **國籍** 詳細資訊 **[!UICONTROL Journey]**。

1. 從 [!DNL Permissions] 產品，選擇 **[!UICONTROL Role]** 按一下 **[!UICONTROL Create role]**。 請注意，您還可以 **[!UICONTROL Label]** 內置角色。

   ![](assets/role_1.png)

1. 添加 **[!UICONTROL Name]** 和 **[!UICONTROL Description]** 到 **[!UICONTROL Role]**，此處：受限角色人口。

1. 從下拉清單中，選擇 **[!UICONTROL Sandbox]**。

   ![](assets/role_2.png)

1. 從 **[!UICONTROL Resources]** 菜單，按一下 **[!UICONTROL Adobe Experience Platform]** 開啟不同的功能。 這裡，我們選擇 **[!UICONTROL Journeys]**。

   ![](assets/role_3.png)

1. 從下拉清單中，選擇 **[!UICONTROL Permissions]** 連結到所選特徵，如 **[!UICONTROL View journeys]** 或 **[!UICONTROL Publish journeys]**。

   ![](assets/role_6.png)

1. 保存新建立的 **[!UICONTROL Role]**&#x200B;按一下 **[!UICONTROL Properties]** 以進一步配置對角色的訪問權限。

   ![](assets/role_7.png)

1. 在 **[!UICONTROL Users]** 索引標籤中，按一下 **[!UICONTROL Add users]**。

   ![](assets/role_8.png)

1. 在&#x200B;**[!UICONTROL Labels]**&#x200B;索引標籤中，選取&#x200B;**[!UICONTROL Add label]**。

   ![](assets/role_9.png)

1. 選擇 **[!UICONTROL Labels]** 要添加到您的角色，然後按一下 **[!UICONTROL Save]**。 對於本示例，我們將為用戶授予標籤C2以訪問以前受限制架構的欄位。

   ![](assets/role_4.png)

中的用戶 **受限角色人口** 角色現在可以訪問C2標籤的對象。

## 為Adobe Experience Platform中的對象分配標籤 {#assign-label}

>[!WARNING]
>
>錯誤的標籤使用可能會中斷對人員的訪問並觸發策略違規。

**[!UICONTROL Labels]** 可用於使用基於屬性的訪問控制來指定特定的特徵區域。
在此示例中，我們要限制對 **國籍** 的子菜單。 只有具有相應欄位的用戶才能訪問此欄位 **[!UICONTROL Label]** 到  **[!UICONTROL Role]**。

請注意，您還可以  **[!UICONTROL Label]** 至  **[!UICONTROL Schema]**。  **[!UICONTROL Datasets]** 和  **[!UICONTROL Segments]**。

1. 建立 **[!UICONTROL Schema]**。 有關此內容的詳細資訊，請參閱 [本文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hant)。

   ![](assets/label_1.png)

1. 在新建立的 **[!UICONTROL Schema]**，我們首先 **[!UICONTROL Demographic details]** 包含 **國籍** 的子菜單。

   ![](assets/label_2.png)

1. 從 **[!UICONTROL Labels]** 頁籤，檢查限制欄位名稱，此處 **國籍**。 然後，從右窗格菜單中，選擇 **[!UICONTROL Edit governance labels]**。

   ![](assets/label_3.png)

1. 選擇相應 **[!UICONTROL Label]**，在這種情況下， C2 — 資料不能導出到第三方。 有關可用標籤的詳細清單，請參閱 [此頁](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels)。

   ![](assets/label_4.png)

1. 如果需要，請進一步個性化您的架構，然後啟用它。 有關如何啟用架構的詳細步驟，請參閱 [頁](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile)。

您架構的欄位現在將只可見，現在只能由使用C2標籤的角色集的一部分的用戶使用。
通過應用 **[!UICONTROL Label]** 到 **[!UICONTROL Field name]**，請注意 **[!UICONTROL Label]** 將自動應用於 **國籍** 的子菜單。

![](assets/label_5.png)

## 訪問Adobe Journey Optimizer中標有標籤的對象 {#attribute-access-ajo}

在給我們的 **國籍** 新架構中的欄位名和我們的新角色，我們現在可以看到此限制在Adobe Journey Optimizer的影響。
例如，對標為C2的對象具有訪問權限的第一個用戶X將建立一個Journey，該Journey的條件針對受限制的 **[!UICONTROL Field name]**。 如果第二個用戶Y無法訪問標有C2的對象，則需要發佈「旅程」。

1. 從Adobe Journey Optimizer，首先需要配置 **[!UICONTROL Data source]** 新架構。

   ![](assets/journey_1.png)

1. 添加新 **[!UICONTROL Field group]** 新建立的 **[!UICONTROL Schema]** 內置 **[!UICONTROL Data source]**。 也可以建立新外部 **[!UICONTROLD資料源]** 關聯 **[!UICONTROL Field groups]**。

   ![](assets/journey_2.png)

1. 選擇之前建立的 **[!UICONTROL Schema]**&#x200B;按一下 **[!UICONTROL Edit]** 從 **[!UICONTROL Fields]** 的子菜單。

   ![](assets/journey_3.png)

1. 選擇 **[!UICONTROL Field name]** 你想瞄準。 在此，我們選擇受限 **國籍** 的子菜單。

   ![](assets/journey_4.png)

1. 然後，建立一個Journey，該Journey將向具有特定國籍的用戶發送電子郵件。 添加 **[!UICONTROL Event]** 然後 **[!UICONTROL Condition]**。

   ![](assets/journey_5.png)

1. 選擇受限 **國籍** 欄位以開始生成表達式。

   ![](assets/journey_6.png)

1. 編輯 **[!UICONTROL Condition]** 以特定人群為目標 **國籍** 的子菜單。

   ![](assets/journey_7.png)

1. 根據需要個性化您的旅程，在此添加 **[!UICONTROL Email]** 操作。

   ![](assets/journey_8.png)

如果User Y不具有對標籤C2對象的訪問權限，則需要使用此限制欄位訪問此行程：

* 用戶Y將無法使用受限欄位名稱，因為它將不可見。

* 用戶Y將無法在「高級」模式下編輯具有受限欄位名稱的表達式。 將出現以下錯誤 `The expression is invalid. Field is no longer available or you don't have enough permission to see it`。

* 用戶Y可以刪除表達式。

* Y用戶將無法testJourney。

* 用戶Y將無法發佈Journey。
