---
title: 批次決策 API
description: 瞭解如何使用批次決策API ，在預先定義的決策範圍內為對象的設定檔選取最佳選件。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 3%

---


# 使用[!DNL Batch Decisioning] API傳遞優惠方案 {#deliver-offers-batch}

[!DNL Batch Decisioning] API可讓組織在一次呼叫中對特定對象中的所有設定檔使用決策功能。 對象中每個設定檔的選件內容都會放在Adobe Experience Platform資料集中，可用於自訂批次工作流程。

透過[!DNL Batch Decisioning] API，您可以在資料集中填入決策範圍之Adobe Experience Platform對象中所有設定檔的最佳選件。 例如，某個組織可能想要執行[!DNL Batch Decisioning]，以便傳送優惠給訊息傳遞廠商。 然後，這些選件會用作傳送給相同使用者對象以進行批次訊息傳送的內容。

為此，組織將：

* 執行[!DNL Batch Decisioning] API，其中包含兩個要求：

   1. **批次POST要求**，用以啟動工作負載，以批次處理選件選擇。

   2. **批次GET請求**&#x200B;以取得批次工作負載狀態。

* 將資料集匯出至訊息傳送供應商API。

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html) to learn more about exporting audiences.) -->

>[!NOTE]
>
>也可以使用Journey Optimizer介面執行批次決策。 如需詳細資訊，請參閱[本節](../../batch-delivery.md)，其中提供在使用批次決定時，要考慮的全域必要條件和限制的相關資訊。

* **每個資料集執行中的批次工作數目**：每個資料集一次最多可以執行五個批次工作。 具有相同輸出資料集的任何其他批次請求都會新增至佇列。 擷取已排入佇列的工作，以便在前一個工作執行完畢後進行處理。
* **頻率限定**：批次會在一天中執行一次設定檔快照。 [!DNL Batch Decisioning] API會限制頻率，並一律從最近的快照載入設定檔。

## 快速入門 {#getting-started}

使用此API之前，請務必完成下列必要步驟。

### 準備決定 {#prepare-decision}

若要準備一或多個決定，請確定您已建立資料集、對象和決定。 這些先決條件在[本節](../../batch-delivery.md)中有詳細說明。

### API需求 {#api-requirements}

除了[!DNL Batch Decisioning]決定管理API開發人員指南[中參考的標頭外，所有](../getting-started.md)要求都需要下列標頭：

* `Content-Type`：`application/json`
* `x-request-id`：識別要求的唯一字串。
* `x-sandbox-name`：沙箱名稱。

## 開始批次處理 {#start-a-batch-process}

若要啟動工作負載以批次處理決定，請對`/workloads/decisions`端點發出POST請求。

>[!NOTE]
>
>有關批次工作處理時間的詳細資訊，請參閱[此區段](../../batch-delivery.md)。

**API格式**

```https
POST {ENDPOINT_PATH}/workloads/decisions
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/dwm` |

**要求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dwm/workloads/decisions' \
-H 'x-request-id: f671a589-eb7b-432f-b6b9-23d5b796b4dc' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-d '{
  "xdm:segmentIds": [
    "609028e4-e66c-4776-b0d9-c782887e2273"
  ],
  "xdm:dataSetId": "6196b4a1a63bd118dafe093c",
  "xdm:propositionRequests": [
        {
            "xdm:activityId": "xcore:offer-activity:1410cdcda196707b",
            "xdm:placementId": "xcore:offer-placement:1410c4117306488a",
            "xdm:itemCount": 1
        }
  ],
  "xdm:includeContent": false
}'
```

| 屬性 | 說明 | 範例 |
| -------- | ----------- | ------- |
| `xdm:activityId` | 決定的唯一識別碼。 |  |
| `xdm:dataSetId` | 可寫入決定事件的輸出資料集。 | `6196b4a1a63bd118dafe093c` |
| `xdm:includeContent` | 這是選擇性欄位，預設為`false`。 如果`true`，則選件內容會包含在資料集的決定事件中。 | `false` |
| `xdm:itemCount` | 此選擇性欄位會顯示專案數量，例如為決定範圍要求的選項。 依預設，API會針對每個範圍傳回一個選項，但您可以指定此欄位以明確要求更多選項。 每個範圍最多可請求30個選項，最少為1個。 | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | 唯一位置識別碼。 | `xcore:offer-placement:1410c4117306488a` |
| `xdm:propositionRequests` | 包含`placementId`和`activityId`的包裝函式 |  |
| `xdm:segmentIds` | 值是包含對象唯一識別碼的陣列。 它只能包含一個值。 | `609028e4-e66c-4776-b0d9-c782887e2273` |

請參閱[決定管理檔案](../../get-started/starting-offer-decisioning.md)，以取得主要概念和屬性的概觀。

**回應**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| 屬性 | 說明 | 範例 |
| -------- | ----------- | ------- |
| `@id` | 決策管理產生的UUID，用於識別單一工作負載。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 組織識別碼。 | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | 決定工作負載請求的建立時間。 | `1648078924834` |
| `ode:status` | 工作負載的狀態。 | `ode:status: "QUEUED"` |

## 擷取批次決定的資訊 {#retrieve-information-on-a-batch-decision}

若要擷取特定決定的資訊，請對`/workloads/decisions`端點提出GET要求，同時為您的決定提供對應的工作負載ID值。

**API格式**

```https
GET {ENDPOINT_PATH}/workloads/decisions/{WORKLOAD_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/dwm` |
| `{WORKLOAD_ID}` | 決策管理產生的UUID，用於識別單一工作負載。 | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dwm/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
-H 'x-request-id: 7832a42a-d4e5-413b-98e8-e49bef056436' \
-H 'Content-Type: application/json' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H'x-sandbox-id: {SANDBOX_ID}' \
-H 'Authorization: Bearer {ACCESS_TOKEN}'
```

**回應**

```json
{
   "@id": "f395ab1f-dfaf-48d4-84c9-199ad6354591",
    "xdm:imsOrgId": "{IMS_ORG}",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| 屬性 | 說明 | 範例 |
| -------- | ----------- | ------- |
| `@id` | 決策管理產生的UUID，用於識別單一工作負載。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 組織ID | `9GTO98D5F@AdobeOrg` |
| `ode:createDate` | 決定工作負載請求的建立時間。 | `1648076994405` |
| `ode:status` | 工作負荷的狀態從「已排入佇列」開始，並變更為「處理中」、「正在擷取」、「已完成」或「錯誤」。 | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | 如果狀態為「正在處理」或「正在擷取」，這會顯示更多詳細資料，例如sparkJobId和batchID。 如果狀態為「ERROR」，則顯示錯誤詳細資料。 |  |

## 後續步驟 {#next-steps}

依照此API指南，您已使用[!DNL [!DNL Batch Decisioning]] API檢查工作負荷狀態和傳遞的選件。 如需詳細資訊，請參閱決策管理[的](../../get-started/starting-offer-decisioning.md)概觀。
