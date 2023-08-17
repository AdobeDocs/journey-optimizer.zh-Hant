---
solution: Journey Optimizer
product: journey optimizer
title: 設定自訂動作
description: 瞭解如何設定自訂動作
feature: Actions
topic: Administration
role: Admin
level: Experienced
badge: label="Beta" type="Informative"
keywords: 動作，協力廠商，自訂，歷程， API
hide: true
hidefromtoc: true
source-git-commit: a3c95497fb7304ddd0aa26435f5d0279ff8fdb0f
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 4%

---

# 自訂動作增強功能

您現在可以在自訂動作中利用API呼叫回應，並根據這些回應協調您的歷程。

此功能僅適用於使用資料來源時。 您現在可以將其用於自訂動作。

>[!AVAILABILITY]
>
>此功能目前以私人測試版的形式提供。

>[!WARNING]
>
>自訂動作應僅搭配私人或內部端點使用，並搭配適當的上限或節流限制使用。 請參閱[此頁面](../configuration/external-systems.md)。

## 定義自訂動作

定義自訂動作時，已提供兩個增強功能：新增GET方法和新的裝載回應欄位。 其他選項和引數則保持不變。 請參閱[此頁面](../action/about-custom-action-configuration.md)。

### 端點設定

此 **URL設定** 區段已重新命名 **端點設定**.

在 **方法** 下拉式清單，您現在可以選取 **GET**.

![](assets/action-response1.png){width="70%" align="left"}

### 裝載

此 **動作引數** 區段已重新命名 **裝載**. 有兩個欄位可供使用：

* 此 **請求** 欄位：此欄位僅適用於POST和PUT呼叫方法。
* 此 **回應** 欄位：這是新功能。 此欄位適用於所有呼叫方法。

>[!NOTE]
> 
>這兩個欄位都是選擇性的。

![](assets/action-response2.png){width="70%" align="left"}

1. 按一下 **回應** 欄位。

   ![](assets/action-response3.png){width="80%" align="left"}

1. 貼上呼叫傳回之裝載的範例。 驗證欄位型別是否正確（字串、整數等）。 以下是呼叫期間擷取的回應裝載範例。 我們的本機端點會傳送熟客點數和設定檔的狀態。

   ```
   {
   "customerID" : "xY12hye",    
   "status":"gold",
   "points": 1290 }
   ```

   ![](assets/action-response4.png){width="80%" align="left"}

   每次呼叫 API 時，系統都會擷取有效負載範例中包含的所有欄位。

1. 我們也將customerID新增為查詢引數。

   ![](assets/action-response9.png){width="80%" align="left"}

1. 按一下&#x200B;**儲存**。

## 在歷程中善用回應

只需將自訂動作新增至歷程即可。 然後，您可以在條件、其他動作和訊息個人化中運用回應裝載欄位。

例如，您可以新增條件以檢查熟客點數。 當人員進入餐廳時，您的本機端點會傳送包含設定檔忠誠度資訊的呼叫。 如果設定檔為黃金客戶，則可傳送推播。 如果在呼叫中偵測到錯誤，請傳送自訂動作以通知您的系統管理員。

![](assets/action-response5.png)

1. 新增您的事件和先前建立的熟客方案自訂動作。

1. 在忠誠度自訂動作中，將客戶ID查詢引數對應至設定檔ID。 核取選項 **在逾時或錯誤的情況下新增替代路徑**.

   ![](assets/action-response10.png)

1. 在第一個分支中，新增條件並使用進階編輯器在 **內容** 節點。

   ![](assets/action-response6.png)

1. 然後新增推播，並使用回應欄位個人化您的訊息。 在範例中，我們使用忠誠度點數和客戶狀態來個人化內容。 動作回應欄位位於 **內容屬性** > **Journey Orchestration** > **動作**.

   ![](assets/action-response8.png)

   >[!NOTE]
   >
   >每個輸入自訂動作的設定檔都會觸發呼叫。 即使回應一律相同，歷程仍會為每個設定檔執行一個呼叫。

1. 在逾時和錯誤分支中，新增條件並利用內建 **jo_status_code** 欄位。 在我們的範例中，我們使用
   **http_400** 錯誤型別。 請參閱[本節](#error-status)。

   ```
   @action{ActionLoyalty.jo_status_code} == "http_400"
   ```

   ![](assets/action-response7.png)

1. 新增將傳送給您的組織的自訂動作。

   ![](assets/action-response11.png)

## 錯誤狀態{#error-status}

此 **jo_status_code** 欄位一律可用，即使未定義回應裝載亦然。

以下是此欄位可能的值：

* http狀態碼： http_`<HTTP API call returned code>`，例如http_200或http_400
* 逾時錯誤： **逾時**
* 上限設定錯誤： **上限**
* 內部錯誤： **internalError**

當傳回的http程式碼大於2xx或發生錯誤時，會將動作呼叫視為錯誤。 在這種情況下，歷程會流向專用逾時或錯誤分支。

>[!WARNING]
>
>只有新建立的自訂動作包含 **jo_status_code** 現成欄位。 如果您想要將其用於現有的自訂動作，則需要更新動作。 例如，您可以更新說明並儲存。

## 運算式語法

語法如下：

```json
#@action{myAction.myField} 
```

以下是一些範例：

```json
 // action response field
 @action{<action name>.<path to the field>}
 @action{ActionLoyalty.status}
```

```json
 // action response field
 @action{<action name>.<path to the field>, defaultValue: <default value expression>}
 @action{ActionLoyalty.points, defaultValue: 0}
 @action{ActionLoyalty.points, defaultValue: @{myEvent.newPoints}}
```

如需欄位參考的詳細資訊，請參閱 [本節](../building-journeys/expression/field-references.md).
