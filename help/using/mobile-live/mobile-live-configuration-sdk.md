---
solution: Journey Optimizer
product: journey optimizer
title: 設定即時活動頻道
description: 瞭解如何設定Adobe Experience Platform Mobile SDK整合
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 02ca7c8e-105a-4e77-9aad-2381904255d0
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# 與Adobe Experience Platform Mobile SDK的即時活動整合 {#mobile-live-config-sdk}


Adobe Experience Platform Mobile SDK為Apple的即時活動提供內建支援。 這可讓您的應用程式直接在鎖定畫面和動態島上顯示即時動態更新，而不需開啟應用程式。

1. [匯入必要的模組](#import)

   匯入下列模組： **[!DNL AEPMessaging]**、**[!DNL AEPMessagingLiveActivity]**、**[!DNL ActivityKit]**。

1. [定義屬性](#attributes)

   符合`LiveActivityAttributes`，包含`LiveActivityData`和`ContentState`屬性。

1. [註冊即時活動](#register)

   在SDK初始化之後使用`Messaging.registerLiveActivity()`。

1. [建立Widget設定](#widget)

   針對鎖定畫面和動態島介面實作`ActivityConfiguration`。

1. [在本機開始上線活動（可選）](#local)

   您可以透過Journey Optimizer從遠端或在應用程式程式碼內的本機方式起始上線活動。

1. [新增偵錯支援（選擇性）](#debug)

   實作Assurance的`LiveActivityAssuranceDebuggable`。

確認已安裝下列最低版本，以確保組態和相容性正確無誤。

>[!BEGINSHADEBOX]

**必要條件：**

* **iOS：**
   * **iOS16.1或更新版本**：基本上線活動功能
   * **iOS 17.2+**：推送至啟動支援
   * **iOS 18+**：廣播頻道支援
* **Xcode：** 14.0或更新版本
* **Swift：** 5.7或更新版本
* **相依性：** AEPCore、AEPMessaging、AEPMessagingLiveActivity、ActivityKit
* **AEP Mobile SDK版本**： iOS Messaging 5.11.0或更新版本

>[!ENDSHADEBOX]

## 步驟1：匯入必要的模組 {#import}

若要開始，您必須先匯入下列模組： **[!DNL AEPMessaging]**、**[!DNL AEPMessagingLiveActivity]**、**[!DNL ActivityKit]**。

```swift
import AEPMessaging
import AEPMessagingLiveActivity
import ActivityKit
```

## 步驟2：定義您的上線活動屬性 {#attributes}

建立符合`LiveActivityAttributes`通訊協定的結構。 這會定義您的即時活動的靜態資料和動態內容狀態。

主要元件包括：

* 包含Adobe Experience Platform特定資料的&#x200B;**`liveActivityData`** （必要）。
   * 個別使用者：使用`LiveActivityData(liveActivityID: "unique-id")`
   * 廣播：使用`LiveActivityData(channelID: "channel-id")`

* 靜態屬性、使用案例專屬的自訂屬性，例如`restaurantName`。

* **`ContentState`**&#x200B;定義可在上線活動生命週期期間更新的動態資料。 它必須符合`Codable`和`Hashable`。

* `LiveActivityOrigin`列舉會指定活動是在應用程式內本機起始，還是透過推播開始通知從遠端起始(iOS 17.2和更新版本支援)。 此值可讓SDK在資料收集期間區分本機啟動與遠端觸發的即時活動。

**範例**

```swift
@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityAttributes: LiveActivityAttributes {
    // Mandatory: AEP Integration Data
    var liveActivityData: LiveActivityData
    
    // Static Attributes: Custom properties that do not change
    var restaurantName: String
    
    // Dynamic Content State: Data that can be updated
    struct ContentState: Codable, Hashable {
        var orderStatus: String
    }
}
```

```swift
@available(iOS 16.1, *)
public struct LiveActivityData: Codable {
    /// Unique identifier for broadcast Live activity channels
    public let channelID: String?
     
    /// Unique identifier for individual Live activity
    public let liveActivityID: String?
     
    /// Indicates local vs remote creation
    public let origin: LiveActivityOrigin?
     
    // Initializers
    public init(channelID: String)        // For broadcast Live activity
    public init(liveActivityID: String)   // For individual Live activity
}
```

您也可以為應用程式註冊多個Live活動型別：

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(AirplaneTrackingAttributes.self)
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
    Messaging.registerLiveActivity(GameScoreLiveActivityAttributes.self)
}
```

## 步驟3：註冊即時活動 {#register}

在SDK初始化後，在您的`AppDelegate`中註冊您的Live活動型別，這可讓您：

* 啟用自動推播開始權杖集合(iOS 17.2+)
* 自動收集即時活動更新權杖
* 啟用生命週期管理和事件追蹤

**食品配送即時活動的範例：**

```swift
if #available(iOS 16.1, *) {
    Messaging.registerLiveActivity(FoodDeliveryLiveActivityAttributes.self)
}
```

## 步驟4：建立即時活動Widget {#widgets}

即時活動會透過Widget顯示，您需要建立Widget套件組合和設定：

**食品配送即時活動的範例：**

```swift
@main
struct FoodDeliveryWidgetBundle: WidgetBundle {
    var body: some Widget {
        FoodDeliveryLiveActivityWidget()
    }
}

@available(iOS 16.1, *)
struct FoodDeliveryLiveActivityWidget: Widget {
    var body: some WidgetConfiguration {
        ActivityConfiguration(for: FoodDeliveryLiveActivityAttributes.self) { context in
            // Lock Screen UI
            VStack {
                Text("Order from \(context.attributes.restaurantName)")
                Text("Status: \(context.state.orderStatus)") // possible status may include "Ordered", "Order accepted", "Preparing", "On the Way","Delivered"
            }
        } dynamicIsland: { context in
            // Dynamic Island UI
            DynamicIsland {
                // Expanded UI
            } compactLeading: {
                // Compact leading UI
            } compactTrailing: {
                // Compact trailing UI
            } minimal: {
                // Minimal UI
            }
        }
    }
}
```

## 步驟5：在本機啟動上線活動（選用） {#local}

雖然Journey Optimizer可從遠端啟動即時活動，但您也可以從本機啟動：

**食品配送即時活動的範例：**

```swift
let attributes = FoodDeliveryLiveActivityAttributes(
    liveActivityData: LiveActivityData(liveActivityID: "order123"),
    restaurantName: "Pizza Palace"
)

let contentState = FoodDeliveryLiveActivityAttributes.ContentState(
    orderStatus: "Ordered"
)

let activity = try Activity<FoodDeliveryLiveActivityAttributes>.request(
    attributes: attributes,
    contentState: contentState,
    pushType: .token
)
```

## 步驟6：新增偵錯支援（選用） {#debug}

如有需要，您可以在Adobe Assurance中偵錯即時活動結構描述：

**食品配送即時活動的範例：**

```swift
@available(iOS 16.1, *)
extension FoodDeliveryLiveActivityAttributes: LiveActivityAssuranceDebuggable {
    static func getDebugInfo() -> (attributes: FoodDeliveryLiveActivityAttributes, state: ContentState) {
        return (
            FoodDeliveryLiveActivityAttributes(
                liveActivityData: LiveActivityData(liveActivityID: "debug-order-123"),
                restaurantName: "Debug Restaurant"
            ),
            ContentState(orderStatus: "Ordered")
        )
    }
}
```
