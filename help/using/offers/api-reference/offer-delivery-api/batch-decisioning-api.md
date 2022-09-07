---
title: 批次決策 API
description: 了解如何使用Batch Decisioning API為預先定義的決策範圍內的分段設定檔選取最佳選件。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1ed01a6b-5e42-47c8-a436-bdb388f50b4e
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 3%

---


# 使用 [!DNL Batch Decisioning] API {#deliver-offers-batch}

此 [!DNL Batch Decisioning] API可讓組織對單一呼叫中指定區段中的所有設定檔使用決策功能。 區段中每個設定檔的選件內容會放置於Adobe Experience Platform資料集中，供自訂批次工作流程使用。

使用 [!DNL Batch Decisioning] API，您可以為資料集填入Adobe Experience Platform區段中所有設定檔的最佳選件，以供決策範圍使用。 例如，組織可能想要執行 [!DNL Batch Decisioning] 以便他們能將選件傳送給訊息傳送廠商。 然後，這些選件會作為內容，傳送出去以批次傳送訊息給相同的使用者區段。

為此，本組織將：

* 執行 [!DNL Batch Decisioning] API，包含兩個請求：

   1. A **批次POST請求** 啟動工作量以批處理選件選擇。

   2. A **批次GET請求** 獲取批工作量狀態。

* 將資料集匯出至訊息傳送廠商API。

<!-- (Refer to the [export jobs endpoint documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/export-jobs.html?lang=en) to learn more about exporting segments.) -->

>[!NOTE]
>
>批次決策也可使用Journey Optimizer介面來執行。 如需詳細資訊，請參閱 [本節](../../batch-delivery.md)，提供使用批次決策時需考量的全域先決條件和限制資訊。

* **每個資料集正在運行的批處理作業數**:每個資料集一次最多可執行5個批次作業。 具有相同輸出資料集的任何其他批次請求都會新增至佇列。 系統會擷取已排入佇列的作業，以在上一個作業完成執行後進行處理。
* **頻率限定**:批次會關閉每天發生一次的設定檔快照。 此 [!DNL Batch Decisioning] API會將頻率設為上限，並一律從最新的快照載入設定檔。

## 快速入門 {#getting-started}

使用此API之前，請務必完成下列必要步驟。

### 準備決定 {#prepare-decision}

若要準備一或多個決策，請確定您已建立資料集、區段和決策。 若需了解這些必要條件，請參閱 [本節](../../batch-delivery.md).

### API需求 {#api-requirements}

全部 [!DNL Batch Decisioning] 除了 [Decision Management API開發人員指南](../getting-started.md):

* `Content-Type`: `application/json`
* `x-request-id`:識別請求的唯一字串。
* `x-sandbox-name`:沙箱名稱。
* `x-sandbox-id`:沙箱ID。

## 啟動批處理 {#start-a-batch-process}

要啟動工作量以批次處理決策，請向 `/workloads/decisions` 端點。

>[!NOTE]
>
>有關批處理作業處理時間的詳細資訊，請參閱 [本節](../../batch-delivery.md).

**API格式**

```https
POST {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/ode` |
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
| `xdm:segmentIds` | 值是包含區段唯一識別碼的陣列。 它只能包含一個值。 | `609028e4-e66c-4776-b0d9-c782887e2273` |
| `xdm:dataSetId` | 輸出資料設定決策事件可寫入中。 | `6196b4a1a63bd118dafe093c` |
| `xdm:propositionRequests` | 包裝包含 `placementId` 和 `activityId` |  |
| `xdm:activityId` | 決策的唯一識別碼。 | `xcore:offer-activity:1410cdcda196707b` |
| `xdm:placementId` | 唯一版位識別碼。 | `xcore:offer-placement:1410c4117306488a` |
| `xdm:itemCount` | 這是選用欄位，顯示決策範圍所請求的選項等項目數。 依預設，API會針對每個範圍傳回一個選項，但您可以指定此欄位，明確要求更多選項。 每個範圍最少可請求1個選項，最多可請求30個選項。 | `1` |
| `xdm:includeContent` | 這是選用欄位，是 `false` 依預設。 若 `true`，則選件內容會包含在資料集的決策事件中。 | `false` |

請參閱 [決策管理檔案](../../get-started/starting-offer-decisioning.md) ，以了解主要概念和屬性的概觀。

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
| `@id` | 由決策管理生成的UUID，用於標識單個工作負載。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 組織ID。 | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 容器ID。 | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 建立決策工作量請求的時間。 | `1648078924834` |
| `ode:status` | 工作負載的狀態。 | `ode:status: "QUEUED"` |

## 檢索有關批決策的資訊 {#retrieve-information-on-a-batch-decision}

若要擷取特定決策的資訊，請向 `/workloads/decisions` 端點，同時為您的決策提供相應的工作量ID值。

**API格式**

```https
GET  {ENDPOINT_PATH}/{CONTAINER_ID}/workloads/decisions/{WORKLOAD_ID}
```

| 參數 | 說明 | 範例 |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | 存放庫API的端點路徑。 | `https://platform.adobe.io/data/core/ode` |
| `{CONTAINER_ID}` | 決策所在的容器。 | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{WORKLOAD_ID}` | 由決策管理生成的UUID，用於標識單個工作負載。 | `47efef25-4bcf-404f-96e2-67c4f784a1f5` |

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
| `@id` | 由決策管理生成的UUID，用於標識單個工作負載。 | `5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8` |
| `xdm:imsOrgId` | 組織ID | `9GTO98D5F@AdobeOrg` |
| `xdm:containerId` | 容器ID | `0948b1c5-fff8-3b76-ba17-909c6b93b5a2` |
| `ode:createDate` | 建立決策工作量請求的時間。 | `1648076994405` |
| `ode:status` | 工作負載的狀態以「QUEUED」開始，並更改為「PROCESSING」、「INGESTING」、「COMPLETED」或「ERROR」。 | `ode:status: "COMPLETED"` |
| `ode:statusDetail` | 如果狀態為「PROCESSING」或「INGESTING」，則會顯示sparkJobId和batchID等更多詳細資訊。 如果狀態為「ERROR」，則會顯示錯誤詳細資訊。 |  |

## 後續步驟 {#next-steps}

依照本API指南，您已使用[!DNL]檢查工作負載狀態並傳送選件 [!DNL Batch Decisioning]] API。 如需詳細資訊，請參閱 [決策管理概述](../../get-started/starting-offer-decisioning.md).
