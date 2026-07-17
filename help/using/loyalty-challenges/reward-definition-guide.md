---
solution: Journey Optimizer
product: journey optimizer
title: 獎勵定義指南
description: 瞭解如何在Adobe Journey Optimizer中設定「忠誠度挑戰」獎勵提供者的獎勵定義。
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="私人測試版" type="Informative"
mini-toc-levels: 1
exl-id: 9b0fd9d8-18d1-4a51-8b6f-b2e2a4c6f1d7
feature_v2: []
subfeature_v2: []
source-git-commit: 00c24e9b97b4f6597048731858f3bfbcb39a0030
workflow-type: tm+mt
source-wordcount: 1206
ht-degree: 3%

---

# 獎勵定義指南 {#reward-definition-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_reward_definition"
>title="獎勵定義指南"
>abstract="使用本指南來設定忠誠度獎勵提供者的獎勵定義，包括預設定義行為和履行裝載欄位。"

>[!BEGINSHADEBOX]

**目錄**

[開始應對忠誠度挑戰](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**建立和管理挑戰**

* [存取及管理挑戰與工作](access-loyalty-challenges.md)
* [創造挑戰](create-challenges.md)
* [建立任務](create-tasks.md)
* [監視忠誠度挑戰績效](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**設定並整合**

* [設定忠誠度挑戰](loyalty-admin.md)
* **獎勵定義指南** ◀︎ **您在這裡**
* [事件轉換器指南](event-transformer-guide.md)
* [熟客資料與資料集](loyalty-data-and-datasets.md)
* [忠誠度挑戰API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中。 如需[!DNL Journey Optimizer]中發行週期與可用性階段的完整詳細資訊，請參閱[發行週期](../rn/releases.md)。

當挑戰任務、里程碑或挑戰完成&#x200B;**並設定了獎勵值**&#x200B;時，平台會呼叫您的獎勵提供者的HTTP端點並使用JSON裝載來發出獎勵。 **獎勵定義**&#x200B;說明問題的獎勵，並提供[JSONata](https://docs.jsonata.org/overview)運算式 — `rewardJsonata` — 以圖形化您的提供者所期望的確切裝載。

本指南涵蓋如何設定獎勵提供者、建立獎勵定義、撰寫`rewardJsonata`運算式，以及瞭解評估時可供使用的內容。

## 雙層模型

獎勵分為兩個層級：

```
Reward Provider  (endpoint, auth, headers)
└── Reward Definition  (denomination, rewardJsonata)
└── Reward Definition
└── ...
```

**獎勵提供者**&#x200B;代表單一外部獎勵系統 — 它包含傳遞端點URL、驗證及任何自訂HTTP標頭。 一個提供者可以保留多個&#x200B;**獎勵定義**，每個定義都描述該提供者提供的不同獎勵型別或面額（例如「50顆星」、「雙顆星」、「免費專案」）。

質詢會依據GUID參考提供者和定義。 當發出獎勵時，平台會評估定義的`rewardJsonata`運算式，並將結果POST至提供者的端點。

## 獎勵提供者與定義欄位

+++獎勵提供者欄位

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>欄位</th><th>類型</th><th>必要</th><th>說明</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>否（系統指派）</td><td>唯一識別碼。 唯讀。</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>是</strong></td><td>顯示名稱，組織內唯一。</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>無</td><td>提供者可讀取的說明。</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>無</td><td>當<code>false</code>時，已針對此提供者下的所有定義暫停<br>獎勵傳遞。</td></tr>
<tr><td><code>url</code></td><td><code>String</code></td><td><strong>是</strong></td><td>接收獎勵裝載的HTTP端點。<br>平台POST將評估過的<br><code>rewardJsonata</code>輸出傳至此URL。</td></tr>
<tr><td><code>additionalHeaders</code></td><td><code>Object</code></td><td>無</td><td>自訂HTTP標頭，可包含在每<br>個傳遞要求中（例如API金鑰、<br>內容型別覆寫）。</td></tr>
<tr><td><code>maxRatePerSecond</code></td><td><code>Integer</code></td><td>無</td><td>選擇性的每個提供者速率限制(1-5000)。<br>Null表示無限制。</td></tr>
<tr><td><code>enableMTLS</code></td><td><code>Boolean</code></td><td>無</td><td>端點是否需要雙向TLS。</td></tr>
</table>

+++

+++獎勵定義欄位

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>欄位</th><th>類型</th><th>必要</th><th>說明</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>否（系統指派）</td><td>唯一識別碼。 唯讀。</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>是</strong></td><td>顯示名稱，在提供者中唯一。</td></tr>
<tr><td><code>denomination</code></td><td><code>String</code></td><td>無</td><td>獎勵的單位，用於顯示<br>，可在運算式中作為<br><code>reward.denomination</code><br>使用（例如<code>"Stars"</code>、<code>"Points"</code>、<code>"Miles"</code>）。</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>無</td><td>獎勵的說明，可在運算式中以<code>reward.desc</code>形式取得<br>。</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>無</td><td>當<code>false</code>時，此定義為非使用中<br>且不會發出獎勵。</td></tr>
<tr><td><code>isDefault</code></td><td><code>Boolean</code></td><td>無</td><td>將此專案標籤為沙箱範圍的預設<br>獎勵定義。 所有提供者一次只能有一個定義<br>是預設值；<br>設定新的預設值會清除上一個定義。<br>用於在發佈時自動填入<br>個人化挑戰的獎勵詳細資料。</td></tr>
<tr><td><code>rewardJsonata</code></td><td><code>String</code></td><td><strong>是</strong></td><td>JSONata運算式在<br>獎勵問題時間評估。 接收完整<br>獎勵內容，且必須將JSON<br>裝載傳回至POST給提供者。</td></tr>
</table>

+++

## 獎勵內容

評估`rewardJsonata`時，它會收到包含獎勵事件所有已知內容的單一根物件。 運算式中的所有路徑都與此根相關。

```json
{
  "rewardContext": {
    "rewardValue": "50",
    "source":      "challenge"
  },
  "reward": {
    "name":         "500 Stars",
    "desc":         "Issue 500 Stars to the member",
    "denomination": "Stars",
    "enabled":      true
  },
  "task": { ... },
  "milestone": { ... },
  "challenge": { ... },
  "timestamp": "2026-02-10T00:29:22.538+00:00"
}
```

+++ 內容欄位

| 欄位 | 說明 |
|----------------------------------------|-------------|
| `rewardContext.rewardValue` | 在觸發此發行的挑戰、任務或里程碑上設定的獎勵值字串。 |
| `rewardContext.source` | 觸發獎勵的專案： `"task"`、`"challenge"`或`"milestone"`。 |
| `reward` | RewardDefinition本身 — `name`、`desc`、`denomination`。 |
| `task` | 完成的工作，包括其`accumulators`、`schedule`和`reward`。 |
| `task.accumulators.spend` | 任務累積的合格總支出。 |
| `task.accumulators.qty` | 任務累積的合格專案總數。 |
| `task.accumulators.item_list` | 套用至任務的所有合格專案。 每個專案都有`item`、`transactionId`、`timestamp`、`utcOffset`、`locationId`。 |
| `task.accumulators.item_list[-1]` | 最近套用的專案（JSONata負索引）。 對於取得最後一個交易ID或時間戳記非常有用。 |
| `task.schedule.currentStreak` | 目前的連續造訪連續計數（針對連續挑戰）。 |
| `task.schedule.currentVisits` | 造訪總數（針對造訪挑戰）。 |
| `milestone` | 觸發此獎勵的里程碑；若不是里程碑獎勵，則為`null`。 包含`count`和`reward.rewardValue`。 |
| `challenge.profileId` | 成員的熟客ID。 |
| `challenge.kvpCustom` | 在挑戰設定的自訂索引鍵值配對。 傳遞行銷活動ID、產品名稱或提供者專用中繼資料的常見模式。 |
| `challenge.name` | 挑戰名稱。 |
| `challenge._id` | 挑戰ID。 |
| `timestamp` | 獎勵簽發的ISO 8601時間戳記。 |

+++

## 撰寫rewardJsonata運算式

運算式會接收獎勵內容作為其輸入，且必須傳回JSON物件 — 裝載已對提供者的端點進行POST。 該物件的形狀完全取決於提供者的API；您可以將內容欄位對應到提供者期望的任何結構。

+++簡單固定裝載

最簡單的情況：提供者需要點數和成員ID，兩者都從內容中得知。

```jsonata
{
  "memberId":   challenge.profileId,
  "points":     $number(rewardContext.rewardValue),
  "currency":   reward.denomination
}
```

**輸出：**

```json
{
  "memberId": "ADB-0000030",
  "points":   50,
  "currency": "Stars"
}
```

> `rewardContext.rewardValue`永遠是字串。 如果您的提供者需要數值，請使用`$number()`進行轉換。

+++

+++針對提供者特定的中繼資料使用`kvpCustom`

提供者通常需要行銷活動ID或原始系統程式碼等欄位，這些欄位是每個挑戰執行所專屬。 編寫挑戰時將這些專案儲存在`challenge.kvpCustom`中，然後在運算式中參照它們 — 讓運算式可跨行銷活動重複使用。

```jsonata
{
  "memberId":         challenge.profileId,
  "points":           $number(rewardContext.rewardValue),
  "campaignId":       challenge.kvpCustom.campaignId,
  "transactionSource": "AJO"
}
```

您也可以將`reward.kvpCustom`用於固定特定獎勵型別（而非每個挑戰）的常數。

+++

+++使用工作累計器資料

任務累計器會儲存每個合格事件的記錄。 使用`item_list[-1]`存取最近套用的專案 — 其`transactionId`和`timestamp`對於提供者端的稽核追蹤和重複資料刪除很有用。

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "transactionId":  task.accumulators.item_list[-1].transactionId,
  "transactionDate": task.accumulators.item_list[-1].timestamp
}
```

+++

+++建構文字訊息

對於通知型提供者（Slack、簡訊、電子郵件），您可以使用JSONata的`&`串連運運算元直接建置訊息字串：

```jsonata
{
  "text": "You just earned " & rewardContext.rewardValue & " " & reward.denomination & "!"
}
```

**輸出：**

```json
{
  "text": "You just earned 50 Stars!"
}
```

+++

## 範例

+++範例1 — 簡單點提供者

**案例：**&#x200B;基本熟客點數API需要會員ID與點數。

**獎勵定義：**

```json
{
  "name":         "Standard Points",
  "denomination": "Points",
  "desc":         "Award loyalty points",
  "enabled":      true,
  "rewardJsonata": "{\"memberId\": challenge.profileId, \"pointQuantity\": $number(rewardContext.rewardValue), \"denomination\": reward.denomination}"
}
```

**格式化運算式：**

```jsonata
{
  "memberId":      challenge.profileId,
  "pointQuantity": $number(rewardContext.rewardValue),
  "denomination":  reward.denomination
}
```

**裝載張貼至提供者：**

```json
{
  "memberId":      "ADB-0000030",
  "pointQuantity": 50,
  "denomination":  "Points"
}
```

+++

+++範例2 — 包含行銷活動中繼資料的提供者裝載

**案例：**&#x200B;提供者需要包含稽核欄位、行銷活動參照和成員說明的結構化獎勵記錄。 行銷活動特定值儲存在`challenge.kvpCustom`中，因此相同的獎勵定義可在行銷活動間運作，而不需編輯運算式。

**挑戰`kvpCustom`** （在編寫挑戰時設定）：

```json
{
  "parentCampaignId": "CAMP-2026-Q1",
  "productName":      "Loyalty Program"
}
```

**獎勵定義：**

```json
{
  "name":         "Stars — Campaign Award",
  "denomination": "Stars",
  "desc":         "Issue Stars for completing a qualifying purchase",
  "enabled":      true,
  "rewardJsonata": "{\"awardPoints\":[{\"idType\":\"externalId\",\"id\":challenge.profileId,\"transactionId\":task.accumulators.item_list[-1].transactionId,\"transactionDate\":task.accumulators.item_list[-1].timestamp,\"originalTransactionId\":task.accumulators.item_list[-1].transactionId,\"transactionSource\":\"AJO\",\"channelSource\":\"Web\",\"parentCampaignId\":challenge.kvpCustom.parentCampaignId,\"productName\":challenge.kvpCustom.productName,\"memberAwardDescription\":reward.desc,\"pointQuantity\":$number(rewardContext.rewardValue)}]}"
}
```

**格式化運算式：**

```jsonata
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    challenge.profileId,
      "transactionId":         task.accumulators.item_list[-1].transactionId,
      "transactionDate":       task.accumulators.item_list[-1].timestamp,
      "originalTransactionId": task.accumulators.item_list[-1].transactionId,
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      challenge.kvpCustom.parentCampaignId,
      "productName":           challenge.kvpCustom.productName,
      "memberAwardDescription": reward.desc,
      "pointQuantity":         $number(rewardContext.rewardValue)
    }
  ]
}
```

**裝載張貼至提供者：**

```json
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    "ADB-0000030",
      "transactionId":         "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionDate":       "2026-02-08T00:12:00.000+00:00",
      "originalTransactionId": "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      "CAMP-2026-Q1",
      "productName":           "Loyalty Program",
      "memberAwardDescription": "Issue Stars for completing a qualifying purchase",
      "pointQuantity":         50
    }
  ]
}
```

+++

+++範例3 — 里程碑獎勵

**案例：** Streak挑戰會每隔N次造訪發出里程碑獎勵。 運算式包含里程碑計數以及提供者端內容的目前連結。

**格式化運算式：**

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "milestoneCount": milestone.count,
  "currentStreak":  task.schedule.currentStreak,
  "denomination":   reward.denomination,
  "source":         rewardContext.source
}
```

**裝載已發佈至提供者** （在第2次造訪里程碑時）：

```json
{
  "memberId":       "ADB-0000030",
  "points":         20,
  "milestoneCount": 2,
  "currentStreak":  2,
  "denomination":   "Stars",
  "source":         "milestone"
}
```

> 當`rewardContext.source`為`"milestone"`時，`milestone`物件會填入`count`和`reward.rewardValue`。 當來源是`"task"`或`"challenge"`時，`milestone`是`null`。

+++

## API 參考

+++獎勵提供者

```http
POST   /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers/{providerId}
PUT    /loyalty/metadata/config/rewards/providers/{providerId}
DELETE /loyalty/metadata/config/rewards/providers/{providerId}
```

所有要求都需要`x-gw-ims-org-id`和`x-sandbox-name`標頭。

**建立提供者：**

```http
POST /loyalty/metadata/config/rewards/providers
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":    "My Points Provider",
  "desc":    "Issues loyalty points via REST",
  "enabled": true,
  "url":     "https://rewards.example.com/award",
  "additionalHeaders": {
    "x-api-key": "YOUR_API_KEY"
  }
}
```

+++

+++獎勵定義

```http
POST   /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
PUT    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
DELETE /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
```

**建立獎勵定義：**

```http
POST /loyalty/metadata/config/rewards/definitions/{providerId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":         "50 Stars",
  "denomination": "Stars",
  "desc":         "Award 50 Stars on task completion",
  "enabled":      true,
  "rewardJsonata": "{ \"memberId\": challenge.profileId, \"points\": $number(rewardContext.rewardValue) }"
}
```

+++

## 運算式驗證

`rewardJsonata`運算式已在發佈時針對語法進行驗證。 如果運算式無效，API會傳回`422`錯誤，其中包含剖析失敗的描述。

若要在發佈之前開發和測試運算式，請使用[JSONata Exerciser](https://try.jsonata.org/)。 將獎勵內容JSON貼上為輸入檔案和您的運算式，以驗證輸出符合您的提供者期望。 每個觸發程式型別(`task`、`milestone`、`challenge`)的代表性獎勵內容會顯示在上面的範例中。

## 常見錯誤

| 錯誤 | 效果 | 修正 |
|---------|--------|-----|
| `rewardContext.rewardValue`已用為數字但未轉換 | 如果提供者驗證欄位為數值，則型別不符 | 以`$number(rewardContext.rewardValue)`換行 |
| `challenge.kvpCustom.someKey`傳回null | 編寫時挑戰未設定金鑰 | 確保在使用這個定義的每個挑戰上`kvpCustom`中都存在金鑰 |
| `task.accumulators.item_list[-1]`為null | 未套用任何專案後才簽發獎勵（非購買事件） | 以條件式保全，或改用內容中的`timestamp` |
| `milestone`在來源為`"task"`或`"challenge"`時存取 | `milestone`為空；運算式擲回或產生null欄位 | 存取`milestone`前請先檢查`rewardContext.source`，或僅在附加至里程碑獎勵的定義中使用`milestone` |
| 運算式傳回陣列而非物件 | 提供者接收未預期的裝載結構 | 在外部物件中換行傳回陣列的運算式： `{ "items": [...] }` |
