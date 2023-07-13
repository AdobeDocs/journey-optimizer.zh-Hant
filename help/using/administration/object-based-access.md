---
solution: Journey Optimizer
product: journey optimizer
title: 物件等級存取控制
description: 瞭解物件層級存取控制，其可讓您定義授權以管理對所選物件的資料存取
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: 物件，層級，存取，控制，標籤， olac，授權
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 15%

---

# 物件等級存取控制 {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="物件等級存取控制"
>abstract="如果您套用任何您無權存取的標籤，則您對此物件的存取權限將被撤銷。"

物件層級存取控制(OLAC)可讓您定義授權，以管理對所選物件的資料存取：

* 歷程
* Campaign
* 登陸頁面
* 優惠
* 優惠收藏
* offer decisioning

其目的在於保護敏感數位資產，使其免受未經授權使用者的侵害，進而進一步保護個人資料。

在Adobe Journey Optimizer中，OLAC可讓您保護資料並授與特定物件的特定存取權。

## 建立標籤 {#create-assign-labels}

>[!IMPORTANT]
>
>若要建立標籤，您必須屬於具有下列專案的角色： **[!UICONTROL 管理使用標籤]** 許可權。

**[!UICONTROL 標籤可讓您根據適用於該資料的使用原則對資料集和欄位進行分類。]****[!UICONTROL 標籤]** 可隨時套用，讓您靈活選擇控管資料的方式。

您可以在中建立標籤 [!DNL Permissions] 產品。 如需詳細資訊，請參閱[此頁面](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html)。

**[!UICONTROL 標籤]** 也可以直接在Journey Optimizer中建立：

1. 從Adobe Journey Optimizer物件，在這裡新建立一個 **[!UICONTROL Campaign]**，按一下 **[!UICONTROL 管理存取權]** 按鈕。

   ![](assets/olac_1.png)

1. 從 **[!UICONTROL 管理存取權]** 視窗，按一下 **[!UICONTROL 建立標籤]**.

   ![](assets/olac_2.png)

1. 設定您的標籤，您必須指定：
   * **[!UICONTROL 名稱]**
   * **[!UICONTROL 易記名稱]**
   * **[!UICONTROL 說明]**

   ![](assets/olac_3.png)

1. 按一下 **[!UICONTROL 建立]** 儲存您的 **[!UICONTROL 標籤]**.

您新建立的 **[!UICONTROL 標籤]** 現在可從清單中取得。 如有需要，您可以在下列位置修改它： [!DNL Permissions] 產品。

## 指派標籤 {#assign-labels}

>[!IMPORTANT]
>
>若要指派標籤，您必須是具有管理許可權的角色的一部分，即 [!DNL Manage journeys]， [!DNL Manage Campaigns] 或 [!DNL Manage decisions]. 若無此許可權， **[!UICONTROL 管理存取權]** 按鈕會呈現灰色。

若要將自訂或核心資料使用標籤指派給您的Journey Optimizer物件：

1. 從Adobe Journey Optimizer物件，在這裡新建立一個 **[!UICONTROL Campaign]**，按一下 **[!UICONTROL 管理存取權]** 按鈕。

   ![](assets/olac_1.png)

1. 從 **[!UICONTROL 管理存取權]** 視窗中，選取您的自訂或核心資料使用標籤，以管理此物件的存取權。

   如需核心資料使用標籤的詳細資訊，請參閱 [此頁面](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. 按一下 **[!UICONTROL 儲存]** 以套用此標籤限制。

若要存取此物件，使用者需要具備特定 **[!UICONTROL 標籤]** 包含在其中 **[!UICONTROL 角色]**.
例如，具有C1標籤的使用者將只能存取C1標籤或未標籤的物件。

如需如何指派的詳細資訊 **[!UICONTROL 標籤]** 至 **[!UICONTROL 角色]**，請參閱 [此頁面](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role).
