---
title: 個人化驗證
description: 進一步瞭解個人化驗證及如何疑難排解
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 個人化驗證{#personalization-validation}

![](../assets/do-not-localize/badge.png)

## 驗證機制

在「運算式」編輯器畫面中，**Validate**&#x200B;按鈕可讓您驗證個人化語法。

>[!NOTE]
> 按一下&#x200B;**添加**&#x200B;關閉編輯器窗口時，將自動執行驗證。


![](assets/perso_validation1.png)

>[!IMPORTANT]
> 如果個人化語法無效，則無法關閉運算式編輯器視窗。


## 常見錯誤

* **找不到路徑&quot;XYZ&quot;**

嘗試引用未在架構中定義的欄位時。

在這種情況下，**firstName1**&#x200B;未定義為描述檔架構中的屬性：

```
{{profile.person.name.firstName1}}
```

* **變數&quot;XYZ&quot;的類型不匹配。需要陣列。 找到字串。**

嘗試在字串上循環（而非陣列）:

在這種情況下，**product**&#x200B;不是陣列：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **無效的車把語法。找到`‘[XYZ}}’`**

使用無效的句柄語法時。

把手運算式被&#x200B;**{{expression}}**&#x200B;包圍

```
   {{[profile.person.name.firstName}}
```

* **無效的區段定義**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

### 與選件相關的特定錯誤

與「電子郵件」或「推播」訊息中的選件整合相關的錯誤模式如下：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

驗證是在訊息發佈期間或在運算式編輯器中個人化內容驗證期間執行。

<table> 
 <thead> 
  <tr> 
   <th> 錯誤標題<br /> </th> 
   <th> 驗證／解析度<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>具有ID placementID的資源，並鍵入OfferPlacement not found <br/>
具有ID activityID的資源，並鍵入OfferActivity not found<br/></td> 
   <td>檢查ActivityID和／或PlacementID是否可用</td> 
  </tr> 
   <tr> 
   <td>無法驗證資源。</td> 
   <td>「位置」中的componentType應符合offerType選件</td> 
  </tr> 
   <tr> 
   <td>offerId中不存在公用URL。</td> 
   <td>影像選件（所有與決策和位置對關聯的個人化和備援）應填入公用URL（deliveryURL不應為空）。</td> 
  </tr> 
  <tr> 
   <td>決定（先前稱為選件活動）包含非描述檔屬性。</td> 
   <td>選件模型用法應僅包含描述檔屬性。</td> 
  </tr> 
  <tr> 
   <td>提取決策使用時出錯。</td> 
   <td>當API嘗試擷取選件模型時，可能會發生此錯誤。</td> 
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

