---
title: 開發人員快速入門
description: 作為資料工程師，深入瞭解如何使用 Journey Optimizer
feature: Get Started
role: Developer
level: Intermediate
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
TQID: https://experienceleague.adobe.com/7fRI-CPkIeBAPjtXmDgFdyNKgB4WwEc01yKrGUXnc3U
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: cf815079d67f4a41c3647c6a6e381ef5f1c44e51
workflow-type: tm+mt
source-wordcount: 3490
ht-degree: 53%

---

# 開發人員快速入門 {#get-started-developers}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;實作SDK、事件串流、自訂動作端點以及連線應用程式至Adobe Journey Optimizer的API，讓您的歷程可以在即時資料上執行。

>[!ENDSHADEBOX]

身為&#x200B;**開發人員**，您負責實作 [!DNL Adobe Journey Optimizer] 並將其整合至您的應用程式與系統。 一旦[系統管理員](administrator.md)及[資料工程師](data-engineer.md)授予您存取權限並準備好您的環境，您就可以開始使用 [!DNL Adobe Journey Optimizer]。

>[!NOTE]
>
>**實作順序：** [管理員](administrator.md) → [資料工程師](data-engineer.md) →您在這裡： **開發人員** → [行銷人員](marketer.md)
>
>在實作您的行動裝置和網頁整合之前，請確定已設定[資料結構描述和事件](data-engineer.md)。

## 您在 Journey Optimizer 生態系統中的角色

其他團隊成員透過使用者介面設定 Journey Optimizer 時，您將專注於：

* 在行動應用程式和網頁應用程式中&#x200B;**實作 SDK**
* 從您的應用程式&#x200B;**傳送事件**&#x200B;以觸發歷程
* **建立 API 端點**，Journey Optimizer 可透過自訂動作呼叫此端點
* **整合** Journey Optimizer 與您現有的系統和基礎結構
* **測試和偵錯**&#x200B;您的實作

您的[資料工程師](data-engineer.md)將處理資料結構描述、事件設定和資料來源。 您的[管理員](administrator.md)將設定權限和管道設定。 [行銷人員](marketer.md)將設計使用您實作的歷程和內容。

本指南涵蓋基本技術實作步驟，以協助您快速入門 Journey Optimizer。 無論您是建立行動應用程式、網頁體驗還是 API 整合，請遵循以下區段來設定您的實作。

## 先決條件 {#prerequisites}

在開始實作之前，請確定您擁有：

| 類別 | 需求 |
|----------|-------------|
| **技術技能** | * 使用 JavaScript (適用於 Web SDK) 或 Swift/Kotlin (適用於 Mobile SDK) 的經驗<br>* 了解 RESTful API 和 JSON<br>* 熟悉非同步程式設計和事件導向架構<br>* 了解貴組織的應用程式架構 |
| **存取權與工具** | * [Adobe Developer Console](https://developer.adobe.com){target="_blank"} 的存取權，以取得 API 認證<br>* 開發環境，以及應用程式程式碼庫的存取權<br>* 測試工具，例如 Postman 以進行 API 測試<br>* 瀏覽器開發人員工具或行動偵錯工具 |
| **來自其他團隊成員** | *您的[管理員](administrator.md)<br>授予的環境存取權* 來自[資料工程師](data-engineer.md)<br>的 XDM 結構描述和事件定義* 來自[行銷人員](marketer.md)的需求和使用案例 |

## 了解技術基礎 {#technical-foundation}

開始實作前，請先熟悉核心技術概念：

1. **Adobe Experience Platform 整合**：Journey Optimizer 原生建立在 Adobe Experience Platform 上。 了解基礎架構將幫助您建立更有效的實作。 深入了解 [Journey Optimizer 的運作方式](../understanding-ajo.md)。

1. **XDM 資料模型**：Journey Optimizer 使用體驗資料模型 (XDM) 來建構事件和輪廓資料。 身為開發人員，您必須了解如何傳送符合[資料工程師](data-engineer.md)所設定之結構描述的資料。 了解 [XDM 結構描述](../../data/get-started-schemas.md)。

1. **驗證和安全性**：所有實作都需要正確的驗證。 了解如何設定 SDK 和 API 的驗證。 了解 [API 驗證](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}。

## 設定行動應用程式整合 {#mobile-integration}

### 設定 Adobe Experience Platform Mobile SDK

行動SDK是您直接內嵌在iOS或Android應用程式中的程式庫集合。 它可作為應用程式與Adobe Experience Platform之間的通訊層：可識別使用者、收集行為事件，並從Journey Optimizer提供指示，包括推播通知、應用程式內訊息和個人化內容。 若沒有它，Journey Optimizer就無法得知您的應用程式使用者在做什麼，也無法聯絡上他們。

1. **安裝及設定 Mobile SDK**：請依照 [Adobe Experience Platform Mobile SDK 文件](https://developer.adobe.com/client-sdks/documentation/getting-started){target="_blank"}操作，開始進行 SDK 整合。

1. **建立行動屬性**：在 [!DNL Adobe Experience Platform Data Collection] 中設定行動屬性。 了解如何[建立和設定行動屬性](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property){target="_blank"}。

1. **設定推播通知**：
   * 針對 **iOS 應用程式**：向 APN (Apple 推播通知服務) 註冊您的應用程式。 若要了解更多資訊，請參閱 [Apple 文件](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}。
   * 針對 **Android 應用程式**：為您的 Android 應用程式設定 Firebase 雲端訊息。 若要了解更多資訊，請參閱 [Google 文件](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}。

1. **測試您的行動整合**：使用[行動快速入門工作流程](../../push/mobile-onboarding-wf.md)來快速設定並測試您的行動設定。

設定推播通知的詳細步驟可在[此頁面](../../push/push-configuration.md)上取得。

### 實作程式碼型體驗 (Mobile SDK)

程式碼型體驗可讓您向原生行動應用程式中的任何表面提供個人化內容（從入門畫面和產品詳細資料頁面，到應用程式內橫幅和功能標幟），而不需要新的應用程式版本。 使用Mobile SDK在執行階段擷取及呈現個人化內容，讓您的團隊可完全掌控版位和簡報：

* 請依照[本教學課程](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial){target="_blank"}中的指示實作 Mobile SDK
* 檢閱 [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} 和 [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"} 的範例實作

## 實作網頁體驗 {#web-implementation}

### 設定 Adobe Experience Platform Web SDK

Web SDK (`alloy.js`)是單一JavaScript資料庫，可取代您網站可能需要的個別Adobe標籤的修補程式。 它會收集行為資料、透過您設定的資料流將其串流至Adobe Experience Platform，並接收回傳的個人化指示 — 所有這些都在一個網路往返中。 設定完成後，Journey Optimizer就可以識別訪客、從他們的動作觸發歷程，並立即將自訂內容提供給您的頁面。

1. **安裝 Web SDK**：請依照 [Web SDK 實作指南](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}操作，在您的網站上設定 SDK。

1. **設定資料流**：啟用 Journey Optimizer 後，在 [!DNL Adobe Experience Platform Data Collection] 中建立並設定資料串流。 在[資料流文件](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant){target="_blank"}中了解更多相關資訊。

1. **啟用網頁推播通知** (選用)：網頁推播通知現在一般可用。 在您的 Web SDK 設定中設定 [pushNotifications 屬性](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/collection/js/commands/configure/pushnotifications){target="_blank"}，並使用 [sendPushSubscription 命令](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/collection/js/commands/sendpushsubscription){target="_blank"}來註冊推播訂閱。 [瞭解網頁推播設定](../../push/push-configuration-web.md)。

### 實作程式碼型體驗 (Web SDK)

不同於行銷人員完全控制版面的視覺管道，程式碼型體驗可讓您完全掌控個人化內容在頁面上的呈現方式。 Journey Optimizer會傳回包含個人化資料的JSON裝載；您的程式碼會決定要在哪裡以及如何顯示。 此模型適用於任何網路介面（英雄橫幅、建議輪播、搜尋結果排名、A/B測試變體），而無需視覺化編輯器或頁面發佈工作流程。

1. **選擇您的實作方法**：用戶端、伺服器端或混合式。 檢閱每個方法的[實作範例](../../code-based/code-based-implementation-samples.md)。

1. **定義表面**：識別您要在應用程式中傳遞個人化內容的位置。 了解[表面設定](../../code-based/code-based-surface.md)。

1. **實作內容轉譯**：使用 Web SDK 擷取並套用個人化內容。 請參閱[程式碼型實作教學課程](../../code-based/code-based-decisioning-implementations.md)。

1. **傳送顯示和互動事件**：追蹤內容顯示的時間以及使用者與內容互動以進行分析和最佳化的時間。

探索 [GitHub 上的範例實作](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}，了解程式碼型體驗的實際運作情況。

深入了解[程式碼型體驗快速入門](../../code-based/get-started-code-based.md)。

## 實作事件串流 {#event-streaming}

### 傳送事件以觸發歷程

歷程在事件上執行 — 使用者登入、將專案新增至購物車、完成購買、放棄表單。 您的工作是在正確的時間從應用程式發出這些事件。 每個事件都是傳送至Experience Platform串流擷取API的XDM結構化JSON裝載；Journey Optimizer會在毫秒內擷取該事件，並將設定檔路由至任何相符歷程。 事件結構描述和裝載結構是由您的[資料工程師](data-engineer.md)所定義 — 在您開始編碼之前先與其協調。

1. **了解事件承載**：請與您的資料工程師合作，取得事件結構描述和必要的承載結構。 承載必須符合其所設定的 XDM 結構描述。 了解[事件結構描述需求](../../event/experience-event-schema.md)。

1. **實作事件串流**：使用[串流擷取 API](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target="_blank"} 將事件傳送至 Adobe Experience Platform。 了解[傳送事件的步驟](../../event/additional-steps-to-send-events-to-journey.md)。

1. **處理事件類型**：
   * **單一事件**：針對個人特定動作實作事件傳送 (例如，按鈕點按、購買完成)
   * **業務事件**：傳送業務相關事件 (例如，庫存更新、價格變更)

1. **測試事件傳送**：確認事件已正確接收，並如預期觸發歷程。 了解[事件疑難排解](../../building-journeys/troubleshooting-inbound.md)。

透過 API 傳送事件的&#x200B;**實作範例**：

```javascript
POST https://{DATACOLLECTION_ENDPOINT}/collection/{DATASTREAM_ID}
Content-Type: application/json

{
  "header": {
    "datasetId": "{DATASET_ID}",
    "imsOrgId": "{ORG_ID}",
    "source": {
      "name": "Web SDK"
    }
  },
  "body": {
    "xdmMeta": {
      "schemaRef": {
        "id": "{SCHEMA_ID}"
      }
    },
    "xdmEntity": {
      "_id": "unique-event-id",
      "eventType": "purchase",
      "timestamp": "2024-01-01T12:00:00Z",
      // ... your event data
    }
  }
}
```

深入了解如何[使用歷程事件](../../event/about-events.md)。

## 開發自訂動作端點 {#custom-actions}

當歷程達到自訂動作步驟時，Journey Optimizer會對您提供的URL （您的後端、CRM、忠誠度平台、任何REST端點）發出傳出HTTP呼叫。 您的工作是建置並公開該端點：定義請求合約（裝載形狀、驗證方法、回應格式）、實作其背後的商業邏輯，並確保其可處理Journey Optimizer將產生的呼叫量。 您的[管理員](administrator.md)接著會在Journey Optimizer中註冊端點，讓行銷人員可以將其用作其歷程中的步驟。

1. **建立您的 API 端點**：建立 Journey Optimizer 將在歷程執行期間呼叫的 RESTful API 端點。 您的端點應：
   * 接受 JSON 承載
   * 驗證請求 (OAuth、API 金鑰或 JWT)
   * 在適當的逾時限制內處理請求
   * 以預期格式傳回回應

1. **了解自訂動作功能**：自訂動作可以連線至第三方系統，例如 Epsilon、Slack、Firebase 或您自己的服務。 深入了解[自訂動作](../../action/action.md)。

1. **使用動作設定**：您的[管理員](administrator.md)或[資料工程師](data-engineer.md)將在 Journey Optimizer 中設定自訂動作，定義 API 端點 URL、驗證方法和參數。 您將為他們提供您的 API 規格。 了解[自訂動作設定](../../action/about-custom-action-configuration.md)。 您可以為逾時/錯誤分支中更豐富的邏輯定義選用的&#x200B;**錯誤回應承載**。

1. **傳回可操作資料**：設計您的 API 以傳回可用於後續歷程步驟的資料。 了解[動作回應](../../action/action-response.md)。

1. **監視自訂動作健康情況**：使用自訂動作監視儀表板來追蹤成功的呼叫、錯誤、輸送量、回應時間和佇列等待時間。 瞭解[自訂動作報告](../../action/reporting.md)。

1. **實作速率限制**：確保您的端點可以處理預期的流量。 Journey Optimizer 套用每秒 5000 次呼叫的限制，但您的系統應可復原。 了解[上限與節流](../../configuration/external-systems.md)。

**範例使用案例**：使用自訂動作[將歷程事件寫入 Experience Platform](../../building-journeys/custom-action-aep.md)。

## 使用 Journey Optimizer API {#apis}

並非所有事情都需要透過Journey Optimizer UI進行。 有時您需要從自己的後端觸發行銷活動、在隱私權請求後隱藏電子郵件地址，或從外部CMS同步內容範本。 Journey Optimizer的REST API可讓您以程式設計方式存取平台的核心功能。 所有呼叫都使用OAuth伺服器對伺服器驗證，舊版的JWT方法已過時。

1. **了解 API 功能**：Journey Optimizer API 可讓您以程式設計方式建立、讀取、更新和刪除各種資源。 深入了解 [Journey Optimizer API](../../configuration/ajo-apis.md)。

1. **驗證**：請依照[本教學課程](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}中的指示，使用 Adobe Developer Console 設定 API 驗證。

1. **探索 API 參考**：瀏覽完整的 API 文件，並直接在 [Adobe Journey Optimizer API 參考](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}中試用 API。

1. **API 觸發的行銷活動**：使用 API 觸發的行銷活動建立交易型訊息。 若是高流量案例 (最多5000 TPS)，請探索[高輸送量模式](../../campaigns/api-triggered-high-throughput.md) (需要附加授權)。

1. **決策管理 API**：使用專門的 API 進行產品建議管理和決策。 若要了解更多資訊，請參閱[決策管理 API 指南](../../offers/api-reference/getting-started.md)。

1. **決策移轉 API**：以程式設計方式將決策管理實體移轉至具有彈性範圍、自動化驗證和復原支援的決策。 若要瞭解更多資訊，請參閱[決策移轉 API 指南](../../experience-decisioning/decisioning-migration-api.md)。

1. **簡訊 Webhook**：設定傳入 Webhook 以擷取傳入訊息和意見回饋 Webhook，以便接收傳遞回條和狀態更新。 [了解更多](../../mobile/mobile-webhook.md)。

## 測試和偵錯 {#testing}

在實作上線之前，您需要確保事件在適當的時刻引發、歷程如預期般觸發、自訂動作在真實負載下運作，以及個人化內容正確呈現。 本節說明用於及早發現問題的工具和技術，從低階SDK記錄，到使用真實設定檔的端對端歷程測試執行。

1. **偵錯SDK實作**：使用Adobe Experience Platform Assurance檢查SDK事件、驗證資料收集，並在整合問題發生時進行疑難排解。 [深入了解 Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=zh-Hant){target="_blank"}。

1. **測試事件傳送**：確認 Adobe Experience Platform 已正確接收來自您應用程式的事件，並如預期觸發歷程。 監視事件擷取並驗證承載結構。

1. **驗證 API 整合**：測試您的自訂動作端點，以確保它們可正確處理 Journey Optimizer 請求、在逾時限制內回應，以及傳回預期的資料格式。

1. **搭配測試輪廓使用測試模式**：與您的[資料工程師](data-engineer.md)合作，存取測試輪廓，然後使用歷程測試模式驗證您的實作。 了解如何[測試歷程](../../building-journeys/testing-the-journey.md)。

1. **監視 SDK 記錄**：在您的 SDK 實作中啟用偵錯記錄，以疑難排解開發期間的問題：
   * **Mobile SDK**：啟用記錄以檢視 SDK 事件和 API 呼叫
   * **Web SDK**：使用瀏覽器控制台監視 SDK 活動

1. **驗證資料流設定**：確定您的資料流已正確設定為傳送資料至 Journey Optimizer。 檢查事件是否流經資料流到達正確的目的地。

1. **查詢歷程資料以進行分析**：使用資料湖上的 SQL 查詢來分析歷程步驟事件、偵錯問題，以及監視自訂動作績效。 探索[歷程分析的查詢範例](../../reports/query-examples.md)，包括：
   * 輪廓進入/退出追蹤與捨棄原因
   * 自訂動作績效量度 (延遲、輸送量、錯誤)
   * 事件傳送和錯誤模式
   * 歷程執行個體狀態

## 進階開發人員主題 {#advanced-topics}

一旦您的核心SDK、事件和API準備就緒，這些主題可協助您更進一步：在執行階段豐富歷程資料而不會膨脹設定檔、處理同意訊號以便選擇退出會傳播到每個整合，以及調整您的實作，以符合生產規模需求的輸送量和可靠性。

### 使用內容資料及擴充

歷程通常需要比觸發事件中提供的更多資料，例如產品名稱、忠誠度等級、訂單條列專案清單。 內容擴充功能可讓您的歷程在執行階段從AEP資料集查詢資料，或從自訂動作回應將其結轉，而非將所有這些預先載入每個設定檔。 然後，您的訊息和分支條件可以參考該資料，而不會將其永久儲存在設定檔上。

* **反覆處理陣列**：使用 Handlebars 語法在訊息中顯示來自事件、自訂動作回應和資料集查詢的動態清單。 了解如何[反覆處理內容資料](../../personalization/iterate-contextual-data.md)。
* **資料集查詢**：實作資料集查詢，以擴充 Adobe Experience Platform 資料集的歷程資料。 與您的資料工程師共同處理設定。 了解[資料集查詢](../../building-journeys/dataset-lookup.md)。

### 使用同意與治理

Journey Optimizer會在平台層級執行資料控管和同意原則，但您的整合也需要遵守這些原則。 當客戶選擇退出行銷通訊，或資料使用標籤限制欄位的使用方式時，這些規則需要在您的自訂動作和資料集查詢中傳播，而不僅僅是封鎖UI中的動作。

* **資料治理**：將資料使用原則套用至自訂動作。 深入了解[資料治理](../../action/action-privacy.md)。
* **同意管理**：在您的實作中處理客戶同意偏好設定。 了解[同意](../../action/consent.md)。

### 最佳化和最佳做法

生產Journey Optimizer實施會定期處理每秒數百萬個事件和數千個歷程執行。 這些資源可協助您針對該規模調整整合 — 在達到速率限制之前先瞭解限制、避免常見的歷程設計陷阱而無訊息地捨棄設定檔，以及建置可正常降低而不是不透明地失敗的錯誤處理。

* **上限與節流**：了解速率限制並實作適當的節流。 了解[外部系統](../../configuration/external-systems.md)。
* **歷程最佳化**：遵循[歷程最佳化](../../building-journeys/optimize.md)的最佳做法。
* **錯誤處理**：實作強大的錯誤處理。 檢閱[錯誤碼](../../building-journeys/error-codes-reference.md)和[疑難排解指南](../../building-journeys/troubleshooting.md)。

## 呼叫Journey Optimizer REST API {#rest-apis}

除了實作SDK和事件串流，您也可以以程式設計方式從您自己的系統中推動Journey Optimizer。 完整的API參考、OpenAPI規格和程式碼範例位於[Journey Optimizer開發人員入口網站](https://developer.adobe.com/journey-optimizer-apis){target="_blank"}。

>[!NOTE]
>
>所有整合都必須使用OAuth伺服器對伺服器驗證 — JWT方法已過時。 [設定驗證](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}

### 執行API觸發的行銷活動 {#api-triggered}

使用互動式訊息執行REST API，觸發來自外部系統的交易或行銷訊息。 呼叫端點之前：

* 在端點接受呼叫之前，行銷活動必須是&#x200B;**已啟動**。
* 呼叫的&#x200B;**逾時為60秒**；內部重試處理未預期的逾時。
* 如果設定了行銷活動的開始/結束日期，則這些日期以外的API呼叫將失敗。
* 若要建置您的裝載，請在Journey Optimizer UI中，從您即時行銷活動的&#x200B;**cURL請求**&#x200B;區段中擷取產生的範例cURL請求，此區段包含該行銷活動的所有個人化變數。
* 標準和[高輸送量行銷活動](../../campaigns/api-triggered-high-throughput.md)使用不同的端點。

[API參考](https://developer.adobe.com/journey-optimizer-apis/references/messaging){target="_blank"} · [程式碼範例](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples){target="_blank"} · [使用API觸發的行銷活動](../../campaigns/api-triggered-campaigns.md)

### 外部端點的上限和節流 {#capping-throttling}

當歷程透過自訂動作或資料來源呼叫外部系統時，上限和節流API可保護這些系統避免過載。 上限會拒絕超過設定限制的呼叫；節流會將它們排入最多6小時的佇列（僅限生產沙箱、自訂動作）。

[上限API參考](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling){target="_blank"} · [使用上限API](../../configuration/capping.md) · [使用節流API](../../configuration/throttling.md)

### 更多REST API {#more-rest-apis}

除了傳訊和上限，Journey Optimizer還會公開REST端點，用於隱藏管理、內容範本、行銷活動擷取、校訂和精心安排的行銷活動執行。 當您需要自動化操作時，請使用這些選項，否則UI中需要手動步驟，例如，拉取資料後大量隱藏位址，或從外部內容管道同步範本。

| 您需要做什麼 | API 參考 |
| ------------------- | ------------- |
| 以程式設計方式排除要傳送的電子郵件地址或網域 | [隱藏API](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"} · [管理隱藏清單](../../configuration/manage-suppression-list.md) |
| 擷取歷程中繼資料以進行稽核或外部同步 | [歷程API](https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve){target="_blank"} |
| 從外部管道建立和管理內容範本和片段 | [內容API](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} · [範本](../../content-management/content-templates.md) · [片段](../../content-management/fragments.md) |
| 擷取及篩選動作行銷活動 | [行銷活動API](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"} |
| 預覽行銷活動並以程式設計方式傳送校樣 | [模擬API](https://developer.adobe.com/journey-optimizer-apis/references/simulations){target="_blank"} |

>[!NOTE]
>
>模擬API可用於API觸發和動作（已排程）行銷活動。 **協調行銷活動不支援**：請改用協調行銷活動使用者介面中的預覽和校訂工作流程來進行。

|驗證資料集並觸發協調的行銷活動執行 | [資料集驗證](https://developer.adobe.com/journey-optimizer-apis/references/orchestrated-campaign-dataset){target="_blank"} · [觸發器](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} · [啟用資料集](../../orchestrated/manual-schema.md) |

## 其他資源 {#additional-resources}

* **Developer Console**：存取 [Adobe Developer Console](https://developer.adobe.com){target="_blank"} 以建立整合並管理 API 認證。
* **範例代碼**：探索 [GitHub 上的範例實作](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}。
* **教學課程影片**：透過 [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hant){target="_blank"} 的實作教學課程學習。
* **開發人員社群**：與其他開發人員交流，並在 Adobe 社群論壇中取得支援。

## 跨角色共同作業 {#next-steps}

您的實作工作與其他團隊成員的工作有交集：

>[!BEGINTABS]

>[!TAB 與資料工程師合作]

與[資料工程師](data-engineer.md)共同作業資料與事件設定。 每個對使用者行為回應的歷程都取決於您傳送的事件 — 資料工程師會定義結構，您實作產生結構的程式碼。

* 取得您需要實作的[XDM結構描述](../../data/get-started-schemas.md)和事件結構
* 瞭解您需要傳送哪些事件及其必要的裝載格式 — 請參閱[使用歷程事件](../../event/about-events.md)
* 確認每個事件裝載中的哪些欄位是必要欄位與選用欄位，以及當預期欄位遺失或格式錯誤時，在歷程中會發生什麼情況 — 請參閱[結構描述需求](../../event/experience-event-schema.md#schema-requirements)
* 使用[Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=zh-Hant){target="_blank"}一起測試事件傳遞和資料擷取

>[!TAB 與管理員合作]

與[管理員](administrator.md)共同作業存取和通道設定。 歷程只能透過管理員設定的管道觸及使用者 — 及早協調，讓您的SDK運作及其設定保持同步。

* 提供將在Journey Optimizer中設定的[自訂動作](../../action/about-custom-action-configuration.md)的API規格
* 透過[Adobe Developer Console](https://developer.adobe.com){target="_blank"}要求必要的許可權和API認證
* 協調通道組態需求 — [iOS](../../push/push-configuration.md)和Android的推播憑證、[網頁推播](../../push/push-configuration-web.md)設定、[SMS webhook](../../mobile/mobile-webhook.md)端點
* 在執行[歷程測試模式](../../building-journeys/testing-the-journey.md)之前，對齊沙箱策略和測試環境

>[!TAB 與行銷人員合作]

與[行銷人員](marketer.md)共同作業歷程設計與測試。 行銷人員建立的歷程和內容完全取決於您傳送的事件和您公開的表面 — 您對齊越近，歷程上線就越快。

* 一起檢閱[Journey Optimizer](../../building-journeys/journey.md)中的歷程設計，瞭解哪些使用者互動必須觸發事件，以及哪些表面需要個人化
* 實作追蹤，讓行銷人員可以測量[內容效能和使用者參與度](../../reports/report-gs-cja.md)
* 使用測試設定檔一起執行[歷程測試模式](../../building-journeys/testing-the-journey.md)，以端對端驗證完整流程
* 疑難排解訊息傳送、個人化轉譯，或[自訂動作](../../action/action.md)回應的問題

>[!ENDTABS]

## 開始實作

準備好開始建立了嗎？ 從以上區段選擇您的第一個實作區域：

1. **行動應用程式？** 開始進行 [Mobile SDK 整合](#mobile-integration)
2. **網站？** 開始[設定 Web SDK](#web-implementation)
3. **API 整合？** 跳轉至[使用 API](#apis)
4. **自訂系統？** 查看[自訂動作](#custom-actions)

每個區段都包含詳細技術文件、程式碼範例和教學課程的連結，以指導您的實作。

## 其他角色指南 {#other-role-guides}

| 角色 | 指南 |
|------|-------|
| 管理員 | [管理員開始使用](administrator.md) |
| 資料工程師 | [資料工程師快速入門](data-engineer.md) |
| Developer | [開發人員快速入門](developer.md) |
| 行銷人員 | [行銷人員快速入門](marketer.md) |

返回[角色和責任總覽](../quick-start.md) ·返回[開始](../../../rp_landing_pages/get-started-landing-page.md)
