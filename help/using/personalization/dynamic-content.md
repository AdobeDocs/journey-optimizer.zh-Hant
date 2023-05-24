---
solution: Journey Optimizer
product: journey optimizer
title: 建立動態內容
description: 瞭解如何將動態添加到郵件中。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表達式，編輯器，動態，內容
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 9%

---

# 建立動態內容 {#dynamic-content}

Adobe Journey Optimizer允許您利用庫中建立的條件規則將動態內容添加到郵件中。

動態內容可以建立到任何欄位中，您可以使用表達式編輯器在其中添加個性化。 這包括主題行、連結、推送通知內容或文本類型服務的表示法。 [瞭解有關個性化上下文的詳細資訊](personalization-contexts.md)

此外，您可以在電子郵件設計器中使用條件規則來建立內容元件的多個變體。

## 將動態內容添加到表達式 {#perso-expressions}

在表達式中添加動態內容的步驟如下：

1. 導航到要添加動態內容的欄位，然後開啟表達式編輯器。

1. 選擇 **[!UICONTROL 條件]** 的子菜單。 按一下規則旁邊的+按鈕，將其添加到當前表達式中。

   也可以通過選擇 **[!UICONTROL 新建]**。 [瞭解如何建立條件](create-conditions.md)

   ![](assets/conditions-expression.png)

1. 在 `{%if}` 和 `{%/if}` 標籤如果滿足條件規則，則要顯示的內容。 您可以根據需要添加任意多個規則，以建立表達式的多個變型。

   在以下示例中，根據收件人的首選語言為SMS內容建立了兩個變型。

   ![](assets/conditions-language-sample.png)

1. 內容準備好後，可以使用 **[!UICONTROL 模擬內容]** 按鈕 [瞭解如何test和預覽消息](../email/preview.md)

   ![](assets/conditions-preview.png)

## 將動態內容添加到電子郵件 {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="條件式內容"
>abstract="使用條件式規則建立內容元件的多個變體。如果傳送訊息時未符合任何條件，將顯示預設變體的內容。"

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="條件式內容"
>abstract="使用儲存在資料庫中的條件式規則或建立新規則。"

在電子郵件設計器中建立內容元件變型的步驟如下：

1. 在電子郵件設計器中，選擇內容元件，然後按一下 **[!UICONTROL 啟用條件內容]**。

   ![](assets/conditions-enable-conditional.png)

1. 的 **[!UICONTROL 條件內容]** 窗格。 在此窗格中，您可以使用條件建立所選內容元件的多個變型。

   通過選擇 **[!UICONTROL 應用條件]** 按鈕

   ![](assets/conditions-apply.png)

1. 顯示條件庫。 選擇要與變數關聯的條件規則，然後按一下 **[!UICONTROL 選擇]**。 在本示例中，我們要根據收件人的首選語言調整元件文本。

   ![](assets/conditions-select.png)

   也可以通過按一下 **[!UICONTROL 新建]**。 [瞭解如何建立條件](create-conditions.md)

1. 條件規則與變型關聯。 為了更好的可讀性，我們建議通過按一下橢圓菜單更名變型。

   現在，配置在發送消息時是否滿足規則時元件應顯示的方式。 在本示例中，如果文本是收件人的首選語言，則我們希望以法語顯示它。

   ![](assets/conditions-design.png)

1. 根據需要為內容元件添加任意多個變型。 您可以隨時在不同變體之間切換，以檢查內容元件將如何根據條件規則顯示。

   >[!NOTE]
   >如果在發送消息時未滿足變型中定義的任何規則，則內容元件將顯示在 **[!UICONTROL 預設變數]**。
   >
   >將根據相關規則按變型的顯示順序來評估條件內容。 如果未滿足其他條件，則始終顯示預設變數。
