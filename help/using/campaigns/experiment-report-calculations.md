---
title: 實驗報告中使用的統計計算
description: 深入瞭解執行實驗報告時使用的統計計算
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 67ba8861-be6f-42ae-b9b8-96168d0dd15c
source-git-commit: c14a9385191cfa4368e0b84ab16a63c4c87e2c69
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 1%

---

# 了解實驗報告中的統計計算 {#experiment-report-calculations}

本頁會記錄Adobe Journey Optimizer行銷活動的實驗報告中使用的詳細統計計算。

請注意，本頁僅供技術使用者使用。

## 轉換率

轉換率或 **平均值**， μ<sub>ν</sub> 每種處理 `ν` 在實驗中，定義為量度加總與指派給該量度的設定檔數量之間的比率，N<sub>ν</sub>：

![](assets/statistical_1.png){width="125" align="center"}

這裡，Y<sub>iν</sub> 是每個設定檔的目標量度值 `i`，已指派給指定變體 *ν*. 當目標量度是「唯一」量度時（即是執行特定動作的設定檔數計數），會顯示為轉換率，並格式化為百分比。 當量度是「計數」或「總值」量度（分別例如電子郵件開啟次數、收入）時，該量度的平均估計會顯示為「每個設定檔計數」或「每個設定檔的值」。

如有需要，範例標準差會與運算式搭配使用：

![](assets/statistical_2.png){width="225" align="center"}

## 提升度 {#lift}

變體之間的提升度  *ν*、和控制變體  *ν<sub>0</sub>* 是轉換率的相對「差異」，定義如下，其中個別轉換率的定義如上所示。 這會以百分比顯示。

![](assets/statistical_3.png){width="125" align="center"}

</br>

## 適用於個別處理的隨時有效信賴區間

Journey Experimentation面板會顯示實驗中個別處理方式的「隨時有效」信賴區間（信賴序列）。

個別變體的信賴序列 `ν` 是Adobe所用統計方法的中心。 您可在此找到其定義： [此頁面](https://doi.org/10.48550/arXiv.2103.06476) (轉載自 [Waudby-Smith等])。

如果您想要預估目標引數 `ψ` 例如，實驗中的變體轉換率，「固定時間」信賴區間(CI)序列和時間一致信賴序列(CS)之間的二分法可以概括如下：

![](assets/statistical_4.png){width="500" align="center"}

對於規則信賴區間，目標引數在ċ值範圍內的機率保證<sub>n</sub> 只對下列的單一固定值有效： `n` (其中 `n` 為樣本數)。 相反地，對於信賴序列，我們保證在任何時候/所有樣本大小值 `t`，則感興趣之引數的「true」值在其界限內。

這隱含幾項對線上測試非常重要的深層含意：

* CS可在新資料可用時選擇性地更新。
* 實驗可以持續監控、自適應停止或繼續。
* type-I錯誤會在所有停止時間（包括資料相依時間）受到控制。

Adobe使用漸近信賴序列，這適用於具有平均估計值的個別變體 `μ` 的格式為：

![](assets/statistical_5.png){width="300" align="center"}

其中：

* `N` 是該變體的單位數。
* `σ` 是標準差的預估範例（定義於上文）。
* `α` 是所需的type-I error （或miscoverage機率）層級。 此值一律設為0.05。
* ρ<sup>2</sup> 是一個常數，可調整CS最緊密的樣本大小。 Adobe已選擇ρ的通用值<sup>2</sup> = 10<sup>-2.8</sup>，適用於線上實驗中顯示的轉換率型別。

## 信賴度 {#confidence}

Adobe使用的信賴度是「隨時有效」的信賴度，這是透過反轉平均處理效果的信賴度序列所取得。

更精確地說，在兩個範例中 *t* 測試兩個變體之間的均數差異，變體之間會有1:1的對應 *p*-value代表這個測試，而信賴區間代表平均數之差。 打個比方，隨時有效 *p*-value可透過反轉平均處理效果估計器的（隨時有效）信賴序列來取得：

![](assets/statistical_6.png){width="200" align="center"}

此處， *E* 是預期。 使用的估計器是反向傾向加權(IPW)估計器。 考慮N = N<sub>0</sub> +N<sub>1</sub> 單位，每個單位的變數指派 `i` 標示為A<sub>ì</sub>=0,1表示單位已指派給變體 `ν`=0,1. 如果使用者被指派了固定機率（傾向） π<sub>0</sub>， (1-π<sub>0</sub>)，其結果量度為Y<sub>ì</sub>，則IPW的平均處理效果估計器為：

![](assets/statistical_12.png){width="400" align="center"}

請注意 *f* 為影響函式，Waudby-Smith等 顯示此估算程式的信賴序列為：

![](assets/statistical_7.png){width="500" align="center"}

以經驗估計取代指派機率： π<sub>0</sub> = N<sub>0</sub>/N，變數項可以用個別樣本平均值估計值μ來表示<sub>0,1</sub> 和標準差估計值，σ<sub>0,1</sub> 作為：

![](assets/statistical_8.png){width="500" align="center"}

接下來，回想一下對於具有測試統計值z = (μ)的常規假設測試<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>)兩者間有通訊 `p` — 值和信賴區間：

![](assets/statistical_9.png){width="500" align="center"}

位置 `Φ` 是標準常數的累積分佈。 隨時有效 `p`-values，根據以上定義的平均處理效果信賴序列，我們可以反轉此關係：

![](assets/statistical_10.png){width="600" align="center"}

最後， **隨時有效的信賴度** 為：

![](assets/statistical_11.png){width="200" align="center"}

## 宣告實驗為有結論

對於雙臂實驗， Journey Optimizer Experimentation面板會顯示訊息，說明實驗是 **已有結果** 當隨時有效信賴度超過95% （即隨時有效）時 `p`-value低於5%)。

當存在兩個以上的變體時，會套用Bonferonni校正，以控制族別錯誤率。 對於的實驗 `K` 處理方式以及單一基準（控制）處理方式有 `K-1` 獨立的假設測試。 Bonferonni校正表示我們拒絕空值假設，即如果隨時有效，控制項和給定變體具有相同的方法 `p`-value （定義於上面）低於臨界值 `α/(K-1)`.

## 績效最佳的手臂

當一個實驗宣告為具有結論性時，會顯示表現最佳的臂。 這是包含控制項的Set中效能最佳（最高平均或轉換率）的臂，以及所有具有 `p` — 值低於Bonferonni臨界值。
