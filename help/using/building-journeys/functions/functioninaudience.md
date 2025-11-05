---
product: journey optimizer
title: inAudience函式
description: 瞭解Adobe Experience Platform inAudience函式
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience，函式，運算式，歷程，對象，細分
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 4f653c0bd3f6998dd54deeae996b7b0427a1744e
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 2%

---

# inAudience函式 {#inAudience}

`inAudience`函式是Adobe Experience Platform函式，可讓您檢查歷程中的個人是否屬於特定對象。 這項強大的功能可讓您根據對象成員資格建立個人化的歷程路徑，在您的客戶體驗中啟用複雜的細分和目標定位。

當您需要以下動作時，請使用`inAudience`函式：

* 根據對象成員資格的分支歷程路徑。 [了解更多](../condition-activity.md#using-a-segment)
* 套用取決於設定檔是否屬於特定區段的條件式邏輯
* 使用個人化體驗鎖定特定的客戶群組
* 評估歷程條件中的即時受眾參與率
* 結合多個對象檢查以建立複雜的目標規則

函式會即時評估對象成員資格並傳回布林值，使其非常適合用於決策節點和條件運算式。 對象是在[Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"}中定義和管理的(深入瞭解[在Journey Optimizer中使用對象](../../audience/about-audiences.md))，運算式編輯器會提供自動完成建議，協助您正確參考對象。

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

## 相關主題

進一步瞭解如何在Adobe Journey Optimizer中使用對象：

* **[關於對象](../../audience/about-audiences.md)** — 瞭解對象如何在Adobe Experience Platform和Journey Optimizer中運作，包括如何建立和管理它們
* **[讀取對象活動](../read-audience.md)** — 使用對象來觸發歷程專案，並讓所有對象成員進入歷程
* **[對象資格事件](../audience-qualification-events.md)** — 從對象中聽取設定檔入口和出口，以即時觸發歷程動作
* **[在條件中使用對象](../condition-activity.md#using-a-segment)** — 使用條件活動，根據對象成員資格建立條件式歷程路徑
* **[歷程屬性 — 合併原則](../journey-properties.md)** — 瞭解在inAudience函式中使用多個對象時，合併原則如何運作

