---
solution: Journey Optimizer
product: journey optimizer
title: 使用動態片段
description: 瞭解如何在Adobe Journey Optimizer中使用動態片段解析，根據設定檔屬性、資料集查詢或內容資料在執行階段選取和插入片段。
feature: Fragments
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: 動態，片段，運算式，個人化，執行階段
source-git-commit: b4affc5b905236419928a65cd173173b49058827
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 2%

---

# 使用動態片段 {#dynamic-fragments}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何在Adobe Journey Optimizer中使用動態片段解析，以根據設定檔屬性、資料集查詢或傳送時傳遞的內容資料，選取在執行階段插入訊息中的已發佈片段。

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer]在執行階段支援&#x200B;**動態片段解析度**，可讓您根據傳送時傳遞的設定檔屬性、資料集查詢或內容資料，選取要插入訊息中的已發佈片段。 如此一來，可啟用高度個人化的內容，而不會複製行銷活動或歷程邏輯。

## 概觀 {#overview}

**靜態片段**&#x200B;在設計階段內嵌於郵件中 — 每個收件者都使用相同的片段。 **動態片段**&#x200B;會在每個收件者的執行階段解析片段ID，這表示不同的設定檔可以在同一個行銷活動或歷程中接收完全不同的內容區塊。

動態片段ID可以來自三個來源：

* **資料集查詢** — 例如，以樣式或產品作為關鍵字的建議資料集
* 儲存在Adobe Experience Platform中的&#x200B;**設定檔屬性**
* 傳送時直接在API要求中傳遞&#x200B;**內容資料**

>[!NOTE]
>
>目前在運算式片段中使用`datasetLookup`協助程式函式僅供有限的客戶使用。 若想取得存取權，請聯絡您的 Adobe 代表。

## 先決條件 {#prerequisites}

在使用動態片段之前，請確定已具備下列專案：

* 您擁有在[!DNL Journey Optimizer]中建立和發佈片段的必要許可權。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)
* 您打算參考的片段是&#x200B;**已發佈** （狀態： **即時**）。 在執行階段無法解析草稿片段。
* 如果從資料集解析片段ID，資料集結構描述會包含儲存片段ID的欄位，而且資料集已[啟用查詢](../data/lookup-aep-data.md)。
* 動態片段本身參考的所有設定檔屬性都會包含在訊息匯出路徑中，或在傳送時可用於設定檔中。

>[!CAUTION]
>
>動態片段流程中會略過片段相關的驗證。 無效的片段ID顯示為執行階段傳遞失敗，而不是預先驗證錯誤。 在啟動行銷活動之前，請務必確認參考的片段ID是否有效且已發佈。

## 步驟1：建立並發佈片段 {#create-fragment}

在動態參考片段之前，必須在[!DNL Journey Optimizer]中發佈該片段。

1. 在[!DNL Journey Optimizer]中，瀏覽至&#x200B;**[!UICONTROL 內容管理]** > **[!UICONTROL 片段]**。

1. 選取&#x200B;**[!UICONTROL 建立片段]**&#x200B;並編寫內容。 [瞭解如何建立片段](create-fragments.md)

1. 當內容準備就緒時，按一下&#x200B;**[!UICONTROL 發佈]**。 發佈為非同步，可能需要幾秒鐘的時間。 繼續之前，請確認片段狀態變更為&#x200B;**即時**。

1. 從片段詳細資料檢視或片段API回應中記下&#x200B;**片段ID**。 您將在訊息中參考此ID。

>[!NOTE]
>
>您可以使用`GET /fragments` API以程式設計方式擷取所有已發佈的片段ID。 如需詳細資訊，請參閱[Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}。

## 步驟2：使用動態片段參考編寫訊息 {#author-message}

在個人化編輯器中，使用下列語法插入動態片段預留位置：

```handlebars
{{fragment id=dynamic_fragment_id}}
```

識別碼`dynamic_fragment_id`是變數名稱。 它的值必須在片段查詢發生之前解析。 您可以使用資料集查詢運算式、設定檔屬性或內容資料來加以解析。

### 從資料集查詢中解析 {#resolve-from-dataset}

如果片段ID儲存在AEP資料集中（例如，樣式對片段對應表格），請使用`datasetLookup`協助程式函式進行解析：

```handlebars
{{
  {datasetLookup datasetId="<your-dataset-id>" key=profile.style attribute="fragmentId"}
}}

{{fragment id=dynamic_fragment_id}}
```

在此範例中，資料集包含樣式值（例如`style1`）所輸入的列。 對於指定的設定檔，查詢會擷取對應的`fragmentId`欄值，並將其指派給`dynamic_fragment_id`，然後用來解析片段。

>[!NOTE]
>
>目前在運算式片段中使用`datasetLookup`協助程式函式僅供有限的客戶使用。 若想取得存取權，請聯絡您的 Adobe 代表。 如需個人化資料集查詢的詳細資訊，請參閱[使用Adobe Experience Platform資料](../data/lookup-aep-data.md)。

### 從內容資料解析 {#resolve-from-context}

如果在傳送時提供片段ID做為API要求內容的一部分，請使用`context`名稱空間參考它：

```handlebars
{{fragment id=context.audiencePayload.fragmentId}}
```

路徑`context.audiencePayload`是所有屬性必要的首碼，這些屬性來源為CSV對象檔案或透過API要求內容傳遞。 來自CSV的欄名稱（例如，`fragmentId`）會接在首碼之後。

### 從設定檔屬性解析 {#resolve-from-profile}

如果片段ID儲存為Adobe Experience Platform中的設定檔屬性，請直接參照它：

```handlebars
{{fragment id=profile.mi.fragmentId}}
```

## 步驟3：針對查詢方法設定資料集 {#configure-dataset}

如果您使用資料集查詢方法，請更新您的資料集結構和資料以攜帶片段ID。

1. 在您的建議或對應資料集中，新增欄（例如，`fragmentId`）以儲存每一列的已發佈AJO片段ID。

1. 對於每個樣式或變體（例如，`style1`、`style2`），請以對應的片段ID填入`fragmentId`欄。

1. 確定資料集已擷取至Adobe Experience Platform中，[已啟用查詢](../data/lookup-aep-data.md)。

1. 確認動態片段內參考的所有設定檔屬性都會擷取到訊息或靜態片段中，以防止在匯出時呈現空白。

**範例資料集結構：**

| 欄 | 範例值 |
|---|---|
| 樣式 | style1 |
| fragmentId | &lt;fragment-id-1> |
| 樣式 | style2 |
| fragmentId | &lt;fragment-id-2> |

## 步驟4：在傳送時傳遞內容資料 {#pass-context-data}

如果您要從內容資料（例如，從CSV對象建議檔案）解析片段ID，請在API請求中在所需的內容首碼下傳遞片段ID。

使用行銷活動校樣API時，請在`context`物件中包含片段ID：

```json
{
  "recipients": [
    {
      "userId": "<profile-email>",
      "namespace": "email"
    }
  ],
  "inChannelData": {
    "channel": "email",
    "emailAddresses": ["<delivery-address>"]
  },
  "context": {
    "audiencePayload": {
      "fragmentId": "<published-fragment-id>",
      "systemSource": "<optional-system-value>"
    }
  }
}
```

前置詞`context.audiencePayload`為必填。 執行即時行銷活動時，巢狀在此索引鍵下方的屬性會直接對應至CSV對象檔案中的欄。

## 步驟5：證明和驗證 {#proof-validate}

在啟用行銷活動之前，請使用行銷活動校樣API來確認動態片段正確解析，且轉譯的電子郵件輸出符合預期。

1. 使用`POST /campaigns/{id}/proofs`端點觸發校訂工作。 在校訂請求中，傳遞您要在`context.audiencePayload.fragmentId`下測試的片段ID。

1. 使用`GET /campaigns/{id}/proofs/{proofId}`端點輪詢校訂工作狀態，直到狀態為`Submitted`或`Failed`。

1. 檢查已傳送的電子郵件，以確認已呈現正確的片段內容。

1. 如果片段內容遺失或不正確，請確認片段ID有效、片段已發佈，且存在所有必要的設定檔屬性。

如需促銷活動API的詳細資訊，請參閱[Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"}。

## 護欄與限制 {#guardrails}

>[!CAUTION]
>
>動態片段模型中的片段未強制使用OLAC （物件層級存取控制）。 確保在行銷活動和對象層級考慮您的存取控制需求。

下列限制適用於使用動態片段：

* **匯出時的設定檔屬性涵蓋範圍**：在執行階段為每個設定檔選擇片段。 動態片段所需的設定檔屬性事先未知。 如果動態片段所依賴的設定檔屬性不存在於原始訊息或訊息中參考的任何靜態片段中，則匯出路徑中可能會呈現空白欄位。

* **沒有預先片段驗證**：此流程中略過片段相關的驗證。 不正確或未發佈的片段ID會顯示為執行階段傳送失敗，而非UI中顯示的驗證錯誤。

* **資料集方法所需的結構描述變更**：使用依識別碼查詢路徑需要更新資料集結構描述，以儲存並傳遞片段ID，加上將其傳入訊息管道所需的管道。

* **匯出的屬性擷取**：請確定動態片段內使用的所有屬性都已在訊息或靜態片段中擷取，以防止匯出路徑中出現空白轉譯。

[此區段](../start/guardrails.md#fragments-guardrails)中有更多套用至片段的護欄。

## 錯誤處理 {#error-handling}

如果動態片段在執行階段無法解析，則會為受影響的設定檔產生排除事件。 目前，所有片段呈現失敗都歸類為單一總括錯誤型別。

若要偵錯片段解析失敗：

1. 檢查行銷活動傳遞報告中的排除事件。
1. 確認在執行階段傳遞的片段ID符合發佈的片段。
1. 確認片段所需的所有設定檔屬性在傳送時都存在於設定檔中。
1. 在啟動行銷活動之前，使用[校訂API](#proof-validate)測試特定片段ID。
