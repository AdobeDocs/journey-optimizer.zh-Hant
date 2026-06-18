---
solution: Journey Optimizer
product: journey optimizer
title: 使用視覺化片段
description: 瞭解如何在Journey Optimizer行銷活動和歷程中建立電子郵件時使用視覺片段
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
TQID: https://experienceleague.adobe.com/YbH8cXjrh5E9v9twpwxB3ENb606W-1JAonJRxnorl9c
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: b5cb2dff-e9ba-4e50-a3eb-6a50eef729b8id: c6e980f5-2d4f-494f-beef-186b9ecf1513id: d08afb72-92f6-4856-88e3-11ec34313c2fid: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 453eb09866109ef5af9f29f1986484e0f6de7040
workflow-type: tm+mt
source-wordcount: 1242
ht-degree: 1%

---

# 在您的電子郵件中新增視覺片段 {#use-visual-fragments}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何在您的電子郵件中插入可重複使用的視覺片段、自訂其可編輯欄位，以及中斷或保留其繼承與原始片段。

>[!ENDSHADEBOX]

片段是可重複使用的元件，可在跨Journey Optimizer行銷活動、歷程或內容範本的一封或多封電子郵件中參考。 此功能允許預先建立多個自訂內容區塊，可供行銷使用者在改良的設計流程中快速組合電子郵件內容。 [瞭解如何建立和管理片段](../content-management/fragments.md)。

➡️ [在此影片中瞭解如何管理、編寫和使用片段](../content-management/fragments.md#video-fragments)

## 使用片段 {#use-fragment}

若要在電子郵件中使用片段，請遵循下列步驟。

>[!NOTE]
>
>您最多可以在給定傳送中新增30個片段。 片段最多只能巢狀1個層級。

1. 使用[電子郵件Designer](get-started-email-design.md)開啟任何電子郵件或範本內容。

1. 從左側邊欄選取&#x200B;**[!UICONTROL 片段]**&#x200B;圖示。

   ![](assets/fragments-in-designer.png)

1. 將會顯示在目前沙箱上建立的所有視覺化片段清單。 它們會依建立日期排序：最近新增的視覺片段會先顯示在清單中。 您可以：

   * 透過開始輸入其標籤來搜尋特定片段。
   * 以遞增或遞減順序排序片段。
   * 變更片段的顯示方式（卡片或清單檢視）。
   * 重新整理清單。

   >[!NOTE]
   >
   >如果您在編輯內容時修改或新增了某些片段，清單會以最新變更更新。

1. 從清單拖放任何片段到您要插入它的區域。

   ![](assets/fragment-insert.png)

   >[!CAUTION]
   >
   >您可以將任何&#x200B;**草稿**&#x200B;或&#x200B;**即時**&#x200B;片段新增至您的內容。 但是，如果正在使用狀態為草稿的片段，您將無法啟用您的歷程或行銷活動。 在歷程或行銷活動發佈中，草稿片段將顯示錯誤，您需要核准它們才能發佈。

1. 如同任何其他元件，您可以在內容中移動片段。

1. 選取片段以在右側顯示對應的窗格。 從那裡，您可以從您的內容中刪除片段或複製它。 您也可以從片段上方顯示的內容功能表直接執行這些動作。

   ![](assets/fragment-right-pane.png)

1. 從&#x200B;**[!UICONTROL 設定]**&#x200B;索引標籤，您可以：

   * 選擇您要顯示片段的裝置。
   * 在新索引標籤中開啟片段，並視需要加以編輯。 [了解更多](../content-management/manage-fragments.md#edit-fragments)
   * 探索引用。 [了解更多](../content-management/fragments.md#visual-expression)

1. 如有需要，您可以中斷具有原始片段的繼承。 [了解更多](#break-inheritance)

   解除鎖定後，您可以進一步將片段自訂為任何其他元件，並使用&#x200B;**[!UICONTROL 樣式]**&#x200B;索引標籤。

1. 新增您想要的片段數，然後&#x200B;**[!UICONTROL 儲存]**&#x200B;您的變更。

## 管理片段中的條件式內容 {#fragment-dynamic-content}

使用包含條件式內容的視覺片段時，請遵循下列准則。 [進一步瞭解動態內容](../personalization/dynamic-content.md#emails)

>[!CAUTION]
>
>**不支援包含條件內容的巢狀片段。** 您不能將包含條件內容的片段放在也包含條件內容的已解除鎖定片段內。 此不受支援的設定可能導致：
>
>* 遺失條件內容變體對應
>* 電子郵件Designer中的相容性模式警告
>* 不一致的電子郵件呈現

**正確建構您的電子郵件：**&#x200B;使用具有條件內容的多個片段時，請在電子郵件層級將每個片段直接新增到其自己的結構區塊中。 避免在其他也包含條件內容的解除鎖定片段中，巢狀內嵌有條件內容的片段。

**預先規劃：**&#x200B;在將片段新增至您的電子郵件之前，請先識別哪些片段包含條件式內容，並據此規劃您的版面。 這有助於防止設定問題，並確保從一開始就是乾淨的結構。

**仔細設計可重複使用的片段：**&#x200B;建立包含條件式內容的片段時，請考慮其使用方式。 如果片段需要巢狀內嵌於其他片段中，請避免同時新增條件式內容至父片段和子片段。

**疑難排解：**&#x200B;如果您遇到條件式內容變體對應或相容性模式警告遺失的情況，請遵循下列步驟。

* 檢查您的電子郵件結構，找出包含條件式內容的巢狀片段
* 透過在電子郵件層級將每個具有條件內容的片段移動到其自己的結構區塊中來重新構建
* 儲存並確認條件式內容變體已正確還原

## 使用隱含變數 {#implicit-variables-in-fragments}

隱含變數可增強現有片段功能，以提升內容重複使用性及指令碼使用案例的效率。 片段可以使用輸入變數，並建立可用於行銷活動和歷程內容的輸出變數。

瞭解如何在[本節](../personalization/use-expression-fragments.md#implicit-variables)中使用隱含變數。

## 自訂可編輯欄位 {#customize-fields}

如果所選片段的某些部分已變為可編輯，您可以在將片段新增到內容中後覆寫其預設值。 [瞭解如何使片段可自訂](../content-management/customizable-fragments.md)

若要自訂電子郵件所用片段中的可編輯欄位，請按照以下步驟操作。

1. 新增可自訂的片段至您的電子郵件內容，並選取它以開啟右側的&#x200B;**[!UICONTROL 片段]**&#x200B;窗格。

1. 片段中所有可編輯的欄位都會顯示在&#x200B;**[!UICONTROL 設定]**&#x200B;索引標籤中的片段屬性下。

   在以下範例中，您可以編輯影像來源和替代文字，以及「標題」/「副標題」欄位和「更多資訊」按鈕URL。

   ![](assets/fragment-editable-fields.png)

1. 將滑鼠懸停在中央畫布中的任何可編輯欄位上。 欄位會以綠色反白，按一下其中包含的文字時，會出現一個鉛筆圖示。

   ![](assets/fragment-editable-field-selected.png){width="80%" align="center"}

1. 直接在中心電子郵件Designer畫布上內嵌編輯欄位文字。

   >[!NOTE]
   >
   >若要輕鬆找到內容中的可編輯欄位，您也可以從右側窗格中選取它們，但您只能在中央畫布中編輯這些欄位。

1. 針對&#x200B;**[!UICONTROL Text]**、**[!UICONTROL Button]**&#x200B;和&#x200B;**[!UICONTROL Html]**&#x200B;元件，電子郵件Designer工具列也可存取RTF格式選項 — 粗體、斜體、超連結等等。

   ![電子郵件Designer工具列中的RTF格式選項](assets/fragment-editable-fields-rich-text.png)

   >[!TIP]
   >
   >在匯入RTF編輯功能之前建立的片段，其可編輯欄位預設為純文字模式。 若要啟用完整的格式選項，請使用&#x200B;**[!UICONTROL 開啟片段]**&#x200B;按鈕移至片段編輯器，按一下&#x200B;**[!UICONTROL 啟用]**&#x200B;以解鎖RTF模式並&#x200B;**[!UICONTROL 儲存]**&#x200B;片段。 [了解更多](../content-management/customizable-fragments.md#rich-text-visual)

   電子郵件Designer](assets/email-custom-fragment-compatibility.png){width="50%" align="center" zoomable="yes"}中的![相容性警告

1. 您可以按一下&#x200B;**[!UICONTROL 模擬內容]**，檢視可編輯的內容和樣式如何呈現。 [進一步瞭解預覽內容](../content-management/preview-test.md)

>[!CAUTION]
>
>當按鈕元件的&#x200B;**標籤**&#x200B;和&#x200B;**URL**&#x200B;在片段中都可以編輯時，追蹤報告會顯示URL而非按鈕標籤。 [進一步瞭解追蹤](message-tracking.md)

## 中斷繼承 {#break-inheritance}

當您編輯視覺片段時，變更會同步。 它們會自動傳播到包含該片段的所有草稿或即時歷程/行銷活動和內容範本。

新增至電子郵件或內容範本時，預設會同步片段。 不過，您可以中斷原始片段的繼承。 在這種情況下，片段的內容會複製到目前的設計中，且變更不再同步。

若要中斷繼承，請遵循下列步驟：

1. 選取片段。

1. 按一下內容工具列中的解鎖圖示。

   ![](assets/fragment-break-inheritance.png)

1. 該片段會成為不再連結至原始片段的獨立元素。 編輯它，就像內容中的任何其他內容元件一樣。 [了解更多](content-components.md)

### 鎖定的片段 {#locked-fragments}

如果片段已由作者鎖定，解鎖圖示會呈現灰色，且無法用來中斷繼承。

![](assets/fragment-locked.png)

鎖定的片段會在其出現處保持同步，以防止可能違反品牌標準或合規要求的本機編輯。

瞭解如何在[本節](../content-management/create-fragments.md#lock-visual-fragment)中鎖定片段。

>[!NOTE]
>
>片段作者稍後可以變更設定，以供日後使用，方法是在片段設定中將其行為重設為&#x200B;**[!UICONTROL 允許中斷繼承]**。

