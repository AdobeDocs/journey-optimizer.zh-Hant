---
title: 試驗報告中使用的統計計算
description: 瞭解有關運行實驗報告時使用的統計計算的詳細資訊
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: b3336381-bc73-4c8f-938f-f10fe37305b0
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 4%

---

# 實驗報告中的統計計算 {#experiment-report-calculations}

>[!BEGINSHADEBOX]

本文件提供下列內容：

* [開始使用內容實驗](get-started-experiment.md)
* [建立內容實驗](content-experiment.md)
* [瞭解統計計算](experiment-calculations.md)
* [設定實驗報告](reporting-configuration.md)
* **[實驗報告中的統計計算](experiment-report-calculations.md)**

>[!ENDSHADEBOX]

本頁記錄了Adobe Journey Optimizer市場活動實驗報告中使用的詳細統計計算。

請注意，本頁面面向技術用戶。

## 轉換率

轉換率或 **平**, μ<sub>ν</sub> 每次治療 `ν` 在實驗中，定義為度量之和與分配給該度量的配置檔案數之比，N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

給你，Y<sub>我</sub> 是每個配置檔案的目標度量值 `i`，它已分配給給定變數 *ν*。 當目標度量是「唯一」度量時，即，它是執行特定操作的配置檔案數的計數，則顯示為轉換率，並以百分比格式設定。 當度量是「計數」或「總值」度量（例如，電子郵件開啟，分別收入）時，度量的平均估計將顯示為「每個配置檔案的計數」或「每個配置檔案的值」。

根據需要，樣本標準差與表達式一起使用：

![](assets/statistical_2.png){width="225" align="center"}

## 提升度 {#lift}

變體之間的升降  *ν*，和控制項變數  *ν<sub>0</sub>* 是換算率中的相對「δ」，定義為下面的計算，其中各個換算率定義如上。 這以百分比顯示。

![](assets/statistical_3.png){width="125" align="center"}

</br>

## 針對個別治療的「任何時間」有效置信區間

「旅程實驗」面板顯示實驗中各個處理的「任何時間有效」置信區間（置信序列）。

單個變體的置信序列 `ν` 是Adobe所用統計方法的核心。 可在 [此頁](https://doi.org/10.48550/arXiv.2103.06476) (從 [沃德比史密斯等])。

如果您對估計目標參數感興趣 `ψ` 如實驗中變數的轉換率、「固定時間」置信區間(CI)序列和時間一致置信序列(CS)序列之間的二分法可以總結如下：

![](assets/statistical_4.png){width="500" align="center"}

對於正則置信區間，概率保證目標參數在值C/C範圍內<sub>n</sub> 僅在一個固定值為 `n` ( `n` 是示例數)。 相反，對於置信序列，我們保證在所有時間/所有樣本大小的值 `t`，感興趣參數的&quot;true&quot;值在界限內。

這對線上測試有很深的影響：

* 當新資料可用時，CS可以根據需要更新。
* 實驗可以連續地被監控、自適應地停止或繼續。
* I類錯誤在所有停止時間（包括與資料相關的時間）都被控制。

Adobe使用漸近置信序列，該序列對於具有平均估計的個體變數 `μ` 具有：

![](assets/statistical_5.png){width="300" align="center"}

執行:

* `N` 是該變數的單位數。
* `σ` 是標準差的樣本估計值（定義於上面）。
* `α` 是I類錯誤（或誤覆蓋概率）的所需級別。 此值始終設定為0.05。
* ρ<sup>2</sup> 是一個常數，它調節CS最緊的樣本大小。 Adobe選擇了ρ的普適值<sup>2</sup> = 10<sup>-2.8</sup>這適用於線上實驗中看到的轉換率類型。

## 信賴度 {#confidence}

Adobe所用的置信度是「隨時有效」的置信度，通過求平均治療效果的置信度序列得到。

準確地說，在兩個樣本中 *t* test兩個變數之間的均值差，在 *p*&#x200B;此test的 — value和均值差的置信區間。 比方說，任何時候 *p*-value可通過求平均處理效果估計器的（任何時間有效）置信序列來獲得：

![](assets/statistical_6.png){width="200" align="center"}

給， *E* 是預期。 所用估計器是逆傾向加權(IPW)估計器。 考慮N = N<sub>0</sub> +N<sub>1</sub> 單位，每個單位的變型分配 `i` 標有A<sub>我</sub>=0,1（如果單位已分配給變型） `ν`=0,1。 如果給用戶分配固定概率（傾向）π<sub>0</sub>, (1-π<sub>0</sub>)，其結果度量為Y<sub>我</sub>然後，IPW估計器對平均治療效果的估計為：

![](assets/statistical_12.png){width="400" align="center"}

注意到 *f* 是影響函式，沃德比 — 史密斯等 表明該估計器的置信序列為：

![](assets/statistical_7.png){width="500" align="center"}

用經驗估計代替分配概率：π<sub>0</sub> = N<sub>0</sub>/N，方差項可以用單個樣本均值估計μ表示<sub>0,1</sub> 標準差估計，σ<sub>0,1</sub> 為：

![](assets/statistical_8.png){width="500" align="center"}

接下來，回想一下，對於test統計量z=(μ)的正則假設test<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>)之間 `p`-values和置信間隔：

![](assets/statistical_9.png){width="500" align="center"}

何處 `Φ` 是標準常態分佈的累積分佈。 對於任何有效時間 `p`-values，給定上述平均治療效果的置信度序列，我們可以反轉這種關係：

![](assets/statistical_10.png){width="600" align="center"}

最後， **任何有效置信度** 為：

![](assets/statistical_11.png){width="200" align="center"}

## 宣告實驗為結論性

對於雙臂實驗，Journey Optimizer實驗面板顯示一條資訊，指出實驗 **結論** 當任何有效置信度超過95%時（即任何有效時間） `p`-value低於5%)。

當存在兩個以上變數時，應用Bonferonni校正來控制家庭誤差率。 為了進行 `K` 和單基線（對照）治療， `K-1` 獨立假設test。 Bonferonni修正意味著，如果在任何有效時間，則我們拒絕控制與給定變數具有相等均值的零假設 `p`-value（上面定義）低於閾值 `α/(K-1)`。

## 最佳手臂

當實驗被確定時，顯示最佳效能臂。 這是具有最佳效能（最高平均或轉換率）的臂，在包括控制項的集合中，以及具有 `p`低於Bonferonni閾值的 — value。
