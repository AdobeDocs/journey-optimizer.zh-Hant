---
title: 個人化驗證
description: 深入了解個人化驗證及疑難排解
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# 個人化驗證 {#personalization-validation}

## 驗證機制

在 **運算式編輯器** 螢幕，使用 **驗證** 按鈕以檢查個人化語法。

>[!NOTE]
> 當您按一下 **新增** 按鈕以關閉編輯器視窗。

![](assets/perso_validation1.png)

>[!IMPORTANT]
> 如果個人化語法無效，則無法關閉運算式編輯器視窗。

## 常見錯誤

* **找不到路徑&quot;XYZ&quot;**

嘗試參考未在架構中定義的欄位時。

在這種情況下 **firstName1** 未定義為設定檔結構中的屬性：

```
{{profile.person.name.firstName1}}
```

* **變數&quot;XYZ&quot;的類型不符。 預期的陣列。 找到字串。**

嘗試迭代運算字串而非陣列時：

在這種情況下 **產品** 不是陣列：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **無效的handlebars語法。 找到`‘[XYZ}}’`**

使用無效的handlebars語法時。

Handlebars表達式被包圍 **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **無效的段定義**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## 與優惠方案相關的特定錯誤

與電子郵件或推送訊息中選件整合相關的錯誤模式如下：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

驗證會在訊息發佈期間或運算式編輯器中個人化內容驗證期間執行。

<table> 
 <thead> 
  <tr> 
   <th> 錯誤標題<br /> </th> 
   <th> 驗證/解決方法 <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>找不到具有id placementID的資源，並鍵入OfferPlacement <br/>
找不到具有id activityID且類型為OfferActivity的資源<br/></td> 
   <td>檢查ActivityID和/或PlacementID是否可用</td> 
  </tr> 
   <tr> 
   <td>無法驗證資源。</td> 
   <td>版位中的componentType應符合offerType選件</td> 
  </tr> 
   <tr> 
   <td>offerId中不存在公用URL。</td> 
   <td>影像選件（與決策和版位配對相關聯的所有個人化和後援）應填入公用URL（deliveryURL不應空白）。</td> 
  </tr> 
  <tr> 
   <td>決策（先前稱為優惠方案活動）包含非設定檔屬性。</td> 
   <td>選件模型使用方式應僅包含設定檔屬性。</td> 
  </tr> 
  <tr> 
   <td>讀取決策使用時出錯。</td> 
   <td>API嘗試擷取選件模型時，可能會發生此錯誤。</td> 
  </tr>
  <tr> 
   <td>選件屬性選件屬性無效。</td> 
   <td>檢查選件記錄中參考的選件屬性是否有效。 以下是有效屬性： <br/>
影像：deliveryURL, linkURL<br/>
文字：內容<br/>
HTML:內容<br/></td> 
  </tr> 
 </tbody> 
</table>
