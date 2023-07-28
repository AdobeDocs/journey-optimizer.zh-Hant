---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
hide: true
hidefromtoc: true
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 97%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2023 年 7 月搶先發行說明 {#july-rn-2023}

**發行日期**：7 月 26 日至 27 日

### 新功能{#july-2023-features}

此發行版本提供下列新功能。

<table>
<thead>
<tr>
<th><strong>對象構成</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以建立構成工作流程，將現有 Adobe Experience Platform 對象與視覺畫布結合，並利用各種活動 (分割、擴充...) 來建立新對象。 新建立的對象會與現有對象一起儲存回 Adobe Experience Platform，並可在 Journey Optimizer 行銷活動中運用，來鎖定目標客戶。</p>
<p>如需詳細資訊，請參閱<a href="../audience/get-started-audience-orchestration.md">詳細文件</a>。</p>
<p>對象構成已與新的 Adobe Experience Platform「對象」選單完全整合，該選單可作為對象的集中式入口網站。 您現在可以使用瀏覽頁面，利用其中具有區段趨勢和重疊的新儀表板 ，來發掘新的深入分析，以及探索以資料夾與標記整理歸類的組織工具。 此體驗包含標準化對象標籤的治理控制項，以及管理啟用工作流程的對象生命週期管理功能。 有了這項新的管理體驗，您現在可以輕鬆安全地從單一位置管理對象。 如需詳細資訊，請參閱 <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hant" target="_blank">Adobe Experience Platform 文件</a>。</p></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
<img src="assets/do-not-localize/gif-dm.gif"/>
<p>For more information, refer to the <a href="../direct-mail/create-direct-mail.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>為電子郵件設計工具轉換 HTML 內容</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在 Journey Optimizer 的電子郵件編輯器中匯入和轉換任何 HTML 內容。 在電子郵件設計工具中，可自動識別和提供內容區塊：使用該工具的強大設計功能來更新和個人化！</p>
<img src="../email/assets/html-imported_2.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>在 Journey Optimizer 中使用標記</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了行銷活動和歷程之外，您現在還可以將 Adobe Experience Platform 整合標籤指派給登陸頁面、內容範本、片段及訂閱清單。 這可讓您輕鬆分類，以及改善所有清單的搜尋和導覽。 </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>如需詳細資訊，請參閱<a href="../start/search-filter-categorize.md#tags">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>內容範本 API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用專用的 API 來建立和管理 Adobe Journey Optimizer 內容範本，與現有的內容系統緊密整合。</p>
<!--<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


### 改進項目 {#july-2023-improvements}

此發行版本隨附下列改進項目。

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
* 已引進新類型的系統警報。 您現在可以在自訂動作失敗時收到通知。—>

**行銷活動**

* 與行銷活動相關的內容事件現在可用於個人化編輯器的「內容屬性」選單。


**對象**

已增強歷程或行銷活動中的對象選取器功能，新增數欄顯示對象的來源與更新頻率。

隨著對象構成入口網站的發行，Adobe Experience Platform 與 Adobe Journey Optimizer 已更新系統和文件內的「對象」與「區段」的使用方式。

* 對象：一組具有共同特徵和行為的人員、帳戶、家庭或其他實體。
* 區段定義：在 Adobe Experience Platform 中，用來描述目標對象之關鍵特性或行為的規則。 此辭彙先前稱為「區段」。

因此，在 Adobe Journey Optimizer 和 Adobe Experience Platform UI 中，您會看到「區段」被「對象」取代，以反映建立和管理對象的新路徑。

**API**

Adobe Journey Optimizer API 驗證 - 已棄用以 JWT 方法來產生存取權杖。 務必使用 OAuth 伺服器對伺服器驗證方法來建立所有新的整合。 Adobe 也建議您將現有的整合移轉至 OAuth 方法。 [了解更多](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)


**其他變更**

現在，所有客戶都可透過公開測試版使用Journey Optimizer資料集匯出至雲端儲存目標。 此功能可讓您與雲端儲存空間位置建立即時連線，以匯出資料集的內容。 [了解更多](../data/export-datasets.md)




