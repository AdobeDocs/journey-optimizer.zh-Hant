---
title: Web頻道設定
description: 建立Web Channel設定
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 1%

---

# 建立Web Channel設定 {#web-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="頁面比對規則"
>abstract="若要有效管理並鎖定共用相同條件的一組URL，請建立頁面比對規則。 此規則可讓您將多個URL整合到一個指引下，以簡化在這些頁面上應用一致設定和動作的程式。"

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="預設撰寫和預覽URL"
>abstract="此欄位可確保規則產生或相符的頁面具有指定的URL，這點對於有效建立和預覽內容而言至關重要。"

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

  | | | |
  |-|-|-|
  | 運運算元  | 說明  | 範例  |
  | 等於  | 路徑的確切相符專案。  |    |
  | 開頭為  | 比對以輸入字串開頭的所有路徑（包括子路徑）。  |    |
  | 結尾為  | 比對以輸入字串結尾的所有路徑（包括子路徑）。  |    |
  | 任何  | 比對所有路徑 — 當鎖定一個或多個網域下的所有路徑時，這個用法很有用。  |    |
  | 萬用字元比對  | 「萬用字元符合」運運算元可讓使用者在路徑中定義內部萬用字元，例如&quot;/products/*/detail&quot;。  路徑**元件中的萬用字元*會比對任何字元順序，直到遇到第一個/字元為止。  /*/符合任何字元順序（包括子路徑）  | 例如：「萬用字元符合： /products/*/detail」，符合所有路徑，例如：  example.com/products/yoga/detail  example.com/products/surf/detail  example.com/products/tennis/detail  example.com/products/yoga/pants/detail   例如：「符合： /prod*/detail，符合所有路徑，例如：  example.com/products/detail  example.com/production/detail   不符合如下的路徑：  example.com/products/yoga/detail  |
  | 包含  | &quot;contains&quot;會轉譯為&quot;mystring&quot;之類的萬用字元，並比對包含此字元序列的所有路徑。  | 例如：「包含：product」，會比對包含字串產品的所有路徑，例如：example.com/products、example.com/yoga/perfproduct、example.com/surf/productdescription、example.com/home/product/page  |


如果您的使用案例無法使用單一規則建模，那麼您可以選擇新增多個頁面規則，並且您可以在它們之間使用「Or」或「Exclude」運運算元。 當符合所定義規則的其中一個頁面不應作為目標時，「排除」會很有用：例如，包含「product」的所有「example.com」頁面，排除下列頁面： `https://example.com/blogs/productinfo`。