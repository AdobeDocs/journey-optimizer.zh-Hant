---
solution: Journey Optimizer
product: journey optimizer
title: 建立條件
description: 瞭解如何建立條件
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表達式，編輯器，條件，規則
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 8%

---

# 使用條件規則 {#conditions}

條件規則是一組規則，根據配置檔案的屬性、段成員身份或上下文事件等各種條件定義應在消息中顯示哪些內容。

條件規則是使用表達式編輯器建立的，如果要在內容中重複使用，則可以儲存這些規則。 [瞭解如何將條件規則保存到庫](#save)

>[!NOTE]
>
>個人需要 [管理庫項目](../administration/ootb-product-profiles.md) 保存或刪除條件規則的權限。 保存的條件可供組織內的所有用戶使用。

## 訪問條件規則生成器 {#access}

條件規則是從 **[!UICONTROL 條件]** 可訪問的表達式編輯器中的菜單：

* 在為電子郵件正文中的元件啟用動態內容時，請從電子郵件設計器中。 [瞭解如何在電子郵件中添加動態內容](dynamic-content.md#emails)

   ![](assets/conditions-access-email.png)

* 在可使用 [表達式編輯器](personalization-build-expressions.md)。

   ![](assets/conditions-access-editor.png)

## 建立條件規則 {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="建立條件"
>abstract="結合設定檔屬性、內容事件或對象以建置定義在訊息中應顯示哪些內容的規則。"

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="建立條件"
>abstract="結合設定檔屬性、內容事件或對象以建置定義在訊息中應顯示哪些內容的規則。"

建立條件規則的步驟如下：

1. 訪問 **[!UICONTROL 條件]** 按鈕，按一下 **[!UICONTROL 新建]**。

1. 根據需要建立條件規則。 要執行此操作，請將所需屬性從左側菜單拖放到畫布中。

   將屬性組合到畫布的步驟與段構建體驗類似。 有關如何使用規則生成器畫布的詳細資訊，請參閱 [本文檔](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#rule-builder-canvas)。

   ![](assets/conditions-create.png)

   屬性分為三個頁籤：

   * **[!UICONTROL 設定檔]**:
      * **[!UICONTROL 段成員資格]** 列出所有段屬性（如狀態、版本等） 為 [Adobe Experience Platform分段服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)。
      * **[!UICONTROL XDM個別配置檔案]** 列出與 [體驗資料模型(XDM)架構](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant) 定義於Adobe Experience Platform。
   * **[!UICONTROL 上下文]**:在行程中使用消息時，上下文行程欄位可通過此頁籤使用。
   * **[!UICONTROL 觀眾]**:列出從建立於 [Adobe Experience Platform分段服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)。

1. 條件規則準備好後，可將其添加到消息中以建立動態內容。 [瞭解如何添加動態內容](dynamic-content.md)

   還可以保存規則以允許進一步重用。 [瞭解如何保存條件](#save)

## 保存條件規則 {#save}

如果有條件規則，您將經常重用，則可以將它們保存到條件庫中。 所有保存的規則都是共用的，組織內的個人可以訪問並使用這些規則。

>[!NOTE]
>
>無法將利用行程上下文屬性的條件規則保存到庫中。

1. 在條件版本螢幕中，按一下 **[!UICONTROL 保存條件]** 按鈕

1. 為規則指定名稱和說明（可選），然後按一下 **[!UICONTROL 添加]**。

   ![](assets/conditions-name-description.png)

1. 條件規則將保存到庫。 現在，您可以使用它在郵件中建立動態內容。 [瞭解如何添加動態內容](dynamic-content.md)

## 編輯和刪除保存的條件規則 {#edit-delete}

您可以隨時使用省略號按鈕刪除條件規則。

![](assets/conditions-open.png)

無法修改保存到庫的條件規則。 但是，您仍然可以使用它們建立新規則。 為此，請開啟條件規則，進行所需的更改，然後將其保存到庫中。 [瞭解如何將條件保存到庫](#save)
