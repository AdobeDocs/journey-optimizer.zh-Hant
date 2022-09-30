---
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9593ea40853221e0eec45f30f7635d8a116b03c1
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 18%

---

# 發行說明 {#release-notes}

本頁面列出[!DNL Journey Optimizer]所有新功能和改進項目。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變動，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target=&quot;_blank&quot;}。

![電子報](../assets/do-not-localize/nl-icon.png) 立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} ，直接把每季最新產品更新、激勵人心的故事、使用案例、提示等內容傳送到您的收件匣。

## 2022 年 9 月發行版本{#sept-2022-release}

### 新功能{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>動態內容與新條件式規則產生器</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以建立動態內容，以根據條件規則調整訊息的內容。</p> 
<p>條件式規則是使用運算式編輯器中的視覺化規則產生器來建立，您可以在其中儲存，以便在歷程和行銷活動中重複使用。</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>如需詳細資訊，請參閱<a href="../personalization/get-started-dynamic-content.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API觸發的行銷活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>除了現有的已排程促銷活動，您現在可以在Journey Optimizer中建立API觸發的促銷活動，並使用API從外部系統叫用它們。</p>
<p>這可讓您涵蓋各種操作和交易式訊息需求，例如密碼重設、OTP Token等。</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>如需詳細資訊，請參閱<a href="../campaigns/api-triggered-campaigns.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>資料存取控制</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>通過基於屬性的訪問控制，管理員可以根據特定屬性控制對特定對象的訪問。 這些屬性可以是新增至物件的中繼資料，例如標籤。 從此版本開始，管理員還可以定義只能訪問特定欄位和/或對象以及與這些欄位和/或對象對應的資料的用戶角色。</p>
<p> 基於屬性的訪問控制目前僅限於選定的客戶使用，並將在將來的版本中部署到所有環境。</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>如需詳細資訊，請參閱<a href="../administration/object-based-access.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>資料控管與隱私權</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過其資料使用標籤與實作(DULE)控管架構，Journey Optimizer現在可以運用Adobe Experience Platform控管政策，防止敏感欄位透過自訂動作匯出至協力廠商系統。 如果系統在自訂動作參數中識別限制欄位，系統會顯示錯誤，使您無法發佈歷程。</p>
<p>資料使用標籤和實作(DULE)的使用目前僅限選定客戶使用，並將在未來版本中部署至所有環境。</p>
<p>如需詳細資訊，請參閱<a href="../action/action-privacy.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自動同意強制（同意政策）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform可讓您輕鬆採用及強制執行行銷政策，以尊重客戶的同意偏好設定。 同意原則在Adobe Experience Platform中定義。 在Journey Optimizer中，您可以將這些同意政策套用至自訂動作。 例如，您可以定義同意原則，以排除尚未同意接收電子郵件、推播或簡訊通訊的客戶。
<p>自動同意強制目前僅適用於已購買Healthcare Shield附加元件產品的組織。</p>
<p>如需詳細資訊，請參閱<a href="../action/consent.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>權限管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer支援定義使用者角色和存取原則，以管理功能和物件的權限。 通過 <strong>Adobe Experience Cloud權限</strong>，您可以建立和管理角色，並為這些角色指派所需的資源權限。 權限也可讓您管理與特定角色相關聯的標籤、沙箱和使用者。</p>
<p> 權限的使用目前僅限於選取的客戶，且將在未來版本中部署至所有環境。</p>
<p>如需詳細資訊，請參閱<a href="../administration/attribute-based-access.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>警報和監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>身為Journey Optimizer使用者，您現在可以透過使用者介面存取系統警報，以在歷程未如預期運作時收到通知。 您可以檢視可用警報並訂閱警報。 如果「讀取區段」活動在定義的時間範圍內未處理任何設定檔，則此版本提供的第一個警報將會警告您。 此工作流程已解除鎖定，將提供更多資訊。</p>
<p>如需詳細資訊，請參閱<a href="../reports/alerts.md">詳細文件</a>。
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### 改進項目{#sept-2022-improvements}

**歷程**

* 此 **實體資料集** 現在可作為Adobe Journey Optimizer中的現成可用資料集。 此查詢資料集包含中繼資料，讓追蹤和意見資料集資訊更為豐富。 這可協助您使用更易理解的資料，改善報表和查詢。 [了解更多](../start/datasets-query-examples.md#entity-dataset)
* 已將新護欄新增至單一歷程（從事件或區段資格開始），以防止同一事件多次錯誤觸發歷程。 設定檔重新進入現在會依預設暫時封鎖5分鐘。 [進一步了解](../start/guardrails.md#events-g)

**管理**

* 現在啟用或停用允許的清單時，會顯示新警告以詳細說明每個動作的影響。 [了解更多](../configuration/allow-list.md#enable-allow-list)
* 更新了用於建立通道表面、建立IP池、管理隱藏清單和允許清單以及配置SMS通道的用戶介面。
* 現在，為指定子網域建立第一個通道曲面時，處理時間將需要10分鐘到10天，使用該子網域的後續曲面最多只需3小時。 [了解更多](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* 更新建立登錄頁面預設集和登錄頁面子網域的使用者介面。 [了解更多](../configuration/lp-subdomains.md)

**稽核控制**

* 透過Journey Optimizer，您可以識別系統中的使用者對各種服務和功能（例如促銷活動、歷程、訊息、登錄頁面等）所執行的動作。 稽核記錄資源現在包含對各種其他動作的變更，並會在活動發生時自動記錄。 在[本頁](../privacy/audit-logs.md)中深入瞭解。

**封存支援**

* 新 **實體資料集** 包含「範本」欄位，可讓您匯出所有通道上已傳送訊息的格式和結構，以用於封存。 [了解更多](../configuration/archiving-support.md)

**登陸頁面**

* 您現在可以使用來自相同登陸頁面內其他頁面的內容資料。 例如，如果您將核取方塊連結至主要登陸頁面上的訂閱清單，則可以在「感謝您」子頁面上使用該訂閱清單。 [了解更多](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### 其他變更{#sept-2022-other}

* 「促銷活動快速傳送」模式已取代「歷程突發模式」。 [了解更多](../campaigns/create-campaign.md#rapid-delivery)
* 為了改善效能，從「讀取」區段、「區段」資格或業務事件活動開始的歷程中，無法再使用體驗事件欄位群組。 此變更僅適用於新歷程。 現有行為會保留目前的行為。 [了解更多](../start/guardrails.md#expression-editor)
* 已移除已排程讀取區段歷程的1小時限制。 這些歷程現在可立即執行。

