---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: 透過Experimentation Accelerator在AI中使用資料
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: 內容，實驗，多個，對象，處理
hide: true
hidefromtoc: true
source-git-commit: 50dcdd30e21fe1b12d502a2b9c478f4ceb546c49
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# 透過Experimentation Accelerator在AI中使用資料{#experiment-accelerator-security}

>[!BEGINSHADEBOX]

* [開始使用Experimentation Accelerator](experiment-accelerator.md)
* [透過Experimentation Accelerator在AI中使用資料](experiment-accelerator-security.md)
* [Experimentation Accelerator最佳作法](experiment-accelerator-best-practices.md)
* [監視實驗](experiment-accelerator-monitor.md)
* [實驗中的量度](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

**Adobe Journey Optimizer Experimentation Accelerator**&#x200B;可讓您自動探索深入見解，並推薦機會以改善您的實驗與實驗計畫。 解決方案利用AI和機器學習來提供這些建議。 此陳述式說明您客戶的資料在&#x200B;**Experimentation Accelerator**&#x200B;中的使用方式。

## 實驗加速器使用哪些資料？

目前有&#x200B;**實驗加速器**&#x200B;使用的三種資料型別：

* **實驗中繼資料**：實驗名稱、實驗中所使用對象的定義，以及實驗中的處理，例如名稱、分割百分比、提供實驗的位置或表面。

* **處理的效能**：人數、成功量度的平均值以及每個處理的標準差。

* **處理的內容**：呈現的HTML和處理的熒幕擷圖，如同使用者在您網站上看到的畫面。

## 實驗加速器會如何處理這些資料？

**實驗加速器**&#x200B;會取得每項處理的內容，並建立內嵌（即內容的數學表示），然後將這些內嵌與處理的效能相互關聯。 此程式可擷取表現最佳以供日後使用的內容屬性。 這些屬性接著會傳入由Adobe託管的大型語言模型，再轉換為人類可讀的陳述式，用來產生深入見解及建議商機。

## Experimentation Accelerator對所使用的資料有何限制？

每個客戶都會指派至特定的組織和沙箱。 每個沙箱都會培訓專屬的模型。 刪除沙箱時，所有相關的資料、訊號和模型都會永久移除。

* 我們只會使用客戶資料來訓練或微調該客戶的模型。

* 我們絕不會混合客戶來訓練或微調模型。

## Adobe模型或AI會自動變更品牌的使用者體驗嗎？

不可以。 **Experimentation Accelerator**&#x200B;僅針對可變更的專案及變更方式提供建議。 只有有權使用Journey Optimizer或Target變更體驗的使用者才能根據這些建議採取行動。 所有建議都可以在推出前進行檢閱和編輯。

## 他們的資料或系統穩定性是否有任何風險？

**Experimentation Accelerator**&#x200B;僅擷取和分析資料，產生見解和建議以供未來測試。 無法修改任何測試設定。 工具內產生的所有建議都會傳送至Target和Journey Optimizer進行實作，確保對客戶的目前活動沒有影響。
