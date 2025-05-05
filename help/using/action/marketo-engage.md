---
solution: Journey Optimizer
product: journey optimizer
title: 與 Marketo Engage 整合
description: 瞭解如何使用Marketo Engage動作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: marketo， marketo engage整合
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: 844c0f8dc9b14d69cbd87893042f048443d7a5e6
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 4%

---

# 與 Marketo Engage 整合 {#integrating-with-marketo-engage}

開始與Marketo Engage無縫整合資料的歷程。 Journey Optimizer中的這個特定自訂動作支援擷取兩種關鍵資料型別：

* 人員（設定檔）： Marketo會將設定檔轉換為可操作的深入分析。
* 自訂物件：使用自訂物件（例如產品）量身打造您的資料，以利個人化行銷方法。

## 先決條件 {#prerequisites}

* Marketo Engage的客戶執行個體必須已啟用IMS。
* Marketo Engage例項和Adobe Experience Platform/Journey Optimizer例項必須位於相同組織。
* 客戶必須布建&#x200B;**MktoSync：內嵌服務存取**

## 設定動作 {#configure-marketo-action}

* 導覽至管理>設定>動作，然後按一下管理
* 在「動作」清單中，按一下「建立動作」。 深入瞭解[自訂動作](../building-journeys/using-custom-actions.md){target="_blank"}。
* 輸入名稱、說明，然後選取Adobe Marketo Engage作為動作型別

![](assets/engage-customaction-creation.png){width="40%" align="left"}

* 按一下&#x200B;**要求**&#x200B;和&#x200B;**回應**&#x200B;裝載的「編輯裝載」。
* 針對這兩者，撰寫您的裝載並在專用的快顯視窗中貼上。

![](assets/engage-customaction-payload.png){width="70%" align="left"}

* Inspect和設定裝載值
注意：若要以動態方式傳遞值，請針對每個欄位變更&#x200B;**常數**&#x200B;至&#x200B;**變數**。

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

* 在[欄位設定]視窗中按一下[儲存]，然後按一下[儲存]，為您的自訂動作&#x200B;**[儲存]**。**&#x200B;**

您現在可以在專屬畫布上使用自訂動作。


## 裝載語法 {#payload-syntax}

### 人員

![](assets/payload-person.png)

### CustomObject

![](assets/payload-customobject.png)


人員&#x200B;**的**&#x200B;裝載範例

```json
{
   "munchkinID": "388-KKG-245",  
   "person": {
    "priority": "normal",
    "partitionName": "XYZ",
    "dedupeFields": {
      "field1": "email",
      "field2": "firstName"
    },
    "objects": [
      {
        "email": "Email address",
        "firstName": "First name",
        "lastName": "Last name"
      }
    ]
  }
}
```

自訂物件的&#x200B;**裝載範例**

```json
{
  "munchkinID": "388-KKG-245", 
  "customObject": {
    "priority": "normal",
    "objectName": "products",
    "objects": [
      {
        "email": "Email Address",
        "productName": "Product Name",
        "productQty": "Product Quantity",
        "priceTotal": "Price Total"
      }
    ]
  }
}
```


## 使用動作 {#engage-using}

* 將自訂動作拖曳至歷程畫布。
* 在&#x200B;**要求引數**&#x200B;區段中，針對每個具有您在承載中設定的動態值的引數，按一下「編輯」。

![](assets/engage-use-canvas.png){width="70%" align="left"}
