---
solution: Journey Optimizer
product: journey optimizer
title: 在 Journey Optimizer 中個人化內容
description: 開始使用個人化。
feature: Personalization
topic: Personalization
role: Developer
level: Beginner
keywords: 運算式，編輯器，開始，個人化
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1403
ht-degree: 11%

---

# 開始使用個人化{#add-personalization}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;開始使用Adobe Journey Optimizer中的個人化功能，包括個人化編輯器的運作方式、您可以使用的設定檔資料、學習遊樂場以及內嵌編輯。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="個人化體驗"
>abstract="使用 **Adobe Journey Optimizer**，利用手邊關於他們的資料與資訊，調整給各個特定接收者的訊息。 可以是他們的姓氏、興趣、居住的地方、購買的產品等等。"

[!DNL Adobe Journey Optimizer]個人化功能可讓您運用您擁有的訊息相關資料與資訊，將訊息調整至每個特定收件者。 可以是他們的姓氏、興趣、居住的地方、購買的產品等等。

## 個人化的運作方式

使用&#x200B;**個人化編輯器**，您可以選取、排列、自訂及驗證所有資料，以建立您內容的自訂個人化，並利用各種工具（例如協助程式功能或預先定義的運算式）來有效地自訂訊息。

Journey Optimizer採用以Handlebars為基礎的內嵌個人化語法，可讓您建立包含雙大括弧&#x200B;**`{{}}`**&#x200B;之內容的運算式。

處理訊息時，Journey Optimizer會以Experience Platform資料集中包含的資料取代運算式。 例如，`Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`會動態變成`Hello John Doe`。 使用此語法，您可以跨多個欄位個人化訊息，包括電子郵件主旨列、訊息本文、推播通知或URL。

## 用於個人化的資料

Personalization是以由Adobe Experience Platform中定義的&#x200B;**XDM個別設定檔**&#x200B;結構描述管理的設定檔資料為基礎。 **XDM Individual Profile**&#x200B;結構描述是唯一可用來個人化[!DNL Journey Optimizer]中內容的結構描述。 在[Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}中進一步瞭解。

您也可以運用&#x200B;**計算屬性**&#x200B;來個人化您的內容。 計算屬性可讓您將個別行為事件摘要為Adobe Experience Platform上可用的計算設定檔屬性。 [瞭解如何使用計算屬性](../audience/computed-attributes.md)

此外，[!DNL Journey Optimizer]可讓您在個人化編輯器中運用Adobe Experience Platform的資料，來個人化您的內容。 若想這樣做，就必須先透過 API 呼叫，啟用查詢個人化所需的資料集。 完成後，您可以使用他們的資料在Journey Optimizer中個人化您的內容。 此功能目前在Beta版中提供。 [了解更多](../personalization/aep-data-perso.md)

## 學習並實驗個人化 {#playground}

**[!DNL Adobe Journey Optimizer]**&#x200B;包含互動式工具，旨在協助您學習及實驗個人化功能。

此遊樂場提供模擬環境，讓您使用範例資料來撰寫和測試個人化程式碼，而不需要即時資料集。 您可以運用預先定義的程式碼範例、編輯虛擬設定檔裝載，並即時預覽個人化程式碼的輸出。

![個人化遊樂場](assets/playground.png)

➡️ [存取個人化遊樂場](https://experienceleague.adobe.com/zh-hant/apps/journey-optimizer/ajo-personalization){target="_blank"}

## 個人化運算式的 AI 助理 {#ai-personalization-expressions}

在&#x200B;**[!UICONTROL Personalization編輯器]**&#x200B;中或從Email Designer工具列（**[!UICONTROL 新增運算式]**）中，**[!UICONTROL AI Assistant]**&#x200B;可協助您從自然語言產生新的運算式、說明現有程式碼的作用，並修正選取範圍中的問題，然後在其符合您的意圖時套用輸出。

![](../content-management/assets/ai-perso-generate.png)

➡️ [瞭解如何使用Personalization運算式的AI小幫手](../content-management/generative-personalization-expressions.md)

## 內嵌編輯設定檔屬性 {#inline-personalization}

在&#x200B;**電子郵件Designer**&#x200B;或&#x200B;**推播通道**&#x200B;編輯器中編輯內容時，您可以直接插入設定檔屬性運算式，而不需開啟完整的個人化編輯器。

若要這麼做，請依照以下步驟進行：

1. 在任何文字欄位中輸入`{{`。 在游標位置會開啟內嵌自動完成下拉式清單。
1. 開始輸入以篩選可用的設定檔屬性。
1. 選取您需要的屬性 — 會以個人化權杖的形式插入游標位置。

![](assets/inline-profile-attributes.png)

## 讓我們深入探討

現在您已瞭解&#x200B;**[!DNL Journey Optimizer]**&#x200B;中的個人化，是時候深入探討這些檔案區段以開始使用此功能了。

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="personalization-build-expressions.md">
<img alt="新增個人化" src="assets/do-not-localize/add.png">
</a>
<div>
<a href="personalization-build-expressions.md"><strong>新增個人化</strong></a>
</div>
<p>
</td>
<td>
<a href="../personalization/personalization-syntax.md">
<img alt="銷售機會" src="assets/do-not-localize/syntax.png">
</a>
<div><a href="../personalization/personalization-syntax.md"><strong>Personalization語法</strong>
</div>
<p>
</td>
<td>
<a href="../personalization/functions/functions.md">
<img alt="不頻繁" src="assets/do-not-localize/functions.png">
</a>
<div>
<a href="../personalization/functions/functions.md"><strong>協助程式函式清單</strong></a>
</div>
<p></td>
<td>
<a href="../personalization/personalization-recipes.md">
<img alt="不頻繁" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-recipes.md"><strong>Personalization配方</strong></a>
</div>
<p></td>
<td>
<a href="../personalization/personalization-use-case.md">
<img alt="不頻繁" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-use-case.md"><strong>Personalization使用案例</strong></a>
</div>
<p></td>
</tr></table>

## 作法影片{#video-perso}

瞭解如何使用歷程中的內容事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/3448153?captions=chi_hant&quality=12)

了解如何將以輪廓為基礎的個人化新增至訊息，以及如何使用客群成員資格作為個人化區塊的先決條件。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

瞭解如何善用個人化編輯器遊樂場，使用範例資料來撰寫及測試個人化程式碼。

>[!VIDEO](https://video.tv.adobe.com/v/3475963?captions=chi_hant&quality=12)

在[Personalization教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/personalize-content/personalization-editor-overview){target="_blank"}中探索更多有關個人化功能和最佳實務的教學課程影片

## 快速參考 {#quick-reference}

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

>[!BEGINTABS]

>[!TAB 概觀]

**TL；DR**

本頁介紹Journey Optimizer中的個人化 — Handlebars式個人化編輯器的運作方式、其使用的資料、互動遊樂場、適用於運算式的AI Assistant，以及在電子郵件Designer和推播編輯器中編輯內嵌屬性。

**個意圖**

* 瞭解Journey Optimizer個人化的運作方式（使用雙大括弧的Handlebars語法）
* 識別可用於個人化的資料來源（XDM個別設定檔結構、計算屬性、Beta版中的AEP資料集查詢）
* 使用不具即時沙箱的互動式遊樂場進行個人化實驗
* 使用AI助理從自然語言產生、說明或修正個人化運算式
* 透過輸入`{{`在電子郵件Designer或推播編輯器中插入內嵌設定檔屬性

>[!TAB 字彙]

* **Personalization編輯器**：用於建置、自訂及驗證個人化運算式的完整功能工具；可在任何支援個人化的Journey Optimizer欄位中使用。 *（產品特定）*
* **XDM Individual Profile結構描述**：唯一可用來個人化Journey Optimizer內容的結構描述；定義所有可用於個人化的設定檔屬性。 *（產品特定）*
* **計算屬性**：將個別行為事件彙總為設定檔層級值的預先計算設定檔屬性；可與標準XDM設定檔欄位一起作為個人化資料。 *（產品特定）*
* **Personalization Playground**： Experience League上的互動式模擬環境，可使用範例資料來撰寫及測試個人化程式碼，不需要即時資料集或沙箱。 *（產品特定）*
* **內嵌編輯**：可在電子郵件Designer或推播頻道編輯器的任何文字欄位中輸入`{{`，以觸發自動完成下拉式清單並插入設定檔屬性，而不需開啟完整個人化編輯器。 *（產品特定）*
* **AI Assistant （個人化運算式）**：個人化編輯器和電子郵件Designer中的AI工具，可從自然語言產生個人化運算式、說明現有程式碼，以及修正選取範圍中的問題。 *（產品特定）*

>[!TAB 術語]

* **正式名稱：**&#x200B;個人化 — 變體：內容個人化、訊息個人化、運算式個人化
* **正式名稱：**&#x200B;個人化編輯器 — 變體：個人化功能
* **請勿混淆：** Personalization編輯器（用來建置訊息和選件中的內容運算式 — 同時支援Handlebars和PQL）≠進階運算式編輯器（用於歷程中的資料來源和事件資訊、自訂等待活動及動作引數對應條件 — 提供內建函式及運運算元，不同於個人化編輯器中的函式及運運算元）
* **請勿混淆：**&#x200B;內嵌編輯（在電子郵件Designer中輸入`{{`，或在未開啟完整編輯器的情況下以推播方式插入快速屬性）≠個人化編輯器（適用於複雜運算式、協助程式函式、條件式規則和片段的完整工具）
* **請勿混淆：** XDM Individual Profile結構描述（Journey Optimizer中唯一可用於個人化的結構描述）≠其他AEP結構描述（除非透過資料集查詢公開，否則無法用於個人化）

>[!TAB 護欄與限制]

* XDM Individual Profile結構描述是唯一可用於個人化Journey Optimizer內容的結構描述。
* 查詢個人化的AEP資料集時，必須先透過API呼叫啟用資料集，才能加以使用；此功能目前仍在測試階段。
* 內嵌編輯（在電子郵件Designer或推播編輯器中輸入`{{`）僅支援設定檔屬性。

>[!TAB 常見問題集]

**問：哪些資料可以在Journey Optimizer中用於個人化？**

來自XDM個別設定檔結構的設定檔資料、運算屬性（在設定檔層級摘要的行為事件）和AEP記錄資料集查詢（目前為測試版 — 需要透過API啟用資料集）。

**問：什麼是個人化遊樂場？**

Experience League上的互動式模擬環境，您可以使用範例資料來撰寫及測試個人化程式碼，而不需要即時Journey Optimizer沙箱或真實資料集。

**問：內嵌屬性編輯如何運作？**

在電子郵件Designer或推播通道編輯器的任何文字欄位中輸入`{{`，以開啟游標位置處的自動完成下拉式清單。 開始輸入以篩選設定檔屬性，然後選取一個以插入作為個人化權杖。 只有設定檔屬性可內嵌。

**問：AI助理可以在個人化編輯器中做什麼？**

它可以從自然語言描述產生新的個人化運算式、說明現有程式碼的作用，並修正所選運算式中的問題 — 然後在其符合您的意圖時套用輸出。

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 248b894f -->
