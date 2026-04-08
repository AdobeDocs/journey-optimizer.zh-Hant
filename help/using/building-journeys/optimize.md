---
solution: Journey Optimizer
product: journey optimizer
title: 活動最佳化
description: 瞭解最佳化活動
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 活動，條件，畫布，歷程，最佳化
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
source-git-commit: 8aeb3e3769e28419982c28620e5b141778d2fa67
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 8%

---

# 開始使用最佳化活動 {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="活動最佳化"
>abstract="藉由將活動&#x200B;**最佳化**，您可以根據特定準則 (包括實驗、目標選擇和特定條件) 建立多條路徑，定義每個個體在您歷程中的進展方式。 請注意，**最佳化**&#x200B;活動是在歷程中建立條件式路徑的新工具。 它取代之前的&#x200B;**條件**&#x200B;活動。"

>[!IMPORTANT]
>
>**最佳化**&#x200B;活動是在歷程中建立條件式路徑的新工具。 它取代了先前的&#x200B;**條件**&#x200B;活動，此活動已從UI中移除。 所有條件式邏輯都會保留，而且現在會透過&#x200B;**最佳化**&#x200B;活動的[條件](conditions.md)處理。
>
>如果您有使用&#x200B;**[!UICONTROL 條件]**&#x200B;活動的現有歷程，您可以像之前一樣繼續使用。 它們現在會以新圖示顯示，作為&#x200B;**[!UICONTROL 使用]**&#x200B;條件&#x200B;**[!UICONTROL 方法最佳化]**&#x200B;活動，但行為未變更。 您在節點上設定的任何自訂標籤都會保留。

**最佳化**&#x200B;活動可讓您根據特定條件（包括實驗、目標定位和特定條件）建立多個&#x200B;**路徑**，以定義個人在您的歷程中如何前進 — 確保最大程度的參與和成功，以建立高度自訂且有效的歷程。

![歷程活動浮動視窗中的「最佳化」按鈕](assets/journey-optimize.png)

## 什麼是歷程路徑？ {#journey-path}

歷程&#x200B;**路徑**&#x200B;可由下列任一專案組成：通訊順序、通訊時間、通訊次數或這三個變數的任意組合。

例如，一個路徑可能包含一封電子郵件，另一個路徑可能包含兩則簡訊，而第三個路徑可能包含一封電子郵件、兩個小時的「等待」節點，然後是一則簡訊。

## 最佳化歷程的三種方法 {#optimization-methods}

透過&#x200B;**最佳化**&#x200B;活動，您可以對歷程路徑執行下列動作：

* [執行路徑實驗](path-experimentation.md) — 根據隨機分割測試不同的路徑，以根據預先定義的成功量度（例如：轉換率、收入、參與）判斷哪些路徑執行效果最佳。

* [運用目標規則](path-targeting.md) — 根據對象區段、設定檔屬性或內容資料，定義客戶必須符合的特定規則，才有資格輸入其中一個歷程路徑。 這可確保正確的對象進入指定路徑。

  >[!AVAILABILITY]
  >
  >此功能目前處於「有限可用性」。 如欲請求存取權，請和您的 Adobe 代表聯絡。

* [套用條件](conditions.md) — 根據特定條件建立條件路徑，例如資料來源、時間、日期、百分比分割或設定檔上限。 這等同於前一個「條件」活動。

## 運作方式 {#how-it-works}

歷程上線後，會根據定義的條件評估設定檔，並根據比對條件，將設定檔從歷程傳送至適當的路徑。

## 後續步驟 {#next-steps}

選取最適合您使用案例的最佳化方法：

* 想要測試並瞭解哪個路徑效果最佳？ →前往[路徑實驗](path-experimentation.md)
* 想要依特定路徑傳送不同對象？ →前往[路徑鎖定目標](path-targeting.md)
* 想要建立條件式邏輯（if/then案例）？ →前往[條件](conditions.md)
