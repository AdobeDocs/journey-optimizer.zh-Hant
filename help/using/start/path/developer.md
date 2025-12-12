---
title: '開發人員快速入門 '
description: 作為資料工程師，深入瞭解如何使用 Journey Optimizer
feature: Get Started
role: Developer
level: Experienced
exl-id: 5053dd4f-d050-415f-bc74-d6d061bdcbe1
source-git-commit: ed3246d0bd552fee9c4df01babe18a5c1acd3b5f
workflow-type: tm+mt
source-wordcount: '1886'
ht-degree: 2%

---

# 開發人員快速入門  {#get-started-developers}

您身為&#x200B;**開發人員**，有責任實作並整合[!DNL Adobe Journey Optimizer]至您的應用程式與系統。 一旦[!DNL Adobe Journey Optimizer]系統管理員[和](administrator.md)資料工程師[授予您存取許可權並準備好您的環境，您就可以開始使用](data-engineer.md)。

## 您在Journey Optimizer生態系統中的角色

其他團隊成員透過使用者介面設定Journey Optimizer時，您將專注於：

* 在行動應用程式和網頁應用程式中&#x200B;**實作SDK**
* 從您的應用程式&#x200B;**傳送事件**&#x200B;以觸發歷程
* **建置API端點**，Journey Optimizer可透過自訂動作呼叫此端點
* **整合** Journey Optimizer與您現有的系統和基礎結構
* **測試和偵錯**&#x200B;您的實作

您的[資料工程師](data-engineer.md)將處理資料結構描述、事件設定和資料來源。 您的[管理員](administrator.md)將設定許可權和通道設定。 [行銷人員](marketer.md)將設計使用您實作的歷程和內容。

本指南涵蓋開始使用Journey Optimizer的基本技術實作步驟。 無論您是建置行動應用程式、網頁體驗或API整合，請遵循以下區段來設定您的實施。

## 先決條件 {#prerequisites}

在開始實作之前，請確定您已：

| 類別 | 需求 |
|----------|-------------|
| **技術技能** | *使用JavaScript (適用於Web SDK)或Swift/Kotlin (適用於Mobile SDK)<br>*瞭解RESTful API和JSON<br>*熟悉非同步程式設計和事件導向架構<br>*瞭解貴組織的應用程式架構 |
| **存取和工具** | *存取[Adobe Developer Console](https://developer.adobe.com){target="_blank"}以取得API認證<br>*開發環境以存取應用程式的程式碼基底<br>*測試工具，例如Postman以進行API測試<br>*瀏覽器開發人員工具或行動偵錯工具 |
| **來自其他團隊成員** | *您的[管理員](administrator.md)<br>* XDM結構描述和事件定義從您的[資料工程師](data-engineer.md)<br>*需求和使用案例授予的環境存取權（從您的[行銷人員](marketer.md)） |

## 瞭解技術基礎 {#technical-foundation}

開始實作前，請先熟悉核心技術概念：

1. **Adobe Experience Platform整合**： Journey Optimizer原本是建置在Adobe Experience Platform上。 瞭解基礎架構將幫助您建置更有效的實作。 深入瞭解[Journey Optimizer的運作方式](../understanding-ajo.md)。

1. **XDM資料模型**： Journey Optimizer使用Experience Data Model (XDM)來建構事件和設定檔資料。 作為開發人員，您必須瞭解如何傳送符合[資料工程師](data-engineer.md)所設定之結構描述的資料。 瞭解[XDM結構描述](../../data/get-started-schemas.md)。

1. **驗證和安全性**：所有實作都需要正確的驗證。 瞭解如何設定SDK和API的驗證。 瞭解[API驗證](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}。

## 設定行動應用程式整合 {#mobile-integration}

### 設定Adobe Experience Platform Mobile SDK

若要啟用推播通知、應用程式內訊息和其他行動功能，請將Adobe Experience Platform Mobile SDK整合至您的行動應用程式。

1. **安裝及設定Mobile SDK**：請依照[Adobe Experience Platform Mobile SDK檔案](https://developer.adobe.com/client-sdks/documentation/getting-started/){target="_blank"}操作，開始使用SDK整合。

1. **建立行動屬性**：在[!DNL Adobe Experience Platform Data Collection]中設定行動屬性。 瞭解如何[建立和設定行動屬性](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/){target="_blank"}。

1. **設定推播通知**：
   * 針對&#x200B;**iOS應用程式**：向APN註冊您的應用程式(Apple推播通知服務)。 在[Apple檔案](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target="_blank"}中進一步瞭解。
   * 針對&#x200B;**Android應用程式**：為您的Android應用程式設定Firebase Cloud Messaging。 在[Google檔案](https://firebase.google.com/docs/cloud-messaging/android/client){target="_blank"}中進一步瞭解。

1. **測試您的行動整合**：使用[行動入門快速入門工作流程](../../push/mobile-onboarding-wf.md)來快速設定並測試您的行動設定。

設定推播通知的詳細步驟可在[此頁面](../../push/push-configuration.md)上取得。

### 實作程式碼型體驗(行動SDK)

針對使用程式碼體驗的原生行動應用程式個人化：

* 請依照[本教學課程](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}中的指示進行Mobile SDK實作
* 檢閱[iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"}和[Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}的範例實作

## 實作Web體驗 {#web-implementation}

### 設定Adobe Experience Platform Web SDK

針對網頁型實作，Web SDK是您的主要整合點：

1. **安裝Web SDK**：請依照[Web SDK實作指南](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}操作，在您的網站上設定SDK。

1. **設定資料串流**：啟用Journey Optimizer後，在[!DNL Adobe Experience Platform Data Collection]中建立並設定資料串流。 在[資料串流檔案](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hant){target="_blank"}中進一步瞭解。

1. **啟用Web推播通知** （選用）：在您的Web SDK設定中設定[pushNotifications屬性](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/pushnotifications){target="_blank"}，並使用[sendPushSubscription命令](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/sendpushsubscription){target="_blank"}來註冊推播訂閱。

### 實作程式碼型體驗(網頁SDK)

程式碼型體驗可讓您個人化任何數位接觸點：

1. **選擇您的實作方法**：使用者端、伺服器端或混合式。 檢閱每個方法的[實作範例](../../code-based/code-based-implementation-samples.md)。

1. **定義介面**：識別您要在應用程式中傳遞個人化內容的位置。 瞭解[表面組態](../../code-based/code-based-surface.md)。

1. **實作內容呈現**：使用網頁SDK擷取並套用個人化內容。 請參閱[程式碼型實作教學課程](../../code-based/code-based-decisioning-implementations.md)。

1. **傳送顯示和互動事件**：追蹤內容顯示的時間以及使用者與內容互動以進行分析和最佳化的時間。

探索GitHub [上的](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}範例實作，瞭解程式碼型體驗的實際運作情況。

深入瞭解[程式碼式體驗快速入門](../../code-based/get-started-code-based.md)。

## 實作事件串流 {#event-streaming}

### 傳送事件以觸發歷程

作為開發人員，您將實作程式碼以傳送觸發歷程的事件。 您的[資料工程師](data-engineer.md)將在Journey Optimizer中設定事件結構描述和定義。

1. **瞭解事件裝載**：請與您的資料工程師合作，取得事件結構描述和必要的裝載結構。 裝載必須符合其所設定的XDM結構描述。 瞭解[事件結構描述需求](../../event/experience-event-schema.md)。

1. **實作事件串流**：使用[串流擷取API](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hant){target="_blank"}將事件傳送至Adobe Experience Platform。 瞭解傳送事件的[步驟](../../event/additional-steps-to-send-events-to-journey.md)。

1. **處理事件型別**：
   * **單一事件**：針對個人特定動作實作事件傳送（例如，按鈕點選、購買完成）
   * **業務活動**：傳送業務相關活動（例如，存貨更新、價格變更）

1. **測試事件傳送**：確認事件已正確接收，並如預期觸發歷程。 瞭解[事件疑難排解](../../building-journeys/troubleshooting-inbound.md)。

**透過API傳送事件的**&#x200B;實作範例：

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

深入瞭解[使用歷程事件](../../event/about-events.md)。

## 開發自訂動作端點 {#custom-actions}

自訂動作可讓歷程呼叫您的API。 作為開發人員，您將建置自訂動作呼叫的API端點：

1. **建置您的API端點**：建立Journey Optimizer將在歷程執行期間呼叫的RESTful API端點。 您的端點應：
   * 接受JSON裝載
   * 驗證請求（OAuth、API金鑰或JWT）
   * 在適當的逾時限制內處理請求
   * 以預期格式傳回回應

1. **瞭解自訂動作功能**：自訂動作可以連線至協力廠商系統，例如Epsilon、Slack、Firebase或您自己的服務。 深入了解[自訂動作](../../action/action.md)。

1. **使用動作設定**：您的[管理員](administrator.md)或[資料工程師](data-engineer.md)將在Journey Optimizer中設定自訂動作，定義API端點URL、驗證方法和引數。 您會提供他們您的API規格。 瞭解[自訂動作組態](../../action/about-custom-action-configuration.md)。

1. **傳回可操作的資料**：設計您的API以傳回可用於後續歷程步驟的資料。 瞭解[動作回應](../../action/action-response.md)。

1. **實作速率限制**：請確定您的端點可以處理預期的磁碟區。 Journey Optimizer套用5000次呼叫/秒的限制，但您的系統應可復原。 瞭解[上限與節流](../../configuration/external-systems.md)。

**範例使用案例**： [使用自訂動作將歷程事件寫入Experience Platform](../../building-journeys/custom-action-aep.md)。

## 使用 Journey Optimizer API 運作 {#apis}

Journey Optimizer提供完整的REST API以便程式設計方式存取：

1. **瞭解API功能**： Journey Optimizer API可讓您以程式設計方式建立、讀取、更新和刪除各種資源。 瞭解[Journey Optimizer API](../../configuration/ajo-apis.md)。

1. **驗證**：請依照[本教學課程](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}中的指示，使用Adobe Developer Console設定API驗證。

1. **探索API參考**：瀏覽完整的API檔案，並直接在[Adobe Journey Optimizer API參考](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}中試用API。

1. **API觸發的行銷活動**：使用API觸發的行銷活動建立交易式訊息。 若是大量情況（最多5000 TPS），請探索[高輸送量模式](../../campaigns/api-triggered-high-throughput.md) （需要附加授權）。

1. **決定管理API**：使用專門的API進行優惠方案管理和決定。 進一步瞭解[決定管理API指南](../../offers/api-reference/getting-started.md)。

## 測試和除錯 {#testing}

1. **偵錯SDK實作**：使用Adobe Experience Platform Assurance即時檢查SDK事件、驗證資料收集，以及疑難排解整合問題。 [進一步瞭解Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=zh-Hant){target="_blank"}。

1. **測試事件傳送**：確認Adobe Experience Platform已正確接收來自您應用程式的事件，並如預期觸發歷程。 監視事件擷取並驗證裝載結構。

1. **驗證API整合**：測試您的自訂動作端點，以確保它們可正確處理Journey Optimizer要求、在逾時限制內回應，以及傳回預期的資料格式。

1. **搭配測試設定檔使用測試模式**：與您的[資料工程師](data-engineer.md)合作，以存取測試設定檔，然後使用歷程測試模式驗證您的實作。 瞭解如何[測試歷程](../../building-journeys/testing-the-journey.md)。

1. **監視SDK記錄**：在您的SDK實作中啟用偵錯記錄，以解決開發期間的問題：
   * **行動SDK**：啟用記錄以檢視SDK事件和API呼叫
   * **網頁SDK**：使用瀏覽器主控台監視SDK活動

1. **驗證資料流設定**：確定您的資料流已正確設定為傳送資料至Journey Optimizer。 檢查事件是否流經資料流到達正確的目的地。

1. **查詢歷程資料以進行分析**：使用資料湖上的SQL查詢來分析歷程步驟事件、偵錯問題，以及監視自訂動作效能。 探索歷程分析的[查詢範例](../../reports/query-examples.md)，包括：
   * 設定檔登入/退出追蹤與捨棄原因
   * 自訂動作效能測量結果（延遲、輸送量、錯誤）
   * 事件傳遞和錯誤模式
   * 歷程執行個體狀態

## 進階開發人員主題 {#advanced-topics}

### 使用內容資料及擴充

* **在陣列上重複**：使用Handlebars語法在訊息中顯示來自事件、自訂動作回應和資料集查詢的動態清單。 瞭解[反複運算內容資料](../../personalization/iterate-contextual-data.md)。
* **資料集查詢**：實作資料集查詢，以擴充Adobe Experience Platform資料集的歷程資料。 與您的資料工程師合作進行設定。 瞭解[資料集查詢](../../building-journeys/dataset-lookup.md)。

### 使用同意與控管

在您的整合中實作資料控管和同意原則：

* **資料控管**：將資料使用原則套用至自訂動作。 深入瞭解[資料控管](../../action/action-privacy.md)。
* **同意管理**：在您的實作中處理客戶同意偏好設定。 瞭解[同意](../../action/consent.md)。

### 最佳化和最佳實務

* **上限與節流**：瞭解速率限制並實作適當的節流。 瞭解[外部系統](../../configuration/external-systems.md)。
* **歷程最佳化**：遵循[歷程最佳化](../../building-journeys/optimize.md)的最佳實務。
* **錯誤處理**：實作健全的錯誤處理。 檢閱[錯誤碼](../../building-journeys/error-codes-reference.md)和[疑難排解指南](../../building-journeys/troubleshooting.md)。

## 其他資源 {#additional-resources}

* **Developer Console**：存取[Adobe Developer Console](https://developer.adobe.com){target="_blank"}以建立整合併管理API認證。
* **範常式式碼**：探索GitHub上的[範例實作](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"}。
* **教學課程影片**：透過[Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hant){target="_blank"}的實作教學課程學習。
* **開發人員社群**：與其他開發人員交流，並在Adobe社群論壇中取得支援。

## 跨角色共同作業 {#next-steps}

您的實作工作與其他團隊成員相交：

>[!BEGINTABS]

>[!TAB 與資料工程師合作]

與[資料工程師](data-engineer.md)共同作業資料與事件設定：

* 取得實施所需的XDM結構描述和事件結構
* 瞭解您需要傳送哪些事件及其必要的裝載格式
* 符合資料收集需求和資料品質標準
* 將測試事件傳送和資料擷取結合在一起

>[!TAB 與系統管理員合作]

與[管理員](administrator.md)共同作業存取和設定：

* 提供要設定之自訂動作的API規格
* 要求必要的許可權和API認證
* 協調通道設定需求（例如推送憑證）
* 調整測試環境和沙箱策略

>[!TAB 與行銷人員合作]

與[行銷人員](marketer.md)共同作業歷程需求和測試：

* 瞭解哪些使用者互動應該觸發事件
* 實施內容效能和使用者參與追蹤
* 支援使用您實作的功能測試歷程
* 疑難排解訊息傳送或個人化問題

>[!ENDTABS]

## 保持最新狀態

跟上最新Journey Optimizer功能和技術變更：

* **[發行說明](../../rn/release-notes.md)**：檢閱每月發行的新功能、API變更、SDK更新及錯誤修正
* **[檔案更新](../../rn/documentation-updates.md)**：追蹤技術檔案最近的變更，包括新的實作指南和程式碼範例
* **[產品通知](../../rn/releases.md#staying-informed)**：瞭解如何訂閱Journey Optimizer更新的電子郵件和產品內通知，包括新的SDK版本、API變更、重大變更和重要安全性更新

## 開始實作

準備好開始建立了嗎？ 從以上區段選擇您的第一個實作區域：

1. **行動應用程式？**&#x200B;開始於[行動SDK整合](#mobile-integration)
2. **網站？**&#x200B;以[網頁SDK設定](#web-implementation)開始
3. **API整合？**&#x200B;跳至[使用API](#apis)
4. **自訂系統？**&#x200B;簽出[自訂動作](#custom-actions)

每個區段都包含詳細技術檔案、程式碼範例和教學課程的連結，以指導您的實施。
