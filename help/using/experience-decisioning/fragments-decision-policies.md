---
title: 在決策政策中善用片段
description: 瞭解如何在決策原則中運用片段
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
badge: label="有限可用性" type="Informative"
source-git-commit: b579e39194f70dd3cb67577b82fa4868de36c5e2
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 1%

---

# 在決策政策中善用片段 {#fragments}

如果您的決定原則包含決定專案（包括片段），您可以在決定原則程式碼中利用這些片段。 [進一步瞭解片段](../content-management/fragments.md)

>[!AVAILABILITY]
>
>此功能在&#x200B;**程式碼型體驗**&#x200B;和&#x200B;**電子郵件**&#x200B;管道的「有限可用性」中提供。 如欲請求存取權，請和您的 Adobe 代表聯絡。

例如，假設您想針對多種行動裝置型號顯示不同的內容。 請務必將與這些裝置對應的片段新增至您在決定原則中使用的決定專案。 [瞭解如何進行](items.md#attributes)。

![決策專案的片段區段，顯示片段參考和位置索引鍵。](assets/item-fragments.png){width=70%}

完成後，您可以使用下列其中一種方法：

>[!BEGINTABS]

>[!TAB 直接插入代碼]

只要將下方的程式碼區塊複製並貼到決定原則程式碼中即可。 以片段ID取代`variable`，並以片段參考索引鍵取代`placement`：

```handlebars
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
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
>如果片段索引鍵不正確或片段內容無效，呈現將會失敗，而導致Edge呼叫中的錯誤。

## 使用片段時的護欄 {#fragments-guardrails}

**在電子郵件中模擬內容和運算式片段**

對於&#x200B;**電子郵件**&#x200B;頻道，當您&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;或促銷活動啟動時，與決定專案相關聯的運算式片段會正確顯示。 但是，**[!UICONTROL 模擬內容]**&#x200B;不會顯示決定專案中的運算式片段。

**電子郵件中的視覺片段和決定專案**

您無法將&#x200B;**[!UICONTROL 視覺化片段]**&#x200B;指派給決定專案，此內容中僅支援&#x200B;**運算式片段**。

**決定專案與內容屬性**

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

**決定專案片段內容驗證**

* 由於這些片段的動態性質，當用於行銷活動時，會針對決策專案中所參考的片段略過行銷活動內容建立期間的訊息驗證。

* 片段內容的驗證僅在片段建立和發佈期間進行。

* 對於JSON型別運算式片段，在儲存片段時會語法驗證內容。 驗證錯誤會顯示為警示。

在執行階段，會驗證行銷活動內容（包括決策專案中的片段內容）。 萬一驗證失敗，行銷活動將不會呈現。
