---
solution: Journey Optimizer
product: journey optimizer
title: 使用外部整合
description: 將外部整合整合整合至管道製作程式，以個人化和動態資訊（包括Adobe Target傳送API回應）豐富內容
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: 整合
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: d16f7424-4847-4b90-a37c-4b52cbdabee5
source-git-commit: 2668028bbdf9299aed836fecea983c548ce74d8e
workflow-type: tm+mt
source-wordcount: 1302
ht-degree: 1%

---


# 使用外部整合進行個人化 {#integrations-personalization}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解行銷人員如何套用已設定的整合來個人化電子郵件、簡訊和推播內容，並將一個API呼叫鏈結到另一個以取得更豐富的動態訊息。

>[!ENDSHADEBOX]

在內容中使用外部整合之前，請確認管理員已設定&#x200B;**並啟動**&#x200B;每個整合（端點、驗證、原則、回應裝載和啟動），如[使用整合](integrations.md)中所述。

您可以在訊息上新增每個&#x200B;**[!UICONTROL 片段]**&#x200B;最多&#x200B;**3**&#x200B;個整合，以及最多&#x200B;**5**&#x200B;個整合。 僅來自片段的整合不會計入&#x200B;**5**。

## 將整合個人化套用至您的內容 {#apply-integration-personalization}

身為行銷人員，您可以使用已設定的整合來個人化您的內容。 請依照下列步驟操作：

1. 存取您的行銷活動內容，然後按一下[文字]或[HTML **[!UICONTROL 元件]**]中的[新增個人化&#x200B;]&#x200B;**。**

   [進一步瞭解元件](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. 瀏覽至&#x200B;**[!UICONTROL 整合]**&#x200B;區段，然後按一下&#x200B;**[!UICONTROL 開啟整合]**&#x200B;以檢視所有使用中的整合。

   請注意，**Journey Optimizer片段**&#x200B;可與整合搭配使用，但僅支援傳出頻道。 片段發佈後，會停用新增和儲存新的整合，以避免對現有歷程和行銷活動造成影響。

   ![](assets/external-integration-content-2.png)

1. 選取整合併按一下&#x200B;**[!UICONTROL 儲存]**。

   ![](assets/external-integration-content-3.png)

1. 啟用&#x200B;**[!UICONTROL Pills]**&#x200B;模式以解除鎖定進階整合功能表。

   ![](assets/external-integration-content-4.png)

1. 當您編寫整合個人化時，整合協助程式會包含&#x200B;**`required`**&#x200B;欄位，以定義失敗或遺失資料如何與預設內容互動：

   * **`required=true`** （預設）：該訊息的轉譯停止。 此傳送已與&#x200B;**`ExternalDataLookupExclusion`**&#x200B;一起排除，而且此排除記錄在&#x200B;**訊息意見資料集**&#x200B;中。
   * **`required=false`**：結果變數已設為&#x200B;**`null`**，且轉譯作業會繼續進行。 在範本中使用預設文字、後援或條件式邏輯，這樣在整合未傳回資料時，設定檔就不會接收空白內容。

     ![](assets/external-integration-content-8.png)

1. 若要完成整合設定，請定義先前在[組態](integrations.md#configure)期間指定的整合屬性。

   您可以使用靜態值（保持常數）或設定檔屬性（動態地從使用者設定檔中提取資訊）來指派值給這些屬性。

   ![](assets/external-integration-content-5.png)

1. 定義整合屬性後，您現在可以按一下![新增](assets/do-not-localize/Smock_Add_18_N.svg)圖示，將內容中的整合欄位用於個人化傳訊。

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >範本中的權杖只能使用管理員在整合設定中公開的欄位。 例如，`{{weatherResponse.temperature}}`在`temperature`公開時有效；如果`humidity`未公開，編輯器中會拒絕`{{weatherResponse.humidity}}`。

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

您的整合個人化現在已成功套用至您的內容，確保每位收件者都能根據您設定的屬性獲得量身打造的相關體驗。

![](assets/external-integration-content-7.png)

## 將一個API呼叫對應至另一個API呼叫 {#map-integration-chain}

您可以連結整合，讓某個呼叫的結果饋送至下一個呼叫，例如路徑區段、標題或查詢引數。 這些呼叫會在相同的訊息中依序執行，支援更豐富的個人化，而不需要自訂程式碼。

開始之前，請確定：

* 管理員已設定並啟動您所需的每項整合。 請參閱[設定整合](integrations.md)。
* 變數路徑預留位置、標題和查詢引數是在具有行銷人員專用標籤的整合設定中設定。
* 管理員會在每個整合的&#x200B;**[!UICONTROL 回應承載]**&#x200B;中公開您所需的回應欄位，以便在編寫時顯示。

以下範例使用訂位整合，從設定檔的預訂傳回航班號碼，然後使用航班資訊整合，將該號碼用於即時狀態（延遲、目的地）。 將第二個整合的輸入對應到第一個呼叫的回應。

1. 開啟您的訊息或片段，然後開啟個人化編輯器。

   ![](assets/uc-integrations-1.png)

1. 在&#x200B;**[!UICONTROL 整合]**&#x200B;中，按一下&#x200B;**[!UICONTROL 開啟整合]**。

   ![](assets/uc-integrations-2.png)

1. 新增其回應將饋送下個呼叫的整合，例如，包括航班識別碼的預訂或預訂資料。

   ![](assets/uc-integrations-3.png)

1. （選用）如果要將具名變數繫結到保留回應，請開啟&#x200B;**[!UICONTROL 協助程式函式]**&#x200B;功能表，並新增協助程式，例如`Let`函式。

   >[!NOTE]
   >
   > 只有管理員定義的&#x200B;**[!UICONTROL 回應承載]**&#x200B;中公開的欄位才可用。 您無法參考設定中未公開的屬性。

1. 如果您使用協助程式變數，請將該變數對應至預訂整合傳回以供下游使用的欄位，例如，乘客或預訂裝載中的航班號碼。

   ![](assets/uc-integrations-4.png)

1. 從&#x200B;**[!UICONTROL 開啟整合]**&#x200B;功能表，新增第二個整合，例如，航班狀態。

   ![](assets/uc-integrations-5.png)

1. 在第二個整合中，開啟&#x200B;**[!UICONTROL 整合屬性]**。 對於必須重複使用來自第一次呼叫的資料的每個輸入，例如路徑變數、標題或查詢引數，請從第一次整合回應中選取對應來源。

   在&#x200B;**[!UICONTROL Pills]**&#x200B;體驗中，您可以將第一次呼叫輸出直接對應到第二次呼叫輸入，而不需要`Let`陳述式。 如果您使用`Let`，可以改為透過該變數進行對應。

   ![](assets/uc-integrations-6.png)

1. 使用![新增](assets/do-not-localize/Smock_Add_18_N.svg)控制項（例如航班資訊回應的目的地），將第二次整合的Token插入內容。

   ![](assets/uc-integrations-8.png)

1. 儲存您的內容。

在&#x200B;**[!UICONTROL 模擬]**&#x200B;或傳送上，Journey Optimizer會依下列順序執行整合：第一個呼叫使用您設定的設定檔內容，其結果會建置第二個要求。 指定的整合是在模擬或傳送時間執行，取決於您的設定和管道。

![](assets/uc-integrations-7.png)

## 在範本中使用Adobe Target資料 {#use-adobe-target-in-templates}

本節說明如何在Adobe Journey Optimizer中使用&#x200B;**整合**，在傳送時從&#x200B;**[!DNL Adobe Target]**&#x200B;擷取個人化資料，並將其用於訊息範本。 此變數假設Target傳送API已設定為整合。

如需設定步驟，請參閱[使用整合](integrations.md)和[Adobe Target Recommendations](vendor-integration.md#adobe-target-recommendations)範例。

Target傳送API傳回`prefetch.mboxes`陣列。 每個mbox包含具有`content`和`type`欄位的`options`物件。 `type`值決定您在範本中使用`content`的方式。 開啟與您的mbox回應相符的標籤，然後依照步驟在訊息中使用該資料。

>[!BEGINTABS]

>[!TAB JSON內容]

當`type`是`json`時，`content`欄位是&#x200B;**JSON字串**。 在存取巢狀欄位之前先加以剖析。 以下範例顯示JSON mbox的典型傳送API回應。

```json
{
  "status": 200,
  "prefetch": {
    "mboxes": [
      {
        "index": 0,
        "name": "SummerOffer",
        "options": {
          "content": "{\"recommendations\":[{\"productId\":\"p101\",\"name\":\"Noise Smartwatch\",\"price\":2999},{\"productId\":\"p205\",\"name\":\"Boat Earbuds\",\"price\":1499}],\"strategy\":\"collaborative-filtering\"}",
          "type": "json"
        }
      }
    ]
  }
}
```

依序使用三個協助程式來擷取、擷取及剖析Target回應。

1. **擷取目標回應。** 呼叫您設定的Target與`externalDataLookup`的整合。 將`integrationName`設定為該整合的&#x200B;**[!UICONTROL 名稱]** （取代範例預留位置`target_recommendations`）。 使用`result`引數來命名包含完整傳送API裝載的範本變數，例如`targetResponse`。

   您也可以在個人化編輯器左側導覽的&#x200B;**[!UICONTROL 整合]**&#x200B;功能表中，直接選取整合。 請參閱[將整合個人化套用至您的內容](#apply-integration-personalization)。

   ```handlebars
   {{externalDataLookup integrationName="target_recommendations" result="targetResponse"}}
   ```

1. **使用valueAtPath擷取特定mbox。** `valueAtPath`透過其以0為基礎的索引從陣列中擷取元素，並將其指派給範本變數。 使用`idx`引數指定要存取的元素。

   ```handlebars
   {{valueAtPath targetResponse.prefetch.mboxes idx=0 result="summerOffer"}}
   ```

   | 參數 | 說明 |
   | --- | --- |
   | `path` | 陣列的路徑（位置，無關鍵字） |
   | `idx` | 0型索引，用於陣列存取（選擇性） |
   | `result` | 儲存擷取值的變數名稱 |

   >[!NOTE]
   >
   > 如果`idx`超出範圍，演算會擲回例外狀況。 當索引可能無效時，保護具有`{%#if idx >= 0 and idx < count(targetResponse.prefetch.mboxes)%}`的無效索引。 PQL運算式無法當作路徑使用。 **自2025.9.0發行後可用。**

1. **使用parseJson剖析JSON字串。** mbox `options.content`欄位是原始JSON字串。 `parseJson`將其轉換為結構化物件，然後可以在範本中直接存取其欄位。

   ```handlebars
   {{parseJson jsonStr=summerOffer.options.content result="summerOfferContent"}}
   ```

   | 參數 | 說明 |
   | --- | --- |
   | `jsonStr` | 包含有效JSON的字串欄位的路徑 |
   | `result` | 儲存剖析物件的變數名稱 |

   >[!NOTE]
   >
   > 如果JSON字串無效或參考為Null，則`result`設定為`null` — 不會擲回演算錯誤。 以您的實際Target回應進行測試，以確認內容是有效的JSON。 **推出日期： 2026.6.0**

1. **存取資料。** 剖析後，請使用點標籤法來存取`summerOfferContent`中的欄位。 若要呈現建議清單：

   ```handlebars
   {{externalDataLookup integrationName="target_recommendations" result="targetResponse"}}
   {{valueAtPath targetResponse.prefetch.mboxes idx=0 result="summerOffer"}}
   {{parseJson jsonStr=summerOffer.options.content result="summerOfferContent"}}
   
   Strategy: {{summerOfferContent.strategy}}
   {{#each summerOfferContent.recommendations as |rec|}}
     {{rec.name}} — {{rec.price}}
   {{/each}}
   ```

>[!TAB HTML內容]

當`type`為`html`時，`content`欄位是準備呈現的HTML字串。 您不需要剖析。 以下範例顯示HTML mbox的典型傳送API回應。

```json
{
  "status": 200,
  "prefetch": {
    "mboxes": [
      {
        "index": 0,
        "name": "SummerOffer",
        "options": {
          "content": "<div class=\"offer\"><h2>Summer Sale</h2><p>50% off Smartwatch</p></div>",
          "type": "html"
        }
      }
    ]
  }
}
```

擷取並擷取mbox，然後直接轉譯`content`。 略過`parseJson`。

```handlebars
{{externalDataLookup integrationName="target_recommendations" result="targetResponse"}}
{{valueAtPath targetResponse.prefetch.mboxes idx=0 result="summerOffer"}}
{{{summerOffer.options.content}}}
```

>[!NOTE]
>
> 使用&#x200B;**三重大括弧** `{{{...}}}`將HTML內容依原樣呈現。 雙大括弧`{{...}}`將逸出HTML實體並轉譯原始標籤字串而非HTML。

>[!ENDTABS]

## 作法影片 {#video}

此影片說明&#x200B;**整合**&#x200B;如何將Adobe Journey Optimizer連線至外部API，以便您可以將即時資料和內容提取至&#x200B;**傳出頻道**&#x200B;電子郵件、簡訊和推播，以進行更相關的個人化。

>[!VIDEO](https://video.tv.adobe.com/v/3484118/?learn=on)
