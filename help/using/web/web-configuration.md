---
title: Web頻道設定
description: 建立網頁管道設定
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 2161baf0-38b7-4397-bffe-083929e8033a
source-git-commit: 37e60e5d7c0ad164cde67015b72341e1f4eda6a9
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 11%

---

# 建立網頁管道設定 {#web-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="頁面比對規則"
>abstract="若要有效管理和定位共用相同準則的 URL 群組，請建立頁面比對規則。此規則可讓您將多個 URL 合併至一個準則下，以便更輕鬆在這些頁面間套用一致的設定和動作。"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="預設製作和預覽 URL"
>abstract="此欄位可確保根據規則產生或符合的頁面具有指定的 URL，這對於有效建立和預覽內容至關重要。"

Web設定是由URL識別的Web屬性，將會傳送內容。 它可以比對單一頁面URL或多個頁面，讓您在一或多個網頁間提供修改內容。

1. 存取&#x200B;**[!UICONTROL 頻道]** > **[!UICONTROL 一般設定]** > **[!UICONTROL 頻道設定]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 建立頻道設定]**。

   ![](assets/web_config_1.png)

1. 輸入設定的名稱和說明（選擇性）。

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線`_`、點`.`和連字型大小`-`字元。

1. 若要將自訂或核心資料使用標籤指派給組態，您可以選取&#x200B;**[!UICONTROL 管理存取權]**。 [進一步瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md)。

1. 選取&#x200B;**Web**&#x200B;管道。

   ![](assets/web_config_2.png)

1. 選取&#x200B;**[!UICONTROL 行銷動作]**，以使用此設定將同意原則與訊息相關聯。 系統會運用與行銷動作相關的所有同意政策，以尊重客戶的偏好設定。 [了解更多](../action/consent.md#surface-marketing-actions)

1. 如果您只想將變更套用至單一頁面，可以輸入&#x200B;**[!UICONTROL 頁面URL]**。

1. 或者，您可以建置符合規則&#x200B;]**的**[!UICONTROL &#x200B;頁面，以符合相同規則的多個URL為目標 — 例如，如果您想要將變更套用至整個網站的主圖橫幅，或新增顯示在網站所有產品頁面上的最上層影像。

   若要這麼做，請選取&#x200B;**[!UICONTROL 符合規則]**&#x200B;的頁面。

1. 定義&#x200B;**[!UICONTROL 網域]**&#x200B;和&#x200B;**[!UICONTROL 頁面]**&#x200B;欄位的條件。

   例如，如果您想要編輯顯示在Luma網站所有女性產品頁面上的元素，請選取&#x200B;**[!UICONTROL 網域]** > **[!UICONTROL 開頭為]** > `luma`和&#x200B;**[!UICONTROL 頁面]** > **[!UICONTROL 包含]** > `women`。

   ![](assets/web_config_3.png)

1. 如果您已建立符合規則&#x200B;]**的**[!UICONTROL &#x200B;頁面，您必須輸入&#x200B;**預設**&#x200B;的製作與預覽URL。 此步驟會確保規則產生或相符的頁面具有用於內容建立和預覽的指定URL。 在以下](#web-page-matching-rule)的[區段中進一步瞭解頁面比對規則。

1. 儲存您的變更。

現在當您在行銷活動或歷程中使用網路通道時，可以選取您的設定。

## 頁面比對規則 {#web-page-matching-rule}

建立符合多個頁面的規則，以便一次在多個頁面上套用相同的內容變更時，您可以在&#x200B;**網域**&#x200B;和&#x200B;**路徑**&#x200B;區段上使用不同的運運算元來建置您想要的規則。 請檢查下方的可用運運算元。

建立頁面比對規則的可用運運算元：

* **網域**

  | 運運算元  | 說明  | 範例  |
  |---|---|---|
  | 等於  | 網域的完全相符專案。  |
  | 開頭為  | 符合以輸入字串開頭的所有網域（包括子網域）。  | 例如：「開頭為：dev」 ->符合開頭為「dev」的所有網域和子網域，例如：dev.example.com、dev.products.example.com、developer.example.com  |
  | 結尾為  | 比對以輸入字串結尾的所有網域（包括子網域）。  | 例如：「結尾為：example.com」 ->會比對所有結尾為「example.com」的網域和子網域，例如：stage.example.com、prod.example.com、myexample.com  |
  | 萬用字元比對  | 「萬用字元符合」運運算元可讓使用者在字串中間定義萬用字元符合，例如「dev」。*.example.com」。 驗證規則是當運運算元為「萬用字元比對」時，值必須包含且僅包含一個萬用字元（星號）。  | 例如：「萬用字元符合： dev.*.example.com&quot; ->會比對下列網域：dev.products.example.com、dev.mytest.products.example.com、dev.blog.example.com  |
  | 任何  | 符合所有網域 — 在跨網域測試特定路徑時很有用  |


* **路徑**

<table>
    <thead>
    <tr>
        <th><strong>運算子</th>
        <th><strong>說明</th>
        <th><strong>範例</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>等於</td>
        <td>路徑的確切相符專案。 </td>
        <td></td>
    </tr>
    <tr>
        <td>開頭為</td>
        <td>比對以輸入字串開頭的所有路徑（包括子路徑）。</td>
        <td></td>
    </tr>
    <tr>
        <td>結尾為</td>
        <td>比對以輸入字串結尾的所有路徑（包括子路徑）。</td>
        <td></td>
    </tr>
    <tr>
        <td>任何</td>
        <td>比對所有路徑 — 當鎖定一個或多個網域下的所有路徑時，這個用法很有用。</td>
        <td></td>
    </tr>
    <tr>
        <td>萬用字元比對</td>
        <td>「萬用字元符合」運運算元可讓使用者在路徑內定義內部萬用字元，例如"/products/*/detail"。  路徑**元件中的萬用字元*會比對任何字元順序，直到遇到第一個/字元為止。  /*/符合任何字元順序（包括子路徑）</td>
        <td>例如：「萬用字元符合：/products/*/detail」，符合所有路徑，例如： <ul><li>example.com/products/yoga/detail</li><li>example.com/products/surf/detail</li><li>example.com/products/tennis/detail</li><li>example.com/products/yoga/pants/detail</li></ul>例如：「符合： /prod*/detail，符合所有路徑，例如： <ul><li>example.com/products/detail</li><li>example.com/production/detail</li></ul>不符合如下的路徑： <ul><li>example.com/products/yoga/detail</li></ul></td>
    </tr>
    <tr>
        <td>包含</td>
        <td>"contains"會轉譯為"mystring"之類的萬用字元，並比對包含此字元序列的所有路徑。</td>
        <td>例如：「包含：產品」，符合包含字串產品的所有路徑，例如： <ul><li>example.com/products</li><li>example.com/yoga/perfproduct</li><li>example.com/surf/productdescription</li><li>example.com/home/product/page</li></ul></td>
    </tr>
    </tbody>
</table>

如果您的使用案例無法使用單一規則建模，那麼您可以選擇新增多個頁面規則，並且您可以在它們之間使用「Or」或「Exclude」運運算元。 當符合所定義規則的其中一個頁面不應作為目標時，「排除」會很有用：例如，包含「product」的所有「example.com」頁面，排除下列頁面： `https://example.com/blogs/productinfo`。
