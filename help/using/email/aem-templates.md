---
solution: Journey Optimizer
product: journey optimizer
title: 使用模AEM板
description: 瞭解如何在中建立模AEM板並將其導出到Journey Optimizer
hide: true
hidefromtoc: true
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
exl-id: e4935129-c1cb-41b1-b84d-cd419053c303
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 3%

---

# 使用Adobe Experience Manager模板 {#aem-templates}

>[!AVAILABILITY]
>
>目前，與Adobe Experience Manager的整合只作為測試版提供給特定用戶。
> 作為測試版用戶，使用 [此表格](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} 共用反饋。

使用Adobe Journey Optimizer，您可以通過Adobe Experience Manager網站建立定製的消息。 首先使用Adobe Experience Manager的內容源設計模板，然後將其發送到Adobe Journey Optimizer。 共用後，這些模板可以在Adobe Journey Optimizer的電子郵件設計師中訪問，從而簡化了為您所需的受眾製作和發送消息的過程。

## 先決條件 {#prerequisites}

開始使用此功能之前，請確保符合以下要求：

* **Experience Manager設定**

   此功能可用於 [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/overview/introduction.html){target="_blank"}。

   作為測試程式的一部分，Cloud Service配置由Adobe Experience ManagerAdobe執行以連接到Adobe Journey Optimizer。

* **權限**

   要在Adobe Journey Optimizer建立、編輯和刪除內容模板，必須 **[!DNL Manage Library Items]** 包含在 **[!DNL Content Library Manager]** 產品配置檔案。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)

## 護欄和限制{#aem-templates-limitations}

為了進一步優化Adobe Experience Manager與Adobe Journey Optimizer的使用，必須注意以下附加的保障和限制：

* 要有效地實現Experience Manager模板中的個性化，需要正確的Journey Optimizer語法。 [了解更多](../personalization/personalization-syntax.md)

* 當前不支援批量模板導出，必須單獨導出模板。

* Experience Manager和Journey Optimizer之間的同步當前不可用。 如果在將Experience Manager模板發送到Journey Optimizer後對其進行了更改，則用戶需要重新導出該模板並將其重新發送到Journey Optimizer。

## 向Journey Optimizer發送模板{#aem-templates-send}

要將Adobe Experience Manager模板導出到Adobe Journey Optimizer，請執行以下步驟：

1. 從您的Adobe Experience Manager首頁，選擇 **[!UICONTROL 出站市場營銷]**。

   ![](assets/aem-outbound-menu.png)

1. 從內容庫中，您可以使用以前配置的模板或從頭建立一個模板。 [了解更多](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

1. 通過將Journey Optimizer個性化語法整合到模板中，您可以增強其自定義功能。 [了解更多](../personalization/personalization-syntax.md)

   ![](assets/aem_ajo_4.png)

1. 選擇要導出到Journey Optimizer的模板，然後按一下 **[!UICONTROL 發送到]** 的子菜單。

   ![](assets/aem-advanced-menu.png)

1. 輸入 **[!UICONTROL 名稱]** ，然後選擇目標 **[!UICONTROL 沙盒]**。

   ![](assets/aem-send-template-settings.png)

1. 按一下後 **[!UICONTROL 發送]** 按鈕，將開始導出過程。 導出完成後，您將在用戶介面中看到以下消息：&quot;模板&quot;XX&quot;已成功發送到AJO&quot;。

該模板將添加到所選沙盒的Adobe Journey Optimizer內容模板。

## 使用並個性化Adobe Experience Manager模板{#aem-templates-perso}

一旦Experience Manager模板在Journey Optimizer作為內容模板可用，您就可以識別並合併電子郵件的必要內容，包括個性化。

1. 在Journey Optimizer, **[!UICONTROL 內容模板]** 的子菜單。

   ![](assets/aem_ajo_1.png)

1. 按一下 **[!UICONTROL 警報]** 按鈕，您可以快速檢查是否缺少任何重要設定。 這將有助於確保正確配置您的消息並防止任何潛在錯誤或問題。

   ![](assets/aem_ajo_2.png)

1. 在 **[!UICONTROL 模板屬性]** 的 **[!UICONTROL 管理訪問]** 按鈕，將自定義或核心資料用法標籤分配給模板。 [瞭解有關對象級訪問控制(OLAC)的詳細資訊](../administration/object-based-access.md)

1. 要進一步個性化您的Experience Manager模板並將自定義個性化添加到您的內容，請按一下 **[!UICONTROL 編輯內容]**。 這樣，您就可以輕鬆進行更改並根據您的特定需求定制模板。 [了解更多](get-started-email-design.md)

   >[!NOTE]
   >
   > 如果要編輯和個性化模板，則只能使用相容模式。

1. 內容模板準備好後， [test並驗證](content-templates.md#test-template)。

1. 定義內容後，您可以通過瀏覽 **[!UICONTROL 保存的模板]** 的下界。 然後，選擇 **[!UICONTROL 使用此模板]**。

   ![](assets/aem_ajo_3.png)

1. 您現在可以編輯和個性化您的內容。 有關如何構建電子郵件內容的詳細資訊，請參閱此 [頁](content-from-scratch.md)。

   ![](assets/aem_ajo_5.png)

1. 如果將個性化內容添加到Experience Manager模板，請按一下 **[!UICONTROL 模擬內容]** 使用test配置檔案預覽消息中的顯示方式。

[瞭解有關預覽和test配置檔案的詳細資訊](../email/preview.md)

   ![](assets/aem_ajo_6.png)

1. 當查看消息預覽時，任何個性化元素將自動替換為來自所選test配置檔案的相應資料。

   如果需要，可通過 **[!UICONTROL 管理test配置檔案]** 按鈕

   ![](assets/aem_ajo_7.png)

當您的電子郵件準備好後，請完成您的 [旅程](../building-journeys/journey-gs.md) 或 [活動](../campaigns/create-campaign.md)，並激活它以發送消息。
