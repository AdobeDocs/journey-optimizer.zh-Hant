---
title: 在訊息中使用決定原則
description: 瞭解如何在訊息中使用決定原則。
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
source-git-commit: f8b91ef5504396ab696acc05ac273423dd5f208e
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 1%

---

# 在訊息中使用決定原則 {#create-decision}

建立決定原則後，您便可以在內容中使用原則及連結至傳回決定專案的屬性，以進行個人化。 若要這麼做，必須先將與決定原則關聯的程式碼插入內容中。 完成後，您可以利用其屬性進行個人化。

## 插入決定原則代碼 {#insert-code}

>[!BEGINTABS]

>[!TAB 程式碼型體驗]

1. 開啟個人化編輯器並存取&#x200B;**[!UICONTROL 決定原則]**&#x200B;功能表。

1. 選取&#x200B;**[!UICONTROL 插入原則]**&#x200B;以新增與決定原則對應的程式碼。

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >如果未顯示程式碼插入按鈕，表示可能已針對上層元件設定決定原則。

1. 已新增決定原則的程式碼。 此序列將重複執行您想要傳回決定原則的次數。 例如，如果您選擇在[建立決定](#add-decision)時傳回2個專案，則相同的順序將重複兩次。

>[!TAB 電子郵件]

1. 開啟個人化編輯器並存取&#x200B;**[!UICONTROL 決定原則]**&#x200B;功能表。

1. 選取&#x200B;**[!UICONTROL 插入語法]**&#x200B;以新增與決定原則對應的程式碼。

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >如果未顯示程式碼插入按鈕，表示可能已針對上層元件設定決定原則。

1. 如果尚未將任何位置預先關聯至元件，請從清單中選取一個位置，然後按一下&#x200B;**[!UICONTROL 指派]**。

   ![](assets/decision-policy-placement.png)

>[!ENDTABS]

新增決定原則的程式碼後，此序列將重複執行您想要傳回決定原則的次數。 例如，如果您選擇在[建立決定](#add-decision)時傳回2個專案，則相同的順序將重複兩次。

## 利用決策專案屬性 {#attributes}

現在，您可以在該程式碼中新增所有需要的決定屬性。 可用的屬性儲存在&#x200B;**[!UICONTROL 選件]**&#x200B;目錄的結構描述中。 自訂屬性儲存在&#x200B;**`_<imsOrg`>**&#x200B;資料夾中，而標準屬性儲存在&#x200B;**`_experience`**&#x200B;資料夾中。 [進一步瞭解優惠方案目錄的結構描述](catalogs.md)

![](assets/decision-code-based-decision-attributes.png)

>[!NOTE]
>
>針對決定原則專案追蹤，決策原則內容需要新增`trackingToken`屬性，如下所示：
>>`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

若要新增屬性，請按一下它旁邊的&#39;+&#39;圖示。 您可以對程式碼新增任意數量的屬性。

![](assets/decision-code-based-add-decision-attributes.png)

請務必將`#each`回圈包裝在一對方括弧`[ ]`內，並在結尾的`/each`前加上逗號。

![](assets/decision-code-based-wrap-code.png)

您也可以新增個人化編輯器中可用的任何其他屬性，例如設定檔屬性。

![](assets/decision-code-based-decision-profile-attribute.png)

## 利用片段（程式碼型體驗） {#fragments}

如果您的決定原則包含決定專案（包括片段），您可以在決定原則程式碼中利用這些片段。 [進一步瞭解片段](../content-management/fragments.md)

>[!AVAILABILITY]
>
>此功能目前僅適用於程式碼型體驗管道和一組組織（可用性限制）。 如需詳細資訊，請聯絡您的 Adobe 代表。

例如，假設您想針對多種行動裝置型號顯示不同的內容。 請務必將與這些裝置對應的片段新增至您在決定原則中使用的決定專案。 [瞭解如何進行](items.md#attributes)。

![](assets/item-fragments.png){width=70%}

完成後，您可以使用下列其中一種方法：

>[!BEGINTABS]

>[!TAB 直接插入代碼]

只要將下方的程式碼區塊複製並貼到決定原則程式碼中即可。 以片段ID取代`variable`，並以片段參考索引鍵取代`placement`：

```
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
```

>[!TAB 遵循詳細步驟]

1. 導覽至&#x200B;**[!UICONTROL 協助程式函式]**，並將&#x200B;**Let**&#x200B;函式`{% let variable = expression %} {{variable}}`新增至程式碼窗格，您可以在其中宣告片段的變數。

   ![](assets/decision-let-function.png)

1. 使用&#x200B;**Map** > **Get**&#x200B;函式`{%= get(map, string) %}`來建置您的運算式。 對應是決策專案中參考的片段，而字串可以是您在決策專案中輸入的裝置模型，做為&#x200B;**[!UICONTROL 片段參考索引鍵]**。

   ![](assets/decision-map-function.png)

1. 您也可以使用包含此裝置型號ID的內容屬性。

   ![](assets/decision-contextual-attribute.png)

1. 新增您為片段選擇的變數作為片段ID。

   ![](assets/decision-fragment-id.png)

>[!ENDTABS]

將會從決定專案的&#x200B;**[!UICONTROL 片段]**&#x200B;區段中選取片段ID和參考索引鍵。

>[!WARNING]
>
>如果片段索引鍵不正確或片段內容無效，呈現將會失敗，而導致Edge呼叫中的錯誤。

### 使用片段時的護欄 {#fragments-guardrails}

**決定專案與內容屬性**

[!DNL Journey Optimizer]片段預設不支援決定專案屬性和內容屬性。 不過，您可以改用全域變數，如下所述。

假設您要在片段中使用&#x200B;*sport*&#x200B;變數。

1. 在片段中參照此變數，例如：

   ```
   Elevate your practice with new {{sport}} gear!
   ```

1. 在決定原則區塊中使用&#x200B;**Let**&#x200B;函式定義變數。 在下列範例中，*sport*&#x200B;是以決定專案屬性定義：

   ```
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

**決定專案片段內容驗證**

* 由於這些片段的動態性質，當用於行銷活動時，會針對決策專案中所參照的片段，略過行銷活動內容建立期間的訊息驗證。

* 片段內容的驗證僅在片段建立和發佈期間進行。

* 至於JSON片段，無法確保JSON物件是否有效。 請確定運算式片段內容是有效的JSON，以便用於決定專案。

在執行階段，會驗證行銷活動內容（包括決策專案中的片段內容）。 萬一驗證失敗，行銷活動將不會呈現。

## 後續步驟 {#final-steps}

準備好您的內容後，請檢閱並發佈您的行銷活動或歷程：

* [發佈歷程](../building-journeys/publishing-the-journey.md)
* [檢閱啟動行銷活動](../campaigns/review-activate-campaign.md)
* [發佈並啟用程式碼型體驗](../code-based/publish-code-based.md)

針對程式碼型體驗，當您的開發人員發出API或SDK呼叫，擷取您頻道設定中定義之表面的內容時，變更就會套用至您的網頁或應用程式。

>[!NOTE]
>
>目前您無法在[程式碼型體驗](../code-based/create-code-based.md)促銷活動或歷程中使用決定，從使用者介面模擬內容。 [此區段](../code-based/code-based-decisioning-implementations.md)中有因應措施。

若要檢視決策的執行方式，您可以建立自訂[Customer Journey Analytics報告控制面板](cja-reporting.md)。

