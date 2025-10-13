---
solution: Journey Optimizer
product: journey optimizer
title: 使用自訂動作動態傳遞集合
description: 使用 Campaign v7/v8 傳送訊息
feature: Journeys, Use Cases, Custom Actions, Collections
topic: Content Management
role: Developer, Data Engineer
level: Experienced
exl-id: 8832d306-5842-4be5-9fb9-509050fcbb01
version: Journey Orchestration
source-git-commit: 3d0e2817ef2b544aced441d7bb8b1a94ac2acccf
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 5%

---


# 使用自訂動作動態傳遞集合{#passing-collection}

您可以在自訂動作引數中傳遞集合，這些引數將在執行階段以動態方式填入。 支援兩種集合：

* 簡單集合：簡單資料型別的陣列，例如，使用listString：

  ```
  {
   "deviceTypes": [
       "android",
       "ios"
   ]
  }
  ```

* 物件集合：JSON物件的陣列，例如：

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

## 限制 {#limitations}

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


* 若要使用測試模式測試集合，您需要使用程式碼檢視模式。 目前商業事件不支援程式碼檢視模式。 您只能傳送包含單一元素的集合。

## 一般程式 {#general-procedure}

在本節中，我們將使用以下JSON裝載範例。 這是一個物件陣列，其中的欄位是一個簡單的集合。

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

您可以看到「products」是兩個物件的陣列。 您至少需要一個物件。

1. 建立您的自訂動作。 請參閱[此頁面](../action/about-custom-action-configuration.md)。

1. 在&#x200B;**[!UICONTROL 動作引數]**&#x200B;區段中，貼上JSON範例。 顯示的結構為靜態：貼上裝載時，所有欄位都會定義為常數。

   ![](assets/uc-collection-1.png)

1. 如有需要，請調整欄位型別。 集合支援下列欄位型別：listString、listInteger、listDecimal、listBoolean、listDateTime、listDateTimeOnly、listDateOnly、listObject

   >[!NOTE]
   >
   >根據裝載範例自動推斷欄位型別。

1. 如果您想要以動態方式傳遞物件，則需要將物件設定為變數。 在此範例中，我們將「products」設為變數。 物件中包含的所有物件欄位都會自動設定為變數。

   >[!NOTE]
   >
   >裝載範例的第一個物件用於定義欄位。

1. 針對每個欄位，定義將顯示在歷程畫布中的標籤。

   ![](assets/uc-collection-2.png)

1. 建立您的歷程並新增您建立的自訂動作。 請參閱[此頁面](../building-journeys/using-custom-actions.md)。

1. 在&#x200B;**[!UICONTROL 動作引數]**&#x200B;區段中，使用進階運算式編輯器定義陣列引數（範例中為「products」）。

   ![](assets/uc-collection-3.png)

1. 對於以下每個物件欄位，輸入來源XDM結構描述中的對應欄位名稱。 如果名稱相同，則不需要這樣做。 在我們的範例中，我們只需要定義「product id」和「color」。

   ![](assets/uc-collection-4.png)

針對陣列欄位，您也可以使用進階運算式編輯器來執行資料操作。 在下列範例中，我們使用[篩選器](functions/functionfilter.md)和[交集](functions/functionintersect.md)函式：

![](assets/uc-collection-5.png)

## 特定案例{#examples}

針對異質型別和陣列陣列，陣列是以listAny型別定義。 您只能對應個別專案，但無法將陣列變更為變數。

![](assets/uc-collection-heterogeneous.png)

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

**相關主題**

[使用自訂動作](../building-journeys/using-custom-actions.md)
