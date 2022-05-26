---
title: 定義特定於登錄頁的內容
description: 瞭解如何在Journey Optimizer設計登錄頁特定內容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
source-git-commit: f4b3a9de47e724f7b23df8a02b8106c131cf1b12
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 2%

---

# 定義特定於登錄頁的內容 {#lp-content}

要定義特定內容，使用戶能夠從登錄頁中選擇和提交其選擇，請使用 **[!UICONTROL Form]** 元件。 為此，請執行以下步驟。

>[!NOTE]
>
>您還可以建立按一下瀏覽登錄頁， **[!UICONTROL Form]** 元件。 在這種情況下，登錄頁將顯示給用戶，但用戶無需提交任何表單。 如果您只想顯示登錄頁而不需要收件人執行任何操作（如選擇加入或選擇退出），或想提供不需要用戶輸入的資訊，則此功能非常有用。

## 使用窗體元件 {#use-form-component}

1. 拖放特定於登錄頁的 **[!UICONTROL Form]** 元件從左調色板移入主工作區。

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL Form]** 元件只能在同一頁上使用一次。

1. 請選取模式。的 **[!UICONTROL Form content]** 頁籤中，您可以編輯窗體的不同欄位。

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >切換到 **[!UICONTROL Form style]** 的子菜單。 [了解更多](#define-lp-styles)

1. 從 **[!UICONTROL Checkbox 1]** 部分，可編輯與此複選框對應的標籤。

1. 定義此複選框是選擇用戶加入還是退出：他們是同意接收通信，還是要求不再聯繫？

   ![](assets/lp_designer-form-update.png)

   從以下三個選項中選擇：

   * **[!UICONTROL Opt in if checked]**:用戶需要選中該框才能同意（選擇加入）。
   * **[!UICONTROL Opt out if checked]**:用戶需要選中該框以刪除其同意（選擇退出）。
   * **[!UICONTROL Opt in if checked, opt out if unchecked]**:此選項允許您插入一個選中/選中退出複選框。 使用者需要勾選方塊同意 (選擇加入)，並取消勾選方塊移除其同意 (選擇退出)。 

1. 選擇以下三個選項之間將更新的內容：

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Subscription list]**:如果配置檔案選中此複選框，則必須選擇將更新的訂閱清單。 瞭解更多 [訂閱清單](subscription-list.md)。

      ![](assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Channel (email)]**:選擇加入或選擇退出適用於整個頻道。 例如，如果一個開啟的配置檔案有兩個電子郵件地址，則這兩個地址將從您的所有通信中排除。

   * **[!UICONTROL Email identity]**:選擇加入或選擇退出僅適用於用於訪問登錄頁的電子郵件地址。 例如，如果一個配置檔案有兩個電子郵件地址，則只有用於選擇加入的電子郵件地址才會從您的品牌接收通信。

1. 按一下 **[!UICONTROL Add field]** > **[!UICONTROL Checkbox]** 複選框。 重複上述步驟以定義其屬性。

   ![](assets/lp_designer-form-checkbox-2.png)

1. 添加所有所需複選框後，按一下 **[!UICONTROL Call to action]** 展開相應的部分。 它使您能夠定義 **[!UICONTROL Form]** 元件。

   ![](assets/lp_designer-form-call-to-action.png)

1. 定義按一下按鈕後將發生的情況：

   * **[!UICONTROL Redirect URL]**:輸入用戶將重定向到的頁面的URL。
   * **[!UICONTROL Confirmation text]**:鍵入將顯示的確認文本。
   * **[!UICONTROL Link to a subpage]**:配置 [子頁](create-lp.md#configure-subpages) 並從顯示的下拉清單中選擇它。

   ![](assets/lp_designer-form-confirmation-action.png)

1. 定義在發生錯誤時按一下按鈕時將發生的情況：

   * **[!UICONTROL Redirect URL]**:輸入用戶將重定向到的頁面的URL。
   * **[!UICONTROL Error text]**:鍵入將顯示的錯誤文本。 定義錯誤文本時，可以預覽錯誤文本 [樣式](#define-lp-styles)。

   * **[!UICONTROL Link to a subpage]**:配置 [子頁](create-lp.md#configure-subpages) 並從顯示的下拉清單中選擇它。

   ![](assets/lp_designer-form-error.png)

1. 如果要在提交表單時進行其他更新，請選擇 **[!UICONTROL Opt in]** 或 **[!UICONTROL Opt out]**，並定義要更新訂閱清單、渠道還是僅使用的電子郵件地址。

   ![](assets/lp_designer-form-additionnal-update.png)

1. 保存您的內容，然後按一下頁面名稱旁的箭頭返回至 [登錄頁屬性](create-lp.md#configure-primary-page)。

   ![](assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->

## 定義登錄頁表單樣式 {#lp-form-styles}

1. 要修改窗體元件內容的樣式，請隨時切換到 **[!UICONTROL Form style]** 頁籤。

   ![](assets/lp_designer-form-style.png)

1. 展開 **[!UICONTROL Checkboxes]** 的子菜單。 例如，可以調整字型系列或大小以及複選框邊框顏色。

   ![](assets/lp_designer-form-style-checkboxes.png)

1. 展開 **[!UICONTROL Buttons]** 按鈕。 例如，可以添加邊框、在懸停時編輯標籤顏色或調整按鈕的對齊方式。

   ![](assets/lp_designer-form-style-buttons.png)

   使用 **[!UICONTROL Preview]** 按鈕 瞭解有關測試登錄頁的詳細資訊 [這裡](create-lp.md#test-landing-page)。

   ![](assets/lp_designer-form-style-buttons-preview.png)

1. 展開 **[!UICONTROL Form layout]** 的子菜單。

   ![](assets/lp_designer-form-style-layout.png)

1. 展開 **[!UICONTROL Form error]** 的子菜單。 選中相應選項以預覽窗體上的錯誤文本。

   ![](assets/lp_designer-form-error-preview.png)

