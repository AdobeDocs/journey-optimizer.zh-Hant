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
source-git-commit: 5592f564456edf86e04dc9849c947402126cf161
workflow-type: tm+mt
source-wordcount: 2234
ht-degree: 85%

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

## 2026年9月更新 {#sep-26-updates}

### 歷程 {#sep-26-journeys}

<table>
<thead>
<tr>
<th><strong>歷程層級保留 (有限可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以直接從歷程屬性設定歷程的保留群組。 保留群組是目標客群中可設定的百分比，這會被排除在歷程之外，且不會收到任何訊息。 將保留設定檔與 Customer Journey Analytics 報告中的現用設定檔進行比較，即可測量歷程帶來的增量提升度 (實際影響)。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。 如需發行週期與可用性階段的完整詳細資訊，請參閱 <a href="releases.md">Journey Optimizer 發行週期</a>。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-properties.md#performance-management">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年9月1日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在歷程中使用AI產生運算式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程進階運算式編輯器現在整合了AI支援的運算式產生：說明您要以自然語言建置的運算式，而編輯器產生您可以立即套用或通過後續提示調整的現成程式碼。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/expression/generate-expression.md">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年9月1日</p>
</td>
</tr>
</tbody>
</table>

* **歷程運算式編輯器中的新dateDiff函式** — 歷程運算式編輯器現在包含`dateDiff`函式，以天數計算兩個日期之間的差異。 此函式適用於以時間為基礎的邏輯，例如建立截止日期、計算客戶生命週期持續時間或在歷程條件中建立倒數計時器。  [了解更多](../building-journeys/functions/date-functions.md#dateDiff)

  推出日期： 2026年9月1日

### 行銷活動 {#sep-26-campaigns}

+++ 即將推出 — **下列資訊可能會有變更。**

<table>
<thead>
<tr>
<th><strong>動作行銷活動中的傳入體驗模擬</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以於上線前，在動作行銷活動中模擬傳入管道動作。 使用模擬模式，透過模擬使用者測試您的設定並預覽呈現的體驗 (包括產生的 URL 和 QR 碼)，讓您可以端到端驗證規則、決策機制與內容呈現。</p>
<p>此功能目前為 Private Beta 版本，僅供特定組織使用。 請聯絡您的 Adobe 代表以取得更多資訊。</p>
<p>推出日期： 2026年9月4日</p>
</td>
</tr>
</tbody>
</table>

* **動作行銷活動的資料夾** — 您現在可以將動作行銷活動整理到資料夾中，以改善介面中的導覽和管理。

* **動作行銷活動編寫流程重新設計** - Adobe Journey Optimizer 動作行銷活動編寫流程已重新設計，提供更直覺、高效且順暢的使用者體驗。

* **覆寫動作行銷活動中的預設執行欄位** — 您現在可以覆寫動作行銷活動引數中針對電子郵件、簡訊和WhatsApp傳遞全域設定的預設執行欄位（先前可在歷程層級使用）。

+++

## 2026 年 8 月發行說明 {#aug-26-updates}

### 內容管理

下列功能和改進功能已引進到此版本的內容管理。

<table>
<thead>
<tr>
<th><strong>AI 內容產生的彈性影像來源</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Journey Optimizer 中產生內容時，現在會直接從 Adobe Experience Manager Assets Essentials 及以上版本中，取得品牌核准的影像。 可透過三種模式控制平衡：平衡 (數位資產管理優先、AI 填補缺口、預設)、資產 (數位資產管理來源) 和創意 (AI)。</p>
<p><img src="../content-management/assets/image-mode-3.png"></p>
<p>如需詳細資訊，請參閱<a href="../content-management/generative-uc.md#image-mode">詳細文件</a>以了解詳情。</p>
<p> 推出日期：2026 年 8 月 5 日</p>
</td>
</tr>
</tbody>
</table>

* **內容變體大小警告** - 當內容變體超過建議大小臨界值時，Journey Optimizer 現會顯示軟性限制警告，範本和訊息為 1200 KB、片段為 700 KB、登陸頁面為 1000 KB。 儲存和發佈不受封鎖。 [了解更多](../start/guardrails.md#content-authoring)

  推出日期： 2026年8月25日

* **內容中的片段數量限制** - Journey Optimizer 現在會驗證一段內容中所使用的不重複片段數量：每個版本最多可使用 60 個片段，而單一訊息的所有版本合計最多可使用 120 個片段。 當達到各項限制的 75% 時，將顯示警告訊息；一旦達到上限，即無法發佈。 [了解更多](../start/guardrails.md#fragments-guardrails)

  推出日期： 2026年8月25日

### 歷程 {#aug-26-journeys}


* **歷程標頭中的開始和結束日期** - 當歷程設定了開始及/或結束日期時，這些日期現在會顯示在即時狀態徽章旁邊的歷程頁首中。 顯示的標籤會根據每個日期是即將到來或是已過去而調整。 [閱讀更多](../building-journeys/journey-properties.md#dates)

  推出日期： 2026年8月20日

* **進階運算式編輯器中的新清單函數** - 進階運算式編輯器中現已提供兩個新函數：`mergeLists` 可合併兩個清單 (無論是否進行重複資料刪除)，而 `differenceLists` 會傳回存在於一個清單，但不存在於另一個清單中的項目。 [了解更多](../building-journeys/functions/list-functions.md)

  推出日期：2026 年 8 月 13 日

* **等待活動中的傳送時間最佳化** - 等待活動現已支援傳送時間最佳化，讓 Adobe 的 AI 決定繼續任何下游活動的最佳時間。 [了解更多](../building-journeys/wait-activity.md#sto-wait)

  推出日期：2026 年 8 月 13 日

### 行銷活動 {#aug-26-campaigns}

下列功能和改進功能已引進到此版本的行銷活動。

<table>
<thead>
<tr>
<th><strong>API 觸發的電子郵件中的個人化 PDF 附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 現在於 API 觸發的行銷活動中，支援每封電子郵件總共最多<b>五個 PDF 附件</b>，包含靜態和特定收件者的 PDF。 特定收件者的 PDF 檔案會從資料登陸區域安全地擷取，並在傳送時附加，每個檔案的位置都直接在 API 承載資料中傳遞。 這可讓現有的上游文件產生系統維持原狀，由 Journey Optimizer 處理傳送。</p>
<p>支援的使用案例包括發票、對帳單、票證、合約、寄件標籤，以及其他依收件者而異的類似文件。 個人化 PDF 附件僅適用於交易型 API 觸發的電子郵件行銷活動，在歷程或協調的行銷活動中並不支援。</p>
<p>PDF 附件附加元件支援較大的附件數量與大小；如需詳細資訊，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../email/pdf-attachments.md#personalized-attachments">詳細文件</a>以了解詳情。</p>
<p>推出日期：2026 年 8 月 12 日</p>
</td>
</tr>
</tbody>
</table>

* **個別行銷活動生命週期警報訂閱** - 除了現有的沙箱層級訂閱之外，您現在也可以訂閱單一行銷活動支援的行銷活動生命週期警報。 這可讓您監視個別高優先順序的行銷活動，而不會收到沙箱中每個行銷活動的相同警報。 [了解更多](../reports/alerts.md#subscribe-alerts)

  推出日期：2026 年 8 月 13 日

### 協調的行銷活動 {#august-26-oc}

下列功能和改進功能已引進到此版本的協調行銷活動。

<table>
<thead>
<tr>
<th><strong>支援「非傳送時間」</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以套用「非傳送時間」。 「非傳送時間」可讓您定義以時間為基礎的排除項目，以防止訊息在特定時段內傳送，協助您在行銷活動協調流程使用案例中，尊重客戶的偏好設定和合規性要求。</p>
<p>如需詳細資訊，請參閱<a href="../conflict-prioritization/quiet-hours.md">詳細文件</a>以了解詳情。</p>
<p>推出日期：2026 年 8 月 18 日</p>
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
<p>您現在可以排程傳出訊息，在一段時間內以受控批次方式傳送。 波段傳送極為適合大批次或具時效性的行銷活動，它具備更好的傳遞能力，並透過降低被標記為垃圾郵件的風險，協助維持良好的寄件者信譽。 </p>
<p>如需詳細資訊，請參閱<a href="../delivery/send-using-waves.md">詳細文件</a>以了解詳情。</p>
<p>推出日期：2026 年 8 月 18 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>LINE 管道支援 (有限可用性)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將 LINE 動作新增至您的協調行銷活動。 這項新活動可讓您建立及提供高度個人化的內容 (包括文字、貼圖、影像、影片、位置資料以及豐富的 Flex 訊息)，以便在 LINE 平台上順暢地與您的客戶互動。 此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/activities/channels.md">詳細文件</a>以了解詳情。</p>
<p>推出日期：2026 年 8 月 12 日</p>
</td>
</tr>
</tbody>
</table>

* **管理輪廓目標維度的功能** - 您現在可以刪除輪廓目標維度，或編輯並更換其設定的身分識別命名空間，讓您對資料設定擁有更高的控制力與彈性。 [了解更多](../orchestrated/target-dimension.md)

  推出日期：2026 年 8 月 18 日

<!-- * **New public APIs** - New API specifications are now available. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines. Documentation link: TBD -->

* **針對每個收件者與行銷活動個人化電子郵件寄件者詳細資料 (可用性限制)** - 協調的行銷活動現在支援使用輪廓屬性或關聯資料，個人化電子郵件標頭欄位 (包括寄件者姓名、寄件者電子郵件前置詞、回覆姓名和回覆電子郵件，以及執行地址)。 如此一來，寄件者詳細資料就能反映每個收件者的相關顧問、位置或分支，而非透過單一公司地址路由所有傳送。 可在管道層級設定標頭值，並使用內容資料覆寫每個行銷活動，以獲得更精確的控制。 [了解更多](../orchestrated/activities/channels.md#configuration)

  此功能僅適用於一組組織 (可用性限制)。

  推出日期：2026 年 8 月 18 日

* **目標維度簡化** - 工作流程畫布上現在會顯示作用中的目標選擇維度，以便您檢視管道活動使用的維度。 多實體細分流程變得更加簡化，因為您不再需要獨立的「變更維度」活動。 此外，您現在可以明確選擇訊息是在輪廓層級還是在次要維度層級傳送。 [了解更多](../orchestrated/activities/channels.md#add)

  推出日期：2026 年 8 月 18 日

### 忠誠度 {#aug-26-loyalty}

<table>
<thead>
<tr>
<th><strong>熟客分析技能</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer推出<strong>忠誠度深入分析</strong>，這是CX同事的新技能，可詢問有關挑戰效能的問題以及擷取到Adobe Experience Platform中忠誠度欄位群組中的其他忠誠度計畫資料。</p>
<p>如需詳細資訊，請參閱<a href="../start/ajo-coworker-skills.md#loyalty-skills">詳細文件</a>以瞭解詳情。</p>
<p>推出日期： 2026年8月31日</p>
</td>
</tr>
</tbody>
</table>

### 管道 {#august-26-channels}

* **即時活動執行中繼資料 (executionMetadata)** - 由 API 觸發的即時動態行銷活動 (交易型和行銷型)， 現在支援為每個收件者設定選用的 executionMetadata 欄位。 這可讓您將自訂索引鍵/值資料 (例如訂單 ID、忠誠度層級或區域代碼) 附加至執行。 [了解更多](../mobile-live/create-mobile-live.md#metadata)

  推出日期：2026 年 8 月 19 日

* **推播輸送量效能附加元件** - API 觸發的行銷活動中，現已提供全新高輸送量的交易型傳訊模式。 此模式專為大規模即時交易型傳訊而設計，最高可支援每秒 5,000 筆交易，而且可用性更高。 此功能先前僅適用於電子郵件管道，現在對於已購買「Adobe 高輸送量交易型傳訊」附加產品的組織，推播管道也已提供此功能。 請聯絡您的 Adobe 代表以取得更多資訊。 [了解更多](../campaigns/api-triggered-high-throughput.md)

  推出日期：2026 年 8 月 11 日

### 設定 {#august-26-configuration}

* **在自訂子網域設定的CSR產生中支援多個SAN** — 使用自訂委派方法來設定或移轉自訂子網域時，現在會自動產生`data.{subdomain}`和`cdn.{subdomain}`憑證簽署要求(CSR)做為主體替代名稱(SAN)。 先前產生的CSR僅包含`data.{subdomain}`，在提交至憑證授權單位之前需要手動新增`cdn.{subdomain}`。 [了解更多](../configuration/custom-subdomain-migration.md#send-csr-to-ca)

  推出日期： 2026年8月20日

### 決策 {#decisioning-august}

* **決策中的刊登層級頻率上限** - 決策中的頻率上限規則現在可以將範圍套用至個別刊登，讓您能更精確地控制產品建議在指定介面中的顯示頻率。 提供兩種模式：**特定刊登上限**，定義僅在所選刊登位置顯示產品建議時才套用的上限；以及&#x200B;**個別刊登上限**，就產品建議出現的每個刊登位置獨立套用上限，因此每個刊登都會維持自己的上限計數器。 請注意，與位置相關的上限不適用於使用以Adobe Experience Platform資料為基礎的規則來設定上限的優惠方案。 [了解更多](../experience-decisioning/items.md#capping)

  推出日期： 2026年8月24日

* **視覺片段中的鏡像頁面** - 您現在可以將鏡像頁面插入視覺片段中。 即使片段用於採用決策功能的電子郵件行銷活動中，決策屬性仍可在鏡像頁面連結上正確呈現。 必須在發佈片段之前，先將鏡像頁面新增到視覺片段，才能顯示決策屬性。 [了解更多](../email/message-tracking.md#decisioning-mirror-page)

  推出日期：2026 年 8 月 11 日

### 可用性改進功能 {#august-26-usability}

* **新歷程畫布中的多重選取** - 新歷程畫布體驗引進簡化的多重節點選取方式：按住 Shift 鍵並拖曳可同時選取多個節點，無需逐一個別選取。 這讓您能夠在數個節點上有效地執行大量動作 (例如複製、刪除或儲存為歷程片段) 。 [了解更多](../building-journeys/using-the-journey-designer.md#canvas-capabilities)

  推出日期：2026 年 8 月 17 日

* **歷程詳細目錄中的大量作業** - 您現在可以直接從歷程詳細目錄清單執行全新的大量動作，讓您能更快速地一次管理多個歷程。 選取多個歷程，只需一個步驟即可套用下列任何新動作：**新增至套件**、**刪除**、**移至資料夾**、**編輯標記**&#x200B;或&#x200B;**管理存取權**。 這讓團隊無需再逐一對每個歷程重複相同的動作，簡化了需管理大量歷程之團隊的歷程管理流程。 [了解更多](../building-journeys/journey-ui.md)

  推出日期：2026 年 8 月 12 日

* **內容測試的新內容模擬體驗** - **模擬內容**&#x200B;工作流程引入重新設計的體驗：所有變體現在都會在單一可捲動網格 (並排、堆疊或自動換行版面) 中一起呈現，取代過去一次僅能檢視單一變體的方式。 單一底部動作列整合了測試變體之間的導覽、縮放、檢視區切換 (桌面/行動裝置)、地區設定切換、新增範例輸入、使用 AI 產生變體、挑選並儲存模擬使用者，以及匯入或匯出變體。 移除左側邊欄並收合額外的頁首分層，可大幅增加預覽的空間。 底部動作列中的&#x200B;**切換至傳統體驗**&#x200B;選項可讓您隨時恢復至先前的體驗。 [了解更多](../test-approve/simulate-content-variations.md)

  推出日期：2026 年 8 月 11 日


