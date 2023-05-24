---
solution: Journey Optimizer
product: journey optimizer
title: 建立內容範本
description: 瞭解如何建立模板以重用Journey Optimizer市場活動和旅程中的內容
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 327de13a-1c99-4d5e-86cf-8180fb7aaf23
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 12%

---

# 使用內容模板 {#content-templates}

為了加快和改進設計過程，您可以建立獨立模板，以便跨整個系統輕鬆地重複使用自定義內容 [!DNL Journey Optimizer] 活動和旅程。

此功能使面向內容的用戶能夠在市場活動或行程之外使用模板。 然後，市場營銷用戶可以在其自己的行程或市場活動中重複使用和調整這些獨立內容模板。

例如，您公司內的用戶僅負責內容，因此無法訪問市場活動或旅程。 但是，此用戶可以建立一個電子郵件模板，您的組織的營銷人員將能夠選擇該模板以用於所有電子郵件作為起點。

➡️ [瞭解如何在此視頻中建立和使用模板](#video-templates)

>[!CAUTION]
>
>要建立、編輯和刪除內容模板，必須 **[!DNL Manage Library Items]** 包含在 **[!DNL Content Library Manager]** 產品配置檔案。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)

## 訪問和管理模板 {#access-manage-templates}

要訪問內容模板清單，請選擇 **[!UICONTROL 內容管理]** > **[!UICONTROL 內容模板]** 的下界。

![](assets/content-template-list.png)

在當前沙箱上建立的所有模板 — 無論是從行程還是使用 [另存為模板](#save-as-template) 選項 **[!UICONTROL 內容模板]** 按鈕。

您可以按建立或修改日期對內容模板進行排序。 也可以選擇只顯示您建立或修改的項目。

![](assets/content-template-list-filters.png)

要編輯模板內容，請按一下清單中的所需項，然後選擇 **[!UICONTROL 編輯內容]**。

![](assets/content-template-list-edit.png)

要刪除模板，請選擇所需模板旁邊的資源回收筒表徵圖。

![](assets/content-template-list-delete.png)

>[!NOTE]
>
>編輯或刪除模板時，市場活動或旅程（包括使用此模板建立的電子郵件）不會受到影響。

## 建立內容範本 {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="定義您自己的內容範本"
>abstract="從頭開始建立獨立的自訂範本，使得您的內容可在多個歷程和行銷活動中重複使用。"

有兩種方法可以建立內容模板：

* 使用左滑軌從頭建立內容模板 **[!UICONTROL 內容模板]** 的子菜單。 [了解作法](#create-template-from-scratch)

* 在市場活動或行程中設計電子郵件時，請將您的電子郵件內容另存為模板。 [了解作法](#save-as-template)

保存後，您的內容模板可用於市場活動或旅程。 無論是從頭建立還是從以前的電子郵件建立，現在都可以在生成任何 [電子郵件](get-started-email-design.md) 內 [!DNL Journey Optimizer]。 [了解作法](email-templates.md)

>[!NOTE]
>
>* 對內容模板所做的更改不會傳播到市場活動或旅程，無論它們是即時的還是草稿。
>
>* 同樣，當模板在市場活動或行程中使用時，您對市場活動和行程內容所做的任何編輯都不會影響以前使用的內容模板。


### 從頭建立模板 {#create-template-from-scratch}

要從頭開始建立內容模板，請執行以下步驟。

1. 通過 **[!UICONTROL 內容管理]** > **[!UICONTROL 內容模板]** 的子菜單。

   ![](assets/content-template-list.png)

1. 選擇 **[!UICONTROL 建立模板]**。

1. 填寫模板詳細資訊。

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >當前僅 **電子郵件** 頻道和 **HTML** 類型。

1. 要將自定義或核心資料使用標籤分配給模板，請選擇 **[!UICONTROL 管理訪問]**。 [瞭解有關對象級訪問控制(OLAC)的詳細資訊](../administration/object-based-access.md)。

1. 按一下 **[!UICONTROL 建立]** 並從不同的選項中選擇您設計電子郵件的方式：

   * [從頭開始設計電子郵件](content-from-scratch.md) 通過電子郵件設計器的介面。

   * [代碼或複製 — 貼上原始HTML](code-content.md) 直接輸入到電子郵件設計器中。

   * 從檔案或 .zip 資料夾[匯入現有 HTML 內容](existing-content.md)。

   * 使用內置模板或自定義模板清單中的現有內容。 有關在電子郵件中使用內容模板的步驟，請參見 [此部分](email-templates.md)。

   ![](assets/content-template-design.png)

1. 的 [電子郵件設計器](get-started-email-design.md) 顯示。 根據您選擇的選項，根據需要編輯您的內容，與您對行程或市場活動中的任何電子郵件所做的操作相同。

   如果需要，您可以test內容。 [了解作法](#test-template)

1. 模板準備好後，按一下 **[!UICONTROL 保存]**。

1. 如果需要，按一下模板名稱旁的箭頭返回到 **[!UICONTROL 詳細資訊]** 並編輯模板。

   ![](assets/content-template-designer-back.png)

此模板現在已準備好在中生成任何電子郵件時使用 [!DNL Journey Optimizer]。 [了解作法](email-templates.md)

### 另存為範本 {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="了解如何移轉訊息"
>abstract="在 2022 年 7 月 25 日，「訊息」選單已消失，現在會直接從歷程編寫訊息。如果您要在歷程中重複使用舊訊息，則需要將它們另存為範本。"

設計 [電子郵件](get-started-email-design.md) 在市場活動或旅途中，您可以保存電子郵件內容以供將來重新使用。 請依照下列步驟以執行此操作。

1. 在電子郵件設計器中，按一下螢幕右上角的省略號。

1. 選擇 **[!UICONTROL 另存為內容模板]** 的下界。

   ![](assets/email_designer-save-template.png)

1. 為此模板添加名稱和說明。

   ![](assets/email_designer-template-name.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

1. 模板將保存到 **[!UICONTROL 內容模板]** 清單，可從 [!DNL Journey Optimizer] 專用菜單。 它成為可以訪問、編輯和刪除的獨立內容模板，與該清單上的任何其他項目一樣。 [了解更多](#access-manage-templates)

現在，在生成任何 [電子郵件](get-started-email-design.md) 內 [!DNL Journey Optimizer]。 [了解作法](email-templates.md)

>[!NOTE]
>
>對該新模板的任何更改都不會傳播到其來源的電子郵件。 同樣，當在該電子郵件中編輯原始內容時，不會修改新模板。

## Test內容模板 {#test-template}

您可以test任何電子郵件內容模板的呈現，無論是從頭建立還是從電子郵件建立。 為此，請執行以下步驟。

>[!CAUTION]
>
>要模擬內容，您必須 **[!DNL Manage Simulate Content]** 包含在 **[!DNL Content Library Manager]** 產品配置檔案。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)

1. 通過 **[!UICONTROL 內容管理]** > **[!UICONTROL 內容模板]** ，然後選擇任何模板。

1. 按一下 **[!UICONTROL 編輯內容]** 從 **[!UICONTROL 模板屬性]**。

1. 按一下 **[!UICONTROL 模擬內容]** 並選擇test配置檔案以檢查電子郵件呈現。 您可以選擇桌面或行動檢視。[了解更多](preview.md)

   ![](assets/content-template-stimulate.png)

1. 您可以發送證據來test您的內容，並且在旅途或市場活動中使用之前，已經獲得一些內部用戶的批准。

   * 為此，請按一下 **[!UICONTROL 發送證明]** 按鈕並遵循中介紹的步驟 [此部分](preview.md#send-proofs)。

   * 在發送證明之前，必須選擇 [電子郵件曲面](../configuration/channel-surfaces.md) 用於test內容。

      ![](assets/content-template-stimulate-proof-surface.png)

## 操作說明影片 {#video-templates}

瞭解如何在中建立、編輯和使用內容模板 [!DNL Journey Optimizer]。

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)
