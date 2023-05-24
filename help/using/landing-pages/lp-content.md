---
solution: Journey Optimizer
product: journey optimizer
title: 定義特定於登錄頁的內容
description: 瞭解如何在Journey Optimizer設計登錄頁特定內容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: 登錄，登錄頁，建立，頁，表單，元件
exl-id: 5bf023b4-4218-4110-b171-3e70e0507fca
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 11%

---

# 定義特定於登錄頁的內容 {#lp-content}

>[!CONTEXTUALHELP]
>id="ac_lp_components"
>title="使用內容元件"
>abstract="內容元件指可用於建立登陸頁面版面的空白內容預留位置。若要定義讓使用者能夠選取並提交他們的選擇的特定內容，請使用表單元件。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/content-components.html#add-content-components" text="新增內容元件"

要設計登錄頁內容，您可以使用與電子郵件相同的元件。 [了解更多](../email/content-components.md#add-content-components)

要設計特定內容，使用戶能夠選擇和提交其選擇， [使用窗體元件](#use-form-component) 定義 [登錄頁特定樣式](#lp-form-styles)。

>[!NOTE]
>
>您還可以建立按一下瀏覽登錄頁， **[!UICONTROL 窗體]** 元件。 在這種情況下，登錄頁將顯示給用戶，但用戶無需提交任何表單。 如果您只想顯示登錄頁而不需要收件人執行任何操作（如選擇加入或選擇退出），或想提供不需要用戶輸入的資訊，則此功能非常有用。

使用登錄頁內容設計器，您還可以利用子頁中首頁的上下文資料。 [了解更多](#use-primary-page-context)

## 使用窗體元件 {#use-form-component}

>[!CONTEXTUALHELP]
>id="ac_lp_formfield"
>title="設定表單元件欄位"
>abstract="定義您的收件者將如何從您的登陸頁面查看和提交他們的選擇。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/lp-content.html#lp-form-styles" text="定義登陸頁面表單樣式"

>[!CONTEXTUALHELP]
>id="ac_lp_submission"
>title="按一下按鈕時會發生什麼事"
>abstract="定義使用者提交登陸頁面表單後會發生什麼事。"

要定義特定內容，使用戶能夠從登錄頁中選擇和提交其選擇，請使用 **[!UICONTROL 窗體]** 元件。 為此，請執行以下步驟。

1. 拖放特定於登錄頁的 **[!UICONTROL 窗體]** 元件從左調色板移入主工作區。

   ![](assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL 窗體]** 元件只能在同一頁上使用一次。

1. 請選取模式。的 **[!UICONTROL 表單內容]** 頁籤中，您可以編輯窗體的不同欄位。

   ![](assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >切換到 **[!UICONTROL 樣式]** 的子菜單。 [了解更多](#define-lp-styles)

1. 從 **[!UICONTROL 複選框1]** 部分，可編輯與此複選框對應的標籤。

1. 定義此複選框是選擇用戶加入還是退出：他們是同意接收通信，還是要求不再聯繫？

   ![](assets/lp_designer-form-update.png)

   從以下三個選項中選擇：

   * **[!UICONTROL 選中時選擇加入]**:用戶需要選中該框才能同意（選擇加入）。
   * **[!UICONTROL 選中時選擇退出]**:用戶需要選中該框以刪除其同意（選擇退出）。
   * **[!UICONTROL 選中時選擇加入，未選中時選擇退出]**:此選項允許您插入一個選中/選中退出複選框。 使用者需要勾選方塊同意 (選擇加入)，並取消勾選方塊移除其同意 (選擇退出)。 

1. 選擇以下三個選項之間將更新的內容：

   ![](assets/lp_designer-form-update-options.png)

   * **[!UICONTROL 訂閱清單]**:如果配置檔案選中此複選框，則必須選擇將更新的訂閱清單。 瞭解更多 [訂閱清單](subscription-list.md)。

      <!--![](assets/lp_designer-form-subs-list.png)-->

   * **[!UICONTROL 渠道（電子郵件）]**:選擇加入或選擇退出適用於整個頻道。 例如，如果一個開啟的配置檔案有兩個電子郵件地址，則這兩個地址將從您的所有通信中排除。

   * **[!UICONTROL 電子郵件標識]**:選擇加入或選擇退出僅適用於用於訪問登錄頁的電子郵件地址。 例如，如果一個配置檔案有兩個電子郵件地址，則只有用於選擇加入的電子郵件地址才會從您的品牌接收通信。

1. 按一下 **[!UICONTROL 添加欄位]** > **[!UICONTROL 複選框]** 複選框。 重複上述步驟以定義其屬性。

   ![](assets/lp_designer-form-checkbox-2.png)

1. 也可以添加 **[!UICONTROL 文本欄位]**。

   ![](assets/lp_designer-form-add-text-field.png)

   * 輸入 **[!UICONTROL 標籤]** 將在窗體中的欄位頂部顯示。

   * 輸入 **[!UICONTROL 佔位符]** 的子菜單。 在用戶填入欄位之前，它將顯示在欄位內。

   * 檢查 **[!UICONTROL 將表單域設定為必填]** 頁籤 在這種情況下，只有在用戶已填入此欄位時，才能提交登錄頁。 如果未填寫必填欄位，則用戶提交頁面時將顯示錯誤消息。

   ![](assets/lp_designer-form-text-field.png)

1. 添加所有所需複選框和/或文本欄位後，按一下 **[!UICONTROL 行動要求]** 展開相應的部分。 它使您能夠定義 **[!UICONTROL 窗體]** 元件。

   ![](assets/lp_designer-form-call-to-action.png)

1. 定義按一下按鈕後將發生的情況：

   * **[!UICONTROL 重定向URL]**:輸入用戶將重定向到的頁面的URL。
   * **[!UICONTROL 確認文本]**:鍵入將顯示的確認文本。
   * **[!UICONTROL 連結到子頁]**:配置 [子頁](create-lp.md#configure-subpages) 並從顯示的下拉清單中選擇它。

   ![](assets/lp_designer-form-confirmation-action.png)

1. 定義在發生錯誤時按一下按鈕時將發生的情況：

   * **[!UICONTROL 重定向URL]**:輸入用戶將重定向到的頁面的URL。
   * **[!UICONTROL 錯誤文本]**:鍵入將顯示的錯誤文本。 定義錯誤文本時，可以預覽錯誤文本 [樣式](#define-lp-styles)。

   * **[!UICONTROL 連結到子頁]**:配置 [子頁](create-lp.md#configure-subpages) 並從顯示的下拉清單中選擇它。

   ![](assets/lp_designer-form-error.png)

1. 如果要在提交表單時進行其他更新，請選擇 **[!UICONTROL 選擇加入]** 或 **[!UICONTROL 退出]**，並定義要更新訂閱清單、渠道還是僅使用的電子郵件地址。

   ![](assets/lp_designer-form-additionnal-update.png)

1. 保存您的內容，然後按一下頁面名稱旁的箭頭返回至 [登錄頁屬性](create-lp.md#configure-primary-page)。

   ![](assets/lp_designer-form-save.png)

## 定義登陸頁面表單樣式 {#lp-form-styles}

1. 要修改窗體元件內容的樣式，請隨時切換到 **[!UICONTROL 樣式]** 頁籤。

   ![](assets/lp_designer-form-style.png)

1. 的 **[!UICONTROL 欄位]** 部分預設展開，可以編輯文本欄位的外觀，如標籤和佔位符字型、標籤的位置、欄位背景顏色或欄位邊框。

   ![](assets/lp_designer-form-style-fields.png)

1. 展開 **[!UICONTROL 複選框]** 的子菜單。 例如，可以調整字型系列或大小，或者調整複選框邊框顏色。

   ![](assets/lp_designer-form-style-checkboxes.png)

1. 展開 **[!UICONTROL 按鈕]** 按鈕。 例如，您可以更改字型、添加邊框、在懸停時編輯標籤顏色或調整按鈕的對齊方式。

   ![](assets/lp_designer-form-style-buttons.png)

   使用 **[!UICONTROL 模擬內容]** 按鈕 瞭解有關測試登錄頁的詳細資訊 [這裡](create-lp.md#test-landing-page)。

   <!--![](assets/lp_designer-form-style-buttons-preview.png)-->

1. 展開 **[!UICONTROL 窗體佈局]** 的子菜單。

   ![](assets/lp_designer-form-style-layout.png)

1. 展開 **[!UICONTROL 表單錯誤]** 的子菜單。 選中相應選項以預覽窗體上的錯誤文本。

   ![](assets/lp_designer-form-error-preview.png)

## 使用首頁上下文 {#use-primary-page-context}

您可以使用來自同一登錄頁內其他頁的上下文資料。

例如，如果連結複選框 <!-- or the submission of the page--> 到 [訂閱清單](subscription-list.md) 在主登錄頁上，您可以使用「謝謝」子頁上的訂閱清單。

假設您將首頁面上的兩個複選框連結到兩個不同的訂閱清單。 如果用戶訂閱了其中一個，則您希望在提交表單時顯示特定消息，具體取決於他們選中的複選框。

要執行此操作，請遵循下列步驟：

1. 在首頁上，連結 **[!UICONTROL 窗體]** 到相關訂閱清單的元件。 [了解更多](#use-form-component)。

   ![](assets/lp_designer-form-luma-newsletter.png)

1. 在子頁上，將滑鼠指針置於要插入文本的位置並選擇 **[!UICONTROL 添加個性化]** 的子菜單。

   ![](assets/lp_designer-form-subpage-perso.png)

1. 在 **[!UICONTROL 編輯個性化]** 窗口，選擇 **[!UICONTROL 上下文屬性]** > **[!UICONTROL 登錄頁]** > **[!UICONTROL 首頁上下文]** > **[!UICONTROL 訂閱]**。

1. 將列出您在首頁面上選擇的所有訂閱清單。 使用+表徵圖選擇相關項。

   ![](assets/lp_designer-form-add-subscription.png)

1. 使用表達式編輯器幫助函式添加相關條件。 [了解更多](../personalization/functions/functions.md)

   ![](assets/lp_designer-form-add-subscription-condition.png)

   >[!CAUTION]
   >
   >如果表達式中有特殊字元，如連字元，則必須轉義包含連字元的文本。

1. 儲存您的變更。

現在，當用戶選中一個複選框時，

![](assets/lp_designer-form-preview-checked-box.png)

在提交表單時，將顯示與選定複選框對應的消息。

![](assets/lp_designer-form-thankyou-preview.png)

<!--![](assets/lp_designer-form-subscription-preview.png)-->

>[!NOTE]
>
>如果用戶選中兩個複選框，則將顯示兩個文本。

<!--
## Use landing page additional data {#use-additional-data}

When [configuring the primary page](create-lp.md#configure-primary-page), you can create additional data to enable storing information when the landing page is being submitted.

>[!NOTE]
>
>This data may not be visible to users who visit the page.

If you defined one or more keys with their corresponding values when [configuring the primary page](create-lp.md#configure-primary-page), you can leverage these keys in the content of your primary page and subpages using the [Expression editor](../personalization/personalization-build-expressions.md).

///When you reuse the same text on a page, this enables you to dynamically change that text if needed, without going through each occurrence.

For example, if you define the company name as a key, you can quickly update it everywhere (on all the pages of a given landing page) by changing it only once in the [primary page settings](create-lp.md#configure-primary-page).///

To leverage these keys in a landing page, follow the steps below:

1. When configuring the primary page, define a key and its corresponding value in the **[!UICONTROL Additional data]** section. [Learn more](create-lp.md#configure-primary-page)

    ![](assets/lp_create-lp-additional-data.png)

1. When editing your primary page with the designer, place the pointer of your mouse where you want to insert your key and select **[!UICONTROL Add personalization]** from the contextual toolbar.

    ![](assets/lp_designer-context-add-perso.png)

1. In the **[!UICONTROL Edit Personalization]** window, select **[!UICONTROL Contextual attributes]** > **[!UICONTROL Landing Pages]** > **[!UICONTROL Additional Context]**.

    ![](assets/lp_designer-contextual-attributes.png)

1. All the keys that you created when configuring the primary page are listed. Select the key of your choice using the + icon.

    ![](assets/lp_designer-context-select-key.png)

1. Save your changes and repeat the steps above as many times as needed.

    ![](assets/lp_designer-context-keys-inserted.png)

    You can see that the personalization item corresponding to your key is now displayed everywhere you inserted it.
-->