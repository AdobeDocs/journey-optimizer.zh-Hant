---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer早期發行說明
hide: true
hidefromtoc: true
source-git-commit: e384991599c19f72910f299350c0839fa16b4588
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 27%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每個月的最後一週合併 [發行說明](release-notes.md).

以下早期發行說明在發行日期之前可能會有所變更，恕不另行通知。 連結、畫面和更新後的檔案會發佈在 [發行說明](release-notes.md)，於發行日期。

## 2023年7月早期發行說明 {#july-rn-2023}

**發行日期**： 7月26日至27日

### 新功能{#july-2023-features}

此版本提供下列新功能。

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
<img src="../audience/assets/audiences-publish.png"/>
<p>如需詳細資訊，請參閱<a href="../audience/get-started-audience-orchestration.md">詳細文件</a>。</p>
<p>對象構成已與新的Adobe Experience Platform「對象」功能表完全整合，該功能表可作為對象的一個集中入口網站。 您現在可以使用包含新儀表板（具有區段趨勢和重疊）的瀏覽頁面，來尋找新的深入分析，並探索用於摺疊和標籤的組織工具。 此體驗包含標準化對象標籤的治理控制項，以及管理啟用工作流程的對象生命週期管理功能。 有了這項全新的管理體驗，您現在可以輕鬆安全地從單一位置管理對象。 如需詳細資訊，請參閱 <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hant" target="_blank">Adobe Experience Platform檔案</a>.</p></p>
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
<img src="../direct-mail/assets/direct-mail-properties.png">
<p>For more information, refer to the <a href="../direct-mail/create-direct-mail.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>轉換電子郵件設計工具的HTML內容</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在Journey Optimizer的電子郵件編輯器中匯入和轉換任何HTML內容。 內容區塊會自動識別，並可在電子郵件設計工具中使用：使用其強大的設計功能來更新和個人化！</p>
<img src="../email/assets/html-imported_2.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>使用Journey Optimizer中的標籤</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了行銷活動和歷程之外，您現在還可以指派Adobe Experience Platform統一標籤至您的登入頁面、內容範本、片段和訂閱清單。 這可讓您輕鬆分類，並改善所有清單中的搜尋和導覽。 </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>如需詳細資訊，請參閱<a href="../start/search-filter-categorize.md#tags">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>內容範本API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以使用專用的API來建立和管理Adobe Journey Optimizer內容範本，提供與現有內容系統的緊密整合。</p>
<!--<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


### 改進項目 {#july-2023-improvements}

此版本隨附下列改善專案。

**歷程**

<!--* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
* 已引入新型別的系統警示。 您現在可以在自訂動作失敗時收到通知。


**行銷活動**

* 與行銷活動相關的內容事件現在可用於個人化編輯器「內容屬性」選單。


**對象**

已針對歷程或行銷活動中的對象選擇器進行增強功能，新增欄顯示對象的原始和更新頻率。

隨著對象構成入口網站的發行，Adobe Experience Platform和Adobe Journey Optimizer已更新系統和檔案內「對象」和「區段」的使用方式。

* 對象：一組具有共同特徵和行為的人員、帳戶、家庭或其他實體。
* 區段定義：在 Adobe Experience Platform 中，用來描述目標對象之關鍵特性或行為的規則。 此辭彙先前稱為「區段」。

因此，在 Adobe Journey Optimizer 和 Adobe Experience Platform UI 中，您會看到「區段」被「對象」取代，以反映建立和管理對象的新路徑。

**API**

Adobe Journey Optimizer API驗證 — 不建議使用產生存取權杖的JWT方法。 所有新的整合都必須使用OAuth伺服器對伺服器驗證方法來建立。 Adobe也建議您將現有的整合移轉至OAuth方法。 [了解更多](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)


**其他變更**

現在，所有客戶都可將Journey Optimizer資料集匯出至雲端儲存空間目標，作為公開測試版使用。 此功能可讓您建立與雲端儲存位置的即時連線，以匯出資料集的內容。 [了解更多](../data/export-datasets.md)




