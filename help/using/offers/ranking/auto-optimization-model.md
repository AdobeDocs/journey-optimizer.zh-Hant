---
product: experience platform
solution: Experience Platform
title: 自動最佳化模型
description: 深入了解自動最佳化模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: a85de6a9-ece2-43da-8789-e4f8b0e4a0e7
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '1404'
ht-degree: 0%

---

# 自動最佳化模型 {#auto-optimization-model}

自動最佳化模型旨在提供可將企業用戶端設定的回報(KPI)最大化的選件。 這些KPI可以是轉換率、收入等形式。 此時，自動最佳化著重於以選件轉換作為目標來最佳化選件點擊。 自動最佳化是非個人化的，且會根據選件的「全域」效能來最佳化。

## 限制 {#limitations}

使用自動最佳化模型進行決策管理受以下限制：

* 自動最佳化模型無法與Batch Decisioning API搭配使用。
* 建立模型所需的意見必須以體驗事件的形式傳入。 不應自動傳入 [!DNL Journey Optimizer] 管道。

## 術語 {#terminology}

討論自動最佳化時，下列詞語相當實用：

* **多臂吃角子**:A [多臂吃角子](https://en.wikipedia.org/wiki/Multi-armed_bandit)最佳化的{target=&quot;_blank&quot;}方法可平衡探索學習與該學習的利用。

* **Thomson採樣**:Thompson取樣是線上決策問題的演算法，其動作依序執行，必須在利用已知的項目來最大化即時效能與投資以累積可改善未來效能的新資訊之間取得平衡。 [了解更多](#thompson-sampling)

* [**Beta發佈**](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}:連續集 [概率分佈](https://en.wikipedia.org/wiki/Probability_distribution)在間隔上定義的{target=&quot;_blank&quot;} [0, 1] [參數化](https://en.wikipedia.org/wiki/Statistical_parameter){target=&quot;_blank&quot;}) [形狀參數](https://en.wikipedia.org/wiki/Shape_parameter){target=&quot;_blank&quot;}。

## Thompson取樣 {#thompson-sampling}

作為自動最佳化基礎的演算法為 **Thompson抽樣**. 在本節中，我們討論了Thompson採樣背後的直覺。

[Thompson抽樣](https://en.wikipedia.org/wiki/Thompson_sampling){target=&quot;_blank&quot;}或Bayesian強盜是多臂強盜問題的貝葉斯方法。  其基本思想是對待平均獎勵??以 **隨機變數** 利用我們迄今收集到的資料來更新我們對平均回報的「信念」。 這個「信念」用數學上的 **後驗概率分佈**  — 基本上是平均獎勵的值範圍，以及獎勵對每個選件具有該值的可信度（或機率）。 那麼，每個決定，我們 **從這些後獎勵分佈中的每個點樣本** 並選擇其抽樣獎勵具有最高價值的優惠方案。

下圖說明此程式，我們提供3個不同選件。 最初，我們沒有從資料中得到任何證據，我們假設所有的獎勵都具有統一的後獎勵分佈。 我們會從每個優惠方案的後獎勵分佈中抽取樣本。 從選件2的分送中選取的範例具有最高值。 這是 **探勘**. 展示選件2後，我們收集任何潛在獎勵（例如轉換/無轉換），並使用貝葉斯定理更新選件2的後驗分佈，如下所述。  我們會繼續進行此程式，並在每次顯示優惠方案並收集獎勵時更新後續分配。 在第二個數字中，選擇了選件3 — 儘管選件1的平均獎勵最高（其後獎勵分佈最靠右），但從每個分佈進行採樣的過程導致我們選擇了明顯次優的選件3。 通過這樣做，我們有機會進一步了解優惠方案3的真正獎勵分配。

隨著收集更多樣本，信賴度增加，並且獲得對可能獎勵的更準確估計（對應於較窄的獎勵分佈）。 隨著更多證據的出現，我們更新信念的過程被稱為 **貝葉斯推理**.

最終，如果某個優惠方案（例如優惠方案1）是明確的獲勝者，其後續獎勵分配將與其他優惠方案分開。 此時，對於每項決策，來自選件1的取樣獎勵可能最高，而我們將以較高的機率加以選擇。 這是 **剝削**  — 我們堅信選件1是最好的，因此，我們選擇選件是為了獲得最大的回報。

![](../assets/ai-ranking-thompson-sampling.png)

**圖1**: *對於每個決策，我們從後獎勵分佈中抽取一個點。 將選擇範例值最高（轉換率）的選件。 在初始階段中，所有選件均具有統一分佈，因為我們沒有任何關於資料選件轉換率的證據。 隨著採集樣本的增多，後驗分佈變窄且更準確。 最終，每次都會選擇轉換率最高的選件。*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**技術詳細資訊**

要計算/更新分配，我們使用 **貝葉斯定理**. 對於每個選件 ***i***，我們要計算它們的***P(??i |資料)***，即針對每個選件 ***i***，獎勵價值的可能性 **??i** 是，因為我們目前已針對該選件收集了資料。

根據貝葉斯定理：

***後驗=似然*前***

此 **先驗概率** 是產出概率的初步猜測。 在收集了一些證據後，機率稱為 **後驗概率**. 

自動最佳化的設計目的是考慮二進位獎勵（點按/無點按）。 在此案例中，機率代表N次試驗的成功次數，並以 **二項式分佈**. 對於某些似然函式，如果選擇某個先驗，則後驗的分佈與前驗的分佈相同。 之前的這個稱為 **共軛先驗**. 這種先驗使得後驗分佈的計算十分簡單。 此 **Beta發佈** 是二項似然（二進位獎勵）前的共軛項，是前、後概率分佈的一種方便、合理的選擇。 ***α*** 和 ***β***. 這些參數可視為成功和失敗的計數，以及由下列項目提供的平均值：

![](../assets/ai-ranking-beta-distribution.png)

如上所述，似然函式是以二項式分佈模型，成功（轉換）和失敗（無轉換）,q是 [隨機變數](https://en.wikipedia.org/wiki/Random_variable){target=&quot;_blank&quot;}，帶有 [β分佈](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}。

驗前分佈採用Beta分佈模型，驗後分佈採用以下形式：

![](../assets/ai-ranking-posterior-distribution.svg)

只要將成功和失敗次數加到現有參數即可計算後驗 ***α***, ***β***.

針對自動最佳化，如上例所示，我們以先前的分佈開始 ***Beta(1, 1)*** （均勻分佈）適用於所有選件，在給定選件成功和失敗之後，後驗將變為含參數的Beta分佈 ***(s+α, f+β)*** 那個提議。
+++

**相關主題**：

如需深入探討Thompson取樣，請閱讀下列研究論文：
* [Thompson抽樣的實證評價](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target=&quot;_blank&quot;}
* [多臂吃角子老虎機問題的Thompson抽樣分析](http://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target=&quot;_blank&quot;}

## 冷啟動問題 {#cold-start}

將新選件新增至促銷活動，且沒有新選件的轉換率相關資料時，就會發生「冷啟動」問題。 在此期間，我們必須想出策略來決定選擇此新選件的頻率，以便將效能下降降到最低，同時收集此新選件的轉換率資訊。 有多種解決方案可以解決此問題。 關鍵是在探索這一新優惠方案之間找到平衡，同時我們不會犧牲太多開採。 目前，我們使用「統一分佈」作為新選件轉換率（先前分佈）的初步猜測。 基本上，我們給出所有轉換率值等於發生概率。


![](../assets/ai-ranking-cold-start-strategies.png)

**圖2**: *假設促銷活動有3個選件。 當促銷活動上線時，選件4會新增至促銷活動。 起初，我們沒有選件4的轉換率相關資料，必須處理冷啟動問題。 我們會使用統一分佈作為對選件4的轉換率的初步猜測，同時收集此新選件的資料。 如 [Thompson抽樣](#thompson-sampling) 區段中，若要選擇要向使用者顯示哪個選件，我們會從選件的後驗獎勵分佈中取樣點，並選取取樣值最高的選件。 在上述範例中，選擇選件4，稍後根據收集的獎勵，更新此選件的後續分佈，如 [Thompson抽樣](#thompson-sampling) 區段。*

## 提升度測量 {#lift}

「提升度」是與基線策略（只隨機提供選件）相比，用來評估排名服務中部署之任何策略之效能的量度。

例如，如果我們有興趣測量用於排名服務的Thompson抽樣(TS)策略的效能，而KPI是轉換率(CVR)，則TS策略相對於基線策略的「提升度」定義為：

![](../assets/ai-ranking-lift.png)
