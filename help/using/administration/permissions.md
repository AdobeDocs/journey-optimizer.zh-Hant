---
title: 管理使用者和產品設定檔
description: 瞭解如何管理權限
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 7e879a56a5ed416cc12c2acc3131e17f9dd1e757
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 14%

---

# 管理使用者和產品設定檔 {#manage-permissions}

>[!IMPORTANT]
>
> 以下詳述的每個程式只能由 **[!UICONTROL Product]** 或 **[!UICONTROL System]** 管理員。 如需詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Product profiles]** 是一組使用者，在您的組織內共用相同的權限和沙箱。

此 [!DNL Journey Optimizer] 產品可讓您在不同的現成可用功能之間進行選取 **[!UICONTROL Product profiles]** 擁有指派給使用者的不同權限。 如需可用 **[!UICONTROL Product profiles]**，請參閱 [頁面](ootb-product-profiles.md).

屬於 **[!UICONTROL Product profiles]** 有權使用產品中包含的Adobe應用程式和服務。

您也可以建立自己的 **[!UICONTROL Product profiles]** 如果您想要微調使用者對介面中特定功能或物件的存取權。

## 指派產品設定檔 {#assigning-product-profile}

您可以選取指派現成可用或自訂 **[!UICONTROL Product profile]** 給您的使用者。

您可以在 [內建的產品設定檔](ootb-product-profiles.md) 區段。

若要指派 **[!UICONTROL Product profile]**:

1. 在 [!DNL Admin Console]，從 **[!UICONTROL Products]** 頁簽，選擇 **[!UICONTROL Experience Cloud - Platform powered applications]** 產品。

1. 選取 **[!UICONTROL Product profile]**。

   ![](../assets/do-not-localize/access_control_2.png)

1. 在 **[!UICONTROL Users]** 索引標籤中，按一下 **[!UICONTROL Add user]**。

   ![](../assets/do-not-localize/access_control_3.png)

1. 輸入您的使用者名稱或電子郵件地址，然後選取使用者。

   若使用者先前未在 [!DNL Admin Console]，請參閱 [新增使用者檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](../assets/do-not-localize/access_control_4.png)

1. 執行上述步驟，將其他使用者新增至您的 **[!UICONTROL Product profile]**. 然後，按一下 **[!UICONTROL Save]**.

接著，您的使用者應會收到一封電子郵件，並重新導向至您的執行個體。

有關用戶管理的詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

存取執行個體時，您的使用者會根據 **[!UICONTROL Product profile]**. 如果使用者沒有權限存取功能，則會出現下列畫面。

![](../assets/do-not-localize/access_control_1.png)

## 編輯現有的產品設定檔 {#edit-product-profile}

適用於現成或自訂 **[!UICONTROL Product profiles]**，您可以隨時決定新增或刪除權限。

在此範例中，我們要新增 **[!UICONTROL Permissions]** 與 **[!UICONTROL Message]** 指派給歷程檢視器的使用者功能 **[!UICONTROL Product profile]**. 然後，使用者便能發佈訊息。

請注意，如果您修改現成可用或自訂 **[!UICONTROL Product profile]**，則會影響指派給此的每個使用者 **[!UICONTROL Product profile]**.

1. 在 [!DNL Admin Console]，從 **[!UICONTROL Products]** 頁簽，選擇 **[!UICONTROL Experience Cloud - Platform powered applications]** 產品。

1. 選取歷程檢視器 **[!UICONTROL Product profile]**.

1. 選取 **[!UICONTROL Permissions]** 索引標籤。

   此 **[!UICONTROL Permissions]** 索引標籤會顯示套用至 **[!UICONTROL Experience Cloud - Platform powered applications]** 產品。

   ![](../assets/do-not-localize/access_control_5.png)

1. 選取 **[!UICONTROL Messages]** 功能。

   ![](../assets/do-not-localize/access_control_6.png)

1. 從 **[!UICONTROL Available Permission Items]** 清單中，選取要指派給您的權限 **[!UICONTROL Product profile]** 按一下加號(+)圖示即可。

   在此，我們新增 **[!UICONTROL Publish messages]** 權限。

   ![](../assets/do-not-localize/access_control_7.png)

1. 如有需要，請在 **[!UICONTROL Included Permission Items]**&#x200B;下方，按一下旁邊的 X 圖示，以移除產品設定檔的權限。

1. 完成後，按一下 **[!UICONTROL Save]**。

   ![](../assets/do-not-localize/access_control_8.png)

如有需要，您也可以使用特定權限建立新的產品設定檔。 有關詳細資訊，請參閱 [建立產品設定檔](#create-product-profile).

## 建立產品設定檔 {#create-product-profile}

[!DNL Journey Optimizer] 可讓您建立自己的 **[!UICONTROL Product profiles]** 並將一組權限和沙箱指派給您的使用者。 使用 **[!UICONTROL Product profiles]**，您可以授權或拒絕存取介面中的特定功能或物件。

如需如何建立和管理沙箱的詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}。

在此範例中，我們將建立名為 **歷程唯讀** 我們會授予歷程功能的唯讀權限。 使用者將只能存取及檢視歷程，而無法存取其他功能，例如 **[!UICONTROL Decision management]** 或 **[!UICONTROL Messages]** in [!DNL Journey Optimizer].

若要建立 **歷程唯讀** **[!UICONTROL product profiles]**:

1. 存取 [!DNL Admin Console].

1. 從 **[!UICONTROL Products]** 頁簽，選擇 **[!UICONTROL Experience Cloud - Platform powered applications]** 產品。

1. 按一下「**[!UICONTROL New Profile]**」。

   ![](../assets/do-not-localize/access_control_9.png)

1. 新增 **[!UICONTROL Product Profile Name]**, **[!UICONTROL Display Name]** 和 **[!UICONTROL Description]** 新 **[!UICONTROL product profiles]**.

   ![](../assets/do-not-localize/access_control_10.png)

1. 在 **[!UICONTROL Notifications]** 類別中，選擇從此產品設定檔新增或移除使用者時，使用者是否會收到電子郵件通知。

1. 完成後，按一下 **[!UICONTROL Save]** 選取您新建立的 **[!UICONTROL product profiles]**.

1. 若要新增使用者存取不同功能的權限，請選取 **[!UICONTROL Permissions]** 標籤。

1. 在不同功能之間選取，例如 **[!UICONTROL Messages]**, **[!UICONTROL Segments]** 或 **[!UICONTROL Decision management]** 可在 [!DNL Journey Optimizer] 清單中。

   在此處，我們選取 **[!UICONTROL Journeys]** 功能。

   ![](../assets/do-not-localize/access_control_11.png)

1. 從 **[!UICONTROL Available Permission Items]** 清單中，選取要指派給您的權限 **[!UICONTROL Product profile]** 按一下加號(+)圖示即可。

   在此，我們選取 **[!UICONTROL View journeys]** 和 **[!UICONTROL View journeys event, data sources, actions]**.

   ![](../assets/do-not-localize/access_control_12.png)

1. 選取 **[!UICONTROL Sandbox access]** 選擇要指派給您的沙箱的功能 **[!UICONTROL Product profile]**.

   ![](../assets/do-not-localize/access_control_13.png)

1. 在 **[!UICONTROL Available Permissions Items]** 下方，按一下加號 (+) 圖示，將沙箱指派給您的設定檔。[進一步瞭解 sandbox](sandboxes.md)。

1. 完成後，按一下 **[!UICONTROL Save]**。

您的 **[!UICONTROL Product profile]** 現在已建立並設定。 您現在需要將其指派給使用者。

如需產品設定檔建立與管理的詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
