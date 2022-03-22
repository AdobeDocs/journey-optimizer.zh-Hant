---
product: experience platform
solution: Experience Platform
title: 關於AI模型
description: 瞭解允許對優惠排序的AI模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: f5627a23ceb0d00dd01db8766e72fed1b5d652a3
workflow-type: tm+mt
source-wordcount: '1508'
ht-degree: 0%

---

# AI模型 {#ai-models}

## 開始使用AI模型 {#get-started-with-ai-rankings}

[!DNL Journey Optimizer] 允許您使用經過培訓的模型系統來對給定配置檔案顯示報價。

>[!CAUTION]
>
>AI模型的使用目前僅在選擇用戶的早期訪問中可用。

此功能使您能夠建立不同的 **AI模型** 根據你的業務目標。 在決策中使用這些不同的基於目標的策略，經過訓練的模型系統將幫助您瞭解不同的人工智慧模型如何影響您的目標。

例如，您可以為電子郵件通道選擇AI模型，為推送通道選擇另一個模型。 對於每個渠道，經過培訓的模型系統將利用多個資料點來確定在給定位置應首先提供哪個優惠，而不是考慮優惠的優先順序分數或 [排序公式](create-ranking-formulas.md)。

>[!NOTE]
>
>當前 [!DNL Journey Optimizer] AI排名唯一支援的模型類型是 **自動優化**。

## 自動優化模型 {#auto-optimization}

自動優化模型旨在為企業客戶設定的回報(KPI)最大化的服務。 該等主要表現指標可以以兌換率、收入等形式呈列。 此時，自動優化將重點放在優化服務點擊量，同時將服務轉換作為我們的目標。 自動優化是非個性化的，並且基於產品的「全局」效能進行優化。

### 術語

以下術語在討論自動優化時非常有用：

* **多兵種強盜**:A [多兵種強盜](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=&quot;_blank&quot;}優化方法平衡了探索性學習和利用該學習。

* **湯姆森採樣**: Thompson抽樣是一種線上決策問題的算法，在這種問題中，動作按順序執行，必須在利用已知的最大化即時效能和投資以積累可能改善未來效能的新資訊之間取得平衡。 [了解更多](#thompson-sampling)

* [**Beta分佈**](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;:連續集 [概率分佈](https://en.wikipedia.org/wiki/Probability_distribution)在間隔上定義的{target=&quot;_blank&quot;} [0、1] [參數化](https://en.wikipedia.org/wiki/Statistical_parameter){target=&quot;_blank&quot;為兩個正 [形狀參數](https://en.wikipedia.org/wiki/Shape_parameter){target=&quot;_blank&quot;}。

### 湯普森抽樣 {#thompson-sampling}

作為自動優化基礎的算法是 **湯普森抽樣**。 在本部分，我們討論湯普森抽樣的直覺。

[湯普森抽樣](https://en.wikipedia.org/wiki/Thompson_sampling){target=&quot;_blank&quot;}或Bayesian強盜是多武強盜問題的Bayes方法。  其基本思想是給平均獎勵？從每個報價中 **隨機變數** 利用我們迄今收集到的資料，更新我們對平均回報的「信念」。 這個「信念」由 **後驗概率分佈**  — 基本上是平均獎勵的價值範圍，以及獎勵對每項獎勵具有該價值的可能性（或概率）。 那麼，每個決定，我們 **從每個後驗獎勵分佈中抽取一個點** 並選擇其抽樣回報最高的報價。

下圖說明了此過程，其中我們有3個不同的報價。 最初，我們沒有從資料中得到任何證據，我們假設所有報價都具有統一的後驗回報分佈。 我們從每份報酬的後驗分佈中抽取樣本。 從「優惠2」的分發中選擇的樣本值最高。 這是 **勘探**。 在顯示出價2後，我們收集任何潛在的回報（例如轉換/無轉換），並使用貝葉斯定理更新出價2的後驗分佈，如下所述。  我們繼續此過程，並在每次顯示要約和收集報酬時更新後驗分佈。 在第二個數字中，我們選擇了要約3 — 儘管要約1具有最高的平均回報（其後的回報分佈最靠右），但從每個分配中抽樣的過程已導致我們選擇一個明顯次優的要約3。 通過這樣做，我們有機會瞭解關於&quot;要約3&quot;的真正獎勵分配的更多資訊。

隨著收集更多樣本，置信度增加，並且獲得對可能獎勵的更準確估計（對應於較窄的獎勵分配）。 隨著更多證據的出現，更新我們信念的過程被稱為 **貝葉斯推理**。

最終，如果一個報價（例如，報價1）是明確的贏家，其後的回報分配將與其他報價分離。 此時，對於每個決定，第1條的抽樣獎勵可能是最高的，我們將以更高的概率選擇它。 這是 **剝削**  — 我們堅信，第1條是最好的，因此我們選擇它是為了最大化回報。

![](../assets/ai-ranking-thompson-sampling.png)

**圖1**: *對於每個決策，我們從後驗獎勵分佈中抽取一個點。 將選擇採樣值最高（轉換率）的服務。 在初始階段，所有報價都具有均勻的分佈，因為我們沒有任何關於資料報價的轉換率的證據。 隨著樣本數的增加，後驗分佈變窄、更準確。 最終，將每次選擇轉換率最高的報價。*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**技術詳細資訊**

要計算/更新分配，我們使用 **貝葉斯定理**。 對於每個優惠 ***我***&#x200B;我們要計算他們的***P(?i |資料)***，即每項優惠 ***我***，獎勵價值的可能性 **?i** 就是，根據我們迄今為此而收集的資料。

從貝葉斯定理：

***後驗=似然*前驗***

的 **先驗概率** 是產出概率的初步猜測。 在收集到一些證據後，概率稱為 **後驗概率**。 

自動優化設計為考慮二進位獎勵（按一下/不按一下）。 在此情況下，可能性表示N次審判的成功數，並以 **二項分佈**。 對於某些似然函式，如果選擇某個先驗，則後驗分佈與前驗分佈相同。 這樣的先生稱為 **共軛先驗**。 這種先驗使得後驗分佈的計算非常簡單。 的 **Beta分佈** 二項似然（二進位獎勵）的前置詞，是先驗和後驗概率分佈的一種方便而明智的選擇。 ***α*** 和 ***β***。 這些參數可以視為成功和失敗的計數，以及由以下方式給出的平均值：

![](../assets/ai-ranking-beta-distribution.png)

如上所述的Likeliod函式由Binomial分佈建模，其成功（轉換）和失敗（無轉換）,q是 [隨機變數](https://en.wikipedia.org/wiki/Random_variable){target=&quot;_blank&quot;&quot;，帶 [β分佈](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}。

驗前分佈採用Beta分佈模型，驗後分佈採用以下形式：

![](../assets/ai-ranking-posterior-distribution.svg)

通過簡單地將成功和失敗次數添加到現有參數中來計算後驗 ***α***。 ***β***。

對於自動優化，如上例所示，我們從先驗分佈開始 ***Beta(1,1)*** （均勻分佈），在獲得成功後，在給定的提供失敗後，後驗變為帶參數的Beta分佈 ***(s+α, f+β)*** 那個提議。
+++

**相關主題**：

要更深入地瞭解湯普森的抽樣，請閱讀以下研究論文：
* [Thompson抽樣的實證評價](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target=&quot;_blank&quot;
* [多武裝盜匪問題的Thompson抽樣分析](http://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target=&quot;_blank&quot;

### 冷啟動問題

「冷啟動」問題是在市場活動中添加新優惠，並且沒有關於新優惠轉換率的資料時發生的。 在此期間，我們必須制定一個策略，說明選擇此新優惠的頻率，以便將效能下降降至最低，同時我們收集有關此新優惠的轉換率的資訊。 有多種解決方案可解決此問題。 關鍵是在探索這一新提議之間找到平衡，同時我們不會犧牲開採。 目前，我們使用&quot;統一分佈&quot;作為對新報價的轉換率（先驗分佈）的初步猜測。 基本上我們給出所有轉換率值等概率。


![](../assets/ai-ranking-cold-start-strategies.png)

**圖2**: *考慮一個包含3個優惠的活動。 在活動現場進行時，會在活動中添加「優惠4」。 最初，我們沒有關於優惠4的轉換率的資料，我們必須處理冷啟動問題。 我們使用統一分佈作為對第4項要約轉換率的初步猜測，同時我們為此新要約收集資料。 如 [湯普森抽樣](#thompson-sampling) 選擇向用戶顯示的服務，我們從服務的後驗獎勵分佈中抽取點，並選擇樣本值最高的服務。 在上例中，選擇了「要約4」，然後根據所收到的獎勵，更新此要約的後驗分佈，如 [湯普森抽樣](#thompson-sampling) 的子菜單。*

### 升程測量

「提升」是衡量在排名服務中部署的任何策略的效能的指標，與基線策略（只是隨機提供服務）相比。

例如，如果我們對衡量在排名服務中使用的Thompson抽樣(TS)策略的效能感興趣，並且KPI是轉換率(CVR)，則TS策略相對於基線策略的「提升」定義為：

![](../assets/ai-ranking-lift.png)
