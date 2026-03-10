---
solution: Journey Optimizer
product: journey optimizer
title: 疑難排解即時活動
description: 瞭解如何針對單一和廣播使用案例（包括設定檔權杖問題、行銷活動設定和傳送失敗）疑難排解Journey Optimizer中的即時活動
role: User
level: Intermediate
source-git-commit: b71dbb0e4987cfc879a7b153d5c1453d6c220bf9
workflow-type: tm+mt
source-wordcount: '4503'
ht-degree: 1%

---


# 疑難排解即時活動 {#troubleshoot-mobile-live}

Adobe Journey Optimizer中的已上線活動可在iOS鎖定畫面和動態島嶼上啟用即時、動態更新。 它們只能透過API觸發的行銷活動來觸發和管理。

**使用案例型別：**

* **單一**：個別鎖定目標、異動（API觸發的異動行銷活動）
* **廣播**：以對象為目標、大量傳送（API觸發的行銷活動）

「已上線活動」的常見挑戰是當API呼叫觸發或更新已上線活動傳回&#x200B;**成功回應(200 OK)**，但已上線活動無法在使用者裝置上顯示或更新時。 API確認與實際裝置行為之間的這種中斷可能會發生在傳送管道中的多個點。 本指南提供系統的疑難排解方法，可識別傳送失敗的位置，透過裝置轉譯檢查API請求驗證的每個階段。

## 先決條件

進行疑難排解之前，請確定您已：

* 
  +++ 設定Assurance工作階段

  設定&#x200B;**Assurance工作階段**&#x200B;以擷取SDK事件並檢查傳遞管道。 Assurance可讓您檢視以下內容：

   * Edge Network請求和回應
   * 設定檔資格事件
   * 推播權杖註冊
   * 已上線的活動生命週期事件

  在[Assurance檔案](https://experienceleague.adobe.com/zh-hant/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance)中瞭解如何設定Adobe Experience Platform Assurance。

  **注意**：對於iOS Live Activity，請確認您的應用程式正在實體iOS裝置(iOS 16.1或更新版本)或Xcode模擬器(iOS 16.1或更新版本)上執行。

  +++

* 
  +++ 收集API觸發的行銷活動詳細資料

  在Journey Optimizer中導覽至您的API觸發的行銷活動，並擷取：

   * 行銷活動名稱
   * 在URL或促銷活動屬性中找到的促銷活動ID
   * 行銷活動版本（如適用）
   * 用於即時活動的表面設定、iOS應用程式表面

  +++

* 
  +++ 收集API請求資訊

  發出API呼叫以觸發即時活動時，請儲存：

   * API要求裝載，包括設定檔識別碼和即時活動資料
   * API回應，包括狀態代碼、訊息ID、請求ID
   * 呼叫API的時間戳記
   * 使用的端點，例如`/campaign/{CAMPAIGN_ID}/execute`

  +++

* 
  +++ 識別測試設定檔

  從您的API請求中擷取：

   * 設定檔名稱空間，例如ECID、電子郵件、客戶ID
   * API呼叫中使用的設定檔ID

  確定您可以在Adobe Experience Platform中查詢此設定檔。 在Experience Platform檔案[中瞭解如何](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide.html)查詢設定檔。

  +++

* 
  +++ 裝置和應用程式資訊

  從測試裝置收集下列專案：

   * 裝置型號，例如iPhone 14 Pro
   * iOS版本
   * 應用程式套件組合識別碼
   * APNs推播權杖
   * 測試時的網路連線狀態

  +++

## 常見案例

### 設定檔或推播權杖問題 {#profile-issue}

[!BADGE 適用於單一和廣播使用案例]{type=Positive}

API傳回HTTP 200，但未出現已上線的活動。 常見原因：

* 設定檔不存在於Adobe Experience Platform中。
* 即時活動推播權杖尚未同步至設定檔。
* 已同步即時活動推播詳細資料，但包含不正確的設定，例如，錯誤的`appId`或`attributeType`。

**廣播使用案例的注意事項**：如果對象中的某些設定檔遺失權杖，則只有這些設定檔將無法接收即時活動。 從您的對象中取樣數個設定檔，以診斷Token問題。 這僅適用於遠端開始事件，不適用於更新或結束事件。

#### 預先檢查

* iOS應用程式需求：
   * iOS 16.1+
   * 在`NSSupportsLiveActivities`中將`YES`設定為`Info.plist`
   * `ActivityAttributes`已正確實作。
* 行動SDK整合：
   * Adobe Experience Platform Mobile SDK (傳訊SDK 5.11.0+)
   * 使用「即時活動」推播權杖實作及呼叫`Messaging.registerLiveActivities`。

#### 偵錯步驟

1. 
   +++ 驗證Adobe Experience Platform中存在設定檔

   1. 在Journey Optimizer中，導覽至&#x200B;**客戶** `>` **設定檔**。
   1. 使用API請求的名稱空間和身分值來搜尋。
   1. 如果找不到設定檔，表示設定檔不存在或內嵌未完成。 在觸發上線活動之前，請建立設定檔或等待擷取。
   1. 如果找到設定檔，請繼續執行下方的步驟2以檢查推送代號是否已同步。

      +++

1. 
   +++ 檢查即時活動推播權杖是否已同步

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

1. 
   +++ 驗證設定檔上的Token詳細資料

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

### Campaign設定和裝載問題 {#payload-issues}

[!BADGE 適用於單一和廣播使用案例]{type=Positive}

具有有效權杖的設定檔已存在，但未顯示已上線活動。 這可能是由於：

* 介面或通道設定錯誤。
* API裝載結構不正確。
* `content-state`和`attributes`不符合iOS `ActivityAttributes`實作。
* 過時`timestamp` （更新/結束的關鍵）。

**廣播使用案例的注意事項**：行銷活動必須是&#x200B;**API觸發的行銷** （非異動）。 承載使用`audience`，而非個別`profile`。 請參閱[此章節](#broadcast-config)以取得廣播特定的裝載結構，並參閱[Adobe Developer檔案](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMAudienceMessageExecution)以取得完整的API規格。

#### 預先檢查

* 行銷活動為&#x200B;**API觸發的交易式** （單一）或&#x200B;**API觸發的行銷** （廣播），且&#x200B;**高輸送量**&#x200B;選項必須為&#x200B;**未啟用**，因為它與即時活動不相容。
* 使用上述[案例](#profile-issue)，確定設定檔存在且權杖已正確同步。

#### 偵錯步驟

1. 
   +++ 驗證行銷活動表面設定

   1. 在Journey Optimizer中，開啟您的&#x200B;**行銷活動**&#x200B;並導覽至&#x200B;**動作**&#x200B;功能表。
   1. 檢查您的&#x200B;**上線活動設定**。 您必須使用符合設定檔`appId`中`liveActivityPushNotificationDetails`的套件組合識別碼，為iOS應用程式設定表面。 例如，如果您的設定檔有`"appId": "com.example.myapp"`，則表面必須針對相同的應用程式。
   1. 檢查促銷活動組態中的&#x200B;**活動型別**&#x200B;是否與設定檔`attributeType`中的`liveActivityPushNotificationDetails`完全相符。 例如，如果您的設定檔有`"attributeType": "FoodDeliveryLiveActivityAttributes"`，則行銷活動必須指定此相同的活動型別。

      +++

1. 
   +++驗證API裝載結構

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
   * 指定何時應自動從裝置移除已上線活動。
   * 如果未在最終事件中提供，則即時活動會維持可見，直到使用者將其解除為止。
   * 必須為未來的時間戳記（晚於`timestamp`）。

     +++

1. 
   +++ 將裝載與iOS實作對齊

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

   * 在`ContentState`中包含所有`content-state`欄位（所有事件型別都需要）。
   * 在`LiveActivityAttributes`中包含所有`attributes`欄位（僅限開始事件），包括：
      * `liveActivityData` （必要；通常包含`liveActivityID`或類似的識別碼）
      * 結構中的所有自訂欄位
   * 完全符合欄位名稱（區分大小寫）。
   * 符合資料型別（String、Int、Bool、巢狀物件）。
   * 保留巢狀物件結構。

   **常見錯誤：**

   | 問題 | 影響 | 修正 |
   |-------|--------|-----|
   | 屬性中遺失`liveActivityData` | 已上線活動將不會開始 | 一律在開始事件中包含`liveActivityData`物件 |
   | 啟動事件中缺少必填欄位 | 已上線活動將不會開始 | 從iOS結構新增所有欄位 |
   | 欄位名稱錯誤（拼寫錯誤/大小寫） | 欄位被忽略或剖析錯誤 | 完全符合iOS欄位名稱 |
   | 錯誤的資料型別 | 剖析錯誤 | 符合iOS資料型別 |
   | 遺失巢狀物件 | 不完整的資料 | 包含所有巢狀結構 |
   | 在更新/結束中包括`attributes` | 不必要，但通常會忽略 | 在開始事件中僅包含`attributes` |
   | 更新/結束時的過時時間戳記 | 裝置忽略更新/結束 | 一律產生新的時間戳記 |

   如需更多範例，請參閱[建立即時活動頁面](create-mobile-live.md)。

   +++

1. 
   +++ 使用Assurance進行測試

   使用Assurance驗證API執行和裝載傳送：

   1. 開啟您的Assurance工作階段。
   1. 執行API呼叫以觸發上線活動。
   1. 在&#x200B;**事件清單**&#x200B;中，檢查：
      * 行銷活動執行事件。
      * 已上線的活動傳送事件。
      * 裝載驗證錯誤事件。
   1. 檢閱事件裝載以驗證：
      * 已正確處理承載。
      * 沒有發生驗證錯誤。
      * 已傳送已上線活動給APN。

      +++

### 傳遞失敗和錯誤分析

[!BADGE 適用於單一和廣播使用案例]{type=Positive}

在此案例中，所有先前的檢查均已通過：

* 具有[有效即時活動推播權杖的設定檔存在](#profile-issue)
* 行銷活動[已正確設定適當的承載](#payload-issues)
* [更新Token已同步](#token-not-synced) （僅適用於更新/結束事件、單一使用案例）

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

1. 
   +++ 檢查行銷活動報告

   1. 導覽至您的&#x200B;**即時活動行銷活動**。
   1. 按一下&#x200B;**報表**&#x200B;按鈕。
   1. 選取&#x200B;**檢視所有時間報表**。
   1. 檢閱下列章節：

      1. 檢查&#x200B;**傳送統計資料**&#x200B;量度以瞭解傳送成功：

         | 量度 | 其含義 | 要尋找的內容 |
         |-|-|-|
         | 已鎖定 | 符合對象資格的設定檔數 | 應該包含您的測試設定檔 |
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

1. 
   +++ 檢查設定檔中的訊息回饋事件

   1. 導覽至Journey Optimizer中的&#x200B;**客戶** > **設定檔**。
   1. 搜尋並開啟設定檔。
   1. 選取&#x200B;**事件**&#x200B;標籤。
   1. 篩選或搜尋具有`eventType = "message.feedback"`的事件。
   1. 尋找與您上線活動的`liveActivityID`和`event`型別相符的意見反應事件。
   1. 檢閱下列重要欄位：

      | 欄位 | 可能的值 | 其含義 |
      |-|-|-|
      | `feedbackStatus` | `sent`、`error`、`denylist` | 來自服務提供者的傳遞結果 |
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

1. 
   +++ 驗證Assurance中傳送至APN的已上線活動

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

1. 
   +++ 繼續其他診斷檢查

   1. 檢查行銷活動報告中的即時活動生命週期量度。

      在行銷活動報告中，檢閱&#x200B;**即時活動生命週期**&#x200B;區段：

      | 量度 | 檢查內容 |
      |-|-|
      | 遠端啟動 | 應該顯示API觸發的開始計數 |
      | 更新 | 應該顯示更新事件的計數 |
      | 結束 | 應該顯示結束事件的計數 |
      | 總計計數 | 整體已上線活動事件數量 |

      如果這些量度為零或不符合您的API呼叫，則Adobe與APN之間會發生傳送問題。

   1. 如果Adobe顯示傳送成功，但裝置未顯示已上線的活動：

      * 檢查iOS裝置記錄檔中的即時活動錯誤。
      * 驗證應用程式在前景或背景（未終止）。
      * 確認裝置具有網路連線。
      * 在多個裝置上測試以排除裝置特定問題。
      * 確認iOS版本為16.1或更新版本。

      +++

1. 
   +++ 提升至Adobe支援

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

### 即時活動更新權杖未同步{#token-not-synced}

裝置上的即時活動已成功啟動，但後續`update`或`end` API呼叫（傳回HTTP 200）無法更新或解除即時活動。 當&#x200B;**即時活動更新Token**&#x200B;未正確同步至Adobe的系統時，就會發生這種情況。

**瞭解更新Token**

當上線活動在裝置上開始時，iOS會為該特定上線活動執行個體產生唯一的更新權杖。 下列專案需要此代號：

* 傳送更新至已上線活動
* 從遠端結束即時活動

每個即時活動執行個體都有自己的唯一更新權杖。 Adobe需要此Token才能傳遞更新和結束事件。

**預期行為**

若要讓更新與結束事件運作，必須發生下列情況：

1. 裝置上的即時活動已成功啟動。
1. 裝置會為該即時活動執行個體產生更新權杖。
1. 行動SDK會擷取更新Token並將其傳送至Adobe。
1. 更新Token會同步並儲存在Adobe的系統中。
1. 針對更新/結束的後續API呼叫會使用此權杖進行傳送。

**預先檢查：**

* **使用者許可權**：當即時活動第一次在裝置上啟動時，iOS會顯示系統提示：「允許[應用程式名稱]提供即時活動更新？」 使用者&#x200B;**必須點選[允許]**&#x200B;才能產生並同步更新權杖。 如果使用者點選「不允許」，則不會建立任何更新Token，且更新/結束請求將失敗。 這是每個應用程式的一次性許可權。
* **設定檔和促銷活動驗證**：完成[案例1](#profile-issue)和[案例2](#payload-issues)檢查，以確保設定檔、代號和促銷活動設定正確無誤。

#### 偵錯步驟

1. 
   +++ 驗證Assurance中的更新權杖同步

   1. 開啟您的Assurance工作階段。
   1. 確定工作階段在裝置上啟動即時活動時處於作用中狀態。
   1. 篩選或搜尋具有`eventType = "liveActivity.updateToken"`的事件。
   1. 選取事件並檢查裝載：

      * 請確認`token`欄位包含有效的更新Token字串。
      * 檢查`liveActivityID`是否與您的已上線活動執行個體相符。
      * 確認`activityType`符合您的`attributes-type`。

   1. 如果找不到事件：

      * SDK未產生或擷取更新Token。
      * 檢查使用者是否已授與即時活動許可權。
      * 確認已在裝置上成功啟動已上線活動。
      * 確認行動SDK已正確整合以擷取更新Token。

   1. 如果找到事件，請繼續進行步驟2。

      +++

2. 
   +++ 驗證設定檔事件中的更新權杖

   1. 導覽至Journey Optimizer中的&#x200B;**客戶** > **設定檔**。
   1. 搜尋並開啟設定檔。
   1. 選取&#x200B;**事件**&#x200B;標籤。
   1. 尋找`liveActivity.updateToken`個事件。
   1. 檢查事件詳細資料：

      * 驗證時間戳記是否為最近（符合即時活動開始的時間）。
      * 確認`token`和`liveActivityID`是否存在。
      * 請確定`activityType`正確。

   1. 如果在設定檔中找不到事件：

      * 更新Token事件可能尚未內嵌至設定檔。
      * 等待5到10分鐘，然後重新檢查。
      * 如果15分鐘後仍然遺失，則可能是事件擷取問題。

   1. 如果找到事件，則表示更新Token已同步。 您可以繼續進行步驟3。

      +++

3. 
   +++ 檢查Assurance中的已上線活動傳送事件

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

## 廣播特定案例

### 廣播行銷活動設定和裝載問題{#broadcast-config}

本節說明廣播即時活動專屬的疑難排解案例，這些案例需要與單一行銷活動不同的偵錯方法。

當設定檔具有有效的權杖，但即時活動未出現、更新或行為與受眾成員的預期相符時，問題通常源於以下問題之一：

* 行銷活動未設定為API觸發的行銷。
* API承載使用不正確的廣播結構（遺失`audience`或`input-push-channel`）。
* `content-state`和`attributes`欄位不符合iOS `ActivityAttributes`實作。
* 未在Apple開發人員入口網站上正確建立`input-push-channel`。

此疑難排解案例適用於廣播行銷活動中的所有即時活動事件： `start`、`update`和`end`。

**預先檢查：**

* **促銷活動型別**：
   * 確認行銷活動建立為API觸發的行銷活動（廣播/對象型行銷活動的必要專案）。
   * 確認對象已定義於行銷活動設定中。
* **設定檔和權杖驗證**：從對象中取樣多個設定檔，以驗證它們是否具有有效的`liveActivityPushNotificationDetails`。 如需詳細的驗證步驟，請遵循[案例1](#profile-issue)。

#### 偵錯步驟

1. 
   +++ 驗證Campaign對象設定

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

1. 
   +++ 驗證廣播API裝載結構

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
   | `input-push-channel` | 廣播必填 — 此廣播執行個體的唯一識別碼 | 遺失或不符合`channelID`中的`liveActivityData` |
   | `timestamp` | 必須永遠為目前/最新的Unix紀元時間（以秒為單位） | 使用舊的/快取的時間戳記 |
   | `event` | 必須為`"start"`、`"update"`或`"end"` | 無效的事件型別 |
   | `attributes-type` | 必須符合行銷活動活動型別 | 不符或拼寫錯誤 |
   | `content-available` | 必須為`1` | 值遺失或錯誤 |

   **重要廣播特定欄位：**

   * **`input-push-channel`**：
      * 所有廣播直播活動皆需要。
      * 作為此特定廣播執行個體的唯一識別碼。
      * 對象中的所有設定檔都會收到連結至此管道的已上線活動。
      * 必須符合`channelID`中的`liveActivityData.channelID` （請參閱步驟3）。
      * 使用者端必須在Apple開發人員入口網站上為`appID`建立。
      * 只有為特定`appID`建立的頻道才能用來廣播該應用程式上的即時活動。

   * **`audience.id`**：
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

1. 
   +++ 讓內容狀態、屬性和輸入推播通道與iOS實作一致

   確認承載欄位符合您的iOS應用程式的`ActivityAttributes`實作，且`input-push-channel`符合`channelID`中的`liveActivityData`。

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

   * `input-push-channel`根目錄中的`aps`值必須與`channelID`中的`liveActivityData`完全相符。
   * 在上述範例中，兩個值均為`"FEt0NgvLEfEAAOqA6AXdIQ=="`。
   * 此比對會將廣播例項連結至即時活動資料。
   * 不相符會導致傳遞失敗。

   **關鍵驗證點：**

   * 包含所有事件型別`ContentState`中的所有`content-state`欄位。
   * 僅針對開始事件在`LiveActivityAttributes`中包含所有自訂`attributes`欄位。
   * 對於開始事件，`liveActivityData.channelID`必須符合`input-push-channel`。
   * 欄位名稱會區分大小寫，且必須完全相符。
   * 資料型別必須相符（字串、Int、Bool、巢狀物件等）。
   * 對於更新/結束事件，請使用與原始開始事件相同的`input-push-channel`。

   **常見錯誤：**

   | 問題 | 影響 | 修正 |
   |-|-|-|
   | 遺失`input-push-channel` | 廣播無法運作 | 為每個廣播新增唯一的頻道ID |
   | `input-push-channel`不符合`channelID` | 已上線活動將不會開始 | 確定兩個值相同 |
   | 更新/結束的不同`input-push-channel` | 更新/結束將不會到達已上線活動 | 在整個生命週期中使用相同的管道ID |
   | 遺失`liveActivityData.channelID` | 即時活動將不會連結到廣播 | 在開始事件的屬性中包含`channelID` |
   | 啟動事件中缺少必填欄位 | 已上線活動將不會開始 | 從iOS結構新增所有欄位 |
   | 欄位名稱錯誤（拼寫錯誤/大小寫） | 欄位被忽略或剖析錯誤 | 完全符合iOS欄位名稱 |
   | 更新/結束時的過時時間戳記 | 裝置忽略更新/結束 | 一律產生新的時間戳記 |

   +++

1. 
   +++ 使用Assurance進行測試

   使用Assurance驗證API執行和裝載傳送：

   1. 在屬於閱聽眾的測試裝置上開啟Assurance工作階段。
   1. 執行廣播API呼叫。
   1. 在&#x200B;**事件清單**&#x200B;中尋找：
      * 行銷活動執行事件。
      * 已上線的活動傳送事件。
      * 指示裝載驗證失敗的錯誤事件。
   1. 檢查事件裝載以確認：
      * 已正確處理承載。
      * `input-push-channel`已存在。
      * 沒有發生驗證錯誤。
      * 已將上線活動傳送至對象成員的APN。

      +++

### 設定檔不在對象或過時的對象快照中

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

1. 
   +++ 驗證設定檔位於對象中

   首先，確認應接收已上線活動的設定檔是否實際屬於對象。

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

2. 
   +++ 檢查對象評估型別和排程

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
