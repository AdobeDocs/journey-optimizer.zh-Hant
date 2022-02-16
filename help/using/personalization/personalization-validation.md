---
title: 個人化驗證
description: 瞭解有關個性化驗證和故障排除的詳細資訊。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 2d859a5dab19a419d424acefd17d254473c00818
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# 個人化驗證 {#personalization-validation}

## 驗證機制 {#validation-mechanisms}

在 **表達式編輯器** 螢幕，使用 **驗證** 按鈕來查看個性化設定語法。

>[!NOTE]
> 按一下 **添加** 按鈕關閉對話框。

![](assets/perso_validation1.png)

>[!IMPORTANT]
> 如果個性化語法無效，則無法關閉表達式編輯器窗口。

## 常見錯誤 {#common-errors}

* **找不到路徑「XYZ」**

嘗試引用未在架構中定義的欄位時。

在這種情況下 **名字1** 未定義為配置檔案架構中的屬性：

```
{{profile.person.name.firstName1}}
```

* **變數「XYZ」的類型不匹配。 需要陣列。 找到字串。**

嘗試在字串而不是陣列上迭代時：

在這種情況下 **產品** 不是陣列：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **句柄語法無效。 找到`‘[XYZ}}’`**

使用無效的句柄語法時。

Handlebar表達式被包圍 **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **段定義無效**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## 與優惠相關的特定錯誤 {#specific-errors}

與提供在電子郵件或推送消息中整合相關的錯誤具有以下模式：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

驗證在消息發佈期間或在表達式編輯器中的個性化內容驗證期間執行。

<table> 
 <thead> 
  <tr> 
   <th> 錯誤標題<br /> </th> 
   <th> 驗證/解決 <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>找不到ID placementID並鍵入OfferPlacement的資源 <br/>
未找到ID為activityID且類型為OfferActivity的資源<br/></td> 
   <td>檢查ActivityID和/或PlacementID是否可用</td> 
  </tr> 
   <tr> 
   <td>無法驗證資源。</td> 
   <td>放置中的componentType應與offerType服務匹配</td> 
  </tr> 
   <tr> 
   <td>offer offerId中不存在公共URL。</td> 
   <td>「影像優惠」（與決策和放置對關聯的所有個性化和回退）應填充公共URL（deliveryURL不應為空）。</td> 
  </tr> 
  <tr> 
   <td>該決定包含非配置檔案屬性。</td> 
   <td>提供模型使用應僅包含配置檔案屬性。</td> 
  </tr> 
  <tr> 
   <td>獲取決策用法時出錯。</td> 
   <td>當API嘗試獲取提供模型時，可能會發生此錯誤。</td> 
  </tr>
  <tr> 
   <td>提供屬性提供屬性無效。</td> 
   <td>檢查聘用記錄中引用的聘用屬性是否有效。 以下是有效屬性： <br/>
影像：交付URL、linkURL<br/>
文本：內容<br/>
HTML:內容<br/></td> 
  </tr> 
 </tbody> 
</table>
