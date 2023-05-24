---
solution: Journey Optimizer
product: journey optimizer
title: 物件等級存取控制
description: 瞭解對象級訪問控制，它允許您定義管理對選定對象的資料存取權限的授權
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: 對象、級別、訪問、控制、標籤、olac、授權
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 14%

---

# 物件等級存取控制 {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="物件等級存取控制"
>abstract="如果您套用任何您無權存取的標籤，則您對此物件的存取權限將被撤銷。"

>[!IMPORTANT]
>
>對象級別訪問控制的使用目前僅限於選定客戶，將在以後的版本中部署到所有環境。

對象級訪問控制(OLAC)允許您定義管理對選定對象的資料存取的授權：

* 歷程
* Campaign
* 登陸頁面
* 優惠
* 優惠集合
* Offer decisioning

其目的是保護敏感數字資產免受未經授權用戶的侵害，從而進一步保護個人資料。

在Adobe Journey Optimizer,OLAC允許您保護資料並授予對特定對象的特定訪問權限。

## 建立標籤 {#create-assign-labels}

>[!IMPORTANT]
>
>要能夠建立標籤，您必須是 **[!UICONTROL 管理使用標籤]** 權限。

**[!UICONTROL 標籤可讓您根據適用於該資料的使用原則對資料集和欄位進行分類。]****[!UICONTROL 標籤]** 可以隨時應用，在選擇如何管理資料方面提供了靈活性。

可在 [!DNL Permissions] 產品。 如需詳細資訊，請參閱[此頁面](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html)。

**[!UICONTROL 標籤]** 也可以直接在Journey Optimizer建立：

1. 從Adobe Journey Optimizer對象，這裡是新建立的 **[!UICONTROL 活動]**，按一下 **[!UICONTROL 管理訪問]** 按鈕

   ![](assets/olac_1.png)

1. 從 **[!UICONTROL 管理訪問]** 窗口，按一下 **[!UICONTROL 建立標籤]**。

   ![](assets/olac_2.png)

1. 配置標籤時，必須指定：
   * **[!UICONTROL 名稱]**
   * **[!UICONTROL 友好名稱]**
   * **[!UICONTROL 說明]**

   ![](assets/olac_3.png)

1. 按一下 **[!UICONTROL 建立]** 保存 **[!UICONTROL 標籤]**。

新建立的 **[!UICONTROL 標籤]** 清單中。 如果需要，可以在 [!DNL Permissions] 產品。

## 分配標籤 {#assign-labels}

>[!IMPORTANT]
>
>要能夠分配標籤，您必須是具有「管理」權限的角色的一部分， [!DNL Manage journeys]。 [!DNL Manage Campaigns] 或 [!DNL Manage decisions]。 如果沒有此權限， **[!UICONTROL 管理訪問]** 按鈕將變灰。

要將自定義或核心資料使用標籤分配給您的Journey Optimizer對象：

1. 從Adobe Journey Optimizer對象，這裡是新建立的 **[!UICONTROL 活動]**，按一下 **[!UICONTROL 管理訪問]** 按鈕

   ![](assets/olac_1.png)

1. 從 **[!UICONTROL 管理訪問]** 窗口，選擇自定義或核心資料使用標籤以管理對此對象的訪問。

   有關核心資料使用標籤的詳細資訊，請參閱 [此頁](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html)。

   ![](assets/olac_4.png)

1. 按一下 **[!UICONTROL 保存]** 以應用此標籤限制。

要訪問此對象，用戶需要具有 **[!UICONTROL 標籤]** 包括 **[!UICONTROL 角色]**。
例如，具有C1標籤的用戶將只能訪問已標籤或未標籤的對象的C1。

有關如何分配的詳細資訊 **[!UICONTROL 標籤]** 到 **[!UICONTROL 角色]**，請參閱 [此頁](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role)。
