---
title: 個人化驗證
description: 深入了解個人化驗證及疑難排解
feature: 個性化
topic: 個性化
role: Data Engineer
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

---


# 個人化驗證 {#personalization-validation}

![](../assets/do-not-localize/badge.png)

## 驗證機制

在「運算式」編輯器畫面中， **Validate**&#x200B;按鈕可讓您驗證個人化語法。

>[!NOTE]
> 按一下&#x200B;**Add**&#x200B;以關閉編輯器視窗時，會自動執行驗證。


![](assets/perso_validation1.png)

>[!IMPORTANT]
> 如果個人化語法無效，則無法關閉運算式編輯器視窗。


## 常見錯誤

* **找不到路徑&quot;XYZ&quot;**

嘗試參考未在架構中定義的欄位時。

在此案例中，**firstName1**&#x200B;未在設定檔架構中定義為屬性：

```
{{profile.person.name.firstName1}}
```

* **變數&quot;XYZ&quot;的類型不符。預期的陣列。 找到字串。**

嘗試迭代運算字串而非陣列時：

在這種情況下，**product**&#x200B;不是陣列：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **無效的handlebars語法。找到`‘[XYZ}}’`**

使用無效的handlebars語法時。

Handlebars表達式被&#x200B;**{{expression}}**&#x200B;包圍

```
   {{[profile.person.name.firstName}}
```

* **無效的段定義**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

### 與優惠方案相關的特定錯誤

與電子郵件或推送訊息中選件整合相關的錯誤模式如下：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

驗證會在訊息發佈期間或運算式編輯器中個人化內容驗證期間執行。

<table> 
 <thead> 
  <tr> 
   <th> 錯誤標題<br /> </th> 
   <th> 驗證/解決方案<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>找不到具有ID placementID的資源，並鍵入OfferPlacement <br/>
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
   <td>檢查選件記錄中參考的選件屬性是否有效。 以下是有效屬性：<br/>
影像：deliveryURL, linkURL<br/>
文字：content<br/>
HTML:內容<br/></td> 
  </tr> 
 </tbody> 
</table>

