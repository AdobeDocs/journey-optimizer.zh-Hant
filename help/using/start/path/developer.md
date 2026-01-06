---
title: '開發人員快速入門 '
description: 作為資料工程師，深入瞭解如何使用 Journey Optimizer
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: 2d699fe8a3320400dad2d5d962028d6e2a5425f8
workflow-type: ht
source-wordcount: '1816'
ht-degree: 100%

---

# 開發人員快速入門  {#get-started-developers}

身為&#x200B;**開發人員**，您負責實作 [!DNL Adobe Journey Optimizer] 並將其整合至您的應用程式與系統。一旦[系統管理員](administrator.md)及[資料工程師](data-engineer.md)授予您存取權限並準備好您的環境，您就可以開始使用 [!DNL Adobe Journey Optimizer]。

## 您在 Journey Optimizer 生態系統中的角色

其他團隊成員透過使用者介面設定 Journey Optimizer 時，您將專注於：

* 在行動應用程式和網頁應用程式中&#x200B;**實作 SDK**
* 從您的應用程式&#x200B;**傳送事件**&#x200B;以觸發歷程
* **建立 API 端點**，Journey Optimizer 可透過自訂動作呼叫此端點
* **整合** Journey Optimizer 與您現有的系統和基礎結構
* **測試和偵錯**&#x200B;您的實作

您的[資料工程師](data-engineer.md)將處理資料結構描述、事件設定和資料來源。您的[管理員](administrator.md)將設定權限和管道設定。[行銷人員](marketer.md)將設計使用您實作的歷程和內容。

本指南涵蓋基本技術實作步驟，以協助您快速入門 Journey Optimizer。無論您是建立行動應用程式、網頁體驗還是 API 整合，請遵循以下區段來設定您的實作。

## 先決條件 {#prerequisites}

在開始實作之前，請確定您擁有：

| 類別 | 需求 |
|----------|-------------|
| **技術技能** | * 使用 JavaScript (適用於 Web SDK) 或 Swift/Kotlin (適用於 Mobile SDK) 的經驗<br>* 了解 RESTful API 和 JSON<br>* 熟悉非同步程式設計和事件導向架構<br>* 了解貴組織的應用程式架構 |
| **存取權與工具** | * [Adobe Developer Console](https://developer.adobe.com){target="_blank"} 的存取權，以取得 API 認證<br>* 開發環境，以及應用程式程式碼庫的存取權<br>* 測試工具，例如 Postman 以進行 API 測試<br>* 瀏覽器開發人員工具或行動偵錯工具 |
| **來自其他團隊成員** | *您的[管理員](administrator.md)<br>授予的環境存取權* 來自[資料工程師](data-engineer.md)<br>的 XDM 結構描述和事件定義* 來自[行銷人員](marketer.md)的需求和使用案例 |

## 了解技術基礎 {#technical-foundation}

開始實作前，請先熟悉核心技術概念：

1. **Adobe Experience Platform 整合**：Journey Optimizer 原生建立在 Adobe Experience Platform 上。了解基礎架構將幫助您建立更有效的實作。深入了解 [Journey Optimizer 的運作方式](../understanding-ajo.md)。

1. **XDM 資料模型**：Journey Optimizer 使用體驗資料模型 (XDM) 來建構事件和輪廓資料。身為開發人員，您必須了解如何傳送符合[資料工程師](data-engineer.md)所設定之結構描述的資料。了解 [XDM 結構描述](../../data/get-started-schemas.md)。

1. **驗證和安全性**：所有實作都需要正確的驗證。了解如何設定 SDK 和 API 的驗證。了解 [API 驗證](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}。

## 設定行動應用程式整合 {#mobile-integration}

### 設定 Adobe Experience Platform Mobile SDK

若要啟用推播通知、應用程式內訊息和其他行動功能，請將 Adobe Experience Platform Mobile SDK 整合至您的行動應用程式。

1. **安裝及設定 Mobile SDK**：請依照 [Adobe Experience Platform Mobile SDK 文件](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"}操作，開始進行 SDK 整合。

1. **建立行動屬性**：在 [!DNL Adobe Experience Platform Data Collection] 中設定行動屬性。了解如何[建立和設定行動屬性](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}。

1. **設定推播通知**：
   * 針對 **iOS 應用程式**：向 APN (Apple 推播通知服務) 註冊您的應用程式。若要了解更多資訊，請參閱 [Apple 文件](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}。
   * 針對 **Android 應用程式**：為您的 Android 應用程式設定 Firebase 雲端訊息。若要了解更多資訊，請參閱 [Google 文件](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}。

1. **測試您的行動整合**：使用[行動快速入門工作流程](../../push/mobile-onboarding-wf.md)來快速設定並測試您的行動設定。

設定推播通知的詳細步驟可在[此頁面](../../push/push-configuration.md)上取得。

### 實作程式碼型體驗 (Mobile SDK)

針對使用程式碼體驗的原生行動應用程式個人化：

* 請依照[本教學課程](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}中的指示實作 Mobile SDK
* 檢閱 [iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} 和 [Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"} 的範例實作

## 實作網頁體驗 {#web-implementation}

### 設定 Adobe Experience Platform Web SDK

針對網頁型實作，Web SDK 是您的主要整合點：

1. **安裝 Web SDK**：請依照 [Web SDK 實作指南](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}操作，在您的網站上設定 SDK。

1. **設定資料流**：啟用 Journey Optimizer 後，在 [!DNL Adobe Experience Platform Data Collection] 中建立並設定資料串流。在[資料流文件](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant){target="_blank"}中了解更多相關資訊。

1. **啟用網頁推播通知** (選用)：在您的 Web SDK 設定中設定 [pushNotifications 屬性](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"}，並使用 [sendPushSubscription 命令](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"}來註冊推播訂閱。

### 實作程式碼型體驗 (Web SDK)

程式碼型體驗可讓您個人化任何數位接觸點：

1. **選擇您的實作方法**：用戶端、伺服器端或混合式。檢閱每個方法的[實作範例](../../code-based/code-based-implementation-samples.md)。

1. **定義表面**：識別您要在應用程式中傳遞個人化內容的位置。了解[表面設定](../../code-based/code-based-surface.md)。

1. **實作內容轉譯**：使用 Web SDK 擷取並套用個人化內容。請參閱[程式碼型實作教學課程](../../code-based/code-based-decisioning-implementations.md)。

1. **傳送顯示和互動事件**：追蹤內容顯示的時間以及使用者與內容互動以進行分析和最佳化的時間。

探索 [GitHub 上的範例實作](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}，了解程式碼型體驗的實際運作情況。

深入了解[程式碼型體驗快速入門](../../code-based/get-started-code-based.md)。

## 實作事件串流 {#event-streaming}

### 傳送事件以觸發歷程

身為開發人員，您將實作程式碼以傳送觸發歷程的事件。您的[資料工程師](data-engineer.md)將在 Journey Optimizer 中設定事件結構描述和定義。

1. **了解事件承載**：請與您的資料工程師合作，取得事件結構描述和必要的承載結構。承載必須符合其所設定的 XDM 結構描述。了解[事件結構描述需求](../../event/experience-event-schema.md)。

1. **實作事件串流**：使用[串流擷取 API](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target="_blank"} 將事件傳送至 Adobe Experience Platform。了解[傳送事件的步驟](../../event/additional-steps-to-send-events-to-journey.md)。

1. **處理事件類型**：
   * **單一事件**：針對個人特定動作實作事件傳送 (例如，按鈕點按、購買完成)
   * **業務事件**：傳送業務相關事件 (例如，庫存更新、價格變更)

1. **測試事件傳送**：確認事件已正確接收，並如預期觸發歷程。了解[事件疑難排解](../../building-journeys/troubleshooting-inbound.md)。

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

自訂動作可讓歷程呼叫您的 API。身為開發人員，您將建立自訂動作叫用的 API 端點：

1. **建立您的 API 端點**：建立 Journey Optimizer 將在歷程執行期間呼叫的 RESTful API 端點。您的端點應：
   * 接受 JSON 承載
   * 驗證請求 (OAuth、API 金鑰或 JWT)
   * 在適當的逾時限制內處理請求
   * 以預期格式傳回回應

1. **了解自訂動作功能**：自訂動作可以連線至第三方系統，例如 Epsilon、Slack、Firebase 或您自己的服務。深入了解[自訂動作](../../action/action.md)。

1. **使用動作設定**：您的[管理員](administrator.md)或[資料工程師](data-engineer.md)將在 Journey Optimizer 中設定自訂動作，定義 API 端點 URL、驗證方法和參數。您將為他們提供您的 API 規格。了解[自訂動作設定](../../action/about-custom-action-configuration.md)。

1. **傳回可操作資料**：設計您的 API 以傳回可用於後續歷程步驟的資料。了解[動作回應](../../action/action-response.md)。

1. **實作速率限制**：確保您的端點可以處理預期的流量。Journey Optimizer 套用每秒 5000 次呼叫的限制，但您的系統應可復原。了解[上限與節流](../../configuration/external-systems.md)。

**範例使用案例**：使用自訂動作[將歷程事件寫入 Experience Platform](../../building-journeys/custom-action-aep.md)。

## 使用 Journey Optimizer API {#apis}

Journey Optimizer 提供完整的 REST API 以便進行程式化存取：

1. **了解 API 功能**：Journey Optimizer API 可讓您以程式設計方式建立、讀取、更新和刪除各種資源。深入了解 [Journey Optimizer API](../../configuration/ajo-apis.md)。

1. **驗證**：請依照[本教學課程](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}中的指示，使用 Adobe Developer Console 設定 API 驗證。

1. **探索 API 參考**：瀏覽完整的 API 文件，並直接在 [Adobe Journey Optimizer API 參考](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}中試用 API。

1. **API 觸發的行銷活動**：使用 API 觸發的行銷活動建立交易型訊息。若是高流量案例 (最多5000 TPS)，請探索[高輸送量模式](../../campaigns/api-triggered-high-throughput.md) (需要附加授權)。

1. **決策管理 API**：使用專門的 API 進行產品建議管理和決策。若要了解更多資訊，請參閱[決策管理 API 指南](../../offers/api-reference/getting-started.md)。

## 測試和偵錯 {#testing}

1. **偵錯 SDK 實作**：使用 Adobe Experience Platform Assurance 即時檢查 SDK 事件、驗證資料收集，以及疑難排解整合問題。[深入了解 Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=zh-Hant){target="_blank"}。

1. **測試事件傳送**：確認 Adobe Experience Platform 已正確接收來自您應用程式的事件，並如預期觸發歷程。監視事件擷取並驗證承載結構。

1. **驗證 API 整合**：測試您的自訂動作端點，以確保它們可正確處理 Journey Optimizer 請求、在逾時限制內回應，以及傳回預期的資料格式。

1. **搭配測試輪廓使用測試模式**：與您的[資料工程師](data-engineer.md)合作，存取測試輪廓，然後使用歷程測試模式驗證您的實作。了解如何[測試歷程](../../building-journeys/testing-the-journey.md)。

1. **監視 SDK 記錄**：在您的 SDK 實作中啟用偵錯記錄，以疑難排解開發期間的問題：
   * **Mobile SDK**：啟用記錄以檢視 SDK 事件和 API 呼叫
   * **Web SDK**：使用瀏覽器控制台監視 SDK 活動

1. **驗證資料流設定**：確定您的資料流已正確設定為傳送資料至 Journey Optimizer。檢查事件是否流經資料流到達正確的目的地。

1. **查詢歷程資料以進行分析**：使用資料湖上的 SQL 查詢來分析歷程步驟事件、偵錯問題，以及監視自訂動作績效。探索[歷程分析的查詢範例](../../reports/query-examples.md)，包括：
   * 輪廓進入/退出追蹤與捨棄原因
   * 自訂動作績效量度 (延遲、輸送量、錯誤)
   * 事件傳送和錯誤模式
   * 歷程執行個體狀態

## 進階開發人員主題 {#advanced-topics}

### 使用內容資料及擴充

* **反覆處理陣列**：使用 Handlebars 語法在訊息中顯示來自事件、自訂動作回應和資料集查詢的動態清單。了解如何[反覆處理內容資料](../../personalization/iterate-contextual-data.md)。
* **資料集查詢**：實作資料集查詢，以擴充 Adobe Experience Platform 資料集的歷程資料。與您的資料工程師共同處理設定。了解[資料集查詢](../../building-journeys/dataset-lookup.md)。

### 使用同意與治理

在您的整合中實作資料治理和同意原則：

* **資料治理**：將資料使用原則套用至自訂動作。深入了解[資料治理](../../action/action-privacy.md)。
* **同意管理**：在您的實作中處理客戶同意偏好設定。了解[同意](../../action/consent.md)。

### 最佳化和最佳做法

* **上限與節流**：了解速率限制並實作適當的節流。了解[外部系統](../../configuration/external-systems.md)。
* **歷程最佳化**：遵循[歷程最佳化](../../building-journeys/optimize.md)的最佳做法。
* **錯誤處理**：實作強大的錯誤處理。檢閱[錯誤碼](../../building-journeys/error-codes-reference.md)和[疑難排解指南](../../building-journeys/troubleshooting.md)。

## 其他資源 {#additional-resources}

* **Developer Console**：存取 [Adobe Developer Console](https://developer.adobe.com){target="_blank"} 以建立整合並管理 API 認證。
* **範例代碼**：探索 [GitHub 上的範例實作](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}。
* **教學課程影片**：透過 [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hant){target="_blank"} 的實作教學課程學習。
* **開發人員社群**：與其他開發人員交流，並在 Adobe 社群論壇中取得支援。

## 跨角色共同作業 {#next-steps}

您的實作工作與其他團隊成員的工作有交集：

>[!BEGINTABS]

>[!TAB 與資料工程師合作]

與[資料工程師](data-engineer.md)共同處理資料與事件設定：

* 取得實作所需的 XDM 結構描述和事件結構
* 了解您需要傳送哪些事件及其必要的承載格式
* 就資料收集需求和資料品質標準達成一致
* 同時測試事件傳送和資料擷取

>[!TAB 與管理員合作]

與[管理員](administrator.md)共同處理存取權和設定：

* 提供要設定之自訂動作的 API 規格
* 請求必要的權限和 API 認證
* 協調管道設定需求 (例如推播憑證)
* 就測試環境和沙箱策略達成一致

>[!TAB 與行銷人員合作]

與[行銷人員](marketer.md)共同處理歷程需求和測試：

* 了解哪些使用者互動應該觸發事件
* 實作內容績效和使用者參與的追蹤
* 支援使用您實作的功能測試歷程
* 對訊息傳送或個人化問題進行疑難排解

>[!ENDTABS]

## 開始實作

準備好開始建立了嗎？從以上區段選擇您的第一個實作區域：

1. **行動應用程式？**&#x200B;開始進行 [Mobile SDK 整合](#mobile-integration)
2. **網站？**&#x200B;開始[設定 Web SDK](#web-implementation)
3. **API 整合？**&#x200B;跳轉至[使用 API](#apis)
4. **自訂系統？**&#x200B;查看[自訂動作](#custom-actions)

每個區段都包含詳細技術文件、程式碼範例和教學課程的連結，以指導您的實作。
