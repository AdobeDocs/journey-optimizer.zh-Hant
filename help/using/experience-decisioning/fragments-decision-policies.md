---
title: 在決策原則中善用片段
description: 瞭解如何在決策原則中運用片段
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
TQID: https://experienceleague.adobe.com/5Vpngi03UnC9YPlB5tdTRcd0NoT7iglH2pRDkmeZKOg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 1918bcb699ea6a4063be28941a30bb6c6ade21ce
workflow-type: tm+mt
source-wordcount: 1743
ht-degree: 0%

---

# 在決策原則中善用片段 {#fragments}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;在決定原則中運用Journey Optimizer內容片段和AEM內容片段，以便個人化並最佳化跨管道的內容決定傳送。

>[!ENDSHADEBOX]

決策專案支援兩種型別的片段內容，在決策原則內編寫訊息時可運用這些內容：

* **Journey Optimizer內容片段** — 在Journey Optimizer中建立且可重複使用的運算式片段，並新增至決定專案的&#x200B;**[!UICONTROL 片段]**&#x200B;區段。 [進一步瞭解AJO內容片段](../content-management/fragments.md)
* **AEM內容片段** — 在Adobe Experience Manager中撰寫的內容、對應至決定專案的屬性，以及透過索引鍵名稱在個人化編輯器中選取的內容。 [瞭解如何將AEM內容片段連結至決定專案](items.md#aem-fragments)

## Journey Optimizer內容片段 {#ajo-fragments}

如果您的決策原則包含決策專案，包括AJO內容片段，您可以在決策原則內的所有可用決策管道（程式碼型體驗、電子郵件、推播、簡訊和歷程）中製作訊息時，利用這些片段。

例如，假設您想針對多種行動裝置型號顯示不同的內容。 將每個屬於不同電話型號的指定片段新增至您在決定原則中使用的決定專案。 [瞭解如何新增片段至決定專案](items.md#attributes)。

![決策專案的片段區段，顯示片段參考和位置索引鍵。](assets/item-fragments.png){width=70%}

完成後，您可以使用下列其中一種方法：

>[!BEGINTABS]

>[!TAB 直接插入代碼]

只要將下方的程式碼區塊複製並貼到決定原則程式碼中即可。 以片段ID取代`variable`，並以片段參考索引鍵取代`placement`：

```handlebars
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable required=false}}
```

>[!TAB 遵循詳細步驟]

1. 導覽至&#x200B;**[!UICONTROL 協助程式函式]**，並將&#x200B;**Let**&#x200B;函式`{% let variable = expression %} {{variable}}`新增至程式碼窗格，您可以在其中宣告片段的變數。

   ![決定原則程式碼編輯器顯示Let helper函式已新增至程式碼窗格。](assets/decision-let-function.png)

1. 使用&#x200B;**Map** > **Get**&#x200B;函式`{%= get(map, string) %}`來建置您的運算式。 對應是決定專案中參照的片段。 字串可以是您在決定專案中輸入的裝置模型，做為&#x200B;**[!UICONTROL 片段參考索引鍵]**。

   ![用來參考片段對應和片段參考索引鍵的Map和Get函式。](assets/decision-map-function.png)

1. 您也可以使用包含此裝置型號ID的內容屬性。

   ![為裝置模型識別碼選取的內容屬性。](assets/decision-contextual-attribute.png)

1. 新增您為片段選擇的變數作為片段ID。

   ![從決定原則代碼中的決定專案設定的片段ID變數。](assets/decision-fragment-id.png)

>[!ENDTABS]

將會從決定專案的&#x200B;**[!UICONTROL 片段]**&#x200B;區段中選取片段ID和參考索引鍵。

>[!WARNING]
>
>如果片段索引鍵不正確或片段內容無效，轉譯可能會失敗並在Edge呼叫中導致錯誤。
>
>為了避免片段暫時無法使用時失敗，請使用`required=false`標幟，以取代略過片段。 [進一步瞭解暫時無法使用的片段](#temporary-unavailable-fragments)

### 使用情況和護欄 {#fragments-guardrails}

以下護欄特別適用於決策專案中使用的&#x200B;**AJO內容片段**。

+++類比電子郵件中的內容和運算式片段

對於&#x200B;**電子郵件**&#x200B;頻道，當您&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;或促銷活動啟動時，與決定專案相關聯的運算式片段會正確顯示。 但是，**[!UICONTROL 模擬內容]**&#x200B;不會顯示決定專案中的運算式片段。

+++

+++電子郵件中的視覺片段和決定專案

您無法將&#x200B;**[!UICONTROL 視覺化片段]**&#x200B;指派給決定專案，此內容中僅支援&#x200B;**運算式片段**。

+++

+++決定專案與內容屬性

[!DNL Journey Optimizer]片段預設不支援決定專案屬性和內容屬性。 不過，您可以改用全域變數，如下所述。

假設您要在片段中使用&#x200B;*sport*&#x200B;變數。

1. 在片段中參照此變數，例如：

   ```text
   Elevate your practice with new {{sport}} gear!
   ```

1. 在決定原則區塊中使用&#x200B;**Let**&#x200B;函式定義變數。 在下列範例中，*sport*&#x200B;是以決定專案屬性定義：

   ```handlebars
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

+++

+++決定專案片段內容驗證

* 由於這些片段的動態性質，當用於行銷活動時，會針對決策專案中所參考的片段略過行銷活動內容建立期間的訊息驗證。

* 片段內容的驗證僅在片段建立和發佈期間進行。

* 對於JSON型別運算式片段，在儲存片段時會語法驗證內容。 驗證錯誤會顯示為警示。

在執行階段，會驗證行銷活動內容（包括決策專案中的片段內容）。 萬一驗證失敗，行銷活動將不會呈現。

+++

+++暫時無法使用的片段已略過{#temporary-unavailable-fragments}

當歷程或行銷活動參考附加到決策專案的片段時，可能會有短暫的同步延遲，更新的片段才能在Edge上使用。

為避免片段暫時不可用時失敗，片段現在會將`required`標幟預設為`false`，以便略過這些標幟，而非導致歷程或行銷活動失敗。

這表示如果片段在Edge上暫時無法使用，則會忽略該片段。 如果片段可用，則會正常轉譯。

**範例**

如果您的決策原則符合兩個優惠方案的資格，且每個方案都有片段 — 例如「20%優惠」和「30%優惠」 — 而第二個片段暫時無法使用，因為`required=false`系統會呈現可用的優惠方案（20%優惠）並略過另一個片段（30%優惠），而不是讓歷程或行銷活動失敗。 如此可改善內容仍在同步處理時的可靠性。

+++

>[!NOTE]
>
>您仍然可以將`required`標幟設定為`true`，將片段標示為必要。 但是，如果片段暫時遺失，可能會導致歷程或行銷活動轉譯失敗。

## AEM內容片段 {#aem-fragments-decisioning}

>[!AVAILABILITY]
>
>此功能適用於支援決策的管道。

在決定原則中運用AEM內容片段之前，請確定您具備：

* 已在Adobe Experience Manager中建立您的內容片段，並以`ajo-enabled:{OrgId}/{SandboxName}`標籤，以便可供Journey Optimizer探索。 [瞭解如何建立和指派標籤](../integrations/aem-fragments.md#create-tag)
* 透過指派唯一的參考名稱，將片段繫結至選件專案的&#x200B;**[!UICONTROL AEM片段]**&#x200B;區段。 [瞭解如何將AEM內容片段連結至決定專案](items.md#attributes)

在個人化編輯器中，與原則選取的決策專案相關聯的所有AEM內容片段都可供使用。 每個片段索引鍵名稱都會顯示一個資料夾。

➡️ [探索如何在影片中搭配Journey Optimizer Decisioning使用AEM內容片段](#video)

在此範例中，決定原則包含兩個決定專案，這些決定專案有AEM片段透過其參考名稱繫結至它們。

![Personalization編輯器在決定原則中顯示每個片段索引鍵名稱可用的AEM內容片段。](assets/aem-fragment-select.png)

1. 按一下+按鈕，將所需的片段新增至運算式中。

   由於單一參考名稱可能具有多個跨不同優惠方案專案繫結至它的片段，Decisioning會根據決定原則的排名條件決定要提供給每個客戶的最佳片段。

1. 選取片段後，您可以利用其屬性（例如影像URL、文字欄位或其他內容），並使用「決策」在適當的時間將適當的內容呈現給適當的客戶。

   ![可在決定原則運算式中用於個人化的已選取AEM內容片段屬性。](assets/aem-fragment-attribute.png)

1. 在啟用您的行銷活動或歷程之前，請使用任一模擬方法來預覽AEM內容片段欄位值將如何呈現。 [進一步瞭解模擬內容](../content-management/preview-test.md)

### 跨頻道使用AEM內容片段 {#aem-fragments-channels}

如何從決定原則插入AEM內容片段屬性，取決於您使用的管道。

>[!BEGINTABS]

>[!TAB 電子郵件]

若要使用決定原則將AEM內容片段屬性插入電子郵件：

1. 在電子郵件Designer中開啟您的電子郵件草稿，然後按一下右側邊欄中的&#x200B;**[!UICONTROL 決策]**&#x200B;圖示以開啟決策原則面板。
1. 選取您組裝的選取策略，並指定&#x200B;**位置**&#x200B;以定義將填入優惠方案的電子郵件區域。
1. 按一下&#x200B;**+**&#x200B;圖示，然後從AEM內容片段中選取應在該區域中呈現的特定欄位，例如主圖影像URL欄位。

   ![電子郵件Designer決定原則面板，其中包含已選取用於版位的AEM內容片段欄位。](assets/aem-fragment-email.png)

1. 發佈之前，請按一下&#x200B;**[!UICONTROL 模擬內容]**&#x200B;以預覽結果，並驗證最高優先順序的選件及其內容片段是否如測試設定檔所預期般轉譯。

>[!TAB 程式碼型體驗(JSON)]

建置JSON型程式碼型體驗時，使用以下結構從決定原則轉譯AEM內容片段屬性。

```handlebars
[
{{#each decisionPolicy.YOUR_POLICY_ID.items as |item|}}
{% let frag = get(item._experience.decisioning.offeritem.aemContentReferencesMap, "YOUR_REFERENCE_KEY").id %}
{{fragment id = frag result='YOUR_REFERENCE_KEY' required=false}}
{
  "fieldName": "{{{YOUR_REFERENCE_KEY.fieldName}}}"
},
{{/each}}
]
```

>[!NOTE]
>
>AEM內容片段使用`aemContentReferencesMap`透過參考索引鍵查詢片段。 這與用於Journey Optimizer內容片段的`contentReferencesMap`不同。

建置JSON裝載時，請記得下列事項：

* 將JSON陣列括弧`[`與`]`放在`#each`回圈的&#x200B;**外部**。
* 對JSON字串內的欄位值使用&#x200B;**三大括弧** `{{{ }}}`可防止HTML逸出特殊字元，並確保有效的JSON輸出。
* `result='YOUR_REFERENCE_KEY'`引數會擷取該名稱下的已解析片段內容，以便您可以使用`YOUR_REFERENCE_KEY.fieldName`參考其欄位。

![程式碼型體驗編輯器顯示從JSON的決定原則轉譯的AEM內容片段屬性。](assets/aem-fragments-cbe.png)

>[!TAB 程式碼型體驗(HTML)]

對於以HTML為基礎的程式碼體驗，請使用標準雙大括弧來轉譯欄位：

```handlebars
{{#each decisionPolicy.YOUR_POLICY_ID.items as |item|}}
{% let frag = get(item._experience.decisioning.offeritem.aemContentReferencesMap, "YOUR_REFERENCE_KEY").id %}
{{fragment id = frag result='YOUR_REFERENCE_KEY' required=false}}
<div>{{YOUR_REFERENCE_KEY.fieldName}}</div>
{{/each}}
```

>[!ENDTABS]

### 使用來自AEM內容片段的資產 {#aem-cf-assets}

AEM內容片段可能包含參照儲存在AEM中之資產的影像欄位。 由於Journey Optimizer只會接收這些資產的&#x200B;**相對路徑**，因此除非在完整發佈URL前面加上，否則影像無法載入。

>[!NOTE]
>
>尚不支援內容片段內AEM資產參考的原生解析。 在新增該支援之前，以下方法都是可用的解決方法。

>[!BEGINTABS]

>[!TAB 在AEM發佈網域前面加上]

1. 從您的AEM執行個體URL，識別作者網域，例如`author-p12345-e67890.adobeaemcloud.com`。

   ![AEM執行個體URL顯示用來衍生髮佈網域的作者網域。](assets/aem-fragment-author-domain.png)

1. 以`publish`取代`author`以取得發佈網域： `publish-p12345-e67890.adobeaemcloud.com`。

1. 在Journey Optimizer個人化編輯器中，將該發佈網域附加至內容片段中的資產參考欄位。

   ![Personalization編輯器，在內容片段資產參考欄位前面加上AEM發佈網域。](assets/aem-fragment-publish-domain.png)

影像現在會在傳送時解析為完整發佈URL。

>[!TAB 將發佈URL儲存在文字欄位中]

1. 在AEM中開啟您的內容片段。
1. 前往JSON預覽並檢查&#x200B;**參考**&#x200B;區段以找出已發佈的資產URL。

   ![顯示已發佈資產URL的AEM內容片段JSON預覽參考區段。](assets/aem-fragment-published-url.png)

1. 複製發佈URL並將其貼到內容片段內的專用文字欄位中。

   ![包含所參考資產之複製發佈URL的AEM內容片段文字欄位。](assets/aem-fragment-copy-url.png)

1. 在Journey Optimizer中，直接將該文字欄位作為個人化運算式中的影像來源參考。

   ![將內容片段文字欄位做為影像來源的Journey Optimizer個人化運算式。](assets/aem-fragment-use-url.png)

此方法可避免手動URL建構，並將發佈URL保留在內容片段本身內。

>[!ENDTABS]

## 作法影片 {#video}

瞭解如何使用Adobe Experience Manager內容片段搭配Journey Optimizer Decisioning來個人化和最佳化內容。

>[!VIDEO](https://video.tv.adobe.com/v/3492215/?learn=on&enablevpops)
