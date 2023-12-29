---
solution: Journey Optimizer
product: journey optimizer
title: 管理使用者和角色
description: 瞭解如何管理使用者和角色
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: 產品，設定檔，沙箱
source-git-commit: be372f8f80d304067748d539fb8e210df6280721
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 4%

---

# 管理使用者和角色 {#manage-permissions}

>[!IMPORTANT]
>
> 以下詳述的每個程式只能由 **[!UICONTROL 產品]** 或 **[!UICONTROL 系統]** 管理員。

**[!UICONTROL 角色]** 請參閱共用相同許可權和沙箱的使用者集合。 這些角色可讓您輕鬆管理組織內不同使用者群組的存取和許可權。

使用 [!DNL Journey Optimizer] 產品，您可從一系列既有的產品中選擇 **[!UICONTROL 角色]**，每個都擁有不同等級的許可權，可指派給您的使用者。 有關可用的 **[!UICONTROL 角色]**，請參閱此 [頁面](ootb-product-profiles.md).

當使用者屬於 **[!UICONTROL 角色]**&#x200B;時，他們會被授予產品中所包含Adobe應用程式和服務的存取權。

如果預先存在的角色不符合您組織的特定需求，您也可以建立自訂 **[!UICONTROL 角色]** 微調介面中特定功能或物件的存取許可權。 如此一來，您便可確保每位使用者僅能存取有效執行其工作所需的資源和工具。

## 指派角色 {#assigning-role}

您可以選擇指派現成可用的或自訂的 **[!UICONTROL 角色]** 給您的使用者。

每個具有指派許可權的現成可用角色清單可在以下連結中找到： [內建角色](ootb-product-profiles.md) 區段。

若要指派 **[!UICONTROL 角色]**：

1. 若要在中指派角色給使用者 [!DNL Permissions] 產品，導覽至 **[!UICONTROL 角色]** 標籤並選取所需的角色。

   ![](assets/do-not-localize/access_control_2.png)

1. 從 **[!UICONTROL 使用者]** 標籤，按一下 **[!UICONTROL 新增使用者]**.

   ![](assets/do-not-localize/access_control_3.png)

1. 輸入使用者的名稱或電子郵件地址，或從清單中選取使用者，然後按一下 **[!UICONTROL 儲存]**.

   如果使用者先前不是在 [!DNL Admin Console]，請參閱 [新增使用者檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html).

   ![](assets/do-not-localize/access_control_4.png)

接著，您的使用者應會收到一封電子郵件，並重新導向至您的執行個體。

如需使用者管理的詳細資訊，請參閱 [存取控制檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hant).

存取執行個體時，您的使用者將會看到特定檢視，具體取決於中的指派許可權 **[!UICONTROL 角色]**. 如果使用者沒有功能的正確存取權，便會顯示下列訊息：

`You don't have permission to access this feature. Permission needed: XX.`

## 編輯現有角色 {#edit-product-profile}

針對現成可用或自訂 **[!UICONTROL 角色]**，您隨時可以決定新增或刪除許可權。

在此範例中，我們要新增 **[!UICONTROL 許可權]** 與 **[!UICONTROL 歷程]** 指派給歷程檢視器之使用者的資源 **[!UICONTROL 角色]**. 之後，使用者就可以發佈歷程。

請注意，如果您修改現成可用的或自訂的 **[!UICONTROL 角色]**，它將會影響指派給此專案的每個使用者 **[!UICONTROL 角色]**.

1. 若要在中指派角色給使用者 [!DNL Permissions] 產品，導覽至 **[!UICONTROL 角色]** 標籤並選取所需的角色，這裡是歷程檢視器 **[!UICONTROL 角色]**.
   ![](assets/do-not-localize/access_control_5.png)

1. 從您的 **[!UICONTROL 角色]** 儀表板，按一下 **[!UICONTROL 編輯]**.

   ![](assets/do-not-localize/access_control_6.png)

1. 此 **[!UICONTROL 資源]** 功能表會顯示套用至「 」的資源清單 **[!UICONTROL Experience Cloud — 平台支援的應用程式]** 產品。 拖放資源以指派許可權。

   從 **[!UICONTROL 歷程]** 資源下拉式清單，我們在這裡選擇發佈歷程 **[!UICONTROL 許可權]**.

   ![](assets/do-not-localize/access_control_14.png)

1. 如有需要，在 **[!UICONTROL 包含的許可權專案]**，按一下旁邊的X圖示，為您的角色移除許可權或資源。

1. 完成後，按一下 **[!UICONTROL 儲存]**.

如有需要，您也可以建立具有特定許可權的新角色。 有關詳細資訊，請參閱 [建立新角色](#create-product-profile).

## 建立新角色 {#create-product-profile}

[!DNL Journey Optimizer] 可讓您建立自己的 **[!UICONTROL 角色]** 並將一組許可權和沙箱指派給您的使用者。 替換為 **[!UICONTROL 角色]**，您可以授權或拒絕存取介面中的特定功能或物件。

有關如何建立和管理沙箱的詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hant){target="_blank"}.

在此範例中，我們將建立名為的角色 **Journeys唯讀** 其中我們將授與歷程功能的唯讀許可權。 使用者將只能存取和檢視歷程，而無法存取其他功能，例如 **[!DNL  Decision management]** 在 [!DNL Journey Optimizer].

若要建立我們的 **Journeys唯讀** **[!UICONTROL 角色]**：

1. 若要在中指派角色給使用者 [!DNL Permissions] 產品，導覽至 **[!UICONTROL 角色]** 標籤並按一下 **[!UICONTROL 建立角色]**.

   ![](assets/do-not-localize/access_control_9.png)

1. 新增 **[!UICONTROL 名稱]** 和 **[!UICONTROL 說明]** 新增 **[!UICONTROL 角色]**. 然後，按一下 **[!UICONTROL 確認]**.

   ![](assets/do-not-localize/access_control_10.png)

1. 從 **[!UICONTROL Sandbox]** resource下拉式清單，選擇要指派給您的 **[!UICONTROL 角色]**. [進一步瞭解 sandbox](sandboxes.md)。

   ![](assets/do-not-localize/access_control_13.png)

1. 在不同的資源之間選取，例如 **[!DNL Journeys]**， **[!DNL Segments]** 或 **[!DNL Decision management]** 可用位置 [!DNL Journey Optimizer] 列於左側功能表中。

   我們在這裡選取 **[!UICONTROL 歷程]** 資源。

   ![](assets/do-not-localize/access_control_11.png)

1. 從 **[!UICONTROL 歷程]** 從下拉式清單中選取要指派給您的使用者的許可權 **[!UICONTROL 角色]**.

   我們在這裡選取 **[!DNL View journeys]**， **[!DNL View journeys report]**  和 **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. 完成後，按一下 **[!UICONTROL 儲存]**.

您的 **[!UICONTROL 角色]** 現在已建立並設定。 您現在需要將其指派給使用者。

有關角色建立與管理的詳細資訊，請參閱 [Admin Console檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html).
