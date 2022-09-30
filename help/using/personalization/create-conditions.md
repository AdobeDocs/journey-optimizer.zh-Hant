---
title: 建立條件
description: 了解如何建立條件
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 9593ea40853221e0eec45f30f7635d8a116b03c1
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 1%

---


# 使用條件式規則 {#conditions}

條件式規則是一組規則，定義應根據各種條件（例如設定檔屬性、區段成員資格或情境事件）在訊息中顯示的內容。

條件式規則是使用運算式編輯器建立，如果您想在整個內容中重複使用這些規則，則可加以儲存。 [了解如何將條件式規則儲存至程式庫](#save)

>[!NOTE]
>
>個人需要 [管理程式庫項目](../administration/ootb-product-profiles.md) 儲存或刪除條件規則的權限。 儲存的條件可供組織內的所有使用者使用。

## 存取條件式規則產生器 {#access}

條件規則是從 **[!UICONTROL 條件]** 運算式編輯器中的功能表，可存取：

* 從電子郵件設計工具，為電子郵件內文中的元件啟用動態內容時。 [了解如何將動態內容新增至電子郵件](dynamic-content.md#emails)

   ![](assets/conditions-access-email.png)

* 在您可以使用 [運算式編輯器](personalization-build-expressions.md).

   ![](assets/conditions-access-editor.png)

## 建立條件式規則 {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="建立條件"
>abstract="結合設定檔屬性、內容事件或對象，以建立規則來定義應在訊息中顯示的內容。"

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="建立條件"
>abstract="結合設定檔屬性、內容事件或對象，以建立規則來定義應在訊息中顯示的內容。"

建立條件式規則的步驟如下：

1. 存取 **[!UICONTROL 條件]** 表達式編輯器或電子郵件設計工具中的菜單，然後按一下 **[!UICONTROL 新建]**.

1. 根據您的需求建立條件式規則。 若要這麼做，請從左側功能表將所需屬性拖放並排列至畫布中。

   將屬性結合至畫布的步驟與區段建立體驗類似。 如需如何使用規則產生器畫布的詳細資訊，請參閱 [本檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#rule-builder-canvas).

   ![](assets/conditions-create.png)

   屬性可組織為三個索引標籤：

   * **[!UICONTROL 設定檔]**:
      * **[!UICONTROL 區段成員資格]** 會列出所有區段屬性（例如狀態、版本等） for [Adobe Experience Platform細分服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html),
      * **[!UICONTROL XDM個別設定檔]** 列出與 [Experience Data Model(XDM)結構](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant) 定義於Adobe Experience Platform。
   * **[!UICONTROL 內容]**:在歷程中使用您的訊息時，可透過此索引標籤使用內容歷程欄位。
   * **[!UICONTROL 對象]**:會列出從中建立的區段產生的所有對象 [Adobe Experience Platform細分服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

1. 條件式規則準備就緒後，您就可以將其新增至訊息，以建立動態內容。 [了解如何新增動態內容](dynamic-content.md)

   您也可以儲存規則以允許進一步重複使用。 [了解如何儲存條件](#save)

## 儲存條件式規則 {#save}

如果您經常重複使用條件規則，可將其儲存至條件程式庫。 所有儲存的規則皆會共用，且可由組織內的個人存取及使用。

>[!NOTE]
>
>無法將運用歷程內容屬性的條件式規則儲存至資料庫。

1. 在條件版本畫面中，按一下 **[!UICONTROL 儲存條件]** 按鈕。

1. 為規則指定名稱和說明（選用），然後按一下 **[!UICONTROL 新增]**.

   ![](assets/conditions-name-description.png)

1. 條件式規則會儲存至程式庫。 您現在可以使用它，在訊息中建立動態內容。 [了解如何新增動態內容](dynamic-content.md)

## 編輯和刪除儲存的條件規則 {#edit-delete}

您可以隨時使用橢圓按鈕刪除條件規則。

![](assets/conditions-open.png)

儲存至程式庫的條件式規則無法修改。 不過，您仍可使用這些規則來建立新規則。 若要這麼做，請開啟條件式規則，進行所需的變更，然後儲存至程式庫。 [了解如何將條件儲存至程式庫](#save)
