---
solution: Journey Optimizer
product: journey optimizer
title: 物件等級存取控制
description: 瞭解物件層級存取控制，其可讓您定義授權，以管理對所選物件的資料存取
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: 物件，層級，存取，控制，標籤， olac，授權
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 8b0310e91e5b5c1418e8e26f4505bda45146ceba
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 17%

---

# 物件等級存取控制 {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="存取權管理標籤"
>abstract="您可以根據存取權標籤限制對物件的存取。這個方法能保護敏感的數位資產，避免未經授權的使用者存取，並確保進一步保護個人資料。**請確認僅選取您有權限使用的標籤。**"

您可以根據存取權標籤限制對物件的存取。此方法可保護敏感數位資產免受未經授權使用者的侵害，並確保進一步保護個人資料。

物件層級存取控制(OLAC)功能可讓您定義授權，以管理所選物件的資料存取：

* 歷程
* Campaign
* 範本
* 片段
* 登陸頁面
* 產品建議
* 靜態優惠收藏
* 優惠決定
* 管道設定
* IP熱身計畫


## 先決條件 {#prereq-labels}

若要能夠[建立標籤](#create-labels)，您必須屬於具有&#x200B;**[!UICONTROL 管理使用標籤]**&#x200B;許可權的角色。

若要能夠[指派標籤](#assign-labels)，您必須屬於具有&#x200B;**管理**&#x200B;許可權的角色，即[!DNL Manage journeys]、[!DNL Manage Campaigns]或[!DNL Manage decisions]。 若沒有此許可權，**[!UICONTROL 管理存取權]**&#x200B;按鈕會變成灰色。

若要了解更多關於權限的資訊，請參閱[此區段](../administration/permissions.md)。

## 建立標籤 {#create-labels}

**[!UICONTROL 標籤]**&#x200B;可讓您根據套用至該資料的使用原則來分類資料集和欄位。 **[!UICONTROL 標籤]**&#x200B;可隨時套用，讓您在控管資料的方式上有彈性。

使用標籤為使用者提供存取權，並強制執行資料治理和同意原則。 這些治理標籤可能會影響下游消耗。

您可以在[!DNL Permissions]產品中建立標籤。 如需詳細資訊，請參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html){target="_blank"}。

您也可以直接在Journey Optimizer中建立&#x200B;**[!UICONTROL 標籤]**。 若要建立標籤，請遵循下列步驟：

1. 從Adobe Journey Optimizer物件（例如新建立的&#x200B;**[!UICONTROL 促銷活動]**），按一下&#x200B;**[!UICONTROL 管理存取權]**&#x200B;按鈕。

   在Adobe Journey Optimizer中![管理存取權按鈕](assets/olac_1.png)

1. 從&#x200B;**[!UICONTROL 管理存取權]**&#x200B;視窗，按一下&#x200B;**[!UICONTROL 建立標籤]**。

   ![](assets/olac_2.png)

1. 設定您的標籤。 您必須指定：

   * **[!UICONTROL 名稱]**
   * **[!UICONTROL 易記名稱]**
   * **[!UICONTROL 說明]**

   ![標籤設定欄位](assets/olac_3.png)

1. 按一下[建立]&#x200B;**[!UICONTROL 以儲存您的]**&#x200B;標籤&#x200B;**[!UICONTROL 。]**

您新建立的&#x200B;**[!UICONTROL 標籤]**&#x200B;現在可在清單中使用。 如有需要，您可以在[!DNL Permissions]產品中修改它。

## 指派標籤 {#assign-labels}

若要將自訂或核心資料使用標籤指派給您的Journey Optimizer物件：

1. 從Adobe Journey Optimizer物件（例如新建立的&#x200B;**[!UICONTROL 促銷活動]**），按一下&#x200B;**[!UICONTROL 管理存取權]**&#x200B;按鈕。

   在Adobe Journey Optimizer中![管理存取權按鈕](assets/olac_1.png)

1. 從&#x200B;**[!UICONTROL 管理存取權]**&#x200B;視窗，選取您的自訂或核心資料使用標籤，以管理此物件的存取權。

   如需核心資料使用標籤的詳細資訊，請參閱[此頁面](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html){target="_blank"}。

   ![](assets/olac_4.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;以套用此標籤限制。

若要存取此物件，使用者的&#x200B;**[!UICONTROL 角色]**&#x200B;中必須包含特定的&#x200B;**[!UICONTROL 標籤]**。 例如，具有C1標籤的使用者將只能存取C1標籤或未標籤的物件。

如需如何將&#x200B;**[!UICONTROL 標籤]**&#x200B;指派給&#x200B;**[!UICONTROL 角色]**&#x200B;的詳細資訊，請參閱[此頁面](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role){target="_blank"}。
