---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 5ce97b443ece6107a54288d632f6e994f12dedf6
workflow-type: tm+mt
source-wordcount: 2468
ht-degree: 19%

---


# 搶鮮版發行說明 {#e-release-notes}

Adobe Journey Optimizer 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.




### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## 2026年7月發行前注意事項 {#july-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面和更新的文件會在變更上線生產時發佈。 雖然大多數變更會在發行日期提供，但有些可能會稍後推出。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年7月28日

### 忠誠度 {#july-26-loyalty}

Journey Optimizer推出了「忠誠度」，這是此版本的新功能。

<table>
<thead>
<tr>
<th><strong>忠誠度挑戰</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>忠誠度挑戰會將忠誠度方案轉換為吸引人的遊戲化體驗，激勵客戶採取有價值的行動，例如進行購買、撰寫評論、在社群媒體上參與或反向連結朋友。</p>
<p>管理員可以使用「忠誠度管理員」功能表，將Journey Optimizer與您的忠誠度生態系統連結，包括獎勵履行API、事件定義、產品詳細目錄、排除和身分設定。 行銷人員隨後可以設計標準、連續或循序挑戰，定義任務和獎勵，提供品牌內容卡和訊息，並使用內建的報告儀表板監控效能。 Journey Optimizer會產生歷程，在背景協調每個挑戰，讓團隊可以聚焦於客戶體驗和業務目標。</p>
<!-- GIF placeholder: to be added -->
<p>Jira： <a href="https://jira.corp.adobe.com/browse/DOCAC-14019">DOCAC-14019</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 入門 {#july-26-onboarding}

Journey Optimizer推出入門中心，此版本的新功能。

<table>
<thead>
<tr>
<th><strong>入門中心</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>從另一個行銷平台轉換成Adobe Journey Optimizer現在更快更簡單。 新的入門中心具有移轉工作區，可讓您自動匯入現有的電子郵件內容和歷程，讓您不必從頭開始重建。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<!-- GIF placeholder: to be added -->
<p>Jira： <a href="https://jira.corp.adobe.com/browse/DOCAC-15180">DOCAC-15180</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 歷程 {#july-26-journeys}

下列功能和改進功能已新增到此版本的歷程。

<table>
<thead>
<tr>
<th><strong>頻道最佳化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以設定歷程動作以包含多個傳出頻道（電子郵件、推播、簡訊），並讓Journey Optimizer透過最佳頻道自動傳送給每個客戶。 有三種最佳化模式可供使用：</p>
<ul>
<li>手動排名：指定您偏好的管道順序。</li>
<li>客戶偏好設定：從他們的設定檔使用客戶偏好的管道（體驗資料模型同意和偏好設定屬性）。</li>
<li>AI模型型排名：使用機器學習傾向分數來推斷每位客戶最有效的管道。</li>
</ul>
<p>當最上層頻道無法使用（未選擇加入、頻率限定或未設定）時，系統會退回至下一個可用頻道。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>Jira： <a href="https://jira.corp.adobe.com/browse/DOCAC-14900">DOCAC-14900</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **歷程模擬中的檔案支援外部對象（逗號分隔值和同盟對象構成）** — 歷程模擬現在支援外部對象。 模擬以逗號分隔值或同盟對象構成對象為目標的歷程時，您可以直接透過UI表單或JSON匯入從這些對象中模擬擴充屬性。 UI只會動態顯示歷程邏輯中使用的特定擴充屬性，以在決策分支和個人化規則上線之前進行精確驗證。 ([DOCAC-15074](https://jira.corp.adobe.com/browse/DOCAC-15074)) <!-- Documentation link: TBD -->

* **歷程標題中的開始和結束日期** — 當在即時歷程中設定開始和/或結束日期時，它們現在會出現在即時狀態徽章旁邊的歷程標題中。 顯示的標籤會根據每個日期是即將到來或是已過去而調整。 ([DOCAC-14702](https://jira.corp.adobe.com/browse/DOCAC-14702)) <!-- Documentation link: TBD -->

### 協調的行銷活動 {#july-26-oc}

下列功能和改進功能已新增到此版本的協調行銷活動。

<table>
<thead>
<tr>
<th><strong>針對協調的行銷活動提供無訊息工作時間支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將無訊息時間套用至協調行銷活動。 無訊息小時可讓您定義以時間為基礎的排除，以防止在特定期間傳送訊息，協助您在行銷活動協調使用案例中遵守客戶偏好設定和合規性要求。</p>
<p>Jira： <a href="https://jira.corp.adobe.com/browse/DOCAC-14054">DOCAC-14054</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>動作行銷活動傳入通道模擬模式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在上線前在「動作」行銷活動中模擬傳入頻道動作。 使用模擬模式透過模擬使用者測試您的設定並預覽呈現的體驗，包括產生的URL和QR碼，因此您可以端對端驗證規則、決策和內容呈現。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<!-- GIF placeholder: to be added -->
<p>Jira： <a href="https://jira.corp.adobe.com/browse/DOCAC-15166">DOCAC-15166</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **管理設定檔目標維度的功能** — 您現在可以刪除設定檔目標Dimension，或編輯並交換其設定的身分名稱空間，讓您對資料設定有更優異的控制權和彈性。 ([DOCAC-15018](https://jira.corp.adobe.com/browse/DOCAC-15018)) <!-- Documentation link: TBD -->

* **檢視協調的行銷活動轉換許可權** — 新增新的&#x200B;**檢視協調的行銷活動轉換**&#x200B;許可權，以取代舊版&#x200B;**在協調的行銷活動中檢視檔案**&#x200B;選項。 此變更可讓您隱藏促銷活動轉變中的預覽結果，以支援個人識別資訊的合規性。 ([DOCAC-14924](https://jira.corp.adobe.com/browse/DOCAC-14924)) <!-- Documentation link: TBD -->

* **支援Line** — 您現在可以直接新增LINE動作至您的協調行銷活動。 這項新活動可讓您建立及提供高度個人化的內容，包括文字、貼圖、影像、影片、位置資料和豐富的Flex訊息，以便在LINE平台上順暢地吸引您的客戶。 此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。 ([DOCAC-14905](https://jira.corp.adobe.com/browse/DOCAC-14905)) <!-- Documentation link: TBD -->

* **新協調行銷活動公開API** — 現已為協調行銷活動提供新API規格。 這些API可讓您以程式設計方式建立、管理和觸發協調的行銷活動，實現與外部系統和自動化管道的更深層整合。 ([DOCAC-14308](https://jira.corp.adobe.com/browse/DOCAC-14308)) <!-- Documentation link: TBD -->

* **個人化每個收件者和行銷活動的電子郵件寄件者詳細資料** — 協調的行銷活動現在支援使用設定檔屬性或關聯資料，個人化電子郵件標題欄位，包括寄件者名稱、寄件者地址和回覆對象。 如此一來，寄件者詳細資料就能反映每個收件者的相關顧問、位置或分支，而非透過單一公司地址路由所有傳送。 可在管道層級設定標頭值，並使用內容資料覆寫每個行銷活動，以獲得更精確的控制。 ([DOCAC-13761](https://jira.corp.adobe.com/browse/DOCAC-13761)) <!-- Documentation link: TBD -->

* **協調行銷活動中的目標維度簡化** — 作用中目標維度現在會顯示在工作流程畫布上，因此您可以檢視頻道活動使用的維度。 多實體區段流程較簡單，因為您不再需要個別的「變更維度」活動。 此外，您現在可以明確選擇訊息是在設定檔層級還是在次要維度層級傳送。 ([DOCAC-13554](https://jira.corp.adobe.com/browse/DOCAC-13554)) <!-- Documentation link: TBD -->

### 行銷活動 {#july-26-campaigns}

下列功能和改善專案已新增至此版本中的行銷活動。

<table>
<thead>
<tr>
<th><strong>API觸發的行銷活動中交易訊息的個人化PDF附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在API觸發的交易式行銷活動中，透過在API裝載中傳遞檔案位置，為每封電子郵件附加最多五個動態的個人化PDF。 如此一來，航空業等產業便能傳送登機證或旅行確認、金融服務業提供個人化發票或報表，零售業則能加入訂單收據或退貨標籤，每個檔案都能在傳送時針對收件者量身打造。</p>
<p>個人化和靜態PDF附件共用相同的配額；超過公平使用限制需要PDF附件附加元件。 歷程或動作行銷活動中不提供此功能。</p>
<p>Jira： <a href="https://jira.corp.adobe.com/browse/DOCAC-15186">DOCAC-15186</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **行銷活動的資料夾** — 您現在可以將行銷活動整理到資料夾中，以改善介面中的導覽和管理。 ([DOCAC-15098](https://jira.corp.adobe.com/browse/DOCAC-15098)) <!-- Documentation link: TBD -->

* **覆寫行銷活動中的預設執行欄位** - 先前可在歷程層級使用，您現在可以在全域覆寫行銷活動參數中電子郵件、簡訊和 WhatsApp 傳送的預設執行欄位集。 ([DOCAC-14718](https://jira.corp.adobe.com/browse/DOCAC-14718)) <!-- Documentation link: TBD -->

* **行銷活動儀表板中的品牌一致性分數** - 您現在可以直接在行銷活動儀表板中評估您的品牌一致性分數，以確保內容符合品牌形象。 這可讓您快速驗證指引，而無需開啟內容設計工具。 ([DOCAC-14516](https://jira.corp.adobe.com/browse/DOCAC-14516)) <!-- Documentation link: TBD -->

### 決策 {#july-26-decisioning}

下列改善專案已新增至此版本中的決策。

* **從自然語言運算式建立決策規則與排名公式** — 您現在可以簡單語言描述您要建立的決策規則或排名公式，並讓AI助理為您產生它。 此功能適用於具有Adobe AI功能存取權的客戶。 ([DOCAC-15231](https://jira.corp.adobe.com/browse/DOCAC-15231)) <!-- Documentation link: TBD -->

* **決策規則和排名公式模擬** — 您現在可以直接從規則或公式編輯器模擬決策規則和排名公式。 新增手動測試變體或使用AI產生變體，然後對您的測試資料執行運算式，以驗證資格並檢閱排名結果，所有這些都部署至生產環境之前。 具有存取Adobe AI功能之客戶可使用產生變體。 ([DOCAC-15227](https://jira.corp.adobe.com/browse/DOCAC-15227)) <!-- Documentation link: TBD -->

* **動態優惠屬性** — 決策專案自訂屬性現在可在傳送時使用設定檔、情境和對象資料進行個人化。 如此一來，行銷人員就不需要針對次要內容變化版本維持重複的產品建議，而能夠管理較少、較靈活的決策項目。 ([DOCAC-14899](https://jira.corp.adobe.com/browse/DOCAC-14899)) <!-- Documentation link: TBD -->

### 內容管理 {#july-26-content}

下列改善專案已新增至此版本的內容管理。

* **電子郵件範本**&#x200B;的`<head>`支援運算式片段 — 現在可以在電子郵件範本的`<head>`中使用運算式片段。 這可讓您集中處理單一片段中的樣式或任何自訂程式碼，並在多個範本中重複使用。 更新並重新發佈片段時，所有根據範本建立的電子郵件都會自動繼承最新的程式碼，無需手動個別更新每封電子郵件。 ([DOCAC-15257](https://jira.corp.adobe.com/browse/DOCAC-15257)) <!-- Documentation link: TBD -->

* **「AI小幫手」已重新命名為「產生內容」** — 「AI小幫手」已重新命名為「透過Adobe Journey Optimizer產生內容」。 此更新僅限於命名和術語；未引入任何功能變更。 內容產生、影像產生、個人化運算式和內容實驗的導覽標籤、按鈕、功能表和對話方塊已從「AI助理」重新命名為「產生內容」。 ([DOCAC-15230](https://jira.corp.adobe.com/browse/DOCAC-15230)) <!-- Documentation link: TBD -->

* **彈性的AI內容產生影像來源** — 在Journey Optimizer中產生內容現在會直接從Adobe Experience Manager Assets Essentials等來源取得品牌核准的影像。 三種模式可控制平衡：Assets （數位資產管理來源，預設）、平衡（數位資產管理優先，AI填補差距）和Creative （AI優先）。 這可確保每個視覺效果都準確、符合品牌規範，並為歷程和行銷活動做好生產準備。 ([DOCAC-14761](https://jira.corp.adobe.com/browse/DOCAC-14761)) <!-- Documentation link: TBD -->

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. ([DOCAC-13801](https://jira.corp.adobe.com/browse/DOCAC-13801)) [Documentation link: TBD]
-->

### 電子郵件管道 {#july-26-email}

下列功能已新增至此版本的電子郵件通道。

<table>
<thead>
<tr>
<th><strong>電子郵件設計工具中的模組</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件設計工具現在包含現成可用的版面模組 (例如頁首、產品卡、資訊區塊和頁尾) 資料庫，您可以將這些模組直接拖放到電子郵件畫布中。 每個模組都預先設定了可編輯的屬性 (影像、標題、文字、按鈕、連結)，並可透過 WYSIWYG 介面完全自訂，因此無需您從頭開始建立結構，即可加速電子郵件的建立。</p>
<!-- GIF placeholder: to be added -->
<p>Jira： <a href="https://jira.corp.adobe.com/browse/DOCAC-14877">DOCAC-14877</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 個人化 {#july-26-personalization}

下列改善專案已新增至此版本中的個人化。

* **管理完整/基本URL個人化的網域** — 您現在可以直接從Adobe Journey Optimizer中的管理設定建立和管理核准的完整和基本URL個人化的網域，而無需連絡Adobe支援。 ([DOCAC-15187](https://jira.corp.adobe.com/browse/DOCAC-15187)) <!-- Documentation link: TBD -->

* **個人化運算式中的新協助程式函式** — 個人化運算式現在提供新協助程式函式：

  * `appendQueryParams`：將查詢引數附加至URL，或如果索引鍵已存在則取代它。
  * `dateBetween`：檢查日期是否落在開始和結束日期範圍（含）。
  * `equalsAnyIgnoreCase`：當字串符合任何提供的值時傳回true，忽略大小寫。
  * `getUrlFragment`：擷取URL的片段部分（#之後的部分）。
  * `join`：使用分隔符號將陣列元素串連到單一字串中。
  * `decode64`：解碼Base64編碼的字串。 如果輸入不是有效的Base64，原始輸入字串會傳回不變。

  `concat`函式也已增強，現在支援兩個或多個引數。

  此外，下列範本移轉功能現已可協助您將現有範本移轉至Journey Optimizer：

  * `ampCompare`：使用指定的比較運運算元比較兩個值。
  * `ampSubstr`：傳回指定開始與結束索引之間的字串部分。
  * `compareTo`：以字典方式比較兩個字串。

  ([DOCAC-15099](https://jira.corp.adobe.com/browse/DOCAC-15099)) <!-- Documentation link: TBD -->

### 管道 {#july-26-channels}

下列功能和改進專案已新增到此版本中的管道。

<table>
<thead>
<tr>
<th><strong>自訂傳出頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在推出自訂管道，這項新功能可讓管理員透過無程式碼管道產生器，將任何外寄的HTTP傳訊管道（例如WeChat、Kakao Talk、Messenger或專屬提供者）直接帶入Journey Optimizer。 設定之後，便可在行銷活動、歷程和協調行銷活動中使用自訂管道，並提供與原生管道相同的完整功能集：使用運算式編輯器進行個人化、內容實驗、預覽和校訂、現成可用的報告，以及同意和治理實施。 這填補了先前由自訂動作填補的空白，這些動作僅限於歷程，缺乏專用頻道功能。</p>
<p>自訂傳出頻道目前以「有限可用性」的形式提供。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<!-- GIF placeholder: to be added -->
<p>Jira： <a href="https://jira.corp.adobe.com/browse/DOCAC-11381">DOCAC-11381</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **WhatsApp管道：支援WhatsApp流程範本** — 您現在可以在Adobe Journey Optimizer中傳送WhatsApp流程範本，以提供互動式的多熒幕體驗，例如調查和潛在客戶擷取。 回應會在提交時擷取，並儲存為新Journey Optimizer管道追蹤事件資料集中的原始JSON裝載。 ([DOCAC-15223](https://jira.corp.adobe.com/browse/DOCAC-15223)) <!-- Documentation link: TBD -->

* **輸送量的效能附加元件 — 推播** — 在API觸發的行銷活動中提供新的高輸送量異動訊息模式。 此模式專為大規模即時交易型傳訊而設計，最高可支援每秒 5,000 筆交易，而且可用性更高。 此功能先前僅適用於電子郵件頻道，現在也可用於推播頻道，適用於已購買Adobe高輸送量異動訊息附加元件產品的組織。 請聯絡您的 Adobe 代表以取得更多資訊。 ([DOCAC-14717](https://jira.corp.adobe.com/browse/DOCAC-14717)) <!-- Documentation link: TBD -->

### 管理 {#july-26-administration}

下列功能已新增至此版本的管理中。

<table>
<thead>
<tr>
<th><strong>Web應用程式防火牆IP白名單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在支援將登入頁面列入Web應用程式防火牆IP白名單，方便組織強制要求所有傳入要求都透過其設定的Web應用程式防火牆基礎架構專門路由。 透過這項增強功能，客戶可設定Journey Optimizer以拒絕任何略過Web應用程式防火牆層的直接請求，確保一致套用Imperva等工具中定義的安全性原則。</p>
<p>此功能可加強具有嚴格網路存取需求之企業的安全狀況，讓企業能夠完全控制其Journey Optimizer託管登陸頁面的流量。</p>
<p>Jira： <a href="https://jira.corp.adobe.com/browse/DOCAC-14814">DOCAC-14814</a></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>
