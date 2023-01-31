---
solution: Journey Optimizer
product: journey optimizer
title: 建立內容範本
description: 了解如何建立範本，以重複使用Journey Optimizer行銷活動和歷程中的內容
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 1%

---

# 建立內容範本 {#content-templates}

>[!CONTEXTUALHELP]
>id="ajo_content_templates"
>title="建立內容範本"
>abstract="建立獨立範本，以重設歷程和行銷活動中的內容。"

為加快和改善設計流程，您可以建立獨立範本，以輕鬆在 [!DNL Journey Optimizer] 行銷活動和歷程。

此功能可讓內容導向的使用者在行銷活動或歷程之外處理範本。 然後，行銷使用者可以在自己的歷程或行銷活動中重複使用和調整這些獨立內容範本。

>[!CAUTION]
>
>若要建立、編輯和刪除內容範本，您必須具備 **[!DNL Manage Library Items]** 包含在 **[!DNL Content Library Manager]** 產品設定檔。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)

例如，您公司內的使用者只負責內容，因此無法存取促銷活動或歷程。 不過，此使用者可以建立電子郵件範本，供您組織的行銷人員選取，以便用於所有電子郵件。

>[!NOTE]
>
>* 對內容範本所做的變更不會傳播至行銷活動或歷程，無論是即時或草稿。
>
>* 同樣地，當範本用於促銷活動或歷程時，您對促銷活動和歷程內容所做的任何編輯都不會影響先前使用的內容範本。


➡️ [了解如何在此影片中建立和使用範本](#video-templates)

若要建立內容範本，請遵循下列步驟。

1. 若要存取內容範本清單，請選取 **[!UICONTROL 內容管理]** > **[!UICONTROL 內容範本]** 的上界。

   ![](assets/content-template-list.png)

1. 在目前沙箱中建立的所有範本(來自歷程、行銷活動或 **[!UICONTROL 內容範本]** 功能表。

   >[!NOTE]
   >
   >您可以依建立或修改日期來排序內容範本。

1. 選擇 **[!UICONTROL 建立範本]**.

1. 填寫範本詳細資訊。

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >目前僅 **電子郵件** 頻道和 **HTML** 支援類型。

1. 若要將自訂或核心資料使用量標籤指派至範本，請選取 **[!UICONTROL 管理存取]**. [進一步了解物件層級存取控制(OLAC)](../administration/object-based-access.md).

1. 按一下 **[!UICONTROL 建立]** 並從下列選項中選擇您設計電子郵件的方式：

   * **[!UICONTROL 從頭設計]**
   * **[!UICONTROL 自行編碼]**
   * **[!UICONTROL 匯入HTML]**
   * **[!UICONTROL 選取設計範本]**

   ![](assets/content-template-design.png)

   >[!NOTE]
   >
   >如果您選取範本，可以在 **[!UICONTROL 範本範例]**，這些是現成可用的電子郵件範本，以及 **[!UICONTROL 已儲存的範本]**，這些是從歷程、行銷活動或從 **[!UICONTROL 內容範本]** 功能表。 [了解更多](email-templates.md#save-as-template)

1. 電子郵件設計工具隨即顯示。 視需要編輯內容，與您針對歷程或行銷活動內任何電子郵件所執行的相同方式，根據您選取的選項：

   * [從草稿開始設計您的電子郵件](content-from-scratch.md) 透過設計人員的介面，並運用 [Adobe Experience Manager Assets Essentials](assets-essentials.md).

   * [程式碼或複製貼上原始HTML](code-content.md) 直接進入電子郵件設計工具。

   * [匯入現有HTML內容](existing-content.md) 或.zip資料夾。

   * [使用現有內容](email-templates.md) 從內建或自訂範本的清單。

   ![](assets/content-template-designer.png)

1. 按一下 **[!UICONTROL 模擬內容]** 檢查電子郵件呈現。 您可以選擇案頭或行動檢視。 [了解更多](preview.md)

   >[!CAUTION]
   >
   >若要模擬內容，您必須具備 **[!DNL Manage Simulate Content]** 包含在 **[!DNL Content Library Manager]** 產品設定檔。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)

   ![](assets/content-template-stimulate.png)

1. 您可以在歷程或行銷活動中使用內容之前，先傳送校樣以測試內容，並讓部分內部使用者核准。

   * 若要這麼做，請按一下 **[!UICONTROL 傳送校樣]** 按鈕，並遵循 [本節](preview.md#send-proofs).

   * 傳送校樣之前，您必須選取 [電子郵件表面](../configuration/channel-surfaces.md) 會用來測試您的內容。

      ![](assets/content-template-stimulate-proof-surface.png)

1. 範本準備就緒後，按一下 **[!UICONTROL 儲存]**.

1. 如有需要，按一下範本名稱旁的箭頭，返回 **[!UICONTROL 詳細資料]** 畫面並編輯範本。

   ![](assets/content-template-designer-back.png)

1. 您現在可以在建立任何 [電子郵件](get-started-email-design.md) with [!DNL Journey Optimizer]. 深入了解 [使用已儲存的範本](email-templates.md#use-saved-template).

   ![](assets/email_designer-saved-templates.png)

## 作法影片{#video-templates}

了解如何在 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)