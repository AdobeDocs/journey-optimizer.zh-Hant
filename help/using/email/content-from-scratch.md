---
solution: Journey Optimizer
product: journey optimizer
title: 在Journey Optimizer中設計電子郵件
description: 了解如何從草稿開始設計您的電子郵件內容
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 1%

---

# 從頭開始 {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="關於結構元件"
>abstract="結構元件可定義電子郵件的版面。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="關於結構元件"
>abstract="結構元件會定義登錄頁面的配置。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="關於結構元件"
>abstract="結構元件定義片段的佈局。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="關於結構元件"
>abstract="結構元件定義模板的佈局。"


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="定義電子郵件欄"
>abstract="電子郵件設計工具可讓您透過定義欄結構來輕鬆定義電子郵件的版面。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="定義登錄頁面欄"
>abstract="電子郵件設計工具可讓您透過定義欄結構來輕鬆定義登錄頁面的版面。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="定義片段欄"
>abstract="電子郵件設計工具可讓您透過定義欄結構來輕鬆定義片段的版面。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="定義範本欄"
>abstract="電子郵件設計工具可讓您透過定義欄結構來輕鬆定義範本的版面。"


電子郵件設計工具可讓您輕鬆定義電子郵件的結構。 透過新增和移動結構元素並執行簡單的拖放動作，您可以在數秒內設計電子郵件的形狀。

若要開始建立電子郵件內容，請遵循下列步驟：

1. 從電子郵件設計工具首頁中，選取 **[!UICONTROL 從頭設計]** 選項。

   ![](assets/email_designer.png)

1. 透過拖放功能，開始設計電子郵件內容 **[!UICONTROL 結構元件]** 填入畫布以定義電子郵件的版面。

   >[!NOTE]
   >
   >堆疊欄與所有電子郵件程式不相容。 不支援時，不會堆疊欄。

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. 新增最多 **[!UICONTROL 結構元件]** 視需要，並在右側的專用窗格中編輯其設定。

   ![](assets/email_designer_structure_components.png)

   選取 **[!UICONTROL n:n欄]** 元件，定義您選取的欄數（介於3和10之間）。 您也可以移動每欄底部的箭頭，以定義每欄的寬度。

   ![](assets/email_designer_structure_n-n-colum.png)

   >[!NOTE]
   >
   >每個列大小不能低於結構元件總寬度的10%。 無法刪除非空的列。

1. 展開 **[!UICONTROL 內容元件]** 區段，並視需要新增多個元素至一或多個結構元件。 [深入了解內容元件](content-components.md)

1. 每個元件可透過 **[!UICONTROL 元件設定]** 窗格。 例如，您可以變更每個元件的文字樣式、邊框間距或邊界。 [進一步了解對齊方式和邊框間距](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. 從 **[!UICONTROL 資產選擇器]**，您可以直接選取儲存在中的資產 **[!UICONTROL Assets資料庫]**. [深入了解資產管理](assets-essentials.md)

   連按兩下包含資產的資料夾。 將它們拖放到結構元件中。

   ![](assets/email_designer_asset_picker.png)

1. 插入個人化欄位，以從設定檔資料自訂您的電子郵件內容。 [深入了解內容個人化](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. 新增動態內容，以根據條件規則調整內容以符合目標設定檔。 [開始使用動態內容](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. 按一下 **[!UICONTROL 連結]** 標籤，以顯示要追蹤之內容的所有URL。 您可以修改其 **[!UICONTROL 追蹤類型]** 或 **[!UICONTROL 標籤]** 新增 **[!UICONTROL 標籤]** 如有需要。 [深入了解連結和訊息追蹤](message-tracking.md)

   ![](assets/email_designer_links.png)

1. 如有需要，您可以按一下 **[!UICONTROL 切換至程式碼編輯器]** 的上界。 [進一步了解程式碼編輯器](code-content.md)

   ![](assets/email_designer_switch-to-code.png)

   >[!CAUTION]
   >
   >切換到代碼編輯器後，您將無法回復到此電子郵件的可視設計器。

1. 內容準備就緒後，按一下 **[!UICONTROL 模擬內容]** 檢查電子郵件呈現。 您可以選擇案頭或行動檢視。 [進一步了解如何預覽您的電子郵件](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. 當您的電子郵件準備就緒時，按一下 **[!UICONTROL 儲存]**.

