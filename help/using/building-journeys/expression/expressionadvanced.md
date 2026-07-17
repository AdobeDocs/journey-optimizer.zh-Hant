---
solution: Journey Optimizer
product: journey optimizer
title: 使用進階運算式編輯器
description: 瞭解如何建立進階運算式
feature: Journeys
role: Developer
level: Experienced
keywords: 運算式編輯器，資料，歷程
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/8RsF-CRRrsLiCzwsaqfJQnWcyy6frmKkdSJBKnIhGgE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: ac5d9310-7772-40fb-9d78-864562e1bfd6id: e51e8901-97d9-4f7d-a835-503025a90e32id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 423db08a3c4c5a8d9540fa0c8e03e28ca36ca299
workflow-type: tm+mt
source-wordcount: 1236
ht-degree: 31%

---

# 使用進階運算式編輯器 {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="關於進階運算式編輯器"
>abstract="進階運算式編輯器可在介面的各個畫面中建立進階運算式。 例如，您可以在設定和使用歷程時以及定義資料來源條件時建置運算式。"

使用Journey進階運算式編輯器，在介面的各種畫面中建置進階運算式。 例如，您可以在設定和使用歷程時以及定義資料來源條件時建置運算式。

此外，您每次必須定義需要特定資料處理的動作參數時，都可以使用它。 您可以善用來自事件的資料或是從資料來源擷取的其他資訊。 在歷程中，顯示的事件欄位清單會與情境相關，而且會根據歷程中新增的事件而有所不同。

![](../assets/journey65.png)


進階運算式編輯器提供一組內建函式和運算子，讓您得以控制值並定義特別符合您需求的運算式。 進階運算式編輯器也可讓您定義外部資料來源引數的值、控制對應欄位和集合。

>[!NOTE]
>
>歷程進階運算式編輯器中可用的功能和功能，與[個人化編輯器](../../personalization/functions/functions.md)中可用的功能和功能不同。

## 存取進階運算式編輯器 {#accessing-the-advanced-expression-editor}

進階運算式編輯器可用於：

* 建立[資料來源](../conditions.md#data_source_condition)及事件資訊的進階條件
* 定義自訂[等待活動](../wait-activity.md#custom)
* 定義動作參數對應

可能的話，您可以使用&#x200B;**[!UICONTROL 進階模式]** / **[!UICONTROL 簡單模式]**&#x200B;按鈕，在兩個模式之間切換。 [此處](../conditions.md#about_condition)會說明簡單模式。

>[!NOTE]
>
>* 可在簡單或進階運算式編輯器中定義條件。 它們一律會傳回布林值類型。
>
>* 藉由選取欄位或透過進階運算式編輯器，以定義動作參數。 他們會根據其運算式傳回特定資料類型。

您可以透過不同方式存取進階運算式編輯器：

* 當您建立資料來源條件時，可以按一下&#x200B;**[!UICONTROL 進階模式]**&#x200B;來存取進階編輯器。

  ![](../assets/journeyuc2_33.png)

* 建立自訂計時器時，會直接顯示進階編輯器。
* 當您對應動作引數時，請按一下&#x200B;**[!UICONTROL 進階模式]**。

>[!NOTE]
>
>若要使用自然語言提示來產生Journey運算式，請透過進階編輯器內的AI控制項，使用&#x200B;**[以AI](generate-expression.md)** (**public beta**)產生運算式。

## 探索介面 {#discovering-the-interface}

此畫面可讓您手動編寫運算式。

![](../assets/journey70.png)

在畫面左側，會顯示可用的欄位和函式：

* **[!UICONTROL 事件]**：選擇從傳入事件接收的其中一個欄位。 顯示的事件欄位清單會與情境相關，而且會根據歷程中新增的事件而有所不同。 [閱讀全文](../../event/about-events.md)

  >[!CAUTION]
  >
  >不支援使用體驗事件建立運算式。 使用體驗事件建立運算式/邏輯的替代方法和最佳實務已參考[這裡](../../building-journeys/exp-event-lookup.md)

* **[!UICONTROL 對象]**：如果您已卸除&#x200B;**[!UICONTROL 對象資格]**&#x200B;事件，請選擇您要在運算式中使用的對象。 [閱讀全文](../conditions.md#using-a-segment)
* **[!UICONTROL 資料來源]**：從資料來源欄位群組中的可用欄位清單中選擇。 [閱讀全文](../../datasource/about-data-sources.md)
* **[!UICONTROL 歷程屬性]**：此區段會將與特定設定檔之歷程相關的技術欄位重新分組。 [閱讀全文](journey-properties.md)
* **[!UICONTROL 函式]**：從允許執行複雜篩選的內建函式清單中選擇。 函式會依類別組織。 [閱讀全文](functions.md)

![](../assets/journey65.png)

自動完成機制會顯示內容建議。

![](../assets/journey68.png)

語法驗證機制會檢查程式碼的完整性。 錯誤會顯示在編輯器上方。

![](../assets/journey69.png)


>[!TIP]
>
>在進階運算式編輯器中建立條件時，請確定您的運算式不包含隱藏或不可列印的字元。 此外，請使用單行運算式，以避免剖析錯誤。


**使用進階運算式編輯器建立條件時，需要使用參數**

如果您從外部資料來源選取需要呼叫引數的欄位（請參閱[此頁面](../../datasource/external-data-sources.md)），右側會出現新索引標籤，讓您指定此引數。 引數值可能來自位於歷程或Experience Platform資料來源中的事件（而非其他外部資料來源）。 例如，在天氣相關資料來源中，常用的參數為 &quot;city&quot;。 因此，您必須選擇要取得此城市參數的位置。 也可將函式套用至參數，以執行格式變更或串聯。

![](../assets/journeyuc2_19.png)

對於更複雜的使用案例，如果您想將資料來源的參數包含在主運算式中，則可使用 &quot;params&quot; 關鍵字來定義其值。 請參閱[此頁面](../expression/field-references.md)。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面介紹Journey進階運算式編輯器 — 其存取點、介面面板，以及使用事件、資料來源、函式和運運算元來建立複雜條件、自訂等待計時器和動作引數對應的功能。

**意圖：**

* 從資料來源條件、自訂等待活動或動作引數對應存取進階運算式編輯器
* 使用事件欄位、資料來源欄位、對象成員資格和歷程屬性來建立進階布林條件
* 設定條件時，在簡單模式和進階模式之間切換
* 使用`params`關鍵字，直接在主要運算式中參考外部資料來源引數
* 使用AI支援的運算式產生功能，從自然語言提示建立運算式

**字彙表：**

* **進階運算式編輯器**：用於撰寫複雜運算式的Journey Optimizer程式碼編輯器；不同於較簡單的指向與點按條件編輯器&#x200B;*（產品特定）*
* **簡單模式**：點選條件編輯器；比進階編輯器更不靈活，但較容易提供給非開發人員使用&#x200B;*（產品特定）*
* **歷程屬性**：可在運算式編輯器&#x200B;*（產品特定）*&#x200B;中存取之歷程執行個體（識別碼、版本、錯誤、目前節點）的相關技術欄位
* **使用AI產生運算式**：進階編輯器中的AI支援功能（公開測試版），可從純文字提示產生運算式&#x200B;*（產品特定）*

**護欄：**

* 不支援直接使用體驗事件建立運算式 — 請使用其他方法，例如計算屬性
* 無論編輯器模式為何，條件一律會傳回布林值型別
* 運算式不得包含隱藏或不可列印的字元，且應使用單行格式以避免剖析錯誤
* 外部資料來源引數值只能來自歷程事件或Experience Platform資料來源，不能來自其他外部資料來源
* 進階運算式編輯器的功能與個人化編輯器中的功能不同

**術語：**

* 正式名稱：進階運算式編輯器 — 縮寫：無 — 變體：進階編輯器，運算式編輯器
* 同義字：「進階模式」=「進階運算式編輯器」
* 請勿混淆：進階運算式編輯器（歷程條件/動作）≠個人化編輯器（訊息內容個人化）

**常見問題集：**

* **問：何時必須使用進階運算式編輯器，而非簡單模式？**  — 當您需要查詢集合、使用函式、參考歷程屬性或建立簡單編輯器無法表示的多條件邏輯時，請使用進階編輯器。
* **問：如何將引數傳遞至運算式中的外部資料來源？**  — 在運算式語法中使用`params`關鍵字，例如`#{DataSource.fieldGroup.field, params: {paramName: value}}`。
* **問：自動完成機制有什麼作用？**  — 它會在您輸入時顯示內容欄位和函式建議，協助您更快建立有效的運算式。
* **問：存取AI的Generate運算式位於何處？**  — 透過進階運算式編輯器中的AI控制項；目前為公開測試版。
* **問：進階編輯器中的條件是否傳回與簡單模式不同的型別？** — No；兩種模式中，條件一律會傳回布林值。

+++
