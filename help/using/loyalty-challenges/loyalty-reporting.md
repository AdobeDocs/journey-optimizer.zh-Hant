---
solution: Journey Optimizer
product: journey optimizer
title: 監視忠誠度挑戰績效
description: 瞭解如何使用忠誠度挑戰報告儀表板來追蹤Adobe Journey Optimizer中的挑戰績效和見解。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="私人測試版" type="Informative"
mini-toc-levels: 1
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 762afe791cc1fa826b7a9f35f6f54591590bab7c
workflow-type: tm+mt
source-wordcount: 592
ht-degree: 4%

---

# 監視忠誠度挑戰績效 {#loyalty-reporting}

>[!BEGINSHADEBOX]

**目錄**

[開始應對忠誠度挑戰](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**建立和管理挑戰**

* [存取及管理挑戰與工作](access-loyalty-challenges.md)
* [創造挑戰](create-challenges.md)
* [建立任務](create-tasks.md)
* **監視忠誠度挑戰績效** ◀︎ **您在這裡**

</td>
<td style="vertical-align:top;">

**設定並整合**

* [設定忠誠度挑戰](loyalty-admin.md)
* [獎勵定義指南](reward-definition-guide.md)
* [事件轉換器指南](event-transformer-guide.md)
* [熟客資料與資料集](loyalty-data-and-datasets.md)
* [忠誠度挑戰API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](../rn/releases.md)。

使用忠誠度挑戰報告來檢視您的挑戰表現如何。 檢視哪些人正在報名、哪些人正在完成挑戰，以及您的計畫產生了多少收入 — 全都集中在一處。 資料來自Adobe Customer Journey Analytics。

若要開啟報告控制面板，請前往Journey Optimizer中的&#x200B;**[!UICONTROL 忠誠度挑戰(Beta)]**，並在左側導覽中選取&#x200B;**[!UICONTROL 忠誠度報告]**。

報告介面有兩個標籤：

* **[報告](#reports-view)**：您面臨的挑戰的數字和圖表。
* **[深入分析](#insights-cards)**：目前值得您關注的重點卡片。

## 報表檢視 {#reports-view}

**報表**&#x200B;索引標籤提供您程式在選定期間執行方式的概觀。 使用頁面頂端的日期選擇器並選取&#x200B;**[!UICONTROL 套用篩選器]**&#x200B;按鈕，以變更報告期間並檢視更新的數字和圖表。

![](assets/reporting-challenge-key.png)

**關鍵量度**&#x200B;區域一下子會顯示四個數字。 每個量度也會顯示和上一個時段相比的百分比變化。

* **熟客方案成員**：期間有多少熟客方案成員在作用中。
* **挑戰註冊**：會員已註冊多少次挑戰。
* **收入**：與挑戰活動相連結的總收入。
* **平均完成率**：完成至少一項挑戰的已註冊成員百分比。

右邊的&#x200B;**最新深入分析**&#x200B;面板會顯示您的程式中由AI產生的最新深入分析。 選取「**[!UICONTROL 檢視全部]**」以開啟完整的&#x200B;**深入分析**&#x200B;索引標籤。

在關鍵量度底下，**挑戰**&#x200B;區段提供您兩個挑戰活動的檢視。

![](assets/reporting-challenge-challenges.png)

* **挑戰參與**：此時間表會顯示該期間有多少成員已開始、正在進行中，以及已完成挑戰。
* **挑戰報告**：包含型別、任務、狀態和註冊號碼等詳細資訊的所有挑戰表格。 使用搜尋列尋找特定挑戰。 選取挑戰，以檢視其包含參與趨勢和績效詳細資訊的完整報告。

  +++挑戰報告範例

  ![](assets/reporting-challenge-report.png)

  +++

## 深入分析索引標籤 {#insights-cards}

**Insights**&#x200B;標籤會顯示AI產生的卡片，其中標示熟客方案中的異常、趨勢和機會。 每張卡片都代表單一觀察結果，並依據其與目前方案資料的關聯程度進行排名。

![](assets/reporting-insights.png)

右上角的&#x200B;**上次抓取時間**&#x200B;時間戳記會顯示insight引擎上次處理您程式資料的時間。

### 卡片動作 {#insight-card-actions}

每個卡片都有![](assets/do-not-localize/Smock_More_18_N.svg)功能表，其中包含兩個動作：

* **解除**：從深入分析清單中永久移除卡片。
* **暫停**：暫時隱藏卡片。 選擇暫停&#x200B;**1天**、**3天**&#x200B;或&#x200B;**7天**。 在暫停期間結束後，卡片會重新出現。

<!--
### Priority badges {#insight-badges}

Each card has a priority badge — **High**, **Medium**, or **Low** — based on how significant the underlying signal is relative to your current program data. These levels are relative: there are always a few **High** cards, even in a quiet week. **High** means "most relevant right now", not that a fixed threshold was crossed.
-->

### 類別標籤 {#insight-category-tags}

每個卡片都含有&#x200B;**類別標籤**，用於識別insight相關的程式部分。

| 類別 | 涵蓋範圍 |
| --- | --- |
| **整個程式** | 忠誠計畫的整體健康狀況和績效 |
| **層級** | 跨成員層級賺取比率、移動和分配 |
| **挑戰** | 特定挑戰或跨挑戰的活動、完成率和異常 |
| **產品** | 產品目錄績效，包括檢視、贖回和目錄層級趨勢 |
| **成員生命週期** | 成員在註冊、參與和流失階段中的進度 |
| **趨勢** | 以時間為基礎的模式，例如，每週週期、季節性尖峰或趨勢逆轉 |
