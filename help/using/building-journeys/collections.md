---
solution: Journey Optimizer
product: journey optimizer
title: 將集合傳遞至自訂動作引數
description: 瞭解如何使用自訂動作在Journey Optimizer中動態傳遞集合
feature: Journeys, Use Cases, Custom Actions, Collections
topic: Content Management
role: Developer
level: Experienced
exl-id: 8832d306-5842-4be5-9fb9-509050fcbb01
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 2%

---


# 將集合傳遞至自訂動作引數 {#passing-collection}

您可以在自訂動作引數中傳遞集合，這些引數會在執行階段以動態方式填入。

支援兩種型別的集合：

* **簡單集合**

  將簡單集合用於基本值清單，例如字串、數字或布林值。 當您只需要傳遞專案清單而沒有其他屬性時，這些會很有用。

  例如，裝置型別清單：

  ```json
  {
   "deviceTypes": [
       "android",
       "ios"
   ]
  }
  ```

* **物件集合**

  當每個專案包含多個欄位或屬性時，使用物件集合。 這些通常用於傳遞結構化資料，例如產品詳細資訊、事件記錄或專案屬性。

  例如：

  ```json
  {
  "products":[
     {
        "id":"productA",
        "name":"A",
        "price":20.1
     },
     {
        "id":"productB",
        "name":"B",
        "price":10.0
     },
     {
        "id":"productC",
        "name":"C",
        "price":5.99
     }
   ]
  }
  ```

>[!NOTE]
>
>集合中的巢狀陣列僅部分支援自訂動作請求承載。 如需詳細資訊，請參閱[限制](#limitations)。

## 一般程式 {#general-procedure}

在本節中，我們會使用下列JSON裝載範例。 這是一個物件陣列，其中的欄位是一個簡單的集合。

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "A",
        "price": 20.1,
        "color":"blue",
        "locations": [
          "Paris",
          "London"
        ]
      },
      {
        "id": "productB",
        "name": "B",
        "price": 10.99
      }
    ]
  }
}
```

您可以看到`products`是兩個物件的陣列。 您至少需要一個物件。

1. 建立您的自訂動作。 請在[此頁面](../action/about-custom-action-configuration.md)了解更多。

1. 在&#x200B;**[!UICONTROL 動作引數]**&#x200B;區段中，貼上JSON範例。 顯示的結構為靜態：貼上裝載時，所有欄位都會定義為常數。

   ![](assets/uc-collection-1.png)

1. 如有需要，請調整欄位型別。 集合支援下列欄位型別：listString、listInteger、listDecimal、listBoolean、listDateTime、listDateTimeOnly、listDateOnly、listObject

   >[!NOTE]
   >
   >根據裝載範例自動推斷欄位型別。

1. 如果您想要以動態方式傳遞物件，則需要將物件設定為變數。 在此範例中，我們將`products`設定為變數。 物件中包含的所有物件欄位都會自動設定為變數。

   >[!NOTE]
   >
   >裝載範例的第一個物件用於定義欄位。

1. 針對每個欄位，定義將顯示在歷程畫布中的標籤。

   ![](assets/uc-collection-2.png){width="70%" align="left"}

1. 建立您的歷程並新增您建立的自訂動作。 請在[此頁面](../building-journeys/using-custom-actions.md)了解更多。

1. 在&#x200B;**[!UICONTROL 動作引數]**&#x200B;區段中，使用進階運算式編輯器定義陣列引數（範例中為`products`）。

   ![](assets/uc-collection-3.png)

1. 對於以下每個物件欄位，輸入來源XDM結構描述中的對應欄位名稱。 如果名稱相同，則不需要這樣做。 在我們的範例中，我們只需要定義`product id`和&quot;color&quot;。

   ![](assets/uc-collection-4.png){width="50%" align="left"}

針對陣列欄位，您也可以使用進階運算式編輯器來執行資料操作。 在下列範例中，我們使用[篩選器](functions/functionfilter.md)和[交集](functions/functionintersect.md)函式：

![](assets/uc-collection-5.png)

## 限制 {#limitations}

雖然自訂動作中的集合可提供傳遞動態資料的靈活性，但需注意某些結構限制：

* **支援自訂動作中的巢狀陣列**

  Adobe Journey Optimizer支援自訂動作&#x200B;**回應承載**&#x200B;中的巢狀物件陣列，但此支援限於&#x200B;**請求承載**。

  在請求裝載中，只有當巢狀陣列包含固定數量的專案時（如自訂動作設定中所定義），才支援巢狀陣列。 例如，如果巢狀陣列一律包含剛好三個專案，則可將其設定為常數。 當專案數量需要為動態時，只能將非巢狀陣列（位於底層的陣列）定義為變數。

  範例：

   1. 下列範例說明&#x200B;**不支援的使用案例**。

      在此範例中，產品陣列包含具有動態專案數的巢狀陣列(`locations`)，這在要求裝載中不受支援。

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "locations": [
            { "name": "Paris" },
            { "name": "London" }
            ]
         }
      ]
      }
      ```

   2. 支援的範例，包含定義為常數的固定專案。

      在此情況下，巢狀位置會由固定欄位(`location1`， `location2`)取代，讓裝載在支援的設定中保持有效。

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "location1": { "name": "Paris" },
            "location2": { "name": "London" }
         }
      ]
      }
      ```


* **測試集合**：若要使用測試模式測試集合，您必須使用程式碼檢視模式。 請注意，商業事件不支援程式碼檢視模式，因此在這種情況下，您只能傳送包含單一元素的集合。


## 特定案例{#examples}

針對異質型別和陣列陣列，陣列是以listAny型別定義。 您只能對應個別專案，但無法將陣列變更為變數。

![](assets/uc-collection-heterogeneous.png){width="70%" align="left"}

異質型別範例：

```json
{
    "data_mixed-types": [
        "test",
        "test2",
        null,
        0
    ]
}
```

陣列陣列範例：

```json
{
    "data_multiple-arrays": [
        [
            "test",
            "test1",
            "test2"
        ]
    ]
}
```

## 其他資源

瀏覽以下章節，進一步瞭解設定、使用及疑難排解自訂動作的相關資訊：

* [開始使用自訂動作](../action/action.md) — 瞭解什麼是自訂動作，以及它們如何協助您連線至您的協力廠商系統
* [設定您的自訂動作](../action/about-custom-action-configuration.md) — 瞭解如何建立和設定自訂動作
* [使用自訂動作](../building-journeys/using-custom-actions.md) — 瞭解如何在歷程中使用自訂動作
* [自訂動作疑難排解](../action/troubleshoot-custom-action.md) — 瞭解如何疑難排解自訂動作

