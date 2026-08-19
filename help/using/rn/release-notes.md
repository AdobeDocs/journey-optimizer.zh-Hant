---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 2be0ef1b72affb0423613d60a3b8eedbcc92ac6d
workflow-type: tm+mt
source-wordcount: 1436
ht-degree: 24%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="最新資訊"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能，並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer] 遵循持續傳遞模式，允許 Adobe 持續傳遞新功能、增強功能和修正。 此方法可讓您分階段推出可擴充的功能，以確保所有環境的效能和穩定性。 基於此模型，發行說明會在每月發行之間更新。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](releases.md)。

[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。 若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

>[!NOTE]
>
>這些發行說明中列出的功能包括&#x200B;**可用日期**，指出每個變更在您的環境中可用的時間。 **即將推出**&#x200B;摺疊式版面中的項目預計將在未來幾天或幾週內推出。 這些部分的資訊可能會有變更。

## 2026年8月發行說明 {#aug-26-updates}

<!--
### Loyalty {#aug-26-loyalty}

<table>
<thead>
<tr>
<th><strong>Loyalty Insights skill</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer introduces <strong>Loyalty Insights</strong>, a new CX Coworker skill for asking questions about challenge performance and other loyalty program data ingested into the Loyalty field groups in Adobe Experience Platform.</p>
<p>For more information, refer to the <a href="../start/ajo-coworker-skills.md">detailed documentation</a>.</p>
<p>Availability date: August 12, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

### 內容管理

下列功能和改善已在此版本中匯入到內容管理。

<table>
<thead>
<tr>
<th><strong>AI內容產生的彈性影像來源</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在Journey Optimizer中產生內容現在會直接從Adobe Experience Manager Assets Essentials等來源取得品牌核准的影像。 三種模式可控制平衡：平衡（數位資產管理優先、AI填補差距、預設）、Assets （數位資產管理來源）和Creative (AI)。</p>
<p><img src="../content-management/assets/image-mode-3.png"></p>
<p>如需詳細資訊，請參閱<a href="../content-management/generative-uc.md#image-mode">詳細文件</a>以瞭解詳情。</p>
<p> 推出日期： 2026年8月5日</p>
</td>
</tr>
</tbody>
</table>

### 歷程 {#aug-26-journeys}

* **進階運算式編輯器中的新清單函式** — 進階運算式編輯器中有兩個新函式： `mergeLists`會結合兩個清單（無論是否重複資料刪除），且`differenceLists`會傳回一個清單中不存在另一個清單的專案。 [了解更多](../building-journeys/functions/list-functions.md)

  推出日期： 2026年8月13日

* **等待活動中的傳送時間最佳化** — 等待活動現在提供傳送時間最佳化，讓Adobe的AI決定繼續任何下游活動的最佳時間。 [了解更多](../building-journeys/wait-activity.md#sto-wait)

  推出日期： 2026年8月13日

### 行銷活動 {#aug-26-campaigns}

此版本已為Campaigns引進下列功能和改善。

<table>
<thead>
<tr>
<th><strong>API觸發的電子郵件中的個人化PDF附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在在API觸發的行銷活動中，支援每封電子郵件最多<b>5個PDF附件</b>，包含靜態和收件者特定的PDF。 收件者特定的PDF檔案會從資料登陸區域安全擷取，並在傳送時附加，每個檔案的位置都直接在API裝載中傳遞。 這可讓現有的上游檔案產生系統維持原狀，由Journey Optimizer處理傳送。</p>
<p>支援的使用案例包括發票、對帳單、票證、合約、出貨標籤，以及依收件者而異的類似檔案。 個人化PDF附件僅適用於異動API觸發的電子郵件行銷活動，在歷程或協調的行銷活動中不支援。</p>
<p>PDF附件附加元件支援較大的附件數量與大小；如需詳細資訊，請聯絡您的Adobe代表。</p>
<p>如需詳細資訊，請參閱<a href="../email/pdf-attachments.md#personalized-attachments">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年8月12日</p>
</td>
</tr>
</tbody>
</table>

* **每個行銷活動生命週期警報訂閱** — 除了現有的沙箱層級訂閱之外，您現在可以訂閱單一行銷活動支援的行銷活動生命週期警報。 這可讓您監視個別高優先順序的行銷活動，而不會收到沙箱中每個行銷活動的相同警報。 [瞭解更多](../reports/alerts.md#subscribe-alerts)
推出日期： 2026年8月13日

### 協調的行銷活動 {#august-26-oc}

此發行版本中，Orchested Campaigns已引進下列功能和改善。

<table>
<thead>
<tr>
<th><strong>無訊息小時支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以套用安靜時間。 「無訊息時間」可讓您定義以時間為基礎的排除專案，以防止訊息在特定期間傳送，協助您在行銷活動協調使用案例中遵守客戶偏好設定和合規性要求。</p>
<p>如需詳細資訊，請參閱<a href="../conflict-prioritization/quiet-hours.md">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年8月18日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用波段傳送</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以排程輸出訊息，以控管批次傳送一段時間。 波次傳送也支援更好的傳遞能力，並降低被標籤為垃圾訊息的風險，有助於維持強大的寄件者信譽，是高流量或時間敏感型行銷活動的理想選擇。 </p>
<p>如需詳細資訊，請參閱<a href="../delivery/send-using-waves.md">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年8月18日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE頻道支援（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以新增LINE動作至您的協調行銷活動。 這項新活動可讓您建立及提供高度個人化的內容，包括文字、貼圖、影像、影片、位置資料和豐富的Flex訊息，以便在LINE平台上順暢地吸引您的客戶。 此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/activities/channels.md">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年8月12日</p>
</td>
</tr>
</tbody>
</table>

* **管理設定檔目標維度的功能** — 您現在可以刪除設定檔目標Dimension，或編輯並交換其設定的身分名稱空間，讓您對資料設定有更優異的控制權和彈性。 [了解更多](../orchestrated/target-dimension.md)

  推出日期： 2026年8月18日

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **個人化每個收件者和行銷活動的電子郵件寄件者詳細資料（可用性限制）** — 協調的行銷活動現在支援使用設定檔屬性或關聯資料，個人化電子郵件標題欄位，包括寄件者名稱、寄件者首碼、回覆名稱和回覆電子郵件，以及執行地址。 如此一來，寄件者詳細資料就能反映每個收件者的相關顧問、位置或分支，而非透過單一公司地址路由所有傳送。 可在管道層級設定標頭值，並使用內容資料覆寫每個行銷活動，以獲得更精確的控制。 [了解更多](../orchestrated/activities/channels.md#configuration)

  此功能僅適用於一組組織 (可用性限制)。

  推出日期： 2026年8月18日

* **目標維度簡化** — 作用中目標維度現在會顯示在工作流程畫布上，以便您檢視頻道活動使用的維度。 多實體區段流程較簡單，因為您不再需要個別的「變更維度」活動。 此外，您現在可以明確選擇訊息是在設定檔層級還是在次要維度層級傳送。 [了解更多](../orchestrated/activities/channels.md#add)

  推出日期： 2026年8月18日

### 管道 {#august-26-channels}


* **即時活動執行中繼資料(executionMetadata)** - API觸發的即時活動行銷活動（交易和行銷）現在支援每個收件者的可選executionMetadata欄位。 這可讓您將自訂索引鍵/值資料（例如訂單ID、忠誠度層級或區域代碼）附加至執行。 [了解更多](../mobile-live/create-mobile-live.md#metadata)

  推出日期： 2026年8月19日


* **輸送量的效能附加元件 — 推播** — 在API觸發的行銷活動中提供新的高輸送量異動訊息模式。 此模式專為大規模即時交易型傳訊而設計，最高可支援每秒 5,000 筆交易，而且可用性更高。 此功能先前僅適用於電子郵件頻道，現在也可用於推播頻道，適用於已購買Adobe高輸送量異動訊息附加元件產品的組織。 請聯絡您的 Adobe 代表以取得更多資訊。 [了解更多](../campaigns/api-triggered-high-throughput.md)

  推出日期： 2026年8月11日

### 可用性改進功能 {#august-26-usability}

* **歷程詳細目錄中的大量作業** — 您現在可以直接從歷程詳細目錄清單執行新的大量動作，以便更快速地一次管理多個歷程。 選取數個歷程，並在單一步驟中套用下列任何新動作： **新增至封裝**、**刪除**、**移至資料夾**、**編輯標籤**&#x200B;或&#x200B;**管理存取權**。 這降低了一次一個歷程重複相同動作的需求，並簡化了處理大量歷程的團隊的歷程管理。 [了解更多](../building-journeys/journey-ui.md)

  推出日期： 2026年8月12日

* **內容測試的新內容模擬體驗** - **模擬內容**&#x200B;工作流程引入重新設計的體驗：所有變體現在都會在單一可捲動格線（並排、棧疊或包裝的版面）中一起呈現，取代一次一個變體。 單一底部動作列可整合測試變體之間的導覽、縮放、檢視區切換（案頭/行動裝置）、地區設定切換、新增範例輸入、使用AI產生變體、挑選並儲存模擬使用者，以及匯入或匯出變體。 移除左側邊欄並收合額外的頁首圖層可大幅增加預覽的空間。 下方動作列中的&#x200B;**切換為傳統體驗**&#x200B;選項可讓您隨時還原成先前的體驗。 [了解更多](../test-approve/simulate-content-variations.md)

  推出日期： 2026年8月11日

* **新歷程畫布中的多重選擇** — 新歷程畫布體驗引進簡化的多重節點選擇：按住Shift鍵並拖曳以同時選取多個節點，而不是分別選取。 如此一來，大量動作（例如複製、刪除或另存為歷程片段）就能在數個節點上有效執行。 [了解更多](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

  推出日期： 2026年8月17日

### 決策 {#decisioning-august}

* **視覺化片段中的映象頁面** — 您現在可以將映象頁面插入視覺化片段中。 即使片段用於運用Decisioning的電子郵件行銷活動中，決策屬性仍可在映象頁面連結上正確轉譯。 必須在發佈片段之前將映象頁面新增到視覺片段，以便顯示決策屬性。

  推出日期： 2026年8月11日

  [了解更多](../email/message-tracking.md#decisioning-mirror-page)