---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
    internal-label: Administration
subfeature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
    internal-label: Journey Optimizer release notes
source-git-commit: 0905e570576a4587cd7734aa036d8f09276e0127
workflow-type: tm+mt
source-wordcount: '2943'
ht-degree: 8%
---

# 搶鮮版發行說明 {#e-release-notes}

Adobe Journey Optimizer 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

## 2026年9月發行前注意事項 {#sep-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面和更新的文件會在變更於生產環境上線後發佈。 雖然大多數變更會在發行日期提供，但有些可能會稍後推出。如需詳細資訊，請參閱每個項目所列的推出日期。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年9月22至23日

>[!BEGINSHADEBOX]

**本月CX Enterprise Coworker的新增功能**

此版本提供數項全新及改善的[同事](../start/ai-features.md#cx-coworker)功能和技能，列於此處，以供您瞭解。 每項資料亦會在下文相關章節中詳細說明。

* [CE Channel內容外掛程式](#sep-26-content-management) — 此新外掛程式可在同事中結合行銷活動副本、影像和電子郵件HTML技能，從行銷活動簡報到生產就緒副本和HTML。
* [忠誠度推薦技能](#sep-26-loyalty) — 直接在同事的對話介面中要求挑戰機會，並將它們變成即時挑戰，而不需要離開聊天。
* [歷程模擬](#sep-26-journeys) — 自動進行端對端歷程驗證，並直接在同事中解譯結果。
* [從同事邊欄建立歷程](#sep-26-journeys) — 使用AI直接從同事右側邊欄產生歷程，取代先前的AI助理體驗。
* [比較歷程版本](#sep-26-journeys) — 透過同事聊天，取得任意兩個歷程版本之間的完整保真、結構化差異。
* [衛生分析技能](#sep-26-journeys) — 掃描使用中的和草稿歷程，以找出中斷的設定、無訊息失敗，以及過時或未使用的資產，並提供建議的修正。
* [業務績效分析技能](#sep-26-journeys) — 直接從聊天室分析歷程績效並取得具體的最佳化建議。

>[!ENDSHADEBOX]

### 內容管理 {#sep-26-content-management}

以下功能即將推出此版本的內容管理。

<table>
<thead>
<tr>
<th><strong>Co-worker中的管道內容外掛程式</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Co-worker現在提供新的<strong>管道內容</strong>外掛程式，將行銷活動復本、影像和組合電子郵件HTML技能整合到策略到部署的單一外掛程式中。 **Channel Content**外掛程式提供下列技能：</p>
<ul>
<li><strong>協調內容製作</strong>。</li>
<li><strong>探索內容策略</strong></li>
<li><strong>內容簡介</strong></li>
<li><strong>產生內容</strong></li>
<li><strong>檢查內容整備</strong></li>
<li><strong>修訂與重新產生內容</strong></li>
<li><strong>產生影像</strong></li>
<li><strong>評估內容設計</strong></li>
<li><strong>儲存頻道內容</strong></li>
<li><strong>從Figma建立電子郵件</strong></li>
<li><strong>品牌查詢</strong> </li>
</ul>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 整合 {#sep-26-integrations}

此版本即將整合下列功能。

* **Experience Manager片段的動態權杖替代** - Experience Manager內容片段參考現在支援&#x200B;**tokenSubstitution**&#x200B;屬性。 設定為`false`時，片段欄位內的個人化會直接解析，參考中不含Token對應。 其預設值為`true`，這會保留現有行為。

  此功能僅適用於部分組織 (限額推出)。 若想取得存取權，請聯絡您的 Adobe 代表。

* **決策中的AEM Managed Services內容片段支援** — 現在管理決策專案時，決策中可支援AEM Managed Services內容片段。

### 忠誠度 {#sep-26-loyalty}

此版本中的「忠誠度」提供下列功能和改善功能。

<table>
<thead>
<tr>
<th><strong>挑戰機會</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>忠誠度績效選單現在包含<strong>機會標籤</strong>，其中會顯示AI偵測到的趨勢和差距，例如層級進展摩擦或挑戰任務流失，每個都具有預計的影響，以及按一下「使用AI建立」動作以產生可解決它的挑戰。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **同事忠誠度建議技能** — 行銷人員現在可以在同事的對話介面中直接要求&#x200B;**挑戰機會**，根據真正的忠誠度計畫趨勢獲得實際的挑戰想法，並在不離開聊天的情況下將其轉換為即時挑戰。

* **內容卡個人化編輯器中的挑戰網域** — 內容卡個人化編輯器現在支援&#x200B;**挑戰**&#x200B;作為網域，讓您在編寫內容卡個人化時存取挑戰中繼資料。 如此一來，您就更輕鬆地針對挑戰的每一個階段（啟動、進行中及結束）建立量身打造的內容，而不需要自訂程式碼。



### 入門 {#sep-26-onboarding}

以下功能即將在此版本中上線。

<table>
<thead>
<tr>
<th><strong>入門電子郵件和歷程的引導功能（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過引導式功能，您可以更輕鬆地從其他行銷平台轉換至 Adobe Journey Optimizer，將現有電子郵件內容和歷程移至 Journey Optimizer。 <strong>專屬工作區</strong>可讓您重複使用現有工作，而非從頭重建。</p>
<p>此功能之前以「有限可用性」的名義發行，目前所有環境都適用 (一般可用性)。</p>
</td>
</tr>
</tbody>
</table>



### 歷程 {#sep-26-journeys}

下列功能和改進功能將新增到此版本的歷程。

<table>
<thead>
<tr>
<th><strong>從同事邊欄建立歷程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>使用AI建立歷程</strong>現在可直接從同事右側邊欄取得，將先前的AI助理體驗取代為品牌重塑的整合式進入點以產生歷程。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程警示的AI推薦卡</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer首頁現在會在歷程警報觸發時顯示<strong>AI建議卡</strong>，其中涵蓋<strong>歷程自訂動作失敗</strong>和<strong>偵測到歷程異常</strong>警報。 選取卡片會開啟歷程，其中右邊欄已預先填入已執行的分析。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>傳入活動停用歷程活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>歷程畫布中的新<strong>傳入活動停用</strong>活動可讓您直接從歷程中移除最多五個傳入活動或體驗的設定檔，將傳入取消資格從歷程退出中解耦，以進行更進階的跨頻道協調。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程畫布中的內容預覽</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>今天檢閱管道內容需要一次一個地個別開啟每個節點 — 在具有許多管道節點的歷程中緩慢且容易出錯，特別是當個人化表示檢查每個節點的多個處理或變體時。 <strong>內容預覽</strong>透過直接在畫布中為每個管道節點呈現內容縮圖，以全熒幕模式檢查並在處理與變體之間切換，來移除該摩擦。</p>
</td>
</tr>
</tbody>
</table>

* **歷程模擬中的補充ID支援** - **歷程模擬現在支援Supplemental ID**，可讓您針對讀取對象和事件觸發的歷程測試複雜的使用者案例。

* **對象資格歷程的跳轉支援** — 以&#x200B;**對象資格**&#x200B;開始的歷程現在可以使用&#x200B;**跳轉**&#x200B;活動來進入事件型開始歷程；跳到對象資格型歷程仍不受支援。

* **與同事比較歷程版本** — 今天，檢閱兩個歷程版本之間的變更內容時，需要在Journey Optimizer節點內依節點手動比較 — 沒有結構化的差異，這會導致變更檢閱、稽核和發佈前檢查緩慢且容易出錯，尤其是當歷程越來越複雜時。 此功能可讓客戶或AI代理程式透過Co-worker Chat比較歷程的任意兩個版本，在不開啟Journey Optimizer的情況下，取回完整保真的&#x200B;**結構化diff** — 新增/移除/修改/移動具有欄位層級詳細資訊、變更連線、歷程層級屬性變更和統計計數的節點。

* **減少等待和事件活動的步驟事件** — 不再為&#x200B;**等待**&#x200B;活動和&#x200B;**事件**&#x200B;活動產生步驟事件，因為設定檔實際上未在該活動中處理。<!-- DRAFT: pending DOCAC sub-task under DOCAC-15691, see CJM-165835 -->
<!-- Documentation link: TBD -->

* **自訂報告的練習步驟事件隱藏** — 作為步驟事件最佳化的一部分，Journey Optimizer現在會在歷程練習期間停止產生某些無法報告的步驟事件。 這只會影響建置在這些模擬執行步驟事件型別上的自訂報表。 如果您受到影響，請重新觸發試執行以重新產生資料。

* **衛生分析同事技能** — 同事中的新衛生分析技能會掃描您的使用中歷程和草稿歷程，找出中斷的設定、無訊息的失敗，以及過時或未使用的資產，例如過時的草稿歷程、孤立的資料來源和持續的自訂動作錯誤，並直接在聊天中顯示建議的修正。<!-- Documentation link: TBD -->

* **業務績效分析同事技能** — 同事中的新&#x200B;**業務績效分析**&#x200B;技能可分析您的歷程執行情形、說明績效較低的領域，並建議具體的最佳化，例如重新參與等待、管道升級和傳送時間最佳化。 <!-- Documentation link: TBD -->

* **歷程屬性中的自動事件復原逾時** — 歷程屬性現在包含&#x200B;**設定事件復原逾時**&#x200B;設定：依預設，受影響的歷程事件會在服務中斷後自動重播長達72小時，而不需要任何動作。 您可以開啟此設定來控制對時間敏感的歷程的重播視窗（0-72小時）。 現有的&#x200B;**逾時或錯誤**&#x200B;欄位也已重新命名為&#x200B;**自訂動作/IDS動作逾時**，以避免這兩個設定混淆。

### 管道 {#sep-26-channels}

此版本中的管道即將推出下列功能和改善。

<table>
<thead>
<tr>
<th><strong>Android Live Updates的已上線活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在將<strong>即時活動支援擴充至Android</strong>，以擴充其即時行動個人化功能。 您可以直接將即時進度更新傳送給使用者，例如訂單追蹤、航班狀態、即時活動更新和即時運動分數。</p>
<p>除了支援iOS Live活動以外，Journey Optimizer現在還管理其平台設定中Android Live更新的暫時推送代號。 它使用API觸發的行銷活動和Headless API來支援廣播和交易式更新流程。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>自訂傳出頻道（一般可用性）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>自訂傳出頻道</strong>可讓管理員透過無程式碼的Channel Builder，將任何傳出以HTTP為基礎的訊息頻道（例如WeChat、Kakao Talk、Messenger或專屬提供者）直接帶入Journey Optimizer。 設定之後，便可在各種行銷活動、歷程和精心安排的行銷活動中使用自訂管道，並提供與原生管道相同的完整功能集：使用運算式編輯器進行個人化、內容實驗、預覽和校樣、現成可用的報告，以及同意與治理強制執行。</p>
<p>在此版本中，自訂傳出頻道也獲得幾個新功能：</p>
<ul>
<li>透過Journey Optimizer編輯器在自訂管道裝載中使用Personalization Decisioning，與程式碼型體驗中的方式相同。</li>
<li>套用商業規則至自訂管道，就像您在原生管道上所做的那樣。</li>
<li>在管道清單中選取API觸發行銷活動的自訂管道，這在之前是不可能的。</li>
<li>為自訂管道定義報表webhook並將其附加至管道設定，以便您可以透過互動事件豐富Journey Optimizer報表。</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Android推播通知範本改善</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Android推播通知先前以單一固定版面呈現：影像一律會置中對齊，長內文會被截斷。 此版本在製作時引入範本選擇器，讓行銷人員可控制Android推播通知的版面。</p>
<p>有以下改良功能可供使用：</p>
<ul>
<li><b>配置選擇</b>：編寫Android推播時新增推播通知配置選擇器（標準/展開）。</li>
<li><b>標準版面配置為「顯示整個影像」</b>：選擇裁切成填色與縮放成符合。</li>
<li><b>展開的版面</b>：不含截斷的多行內文，加上選用的大圖示縮圖。</li>
<li><b>收合內文（展開版面）</b>：為收合狀態設定個別較短的內文。</li>
</ul>
</td>
</tr>
</tbody>
</table>


* **自訂SMS BYOP驗證彈性** — 您現在可以在連線您的SMS提供者的OAuth設定時，設定&#x200B;**自訂驗證標頭**，包括權杖在傳出訊息中的放置位置以及權杖請求本身的格式。

* **直接郵件 — 自動分割大型檔案** — 直接郵件檔案現在可在約超過20 GB時自動分割為多個部分，或透過在檔案路由設定中選擇目標檔案大小來手動分割。

* **直接郵件 — 增加對象上限** — 直接郵件管道對象上限已從300萬個設定檔增加到1億個，讓您可鎖定更大的對象，而不會發生檔案建立錯誤。

### 電子郵件頻道 {#sep-26-email-channel}

此版本的電子郵件頻道即將提供下列功能和改善。

<table>
<thead>
<tr>
<th><strong>覆寫電子郵件通道組態設定</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>建立您的歷程和行銷活動時，您現在可以直接在歷程或行銷活動動作層級覆寫從所選管道設定衍生的電子郵件引數。</p>
<p>這可讓您個人化電子郵件標題欄位（<strong>來自名稱</strong>、<strong>來自電子郵件前置詞</strong>、<strong>回覆名稱</strong>和<strong>回覆電子郵件</strong>）、執行位址和清單取消訂閱值，使用設定檔屬性或內容資料以取得更精確的控制權。 特別是，這允許寄件者詳細資料反映每個收件者的相關顧問、位置或分支，而不是透過單一公司地址路由傳送所有傳送。</p>
</td>
</tr>
</tbody>
</table>

* **電子郵件動作層級的隱藏清單覆寫** - Journey Optimizer現在可讓您直接在歷程與行銷活動的電子郵件動作層級覆寫隱藏清單行為。 這樣一來，團隊在需要專用傳送設定的作業或法規遵循關鍵通訊時，就能擁有更大的彈性，同時還能保留所有其他傳送的現有全域隱藏清單控制項。 此增強功能可協助組織精準處理例外狀況，而不會變更其更廣泛的隱藏治理模型。

* **電子郵件製作中的URL語法驗證** - Journey Optimizer現在會驗證電子郵件製作流程中先前的URL，並在偵測到語法格式錯誤時顯示更清楚的指引。 這有助於作者在定稿前找出問題、減少發佈錯誤，並提升傳送可信度。

### 電子郵件設計工具 {#sep-26-email-designer}

此版本中的電子郵件Designer即將提供下列功能和改善。

<table>
<thead>
<tr>
<th><strong>電子郵件主題變體的深色模式支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件主題現在支援深色模式，因此每個顏色變體都可以呈現為收件者量身打造的外觀，適合在啟用深色模式的使用者端中檢視您的電子郵件。</p>
<p>啟用後，系統會自動為每個變體產生預設的深色調色盤，而您可以使用不同的調色盤或您自己的自訂顏色來進一步自訂調色盤 — 與淺色模式設計無關，因此在一個模式中所做的變更不會影響另一個模式。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>直接在電子郵件Designer中從PSD檔案匯入Dynamic Media範本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件Designer的Dynamic Media元件現在可讓您在瀏覽現有Dynamic Media範本之外，直接匯入Photoshop (PSD)檔案為新範本。 將PSD檔案拖放至元件中，Adobe Journey Optimizer會自動將其轉換為儲存在Dynamic Media中的動態媒體範本，不需要手動轉換或穿過Adobe Experience Manager來迴轉換。 匯入後，您可使用內建的Dynamic Media編輯器編輯範本，這與電子郵件Designer中的Adobe Express內容使用相同的體驗。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件Designer中的新表格元件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件Designer現在包含內建<strong>表格元件</strong>，可讓您直接在電子郵件中建構列和欄的內容。 將元件拖放至畫布上、自訂列和欄數，並獨立設定每個儲存格的樣式，以建立清晰、有組織的版面配置，而不依賴自訂HTML。</p>
</td>
</tr>
</tbody>
</table>

* **電子郵件主題中自訂字型的遞補字型** — 您現在可以為任何透過電子郵件主題套用的自訂(Web)字型定義遞補字型。 如果訂閱者的電子郵件使用者端不支援自訂字型，Adobe Journey Optimizer會自動顯示指定的遞補字型，而不會將選項保留給電子郵件使用者端的預設值。 這可讓電子郵件印刷樣式更貼近您的品牌方針，並減少電子郵件使用者端間的字型轉譯不一致問題。

### 協調的行銷活動 {#sep-26-oc}

下列功能和改進功能將新增到此版本的協調行銷活動。

<table>
<thead>
<tr>
<th><strong>或是加入協調行銷活動的活動</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在協調的行銷活動中，<strong>加入活動</strong>現在支援AND和OR加入條件。 使用OR邏輯時，完成任一上游分支（而非全部）的設定檔會沿著單一共用下游路徑繼續。 如此一來，就可以直接在畫布上建立「如果A、B或C，則執行此動作」的模式，而不需跨不同分支重複下游步驟。</p>
</td>
</tr>
</tbody>
</table>

* 協調行銷活動的&#x200B;**LINE頻道** - LINE現在可做為協調行銷活動的原生傳出頻道，連同電子郵件、簡訊和推播。 您可以直接從行銷活動畫布建立及傳送LINE訊息，包括文字、貼圖、影像、影片、位置資料和Flex訊息，在日本和APAC等以LINE為主的市場支援促銷、交易和持續參與使用案例。 此功能先前以「有限可用性」發行，現已正式推出。

* **新的協調行銷活動監控API** — 新的&#x200B;**API規格**&#x200B;現在可用於協調行銷活動，可讓您以程式設計方式建立、管理和觸發協調行銷活動，與外部系統和自動化管道進行更深入的整合。

* **直接加入UX改良功能** — 從相關集合新增屬性時，您現在可以在三種加入模式（新預設值，警告您卡式產品對效能的潛在影響，加上現有的彙總和進階模式）之間選擇，讓您更容易在建置查詢之前瞭解查詢的取捨。

* **促銷活動協調流程監控** — 現在有新的使用者介面可用，以追蹤協調促銷活動細分所使用的關聯式存放區資料的擷取狀態和最新狀態。 它可讓您直接檢視傳送批次對象之資料的健康狀態。 Adobe Experience Platform的「監控」控制面板中新增的「促銷活動協調」索引標籤，能顯示關聯式存放區資料流程（擷取/更新/刪除/失敗/略過的記錄）的健康情況，並具備向下鑽研圖表和每個資料流程/資料集劃分，包括譜系。


### 報表 {#sep-26-reporting}

以下功能即將在此版本中報告。

<table>
<thead>
<tr>
<th><strong>Data Management中的新輸入監檢視形</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以從<strong>資料管理&gt;監視&gt; Edge</strong>直接監視傳入資料健康情況，共有六個新的圖表涵蓋輸送量、延遲和主張事件：</p>
<ul>
<li><strong>AJO輸入輸送量</strong> — 一段時間的整體輸入輸送量（每秒記錄數）。</li>
<li><strong>AJO傳入輸送量劃分</strong> — 依位置劃分的傳入輸送量。</li>
<li><strong>AJO傳入延遲</strong> — 傳入要求延遲（以毫秒為單位），依值分佈（P50、P90等）劃分。</li>
<li><strong>AJO傳入主張事件輸送量</strong> — 主張事件的輸送量（使用者互動、檢視或觸發個人化優惠時產生的追蹤訊號）。</li>
<li><strong>依管道的AJO傳入主張事件輸送量</strong> — 依傳入管道（CBE、應用程式內、內容卡）劃分的主張事件輸送量。</li>
<li><strong>依事件型別</strong>的AJO傳入主張事件輸送量 — 依事件型別（已解除、已隱藏、已顯示、已觸發、已互動、已傳送）劃分的主張事件輸送量。</li>
</ul>
</td>
</tr>
</tbody>
</table>

### 可用性改進功能 {#sep-26-usability}

* **內容模擬體驗中的可用性改善** — 新的內容模擬體驗現在可讓您命名並組織變體以便輕鬆比較、直接從每個卡片複製或刪除變體詳細資料、依需求檢視完整屬性路徑和每個卡片管道設定，以及從更顯眼的上傳按鈕上傳您自己的CSV、JSON或JSONL設定檔。

* **片段驗證警示中的AI總覽** — 片段驗證警示對話方塊現在包含AI總覽，其中總結並說明了驗證問題（例如格式錯誤的運算式、缺少設定檔欄位以及無效的JSON），讓使用者可以更快進行疑難排解。

* **行銷活動、歷程及協調行銷活動的統一行事曆** — 歷程及行銷活動的行事曆檢視現在會從個別的清查移至統一的左側邊欄可存取功能表，這兩個功能表都會顯示在一個合併的檢視中。

