---
title: Decisioning移轉API
description: 瞭解如何使用決策移轉服務API，透過自動化相依性解析和復原支援，在沙箱之間移轉決策管理物件。
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
source-git-commit: 398d4c2ab3a2312a0af5b8ac835f7d1f49a61b5b
workflow-type: tm+mt
source-wordcount: '1154'
ht-degree: 3%

---


# Decisioning移轉API {#decisioning-migration-api}

決策移轉服務API可讓您將決策管理物件從一個沙箱移轉至另一個沙箱。 移轉程式會以非同步工作流程執行，其中包含相依性分析、執行和選用的復原功能。

此API可讓您在環境之間（例如，從開發到測試，或從測試到生產）順暢地轉換決策內容，同時維護資料完整性和關係。

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

## API 基本概念 {#api-basics}

### 基本URL {#base-urls}

根據您的環境使用下列基底URL：

* **生產**： `https://platform.adobe.io`
* **暫存**： `https://platform-stage.adobe.io`

### Authentication {#authentication}

所有API請求都需要以下標頭：

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `x-api-key: <CLIENT_API_KEY>`
* `Content-Type: application/json`

如需設定驗證的詳細指示，請參閱[Journey Optimizer驗證指南](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}。

### 工作流程模型 {#workflow-model}

每個API呼叫都會建立或擷取工作流程資源。 工作流程是非同步操作，可追蹤移轉工作的進度和結果。

工作流程有下列屬性：

* `id` — 唯一的工作流程識別碼(UUID)
* `status` — 目前的工作流程狀態： `New`、`Running`、`Completed`、`Failed`或`Cancelled`
* `result` — 完成時的工作流程輸出（包含移轉結果和警告）
* `errors` — 失敗時的結構化錯誤詳細資料
* `_etag` — 用於刪除作業的版本識別碼（僅限服務使用者）
* `_links.self` — 擷取狀態的工作流程URL

## 移轉工作流程 {#migration-workflow}

移轉程式包含兩個主要步驟：分析相依性並執行移轉。 請依照下列步驟操作，以確保成功移轉。

### 步驟1：分析相依性 {#analyze-dependencies}

在移轉之前，請使用相依性工作流程來識別需要在目標沙箱中從決定管理對應到決定的專案。 此分析可協助您瞭解物件之間的關係，並準備必要的對應。

#### 建立相依性工作流程 {#create-dependency-workflow}

使用以下API呼叫建立相依性分析工作流程。

**API格式**

```http
POST /migration/service/dependency
```

**沙箱層級相依性（建議優先）**

從沙箱層級分析開始，以取得所有相依性的完整檢視：

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/dependency" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**選件層級相依性**

若要只分析特定選件的相依性，請設定`requestLevel: "offer"`並提供具有您要分析之選件ID的`offersList`陣列。

**決定層級相依性**

若要只分析特定決定的相依性，請設定`requestLevel: "decision"`並提供包含您要分析之決定ID的`decisionsList`陣列。

#### 檢查相依性工作流程狀態 {#poll-dependency-status}

輪詢相依性工作流程以檢查分析何時完成。

**API格式**

```http
GET /migration/service/dependency/{id}
```

**要求**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/dependency/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

當`status`欄位顯示`Completed`時，相依性分析已準備就緒。 使用工作流程輸出建置您的移轉相依性對應：

* **profileAttributeDependency** — 將來源設定檔屬性對應到目標設定檔屬性
* **contextAttributeDependency** — 將來源內容屬性對應至目標內容屬性
* **segmentsDependency** — 將來源區段索引鍵對應到目標區段識別碼(`{segmentNamespace, segmentId}`)
* **datasetName** — 指定移轉的目標資料集名稱

### 步驟2：執行移轉 {#execute-migration}

分析相依性並準備對應後，您就可以執行移轉。

#### 建立移轉工作流程 {#create-migration-workflow}

使用步驟1的相依性對應來設定並執行您的移轉。

**API格式**

```http
POST /migration/service/migrations
```

**沙箱層級移轉**

若要將所有決策物件從一個沙箱移轉至另一個沙箱：

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/migrations" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributeDependency": {
        "sourceAttr1": "targetAttr1"
      },
      "segmentsDependency": {
        "sourceSegmentKey1": {
          "segmentNamespace": "<TARGET_SEGMENT_NAMESPACE>",
          "segmentId": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributeDependency": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    },
    "requestLevel": "sandbox"
  }'
```

**選件層級移轉**

若要僅移轉特定優惠方案，請使用`requestLevel: "offer"`並新增`offersList`陣列：

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**決策層級移轉**

若要僅移轉特定決定，請使用`requestLevel: "decision"`並新增`decisionsList`陣列：

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### 監視移轉狀態 {#poll-migration-status}

輪詢移轉工作流程以追蹤其進度。

**API格式**

```http
GET /migration/service/migrations/{id}
```

**要求**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/migrations/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

**移轉結果**

當`status`欄位顯示`Completed`時，移轉已成功。 工作流程`result`包含：
* 已移轉物件的對應
* 移轉期間遇到的任何警告

當`status`欄位顯示`Failed`時，請檢閱`errors[]`陣列和`result.error`欄位以取得有關所發生問題的詳細資訊。

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
POST /migration/service/rollbacks/{migrationWorkflowId}
```

將`{migrationWorkflowId}`取代為您要復原的移轉工作流程識別碼。

**要求**

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/rollbacks/<MIGRATION_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

### 監視復原狀態 {#poll-rollback-status}

輪詢復原工作流程以追蹤其進度。

**API格式**

```http
GET /migration/service/rollbacks/{rollbackWorkflowId}
```

**要求**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/rollbacks/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

## 處理並行工作流程 {#handle-concurrency}

移轉API一次只允許每個組織執行一個工作流程。 如果您嘗試在另一個工作流程進行中時建立新工作流程，您將會收到&#x200B;**409衝突**&#x200B;錯誤回應（「工作流程已在進行中……」）。

在這種情況下，請等待進行中的工作流程完成，或擷取工作流程ID並輪詢其狀態。 目前的工作流程完成後，您可以建立一個新的工作流程。

## 實體對應參考 {#entity-mapping}

從決定管理移轉至Decisioning時，實體對應如下：

| 決策管理 | 決策 |
|-------------------|-------------|
| 產品建議 | 決定專案 |
| 優惠收藏 | 專案集合 |
| 適用性規則 | 適用性規則 |
| 排名公式 | 排名公式 |
| 決定 | 選擇策略+決定策略 |
| Campaign | 行銷活動&#x200B;*（僅限基本內容）* |
| 刊登 | 表面+頻道設定 |
| 標記 | 統一標籤 |

## 工作流程清理 {#cleanup}

工作流程資源只能由服務使用者刪除。 刪除作業需要具有工作流程`If-Match`值的`_etag`標頭。

**可用的刪除作業：**

* `DELETE /migration/service/dependency/{id}`
* `DELETE /migration/service/migrations/{id}`
* `DELETE /migration/service/rollbacks/{id}`

>[!NOTE]
>
>只有具有適當許可權的服務帳戶才能刪除工作流程。 如果您需要刪除工作流程資源，請聯絡您的系統管理員。

## 相關主題 {#related-topics}

* [從決定管理移轉至決定](migrate-to-decisioning.md) — 瞭解移轉至決定的優點與功能
* [開始使用決策](gs-experience-decisioning.md)
* [決策護欄和限制](decisioning-guardrails.md)
* [開始使用決策 API](api-reference/getting-started.md)
