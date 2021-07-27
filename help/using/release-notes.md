---
title: 發行說明
description: Journey Optimizer 發行說明
source-git-commit: 4d3352184aac7fe19096c21650982e29506f2bff
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 24%

---


# 發行說明 {#release-notes}

本頁面列出 Journey Optimizer 的所有新功能和改善項目。
您也可以參閱最新的[文件更新](documentation-updates.md)。

## 2021年7月發行 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>利用架構關係</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform可讓您定義結構間的關係，以使用一個資料集作為另一個資料集的查閱表格。 Journey Optimizer現在可以運用來自連結結構的資料。</p>
<p>這些欄位可用於統一事件設定、歷程條件、訊息個人化和自訂動作個人化。</p>
<p>如需詳細資訊，請參閱<a href="event/experience-event-schema.md#leverage_schema_relationships">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>允許的清單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在沙箱層級定義特定的傳送安全清單，以避免在測試環境中傳送不想要的電子郵件給收件者。
</p>
<p>如需詳細資訊，請參閱<a href="allow-list.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改良功能

* 在同一沙箱中同時執行的所有讀取區段的總節流率限制為每秒17,000條訊息。 [閱讀全文](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* 已從資料源配置窗格中刪除&#x200B;**快取持續時間**&#x200B;欄位。 [閱讀全文](datasource/about-data-sources.md)
* 對於外部資料來源，現在會自動定義每秒15次呼叫的上限規則。 [閱讀全文](configuration/external-systems.md#capping)
* 對於即時歷程，歷程屬性畫面現在會顯示發佈日期和發佈歷程的使用者名稱。 [閱讀全文](building-journeys/journey-gs.md#change-properties)
* 在歷程清單畫面中，已新增歷程類型篩選器。 [閱讀全文](user-interface.md#section_lgm_hpz_pgb)
* 已在讀取區段活動中新增[!UICONTROL Throttling rate]參數。 [閱讀全文](building-journeys/read-segment.md#configuring-segment-trigger-activity)
