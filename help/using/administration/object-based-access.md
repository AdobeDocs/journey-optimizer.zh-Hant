---
solution: Journey Optimizer
product: journey optimizer
title: 物件等級存取控制
description: 瞭解物件層級存取控制，其可讓您定義授權，以管理對所選物件的資料存取
feature: Access Management
topic: Administration
role: Admin, Developer
level: Experienced
keywords: 物件，層級，存取，控制，標籤， olac，授權
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
feature_v2: id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2: []
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 1017
ht-degree: 10%

---

# 物件等級存取控制 {#object-level-access}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;使用物件層級存取控制來限制個別物件（例如歷程、行銷活動和優惠方案）的存取標籤，因此您可以將敏感內容和個人資料限制在授權的使用者之內。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="存取權管理標籤"
>abstract="您可以根據存取權標籤限制對物件的存取。 這個方法能保護敏感的數位資產，避免未經授權的使用者存取，並確保進一步保護個人資料。 **請確認僅選取您有權限使用的標籤。**"

您可以根據存取權標籤限制對物件的存取。 這個方法能保護敏感的數位資產，避免未經授權的使用者存取，並確保進一步保護個人資料。

物件層級存取控制(OLAC)功能可讓您定義授權，以管理所選物件的資料存取：

* 歷程
* 促銷活動
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

若要了解權限的詳細資訊，請參閱[本章節](../administration/permissions.md)。

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

1. 按一下[建立]**[!UICONTROL 以儲存您的**[!UICONTROL &#x200B;標籤&#x200B;]**。]**

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

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;物件層級存取控制(OLAC)可讓您將存取標籤套用至特定的Journey Optimizer物件，例如歷程、行銷活動和選件，因此只有角色包含相符標籤的使用者才能檢視這些物件或與之互動。

**意圖：**

* 直接在Journey Optimizer中或透過許可權產品建立自訂存取標籤
* 將存取權標籤指派給Journey Optimizer物件（歷程、行銷活動、優惠方案等）
* 將敏感內容限製為僅供授權使用者使用
* 瞭解建立和指派標籤所需的許可權

**字彙表：**

* **OLAC （物件層級存取控制）**：可定義授權，以管理特定Journey Optimizer物件&#x200B;*（特定產品）*&#x200B;之選取專案的資料存取
* **標籤**：套用至物件的標籤，可依使用原則加以分類，並根據角色成員資格&#x200B;*（產品特定）*&#x200B;限制存取
* **管理存取權**：受支援的Journey Optimizer物件上可用的按鈕或介面，用於建立和指派存取權標籤&#x200B;*（產品專用）*
* **核心資料使用標籤**： Adobe Experience Platform提供的預先定義標籤，與組織&#x200B;*（產品特定）*&#x200B;建立的自訂標籤相反

**護欄：**

* 建立標籤需要&#x200B;**管理使用標籤**&#x200B;許可權（先決條件）
* 指派標籤需要物件型別的&#x200B;**管理**&#x200B;許可權（例如，管理歷程、管理行銷活動或管理決定）；若無此許可權，**管理存取權**&#x200B;按鈕將會變灰（先決條件）
* OLAC標籤支援的物件：歷程、行銷活動、範本、片段、登陸頁面、優惠、靜態優惠集合、優惠決定、頻道設定、IP熱身計畫

**術語：**

* 正式名稱：物件層級存取控制 — 縮寫：OLAC — 變體：物件存取控制、物件存取管理
* 請勿混淆： OLAC （限制存取特定AJO物件，例如使用標籤的歷程和行銷活動）≠ABAC （以屬性為基礎，將標籤原則套用至結構描述欄位、資料集和平台層級的對象）
* 請勿混淆：「核心資料使用標籤」（來自Adobe Experience Platform的預建標籤）≠「自訂標籤」（組織建立的標籤）

**常見問題集：**

* **問：我可以直接在Journey Optimizer中建立標籤，而不需前往「許可權」產品嗎？**  — 是；對任何支援的物件使用「管理存取」視窗，然後按一下「建立標籤」。
* **問：哪些物件型別支援OLAC標籤？**  — 歷程、行銷活動、範本、片段、登陸頁面、優惠、靜態優惠集合、優惠決定、頻道設定和IP熱身計畫。
* **問：指派標籤給歷程需要什麼許可權？** — 「管理歷程」許可權；沒有「管理」許可權，「管理」存取按鈕會變灰。
* **問：如果使用者的角色中只有C1標籤，可以存取哪些物件？**  — 只有C1標籤或未標籤的物件。

+++
<!-- ai-accordion-version: 1 | source-hash: 4e9b2577 -->
