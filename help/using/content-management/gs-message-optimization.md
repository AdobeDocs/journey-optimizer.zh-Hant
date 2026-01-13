---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用內容最佳化
description: 瞭解如何使用內容最佳化，在您的行銷活動和歷程中提供個人化和最佳化的內容。
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: 最佳化、目標定位、實驗、A/B測試、行銷活動、歷程、個人化
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: 8dba26f29fda47d0b953d80656aa0f0b6fe294a9
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 8%

---

# 開始使用內容最佳化 {#message-optimization}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_optimization"
>title="內容最佳化"
>abstract="Journey Optimizer中的內容最佳化可讓您測試內容的不同版本，並判斷哪些版本效果最佳。 您可以使用目標定位為特定區段提供個人化內容、實驗測試多種變數，或結合兩種方法以制定複雜的最佳化策略。"

內容最佳化可讓您在適當的時間將適當的訊息傳遞給適當的對象。 結合資料導向式深入分析和強大的個人化功能，您就能在行銷活動和歷程中實現最大化的參與度和轉換。

內容最佳化可在[行銷活動](../campaigns/create-campaign.md)和[歷程](../building-journeys/journey-gs.md)中使用，讓您對所有客戶接觸點套用相同的最佳化策略。

➡️ [在此影片中瞭解如何在行銷活動中運用內容最佳化](#video)

## 最佳化功能 {#capabilities}

透過Journey Optimizer中的內容最佳化，您可以：

* [使用目標定位](optimization-targeting.md)，根據設定檔屬性、情境資料或對象會籍，將個人化內容傳送給特定對象區段。

* [執行實驗](optimization-experimentation.md)以測試多個內容變異，並根據您的成功量度識別哪些變數表現最好。

* [結合這兩種方法](optimization-combination.md)以建立複雜的最佳化策略，您可在其中測試每個目標區段的不同變數。

## 目標定位與實驗 {#targeting-vs-experimentation}

瞭解鎖定目標與實驗之間的差異，可協助您針對目標選擇正確的最佳化方法。

**鎖定目標**&#x200B;會使用確定性規則，根據已知的設定檔屬性、內容或對象成員資格，將個人化內容傳送給特定區段。 這可確保正確的訊息能傳達給正確的受眾。

**實驗性**&#x200B;使用隨機指派來測試多個內容變異，並探索表現最佳的變異。 它可協助您透過資料導向測試，瞭解哪些內容最能引起觀眾的共鳴。

下表總結了主要差異：

| 功能 | 目標定位 | 實驗 |
|--------|-----------|-----------------|
| **指派方法** | 確定性 — 根據規則 | 隨機 — 根據流量分配 |
| **根據** | 設定檔屬性、內容、對象 | 隨機分佈 |
| **使用案例** | 將相關內容傳遞至已知區段 | 探索哪些內容表現最佳 |
| **範例** | 依位置顯示不同的促銷活動 | 測試2個主旨行，以檢視哪些主題行有更多開啟 |
| **最適合** | 大規模Personalization | 最佳化與學習 |

![](../campaigns/assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## 常見使用實例 {#use-cases}

以下是一些典型案例，內容最佳化可協助您獲得更好的結果：

目標定位：

* **地理定位** — 根據您的客戶所在位置，傳送特定於位置的選件。 例如，在較冷地區推廣冬季外套，在較溫暖的氣候中推廣泳衣。

* **裝置最佳化** — 提供裝置特定內容，例如案頭使用者的案頭最佳化版面配置以及智慧型手機使用者的行動最佳化版面配置。

實驗：

* **A/B測試** — 測試不同的電子郵件主旨列、call-to-action按鈕或促銷優惠，以找出哪些可帶來最多轉換。

* **生命週期行銷** — 測試新客戶的不同上線訊息與現有客戶的保留優惠。

組合：

* **進階分段** — 依忠誠度層級鎖定客戶，並在每個層級內測試不同的獎勵訊息，以最大化所有區段的參與度。

## 開始使用 {#get-started}

若要開始最佳化您的內容：

1. **建立行銷活動或歷程**：設定您的[行銷活動](../campaigns/create-campaign.md)或[歷程](../building-journeys/journey-gs.md)，並新增至少一個動作。

1. **選擇最佳化方法**：
   * [使用目標](optimization-targeting.md)個人化特定區段的內容。
   * [使用實驗](optimization-experimentation.md)測試多個變數。
   * [合併兩者](optimization-combination.md)以進行進階最佳化。

1. **定義您的內容**：為您的最佳化策略建立不同的內容變數。

1. **啟動和監視**：啟動您最佳化的行銷活動或歷程，並在[報告](../reports/campaign-global-report-cja.md)中追蹤效能。

## 運作方式 {#how-it-works}

在您的歷程或行銷活動上線後，會根據您定義的條件評估設定檔。 根據這些評估，每個設定檔都會收到最適當的內容版本：

1. **設定檔評估** — 當設定檔進入您的行銷活動或歷程時，Journey Optimizer會評估其屬性和內容。

1. **內容指派** — 根據您的最佳化設定：
   * 針對&#x200B;**目標定位**，符合特定條件的設定檔會收到對應的個人化內容。
   * 針對&#x200B;**實驗**，設定檔會根據您的流量配置設定，隨機指派給不同的內容變數。
   * 對於&#x200B;**組合**，設定檔會先符合目標規則，然後隨機指派給該區段的其中一個實驗變數。

1. **效能追蹤** - Journey Optimizer會自動追蹤參與量度和轉換資料，協助您識別哪些內容的效能最佳。

## 作法影片 {#video}

瞭解如何在行動中或API觸發的行銷活動中運用內容最佳化。 您將深入了解如何鎖定子對象目標、建立以位置為依據的訊息變化、啟用遞補內容，以及在單一行銷活動中執行多個實驗。本教學課程也涵蓋如何管理多頻道行銷活動，同時維持訊息的一致性。

>[!VIDEO](https://video.tv.adobe.com/v/3470379?captions=chi_hant&quality=12)

**相關主題**

* [建立行銷活動](../campaigns/create-campaign.md)
* [建立歷程](../building-journeys/journey-gs.md)
* [內容實驗](../content-management/get-started-experiment.md)
