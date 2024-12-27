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
ht-degree: 7%

---

# 管理使用者和角色 {#manage-permissions}

>[!IMPORTANT]
>
> 以下詳述的每個程式只能由&#x200B;**[!UICONTROL 產品]**&#x200B;或&#x200B;**[!UICONTROL 系統]**&#x200B;管理員執行。

**[!UICONTROL 角色]**&#x200B;是指共用相同許可權和沙箱的使用者集合。 這些角色可讓您輕鬆管理組織內不同使用者群組的存取和許可權。

透過[!DNL Journey Optimizer]產品，您能夠從預先存在的&#x200B;**[!UICONTROL 角色]**&#x200B;範圍中進行選擇，每個角色都具有不同等級的許可權，以便指派給您的使用者。 如需可用&#x200B;**[!UICONTROL 角色]**&#x200B;的詳細資訊，請參閱此[頁面](ootb-product-profiles.md)。

當使用者屬於&#x200B;**[!UICONTROL Role]**&#x200B;時，他們會被授予產品內含之Adobe應用程式和服務的存取權。

如果預先存在的角色不符合您組織的特定需求，您也可以建立自訂&#x200B;**[!UICONTROL 角色]**，以微調介面中特定功能或物件的存取許可權。 如此一來，您便可確保每位使用者僅能存取有效執行其工作所需的資源和工具。

## 指派角色 {#assigning-role}

您可以選擇指派現成可用的或自訂的&#x200B;**[!UICONTROL 角色]**&#x200B;給使用者。

您可以在[內建角色](ootb-product-profiles.md)區段中找到每個具有指派許可權的現成角色清單。

若要指派&#x200B;**[!UICONTROL 角色]**：

1. 若要將角色指派給[!DNL Permissions]產品中的使用者，請瀏覽至&#x200B;**[!UICONTROL 角色]**&#x200B;索引標籤，然後選取所要的角色。

   ![](assets/do-not-localize/access_control_2.png)

1. 在&#x200B;**[!UICONTROL 使用者]**&#x200B;標籤中，按一下&#x200B;**[!UICONTROL 新增使用者]**。

   ![](assets/do-not-localize/access_control_3.png)

1. 輸入您的使用者名稱或電子郵件地址，或從清單中選擇使用者，然後按一下&#x200B;**[!UICONTROL 儲存]**。

   如果使用者先前未在[!DNL Admin Console]中建立，請參閱[新增使用者檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html)。

   ![](assets/do-not-localize/access_control_4.png)

接著，使用者應會收到一封電子郵件，並重新導向至您的執行個體。

如需使用者管理的詳細資訊，請參閱[存取控制檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hant)。

存取執行個體時，您的使用者將會看到特定檢視，視&#x200B;**[!UICONTROL 角色]**&#x200B;中的指派許可權而定。 如果使用者沒有功能的正確存取權，便會顯示下列訊息：

`You don't have permission to access this feature. Permission needed: XX.`

## 編輯現有角色 {#edit-product-profile}

針對現成或自訂&#x200B;**[!UICONTROL 角色]**，您可以隨時決定新增或刪除許可權。

在此範例中，我們要為指派給歷程檢視器&#x200B;**[!UICONTROL 角色]**&#x200B;的使用者，新增與&#x200B;**[!UICONTROL 歷程]**&#x200B;資源相關的&#x200B;**[!UICONTROL 許可權]**。 之後，使用者就可以發佈歷程。

請注意，如果您修改現成可用的或自訂的&#x200B;**[!UICONTROL 角色]**，將會影響指派給此&#x200B;**[!UICONTROL 角色]**&#x200B;的每個使用者。

1. 若要在[!DNL Permissions]產品中將角色指派給使用者，請瀏覽至&#x200B;**[!UICONTROL 角色]**&#x200B;索引標籤，並選取所需的角色，這裡是歷程檢視器&#x200B;**[!UICONTROL 角色]**。
   ![](assets/do-not-localize/access_control_5.png)

1. 從您的&#x200B;**[!UICONTROL 角色]**&#x200B;儀表板，按一下&#x200B;**[!UICONTROL 編輯]**。

   ![](assets/do-not-localize/access_control_6.png)

1. **[!UICONTROL 資源]**&#x200B;功能表會顯示套用至&#x200B;**[!UICONTROL Experience Cloud- Platform支援的應用程式]**&#x200B;產品的資源清單。 拖放資源以指派許可權。

   從&#x200B;**[!UICONTROL 歷程]**&#x200B;資源下拉式清單中，我們在這裡選擇Publish歷程&#x200B;**[!UICONTROL 許可權]**。

   ![](assets/do-not-localize/access_control_14.png)

1. 如有需要，請在&#x200B;**[!UICONTROL 包含的許可權專案]**&#x200B;下，按一下角色旁的X圖示，移除許可權或資源。

1. 完成時，按一下&#x200B;**[!UICONTROL 儲存]**。

如有需要，您也可以建立具有特定許可權的新角色。 如需詳細資訊，請參閱[建立新角色](#create-product-profile)。

## 建立新角色 {#create-product-profile}

[!DNL Journey Optimizer]可讓您建立自己的&#x200B;**[!UICONTROL 角色]**，並將一組許可權和沙箱指派給您的使用者。 透過&#x200B;**[!UICONTROL 角色]**，您可以授權或拒絕存取介面中的特定功能或物件。

有關如何建立和管理沙箱的詳細資訊，請參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hant){target="_blank"}。

在此範例中，我們將建立名為&#x200B;**Journeys唯讀角色**，其中我們將授與歷程功能的唯讀許可權。 使用者將只能存取及檢視歷程，而且將無法存取[!DNL Journey Optimizer]中的其他功能，例如&#x200B;**[!DNL  Decision management]**。

若要建立我們的&#x200B;**唯讀歷程** **[!UICONTROL 角色]**：

1. 若要將角色指派給[!DNL Permissions]產品中的使用者，請瀏覽至&#x200B;**[!UICONTROL 角色]**&#x200B;索引標籤，然後按一下&#x200B;**[!UICONTROL 建立角色]**。

   ![](assets/do-not-localize/access_control_9.png)

1. 為您的新&#x200B;**[!UICONTROL 角色]**&#x200B;新增&#x200B;**[!UICONTROL 名稱]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。 然後，按一下&#x200B;**[!UICONTROL 確認]**。

   ![](assets/do-not-localize/access_control_10.png)

1. 從&#x200B;**[!UICONTROL 沙箱]**&#x200B;資源下拉式清單中，選擇要指派給您的&#x200B;**[!UICONTROL 角色]**&#x200B;的沙箱。 [進一步瞭解 sandbox](sandboxes.md)。

   ![](assets/do-not-localize/access_control_13.png)

1. 在左側功能表中列出的[!DNL Journey Optimizer]中可用的不同資源（例如&#x200B;**[!DNL Journeys]**、**[!DNL Segments]**&#x200B;或&#x200B;**[!DNL Decision management]**）之間選取。

   在此我們選取&#x200B;**[!UICONTROL Journeys]**&#x200B;資源。

   ![](assets/do-not-localize/access_control_11.png)

1. 從&#x200B;**[!UICONTROL 歷程]**&#x200B;下拉式清單中，選取要指派給您&#x200B;**[!UICONTROL 角色]**&#x200B;的許可權。

   我們在這裡選取&#x200B;**[!DNL View journeys]**、**[!DNL View journeys report]**&#x200B;和&#x200B;**[!DNL View journeys event, data sources, actions]**。

   ![](assets/do-not-localize/access_control_12.png)

1. 完成時，按一下&#x200B;**[!UICONTROL 儲存]**。

您的&#x200B;**[!UICONTROL 角色]**&#x200B;現已建立並設定。 您現在需要將其指派給使用者。

如需角色建立與管理的詳細資訊，請參閱[Admin Console檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html)。
