---
title: 管理使用者和產品設定檔
description: 瞭解如何管理權限
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: 控制組
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 15%

---

# 管理使用者和產品設定檔 {#manage-permissions}

>[!IMPORTANT]
>
> 下面詳述的每個過程只能由&#x200B;**[!UICONTROL Product]**&#x200B;或&#x200B;**[!UICONTROL System]**&#x200B;管理員執行。 如需詳細資訊，請參閱[管理控制台檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html)。

**[!UICONTROL Product profiles]** 是一組使用者，在您的組織內共用相同的權限和沙箱。

[!DNL Journey Optimizer]產品可讓您在不同現成可用的&#x200B;**[!UICONTROL Product profiles]**&#x200B;之間進行選取，具有指派給您使用者的不同權限層級。 有關可用&#x200B;**[!UICONTROL Product profiles]**&#x200B;的詳細資訊，請參閱此[page](ootb-product-profiles.md)。

屬於&#x200B;**[!UICONTROL Product profiles]**&#x200B;的每個使用者都有權使用產品中包含的Adobe應用程式和服務。

如果您想要微調用戶對介面中某些功能或對象的訪問，也可以建立自己的&#x200B;**[!UICONTROL Product profiles]**。

## 指派產品設定檔 {#assigning-product-profile}

您可以選擇將現成可用或自訂&#x200B;**[!UICONTROL Product profile]**&#x200B;指派給您的使用者。

您可在[內建產品設定檔](ootb-product-profiles.md)區段中，找到每個具備指派權限的現成可用產品設定檔清單。

要分配&#x200B;**[!UICONTROL Product profile]**:

1. 在[!DNL Admin Console]中，從&#x200B;**[!UICONTROL Products]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Experience Cloud - Platform powered applications]**&#x200B;產品。

1. 選取 **[!UICONTROL Product profile]**。

   ![](../assets/access_control_2.png)

1. 在 **[!UICONTROL Users]** 索引標籤中，按一下 **[!UICONTROL Add user]**。

   ![](../assets/access_control_3.png)

1. 輸入您的使用者名稱或電子郵件地址，然後選取使用者。

   如果用戶先前未在[!DNL Admin Console]中建立，請參閱[添加用戶文檔](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)。

   ![](../assets/access_control_4.png)

1. 執行與上述步驟相同的步驟，將其他使用者新增至您的&#x200B;**[!UICONTROL Product profile]**。 然後，按一下&#x200B;**[!UICONTROL Save]**。

接著，您的使用者應會收到一封電子郵件，並重新導向至您的執行個體。

有關用戶管理的詳細資訊，請參閱[Admin Console文檔](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html)。

存取執行個體時，您的使用者會根據&#x200B;**[!UICONTROL Product profile]**&#x200B;中指派的權限看到特定檢視。 如果使用者沒有權限存取功能，則會出現下列畫面。

![](../assets/access_control_1.png)

## 編輯現有的產品設定檔 {#edit-product-profile}

若為現成可用或自訂的&#x200B;**[!UICONTROL Product profiles]**，您可以隨時決定新增或刪除權限。

在此範例中，我們想為指派給歷程檢視器&#x200B;**[!UICONTROL Product profile]**&#x200B;的使用者新增與&#x200B;**[!UICONTROL Message]**&#x200B;功能相關的&#x200B;**[!UICONTROL Permissions]**。 然後，使用者便能發佈訊息。

請注意，如果您修改現成可用或自訂&#x200B;**[!UICONTROL Product profile]**，則會影響指派給此&#x200B;**[!UICONTROL Product profile]**&#x200B;的每個使用者。

1. 在[!DNL Admin Console]中，從&#x200B;**[!UICONTROL Products]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Experience Cloud - Platform powered applications]**&#x200B;產品。

1. 選取歷程檢視器&#x200B;**[!UICONTROL Product profile]**。

1. 選取 **[!UICONTROL Permissions]** 索引標籤。

   **[!UICONTROL Permissions]**&#x200B;標籤顯示適用於&#x200B;**[!UICONTROL Experience Cloud - Platform powered applications]**&#x200B;產品的功能清單。

   ![](../assets/access_control_5.png)

1. 選擇&#x200B;**[!UICONTROL Messages]**&#x200B;功能。

   ![](../assets/access_control_6.png)

1. 從&#x200B;**[!UICONTROL Available Permission Items]**&#x200B;清單中，按一下加號(+)圖示，選取要指派給&#x200B;**[!UICONTROL Product profile]**&#x200B;的權限。

   在此處新增&#x200B;**[!UICONTROL Publish messages]**&#x200B;權限。

   ![](../assets/access_control_7.png)

1. 如有需要，請在 **[!UICONTROL Included Permission Items]**&#x200B;下方，按一下旁邊的 X 圖示，以移除產品設定檔的權限。

1. 完成後，按一下 **[!UICONTROL Save]**。

   ![](../assets/access_control_8.png)

如有需要，您也可以使用特定權限建立新的產品設定檔。 如需詳細資訊，請參閱[建立產品設定檔](#create-product-profile)。

## 建立產品設定檔 {#create-product-profile}

[!DNL Journey Optimizer] 可讓您建立自己的 **[!UICONTROL Product profiles]** 權限，並將一組權限和沙箱指派給您的使用者。使用&#x200B;**[!UICONTROL Product profiles]**，您可以授權或拒絕訪問介面中的某些功能或對象。

如需如何建立和管理沙箱的詳細資訊，請參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}。

在此範例中，我們將建立名為&#x200B;**Journeys唯讀**&#x200B;的產品設定檔，其中我們會授予Journey功能的唯讀權限。 使用者將只能存取和檢視歷程，而無法存取&#x200B;**[!UICONTROL Decision management]**&#x200B;或&#x200B;**[!UICONTROL Messages]**&#x200B;等[!DNL Journey Optimizer]中的其他功能。

若要建立我們的&#x200B;**歷程唯讀** **[!UICONTROL product profiles]**:

1. 訪問[!DNL Admin Console]。

1. 從&#x200B;**[!UICONTROL Products]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Experience Cloud - Platform powered applications]**&#x200B;產品。

1. 按一下「**[!UICONTROL New Profile]**」。

   ![](../assets/access_control_9.png)

1. 為新&#x200B;**[!UICONTROL product profiles]**&#x200B;新增&#x200B;**[!UICONTROL Product Profile Name]**、**[!UICONTROL Display Name]**&#x200B;及&#x200B;**[!UICONTROL Description]**。

   ![](../assets/access_control_10.png)

1. 在 **[!UICONTROL Notifications]** 類別中，選擇從此產品設定檔新增或移除使用者時，使用者是否會收到電子郵件通知。

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;並選擇新建立的&#x200B;**[!UICONTROL product profiles]**。

1. 要添加用戶訪問不同功能的權限，請選擇&#x200B;**[!UICONTROL Permissions]**&#x200B;頁簽。

1. 在左側功能表所列的[!DNL Journey Optimizer]中可用的不同功能（如&#x200B;**[!UICONTROL Messages]**、**[!UICONTROL Segments]**&#x200B;或&#x200B;**[!UICONTROL Decision management]**）之間進行選擇。

   在此，我們選取&#x200B;**[!UICONTROL Journeys]**&#x200B;功能。

   ![](../assets/access_control_11.png)

1. 從&#x200B;**[!UICONTROL Available Permission Items]**&#x200B;清單中，按一下加號(+)圖示，選取要指派給&#x200B;**[!UICONTROL Product profile]**&#x200B;的權限。

   在此處，我們選取&#x200B;**[!UICONTROL View journeys]**&#x200B;和&#x200B;**[!UICONTROL View journeys event, data sources, actions]**。

   ![](../assets/access_control_12.png)

1. 選取&#x200B;**[!UICONTROL Sandbox access]**&#x200B;功能，以選擇要指派給&#x200B;**[!UICONTROL Product profile]**&#x200B;的沙箱。

   ![](../assets/access_control_13.png)

1. 在 **[!UICONTROL Available Permissions Items]** 下方，按一下加號 (+) 圖示，將沙箱指派給您的設定檔。[進一步瞭解 sandbox](sandboxes.md)。

1. 完成後，按一下 **[!UICONTROL Save]**。

您的&#x200B;**[!UICONTROL Product profile]**&#x200B;現在已建立並設定。 您現在需要將其指派給使用者。

如需產品設定檔建立與管理的詳細資訊，請參閱[Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html)。
