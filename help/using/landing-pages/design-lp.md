---
title: 設計登錄頁面
description: 了解如何在Journey Optimizer中設計登錄頁面的內容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 設計登錄頁面內容 {#design-lp-content}

若要開始從登陸建立內容 [主要頁面](create-lp.md#configure-primary-page) 或 [子頁面](create-lp.md#configure-subpages)，將滑鼠移至主要頁面內容上，然後按一下 **[!UICONTROL Open Designer]**，或按一下右側浮動視窗中的對應按鈕。

![](../assets/lp_open-designer.png)

從那裡，您可以：

* **從草稿開始設計您的登錄頁面** 透過內容設計工具的介面，並運用 [Adobe Experience Manager Assets Essentials](../assets-essentials.md). 了解如何設計內容或使用內建範本 [在本節](../create-email-content.md).

* **程式碼或貼上原始HTML** 直接進入內容設計工具。 了解如何編寫您自己的內容 [在本節](../existing-content.md#import-raw-html-code).

* **匯入現有HTML內容** 或.zip資料夾。 了解如何匯入內容 [在本節](../existing-content.md#import-html-content-from-file).

>[!NOTE]
>
>登錄頁面內容設計工具大多與電子郵件設計工具類似。 進一步了解如何使用 [!DNL Journey Optimizer] [此處](../design-emails.md).

若要定義登錄頁面特定內容，請遵循下列步驟。

1. 拖放登錄頁面專用 **[!UICONTROL Form]** 元件從左側浮動視窗移入主工作區。

   ![](../assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL Form]** 元件在相同頁面上只能使用一次。

1. 請選取模式。此 **[!UICONTROL Form content]** 標籤會顯示在右側浮動視窗中，讓您編輯表單的不同欄位。

   ![](../assets/lp_designer-form-content-options.png)

1. 從 **[!UICONTROL Checkbox 1]** 區段中，您可以編輯與此核取方塊對應的標籤。

1. 定義此核取方塊是要選擇使用者加入或退出：他們是否同意接收通信？還是要求不再聯繫？

   ![](../assets/lp_designer-form-update.png)

1. 在下列三個選項之間選擇要更新的項目：

   ![](../assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Subscription list]**:如果配置檔案選中此複選框，則必須選擇要更新的訂閱清單。 進一步了解 [本節](subscription-list.md).

      ![](../assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Channel (email)]**:選擇加入或選擇退出會套用至整個管道。 例如，如果選擇退出的設定檔有兩個電子郵件地址，則這兩個地址都將從您的所有通訊中排除。

   * **[!UICONTROL Email entity]**:選擇加入或選擇退出僅適用於用來存取登錄頁面的電子郵件地址。 例如，如果設定檔有兩個電子郵件地址，則只有用來選擇加入的電子郵件地址才會收到來自您品牌的通訊。

1. 按一下 **[!UICONTROL Add field]** > **[!UICONTROL Checkbox]** 添加其他複選框。 重複上述步驟以定義其屬性。

   ![](../assets/lp_designer-form-checkbox-2.png)

1. 按一下 **[!UICONTROL Call to action]** 以展開對應的區段。 它可讓您定義 **[!UICONTROL Form]** 元件。

   ![](../assets/lp_designer-form-call-to-action.png)

1. 定義按一下按鈕後將發生的事項：

   * **[!UICONTROL Redirect URL]**:輸入將使用者重新導向的頁面URL。
   * **[!UICONTROL Confirmation text]**:輸入將顯示的確認文本。
   * **[!UICONTROL Link to a subpage]**:設定 [子頁面](create-lp.md#configure-subpages) 並從顯示的下拉式清單中選取。

   ![](../assets/lp_designer-form-confirmation-action.png)

1. 定義發生錯誤時按一下按鈕後會發生什麼事：

   * **[!UICONTROL Redirect URL]**:輸入將使用者重新導向的頁面URL。
   * **[!UICONTROL Error text]**:輸入將顯示的錯誤文本。 您可以選取對應的核取方塊來預覽錯誤文字。

      ![](../assets/lp_designer-form-error-preview.png)

   * **[!UICONTROL Link to a subpage]**:設定 [子頁面](create-lp.md#configure-subpages) 並從顯示的下拉式清單中選取。

1. 如果要在提交表單時進行其他更新，請選擇 **[!UICONTROL Opt in]** 或 **[!UICONTROL Opt out]**，並定義您是否要更新訂閱清單、通道或僅使用的電子郵件地址。

   ![](../assets/lp_designer-form-additionnal-update.png)

1. 儲存您的內容，然後按一下頁面名稱旁的箭頭，返回 [登陸頁面屬性](create-lp.md#configure-primary-page).

   ![](../assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->


