---
product: experience platform
solution: Experience Platform
title: 自動最佳化模型
description: 進一步瞭解自動最佳化模型
badge: label="舊版" type="Informative"
feature: Ranking, Decision Management
role: User
level: Experienced
exl-id: a85de6a9-ece2-43da-8789-e4f8b0e4a0e7
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 0%

---

# 自動最佳化模型 {#auto-optimization-model}

自動最佳化模型旨在提供可大幅提升業務客戶所設定回報(KPI)的優惠方案。 這些KPI可以是轉換率、收入等形式。 此時，自動最佳化的重點是最佳化優惠點按，並將優惠轉換作為我們的目標。 自動最佳化是非個人化的，並根據選件的「全域」效能進行最佳化。

## 資料集需求

若要訓練自動最佳化模型，資料集必須符合下列最低需求：

* 資料集中至少有2個選件在過去14天內必須具有至少100個顯示事件和5個點選事件。
* 少於100個顯示和/或過去14天內5個點選事件的選件，模型會將視為新選件，且僅符合由Exploration Bandit提供的資格。
* 模型會將過去14天內有超過100個顯示區和5個點選事件的優惠方案視為現有優惠方案，並符合約時接受探索和開發強盜服務的資格。

在首次訓練自動最佳化模型之前，使用自動最佳化模型的選取策略中的選件將會隨機提供。

## 限制 {#limitations}

使用自動最佳化模型以進行決策管理時，必須遵守下列限制：

* 自動最佳化模型不適用於批次決策API。
* 建立模型所需的意見反應必須作為體驗事件傳入中。 不應在[!DNL Journey Optimizer]通道中自動傳送。

## 術語 {#terminology}

討論自動最佳化時，下列字詞相當實用：

* **多臂吃角子老虎機**：最佳化的[多臂吃角子老虎機](https://en.wikipedia.org/wiki/Multi-armed_bandit){target="_blank"}方法可平衡探索學習和該學習的利用。

* **Thomson抽樣**： Thompson抽樣是一種用於線上決策問題的演演算法，其動作是循序執行的，必須在開發已知能最大化即時效能與投資累積可能改善未來效能的新資訊之間取得平衡。 [了解更多](#thompson-sampling)

* [**Beta分佈**](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}：在間隔[0、1](https://en.wikipedia.org/wiki/Probability_distribution){target="_blank"} [引數化]上定義的一組連續[機率分佈](https://en.wikipedia.org/wiki/Statistical_parameter){target="_blank"}，由兩個正的[形狀引數](https://en.wikipedia.org/wiki/Shape_parameter){target="_blank"}所定義。

## Thompson取樣 {#thompson-sampling}

自動最佳化基礎的演演算法是&#x200B;**Thompson取樣**。 在本節中，我們將討論Thompson取樣背後的直覺。

[Thompson取樣](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}或是Bayesian強盜，是多臂強盜問題的貝葉斯方法。  基本想法是將每個優惠的平均獎勵𝛍視為&#x200B;**隨機變數**，並使用我們目前所收集的資料來更新我們關於平均獎勵的「信念」。 此「信念」以數學方式表示為&#x200B;**後驗機率分佈** — 基本上是平均獎勵值的範圍，以及每個優惠的獎勵具有該值的可能性（或機率）。 然後，對於每個決定，我們將&#x200B;**從這些後驗獎勵分佈中的每個分佈**&#x200B;取樣一個點，並選取取樣獎勵具有最高值的優惠。

此程式如下圖所示，我們有3個不同的選件。 起初，我們無法從資料中取得任何證據，而且我們假設所有優惠方案都有一個統一的後驗獎勵分佈。 我們會從每個優惠方案的前端回報分佈中抽取樣本。 從選件2的分佈中選取的範例具有最高值。 這是&#x200B;**探索**&#x200B;的範例。 顯示優惠方案2後，我們會收集任何潛在獎勵（例如轉換/不轉換），並使用貝葉斯定理更新優惠方案2的後驗分佈，如下所述。  我們將繼續此程式，並在每次顯示優惠方案並收集獎勵時更新後續分配。 在第二個數字中，已選取「選件3」 — 儘管選件1的平均報酬最高（其後方的報酬分佈最靠右），從每個分佈取樣的程式已導致我們選擇明顯次優的選件3。 我們藉此機會進一步瞭解Offer 3的真正獎勵分配。

當收集到更多的範例時，可信度會提高，並取得可能獎勵的更準確預估（對應於較窄的獎勵分佈）。 這個在更多證據出現時更新我們信念的過程稱為&#x200B;**貝葉斯推斷**。

最終，如果一個選件（例如選件1）是明確的獲勝者，其後驗獎勵分配將與其他選件分開。 此時，對於每個決定，從選件1取得的抽樣獎勵可能是最高的，而我們將以較高的機率選擇它。 這是&#x200B;**利用** — 我們堅信選件1是最好的，因此選擇它是為了最大化回報。

![](../assets/ai-ranking-thompson-sampling.png)

**圖1**： *對於每項決定，我們都會從後驗獎勵分配中取樣一個分數。 將會選擇具有最高範例值（轉換率）的選件。 在初始階段，所有選件具有統一分佈，因為我們沒有任何證據可以證明資料中選件的轉換率。 當我們收集到更多樣本時，後驗分佈會變得更窄且更準確。 最終，每次都會選擇轉換率最高的選件。*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**技術詳細資料**

若要計算/更新分佈，請使用&#x200B;**貝葉斯定理**。 我們想要針對每個選件&#x200B;***i***&#x200B;計算其***P(𝛍i) | 資料)***，亦即對於每個優惠方案&#x200B;***i***，考慮到我們目前為止針對該優惠方案所收集的資料，獎勵值&#x200B;**𝛍i**&#x200B;的可能性有多大。

從貝葉斯定理：

***後方=可能性*先前***

**先前機率**&#x200B;是產生輸出機率的初始猜測。 在收集了一些證據之後，此機率稱為&#x200B;**後驗機率**。 

自動最佳化的設計會考量二進位獎勵（按一下/不按一下）。 在此案例中，可能性代表N個試用中的成功次數，並以&#x200B;**二項式分佈**&#x200B;建模。 對於某些似然函式，如果您選擇特定的前一個，則後一個分佈會與前一個分佈相同。 如此的前置位址稱為&#x200B;**共軛前置**。 這種先驗使後驗分佈的計算非常簡單。 **Beta分佈**&#x200B;在二項式似然之前（二進位獎勵）是共軛的，因此對於前後概率分佈來說，這是一個方便而合理的選擇。Beta分佈有兩個引數，***α***&#x200B;和&#x200B;***β***。 這些引數可視為成功和失敗的計數，以及下列引數提供的平均值：

![](../assets/ai-ranking-beta-distribution.png)

如上所述的Likelihood函式是由二項式分佈模型化，其中s成功（轉換）和f失敗（無轉換），而q是具有[beta分佈](https://en.wikipedia.org/wiki/Random_variable){target="_blank"}的[隨機變數](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}。

前置式分佈是以Beta分佈為模型，而後置式分佈則採用下列形式：

![](../assets/ai-ranking-posterior-distribution.svg)

只要將成功和失敗的數目加到現有引數&#x200B;***α***、***β***&#x200B;即可計算後驗數。

對於自動最佳化，如上述範例所示，我們以所有選件的先前分佈&#x200B;***Beta(1， 1)*** （統一分佈）開始，並且在特定選件成功和f次失敗後，後驗會變成該選件的引數&#x200B;***(s+α， f+β)***&#x200B;的Beta分佈。
+++

**相關主題**：

如需深入瞭解Thompson取樣，請閱讀下列研究檔案：

* [Thompson抽樣經驗評估](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target="_blank"}
* [多臂吃角子老虎機問題的Thompson取樣分析](https://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target="_blank"}

## 冷啟動問題 {#cold-start}

將新優惠方案新增至行銷活動時，會發生「冷啟動」問題，且沒有新優惠方案的轉換率相關資料可用。 在此期間，我們必須提出一項策略，決定選擇此新選件的頻率，以便將效能下降降至最低，同時收集此新選件轉換率的相關資訊。 有多種解決方案可以解決這個問題。 關鍵是要在這項新優惠方案探索之間取得平衡，同時不犧牲太多開發成果。 目前我們使用「統一分送」，作為新優惠方案轉換率（先前分送）的初步猜測。 基本上，我們提供所有轉換率值等於發生機率。


![](../assets/ai-ranking-cold-start-strategies.png)

**圖2**： *考慮包含3個選件的行銷活動。 行銷活動進行時，選件4會新增至行銷活動。 我們最初沒有有關Offer 4轉換率的資料，因此必須處理冷啟動問題。 我們使用統一分佈來做我們對Offer 4轉換率的初步猜測，同時我們收集這個新選件的資料。 如[Thompson取樣](#thompson-sampling)區段所述，為了選擇要向使用者顯示哪個優惠方案，我們會從優惠方案的後驗獎勵分佈中取樣點數，並選取具有最高取樣值的優惠方案。 在上述範例中，已選取選件4，而且稍後會根據所收集的獎勵，更新此選件的後驗分佈，如[Thompson取樣](#thompson-sampling)區段中所述。*

## 提升度測量 {#lift}

「提升度」量度可用來測量排名服務中部署的任何策略與基線策略（隨機提供選件）的效能。

例如，如果我們想要測量用於排名服務的Thompson取樣(TS)策略效能，而KPI是轉換率(CVR)，則TS策略相對於基準策略的「提升度」定義為：

![](../assets/ai-ranking-lift.png)
