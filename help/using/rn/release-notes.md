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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 1ddc46d8ea79660610ff6ba9600ed78d57c86ab5
workflow-type: tm+mt
source-wordcount: 1446
ht-degree: 28%

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

## 2026年7月發行說明 {#july-26-updates}

### 忠誠度挑戰 {#july-26-loyalty}

Journey Optimizer推出「忠誠度挑戰」，此版本的新功能。

<table>
<thead>
<tr>
<th><strong>忠誠度挑戰</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>忠誠度挑戰會將忠誠度方案轉換為吸引人的遊戲化體驗，激勵客戶採取有價值的行動，例如進行購買、撰寫評論或任何想要的行為。</p>
<p>管理員可以使用「忠誠度管理員」功能表，將Journey Optimizer與您的忠誠度生態系統連結，包括獎勵履行API、事件定義、產品詳細目錄、排除和身分設定。 行銷人員隨後可以設計標準、連續或循序挑戰，定義任務和獎勵，提供品牌內容卡和訊息，以及使用AI支援的報告儀表板來監控效能。 Journey Optimizer會產生歷程，在背景協調每個挑戰，讓團隊可以聚焦於客戶體驗和業務目標。</p>
<p>忠誠度也會引進同事技能，讓團隊更有效率地執行關鍵挑戰操作，包括建立挑戰、設定挑戰屬性、管理對象和相關設定，以及檢閱見解以監控挑戰參與度和獎勵績效。</p>
<p>此功能僅適用於獲得Journey Optimizer忠誠度授權的組織。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p>如需詳細資訊，請參閱<a href="../loyalty-challenges/get-started.md">詳細說明文件</a>。</p>
<p> 推出日期： 2026年7月28日</p>
</td>
</tr>
</tbody>
</table>

### 傳出頻道 {#july-26-outbound-channels}

此發行版本已引入下列功能。

<table>
<thead>
<tr>
<th><strong>頻道最佳化</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以設定歷程或行銷活動動作，以包含多個傳出頻道（電子郵件、推播、簡訊），並讓Journey Optimizer透過最佳頻道自動傳送給每個客戶。 有三種最佳化模式可供使用：</p>
<ul>
<li>手動排名：指定您偏好的管道順序。</li>
<li>客戶偏好設定：從他們的設定檔使用客戶偏好的管道（體驗資料模型同意和偏好設定屬性）。</li>
<li>AI模型型排名：使用機器學習傾向分數來推斷每位客戶最有效的管道。</li>
</ul>
<p>當最上層頻道無法使用（未選擇加入、頻率限定或未設定）時，系統會退回至下一個可用頻道。</p>
<p>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<p><img src="assets/do-not-localize/channel-optimization.gif"></p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/channel-optimization.md">詳細說明文件</a>。</p>
<p>推出日期： 2026年7月22日</p>
</td>
</tr>
</tbody>
</table>

### 歷程 {#july-26-journeys}

下列功能和改進功能已新增到此版本的歷程。
<table>
<thead>
<tr>
<th><strong>新使用者介面</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>已針對歷程畫布引入<b>新使用者介面</b>，為大型歷程提供更優異的效能、可更好閱讀的自動版面配置，以及引導式撰寫體驗。</p>
<p><img src="../building-journeys/assets/journey-new-canvas.png"></p>
<p>若要切換到新的UI，請按一下<b>新增體驗</b>按鈕。 此設定會儲存在歷程層級，因此預設會在新體驗中重新開啟歷程。 若要還原，請按一下<b>舊體驗</b>。 <a href="../building-journeys/using-the-journey-designer.md#canvas-capabilities">了解更多</a>。</p>
<p><img src="../building-journeys/assets/journey-new-experience-switch.png"></p>
<p> 推出日期： 2026年7月16日</p>
</td>
</tr>
</tbody>
</table>

* [!BADGE 淘汰]{type=Negative}對象資格節點中不再支援批次對象 — 自2026年8月3日起，Journey Optimizer會封鎖在「對象資格」節點中使用批次對象之任何歷程的發佈。 此強制措施取代了6月版本中推出的畫布警告。 現有的即時歷程不受影響。 在「對象資格」節點中使用串流對象，或切換至「讀取對象」活動。 [瞭解如何移轉您的歷程](../building-journeys/aq-batch-audiences-migration.md)

### 電子郵件設計工具 {#july-26-email}

下列功能已新增至此版本的電子郵件通道。

<table>
<thead>
<tr>
<th><strong>電子郵件Designer中的內容檢查（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 現在包含直接在電子郵件設計工具中的自動化技術驗證，可幫助您在傳送前捕捉 HTML 和 CSS 問題。</p>
<p>檢查涵蓋不支援的元素，例如 <code>&lt;script&gt;</code> 和 <code>&lt;base&gt;</code> 標籤、可能中斷 Microsoft Outlook 版面的空白 div、HTML 中繼重新整理標籤，以及觸發 Gmail 轉譯失敗的 CSS 或 HTML 大小臨界值。</p>
<p>結果會直接在製作面板中顯示為錯誤、警告或資訊性通知，其中包含內容詳細資訊和適用的一鍵式修正，因此無需離開編輯器即可解決問題。</p>
<p>此功能之前以「有限可用性」的名義提供，現在可供所有客戶使用。</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>如需詳細資訊，請參閱<a href="../email/content-check.md">詳細文件</a>。</p>
<p>推出日期： 2026年7月16日</p>
</td>
</tr>
</tbody>
</table>

### 協調的行銷活動 {#july-26-oc}

下列功能和改進功能將新增到此版本的協調行銷活動。

<table>
<thead>
<tr>
<th><strong>協調行銷活動中的檔案型目標定位</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>協調的行銷活動現在支援直接將<strong>CSV或TXT檔案</strong>載入行銷活動畫布，作為目標對象，而不先將檔案擷取到Adobe Experience Platform。 檔案資料會在執行時使用，不會儲存為Adobe Experience Platform資料集。 在檔案設定期間，您可以定義欄對應、資料型別、NULL處理和每欄錯誤原則。 未通過驗證的列會在行銷活動執行前遭到拒絕並記錄，讓對象保持乾淨，無需手動預先處理。 這尤其適合在無法建立完整擷取管道的臨時傳送或合作夥伴清單行銷活動。</p>
<p>如需詳細資訊，請參閱<a href="../orchestrated/activities/load-file.md">詳細文件</a>。</p>
<p> 推出日期：2026年7月6日</p>
</td>
</tr>
</tbody>
</table>

### 內容管理 {#july-26-content}

下列功能和改善專案已新增至此版本的內容管理。

* **片段詳細目錄中的快速啟動捷徑** — 您現在可以使用&#x200B;**[!UICONTROL 更多動作]**&#x200B;按鈕，從片段清單中快速存取常見動作。 可用的捷徑包括編輯片段、開啟其詳細資訊以及捨棄草稿版本。 [了解更多](../content-management/manage-fragments.md#quick-launch-fragments)

  ![](../content-management/assets/fragment-quick-launch.png)

* **範本詳細目錄中的快速啟動捷徑** — 「內容範本」清單中的&#x200B;**[!UICONTROL 更多動作]**&#x200B;按鈕現在提供對常見動作的快速存取：編輯範本詳細資料、模擬內容以及刪除範本。 對於電子郵件範本，其他捷徑可讓您編輯主旨行和電子郵件內文、檢視或傳送校樣、執行垃圾郵件報告，以及呈現電子郵件。 [了解更多](../content-management/access-content-templates.md#quick-launch-templates)

  ![](../content-management/assets/content-template-quick-launch.png)

### 內容與整合 {#july-26-integration}

下列功能和改進功能將新增到此版本的內容管理與整合。

* **決定專案的動態自訂屬性** — 決定專案自訂屬性現在可以在傳遞時使用設定檔、情境和對象資料進行個人化。 如此一來，行銷人員就不需要針對次要內容變化版本維持重複的產品建議，而能夠管理較少、較靈活的決策項目。 [閱讀更多](../experience-decisioning/items.md#attributes)

  推出日期： 2026年7月27日

* **AJO MCP伺服器新工具** - [!DNL Adobe Journey Optimizer] MCP伺服器現在會公開五個額外的唯讀&#x200B;**通道設定工具**，讓您能夠直接從AI助理查詢通道設定、支援資源和行銷動作。 您現在可以使用&#x200B;**列出頻道設定** （橫跨所有AJO頻道）、**取得頻道設定**、**列出設定資源**、**取得設定資源**&#x200B;以及&#x200B;**列出行銷動作**。 [閱讀更多](../integrations/ajo-mcp.md#mcp-tools)

  推出日期： 2026年7月9日

* **個人化運算式中的新協助程式函式** — 個人化運算式現在提供新協助程式函式：

  * `appendQueryParams`：將查詢引數附加至URL，或如果索引鍵已存在則取代它。
  * `dateBetween`：檢查日期是否落在開始和結束日期範圍（含）。
  * `equalsAnyIgnoreCase`：當字串符合任何提供的值時傳回true，忽略大小寫。
  * `getUrlFragment`：擷取URL的片段部分（#之後的部分）。
  * `join`：使用分隔符號將陣列元素串連到單一字串中。
  * `decode64`：解碼Base64編碼的字串。 如果輸入不是有效的Base64，原始輸入字串會傳回不變。
  * `parseJson`：將JSON字串剖析為可在範本中使用的結構化變數。
  * `valueAtPath`：從資料路徑指派值給範本變數，並附上選擇性索引，以從陣列或集合中擷取特定元素。
  * `abort`：在轉譯期間到達時停止訊息傳遞。

  `concat`函式也已增強，現在支援兩個或多個引數。

  此外，下列範本移轉功能現已可協助您將現有範本移轉至Journey Optimizer：

  * `ampCompare`：使用指定的比較運運算元比較兩個值。
  * `ampSubstr`：傳回指定開始與結束索引之間的字串部分。
  * `compareTo`：以字典方式比較兩個字串。

  [進一步瞭解協助程式功能](../personalization/functions/functions.md)

  推出日期： 2026年7月28日

### 管理 {#july-26-administration}

此版本中的管理和資料管理已新增下列改善專案。

* **資料集存留時間(TTL)護欄 — 現有的沙箱** - Journey Optimizer系統產生的資料集的存留時間(TTL)護欄（設定檔存放區為90天，資料湖為13個月）將從&#x200B;**2026年10月1日起，在**&#x200B;現有的客戶沙箱和組織&#x200B;**上強制執行**。 [了解更多](../data/datasets-ttl.md#ttl-guardrail)


