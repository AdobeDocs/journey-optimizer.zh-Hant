---
title: 個人化使用案例&冒號；購物車放棄電子郵件
description: 了解如何使用協助程式功能個人化訊息
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 9c9598c0-6fb1-4e2f-b610-ccd1a80e516e
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 3%

---

# 個人化使用案例：購物車放棄電子郵件 {#personalization-use-case-helper-functions}

在此範例中，您將個人化電子郵件訊息的內文。 此訊息會鎖定已在購物車中留下項目，但尚未完成購買的客戶。

您將使用以下類型的協助程式函式：

* 此 `upperCase` 字串函式，以在大寫字母中插入客戶的名字。 [了解更多](functions/string.md#upper)。
* 此 `each` 協助工具，列出購物車中的項目。 [了解更多](functions/helpers.md#each)。
* 此 `if` 協助工具，以在相關產品在購物車中時插入產品專屬備注。 [了解更多](functions/helpers.md#if-function)。

<!-- **Context**: personalization based on contextual data from the journey -->

開始之前，請確定您知道如何設定這些元素：
* 電子郵件訊息。 [了解更多](../create-message.md)
* 電子郵件的正文。 [了解更多](../create-email-content.md)。
* 單一事件。 [了解更多](../event/about-events.md)。
* 以事件開始的歷程。 [了解更多](../building-journeys/using-the-journey-designer.md)。

請依照下列步驟操作：
1. [建立電子郵件訊息](#configure-email).
1. [在大寫字母中插入客戶的名字](#uppercase-function).
1. [建立初始事件和歷程](#create-context).
1. [將購物車內容新增至電子郵件](#each-helper).
1. [插入產品特定附註](#if-helper).
1. [測試並發佈歷程](#test-and-publish).

## 步驟1:建立電子郵件{#configure-email}

1. 建立或修改電子郵件訊息，然後按一下 **[!UICONTROL Email Designer]**.
   ![](../assets/personalization-uc-helpers-1.png)

1. 從電子郵件設計工具首頁的左側浮動視窗，將三個結構元件拖放至訊息內文。

1. 將HTML內容元件拖放至每個新結構元件。

   ![](../assets/personalization-uc-helpers-2.png)

## 步驟2:在大寫字母中插入客戶的名字 {#uppercase-function}

1. 在電子郵件設計工具首頁上，按一下要添加HTML名的客戶元件。
1. 在內容工具列上，按一下 **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

1. 在 **[!UICONTROL Edit HTML]** 窗口，添加 `upperCase` 字串函式：
   1. 在清單中，選取 **[!UICONTROL Helper functions]**.
   1. 使用搜索欄位查找「大寫」。
   1. 從搜尋結果中，新增 `upperCase` 函式。 要執行此操作，請按一下旁邊的加號(+) `{%= upperCase(string) %}: string`.

      運算式編輯器會顯示此運算式：

      ```handlebars
      {%= upperCase(string) %}
      ```

      ![](../assets/personalization-uc-helpers-4.png)

1. 從運算式中移除「字串」預留位置。
1. 新增名字代號：
   1. 在清單中，選取 **[!UICONTROL Profile]**.
   1. 選擇 **[!UICONTROL Profile]** > **[!UICONTROL Person]** > **[!UICONTROL Full name]**.
   1. 新增 **[!UICONTROL First name]** 代號至運算式。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ```

      ![](../assets/personalization-uc-helpers-5.png)

      深入了解人員名稱資料類型 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html){target=&quot;_blank&quot;}。

1. 按一下「**[!UICONTROL Validate]**」，然後按一下「**[!UICONTROL Save]**」。

   ![](../assets/personalization-uc-helpers-6.png)
1. 儲存訊息。

## 步驟3:建立初始事件和相關歷程 {#create-context}

購物車內容是歷程的情境資訊。 因此，您必須先新增初始事件和電子郵件至歷程，才能將購物車專屬資訊新增至電子郵件。

1. 建立其架構包含 `productListItems` 陣列。
1. 將此陣列中的所有欄位定義為此事件的有效負載欄位。

   深入了解產品清單項目資料類型 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target=&quot;_blank&quot;}。

1. 建立以此事件開始的歷程。
1. 將訊息新增至歷程。
1. 以結束活動結束歷程。

   由於您尚未發佈訊息，因此您既無法測試也不能發佈歷程。

   ![](../assets/personalization-uc-helpers-7.png)

1. 按一下「**[!UICONTROL OK]**」。

   訊息會通知您歷程內容已傳遞至訊息。

   ![](../assets/personalization-uc-helpers-8.png)

## 步驟4:插入購物車中的項目清單 {#each-helper}

1. 重新開啟訊息。

   ![](../assets/personalization-uc-helpers-18.png)

1. 在電子郵件設計工具首頁上，按一下您要列出購物車內容的HTML元件。
1. 在內容工具列上，按一下 **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

1. 在 **[!UICONTROL Edit HTML]** 窗口，添加 `each` 幫助者：
   1. 在清單中，選取 **[!UICONTROL Helper functions]**.
   1. 使用搜尋欄位來尋找「每個」。
   1. 從搜尋結果中，新增 `each` 幫手。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```

      ![](../assets/personalization-uc-helpers-9.png)

1. 新增 `productListItems` array到運算式：

   1. 從運算式中移除「someArray」預留位置。
   1. 在清單中，選取 **[!UICONTROL Context]**.

      此 **[!UICONTROL Context]** 選項僅在歷程內容傳遞至訊息後才可用。

   1. 選擇 **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]***，然後展開 **[!UICONTROL productListItems]** 節點。

      在此範例中， *event_name* 代表事件的名稱。

   1. 新增 **[!UICONTROL Product]** 代號至運算式。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```
      在此範例中， *event_ID* 代表事件的ID。

      ![](../assets/personalization-uc-helpers-10.png)

   1. 修改運算式：
      1. 移除「.product」字串。
      1. 將「變數」預留位置取代為「product」。

      此示例顯示修改後的表達式：

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```
1. 將此程式碼貼到開頭 `{{#each}}` 標籤和結尾 `{/each}}` 標籤：

   ```html
   <table>
      <tbody>
         <tr>
            <td><b>#name</b></td>
            <td><b>#quantity</b></td>
            <td><b>$#priceTotal</b></td>
         </tr>
      </tbody>
   </table>
   ```

1. 為項目名稱、數量和價格新增個人化代號：

   1. 從HTML表格中移除預留位置「#name」。
   1. 從先前的搜尋結果中，新增 **[!UICONTROL Name]** 代號至運算式。

   重複這些步驟兩次：
   * 將預留位置「#quantity」取代為 **[!UICONTROL Quantity]** 代號。
   * 將預留位置「#priceTotal」取代為 **[!UICONTROL Total price]** 代號。

   此示例顯示修改後的表達式：

   ```handlebars
   {{#each context.journey.events.event_ID.productListItems as |product|}}
      <table>
         <tbody>
            <tr>
               <td><b>{{context.journey.events.event_ID.productListItems.name}}</b></td>
               <td><b>{{context.journey.events.event_ID.productListItems.quantity}}</b></td>
               <td><b>${{context.journey.events.event_ID.productListItems.priceTotal}}</b></td>
            </tr>
         </tbody>
      </table>
   {{/each}}
   ```
1. 按一下「**[!UICONTROL Validate]**」，然後按一下「**[!UICONTROL Save]**」。
   ![](../assets/personalization-uc-helpers-11.png)

## 步驟5:插入產品特定附註 {#if-helper}

1. 在電子郵件設計工具首頁上，按一下要插入注釋的HTML元件。
1. 在內容工具列上，按一下 **[!UICONTROL Show the source code]**.

   ![](../assets/personalization-uc-helpers-3.png)

1. 在 **[!UICONTROL Edit HTML]** 窗口，添加 `if` 幫助者：
   1. 在清單中，選取 **[!UICONTROL Helper functions]**.
   1. 使用搜尋欄位來尋找&quot;if&quot;。
   1. 從搜尋結果中，新增 `if` 幫手。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-12.png)

1. 從運算式中移除此條件：

   ```handlebars
   {%else if condition2%} render_2
   ```

   此示例顯示修改後的表達式：

   ```handlebars
   {%#if condition1%} render_1
      {%else%} default_render
   {%/if%}
   ```

1. 將產品名稱代號新增至條件：
   1. 從運算式中移除「condition1」預留位置。
   1. 在清單中，選取 **[!UICONTROL Context]**.
   1. 選擇 **[!UICONTROL Journey Orchestration]** > **[!UICONTROL Events]** > ***[!UICONTROL event_name]***，然後展開 **[!UICONTROL productListItems]** 節點。

      在此範例中， *event_name* 代表事件的名稱。

   1. 新增 **[!UICONTROL Name]** 代號至運算式。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```
      ![](../assets/personalization-uc-helpers-13.png)

1. 修改運算式：
   1. 在運算式編輯器中，指定產品名稱后方的 `name` 代號。

      請使用此語法，其中 *product_name* 代表您的產品名稱：

      ```javascript
      = "product_name"
      ```

      在此範例中，產品名稱為「Juno Jacket」：

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         render_1
         {%else%} default_render
      {%/if%}
      ```

   1. 將「render_1」預留位置替換為注釋的文本。

      範例：

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         Due to longer than usual lead times on the Juno Jacket, please expect item to ship two weeks after purchase.
         {%else%} default_render
      {%/if%}
      ```
   1. 從運算式中移除「default_render」預留位置。
1. 按一下「**[!UICONTROL Validate]**」，然後按一下「**[!UICONTROL Save]**」。

   ![](../assets/personalization-uc-helpers-14.png)

1. 儲存並發佈訊息。

## 步驟6:測試並發佈歷程 {#test-and-publish}

1. 開啟歷程。 如果歷程已開啟，請重新整理頁面。
1. 開啟 **[!UICONTROL Test]** 切換，然後按一下 **[!UICONTROL Trigger an event]**.

   只有在發佈訊息後，才可以開啟測試模式。

   ![](../assets/personalization-uc-helpers-15.png)

1. 在 **[!UICONTROL Event configuration]** ，輸入輸入值，然後按一下 **[!UICONTROL Send]**.

   測試模式僅適用於測試設定檔。

   ![](../assets/personalization-uc-helpers-16.png)

   電子郵件會傳送至測試設定檔的地址。

   在此範例中，電子郵件包含關於Juno Jacket的附註，因為此產品位於購物車中：

   ![](../assets/personalization-uc-helpers-17.png)

1. 確認沒有錯誤，然後發佈歷程。


## 相關主題

### Handlebars函式

* [輔助程式](functions/helpers.md)

* [字串函式](functions/string.md)

### 使用案例

* [使用設定檔資訊、內容和選件進行個人化](personalization-use-case.md)

* [使用決策型選件進行個人化](../offers/offers-e2e.md)

## 教學課程影片{#helper-functions-video}

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
