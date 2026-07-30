---
product: journey optimizer
title: inAudience 函式
description: 瞭解Adobe Experience Platform inAudience函式
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience，函式，運算式，歷程，對象，細分
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DU8HtduB2-GmakiaHBMFU1vzBBPoVTNvrOCPWQrr5SU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1279
ht-degree: 1%

---

# inAudience 函式 {#inAudience}

`inAudience`函式是Adobe Experience Platform函式，可讓您檢查歷程中的個人是否屬於特定對象。 這項強大的功能可讓您根據對象成員資格建立個人化的歷程路徑，在您的客戶體驗中啟用複雜的細分和目標定位。

當您需要以下動作時，請使用`inAudience`函式：

* 根據對象成員資格的分支歷程路徑。 [了解更多](../conditions.md#using-a-segment)
* 套用取決於設定檔是否屬於特定區段的條件式邏輯
* 使用個人化體驗鎖定特定的客戶群組
* 評估歷程條件中的即時受眾參與率
* 結合多個對象檢查以建立複雜的目標規則

函式會即時評估對象成員資格並傳回布林值，使其非常適合用於決策節點和條件運算式。 對象是在[Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"}中定義和管理的（深入瞭解[在Journey Optimizer中使用對象](../../audience/about-audiences.md)），運算式編輯器會提供自動完成建議，協助您正確參考對象。

**對象狀態：**

對象可以有兩種參與狀態：

* **已實現**：該個人符合對象定義的資格且是作用中成員
* **已退出**：個人已離開對象，不再符合資格

只有狀態為&#x200B;**已實現**&#x200B;的個人才會被視為作用中對象成員。 函式傳回`true`時，會確認個人已實現狀態；傳回`false`時，會表示已結束狀態。 如需對象評估的詳細資訊，請參閱[Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}。

+++語法

`inAudience(<parameter>)`

+++

+++參數

| 參數 | 說明 | 類型 |
|--- |--- |--- |
| 客群 | 對象名稱 | `<string>` |

**重要限制：**

* 對象名稱必須是字串常數
* 不能是欄位參考或運算式
* 您可在單一歷程中擷取最多100個對象

+++

+++簽章與傳回的型別

`inAudience(<string>)`

傳回布林值：
* `true`：個人是對象的成員（已實現狀態）

* `false`：個人不是對象的成員（退出狀態）

+++

+++範例

`inAudience("men over 50")`

如果歷程執行個體中的個人屬於名為「50歲以上的男性」的Adobe Experience Platform對象，則傳回&#x200B;**true**，否則傳回&#x200B;**false**。

**實際使用案例：**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## 護欄與限制 {#guardrails}

在您的歷程中使用`inAudience`函式時，請注意下列護欄和限制：

**對象擷取限制：**
* 您可在單一歷程中擷取最多100個對象
* 運算式編輯器提供自動完成的可用對象清單，可幫助您正確參考這些對象

**引數條件約束：**
* 對象名稱必須是字串常數
* 欄位參考和運算式不支援做為引數

**對象名稱變更：**
* 變更Adobe Experience Platform中現有對象的名稱時，不會自動更新歷程運算式中對該對象的任何參照
* 如果您的條件節點使用`inAudience('oldAudienceName')`，您必須手動編輯運算式以使用新名稱
* 若未更新對象名稱，將會導致歷程條件中斷，並可能導致錯誤的歷程行為

**合併原則考量事項：**
* 透過`inAudience`函式使用多個對象時，合併原則不一致會導致錯誤或警示
* 如需合併原則行為的詳細資訊，請參閱[歷程屬性](../journey-properties.md)

**傳播時間：** {#propagation-timing}

在條件節點中使用`inAudience()`時，區段會籍評估時間會依條件在歷程中出現的位置而有所不同：

* **在讀取對象歷程中，在等待活動之前：** Journey Optimizer會從設定檔的批次投影中讀取。 此投影中的資料在內嵌後&#x200B;**2小時**&#x200B;內已重新整理。 依賴日型或時間型條件的對象可能會遇到額外的延遲。 在歷程開始時新增短的[等待活動](../wait-activity.md)，或允許緩衝時間，以確保反映最新的區段會籍。
* **在單一事件歷程中或等待活動後：**&#x200B;從串流（單一）投影讀取區段會籍。 資料通常可在&#x200B;**15分鐘**&#x200B;內取得。 如需詳細資訊，請參閱[Adobe Experience Platform串流擷取檔案](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/streaming/overview){target="_blank"}。

## 相關主題

進一步瞭解如何在Adobe Journey Optimizer中使用對象：

* **[關於對象](../../audience/about-audiences.md)** — 瞭解對象如何在Adobe Experience Platform和Journey Optimizer中運作，包括如何建立和管理它們
* **[讀取對象活動](../read-audience.md)** — 使用對象來觸發歷程專案，並讓所有對象成員進入歷程
* **[對象資格事件](../audience-qualification-events.md)** — 從對象中聽取設定檔入口和出口，以即時觸發歷程動作
* **[在條件中使用對象](../conditions.md#using-a-segment)** — 使用「最佳化」活動，根據對象成員資格建立條件式歷程路徑
* **[歷程屬性 — 合併原則](../journey-properties.md)** — 瞭解在inAudience函式中使用多個對象時，合併原則如何運作

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面會記錄`inAudience`函式，此函式會即時檢查歷程設定檔是否屬於已命名的Adobe Experience Platform對象，並傳回歷程條件中使用的布林值。

**意圖：**
* 使用`inAudience`根據設定檔是否為特定對象成員來分支歷程路徑
* 結合多個`inAudience`檢查與AND/OR邏輯以建立複雜的鎖定目標條件
* 使用否定檢查(`inAudience("...") == false`)確認設定檔尚未進入特定對象
* 了解讀取對象歷程和單一事件歷程之間的傳播時間差異
* 識別並修正Adobe Experience Platform中因對象重新命名而造成的中斷對象引用

**字彙表：**
* **已實現**：對象參與狀態，指出個人目前符合對象定義資格，且是作用中成員&#x200B;*（產品特定）*
* **已退出**：對象參與狀態，指出個人已離開對象，不再符合&#x200B;*（產品特定）*
* **合併原則**： Adobe Experience Platform中的規則，可決定在評估對象成員資格&#x200B;*（產品特定）*&#x200B;時，如何合併來自多個資料集的設定檔資料
* **批次投影**：設定檔資料存放區已按照讀取對象歷程&#x200B;*（產品特定）*&#x200B;所使用的排程（擷取後2小時內）重新整理
* **串流投影**：用於單一事件歷程和等待活動後的即時設定檔資料存放區&#x200B;*（產品特定）* （通常在15分鐘內可用）

**護欄：**
* 單一歷程最多可擷取100個對象
* 對象名稱引數必須是字串常數；不支援欄位參考和動態運算式
* 在Adobe Experience Platform中重新命名對象不會自動更新歷程運算式中的`inAudience`參考 — 需要手動更新
* 同一個歷程中所使用的多個對象之間的合併原則不一致，可能會導致錯誤或警報

**術語：**
* 正式名稱：inAudience — 縮寫：none — 變體：inSegment （舊名稱）
* 同義字： &quot;inAudience&quot; = &quot;audience membership check function&quot;
* 請勿混淆：「已實現」（作用中成員）≠「已退出」（不再是成員）
* 請勿混淆：「inAudience」（目前函式）≠「inSegment」（已棄用的舊版函式）

**常見問題集：**
* **問：當設定檔退出對象時，`inAudience`會傳回什麼？**  — 它會傳回`false`；只有具有「已實現」狀態的設定檔才會被視為作用中成員，並傳回`true`。
* **問：我可以簽入單一歷程中的對象數目？**  — 單一歷程中最多可擷取100個對象。
* **問：如果在歷程中使用對象後重新命名Adobe Experience Platform中的對象，會發生什麼情況？**  — 歷程運算式不會自動更新；您必須手動編輯`inAudience`呼叫以使用新的對象名稱，否則條件將會中斷。
* **問：在讀取對象歷程中更新設定檔後，對象會籍的可用速度為何？**  — 在等待活動之前的讀取對象歷程中，會從擷取後2小時內重新整理的批次投影讀取資料。
* **問：我可以將設定檔屬性傳遞為對象名稱引數嗎？**  — 否，對象名稱必須是字串常數；不支援欄位參考和運算式。

+++
