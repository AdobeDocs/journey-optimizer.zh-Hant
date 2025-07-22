---
solution: Journey Optimizer
product: journey optimizer
title: 使用外部端點的資料個人化內容
description: 瞭解如何從外部端點動態擷取資料，以個人化傳入內容。
badge: label="有限可用性" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 0%

---


# 使用外部端點的資料個人化內容 {#data-endpoint}

>[!AVAILABILITY]
>
>此功能僅適用於一組組織（可用性限制）。

Journey Optimizer可讓您運用外部端點的資料，在傳入頻道（例如程式碼型體驗、網頁和應用程式內訊息頻道）中個人化您的內容。

若要這麼做，個人化編輯器中會提供專屬的協助程式功能`externalDataLookup`。 若要使用協助程式，您必須先定義一個[!DNL Journey Optimizer] **動作**，您可在其中設定有關外部端點的詳細資訊。

## 必讀

### 執行階段執行

當輸入動作包含externalDataLookup協助程式時，會在[!DNL Adobe Experience Platform] Edge Network收到並處理個人化要求時動態呼叫端點。 這表示外部端點至少需要能夠處理使用者端針對指定表面傳送至AEP Edge Network的並行負載和輸送量。

### Authentication

externalDataLookup協助程式目前不支援動作設定中的驗證選項。
同時，針對API金鑰式驗證或其他純文字授權金鑰，您可以在動作設定中將它們指定為標頭欄位。
僅適用於Adobe內部端點：聯絡AJO工程部門以啟用端點的服務權杖型驗證。

### 護欄和限制

也請參閱AJO傳入頻道行銷活動和Journeys#GuardrailsandGuidelines中的自訂動作。

依預設，AJO在呼叫外部端點時會使用300毫秒的逾時。 請聯絡AJO工程部門以提高端點的此逾時。
在Personalization編輯器中，AJO不允許您在插入運算式時瀏覽端點回應的結構描述，且不會驗證運算式中所使用回應的JSON屬性參考。
透過externalDataLookup協助程式替代的承載變數引數支援的資料型別為字串、整數、小數、布林值、listString、listInt、listInteger、listDecimal
對動作設定的變更不會反映在即時行銷活動和歷程中的對應externalDataLookup呼叫。 為了反映變更，您需要複製或修改任何在externalDataLookup協助程式中使用動作的即時行銷活動或歷程。
尚不支援在外部資料查詢協助程式引數中使用變數。
目前不支援動態URL路徑。   — 傳入自訂動作增強功能#DynamicPathSegments

## 建立動作

建立動作來設定查閱的端點。 每個端點只需要完成一次，且應由技術使用者完成。 請參閱此頁面。

相同的動作可用於&#x200B;**[!UICONTROL 自訂動作]**&#x200B;活動中以擷取歷程中的內容，也可用於`externalDataLookup`協助程式函式中，以擷取歷程或行銷活動中傳入動作的資料。

瀏覽至&#x200B;**[!UICONTROL 管理]** / **[!UICONTROL 組態]**&#x200B;功能表。

記下動作ID，並複製它以用於步驟6。


## 使用擷取的資料個人化您的內容

### 將協助程式函式新增至您的內容

1. 建立傳入行銷活動或歷程動作並編輯其內容。

1. 找出您要在其中使用從外部端點取得的資料的內容，並存取個人化編輯器。

1. 選取[協助程式功能]功能表，並找到`externalDataLookup`協助程式功能。

1. 選取將相關語法插入程式碼中，並取代`actionId`和`result`引數值，如下所示：

   * `actionId` ：貼上建立動作時複製的action nID。
   * `result`：將此引數設定為您選擇的名稱。 您將使用此結果變數來存取擷取的內容。

1. 新增任何變數引數值，以作為端點呼叫的一部分傳遞。 例如，以下說明如何傳遞語言引數和最大專案引數。

### 使用擷取的資料進行個人化

若要存取從外部端點查詢呼叫擷取的資料，您可以使用個人化運算式和協助程式函式，參考動作定義中回應裝載所定義的欄位。

使用`result`變數來存取擷取的資料，並將其插入傳入動作的內容中。 例如，以下說明如何傳回從端點擷取的JSON專案陣列。

讓我們以下列範例為例，動作中的回應裝載已設定如下：

```
{
    "videos": [
        {
            "id": "integer",
            "title": "string",
            "description": "string",
            "thumbnail_url": "string",
            "video_page_url": "string",
            "url": "string",
            "video_type": "string",
            "start_timestamp": "dateOnly",
            "created_on": "dateOnly",
            ...
        }
    ]
}
```

Personalization範例1 — 在程式碼型Experience HTML動作中顯示第一部影片的說明：

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Personalization範例2 — 在程式碼型體驗JSON動作中傳回專案陣列：

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
[
{{#each result.videos as |item|}}
    {                                                  
        "title": "{{item.title}}",
        "url": "{{item.video_page_url}}",
        "thumbnail_url": "{{item.thumbnail_url}}",
        "start_timestamp": "{{item.start_timestamp}}"
    },
{{/each}}
]
```

## 逾時和錯誤處理

AJO在呼叫外部端點時使用嚴格的逾時，以維護AEP Edge Network的低延遲、高輸送量的效能特性。

如果端點逾時或到達端點時發生任何其他型別的錯誤，則結果變數將為空白。 在此情況下，結果變數內對屬性的任何參照也將是空的。 如果您只顯示內容中的屬性，則會顯示為空白。 如果您嘗試在結果中重複執行陣列屬性，將不會傳回任何專案。

如果您想要更順暢地處理逾時或錯誤，藉由顯示遞補內容，您可以檢查查詢結果是否為空白，並在該情況下顯示遞補內容。

例如，您可以顯示單一屬性的遞補值，如下所示：

第一個視訊描述： {%=result.videos[0].description ？： &quot;none found&quot; %}


或者，您可以有條件地呈現整個內容區塊，如下所示：

{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}

{%#if result%}
...對結果執行動作……
{%else%}
...傳回遞補內容……
{%/if%}
偵錯
為協助進行偵錯，外部資料查詢的逾時和錯誤詳細資料包含在AEP Assurance的Edge Delivery檢視中。 如果您在傳入動作中看不到externalDataLookup協助程式的預期結果，您可以啟動Assurance工作階段、從網路或行動實作起始AJO呼叫，並使用Edge Delivery檢視來檢查逾時或錯誤詳細資訊。

例如：

在執行詳細資訊中，在保證追蹤的Edge Delivery區段底下新增了一個新的customActions區塊，

要求和回應的詳細資料，類似於以下內容。 如果在執行自訂動作時發生任何問題，錯誤區段應該有助於進行偵錯

## 常見問題

+++如何將內容屬性從請求以引數的形式傳遞至外部資料查詢？

使用內容屬性>資料串流>事件功能表來瀏覽您使用的體驗事件結構，並插入相關屬性作為引數值，如下所示：

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

+++

+++AJO是否對外部端點回應執行任何快取？

目前不會。 未來將支援此功能。

+++









語法
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}



傳遞引數
呼叫外部端點時，動作中定義的所有常數標頭值、查詢引數和要求裝載值，都會隨動作設定中指定的值傳送。

對於任何變數標頭值、查詢/路徑引數或要求裝載值，您可以使用引數將值動態傳遞至externalDataLookup協助程式。

引數名稱：

標題引數：標題。<parameter-name>
查詢引數：查詢。<parameter-name>
裝載引數：裝載。<parameter-name>
路徑引數： dynamic_path。<parameter-name>
例如：

{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}
引數值可以是固定值，也可以透過參考設定檔欄位或其他內容屬性進行個人化，例如：

{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
可使用點標籤法提供裝載引數，以參考巢狀JSON屬性，例如：

{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}