---
product: experience platform
solution: Experience Platform
title: 授與 Offer Decisioning 的存取權限
description: 了解如何透過Adobe Admin Console管理Offer Decisioning服務的使用者權限。
feature: Collections
role: User
level: Intermediate
exl-id: 2a2fece9-1ad5-498e-b0ee-5bb0b73a2cd5
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 7%

---

# 授予決策管理的存取權 {#granting-acess-to-decision-management}

存取和使用offer decisioning功能的權限是透過 [Adobe Admin Console](https://helpx.adobe.com/tw/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}。

若要授與「決策管理」功能的存取權，您必須建立 **[!UICONTROL Product profile]** 並指派對應的權限給您的使用者。 深入了解管理 [!DNL Journey Optimizer] 使用者和權限 [本節](../../administration/permissions.md).

決策管理的特定權限列於 [本節](../../administration/high-low-permissions.md#manage-decisioning).

<!--If you are a [!DNL Journey Optimizer] user leveraging the **Decision Management** functionality, you need to have the [Decision management permissions](../../administration/high-low-permissions.md#decisions-permissions) enabled to acces all related capabilities. Learn more on managing [!DNL Journey Optimizer] users and permissions in [this section](../../administration/permissions.md).

If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service, follow the steps [below](#granting-acess-to-offer-decisioning) to grant access to [!DNL Offer Decisioning].

Grant access to Offer Decisioning

The steps below only apply to **Experience Platform users** leveraging the [!DNL Offer Decisioning] service.-->

1. 開啟 [Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html)，然後選取 **[!UICONTROL Adobe Experience Platform]**.

   <!--![](../../assets/offers_admin_console.png)-->

1. 服務的產品設定檔隨即顯示。 若要建立新的產品設定檔，請按一下 **[!UICONTROL New Profile]** 按鈕。

   ![](../../assets/offers_rights_productprofile.png)

   >[!NOTE]
   >
   >您可以有任意數量的產品設定檔，對應您要為組織設定的各種角色。

1. 指定產品設定檔的名稱和說明，然後按一下 **[!UICONTROL Next]**.

   ![](../../assets/create-product-profile.png)

   <!--To access the product profile’s permissions, select the **[!UICONTROL Permissions]** line.-->

1. 選取要為產品設定檔啟用的服務。 依預設，會選取所有服務，以確保所有Experience Platform功能皆可使用。

   ![](../../assets/enable-services.png)

1. 在 **[!UICONTROL Decision Management]** 區段，按一下 **+** 按鈕，將權限指派給產品設定檔，然後按一下 **[!UICONTROL Save]**.

   ![](../../assets/configure-profile.png)

   可用權限包括：

   **[!UICONTROL Manage Decisioning Activities]**：

   * 讀、寫、刪除優惠方案
   * 讀取、寫入、刪除決策（先前稱為優惠方案活動）
   * 讀、寫、刪除版位

   **[!UICONTROL Execute Decisioning Activities]**：

   * 讀取優惠方案
   * 閱讀決策
   * 讀取版位

   **[!UICONTROL Manage Decisioning Options]**：

   * 讀、寫、刪除優惠方案
   * 閱讀決策
   * 讀、寫、刪除版位



1. 隨即顯示產品設定檔權限的摘要。 您現在可以將使用者指派至產品設定檔，讓他們存取這些權限。

   ![](../../assets/product-profile-created.png)

>[!NOTE]
>
>如需如何管理使用者權限的詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}。

