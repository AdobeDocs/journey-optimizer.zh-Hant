---
solution: Journey Optimizer
product: journey optimizer
title: 在Journey Optimizer中使用資產
description: 開始使用Experience Manager Assets
feature: Assets, Integrations
topic: Content Management, Integrations
role: User
level: Beginner
keywords: 資產， experience manager，整合
exl-id: d4fde14b-e2da-40bf-a387-ee9f2f7ff204
source-git-commit: 4899dbe71243184b6283a32a4fe7eb2edb82f872
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 8%

---

# 透過建立和管理資產 [!DNL Experience Manager Assets]{#experience-manager-assets}

## 開始使用 [!DNL Experience Manager Assets] {#get-started-assets}

利用 **[!DNL Adobe Experience Manager Assets]** 將行銷與創意內容工作流程結合在一起。原生整合，與 **[!DNL Adobe Journey Optimizer]**，存取 **[!DNL Assets Essentials]** 或 **[!DNL Assets as a Cloud Service]** 儲存、管理、探索及發佈數位資產。 提供了可用於填入訊息的單一、集中式資產存放庫。

**[!DNL Adobe Experience Manager Assets]** 提供兩個合作和集中式資產工作區，可擴充您的創意系統並統一數位資產以提供體驗：

* **[!DNL Assets as a Cloud Service]**：Adobe Experience Manager Assetsas a Cloud Service提供簡單易用的雲端解決方案，讓您有效率地管理數位資產管理和Dynamic Media作業。 它緊密整合了進階功能，包括人工智慧和機器學習。

  進一步瞭解 [Adobe Experience Manager as a Cloud Service檔案](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/overview.html).

* **[!DNL Assets Essentials]**： Experience Manager Assets Essentials是Assetsas a Cloud Service的輕量型解決方案，提供統一的資產管理和共同作業功能。 透過現代化、簡化的介面，其可讓創意和行銷團隊輕鬆儲存、探索和分發數位資產。

  進一步瞭解 [Adobe Experience Manager Assets Essentials檔案](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

根據您的合約， **[!DNL Adobe Experience Manager Assets Essentials]** 或 **[!DNL Adobe Experience Manager Assets as a Cloud Service]** 可以直接從存取 **[!DNL Adobe Journey Optimizer]** 透過左側功能表 **[!UICONTROL 資產]** 區段。 您也可以在下列情況下存取資產和資料夾： [設計電子郵件內容](../email/get-started-email-design.md).

## 先決條件{#assets-prerequisites}

>[!BEGINTABS]

>[!TAB Adobe Experience Manager Assets Essentials]

使用前 [!DNL Adobe Experience Manager Assets Essentials]，您必須將使用者新增至 **Assets Essentials消費者使用者** 或/和 **Assets Essentials使用者** 產品設定檔。 詳細內容： [Assets Essentials檔案](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html#add-user-groups){target="_blank"}.

>[!NOTE]
>針對 2022 年 1 月 6 日之前取得的 Journey Optimizer 產品，您必須為貴組織部署 **[!DNL Adobe Experience Manager Assets Essentials]** 。 在[部署 Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=zh-Hant){target="_blank"} 一節中了解更多。

>[!TAB Adobe Experience Manager Assets 雲端服務]

使用前 **[!DNL Adobe Experience Manager Assets as a Cloud Service]**，您必須將使用者新增至「資產」Cloud Service。 詳細內容： [Adobe Experience Manager Assetsas a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/security/ims-support.html).

>[!ENDTABS]

## 上傳和插入資產{#add-asset}

將檔案匯入 **[!DNL Assets Essentials]** 或 **[!DNL Assets as a Cloud Service]**，您必須先瀏覽或建立要儲存的資料夾。 然後，您就可以將它們插入您的電子郵件內容。

1. 從 [!DNL Adobe Journey Optimizer] 首頁，選取 **[!UICONTROL 資產]** 標籤下的 **[!UICONTROL 內容管理]** 功能表以存取 **[!DNL Assets Essentials]** 或 **[!DNL Assets as a Cloud Service]**.

   ![](assets/media_library_1.png)

1. 在Journey Optimizer中選擇資產的存放庫。 您可以選擇 **[!DNL Assets Essentials]** 或 **[!DNL Assets as a Cloud Service]** 存放庫，前提是您擁有此解決方案。

   ![](assets/media_library_4.png)

+++ 瞭解如何切換資產存放庫。

   若要變更您的資產存放庫，請選取右上角的「帳戶」圖示，然後按一下 **[!UICONTROL 選取存放庫]**.

   ![](assets/media_library_3.png)

+++

1. 在中央區段或樹狀檢視中連按兩下資料夾以開啟它。

   您也可以按一下 **[!UICONTROL 建立資料夾]** 以建立新資料夾。

   ![](assets/media_library_8.png)

1. 一旦進入選取或建立的資料夾，按一下 **[!UICONTROL 新增資產]** 將新資產上傳至資料夾。

   ![](assets/media_library_2.png)

1. 從 **[!UICONTROL 上傳檔案]**，按一下 **[!UICONTROL 瀏覽]** 並選擇是否要 **[!UICONTROL 瀏覽檔案]** 或 **[!UICONTROL 瀏覽資料夾]**.

1. 選取您要上傳的檔案。 完成後，按一下 **[!UICONTROL 上傳]**. 要瞭解有關如何管理資產的詳細資訊，請參閱本 [頁面](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/manage-organize.html).

1. 若要使用Adobe Photoshop Express進一步編輯您的資產，請連按兩下資產。 然後，從右側功能表中選取 **[!UICONTROL 編輯模式]** 圖示。 [了解更多](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/edit-images.html){target="_blank"}.

   ![](assets/media_library_12.png)

1. 從 [!DNL Adobe Journey Optimizer]，選取 **[!UICONTROL 資產選取器]** 電子郵件設計工具左窗格中的功能表。

   ![](assets/media_library_5.png)

1. 選取您先前建立的 **[!UICONTROL 資產]** 資料夾。 您也可以在搜尋列中搜尋資產或資料夾。

1. 將您的資產拖放到電子郵件內容中。

   ![](assets/media_library_6.png)

1. 您可以進一步自訂資產，例如使用新增外部連結或文字 **[!UICONTROL 設定]** 和 **[!UICONTROL 樣式]** 索引標籤。 [深入瞭解元件設定](../email/content-components.md)

   ![](assets/media_library_13.png)

   <!--
    After adding your asset to your email, use the **[!UICONTROL Find similar Stock photos]** option to locate Stock photos that match the content, color, and composition of your image. [Learn more about Adobe Stock](stock.md).

    Note that this option is available for licensed/unlicensed Stock images and images from your Assets folder. 

    ![](assets/media_library_14.png)
    -->


## [!DNL Adobe Experience Manager Assets]常見問題集 {#faq-assets}

+++ 我可以繼續使用Journey Optimizer中的Assets Essentials隨附存放庫嗎？

如果您布建於 **[!DNL Adobe Experience Manager Assets as a Cloud Service]**，您可以同時存取 **[!DNL Adobe Experience Manager Assets Essentials]** 和 **[!DNL Adobe Experience Manager Assets as a Cloud Service]** 存放庫（如果使用者擁有正確的許可權）。 這些存放庫是分開且不同步。 Journey Optimizer中的使用者將能夠檢視這兩個存放庫，包括他們有權存取的其他環境，例如Stage、Dev等，並且應該能夠使用存放庫選擇器順暢地在它們之間切換。

+++

+++ 如何管理資產？ as a Cloud Service的資產變更是否會反映在Journey Optimizer中？

**[!DNL Adobe Experience Manager Assets as a Cloud Service]** 與Journey Optimizer整合的方式與類似 **[!DNL Adobe Experience Manager Assets Essentials]**. 對資產進行修改時，會產生二進位副本。 請注意，更新於 **[!DNL Assets as a Cloud Service]** 不要自動傳播至即時電子郵件行銷活動。 您必須在電子郵件設計工具中手動重新選取任何變更，以確保資產與正在進行的電子郵件行銷活動之間的同步。

+++

+++ 我可以在Journey Optimizer中製作電子郵件時使用Dynamic Media URL嗎？

是，您可以在Journey Optimizer電子郵件製作中使用Dynamic Media URL。 只要貼上URL即可，無需從資產選擇器中選取。

+++

+++ Journey Optimizer使用者可以從Journey Optimizer介面變更Adobe Experience Manager Assetsas a Cloud Service存放庫嗎？

只要Journey Optimizer使用者有權使用 **[!DNL Adobe Experience Manager Assets as a Cloud Service]** 標準使用者並擁有存放庫的「編輯」許可權，使用者便能編輯 **[!DNL Adobe Experience Manager Assets as a Cloud Service]** 存放庫。

+++
