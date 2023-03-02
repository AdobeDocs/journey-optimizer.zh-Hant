---
solution: Journey Optimizer
product: journey optimizer
title: 使用AEM範本
description: 了解如何在AEM中建立範本，並將其匯出至Journey Optimizer
hide: true
hidefromtoc: true
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informity"
source-git-commit: c909e366ba5e911f685656140caf53cc122552ee
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 1%

---

# 使用Adobe Experience Manager範本 {#aem-templates}

>[!AVAILABILITY]
>
>目前，與Adobe Experience Manager的整合僅供選取的使用者測試版使用。
> 身為測試版使用者，請使用 [此表單](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} 分享意見。

透過Adobe Journey Optimizer，您可以透過Adobe Experience Manager網站建立自訂量身打造的訊息。 首先，使用Adobe Experience Manager的內容來源設計範本，然後將其傳送至Adobe Journey Optimizer。 共用後，您就可以在Adobe Journey Optimizer的電子郵件設計工具中存取這些範本，簡化建立訊息並傳送訊息給所需對象的程式。

## 先決條件 {#prerequisites}

開始使用此功能之前，請務必符合下列需求：

* **Experience Manager設定**

   自Adobe Experience Manager 6.5.14開始，即可使用此功能。您必須在Managed Services製作環境中連線至Adobe Experience Manager Sites。

   測試版程式中，Cloud Service設定是由Adobe Experience Manager中的Adobe執行，以連線至Adobe Journey Optimizer。

* **權限**

   若要在Adobe Journey Optimizer中建立、編輯和刪除內容範本，您必須具備 **[!DNL Manage Library Items]** 包含在 **[!DNL Content Library Manager]** 產品設定檔。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)


## 護欄和限制{#aem-templates-limitations}

若要進一步最佳化您搭配Adobe Journey Optimizer使用Adobe Experience Manager的方式，請務必注意下列額外護欄和限制：

* Experience Manager範本不得包含個人化。 個人化僅應在Journey Optimizer中執行。

* 目前不支援大量範本匯出，必須個別匯出範本。

* 目前無法同步Experience Manager和Journey Optimizer。 如果在將Experience Manager範本傳送至Journey Optimizer後對其進行變更，使用者將需要重新匯出範本，並將其重新傳送至Journey Optimizer。

## 傳送範本至Journey Optimizer{#aem-templates-send}

若要將Adobe Experience Manager範本匯出至Adobe Journey Optimizer，請遵循下列步驟：

1. 從Adobe Experience Manager首頁，選取 **[!UICONTROL 對外行銷]**.

   ![](assets/aem-outbound-menu.png)

1. 存取您的內容庫，並選取您要匯出至Journey Optimizer的範本。

   您也可以從草稿開始建立新頁面。 [了解更多](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

   ![](assets/aem-send-template.png)

1. 選取範本後，請選取 **[!UICONTROL 傳送至]** 的上界。

   ![](assets/aem-advanced-menu.png)

1. 輸入 **[!UICONTROL 名稱]** ，然後選取目標 **[!UICONTROL 沙箱]**.

   ![](assets/aem-send-template-settings.png)

1. 在您按一下 **[!UICONTROL 傳送]** 按鈕，則會開始匯出程式。 匯出完成後，您會在使用者介面中看到下列訊息：&quot;模板&quot;XX&quot;已成功發送到AJO&quot;。

範本會新增至所選沙箱的Adobe Journey Optimizer內容範本。

## 使用並個人化Adobe Experience Manager範本{#aem-templates-perso}

在Journey Optimizer中提供Experience Manager範本作為內容範本後，您就可以識別並納入電子郵件的必要內容，包括個人化內容。

1. 在Journey Optimizer，從 **[!UICONTROL 內容範本]** 功能表，存取匯入的範本。

   ![](assets/aem_ajo_1.png)

1. 按一下 **[!UICONTROL 警報]** 按鈕，您可以快速檢查是否缺少任何重要設定。 這將有助於確保您的訊息已正確設定，並防止任何可能的錯誤或問題。

   ![](assets/aem_ajo_2.png)

1. 在「模板屬性」窗口中，按一下 **[!UICONTROL 管理存取]** 按鈕，將自訂或核心資料使用量標籤指派給範本。 [進一步了解物件層級存取控制(OLAC)](../administration/object-based-access.md)

1. 若要進一步個人化您的AEM範本，並將自訂個人化新增至您的內容，請按一下 **[!UICONTROL 編輯內容]**. 這可讓您輕鬆進行變更，並根據您的特定需求量身打造範本。 [了解更多](get-started-email-design.md)

   >[!NOTE]
   >
   > 如果您想要編輯並個人化範本，則只能使用相容性模式。

1. 當內容範本準備就緒時， [測試和驗證](content-templates.md#test-template).

1. 定義內容後，您就可以瀏覽 **[!UICONTROL 已儲存的範本]** 集合。 然後，選取 **[!UICONTROL 使用此模板]**.

   了解如何在 [本節](content-from-scratch.md).

   ![](assets/aem_ajo_3.png)

當您的電子郵件準備就緒時，請完成 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md)，然後啟用它以傳送訊息。
