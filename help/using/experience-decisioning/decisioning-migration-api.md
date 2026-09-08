---
title: 決策移轉 API
description: 瞭解如何使用決策移轉服務API，透過自動化相依性解析和復原支援，在沙箱之間移轉決策管理物件。
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 02ff2d2090fd2271c3b6ffc0832ff66b9fd0f0b7
workflow-type: tm+mt
source-wordcount: 3211
ht-degree: 2%

---

# 決策移轉 API {#decisioning-migration-api}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;使用Decisioning Migration Service API在沙箱之間移動決策管理物件，並具備自動化相依性分析和復原支援，因此您可以跨環境轉換決策內容，同時保留資料完整性。

>[!ENDSHADEBOX]

決策移轉服務API可讓您將決策管理物件從一個沙箱移轉至另一個沙箱。 移轉程式會以非同步工作流程執行，其中包含相依性分析、執行和選用的復原功能。

此API可讓您在環境<!--(e.g., from development to staging, or staging to production) -->之間順暢地轉換決策內容，同時維持資料完整性和關聯性。

若要瞭解與決策管理相較之決策的優點和功能，請參閱[此頁面](migrate-to-decisioning.md)。

## 功能 {#capabilities}

Decisioning移轉服務API提供下列功能：

* **相依性分析** — 識別來源和目標沙箱之間所有必要的相依性，包括屬性、區段和資料集需求。
* **彈性的移轉範圍** — 根據您的需求，在沙箱、優惠或決定層級執行移轉。
* **復原支援** — 如果在驗證期間發現問題，請還原已完成的移轉。

## 先決條件 {#prerequisites}

### 必要權限 {#permissions}

若要使用移轉API，您需要在來源沙箱和目標沙箱中設定適當的許可權：

**Source沙箱** — 決策管理物件的讀取存取權

**Target沙箱** — 建立和編輯決策物件的存取權

一般許可權包括：

* 管理/檢視決策
* 管理/檢視決定
* 管理產品建議
* 管理排名策略
* 管理行銷活動（如果移轉行銷活動相關成品）
* 管理/檢視資料串流（如果建立資料串流）
* 管理/檢視結構描述

>[!NOTE]
>
>瞭解如何在[本節](gs-experience-decisioning.md#steps)中指派決策許可權。 如需完整的許可權清單，請參閱[內建許可權](../administration/ootb-permissions.md#ootb-permissions)頁面。

### 準備您的目標沙箱 {#target-sandbox-preparation}

在執行移轉之前，請確定您的目標沙箱已正確設定：

* **屬性** — 確認必要的設定檔屬性和內容屬性存在於目標沙箱中，或為其準備對應。
* **區段** — 確認目標沙箱中存在必要的區段，或計畫使用名稱空間和ID來對應它們。
* **資料集** — 識別要用於移轉的資料集名稱(`dependency.datasetName`)。
* **資料流** — 決定移轉是否應建立資料流(`createDataStream`)。

如需沙箱管理的詳細資訊，請參閱[使用和指派沙箱](../administration/sandboxes.md)。

>[!NOTE]
>
>目標沙箱可與來源沙箱相同。 移轉流程會處理此情境並確保資料完整性，無論物件是在同一個沙盒內移轉，還是移轉至不同的沙箱。

### 跨沙箱移轉的必要條件 {#cross-sandbox-prerequisites}

當來源沙箱≠目標沙箱時，需要以下專案：

* **設定檔屬性** — 必須存在於目標沙箱中或具有預先定義的對應
* **區段ID** — 必須在目標沙箱中預先建立具有舊→新ID對應
* **身分對應** — 必須設定為一致的身分解析

## API 基本概念 {#api-basics}

### 基底 URL {#base-url}

使用以下基底URL：

* **生產**： `https://decisioning-migration.adobe.io`

### Authentication {#authentication}

所有API請求都需要以下標頭：

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

如需設定驗證的詳細指示，請參閱[Journey Optimizer驗證指南](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}。

## 移轉工作流程 {#migration-workflow}

移轉程式包含兩個主要步驟：分析相依性並執行移轉。 請依照下列步驟操作，以確保成功移轉。

### 步驟1：分析相依性 {#analyze-dependencies}

在移轉之前，請使用相依性工作流程來識別需要在目標沙箱中從決定管理對應到決定的專案。 此分析可協助您瞭解物件之間的關係，並準備必要的對應。

#### 建立相依性工作流程 {#create-dependency-workflow}

使用以下API呼叫建立相依性分析工作流程。

**API格式**

```http
POST /workflows/generate-dependencies
```

**沙箱層級相依性（建議優先）**

從沙箱層級分析開始，以取得所有相依性的完整檢視：

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies?request-level=sandbox" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" }
  }'
```

**選件層級相依性**

若要僅分析特定選件的相依性，請呼叫在查詢字串中具有`request-level=offer`的相同端點，並在內文中提供包含您要分析之選件ID的`offersList`陣列。

**決定層級相依性**

若要僅分析特定決定的相依性，請在查詢字串中使用`request-level=decision`，並在內文中提供包含您要分析之決定ID的`decisionsList`陣列。

#### 檢查相依性工作流程狀態 {#poll-dependency-status}

輪詢相依性工作流程以檢查分析何時完成。

**API格式**

```http
GET /workflows/generate-dependencies/{id}
```

**要求**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

當`status`欄位顯示`Completed`時，相依性分析已準備就緒。 使用工作流程輸出建置您的移轉相依性對應：

* **profileAttributes** — 將來源設定檔屬性對應到目標設定檔屬性
* **contextAttributes** — 將來源內容屬性對應至目標內容屬性
* **區段** — 將每個來源區段索引鍵對應到目標區段識別碼(`{namespace, id}`)
* **datasetName** — 用於移轉的目標體驗事件資料集。 資料流必須附加至啟用Journey Optimizer Edge (Web SDK)呼叫的資料流；其結構描述可用來新增移轉的內容屬性。

您在步驟2中移轉請求的`dependency`物件中提供這些對應。

### 步驟2：執行移轉 {#execute-migration}

分析相依性並準備對應後，您就可以執行移轉。

#### 建立移轉工作流程 {#create-migration-workflow}

使用步驟1的相依性對應來設定並執行您的移轉。

**API格式**

```http
POST /workflows/migration
```

**沙箱層級移轉**

若要將所有決策物件從一個沙箱移轉至另一個沙箱：

```shell
curl --request POST \
  --url 'https://decisioning-migration.adobe.io/workflows/migration?request-level=sandbox' \
  --header 'Authorization: Bearer <IMS_ACCESS_TOKEN>' \
  --header 'Content-Type: application/json' \
  --header 'x-gw-ims-org-id: <IMS_ORG_ID>' \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributes": {
        "sourceAttr1": "targetAttr1"
      },
      "segments": {
        "sourceSegmentKey1": {
          "namespace": "<TARGET_SEGMENT_NAMESPACE>",
          "id": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributes": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    }
  }'
```

**選件層級移轉**

若要僅移轉特定選件，請在查詢字串中使用`request-level=offer`並將`offersList`陣列新增至內文：

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**決策層級移轉**

若要僅移轉特定決定，請在查詢字串中使用`request-level=decision`並將`decisionsList`陣列新增至內文：

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

**要求欄位**

* **要求層級** （查詢） — 移轉範圍： `sandbox`、`offer`或`decision`。
* **imsOrgId** （必要） — 您的IMS組織ID。
* **sourceSandboxDetails.sandboxName** （必要） — 包含決定管理實體的Source沙箱。
* **targetSandboxDetails.sandboxName** （必要） — 建立決策實體的目標沙箱。
* **dependency.datasetName** （必要） — 目標體驗事件資料集。 它必須附加至啟用Journey Optimizer Edge (Web SDK)呼叫的資料流；其結構描述用於新增移轉的內容屬性。
* **createDataStream** - `true`會建立啟用Journey Optimizer的新資料流；`false`會重複使用已附加至`dependency.datasetName`中資料集的資料流。
* **dependency.profileAttributes** — 來源→目標設定檔屬性的對應。
* **dependency.contextAttributes** — 來源→目標內容屬性的對應。
* **dependency.segments** — 來源區段索引鍵→目標區段(`{namespace, id}`)的對應。
* **offersList[]** / **decisionsList[]** — 要移轉的優惠或決定ID；當`request-level`分別為`offer`或`decision`時為必要。

#### 監視移轉狀態 {#poll-migration-status}

輪詢移轉工作流程以追蹤其進度。

**API格式**

```http
GET /workflows/migration/{id}
```

**要求**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/migration/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

**移轉結果**

當`status`欄位顯示`Completed`時，移轉已成功。 工作流程`result`包含：
* 已移轉物件的對應
* 移轉期間遇到的任何警告

當`status`欄位顯示`Failed`時，請檢閱`errors[]`陣列和`result.error`欄位以取得有關所發生問題的詳細資訊。

每個工作流程（相依性、移轉和回覆）會傳回相同的資源欄位：

* **id** — 工作流程識別碼(UUID)；以相符的`GET /{id}`輪詢其狀態。
* **狀態** — 生命週期狀態： `New`、`Running`、`Completed`或`Failed`。
* **結果** — 出現在`Completed`上；工作流程輸出（例如，已移轉物件的對應及任何警告）。
* **錯誤[]** — 出現在`Failed`；結構化錯誤詳細資料（另請參閱`result.error`）。
* **_links.self** — 工作流程資源的URL。

## 驗證您的移轉 {#validate-migration}

移轉成功完成後，請確認所有物件皆已正確移轉。

### 驗證檢查清單 {#validation-checklist}

1. **區段** — 確認所有參照的區段都能根據您的對應正確解析目標沙箱中。
2. **屬性** — 確認所有設定檔屬性和內容屬性都存在於目標沙箱中，並已正確對應。
3. **決策物件** — 檢閱Journey Optimizer使用者介面中已移轉的物件：
   * 優惠（決定專案）
   * 適用性規則
   * 排名公式
   * 選擇策略
   * 決定原則
4. **資料流測試** — 如果已建立資料流，請使用Edge Interact API測試執行階段傳遞。

### 範例 {#test-runtime-delivery}

如果您的移轉建立了資料流，則可使用以下範例測試選件傳送：

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## 復原移轉 {#rollback}

如果您在驗證期間發現問題，您可以復原已完成的移轉，以將目標沙箱還原至其先前的狀態。

### 建立復原工作流程 {#create-rollback-workflow}

建立參考您要還原之移轉的復原工作流程，以啟動復原。

**API格式**

```http
POST /workflows/rollback
```

**要求**

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/rollback" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{ "rollbackWorkflowId": "<MIGRATION_WORKFLOW_ID>" }'
```

將`<MIGRATION_WORKFLOW_ID>`取代為您要復原的移轉工作流程識別碼。

### 監視復原狀態 {#poll-rollback-status}

輪詢復原工作流程以追蹤其進度。

**API格式**

```http
GET /workflows/rollback/{rollbackWorkflowId}
```

**要求**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/rollback/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

## 處理並行工作流程 {#handle-concurrency}

移轉API一次只允許每個組織執行一個工作流程。 如果您嘗試在另一個工作流程進行中時建立新工作流程，您將會收到&#x200B;**409衝突**&#x200B;錯誤回應（「工作流程已在進行中……」）。

在這種情況下，請等待進行中的工作流程完成，或擷取工作流程ID並輪詢其狀態。 目前的工作流程完成後，您可以建立一個新的工作流程。

## 移轉範圍和涵蓋範圍 {#migration-scope}

瞭解移轉的範圍，可協助您規劃及驗證從決策管理到決策的轉換。 本節概述移轉程式所涵蓋的內容，以及需要採取手動動作的內容。

### 範圍：涵蓋內容 {#in-scope}

移轉API會處理下列專案和功能：

* **使用案例** — 只有傳入/Edge決策使用案例在範圍內。 Journey Optimizer電子郵件頻道移轉中支援傳出或OD，但需要手動更新。
* **程式碼型體驗行銷活動** — 在移轉期間自動建立，目標沙箱中每個移轉的決定範圍會有一個行銷活動。
* **管道設定/介面** — 根據決策管理位置建立的管道設定/介面，確保決策回應的路由正確。
* **選件內容型別** — 只有在其內容型別為JSON或文字時，才會移轉選件。 其他內容型別需要手動重新建立。
* **優惠特性** — 保留在「個人化優惠專案 — 體驗決策」結構描述上的`offer_item_custom_attributes`欄位群組中，維護自訂中繼資料。
* **內容屬性** — 已新增至`custom_context_attributes`欄位群組中的Experience Event結構描述，以便追蹤及個人化。
* **決定範圍** — 一個決定管理決定範圍對應到一個選擇策略+一個決定策略+一個決策中的行銷活動，以確保正確的實體階層。
* **僅限API的適用性規則** — 僅限透過API建立的適用性規則（不在決定管理UI中）已移轉，並在決定中保持僅限API。 UI建立的規則也會移轉。

### 超出範圍：未涵蓋或需要手動操作的專案 {#out-of-scope}

下列專案需要手動動作或移轉工具不支援：

* **決策位置** — 移轉工具未建立位置。 您必須根據架構，在移轉之前或之後，於決策中手動建立這些專案。
* **位置層級上限** — 未移轉位置層級頻率上限。
* **非JSON/文字選件內容** — 具有JSON或文字以外內容型別（例如HTML、影像）的選件不會移轉，且需要在決定中手動重新建立。
* **設定檔屬性和區段** — 移轉工具絕對不會建立或編輯設定檔屬性和區段會籍。 這些必須已存在於您的目標沙箱中，才能執行移轉。
* **區段ID對應** — 區段ID必須在目標沙箱中預先建立。 您必須在移轉API請求中提供新→舊ID對應，以便解析區段。
* **資料收集程式碼變更** — 使用者端和伺服器端事件追蹤程式碼變更未自動化。 您的實作團隊必須更新事件集合，以使用決策請求/回應格式和決策事件結構。

## 實體對應參考 {#entity-mapping}

從決定管理移轉至決定時，實體會根據下表進行對應。 對應包括主要決策實體以及在移轉期間建立或使用的其他關聯實體。

### 決策實體對應的決策管理

| 決定管理實體 | 決策實體 | 其他實體 |
|-----------|--------------|-------------------|
| 決定 | 選擇策略 | 料號收集、適用性規則、排名公式 |
| | 決定原則 | 專案計數、選取策略、遞補優惠專案 |
| | 程式碼型體驗行銷活動 | 決定原則、內容、頻道設定、Journey Optimizer片段 |
| 放置環境 | 管道設定 | — |
| 集合 | 專案集合 | 整合標籤、選件專案 |
| 集合限定詞 | 統一標記 | — |
| 規則 | 決策規則 | — |
| 排名公式 | 決定排名公式 | — |
| 產品建議 | 選件專案 | 適用性規則、Journey Optimizer片段、統一標籤、頻率限定 |
| | 選件專案結構描述 | — |
| | Journey Optimizer片段 | — |

### 命名慣例

移轉程式會套用使用`ExD_`首碼的命名慣例，以確保一致性並防止命名衝突。

| Source物件 | 決定管理名稱模式 | 決策名稱模式 |
|---------------|-----------------|-------------------|
| 產品建議 | `<offerName>` | `ExD_<offerName>` |
| 適用性規則 | `<ruleName>` | `ExD_<ruleName>` |
| 排名公式 | `<formulaName>` | `ExD_<formulaName>` |
| 集合 | `<collectionName>` | `ExD_<collectionName>_<placementName>` |
| 決定→選擇策略 | `<decisionName>` | `ExD_<decisionName>_selection_strategy_<index>` |
| 決定→決定原則 | `<decisionName>` | `ExD_<decisionName>_<placementName>` |
| Journey Optimizer片段 | `<offerName>` | `ExD_<offerName>_<placementName>_<index>` |
| 放置→曲面 | `<placementName>` | `ExD_<placementName>` *（空格/點轉換為底線）* |
| 統一標籤 | `<sourceName>, <targetName>` | `ExDMigration_<sourceName>_<targetName>` |
| CBE Campaign | `<decisionName>, <placementName>` | `Campaign for <decisionName> : <placementName>` |

### 其他屬性

| Source屬性 | 目標位置 |
|-----------------|-----------------|
| 產品建議屬性 | 個人化優惠方案結構描述中的「migratedofferattributes」欄位 |
| 內容屬性 | 在移轉期間提供的資料集所附加之結構描述中的「migratedcontextattributes」欄位 |

## 請求和回應模型 {#request-response-model}

從決定管理移轉至Decisioning時，必須更新您的應用程式程式碼，才能使用新的請求和回應格式。 兩個系統都使用Edge Network端點，但裝載結構和欄位名稱不同。

### 決定管理Edge請求（最新） {#dm-request}

目前的決定管理Edge請求會遵循此結構：

**端點：**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**標頭：**
- `Authorization: Bearer <IMS_ACCESS_TOKEN>`
- `x-api-key: <API_KEY>` （來自Developer Console）
- `x-gw-ims-org-id: <IMS_ORG_ID>` （格式： `{ORG_ID}@AdobeOrg`）
- `x-request-id: <UNIQUE_REQUEST_ID>` （用於追蹤與重複資料刪除）
- `Content-Type: application/vnd.adobe.xdm+json; schema="…/decision-request;version=1.0"`
- `Accept: application/vnd.adobe.xdm+json; schema="…/decision-response;version=1.0"`
- `x-sandbox-name: <SANDBOX_NAME>` （例如prod、dev）

**要求內文引數：**
- `xdm:dryRun` (true/false) — 測試要求而不汙染報告
- `xdm:propositionRequests[]` — 決定要求陣列：
  - `activityId` — 決定活動識別碼
  - `placementId` — 位置識別碼
  - `itemCount` — 要傳回的最大優惠方案數量
- `xdm:profiles[].xdm:identityMap` — 身分對應（電子郵件、ECID等）
- `xdm:validateContextData` — 嚴格的內容資料驗證旗標
- `xdm:responseFormat.xdm:includeContent` — 僅包含實際內容與ID

**範例要求內文：**

```json
{
  "xdm": {
    "dryRun": false,
    "propositionRequests": [
      { "activityId": "<ACTIVITY_ID>", "placementId": "<PLACEMENT_ID>", "itemCount": 3 }
    ],
    "profiles": [
      { "identityMap": { "ECID": [ { "id": "<ECID>", "primary": true } ] } }
    ],
    "validateContextData": true,
    "responseFormat": { "includeContent": true }
  }
}
```

>[!NOTE]
>如需完整的決定管理(OD)要求/回應參考，請參閱[Edge Decisioning API](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api) （網頁SDK / Edge變體，其使用帶有`activityId`和`placementId`的base64編碼`decisionScopes`）。

### 決定Edge請求（移轉後） {#decisioning-request}

移轉後，請透過相同的Edge Network端點使用決策請求格式。

**端點：**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**金鑰要求欄位：**
- `query.identity.fetch` — 要解析的身分型別陣列（例如，`["ECID"]`）
- `event.xdm.environment.type` — 環境型別： `"browser"`、`"app"`或`"server"`
- `event.xdm.environment.browserDetails` — 瀏覽器中繼資料(`viewportWidth`， `viewportHeight`， `userAgent`)
- `event.xdm.identityMap` — 與決定管理相同的身分對應
- `event.xdm.timestamp` - ISO 8601時間戳記
- `query.personalization.surfaces` — 目標表面的陣列（例如，`["web://site.com/homepage"]`） — 取代`decisionScope`
- `query.personalization.schemas` — 要傳回的內容結構描述（例如，`["json-content-item", "html-content-item"]`）
- `data.__adobe.ajo.allowDuplicateDecisionItems` — 重複資料刪除控制項（預設為`true`；設定`false`，以便符合多個表面的專案僅傳回一次，而其他表面接收遞補/空白專案）。 取代決定管理`allowDuplicatePropositions`。
- `data.__adobe.ajo.dryRun` — 測試旗標；隱藏報表和上限計數器的意見回饋事件。 取代決定管理`xdm:dryRun`。 在生產前移除。

**範例要求內文（伺服器端）：**

```json
{
  "events": [
    {
      "query": {
        "identity": { "fetch": ["ECID"] },
        "personalization": {
          "surfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"],
          "schemas": [
            "https://ns.adobe.com/personalization/json-content-item",
            "https://ns.adobe.com/personalization/html-content-item"
          ]
        }
      },
      "xdm": {
        "eventType": "decisioning.propositionFetch",
        "environment": {
          "type": "browser",
          "browserDetails": { "viewportWidth": 1280, "viewportHeight": 900, "userAgent": "<USER_AGENT>" }
        },
        "identityMap": {
          "ECID": [ { "id": "<ECID>", "authenticatedState": "ambiguous", "primary": true } ]
        },
        "timestamp": "2025-09-08T12:00:00.000Z"
      },
      "data": {
        "__adobe": { "ajo": { "allowDuplicateDecisionItems": false } }
      }
    }
  ],
  "meta": {
    "state": {
      "domain": "my-web",
      "cookiesEnabled": true,
      "entries": [
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>" },
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>" }
      ]
    }
  }
}
```

>[!NOTE]
>如需完整的Journey Optimizer Decisioning網頁SDK / Edge參考資料，請參閱[程式碼型體驗：決策實作](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations)。

### 決定Edge回應 {#decisioning-response}

決策回應包含多個控點，其組織方式為關注點型別： `personalization:decisions` （選件）、`locationHint:result`及`state:store` （要保留的Cookie）。

**回應結構：**

```json
{
  "requestId": "<REQUEST_ID>",
  "handle": [
    {
      "type": "personalization:decisions",
      "eventIndex": 0,
      "payload": [
        {
          "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
          "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
          "scopeDetails": {
            "decisionProvider": "AJO",
            "correlationID": "<CORRELATION_ID>",
            "characteristics": {
              "eventToken": "<base64 message-level event token>",
              "subPropositions": "<base64-encoded array of decision items>"
            },
            "rank": 1,
            "activity": {
              "id": "<campaignId>#<actionId>",
              "priority": 0,
              "matchedSurfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"]
            }
          },
          "items": [
            {
              "id": "36646bab-af1b-44c6-b632-bbfb9c357919",
              "schema": "https://ns.adobe.com/personalization/json-content-item",
              "data": { "content": "{ ...offer JSON... }" }
            }
          ]
        }
      ]
    },
    {
      "type": "locationHint:result",
      "payload": [
        { "scope": "EdgeNetwork", "hint": "ind1", "ttlSeconds": 1800 }
      ]
    },
    {
      "type": "state:store",
      "payload": [
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>", "maxAge": 1800 },
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>", "maxAge": 34128000 }
      ]
    }
  ]
}
```

**金鑰回應欄位：**
- `handle[].type` — 控制代碼型別(`personalization:decisions`， `locationHint:result`， `state:store`)
- `payload[].id` — 唯一的主張執行個體識別碼 — 在顯示/互動事件上回呼
- `payload[].scope` — 主張已解析的表面URI
- `payload[].scopeDetails.decisionProvider` — 確認引擎為`AJO`
- `payload[].scopeDetails.correlationID` — 連結決策執行個體以服務事件
- `payload[].scopeDetails.rank` / `payload[].scopeDetails.activity` — 主張的排名和行銷活動/動作中繼資料
- `payload[].scopeDetails.characteristics.eventToken` — 訊息層級追蹤權杖
- `payload[].scopeDetails.characteristics.subPropositions` — 決定專案&#x200B;**的Base64編碼**&#x200B;陣列；每個專案都有自己的每個專案`token`。 這些每個專案的代號就是您在顯示/互動事件中傳入`propositionAction.tokens`的內容
- `payload[].items[].schema` / `payload[].items[].data.content` — 要呈現的內容結構描述和實際選件內容(JSON/HTML)
- `state:store`裝載 — 要在後續請求上保留及轉送的身分和叢集Cookie （伺服器端）

`characteristics.subPropositions`字串base64會解碼成服務專案的陣列，每個專案都有其個別專案`token`：

```json
[
  {
    "id": "1ae75277-8832-4c23-bbbc-09f01cfe6c8b",
    "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
    "scopeDetails": { "decisionProvider": "EXD", "correlationID": "<CORRELATION_ID>-0", "rank": 1 },
    "items": [
      { "id": "dps:<schema>:1be64ff83a612488", "name": "ExD_Personal Loan Offer", "score": 997.0, "token": "CLaefQnVLcLbCtzEXV3Jeg" },
      { "id": "dps:<schema>:1be6516838e1248c", "name": "ExD_Home Loan Offer",     "score": 995.0, "token": "ALlB5KV1B0e+CpHoahi7Ew" },
      { "id": "dps:<schema>:1be650da3cd06e98", "name": "ExD_Auto Loan Offer",     "score": 994.0, "token": "koJTRQcwFkR92AqbZ88ytQ" },
      { "id": "dps:<schema>:1be65612d5a1248d", "name": "ExD_Fallback Offer",      "itemSelection": { "selectionDetail": { "selectionType": "fallback" } }, "token": "GHo4ow7h6iCzBOhYR1+6jg" }
    ]
  }
]
```

## 實作模式 {#implementation-patterns}

Decisioning支援三種實施方法：

### 使用者端實施（網頁SDK /行動SDK） {#client-side}

網頁SDK或行動SDK會自動處理所有請求和Cookie管理。 SDK會儲存及轉送每個要求的身分識別與叢集Cookie。

**Cookie處理：**&#x200B;自動 — Web SDK管理`kndctr_<OrgId>_identity`和`kndctr_<OrgId>_cluster` Cookie。

### 伺服器端實作(Edge Network API) {#server-side}

應用程式伺服器會直接將訊息發佈至Edge Network，而且必須手動管理Cookie轉送。 伺服器會從傳入的請求中擷取瀏覽器Cookie，並透過`meta.state.entries[]`將其轉送至Edge Network，然後在回應中傳回Cookie。

**Cookie處理：**&#x200B;手動 — 應用程式伺服器必須從瀏覽器要求擷取Cookie，在要求內文中轉送至Edge Network，並設定為回應。 Cookie必須在`meta.state.entries`中明確轉送，以保持身分的一致性。

### 混合實施 {#hybrid}

結合伺服器端轉譯（初始頁面載入）和使用者端SDK （後續互動）。 伺服器會透過Edge Network呈現初始內容，然後由Web SDK接手後續的個人化請求。

**Cookie處理：**&#x200B;混合 — 伺服器端需要手動將Cookie轉送至Edge Network；使用者端會由Web SDK自動處理。 確保伺服器端轉譯的身分識別權杖可供使用者端SDK使用，以取得一致的身分識別解析。

## 事件追蹤和資料收集 {#event-tracking}

若要正確屬性化決策結果、啟用頻率上限並運用人工智慧為基礎的排名最佳化，您必須使用決策事件結構描述來實作事件追蹤。

### 必要事件欄位 {#event-fields}

需要`eventType`和`_experience.decisioning.propositionEventType`。 如果缺少其中一項，則對應的display/interact計數器不會增加。

* **`eventType`** — 指定事件類別：
  - `decisioning.propositionDisplay` — 曝光事件（向使用者顯示的優惠）
  - `decisioning.propositionInteract` — 互動事件（使用者已點按或參與優惠方案）

* **`_experience.decisioning.propositionEventType`** — 標幟事件子型別。 包含設定為`1`的&#x200B;**一個**&#x200B;事件型別索引鍵（每個值為`1`或`0`；請勿將多個事件型別設定為相同物件中的`1`）：
  - `{ "display": 1 }` — 曝光事件
  - `{ "interact": 1 }` — 互動事件
  - 如果所有`display`/`interact`/`dismiss`都是`0` — 或`eventType`是`decisioning.proposition<Display|Interact|Dismiss>`以外的任何值 — 此事件會視為&#x200B;**自訂事件**。

* **`_experience.decisioning.propositionAction.tokens[]`** — 每個專案的Token識別要遞增計數器的服務專案：
  - 從已解碼的`subPropositions`陣列複製每個專案的`token` — **not** `scopeDetails.characteristics.eventToken`，這是不同的訊息層級權杖。
  - 完全按照收到的方式傳遞Token，未加以修改。
  - **互動事件：**&#x200B;提供&#x200B;**正好一個**&#x200B;權杖（點選的專案）。
  - **顯示事件：**&#x200B;選擇性 — 提供語彙基元以遞增特定專案，或&#x200B;**省略** `tokens`以遞增`subPropositions`中&#x200B;**所有**&#x200B;專案的計數器。

* **`_experience.decisioning.propositions[]`** — 回應已提供的主張，包括`id`、`scope`和回應中的完整`scopeDetails` （包含`characteristics.subPropositions`且需要`decisionProvider`）。 您不需要建置明確的`items[]`陣列。

### 結構描述需求 {#schema-requirements}

在移轉之前，將決定欄位群組關聯至您的事件資料集結構：

1. 在Experience Platform中，開啟您的事件資料集結構
2. 新增`Experience Event - Proposition Details`欄位群組
3. 確認下列欄位已對應：
   - `_experience.decisioning.*`欄位
   - `_experience.decisioning.propositionAction.tokens`
   - `_experience.decisioning.propositionEventType`

### 追蹤權杖處理 {#tracking-token}

追蹤權杖必須按照以下要求處理：

* **每個專案的Token磁碟機計數器** — `propositionAction.tokens`中的值是來自`subPropositions`之每個服務專案的`token`，而不是訊息層級`characteristics.eventToken`。
* **互動事件** — 僅提供一個權杖（點選的專案）。
* **顯示事件** — Token是選擇性的；省略以增加`subPropositions`中的所有專案，或提供特定的Token以僅增加這些專案。
* **請勿修改Token** — 將值與收到的值完全傳遞；請勿加以編碼、剖析或變更。

## 決策事件範例 {#event-examples}

每個範例都會回溯已送達的主張（包括其攜帶`characteristics.subPropositions`的`scopeDetails`），並設定`eventType`和`propositionEventType`。 計數器會針對`subPropositions`中的專案遞增；`propositionAction.tokens`會選取哪些專案。

### 顯示事件

當優惠方案顯示給使用者時，顯示事件通知Decisioning。 提供顯示專案的語彙基元，或省略`tokens`以增加`subPropositions`中所有專案的顯示計數器：

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionDisplay",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg", "ALlB5KV1B0e+CpHoahi7Ew"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### 互動（點按）事件

互動事件會追蹤使用者何時點按或參與顯示的選件。 您&#x200B;**必須**&#x200B;提供&#x200B;**正好一個**&#x200B;語彙基元，用來識別被點按的專案：

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionInteract",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "interact": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### 自訂事件

自訂事件使用客戶定義的`eventType` （任何非`decisioning.proposition<Display|Interact|Dismiss>`的值），並在`propositionEventType`中將所有`display`/`interact`/`dismiss`設定為`0` （分類為`OTHER`）。 自訂事件會像顯示事件（多重權杖篩選）一樣針對`subPropositions`進行解碼，並透過設定的PQL進行評估：

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "originalTimestamp": 1700000
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "add-to-cart",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 0, "interact": 0, "dismiss": 0 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

這些事件可啟用頻率限定、現成可用的報告，以及Decisioning中的AI驅動排名最佳化。 若要使用Web SDK傳送主張事件，請參閱[程式碼型體驗：決策實施](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations)。

## 端對端移轉程式 {#migration-process}

1. 驗證先決條件 — 在開始移轉之前，請確保您的目標沙箱已準備就緒，並且已識別所有先決條件相依性並準備就緒（設定檔屬性、區段ID、ID對應）。

1. 呼叫移轉API — 執行移轉API，使用您準備的先決條件和對應，將決策管理物件移轉至決策。

1. 草稿決定實體產生 — 工具會在每個實體對應的草稿狀態下建立行銷活動、決定政策、選擇策略、優惠專案等。 檢閱目標沙箱中所有產生的決策物件。 驗證命名、實體型別和參照是否正確。 尚無任何面向客戶的專案，決定管理會持續提供即時流量。

1. 更新使用者端與伺服器程式碼 — 實作必要的程式碼變更，以使用新的決策請求/回應格式，並使用必要的欄位實作事件追蹤。

1. 啟動和切換 — 啟動您的決定物件（策略、原則、行銷活動、表面），並在您自己的時間軸上從決定管理中轉移流量。

## 相關主題 {#related-topics}

* [從決定管理移轉至決定](migrate-to-decisioning.md) — 瞭解移轉至決定的優點與功能
* [開始使用決策](gs-experience-decisioning.md)
* [決策護欄和限制](decisioning-guardrails.md)
* [開始使用決策 API](api-reference/getting-started.md)