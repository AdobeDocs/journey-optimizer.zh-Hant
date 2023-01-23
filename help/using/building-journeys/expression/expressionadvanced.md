---
solution: Journey Optimizer
product: journey optimizer
title: 關於進階運算式編輯器
description: 瞭解如何建立進階運算式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 運算式編輯器，資料，歷程
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 65%

---

# 關於進階運算式編輯器 {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="關於進階運算式編輯器"
>abstract="使用進階運算式編輯器，在介面的各種畫面中建立進階運算式。 例如，您可以在設定和使用歷程時，以及定義資料來源條件時建立運算式。"

使用進階運算式編輯器，在介面的各種畫面中建立進階運算式。 例如，您可以在設定和使用歷程時，以及定義資料來源條件時建立運算式。
此外，您每次必須定義需要特定資料處理的動作參數時，都可以使用它。您可以善用來自事件的資料或是從資料來源擷取的其他資訊。在歷程中，顯示的事件欄位清單會與情境相關，而且會根據歷程中新增的事件而有所不同。

進階運算式編輯器提供一組內建函式和運算子，讓您得以控制值並定義特別符合您需求的運算式。進階運算式編輯器也可讓您定義外部資料來源參數的值、控制對應欄位和集合，例如體驗事件。

![](../assets/journey65.png)

_進階運算式編輯器介面_

進階運算式編輯器可用於：

* 建立[資料來源](../condition-activity.md#about_condition)及事件資訊的進階條件
* 定義自訂[等待活動](../wait-activity.md#custom)
* 定義動作參數對應

如有可能，您可以使用 **[!UICONTROL 進階模式]** / **[!UICONTROL 簡單模式]** 按鈕。 [此處](../condition-activity.md#about_condition)會說明簡單模式。

>[!NOTE]
>
>可在簡單或進階運算式編輯器中定義條件。它們一律會傳回布林值類型。
>
>藉由選取欄位或透過進階運算式編輯器，以定義動作參數。他們會根據其運算式傳回特定資料類型。

## 存取進階運算式編輯器 {#accessing-the-advanced-expression-editor}

您可以透過不同方式存取進階運算式編輯器：

* 建立資料來源條件時，可按一下 **[!UICONTROL 進階模式]**.

   ![](../assets/journeyuc2_33.png)

* 建立自訂計時器時，會直接顯示進階編輯器。
* 對應動作參數時，按一下 **[!UICONTROL 進階模式]**.

## 探索介面{#discovering-the-interface}

此畫面可讓您手動編寫運算式。

![](../assets/journey70.png)

在畫面左側，會顯示可用的欄位和函式：

* **[!UICONTROL 事件]**:從入站事件接收的其中一個欄位。 顯示的事件欄位清單會與情境相關，而且會根據歷程中新增的事件而有所不同。[閱讀全文](../../event/about-events.md)
* **[!UICONTROL 區段]**:如果你掉了 **[!UICONTROL 區段資格]** 事件，選擇您要在運算式中使用的區段。 [閱讀全文](../condition-activity.md#using-a-segment)
* **[!UICONTROL 資料來源]**:從資料來源欄位群組中的可用欄位清單中選擇。 [閱讀全文](../../datasource/about-data-sources.md)
* **[!UICONTROL 歷程屬性]**:本節會重新分組指定設定檔之歷程的相關技術欄位。 [閱讀全文](journey-properties.md)
* **[!UICONTROL 函式]**:從可執行複雜篩選的內建函式清單中選擇。 函式會依類別組織。[閱讀全文](functions.md)

![](../assets/journey65.png)

自動完成機制會顯示內容建議。

![](../assets/journey68.png)

語法驗證機制會檢查程式碼的完整性。錯誤會顯示在編輯器上方。

![](../assets/journey69.png)

**使用進階運算式編輯器建立條件時，需要使用參數**

如果您從外部資料來源選取欄位，需要呼叫參數(請參閱 [本頁](../../datasource/external-data-sources.md). 例如，在天氣相關資料來源中，常用的參數為 &quot;city&quot;。因此，您必須選擇要取得此城市參數的位置。也可將函式套用至參數，以執行格式變更或串聯。

![](../assets/journeyuc2_19.png)

對於更複雜的使用案例，如果您想將資料來源的參數包含在主運算式中，則可使用 &quot;params&quot; 關鍵字來定義其值。請參閱[本頁](../expression/field-references.md)。
