---
solution: Journey Optimizer
product: journey optimizer
title: 在Journey Optimizer中從頭開始設計內容
description: 瞭解如何從頭開始設計內容
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 內容，編輯器，電子郵件，開始
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 3f363a006ed25c07f3ea5b516f5fc306b230d029
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 49%

---

# 使用電子郵件設計工具從頭開始設計內容 {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="新增結構元件"
>abstract="結構元件會定義電子郵件的版面。將&#x200B;**結構**&#x200B;元件拖放到畫布中開始設計您的電子郵件內容。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="新增結構元件"
>abstract="結構元件會定義登陸頁面的版面。將&#x200B;**結構**&#x200B;元件拖放到畫布中開始設計您的登入頁面內容。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="新增結構元件"
>abstract="結構元件會定義區段的版面。將&#x200B;**結構**&#x200B;元件拖放到畫布中開始設計您的片段內容。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="新增結構元件"
>abstract="結構元件會定義範本的版面。將&#x200B;**結構**&#x200B;元件拖放到畫布中開始設計您的範本內容。"


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="定義電子郵件欄"
>abstract="電子郵件設計工具可讓您透過選取欄結構輕鬆定義電子郵件的版面。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="定義登陸頁面欄"
>abstract="Designer 可讓您透過選取欄結構輕鬆定義登陸頁面的版面。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="定義片段欄"
>abstract="Designer 可讓您透過選取欄結構輕鬆定義片段的版面。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="定義範本欄"
>abstract="Designer 可讓您透過選取欄結構輕鬆定義範本的版面。"


使用[!DNL Adobe Journey Optimizer]電子郵件Designer以輕鬆定義內容結構。 透過使用簡單的拖放動作新增和移動結構元素，您可以在數秒內設計內容的形狀。

>[!NOTE]
>
>[歐洲無障礙法案](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"}規定所有數位通訊都應該能透過無障礙方式取得。在[中設計內容時，請務必遵循](accessible-content.md)此頁面[!DNL Journey Optimizer]上列出的特定准則。

若要開始建立您的內容，請遵循下列步驟：

1. 從Designer首頁，選取&#x200B;**[!UICONTROL 從頭開始設計]**&#x200B;選項。

   ![](assets/email_designer.png)


1. 使用AI Assistant加速電子郵件建立，並使用[AI Assistant產生包含文字和影像的完整電子郵件內容，以進行完整內容產生](../content-management/generative-full-content.md)。

1. 將&#x200B;**[!UICONTROL Structures]**&#x200B;拖放到畫布中，以定義電子郵件的配置，開始設計您的內容。

   >[!NOTE]
   >
   >堆疊欄與所有電子郵件程式都不相容。當不支援時，欄將不會棧疊。

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. 視需要新增多個&#x200B;**[!UICONTROL 結構]**，並在右側的專用窗格中編輯其設定。

   ![](assets/email_designer_structure_components.png)

   選取&#x200B;**[!UICONTROL n:n資料行]**&#x200B;元件以定義您所選擇的資料行數目（介於3到10之間）。 您也可以移動每個欄底部的箭頭來定義其寬度。

   >[!NOTE]
   >
   >每個欄的大小不能小於結構元件總寬度的 10%。如果欄不是空的，則無法移除。

1. 展開&#x200B;**[!UICONTROL 內容]**&#x200B;區段，並新增您所需數量的元素至一或多個結構元件。 [進一步了解內容元件](content-components.md)

1. 每個元件都可以使用右方功能表中的&#x200B;**[!UICONTROL 設定]**&#x200B;或&#x200B;**[!UICONTROL 樣式]**&#x200B;標籤進一步自訂。 例如，您可以變更每個元件的文字樣式、邊框間距或邊界。[了解對齊方式和邊框間距的詳細資訊](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. 您可以從&#x200B;**[!UICONTROL 資產選擇器]**&#x200B;直接選取儲存在&#x200B;**[!UICONTROL Assets資料庫]**&#x200B;中的資產。 [進一步瞭解資產管理](../integrations/assets.md)

   連按兩下包含資產的資料夾。 將其拖放至結構元件中。

   ![](assets/email_designer_asset_picker.png)

1. 插入個人化欄位，從設定檔屬性、對象成員資格、內容屬性等自訂內容。 [進一步了解內容個人化](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. 按一下&#x200B;**[!UICONTROL 啟用條件內容]**&#x200B;以新增動態內容，並根據條件規則將內容調整至目標設定檔。 [開始使用動態內容](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. 從左窗格按一下&#x200B;**[!UICONTROL 連結]**&#x200B;索引標籤，以顯示您要追蹤之內容的所有URL。 您可以修改其&#x200B;**[!UICONTROL 追蹤型別]**&#x200B;或&#x200B;**[!UICONTROL 標籤]**，並視需要新增&#x200B;**[!UICONTROL 標籤]**。 [進一步瞭解連結和追蹤](message-tracking.md)

   ![](assets/email_designer_links.png)

1. 如果需要，您可以按一下「進階」選單中的「**[!UICONTROL 切換到程式碼編輯器]**」進一步個人化您的電子郵件。這可讓您編輯電子郵件原始碼，例如新增追蹤或自訂 HTML 標記。[進一步了解程式碼編輯器](code-content.md)

   >[!CAUTION]
   >
   >切換到程式碼編輯器後，您無法恢復到此電子郵件的視覺化設計工具。

1. 內容準備就緒後，按一下&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕以檢查轉譯。 您可以選擇桌面或行動檢視。有關如何選取測試設定檔及預覽內容的詳細資訊，請參閱[內容管理](../content-management/preview-test.md)區段。

   ![](assets/email_designer_simulate_content.png)

1. 您也可以驗證內容品質，以評估可讀性、有效性和內容一致性。 [進一步瞭解內容品質驗證](../content-management/brands-score.md#validate-quality)

1. 當您的內容準備就緒時，請按一下[儲存]。****
