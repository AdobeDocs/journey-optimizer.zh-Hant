---
title: 「實驗」報表中使用的統計計算
description: 進一步了解執行實驗報表時所使用的統計計算
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# 實驗報表中的統計計算 {#experiment-report-calculations}

本頁記錄在Adobe Journey Optimizer中「行銷活動實驗」報表中使用的詳細統計計算。

請注意，本頁面適用於技術使用者。

## 轉換率

轉換率或 **平均值**,μ<sub>ν</sub> 每次治療 `ν` 在實驗中，定義為量度總和與指派給該量度的設定檔數之比，N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

給你，Y<sub>iν</sub> 是每個設定檔的目標量度值 `i`，已指派給指定變體 *ν*. 當目標量度是「不重複」量度時（亦即是執行特定動作的設定檔數目計數），這會顯示為轉換率，並以百分比格式設定。 當量度是「計數」或「總值」量度時（例如分別開啟電子郵件、收入），量度的平均估計值會顯示為「每個設定檔的計數」或「每個設定檔的值」。

如有需要，則會搭配使用範例標準差與運算式：

![](assets/statistical_2.png){width="225" align="center"}

## 提升度 {#lift}

變體之間的提升度  *ν*，和控制變數  *ν<sub>0</sub>* 是轉換率中的相對「差值」，定義為下方的計算，其中個別轉換率如上所定義。 這會以百分比顯示。

![](assets/statistical_3.png){width="125" align="center"}

</br>

## 個別處理的任何有效信賴區間

歷程實驗面板會針對實驗中的個別處理項目顯示「隨時有效」信賴區間（信賴序列）。

個別變體的信賴序列 `ν` 是Adobe所使用統計方法的核心。 您可以在 [本頁](https://doi.org/10.48550/arXiv.2103.06476) (重制自 [沃比 — 史密斯等])。

如果您想要預估目標參數 `ψ` 例如實驗中變數的轉換率、「固定時間」信賴區間(CI)序列與時間一致信賴序列(CS)之間的二分法可總結如下：

![](assets/statistical_4.png){width="500" align="center"}

對於一般信賴區間，概率保證目標參數位於值範圍內，Canalytic Consite Consite Consite Consite Consite Consite Consite Consite Consite Consite Consite Consite Consite Consite Consite Consite Co Co Cono Consite Con<sub>n</sub> 僅對 `n` (其中 `n` 是樣本數)。 反之，對於信賴序列，我們保證在所有時間/所有樣本大小的值 `t`，則目標參數的「true」值位於界限內。

這對線上測試來說很重要，其含意很深：

* 每當有新資料可用時，CS即可選擇更新。
* 實驗可以持續地監視、自適應地停止或繼續。
* I類錯誤會在所有停止時間（包括與資料相關的時間）進行控制。

Adobe使用漸近信賴序列，此序列用於具有平均估計的個體變體 `μ` 有下清單單：

![](assets/statistical_5.png){width="300" align="center"}

執行:

* `N` 是該變體的單位數。
* `σ` 是標準差的範例估計值（如上所定義）。
* `α` 是所需的I類錯誤等級（或誤覆概率）。 此值一律設為0.05。
* ρ<sup>2</sup> 是調整CS最緊的樣本大小的常數。 Adobe選擇了一個普適值ρ<sup>2</sup> = 10<sup>-2.8</sup>，此變數適用於線上實驗中的轉換率類型。

## 信賴度 {#confidence}

Adobe使用的置信度是「隨時有效」的置信度，該置信度通過反向平均處理效果的置信度序列而獲得。

準確地說，在兩個樣本中 *t* 測試兩種變體之間的均值差異時， *p*-value，以及不同值的信賴區間。 比如，任何時候 *p*&#x200B;通過為平均處理效果估計器求逆（隨時有效）置信序列，可獲得 — value:

![](assets/statistical_6.png){width="200" align="center"}

這裡， *E* 是預期。 所使用的估計器是逆傾向加權(IPW)估計器。 考慮N = N<sub>0</sub> +N<sub>1</sub> 件數，每個件數的變型分配 `i` 標籤為A<sub>i</sub>=0,1，如果單位被分配給變型 `ν`=0,1。 如果為使用者指派的機率（傾向）π固定<sub>0</sub>,(1-π)<sub>0</sub>)，其結果量度為Y<sub>i</sub>，則平均處理效果的IPW估計器為：

![](assets/statistical_12.png){width="400" align="center"}

注意到 *f* 是影響函式，沃比 — 史密斯等 表明該估計器的置信序列為：

![](assets/statistical_7.png){width="500" align="center"}

用其經驗估計代替分配概率：π<sub>0</sub> = N<sub>0</sub>/N，方差項可以用單個樣本平均估計μ來表示<sub>0,1</sub> 和標準差估計，σ<sub>0,1</sub> 如下：

![](assets/statistical_8.png){width="500" align="center"}

接下來，回想一下，對於測試統計值z =(μ)的常規假設測試<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>) `p`-values和信賴區間：

![](assets/statistical_9.png){width="500" align="center"}

where `Φ` 是標準常態的累積分佈。 在有效時 `p`-values，給定上述平均處理效果的置信度序列，我們可以反轉此關係：

![](assets/statistical_10.png){width="600" align="center"}

最後， **任何有效信任** 為：

![](assets/statistical_11.png){width="200" align="center"}

## 宣佈實驗結論

對於雙臂實驗，Journey Optimizer實驗面板會顯示訊息，指出實驗為 **結論** 當任何時間的有效信賴度超過95%時(即任何時間的有效 `p`-value低於5%)。

當存在兩個以上變體時，應用Bonferonni校正來控制家庭錯誤率。 為了實驗 `K` 處理和單基線（控制）處理 `K-1` 獨立假設檢驗。 Bonferonni校正意味著，如果在任何時間內有效，則我們拒絕控制和給定變數均等的空假設 `p`-value（如上定義）低於閾值 `α/(K-1)`.

## 效能最佳的手臂

當實驗被宣佈為結論性時，顯示最佳效能臂。 這是效能最佳（平均值或轉換率最高）的臂，位於包含控制項的集合中，且所有臂均具有 `p` — 值低於Bonferonni閾值。
