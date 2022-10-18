---
solution: Journey Optimizer
product: journey optimizer
title: 管理使用者和產品設定檔
description: 瞭解如何管理權限
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 6%

---

# 管理使用者和產品設定檔 {#manage-permissions}

>[!IMPORTANT]
>
> 以下詳述的每個程式只能由 **[!UICONTROL 產品]** 或 **[!UICONTROL 系統]** 管理員。 如需詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL 產品設定檔]** 是一組使用者，在您的組織內共用相同的權限和沙箱。

此 [!DNL Journey Optimizer] 產品可讓您在不同的現成可用功能之間進行選取 **[!UICONTROL 產品設定檔]** 擁有指派給使用者的不同權限。 如需可用 **[!UICONTROL 產品設定檔]**，請參閱 [頁面](ootb-product-profiles.md).

屬於 **[!UICONTROL 產品設定檔]** 有權使用產品中包含的Adobe應用程式和服務。

您也可以建立自己的 **[!UICONTROL 產品設定檔]** 如果您想要微調使用者對介面中特定功能或物件的存取權。

## 指派產品設定檔 {#assigning-product-profile}

您可以選取指派現成可用或自訂 **[!UICONTROL 產品設定檔]** 給您的使用者。

您可以在 [內建的產品設定檔](ootb-product-profiles.md) 區段。

若要指派 **[!UICONTROL 產品設定檔]**:

1. 在 [!DNL Admin Console]，從 **[!UICONTROL 產品]** 頁簽，選擇 **[!UICONTROL Experience Cloud — 平台支援的應用程式]** 產品。

1. 選取 **[!UICONTROL 產品設定檔]**.

   ![](assets/do-not-localize/access_control_2.png)

1. 從 **[!UICONTROL 使用者]** 按一下 **[!UICONTROL 新增使用者]**.

   ![](assets/do-not-localize/access_control_3.png)

1. 輸入您的使用者名稱或電子郵件地址，然後選取使用者。

   若使用者先前未在 [!DNL Admin Console]，請參閱 [新增使用者檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. 執行上述步驟，將其他使用者新增至您的 **[!UICONTROL 產品設定檔]**. 然後，按一下 **[!UICONTROL 儲存]**.

接著，您的使用者應會收到一封電子郵件，並重新導向至您的執行個體。

有關用戶管理的詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

存取執行個體時，您的使用者會根據 **[!UICONTROL 產品設定檔]**. 如果使用者沒有權限存取功能，則會出現下列訊息：

`You don't have permission to access this feature. Permission needed: XX.`

## 編輯現有的產品設定檔 {#edit-product-profile}

適用於現成或自訂 **[!UICONTROL 產品設定檔]**，您可以隨時決定新增或刪除權限。

在此範例中，我們要新增 **[!UICONTROL 權限]** 與 **[!UICONTROL 歷程]** 指派給歷程檢視器的使用者功能 **[!UICONTROL 產品設定檔]**. 然後，使用者就能發佈歷程。

請注意，如果您修改現成可用或自訂 **[!UICONTROL 產品設定檔]**，則會影響指派給此的每個使用者 **[!UICONTROL 產品設定檔]**.

1. 在 [!DNL Admin Console]，從 **[!UICONTROL 產品]** 頁簽，選擇 **[!UICONTROL Experience Cloud — 平台支援的應用程式]** 產品。

1. 選取歷程檢視器 **[!UICONTROL 產品設定檔]**.

1. 選取 **[!UICONTROL 權限]** 標籤。

   此 **[!UICONTROL 權限]** 索引標籤會顯示套用至 **[!UICONTROL Experience Cloud — 平台支援的應用程式]** 產品。

   ![](assets/do-not-localize/access_control_5.png)

1. 選取 **[!UICONTROL 歷程]** 功能。

   ![](assets/do-not-localize/access_control_6.png)

1. 從 **[!UICONTROL 可用權限項目]** 清單中，選取要指派給您的權限 **[!UICONTROL 產品設定檔]** 按一下加號(+)圖示即可。

   在此，我們新增 **[!UICONTROL 發佈歷程]** 權限。

1. 如有需要，在 **[!UICONTROL 包含的權限項目]**，按一下旁邊的X圖示以移除產品設定檔的權限。

1. 完成時，按一下&#x200B;**[!UICONTROL 「儲存」]**。

如有需要，您也可以使用特定權限建立新的產品設定檔。 有關詳細資訊，請參閱 [建立產品設定檔](#create-product-profile).

## 建立產品設定檔 {#create-product-profile}

[!DNL Journey Optimizer] 可讓您建立自己的 **[!UICONTROL 產品設定檔]** 並將一組權限和沙箱指派給您的使用者。 使用 **[!UICONTROL 產品設定檔]**，您可以授權或拒絕存取介面中的特定功能或物件。

如需如何建立和管理沙箱的詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}。

在此範例中，我們將建立名為 **歷程唯讀** 我們會授予歷程功能的唯讀權限。 使用者將只能存取及檢視歷程，而無法存取其他功能，例如 **[!DNL  Decision management]** in [!DNL Journey Optimizer].

若要建立 **歷程唯讀** **[!UICONTROL 產品設定檔]**:

1. 存取 [!DNL Admin Console].

1. 從 **[!UICONTROL 產品]** 頁簽，選擇 **[!UICONTROL Experience Cloud — 平台支援的應用程式]** 產品。

1. 按一下「**[!UICONTROL 新描述檔]**」。

   ![](assets/do-not-localize/access_control_9.png)

1. 新增 **[!UICONTROL 產品設定檔名稱]**, **[!UICONTROL 顯示名稱]** 和 **[!UICONTROL 說明]** 新 **[!UICONTROL 產品設定檔]**.

   ![](assets/do-not-localize/access_control_10.png)

1. 在 **[!UICONTROL 通知]** 類別，選擇從此產品設定檔新增或移除使用者時，使用者是否會收到電子郵件通知。

1. 完成後，按一下 **[!UICONTROL 儲存]** 選取您新建立的 **[!UICONTROL 產品設定檔]**.

1. 若要新增使用者存取不同功能的權限，請選取 **[!UICONTROL 權限]** 標籤。

1. 在不同功能之間選取，例如 **[!DNL Journeys]**, **[!DNL Segments]** 或 **[!DNL Decision management]** 可在 [!DNL Journey Optimizer] 清單中。

   在此處，我們選取 **[!UICONTROL 歷程]** 功能。

   ![](assets/do-not-localize/access_control_11.png)

1. 從 **[!UICONTROL 可用權限項目]** 清單中，選取要指派給您的權限 **[!UICONTROL 產品設定檔]** 按一下加號(+)圖示即可。

   在此，我們選取 **[!DNL View journeys]** 和 **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. 選取 **[!UICONTROL 沙箱存取]** 選擇要指派給您的沙箱的功能 **[!UICONTROL 產品設定檔]**.

   ![](assets/do-not-localize/access_control_13.png)

1. 在 **[!UICONTROL 可用權限項目]**，按一下加號(+)圖示，將沙箱指派給您的設定檔。 [進一步瞭解 sandbox](sandboxes.md)。

1. 完成時，按一下&#x200B;**[!UICONTROL 「儲存」]**。

您的 **[!UICONTROL 產品設定檔]** 現在已建立並設定。 您現在需要將其指派給使用者。

如需產品設定檔建立與管理的詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
