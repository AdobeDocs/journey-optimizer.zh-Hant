---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4945e2fb37b54683f56ca3b832553345486d0a80
workflow-type: tm+mt
source-wordcount: '1416'
ht-degree: 88%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="有哪幾種新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。所有變更都會整合到每月最後一週的發行說明一起發表。[!DNL Adobe Journey Optimizer] 是原生建置在 [!DNL Adobe Experience Platform] 的並繼承其最新創新和改善項目。若要了解更多有關這些變更的資訊，請參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

## 2025年6月更新 {#25-6-rn}

<table>
<thead>
<tr>
<th><strong>提高實驗勝率</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>縮放您的Experimentation成功者，可讓您自動或手動將實驗的成功變數轉出給完整受眾。 此功能可確保一旦確定高績效人才，您就可以大幅提高影響力和效率，不必再不斷進行人工監督。</p>
<p>如需詳細資訊，請參閱<a href="../content-management/content-experiment.md">詳細文件</a>。</p>
<p>推出日期： 2025年6月2日</p></td>
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
<p>推出日期： 2025年6月3日</p>
</td>
</tr>
</tbody>
</table>

### 改良功能

* **決策** — 推出日期： 2025年6月3日

  可以立即在沙箱之間複製決策物件，以便簡化測試，同時部署工作流程。[閱讀全文](../configuration/copy-objects-to-sandbox.md#decisioning)


## 2025 年 5 月發行說明 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### 全新功能 {#25-05-features}

此版本隨附的新功能詳述如下。

<table>
<thead>
<tr>
<th><strong>行銷活動和歷程庫存的行事曆視圖</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程和行銷活動清單中，目前只有提供行事曆視圖。 行事曆視圖讓您可以透過視覺化方式，呈現個別清單中的所有歷程，同時啟用行銷活動。</p>
<p>此變更目前僅適用於一組組織（可用性限制）。 若要要求存取權，請使用<a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">此表單</a>。</p>
<img src="assets/do-not-localize/calendar.gif">
<p>如需詳細資訊，請參閱下列章節： <a href="../building-journeys/journey-ui.md">瀏覽及篩選您的歷程</a>、<a href="../campaigns/modify-stop-campaign.md">存取行銷活動</a>。</p>
<p>推出日期： 2025年5月28日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager 內容片段整合</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過整合 Adobe Experience Manager 與 Adobe Journey Optimizer，您就可以立即在 Journey Optimizer 內容中，輕鬆使用 Adobe Experience Manager 內容片段。 這種順暢連線讓您能更輕鬆地直接在 Journey Optimizer 中存取，同時使用 AEM 內容。</p>
<p>此功能先前可用於一組有限的組織(LA)，現在為GA，並具備下列增強功能：您現在可以使用編輯器模式，定義片段簽章中的預留位置及對應個人化值。</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>如需詳細資訊，請參閱<a href="../integrations/aem-fragments.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Adobe Experience Manager 動態媒體整合</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dynamic Media 資產現在可直接在 Journey Optimizer 中使用和存取。此整合可讓您：</p>
<ul>
<li>透過即時更新，集中一處管理資產</li>
<li>立即修改資產設定，例如長寬的數字</li>
<li>更新內容並新增個人化欄位，以便自訂動態媒體範本。</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>之前以「限量」的名義發行，目前此功能所有環境都適用（一般可用性）。</p>
<p>如需詳細資訊，請參閱<a href="../integrations/aem-dynamic.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>事件觸發歷程的補充識別碼</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>目前您可以使用輪廓 ID 和其他識別碼（例如訂購 ID、訂閱 ID 或處方 ID）來觸發歷程，即可允許同一設定檔同時出現在同一歷程中許多次。這能啟用某些情境，同時管理許多訂單或訂閱，每個執行個體還會依循自己的歷程路徑操作。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/supplemental-identifier.md">詳細文件</a>。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>推出日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>模擬內容變化版本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>此功能之前以 [限量] 的名義發行，目前所有環境都可以使用。 在 [一般可用性] 發行版本中，此功能現在包含對多語言內容和內容實驗的支援，讓您能夠測試不同語言和處理方式的變化。 此外，目前有支援內容屬性（除了設定檔屬性外），以便允許進行更多動態和情境式內容測試。</p>
<img src="assets/do-not-localize/variants.gif">
<p>如需詳細資訊，請參閱<a href="../test-approve/simulate-sample-input.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 23 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>將讀取客群排程與批次分段工作同步處理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>完成批次分段後，就可以立即觸發日常歷程執行目前所有客戶都可以在每日排程的歷程中，使用此選項。 此選項可讓您定義的時間視窗長達 6 小時之久，等待批次分段作業的客群資料，確保使用到最新資料，執行歷程。或者如果還未準備好，就可以直接跳過。</p>
<p>之前以「限量」的名義發行，目前此功能所有環境都適用（一般可用性）。</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>如需詳細資訊，請參閱<a href="../building-journeys/read-audience.md#schedule">詳細文件</a>。</p>
<p>推出日期： 2025年5月20日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自訂簡訊提供者</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 目前可讓您在預設選項之外，設定以下其他 SMS 提供者：Sinch、Infobip 和 Twilio。 透過自訂 SMS 提供者設定，您就可以直接整合第三方提供者，運用動態訊息的進階來承載自訂，同時管理同意偏好設定（選擇加入/選擇退出），以便確保有遵守法規遵循規範。</p>
<p>如需詳細資訊，請參閱<a href="../sms/sms-configuration-custom.md">詳細文件</a>。</p>
<p>之前以「限量」的名義發行，目前此功能所有環境都適用（一般可用性）。</p>
<p>推出日期： 2025年5月20日</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件設計工具中的主題</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>目前您可以快速套用事先審核通過的主題，以便確保所有電子郵件的品牌都有保持一致性，加快投放行銷活動的流程，個別製作高品質的電子郵件，同時減少對設計團隊的依賴。</p>
<p>此功能目前為 Beta 版本，僅供 Beta 版客戶使用。若要加入 Beta 版計畫，請聯絡 Adobe 代表。</p>
<img src="assets/do-not-localize/themes.gif">
<p>如需詳細資訊，請參閱<a href="../email/apply-email-themes.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 14 日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>決策 — 全新 AI 公式產生器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以馬上從改善的新介面，定義並結合條件，以便建立特定決策排名公式。 您可以定義自訂排名公式，這類公式會透過引導式介面，結合 AI 模型分數、優惠方案優先順序、設定檔屬性、優惠方案屬性和內容訊號，不會只單純仰賴靜態優惠方案的優先順序。</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>如需詳細資訊，請參閱<a href="../experience-decisioning/exd-ranking-formulas.md">詳細文件</a>。</p>
<p>推出日期：2025 年 5 月 14 日</p>
</td>
</tr>
</tbody>
</table>

### 改良功能 {#25-05-improv}

以下列舉部分發布內容附上的改良功能。


* **沙箱復本的新行銷活動物件支援** — 推出日期： 2025年5月15日

  當使用套件匯出和匯入功能跨眾多沙箱複製活動時，也會立即複製以下相依性：頻道設定、實驗變體和設定、決策策略和項目。[閱讀全文](../configuration/copy-objects-to-sandbox.md)

* **登陸頁面的資料夾** — 推出日期：2025 年 5 月 9 日

  為了輕鬆管理登陸頁面，您可以立即使用資料夾，便可更有效地將資料夾整理成精簡的階層。[閱讀全文](../landing-pages/manage-lp.md)

* **直接郵件：SFTP 連線的 SSH 金鑰支援** — 推出日期：2025 年 5 月 5 日

  除了具有密碼驗證型別的現有 SFTP 之外，還可在直接郵件檔案路由設定中，立即將直接郵件檔案匯出至具有 SSH 金鑰驗證的 SFTP 伺服器。 [閱讀全文](../direct-mail/direct-mail-configuration.md)

* **啟用 [膠囊狀] 按鈕來執行個人化** — 推出日期：2025 年 5 月 5 日

  個人化編輯器已新增新的 [膠囊狀] 按鈕。啟用時，設定檔和內容屬性都會以 [膠囊狀] 按鈕形式顯示，增強驗證碼的可讀性。[閱讀全文](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >在接下來 30 天內，會將此功能逐步推廣到合適環境。

* Web channel **中的**&#39;重新導向至URL&#39;支援 — 推出日期： 2025年5月20日

  Journey Optimizer 網頁管道目前可讓您將訪客重新導向至其他現有網址，而不是重新導向視覺化編輯器中製作的新變化版本。 此功能可用來執行比較兩種截然不同頁面的實驗，而不只是用來更改頁面中的少數元素。 [閱讀全文](../web/create-web.md#web-redirect-to-url)

* **範本和片段的資料夾** — 可用日期： 2025年5月20日

  資料夾讓您可以更輕鬆有效地將內容範本、片段整理成結構化的階層。以前可供一組組織 (LA) 使用的資料夾，現在可供所有使用者 (GA) 管理其內容範本和片段。 請到[內容範本](../content-management/access-content-templates.md#folders)和[片段](../content-management/manage-fragments.md#folders)專區，閱讀更多內容。

* **電子郵件範本中的點選追蹤** — 推出日期： 2025年5月20日

  請在以下位置點擊追蹤：`<area>`位於電子郵件內容中影像地圖內的元素，目前有提供原生支援[!DNL Journey Optimizer]。 這是為了確保影像地圖區域收到與標準超連結相同的追蹤包裝、追蹤資料和附加參數。[深入了解訊息追蹤](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **行銷活動清單中的右側邊欄** — 推出日期： 2025年5月20日

  現在，在行銷活動清單中，選取行銷活動會開啟窗格並顯示其詳細資訊。

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.

* **Decision item attribute support for decisioning rules**
  
  You can now leverage decision item attributes to create decisioning rules.

* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

