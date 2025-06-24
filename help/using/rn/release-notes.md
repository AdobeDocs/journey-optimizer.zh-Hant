---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7e378cbda6ee2379a8bd795588c328cb14107aa4
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 72%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="有哪幾種新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會整合到每月最後一週的發行說明一起發表。[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。


## 2025年6月發行說明 {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**發行日期**：2025 年 6 月 18 日

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### 全新功能 {#25-06-features}

此版本隨附的新功能詳述如下。


<table>
<thead>
<tr>
<th><strong>RCS 傳送訊息</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 目前有支援進階通訊解決方案 (RCS) 傳訊，可根據提供者、電信業者支援，啟用下列增強傳送訊息的功能：</p>
<ul>
<li>有品牌、已驗證寄件者支援：使用具有品牌化元素（標誌、寄件者名稱等）的已驗證企業檔案，可以用來來傳送訊息。</li>
<li>訊息傳遞洞察力：接收包括訊息狀態更新（例如已傳送、已傳遞、已讀取）等詳細傳遞報告。</li>
<li>連結追蹤：請在 RCS 訊息中內嵌、追蹤網址，以便進行參與分析。</li>
<li>遞補簡訊：當設定檔的裝置暫不支援 RCS，或是暫時無法透過 RCS 連線時，系統會自動回覆簡訊。</li>
<li>基本訊息構成：傳送包含選擇性媒體、豐富元素的文字型 RCS 訊息，會視供應商支援而定。</li>
</ul>
<p>如需詳細資訊，請參閱<a href="../sms/sms-configuration.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>程式碼型體驗內容中的表單欄位</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以立即到 JSON 或 HTML 內容範本中，定義特定可編輯欄位，即便不是技術使用者，也能輕鬆地在製作程式碼型體驗頻道上的表單檢視中編輯內容，不用要操作任何程式碼。<br />此外，當定義程式碼型體驗內容範本時，目前可以在範本中插入決定原則，增加可重複使用性，方便使用。</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>如需詳細資訊，請參閱<a href="../code-based/code-based-form-fields.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>歷程中的內容決定活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以透過歷程畫布中的專用內容決定活動，將個人化優惠方案納入您的歷程，並在歷程活動（包括條件和自訂動作）中使用。</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>此功能僅適用於某個組織（可用性限制），可在全球推出未來的版本。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/content-decision.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程試運行</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程試運行是 Adobe Journey Optimizer 中的特殊歷程發佈模式，允許歷程從業人員使用真實的生產資料，即可測試歷程，不用聯絡實際客戶，或是更新設定檔資訊。此功能可協助歷程從業人員，針對歷程設計、客群目標市場選擇，累積信心，然後再將歷程發佈上線。</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>此功能僅適用於某個組織（可用性限制），可在全球推出未來的版本。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-dry-run.md">詳細文件</a>。</p>

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>暫停並繼續歷程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您立即可以暫停，繼續歷程。在不中斷客戶體驗的情況下，此功能可讓歷程從業人員暫時暫停即時歷程，藉此提供更大控制力，帶來更多彈性。 暫停時，系統就不會傳送任何通訊，設定檔會維持在暫停狀態，直到繼續歷程為止。</p>
<p>您只能暫停並繼續單一歷程，或可執行大量暫停，然後繼續另一組歷程操作。</p>
<p>此外，您還可以將全域篩選器套用至已暫停歷程，即可根據屬性排除設定檔。</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>此功能僅適用於某個組織（可用性限制），可在全球推出未來的版本。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/journey-pause.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>提高實驗勝率</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>擴大實驗獲勝者的規模，讓您能夠透過自動或手動方式，將實驗的獲勝變化版本推廣給所有客群參考。此功能可確保一旦確定高績效人才，您就可以大幅提高影響力和效率，不必再不斷進行人工監督。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/content-experiment.md">詳細文件</a>。</p>
<p>推出日期：2025 年 6 月 2 日</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>衝突與優先順序</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>請在 Journey Optimizer 中，管理行銷活動和歷程流量和時間非常重要，才能避免過多的互動，給客戶帶來負擔。Journey Optimizer 目前有提供幾種可用於衝突管理和優先排序的工具，以前只適用於有限存取 (LA) 組織 - 現已普遍開放使用 (GA)。</p>
<p>此功能之前以 [限量] 的名義發行，目前所有環境都可以使用。 已在此一般可用性版本中，引進以下增強功能：</p>
<ul>
<li>擴展支援：除了閱讀受眾歷程之外，衝突管理工具目前還有支援單一歷程和受眾資格歷程。</li>
<li>改善的疑難排解：查詢服務中目前有提供兩種新的步驟事件欄位，讓您能分析設定檔遭到歷程或行銷活動拒絕的原因。</li>
<li>增強報告：報告目前可以指定哪些特定規則會將設定檔排除在歷程，或是行銷活動之外，提供更高透明度和可操作的洞察力。</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>如需詳細資訊，請參閱<a href="../conflict-prioritization/gs-conflict-prioritization.md">詳細文件</a>。</p>
<p>推出日期：2025 年 6 月 3 日</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>決策中的Adobe Experience Platform資料集（測試版）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform資料集以前可用於個人化，現在可用於決策。 這可讓您將決策屬性的定義擴充至資料集中的其他資料，以便定期變更的大量更新，而無需一次手動更新一個屬性。 例如，可用性、等待時間等。</p>
<p>只要是客戶都可在公開測試版中，使用此功能。如果您想要存取此功能，請聯絡您的客戶代表</p>
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/aep-data-exd.md">詳細文件</a>。</p>
<p>推出日期： 2025年6月20日</p>
</td>
</tr>
</tbody>
</table>

### 改良功能 {#25-06-improv}

以下列舉部分發布內容附上的改良功能。

* **頻道規則集**

   * **上限的自訂持續時間視窗** — 新的&#x200B;**Every**&#x200B;欄位現在可在頻道規則集設定畫面中使用，可讓您根據指定的持續時間，在多天、幾週或幾個月內套用頻率上限規則。

   * **每小時重設上限頻率** — 您現在可以每小時為管道規則集套用上限。 此功能僅適用於一組組織 (可用性限制)。 請連絡您的客戶服務以啟用它。

   * **每日持續時間** — 先前在「有限可用性」中提供，現在所有客戶都可以使用管道規則集中的「每日」頻率上限。

  如需詳細資訊，請參閱[詳細文件](../conflict-prioritization/channel-capping.md)。

* **程式碼型體驗**

   * 現在可在程式碼型體驗內容範本中新增決定原則，以便用於利用可編輯表單欄位中的優惠方案。 [閱讀全文](../code-based/code-based-form-fields.md)

   * 從程式碼型體驗歷程或行銷活動版本畫面，您現在可以直接新增決定原則，無需開啟個人化編輯器。 [閱讀全文](../code-based/create-code-based.md#edit-code)

* **電子郵件設計工具的自訂 CSS 支援**

  Journey Optimizer現在可讓您直接在電子郵件Designer中，將自訂CSS新增至您的電子郵件內容。 [閱讀全文](../email/custom-css.md)

* **新的行銷活動索引標籤式導覽**

  新的導覽模式可讓您更快速地存取內容製作，並支援在行銷活動中進一步擴充設定。 [閱讀全文](../campaigns/create-campaign.md)

* **Decisioning**

   * **沙箱複製和決策** （推出日期：2025年6月3日） — 決策物件現在可以在沙箱之間複製，精簡測試和部署工作流程。 [閱讀全文](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **決策規則的決策專案屬性支援** （推出日期：2025年6月4日） — 您現在可以運用決策專案屬性來建立決策規則。 [閱讀全文](../experience-decisioning/rules.md#create)

* **互動式訊息執行 API 更新** — 推出日期：2025 年 6 月 6 日

  互動式訊息執行 API 讓您可以立即刪除即將執行的行銷活動排程。[閱讀全文](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
