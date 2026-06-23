---
solution: Journey Optimizer
product: journey optimizer
title: 疑難排解即時動態
description: 瞭解如何針對單一和廣播使用案例（包括設定檔權杖問題、行銷活動設定和傳送失敗）疑難排解Journey Optimizer中的即時活動
role: User
level: Intermediate
exl-id: f0f83bd2-7c2b-4d9b-b455-e1df12dfa175
feature_v2: id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909id: ed2fba79-65cb-4680-96d2-2ad5d851714d
source-git-commit: 8d7aea9c58b0f7622f3b11c21db55536ffe1cb66
workflow-type: tm+mt
source-wordcount: 5964
ht-degree: 1%

---

# 疑難排解即時動態 {#troubleshoot-mobile-live}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;系統化診斷您的Live活動無法出現、更新或結束的原因，以便您解決單一和廣播使用案例中的設定檔權杖、行銷活動設定、裝載和傳遞問題。

>[!ENDSHADEBOX]

Adobe Journey Optimizer中的已上線活動可在iOS鎖定畫面和動態島嶼上啟用即時、動態更新。 它們只能透過API觸發的行銷活動來觸發和管理。

**使用案例型別：**

* **單一**：個別鎖定目標、異動（API觸發的異動行銷活動）
* **廣播**：以對象為目標、大量傳送（API觸發的行銷活動）

Live活動的一個常見挑戰是當API呼叫觸發或更新已上線活動傳回&#x200B;**成功回應(200 OK)**，但Live活動無法在使用者裝置上顯示或更新時。 API確認與實際裝置行為之間的這種中斷可能會發生在傳送管道中的多個點。 本指南提供系統的疑難排解方法，可識別傳送失敗的位置，透過裝置轉譯檢查API請求驗證的每個階段。

## 最常見的問題

| 症狀 | 使用案例 | 前往 |
|---------|----------|-------|
| API傳回「200確定」，但裝置上絕不會出現「即時」活動 | 兩者 | [案例1：設定檔或推播權杖問題](#scenario-1-profile-or-push-token-issues) |
| 已上線活動出現，但不會更新或結束 | 單一(1:1) | [案例4：更新權杖未同步](#scenario-4-live-activity-update-token-not-synced) |
| 行銷活動和代號看起來正確，但傳送仍失敗 | 兩者 | [案例3：傳遞失敗和錯誤分析](#scenario-3-delivery-failures-and-error-analysis) |
| 裝載設定或API結構不清楚 | 兩者 | [案例2：行銷活動設定和裝載問題](#scenario-2-campaign-configuration-and-payload-issues) |
| 特定對象成員未收到廣播 | 廣播 | [案例7：設定檔不在對象中或過時的快照集](#scenario-7-profile-not-in-audience-or-stale-audience-snapshot) |
| 需要以程式設計方式確認執行狀態 | 單一(1:1) | [案例5：透過API檢查執行狀態](#scenario-5-checking-execution-status-via-the-api) |
| 無Assurance存取權；需要生產層級的偵錯 | 兩者 | [進階：透過資料集查詢進行偵錯](#advanced-debugging-via-dataset-queries) |

## 瞭解這兩個使用案例

在偵錯之前，請確認哪個使用案例適用於您的行銷活動。 根本原因和偵錯路徑兩者之間差異極大。

| | 單一(1:1) | 廣播 |
|---|---|---|
| **AJO行銷活動型別** | API觸發的交易式 | API觸發的行銷 |
| **目標定位** | 透過`recipients[].userId`個別設定檔 | 透過`audience.id`的對象區段 |
| **要啟動的Token** | 推播至開始權杖（依設定檔） | `input-push-channel` （每個廣播執行個體） |
| **要更新/結束的Token** | 更新Token （每個「已上線」活動執行個體） | 與開始時間相同`input-push-channel` |
| **對象新鮮度風險** | 不適用 | 長達24小時過時（批次評估） |

## 術語辭彙表

| 術語 | 定義 |
|------|------------|
| **推播至開始權杖** | iOS 17+產生的APN代號，可讓AJO在裝置上遠端啟動即時活動，而不需開啟應用程式。 由行動SDK註冊並儲存在AEP設定檔中。 |
| **更新Token** | 當裝置上開始即時活動時產生的每個執行個體的APN代號。 單一`update`和`end`事件的必要專案。 每個已上線活動執行個體都有自己的唯一更新權杖。 |
| **input-push-channel** | 在Apple開發人員入口網站上為廣播直播活動建立的唯一管道識別碼。 做為廣播更新Token，訂閱此頻道的所有裝置都會收到相同的即時活動事件。 |
| **liveActivityData** | Adobe SDK的`LiveActivityAttributes`通訊協定上的必要屬性。 單一包含`liveActivityID`；廣播包含`channelID`。 必須包含在啟動事件裝載的`attributes`欄位中。 |
| **廣播頻道識別碼** | `input-push-channel`的值。 必須完全符合廣播承載中的`liveActivityData.channelID`。 |
| **attributeType / attributes-type** | Swift `ActivityAttributes`結構的名稱。 在AEP設定檔屬性中儲存為`attributeType` （駝峰式大小寫），並在APS JSON裝載中傳送為`attributes-type` （斷字）。 在不同的表示中，這些是相同的值。 |
| **liveActivityPushNotificationDetails** | 儲存裝置的推送至開始Token `appId`、`platform`和`attributeType`的AEP設定檔屬性。 必須存在且有效，遠端啟動才能運作。 |
| **APS承載** | 在`context.requestPayload.aps`下的API要求內傳送的JSON結構。 包含已上線活動活動、`content-state`、`attributes`和控制欄位。 |
| **保證** | Adobe Experience Platform Assurance，連線測試裝置的即時偵錯工具。 不適用於生產用一般使用者裝置。 |

## 先決條件

進行疑難排解之前，請確定您已：

+++ 適用於Live活動的Assurance外掛程式

Adobe Experience Platform Assurance中的「已上線活動」檢視可驗證應用程式的設定、檢查活動事件，並可讓您從遠端啟動、更新或結束測試工作階段中的活動。

>[!IMPORTANT]
>
> Assurance工作階段僅適用於測試和QA裝置。 一般使用者生產裝置未連線至Assurance。 對於生產診斷，請使用本指南結尾的[進階：透過資料集查詢](#advanced-debugging-via-dataset-queries)節進行偵錯。

### 需求

| 需求 | 詳細資料 |
|---|---|
| iOS裝置 | 執行iOS 16.1或更新版本的實體裝置 |
| Xcode模擬器 | iOS 16.1或laterm **僅限本機啟動**，模擬器不支援透過APN的遠端推播 |
| 從Assurance遠端啟動 | iOS 17.1或更新版本、有效的推播開始代號，以及有效的管道設定 |
| Mobile SDK | Adobe Experience Platform Mobile SDK 5.11.0或更新版本 |
| Session | 作用中的Assurance工作階段 |

### 三個索引標籤

| 標記 | 它顯示的內容 |
|-----|---------------|
| **使用者端資訊** | 裝置、設定檔和App Store憑證。 綠色檢查=設定正確；內嵌警報=建議修正的問題。 將直接對應至以下每個案例中的預先檢查。 |
| **活動** | 所選使用者端的已上線活動：型別（單一/廣播）、ID、狀態和事件計數。 子標籤：概覽（基本資訊+傳送更新按鈕）、活動流程（具有可檢查裝載的生命週期時間表）、事件詳細資料（每個事件的完整裝載檢查）。 |
| **活動** | 適用於使用者端的所有Assurance事件，包括即時活動開始、更新和結束事件。 |

### 從Assurance開始、更新和結束

**啟動已上線活動**。 開啟對話方塊以挑選註冊的活動型別、選擇單一或廣播、輸入廣播頻道ID （僅限廣播），以及編輯預先填寫的APS JSON裝載。 如果不符合開始推播權杖、iOS版本或頻道設定需求，按鈕會停用或傳回錯誤。

**傳送更新**。 從現有活動的Overview索引標籤，傳送更新（推送新內容）或結束事件。 為了統一，外掛程式會自動使用活動的更新Token。 如果是廣播，它會鎖定訂閱相同廣播頻道ID的所有裝置。 裝載必須是有效的JSON，並符合活動的屬性結構描述；否則會拒絕要求。

如需設定和工作階段連線步驟，請參閱[Adobe Experience Platform Assurance檔案](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home.html)。

+++

+++ 收集API觸發的行銷活動詳細資料

在Journey Optimizer中導覽至您的API觸發的行銷活動，並擷取：

* 行銷活動名稱和ID
* Campaign版本（如果適用）
* 行銷活動型別： **異動** （單一）或&#x200B;**行銷** （廣播）
* 表面設定：用於即時活動的iOS應用程式表面
* 活動型別：在行銷活動中設定的`AttributeType`結構名稱

+++

+++ 收集API請求資訊

發出API呼叫以觸發即時活動時，請儲存：

* API要求裝載，包括設定檔識別碼和即時活動資料
* API回應，包括狀態代碼、訊息ID、請求ID
* 呼叫API的時間戳記
* 使用的端點，例如`/campaign/{CAMPAIGN_ID}/execute`

+++

+++ 識別測試設定檔

從您的API請求中擷取：

* 設定檔名稱空間，例如ECID、電子郵件、客戶ID
* API呼叫中使用的設定檔ID

確定您可以在Adobe Experience Platform中查詢此設定檔。 在Experience Platform檔案](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html)中瞭解如何[查詢設定檔。

+++

+++ 裝置和應用程式資訊

從測試裝置收集下列專案：

* 裝置型號，例如iPhone 14 Pro
* iOS版本
* 應用程式套件組合識別碼
* APNs推播權杖
* 測試時的網路連線狀態

+++

## 常見案例

### 案例1：設定檔或推播權杖問題 {#scenario-1-profile-or-push-token-issues}

[!BADGE 適用於單一和廣播使用案例]{type=Positive}

API傳回HTTP 200，但未顯示上線活動。 常見原因：

* 設定檔不存在於Adobe Experience Platform中。
* 即時活動推播權杖尚未同步至設定檔。
* 已同步即時活動推播詳細資料，但包含不正確的設定，例如，錯誤的`appId`或`attributeType`。

**廣播使用案例的注意事項**：如果對象中的某些設定檔遺失權杖，則只有這些設定檔將無法接收即時活動。 從您的對象中取樣數個設定檔，以診斷Token問題。 這僅適用於遠端開始事件，不適用於更新或結束事件。

#### 預先檢查

* iOS應用程式需求：
   * iOS 16.1+
   * 在`Info.plist`中將`NSSupportsLiveActivities`設定為`YES`
   * `ActivityAttributes`已正確實作。
* 行動SDK整合：
   * Adobe Experience Platform Mobile SDK （傳訊SDK 5.11.0+）
   * 使用Live活動推播權杖實作及呼叫`Messaging.registerLiveActivities`。

#### 偵錯步驟

+++ &#x200B;1. 驗證Adobe Experience Platform中存在設定檔

1. 在Journey Optimizer中，導覽至&#x200B;**客戶** `>` **設定檔**。
1. 使用API請求的名稱空間和身分值來搜尋。
1. 如果找不到設定檔，表示設定檔不存在或內嵌未完成。 在觸發上線活動之前，請建立設定檔或等待擷取。
1. 如果找到設定檔，請繼續執行下方的步驟2以檢查推送代號是否已同步。

+++

+++ &#x200B;2. 檢查即時活動推播權杖是否已同步

您可以使用Assurance來驗證Token註冊：

1. 在Assurance中，從&#x200B;**事件**&#x200B;清單，篩選或搜尋事件`eventType = "liveActivity.pushToStart"`。
1. 選取&#x200B;**事件**&#x200B;並檢查裝載。
1. 檢查權杖、appId和attributeType值是否存在。
1. 確認事件是否成功傳送。

您也可以存取Adobe Experience Platform設定檔。

1. 在Adobe Experience Platform中，從您的&#x200B;**設定檔**&#x200B;存取&#x200B;**事件**&#x200B;索引標籤。
1. 搜尋`liveActivity.pushToStart`個事件。
1. 檢查偶數時間戳記和承載。

如果找不到事件，表示您的行動應用程式無法正確呼叫`Messaging.registerLiveActivity`。 您需要修正SDK整合。

+++

+++ &#x200B;3. 驗證設定檔上的Token詳細資料

1. 從您的&#x200B;**設定檔**，存取&#x200B;**屬性**&#x200B;標籤。
1. 找到`liveActivityPushNotificationDetails`。
1. 驗證權杖設定：

   ```json
   {
      "liveActivityPushNotificationDetails": [
      {
         "appId": "com.example.myapp",
         "token": "abc123def456...",
         "platform": "apns",
         "denylisted": false,
         "attributeType": "OrderTrackingAttributes",
         "identity": {}
      }
      ]
   }
   ```

**驗證每個欄位：**

| 欄位 | 需求 | 常見問題 |
|-|-|-|
| `appId` | 必須完全符合iOS套件組合識別碼 | 開發/生產套件組合ID不相符 |
| `attributeType` | 必須完全符合Swift `ActivityAttributes`結構名稱（區分大小寫） | 拼寫錯誤或不正確的結構名稱 |
| `platform` | 必須為`"apns"`或`"apnsSandbox"` | 錯誤的平台值 |
| `denylisted` | 必須為`false` | 權杖標示為無效或使用者選擇退出 |
| `token` | 有效的APN推播權杖 | Token已過期或重新安裝應用程式 |

如果任何欄位不正確：更新行動應用程式，使用`Messaging.registerLiveActivities`重新註冊，等待5到10分鐘，然後重新檢查。

如果`liveActivityPushNotificationDetails`遺失： Token尚未同步。 在Assurance中看到`liveActivity.pushToStart`事件後，請等待5至10分鐘。

+++

### 案例2：促銷活動設定和裝載問題 {#scenario-2-campaign-configuration-and-payload-issues}

[!BADGE 適用於單一和廣播使用案例]{type=Positive}

具有有效權杖的設定檔已存在，但未顯示即時活動。 這可能是由於：

* 介面或通道設定錯誤。
* API裝載結構不正確。
* `content-state`和`attributes`不符合iOS `ActivityAttributes`實作。
* 過時`timestamp` （更新/結束的關鍵）。

**廣播使用案例的注意事項**：行銷活動必須是&#x200B;**API觸發的行銷** （非異動）。 承載使用`audience`，而非個別`profile`。 請參閱[此章節](#broadcast-config)以取得廣播特定的裝載結構，並參閱[Adobe Developer檔案](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution)以取得完整的API規格。

#### 預先檢查

* 行銷活動為&#x200B;**API觸發的交易式** （單一）或&#x200B;**API觸發的行銷** （廣播），且&#x200B;**高輸送量**&#x200B;選項必須為&#x200B;**未啟用**，因為它與即時活動不相容。
* 使用上述[案例](#scenario-1-profile-or-push-token-issues)，確定設定檔存在且權杖已正確同步。

#### 偵錯步驟

+++ &#x200B;1. 驗證行銷活動表面設定

1. 在Journey Optimizer中，開啟您的&#x200B;**行銷活動**&#x200B;並導覽至&#x200B;**動作**&#x200B;功能表。
1. 檢查您的&#x200B;**上線活動設定**。 您必須使用符合設定檔`liveActivityPushNotificationDetails`中`appId`的套件組合識別碼，為iOS應用程式設定表面。 例如，如果您的設定檔有`"appId": "com.example.myapp"`，則表面必須針對相同的應用程式。
1. 檢查促銷活動組態中的&#x200B;**活動型別**&#x200B;是否與設定檔`liveActivityPushNotificationDetails`中的`attributeType`完全相符。 例如，如果您的設定檔有`"attributeType": "FoodDeliveryLiveActivityAttributes"`，則行銷活動必須指定此相同的活動型別。

+++

+++ &#x200B;2. 驗證API裝載結構

透過API執行行銷活動時，請確定裝載遵循正確結構。

**單一承載：**

```json
{
   "campaignId": "your-campaign-id",
   "recipients": [{
      "type": "aep",
      "userId": "user@example.com",
      "namespace": "email",
      "context": {
      "requestPayload": {
         "aps": {
            "content-available": 1,
            "timestamp": 1756984054,
            "event": "start",
            "attributes-type": "FoodDeliveryLiveActivityAttributes",
            "content-state": { ... },
            "attributes": { ... }
         }
      }
      }
   }]
}
```

**常見承載問題：**

| 欄位 | 需求 | 常見問題 |
|-|-|-|
| `attributes-type` | 必須符合行銷活動型別與設定檔`attributeType` | 不符或拼寫錯誤 |
| `campaignId` | 必須符合啟用的行銷活動ID | 行銷活動ID錯誤或遺失 |
| `content-available` | 必須為`1` | 值遺失或錯誤 |
| `event` | 必須為`"start"`、`"update"`或`"end"` | 無效的事件型別 |
| `timestamp` | 必須永遠為目前/最新的Unix紀元時間（以秒為單位） | 使用舊的/快取的時間戳記 |
| `userId` / `namespace` | 必須與AEP中的現有設定檔相符 | 設定檔識別碼不相符 |

**嚴重：一律使用最新的時間戳記**

* 進行每個API呼叫時，`timestamp`欄位必須&#x200B;**一律**&#x200B;為&#x200B;**目前的Unix紀元時間** （以秒為單位）。
* 這適用於&#x200B;**所有事件型別**： `start`、`update`以及&#x200B;**特別是`end`**。
* **對更新/結束要求的影響**：使用過時或舊時間戳記會導致更新及結束要求失敗或被裝置忽略。
* 請&#x200B;**不**&#x200B;重複使用先前請求的時間戳記，或使用快取的值。
* 為每個API呼叫產生新的時間戳記。

**選用欄位（所有事件型別）：**

* `requestId`：追蹤的唯一識別碼（建議）。
* `alert`：通知物件有`title`和`body` （有助於提醒注意更新）。

**關於`dismissal-date`：**

* 包含Unix紀元時間（秒）的可選欄位。
* **僅在`event: "end"`**&#x200B;時相關。
* 指定何時應自動從裝置移除即時活動。
* 如果未在最終事件中提供，則即時活動會維持可見，直到使用者將其解除為止。
* 必須為未來的時間戳記（晚於`timestamp`）。

+++

+++ &#x200B;3. 將裝載與iOS實作對齊

確認您的API裝載符合您的iOS應用程式的`ActivityAttributes`實作。 Adobe SDK的`LiveActivityAttributes`通訊協定擴充iOS `ActivityAttributes`，並需要`liveActivityData`屬性。

**驗證對應：**

1. 您的`ActivityAttributes`必須實作Adobe的`LiveActivityAttributes`通訊協定。 範例：

   ```swift
   struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
      public struct ContentState: Codable, Hashable {
         var orderStatus: String
         var estimatedDeliveryTime: String
      }
   
      // Adobe SDK requirement
      var liveActivityData: LiveActivityData
   
      // Your custom attributes
      var restaurantName: String
   }
   ```

   **請注意** `liveActivityData`欄位是Adobe SDK的必要欄位，必須包含在所有實作中。

1. 您的API裝載必須映象iOS結構：

   ```json
   {
      "aps": {
         "event": "start",
         "timestamp": 1756984054,
         "attributes-type": "FoodDeliveryLiveActivityAttributes",
         "content-state": {
         "orderStatus": "Preparing",
         "estimatedDeliveryTime": "20 mins"
      },
      "attributes": {
         "liveActivityData": {
         "liveActivityID": "order-12345"
         },
         "restaurantName": "Pizza Palace"
      }
      }
   }
   ```

**驗證檢查清單：**

* 在`content-state`中包含所有`ContentState`欄位（所有事件型別都需要）。
* 在`attributes`中包含所有`LiveActivityAttributes`欄位（僅限開始事件），包括：
   * `liveActivityData` （必要；通常包含`liveActivityID`或類似的識別碼）
   * 結構中的所有自訂欄位
* 完全符合欄位名稱（區分大小寫）。
* 符合資料型別（String、Int、Bool、巢狀物件）。
* 保留巢狀物件結構。

**常見錯誤：**

| 問題 | 影響 | 修正 |
|-------|--------|-----|
| 屬性中遺失`liveActivityData` | 即時活動不會開始 | 一律在開始事件中包含`liveActivityData`物件 |
| 啟動事件中缺少必填欄位 | 即時活動不會開始 | 從iOS結構新增所有欄位 |
| 欄位名稱錯誤（拼寫錯誤/大小寫） | 欄位被忽略或剖析錯誤 | 完全符合iOS欄位名稱 |
| 錯誤的資料型別 | 剖析錯誤 | 符合iOS資料型別 |
| 遺失巢狀物件 | 不完整的資料 | 包含所有巢狀結構 |
| 在更新/結束中包括`attributes` | 不必要，但通常會忽略 | 在開始事件中僅包含`attributes` |
| 更新/結束時的過時時間戳記 | 裝置忽略更新/結束 | 一律產生新的時間戳記 |

如需更多範例，請參閱[建立即時活動頁面](create-mobile-live.md)。

+++

+++ &#x200B;4. 使用Assurance進行測試

使用Assurance驗證API執行和裝載傳送：

1. 開啟您的Assurance工作階段。
1. 執行API呼叫以觸發上線活動。
1. 在&#x200B;**事件清單**&#x200B;中，檢查：
   * 行銷活動執行事件。
   * 已上線的活動傳送活動。
   * 裝載驗證錯誤事件。
1. 檢閱事件裝載以驗證：
   * 已正確處理承載。
   * 沒有發生驗證錯誤。
   * 已將上線活動傳送至APN。

+++

### 案例3：傳送失敗和錯誤分析 {#scenario-3-delivery-failures-and-error-analysis}

[!BADGE 適用於單一和廣播使用案例]{type=Positive}

在此案例中，所有先前的檢查均已通過：

* 具有[有效即時活動推播權杖的設定檔存在](#scenario-1-profile-or-push-token-issues)
* 行銷活動[已正確設定適當的承載](#scenario-2-campaign-configuration-and-payload-issues)
* [更新Token已同步](#scenario-4-live-activity-update-token-not-synced) （僅適用於更新/結束事件、單一使用案例）

但已上線的活動還是沒有如預期般出現、更新或結束。 問題可能是Adobe傳遞系統層級或推播通知服務提供者(APN)的問題。

**廣播使用案例的注意事項**：報表顯示所有對象成員的量度。 有些設定檔可能會成功，而有些設定檔則會失敗。

**預先檢查**

* **已驗證的先前案例：**
   * 具有正確`liveActivityPushNotificationDetails`的設定檔已存在
   * 行銷活動表面和活動型別正確
   * API裝載對目前時間戳記有效
   * 更新Token已同步（適用於更新/結束事件）

* **已確認的API呼叫：**

   * API呼叫傳回HTTP 200 （成功）
   * 行銷活動ID和收件者詳細資料正確

#### 偵錯步驟

+++ &#x200B;1. 檢查行銷活動報告

1. 導覽至您的&#x200B;**即時活動行銷活動**。
1. 按一下&#x200B;**報表**&#x200B;按鈕。
1. 選取&#x200B;**檢視所有時間報表**。
1. 檢閱下列章節：

   1. 檢查&#x200B;**傳送統計資料**&#x200B;量度以瞭解傳送成功：

      | 量度 | 其含義 | 要尋找的內容 |
      |-|-|-|
      | 已鎖定目標 | 符合對象資格的設定檔數 | 應該包含您的測試設定檔 |
      | 傳送 | 嘗試的推播通知總數 | 應該符合您的API呼叫 |
      | 已傳遞 | 已成功傳遞至裝置 | 與傳送比較以檢視成功率 |
      | 傳送錯誤 | 無法傳送的推播通知 | 高數字 |
      | 傳送排除專案 | Adobe Journey Optimizer排除的設定檔 | 檢查您的設定檔是否已排除 |

   1. 如果傳送錯誤> 0，請檢查&#x200B;**錯誤原因**&#x200B;資料表以取得特定的錯誤碼和訊息：

      | 常見錯誤 | 含義 | 解決方法 |
      |-|-|-|
      | 權杖無效 | 推播權杖無效或過期 | 從裝置重新註冊即時活動權杖 |
      | 找不到語彙基元 | 沒有與設定檔相關聯的有效權杖 | 驗證`liveActivityPushNotificationDetails`是否存在 |
      | 已拒絕APN | Apple推播通知服務已拒絕推播 | 檢查APNs憑證、套件ID、環境 |
      | 網路逾時 | 無法連線APN | 暫時性問題；請重試API呼叫 |

   1. 如果&#x200B;**傳送排除專案** > 0，請檢查&#x200B;**排除的原因**&#x200B;資料表：

      | 常見排除 | 含義 | 解決方法 |
      |-|-|-|
      | 設定檔已選擇退出 | 使用者已選擇退出通知 | 檢查設定檔同意狀態 |
      | 權杖已加入封鎖清單 | 標籤為無效的權杖 | 重新註冊Token或檢查封鎖清單狀態 |
      | 設定檔不合格 | 設定檔不符合行銷活動條件 | 檢閱行銷活動對象規則 |

在[即時活動行銷活動報告頁面](../reports/campaign-global-report-cja-activity.md)瞭解更多。

+++

+++ &#x200B;2. 檢查設定檔中的訊息回饋事件

1. 導覽至Journey Optimizer中的&#x200B;**客戶** > **設定檔**。
1. 搜尋並開啟設定檔。
1. 選取&#x200B;**事件**&#x200B;標籤。
1. 篩選或搜尋具有`eventType = "message.feedback"`的事件。
1. 尋找與您上線活動的`liveActivityID`和`event`型別相符的意見反應事件。
1. 檢閱下列重要欄位：

   | 欄位 | 可能的值 | 其含義 |
   |---|---|---|
   | `feedbackStatus` | `sent`, `error`, `denylist` | 來自服務提供者的傳遞結果 |
   | `serviceProvider` | `apns/apnsSandbox` | 應該是iOS Live活動的APN |
   | `errorCode` | 數值代碼或`null` | APNs專屬錯誤碼（若失敗） |
   | `errorMessage` | 錯誤描述或`null` | 人類看得懂的錯誤訊息 |

1. **若`feedbackStatus: "error"`：**
   * 檢查`errorCode`和`errorMessage`是否有特定的APN錯誤
   * 常見的APN錯誤包括過期的權杖、無效的憑證、錯誤的套件組合識別碼

1. **如果找不到意見反應事件：**
   * 可能尚未嘗試推播通知
   * 如上述步驟1所述，檢查促銷活動報表中是否排除設定檔。

+++

+++ &#x200B;3. 驗證Assurance中傳送至APN的即時活動

1. 開啟您的Assurance工作階段，它必須在API呼叫期間作用中。
1. 執行API呼叫（開始、更新或結束）。
1. 在&#x200B;**活動清單**&#x200B;中，尋找已上線活動傳遞活動。
1. 搜尋與APN推送傳遞相關的事件。
1. 檢查下列指標：
   * **推送要求至APN**：確認Adobe已傳送推送要求至Apple的伺服器
   * **APN回應**：顯示APN是否接受或拒絕推播
   * **傳遞狀態**：成功或失敗指示
1. 如果發現問題，請參閱以下常見的APN傳送問題：

   | 問題 | Assurance中的症狀 | 解決方法 |
   |-|-|-|
   | APNs憑證已過期 | 驗證錯誤 | 更新及上傳新的APNs憑證 |
   | 錯誤的環境（開發環境vs生產環境） | 權杖不符錯誤 | 確保憑證符合應用程式建置型別 |
   | 套件組合ID不相符 | 無效的套件組合識別碼 | 驗證憑證套件組合ID是否與應用程式相符 |
   | 權杖已到期 | 來自APN的InvalidToken錯誤 | 重新註冊即時活動權杖 |
   | 速率限制 | 請求次數過多 | 降低API呼叫頻率 |

+++

+++ &#x200B;4. 繼續其他診斷檢查

1. 檢查行銷活動報告中的即時活動生命週期量度。

   在行銷活動報告中，檢閱&#x200B;**即時活動生命週期**&#x200B;區段：

   | 量度 | 檢查內容 |
   |-|-|
   | 遠端啟動 | 應該顯示API觸發的開始計數 |
   | 更新 | 應該顯示更新事件的計數 |
   | 結束 | 應該顯示結束事件的計數 |
   | 總計計數 | 整體已上線活動活動量度 |

   如果這些量度為零或不符合您的API呼叫，則Adobe與APN之間會發生傳送問題。

1. 如果Adobe顯示傳送成功，但裝置未顯示已上線的活動：

   * 檢查iOS裝置記錄檔中的即時活動錯誤。
   * 驗證應用程式在前景或背景（未終止）。
   * 確認裝置具有網路連線。
   * 在多個裝置上測試以排除裝置特定問題。
   * 確認iOS版本為16.1或更新版本。

+++

+++ &#x200B;5. 提升至Adobe支援

如果您已完成所有步驟，但問題仍未解決，請聯絡Adobe客戶服務，聯絡：

**必要資訊：**

* 行銷活動 ID 和名稱
* 設定檔名稱空間和ID
* 來自API裝載`liveActivityID`
* API呼叫的時間戳記
* 熒幕擷圖：
* 行銷活動報告（傳送統計資料、錯誤原因、排除的原因）
* 設定檔事件(`liveActivity.updateToken`， `message.feedback`)
* 顯示傳遞事件的Assurance工作階段
* 完成API請求裝載
* APNs憑證詳細資料（到期、環境、套件組合ID）

+++

## 單一特定案例

### 案例4：即時活動更新Token未同步 {#scenario-4-live-activity-update-token-not-synced}

裝置上的即時活動已成功啟動，但後續`update`或`end` API呼叫（傳回HTTP 200）無法更新或解除即時活動。 當&#x200B;**即時活動更新Token**&#x200B;未正確同步至Adobe的系統時，就會發生這種情況。

**瞭解更新Token**

當上線活動在裝置上開始時，iOS會為該特定上線活動執行個體產生唯一的更新權杖。 下列專案需要此代號：

* 傳送更新至已上線活動
* 從遠端結束即時活動

每個已上線活動執行個體都有自己的唯一更新權杖。 Adobe需要此Token才能傳遞更新和結束事件。

**預期行為**

若要讓更新與結束事件運作，必須發生下列情況：

1. 裝置上的即時活動已成功啟動。
1. 裝置產生該即時活動執行個體的更新權杖。
1. 行動SDK會擷取更新Token並將其傳送至Adobe。
1. 更新Token會同步並儲存在Adobe的系統中。
1. 針對更新/結束的後續API呼叫會使用此權杖進行傳送。

**預先檢查：**

* **使用者許可權**：首次在裝置上啟動即時活動時，iOS會顯示系統提示：「允許[應用程式名稱]提供即時活動更新？」 使用者&#x200B;**必須點選[允許]**&#x200B;才能產生並同步更新權杖。 如果使用者點選「不允許」，則不會建立任何更新Token，且更新/結束請求將失敗。 這是每個應用程式的一次性許可權。
* **設定檔和促銷活動驗證**：完成[案例1](#scenario-1-profile-or-push-token-issues)和[案例2](#scenario-2-campaign-configuration-and-payload-issues)檢查，以確保設定檔、代號和促銷活動設定正確無誤。

#### 偵錯步驟

+++ 驗證Assurance中的更新權杖同步

1. 開啟您的Assurance工作階段。
1. 確定工作階段在裝置上開始即時活動時處於作用中狀態。
1. 篩選或搜尋具有`eventType = "liveActivity.updateToken"`的事件。
1. 選取事件並檢查裝載：

   * 請確認`token`欄位包含有效的更新Token字串。
   * 檢查`liveActivityID`是否與您的即時活動執行個體相符。
   * 確認`activityType`符合您的`attributes-type`。

1. 如果找不到事件：

   * SDK未產生或擷取更新Token。
   * 檢查使用者是否已授與上線活動許可權。
   * 確認已在裝置上成功啟動上線活動。
   * 確認行動SDK已正確整合以擷取更新Token。

1. 如果找到事件，請繼續進行步驟2。

+++

+++ &#x200B;2. 驗證設定檔事件中的更新權杖

1. 導覽至Journey Optimizer中的&#x200B;**客戶** > **設定檔**。
1. 搜尋並開啟設定檔。
1. 選取&#x200B;**事件**&#x200B;標籤。
1. 尋找`liveActivity.updateToken`個事件。
1. 檢查事件詳細資料：

   * 驗證時間戳記是否為最近（符合上線活動開始的時間）。
   * 確認`token`和`liveActivityID`是否存在。
   * 請確定`activityType`正確。

1. 如果在設定檔中找不到事件：

   * 更新Token事件可能尚未內嵌至設定檔。
   * 等待5到10分鐘，然後重新檢查。
   * 如果15分鐘後仍然遺失，則可能是事件擷取問題。

1. 如果找到事件，則表示更新Token已同步。 您可以繼續進行步驟3。

+++

+++ &#x200B;3. 檢查Assurance中的即時活動傳送事件

1. 在您的Assurance工作階段中，執行更新或結束API呼叫。
1. 在&#x200B;**事件清單**&#x200B;中，尋找已上線活動傳遞事件（APNs推播事件）。
1. 檢查事件以指出：
   * 推播通知已傳送至APN。
   * APN的回應（成功或錯誤）。
   * 傳遞確認。
1. 如果APNs傳送事件存在：已傳送推播通知。 如果裝置仍未更新，則問題可能出在裝置端（應用程式未處理推播、網路問題等）。
1. 如果APN傳遞事件遺失：更新Token可能無法正確儲存，或與Adobe系統中的設定檔建立關聯。
1. 如果出現錯誤事件：檢查錯誤詳細資料以找出特定的失敗原因（無效的Token、拒絕的APN等）。

+++

### 案例5：透過API檢查執行狀態 {#scenario-5-checking-execution-status-via-the-api}

[!BADGE 僅套用至單一(1:1)使用案例]{type=Informative}

觸發單一即時活動後，**GET訊息執行API**&#x200B;會傳回執行的目前狀態。 使用它來確認執行是否已排入佇列、進行中、完成或失敗，而不等待意見反應事件進入資料集。

`executionId`是觸發程式回應中傳回的訊息ID。 對於單一執行，其前置詞為`HUOC-`。

#### 端點和範例要求

**端點**： `GET https://cjm.adobe.io/imp/message/executions/{executionId}`

```bash
curl --location 'https://cjm.adobe.io/imp/message/executions/HUOC-123456' \
  --header 'x-gw-ims-org-id: <IMS_ORG_ID>' \
  --header 'Authorization: Bearer <ACCESS_TOKEN>' \
  --header 'x-sandbox-name: <SANDBOX_NAME>' \
  --header 'x-sandbox-id: <SANDBOX_UUID>' \
  --header 'x-api-key: <API_KEY>'
```

#### HTTP回應代碼

| 程式碼 | 含義 |
|------|---------|
| 200 OK | 找到執行並成功傳回 |
| 401未獲授權 | 持有人權杖遺失或無效 |
| 403禁止 | 有效的Token，但許可權不足 |
| 404找不到 | 執行識別碼不存在 |

#### 執行狀態值

200回應中的`status`欄位表示執行進度：

| 狀態 | 說明 |
|--------|-------------|
| `PENDING` | 執行已佇列但尚未開始 |
| `INPROGRESS` | 目前正在處理執行 |
| `COMPLETED` | 執行已成功完成 |
| `FAILED` | 執行發生錯誤 |

200回應也傳回`executionType` （`unitary`或`batch`）、`executionRunMode` （`default`或`test`）以及含有將執行繫結回觸發行銷活動或歷程的中繼資料（`campaignId`、`journeyId`、`batchInstanceId`、資產資訊）的`source`區塊。

## 廣播特定案例

### 案例6：廣播行銷活動設定和裝載問題{#broadcast-config}

[!BADGE 僅套用至廣播使用案例]{type=Informative}

本節說明廣播直播活動專屬的疑難排解案例，這些案例需要與單一行銷活動不同的偵錯方法。

當設定檔具有有效的權杖，但受眾成員的即時活動未出現、更新或按預期行事時，問題通常源於以下問題之一：

* 行銷活動未設定為API觸發的行銷。
* API承載使用不正確的廣播結構（遺失`audience`或`input-push-channel`）。
* `content-state`和`attributes`欄位不符合iOS `ActivityAttributes`實作。
* 未在Apple開發人員入口網站上正確建立`input-push-channel`。

此疑難排解案例適用於廣播行銷活動中的所有即時活動事件： `start`、`update`和`end`。

**預先檢查：**

* **促銷活動型別**：
   * 確認行銷活動建立為API觸發的行銷活動（廣播/對象型行銷活動的必要專案）。
   * 確認對象已定義於行銷活動設定中。
* **設定檔和權杖驗證**：從對象中取樣多個設定檔，以驗證它們是否具有有效的`liveActivityPushNotificationDetails`。 如需詳細的驗證步驟，請遵循[案例1](#scenario-1-profile-or-push-token-issues)。

#### 偵錯步驟

+++ &#x200B;1. 驗證Campaign對象設定

1. 在Journey Optimizer中開啟&#x200B;**API觸發的行銷活動**。
1. 導覽至&#x200B;**對象**&#x200B;區段並驗證：
   * 已為行銷活動選取閱聽眾。
   * 對象ID符合您的API裝載中使用的對象ID。
   * 對象包含預期的設定檔。
1. 導覽至&#x200B;**動作**&#x200B;區段。
1. 檢查&#x200B;**上線活動設定**：
   * 必須使用正確的套件識別碼為iOS應用程式設定設定。
   * 活動型別必須符合您API承載中的`attributes-type`。 例如，如果您的裝載包含`"attributes-type": "AirplaneTrackingAttributes"`，則行銷活動必須指定此相同的活動型別。

+++

+++ &#x200B;2. 驗證廣播API裝載結構

廣播裝載結構與單一行銷活動不同。 確認您的裝載是否遵循正確的廣播格式。

**廣播的必要欄位：**

```json
{
   "campaignId": "878a11d4-b519-47bd-8313-fecfee19857b",
   "audience": {
      "id": "8c3dbdea-2957-401f-acf0-3966fba1601e"
   },
   "context": {
      "requestPayload": {
      "aps": {
         "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
         "content-available": 1,
         "timestamp": 1771829292,
         "event": "update",
         "attributes-type": "AirplaneTrackingAttributes",
         "content-state": { ... },
         "attributes": { ... }
      }
      }
   }
}
```

**常見承載問題：**

| 欄位 | 需求 | 常見問題 |
|-|-|-|
| `campaignId` | 必須符合已啟用的行銷活動ID | 錯誤的行銷活動ID或使用異動行銷活動 |
| `audience.id` | 必須符合AEP中的現有對象 | 錯誤的對象ID或對象不存在 |
| `input-push-channel` | 廣播必填 — 此廣播執行個體的唯一識別碼 | 遺失或不符合`liveActivityData`中的`channelID` |
| `timestamp` | 必須永遠為目前/最新的Unix紀元時間（以秒為單位） | 使用舊的/快取的時間戳記 |
| `event` | 必須為`"start"`、`"update"`或`"end"` | 無效的事件型別 |
| `attributes-type` | 必須符合行銷活動活動型別 | 不符或拼寫錯誤 |
| `content-available` | 必須為`1` | 值遺失或錯誤 |

**重要廣播特定欄位：**

* **`input-push-channel`**:
   * 所有廣播Live活動皆需要。
   * 作為此特定廣播執行個體的唯一識別碼。
   * 對象中的所有設定檔都會收到連結至此管道的已上線活動。
   * 必須符合`liveActivityData.channelID`中的`channelID` （請參閱步驟3）。
   * 使用者端必須在Apple開發人員入口網站上為`appID`建立。
   * 只有為特定`appID`建立的頻道才能用來廣播該應用程式上的即時活動。

* **`audience.id`**:
   * 必須參考在Adobe Experience Platform中建立的有效對象區段。
   * 此對象中的所有設定檔都是上線活動的目標。
   * 必須啟用對象，並包含具有有效`liveActivityPushNotificationDetails`的設定檔。

**一律使用最新的時間戳記：**

* `timestamp`欄位一律為每個API呼叫的目前Unix紀元時間（以秒為單位）。
* 此要求適用於所有事件型別： `start`、`update`和`end`。
* **更新/結束的關鍵**：使用過時的時間戳記會導致更新和結束要求失敗。
* 為每個廣播API呼叫產生新的時間戳記。

**選用欄位：**

* `dismissal-date`：自動解除的Unix紀元時間（僅與`end`個事件相關）
* `alert`：通知物件有`title`和`body`

如需完整API規格，請參閱[Adobe Journey Optimizer傳訊API檔案](https://developer.adobe.com/journey-optimizer-apis/references/messaging)。

+++

+++ &#x200B;3. 讓內容狀態、屬性和輸入推播通道與iOS實作一致

確認承載欄位符合您的iOS應用程式的`ActivityAttributes`實作，且`input-push-channel`符合`liveActivityData`中的`channelID`。

1. 檢閱您的iOS ActivityAttributes定義。

您的自訂`ActivityAttributes`結構必須實作Adobe的`LiveActivityAttributes`通訊協定：

```swift
struct AirplaneTrackingAttributes: LiveActivityAttributes {
   public struct ContentState: Codable, Hashable {
      var journeyProgress: Int
   }
   
   // Adobe SDK requirement
   var liveActivityData: LiveActivityData
   
   // Your custom attributes
   var arrivalAirport: String
   var departureAirport: String
   var arrivalTerminal: String
}
```

1. 將iOS欄位對應至廣播API裝載。

對於所有事件，同時包含`attributes`和`content-state`：

```json
      {
      "aps": {
         "input-push-channel": "FEt0NgvLEfEAAOqA6AXdIQ==",
         "event": "start",
         "timestamp": 1771829292,
         "attributes-type": "AirplaneTrackingAttributes",
         "content-state": {
         "journeyProgress": 0
         },
         "attributes": {
         "arrivalAirport": "DEL",
         "departureAirport": "MUM",
         "arrivalTerminal": "T1",
         "liveActivityData": {
            "channelID": "FEt0NgvLEfEAAOqA6AXdIQ=="
         }
         }
      }
      }
```

**嚴重： `input-push-channel`必須符合`channelID`**

* `aps`根目錄中的`input-push-channel`值必須與`liveActivityData`中的`channelID`完全相符。
* 在上述範例中，兩個值均為`"FEt0NgvLEfEAAOqA6AXdIQ=="`。
* 此比對會將廣播例項連結至即時活動資料。
* 不相符會導致傳遞失敗。

**關鍵驗證點：**

* 包含所有事件型別`content-state`中的所有`ContentState`欄位。
* 僅針對開始事件在`attributes`中包含所有自訂`LiveActivityAttributes`欄位。
* 對於開始事件，`liveActivityData.channelID`必須符合`input-push-channel`。
* 欄位名稱會區分大小寫，且必須完全相符。
* 資料型別必須相符（字串、Int、Bool、巢狀物件等）。
* 對於更新/結束事件，請使用與原始開始事件相同的`input-push-channel`。

**常見錯誤：**

| 問題 | 影響 | 修正 |
|-|-|-|
| 遺失`input-push-channel` | 廣播無法運作 | 為每個廣播新增唯一的頻道ID |
| `input-push-channel`不符合`channelID` | 即時活動不會開始 | 確定兩個值相同 |
| 更新/結束的不同`input-push-channel` | 更新/結束將不會到達已上線活動 | 在整個生命週期中使用相同的管道ID |
| 遺失`liveActivityData.channelID` | 即時活動將不會連結到廣播 | 在開始事件的屬性中包含`channelID` |
| 啟動事件中缺少必填欄位 | 即時活動不會開始 | 從iOS結構新增所有欄位 |
| 欄位名稱錯誤（拼寫錯誤/大小寫） | 欄位被忽略或剖析錯誤 | 完全符合iOS欄位名稱 |
| 更新/結束時的過時時間戳記 | 裝置忽略更新/結束 | 一律產生新的時間戳記 |

+++

+++ &#x200B;4. 使用Assurance進行測試

使用Assurance驗證API執行和裝載傳送：

1. 在屬於閱聽眾的測試裝置上開啟Assurance工作階段。
1. 執行廣播API呼叫。
1. 在&#x200B;**事件清單**&#x200B;中尋找：
   * 行銷活動執行事件。
   * 已上線的活動傳送活動。
   * 指示裝載驗證失敗的錯誤事件。
1. 檢查事件裝載以確認：
   * 已正確處理承載。
   * `input-push-channel`已存在。
   * 沒有發生驗證錯誤。
   * 已將上線活動傳送至對象成員的APN。

+++

### 案例7：設定檔不在對象中或過時的對象快照 {#scenario-7-profile-not-in-audience-or-stale-audience-snapshot}

在此案例中，行銷活動和裝載已正確設定，但特定設定檔不會接收即時活動。 這通常發生在以下情況：

* 設定檔不是連結至行銷活動的對象成員。
* 對象是批次對象，並包含設定檔資料的過時快照。
* 設定檔的即時活動權杖最近已新增，但尚未反映在對象快照中。

此疑難排解案例尤其適用於使用受眾型定位的廣播行銷活動。

**瞭解對象評估**

Adobe Experience Platform使用不同的對象評估方法，判斷設定檔更新何時會反映在對象中：

| 方法 | 評估頻率 | 資料新鮮度 | 最適合 |
|-|-|-|--|
| 批次 | 每日（已排程）一次 | 可能長達24小時已過時 | 大型受眾，不區分時間 |
| 串流 | 即時（設定檔變更） | 更新的設定檔近乎即時 | 時效性，需要設定檔更新 |

**預先檢查：**

* **行銷活動和承載驗證**：
   * 完成[此情境](#broadcast-config)中的檢查，以確保行銷活動和承載正確。
   * 確認API承載中的`audience.id`符合行銷活動設定。
* **設定檔存在**：確認設定檔存在於AEP中，且有效`liveActivityPushNotificationDetails`。

#### 偵錯步驟

+++ &#x200B;1. 驗證設定檔位於對象中

首先，確認應接收上線活動的設定檔是否實際屬於對象。

1. 導覽至Adobe Experience Platform中的&#x200B;**對象**。
1. 使用行銷活動中的`audience.id`搜尋並開啟對象。
1. 按一下&#x200B;**瀏覽**&#x200B;或&#x200B;**範例設定檔**&#x200B;以檢視對象成員。
1. 使用名稱空間和身分值搜尋您的測試設定檔。
1. **如果在對象中找不到設定檔：**
   * 設定檔不符合對象條件或區段規則。
   * 檢閱對象定義以瞭解成員資格要求。
   * 更新設定檔資料或對象定義，以包含設定檔。
   * 等待對象評估完成（請參閱步驟2）。
1. **如果在對象中找到設定檔：**&#x200B;請繼續執行步驟2以檢查資料的時效性。

+++

+++ &#x200B;2. 檢查對象評估型別和排程

識別對象是使用批次還是串流評估，因為這決定了資料的時效性。

1. 在&#x200B;**對象詳細資料**&#x200B;頁面上，檢查&#x200B;**評估方法**：
   * **批次**：依排程每日評估一次。
   * **串流**：在發生設定檔更新時即時評估。
   * **Edge**：在邊緣位置即時評估。

根據評估方法，遵循適當的疑難排解步驟：

**如果對象使用批次評估：**

1. **瞭解批次對象限制：**
   * 批次對象每天評估一次（通常隔夜）。
   * 對象快照可能長達24小時之前。
   * 如果設定檔最近註冊了即時活動權杖，這些權杖可能不會在目前的快照中。
   * 在下次批次評估前不會反映設定檔的更新。

1. **檢查上次評估發生的時間：**
   * 在對象詳細資訊中，尋找&#x200B;**上次評估**&#x200B;時間戳記。
   * 如果設定檔的`liveActivityPushNotificationDetails`在此時間戳記之後更新，則對象具有過時資料。

1. **解析過時資料：**
   1. **選項1：等候排定的批次評估**
      * 下一個批次評估將包含更新的設定檔資料。
      * 此作業每天自動進行一次。
      * 最適合非緊急情況。

   1. **選項2：觸發隨選對象評估**
      1. 導覽至AEP中的&#x200B;**對象**。
      1. 選取您的客群。
      1. 按一下&#x200B;**立即評估**&#x200B;或&#x200B;**依需求啟用**。
      1. 等候評估完成（根據對象人數而定，這可能需要幾分鐘到幾小時的時間）。
      1. 確認設定檔現在已更新對象快照中的資料。
      1. 重試廣播API呼叫。

**如果對象使用串流評估：**

1. **瞭解串流對象行為：**
   * 當設定檔更新發生時，串流對象會即時評估。
   * **新設定檔**：如果設定檔符合區段條件，建立後即符合資格。
   * **已更新設定檔**：更新後不久即符合或取消資格。
   * **現有未變更的設定檔**：除非進行更新，否則不會重新評估。

1. **識別問題：**
   * 如果設定檔已存在並符合區段標準，但該設定檔未發生更新，則可能無法將其新增到新建立的串流受眾。
   * 設定檔必須接收更新（任何屬性變更），才能觸發重新評估。

1. **解決問題：**
   * **對於新設定檔**：如果符合條件，它們會自動符合條件。 不需要採取任何動作。
   * **對於沒有最近更新的現有設定檔：**
      * 對設定檔進行微幅更新（例如，更新時間戳記欄位）。
      * 這會觸發串流評估，並將設定檔新增至對象。
      * 替代方案：針對現有設定檔使用批次對象或邊緣對象。

+++

## 進階：透過資料集查詢進行偵錯 {#advanced-debugging-via-dataset-queries}

>[!BEGINSHADEBOX]

**對象**：開發人員和資料工程師。 需要透過Adobe Experience Platform查詢服務以SQL方式存取Journey Optimizer資料集。

**何時使用**： Assurance僅限於測試在使用中工作階段期間連線的裝置。 使用資料集查詢來調查生產作業一般使用者回報的問題，或在事後稽核傳遞歷史記錄。 資料集會顯示與Assurance外掛程式相同的生命週期和失敗資訊。

>[!ENDSHADEBOX]

### 找到資料集

1. 在Journey Optimizer中導覽至&#x200B;**資料管理** `>` **資料集**。

1. 啟用&#x200B;**顯示系統資料集**&#x200B;切換功能，並開啟&#x200B;**AJO訊息回饋事件資料集**。

請注意詳細資訊頁面上顯示的確切表格名稱。 下列查詢使用`ajo_message_feedback_event_dataset`，如果它不同，請以實際資料表名稱取代。

### 依已上線活動ID查詢

如果您知道即時活動ID （例如訂單UUID或出貨追蹤ID），並想要讓每個回饋事件在整個生命週期中與其連結，請使用此選項。

```sql
SELECT
  timestamp,
  identitymap,
  _experience.customerJourneyManagement
    .messageDeliveryfeedback.feedbackStatus AS status,
  _experience.customerJourneyManagement
    .messageDeliveryfeedback.messageFailure.reason AS failure_reason,
  _experience.customerJourneyManagement
    .pushChannelContext.liveActivity.event AS la_event,
  _experience.customerJourneyManagement
    .messageExecution.campaignID AS campaign_id,
  _experience.customerJourneyManagement
    .messageExecution.batchInstanceID AS batch_id,
  _id
FROM ajo_message_feedback_event_dataset
WHERE
  _experience.customerJourneyManagement
    .pushChannelContext.liveActivity.liveActivityID
    = '<YOUR_LIVE_ACTIVITY_ID>'
  AND eventtype = 'message.feedback'
ORDER BY timestamp ASC
```

### 依ECID查詢

當受影響設定檔的ECID已知時，請使用此選項。 以從設定檔擷取的ECID值取代`<YOUR_ECID>`。

```sql
SELECT
  timestamp,
  _experience.customerJourneyManagement
    .messageDeliveryfeedback.feedbackStatus AS status,
  _experience.customerJourneyManagement
    .messageDeliveryfeedback.messageFailure.reason AS failure_reason,
  _experience.customerJourneyManagement
    .pushChannelContext.liveActivity.event AS la_event,
  _experience.customerJourneyManagement
    .pushChannelContext.liveActivity.liveActivityID AS la_id,
  _experience.customerJourneyManagement
    .messageExecution.campaignID AS campaign_id,
  _id
FROM ajo_message_feedback_event_dataset
WHERE
  identityMap['ECID'][0].id = '<YOUR_ECID>'
  AND eventtype = 'message.feedback'
ORDER BY timestamp ASC
```

>[!NOTE]
>
> `identityMap`是結構化MAP型別，不是字串。 使用上述陣列和結構存取子語法。 `LIKE`之類的字串函式將傳回`DATATYPE_MISMATCH`錯誤。
>
></br>
&gt;訊息回饋事件資料集只會將ECID儲存在其「identityMap」中。 如果受影響的設定檔由自訂名稱空間而非ECID識別，請先解析ECID：導覽至AEP中的**設定檔**，使用自訂名稱空間和身分值搜尋設定檔，然後從設定檔的身分詳細資料擷取ECID。 在上述查詢中使用該ECID值。

### feedbackStatus值

| 值 | 含義 |
|-------|---------|
| `sent` | 已移交給APN — 不確認裝置轉譯（請參閱下面的附註） |
| `error` | 傳遞錯誤 — 檢查`failure_reason`以取得詳細資料 |
| `exclude` | 傳送前已排除設定檔（遺失權杖、同意問題或型別規則） |
| `delay` | 傳遞已延遲；將重試 |

>[!NOTE]
>
> 對於`la_event`欄位，資料集記錄的是初始傳遞事件的`remotestart`，而不是`start`。 依事件型別進行查詢時，請適當的篩選。

### 解譯已傳送狀態

`sent`的`feedbackStatus`確認Journey Optimizer已成功將通知傳遞至APN。 它&#x200B;**不**&#x200B;會確認已在裝置上轉譯即時活動。

當通知離開APN時，iOS不提供回呼。 無法從資料集中觀察裝置端失敗，例如作業系統限制、APN與裝置之間的網路中斷，或達到8小時的即時活動持續時間限制。 如果`feedbackStatus`是`sent`，但裝置上未出現任何上線活動，則問題不屬於Journey Optimizer管道。 使用Assurance外掛程式或應用程式層級記錄來診斷裝置端行為。

