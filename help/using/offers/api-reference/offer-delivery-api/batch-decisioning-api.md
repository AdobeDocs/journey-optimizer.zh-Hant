---
title: 批次決策 API
description: 瞭解如何使用批處理決策API為預定義決策範圍內的分段配置檔案選擇最佳優惠。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 3%

---


# 使用 [!DNL Batch Decisioning] API {#deliver-offers-batch}

的 [!DNL Batch Decisioning] API允許組織在一次調用中對給定段中的所有配置檔案使用offer decisioning功能。 段中每個配置檔案的提供內容都放在Adobe Experience Platform資料集中，在該資料集中可用於自定義批處理工作流。

使用 [!DNL Batch Decisioning] API，您可以使用針對決策範圍的Adobe Experience Platform段中所有配置檔案的最佳優惠來填充資料集。 例如，組織可能希望運行 [!DNL Batch Decisioning] 這樣他們就可以向消息傳遞供應商發送報價。 然後，這些優惠將用作發送給同一用戶段的批消息傳遞的內容。

為此，該組織將：

* 運行 [!DNL Batch Decisioning] API，它包含兩個請求：

   1. A **批POST請求** 啟動工作量以批處理提供選擇。

   2. A **批GET請求** 獲取批處理工作量狀態。

* 將資料集導出到消息傳遞供應商API。

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

>[!NOTE]
>
>批量判定也可使用Journey Optimizer介面執行。 有關詳細資訊，請參閱 [此部分](../../batch-delivery.md)，它提供有關使用批決策時要考慮的全局先決條件和限制的資訊。

* **每個資料集正在運行的批處理作業數**:每個資料集一次最多可運行五個批處理作業。 具有相同輸出資料集的任何其他批處理請求都會添加到隊列。 已排隊的作業在前一作業完成運行後被拾取處理。
* **頻率封蓋**:批處理將運行每天發生一次的配置檔案快照。 的 [!DNL Batch Decisioning] API會限制頻率，並始終從最近的快照載入配置檔案。

## 快速入門 {#getting-started}

使用此API之前，請確保完成以下必備步驟。

### 準備決定 {#prepare-decision}

要準備一個或多個決策，請確保已建立資料集、段和決策。 這些先決條件詳見 [此部分](../../batch-delivery.md)。

### API要求 {#api-requirements}

全部 [!DNL Batch Decisioning] 除了在 [決策管理API開發人員指南](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`:標識請求的唯一字串。
* `x-sandbox-name`:沙盒名稱。
* `x-sandbox-id`:沙盒ID。

## 啟動批處理 {#start-a-batch-process}

要啟動工作量以批處理決策，請向 `/workloads/decisions` 端點。

>[!NOTE]
>
>有關批處理作業處理時間的詳細資訊，請參閱 [此部分](../../batch-delivery.md)。

**API格式**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的終結點路徑。 | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**要求**

```shell
curl -X POST 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions' \
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
| `xdm:segmentIds` | 值是包含段的唯一標識符的陣列。 它只能包含一個值。 | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | 輸出資料設定可以寫入決策事件的資料。 | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | 包含 `placementId` 和 `activityId` |  |
| `xdm:activityId` | 決策的唯一標識符。 | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | 唯一的放置標識符。 | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | 這是一個可選欄位，顯示為決策範圍請求的選項等項數。 預設情況下，API會為每個範圍返回一個選項，但可以通過指定此欄位來顯式請求更多選項。 每個範圍最少可請求1個選項，最多可請求30個選項。 | `1` |
| `xdm:includeContent` | 這是可選欄位， `false` 預設值。 如果 `true`在資料集的決策事件中包含了服務內容。 | `false` |

請參閱 [決策管理文檔](../../get-started/starting-offer-decisioning.md) 的子菜單。

**回應**

```json
{
    "@id": "47efef25-4bcf-404f-96e2-67c4f784a1f5",
    "xdm:imsOrgId": "9GTO98D5F@AdobeOrg",
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648078924834,
    "ode:status": "QUEUED"
}
```

| 屬性 | 說明 | 範例 |
| -------- | ----------- | ------- |
| `@id` | 由標識單個工作負載的Offer decisioning生成的UUID。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 組織ID。 | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 容器ID。 | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 建立決策工作量請求的時間。 | `1648078924834` |
| `ode:status` | 工作負荷的狀態。 | `ode:status: "QUEUED"` |

## 檢索有關批決策的資訊 {#retrieve-information-on-a-batch-decision}

要檢索有關特定決策的資訊，請向 `/workloads/decisions` 端點，同時為您的決策提供相應的工作負荷ID值。

**API格式**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 儲存庫API的終結點路徑。 | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | 由標識單個工作負載的Offer decisioning生成的UUID。 | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

**要求**

```shell
curl -X GET 'https://platform.adobe.io/data/core/ode/0948b1c5-fff8-3b76-ba17-909c6b93b5a2/workloads/decisions/f395ab1f-dfaf-48d4-84c9-199ad6354591' \
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
    "xdm:containerId": "0948b1c5-fff8-3b76-ba17-909c6b93b5a2",
    "ode:createDate": 1648076994405,
    "ode:status": "COMPLETED"
}
```

| 屬性 | 說明 | 範例 |
| -------- | ----------- | ------- |
| `@id` | 由標識單個工作負載的Offer decisioning生成的UUID。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 組織ID | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 容器ID | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 建立決策工作量請求的時間。 | `1648076994405` |
| `ode:status` | 工作負荷的狀態以「QUEUED」開頭，並更改為「PROCESSING」、「INGESTING」、「COMPLETED」或「ERROR」。 | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | 如果狀態為「PROCESSING」或「INGESTING」，則顯示sparkJobId和batchID等詳細資訊。 如果狀態為「ERROR（錯誤）」，則顯示錯誤詳細資訊。 |  |

## 後續步驟 {#next-steps}

按照本API指南，您已使用[!DNL]檢查了工作負載狀態並提供了服務 [!DNL Batch Decisioning]] API。 有關詳細資訊，請參見 [決策管理概述](../../get-started/starting-offer-decisioning.md)。
