---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
feature: Release Notes
topic: Content Management
description: Adobe Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: b1f23144d996e152018519b540d70f45b7c58695
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 83%

---

# 發行說明 {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="新增功能？"
>abstract="**Adobe Journey Optimizer** 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。"

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於發行說明。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變更，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target="_blank"}。

![電子報](../assets/do-not-localize/nl-icon.png)立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"}，把每季最新產品更新、精彩故事、使用案例、提示等內容直接傳送到您的收件匣。

## 9 月份更新版 {#9-2024}

<table>
<thead>
<tr>
<th><strong>AI Assistant — 內容加速器 </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在您建立並個人化訊息後，請使用Journey Optimizer中的AI Assistant for Content Acceleration將您的內容提升到新的境界。 您現在可以使用AI助理透過實驗不同的主要標題和影像，以最佳化訊息的影響。 每個變體都會視為獨特的處理來管理，以測量並比較哪個標題能有效產生更多點按次數。</p>
<p>透過<a href="https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator">我們的即時功能預覽</a>，親身體驗親身體驗，讓您親身體驗功能並充分瞭解其功能。</a></p>
<p>如需詳細資訊，請參閱<a href="../content-management/gs-generative.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>推出日期： 9月12日</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>引導式頻道設定</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>引導式頻道設定讓您可以透過統一體驗，將頻道設定自動化，並加以驗證，便可使用 Journey Optimizer，加速快速入門的流程。 這項全新引導式設定能簡化快速頻道設定，確保能在 Experience Platform、Journey Optimizer 和資料彙集中，輕鬆安裝所有必要資源，確保一切運作都能順暢。這讓行銷、產品和資料工程團隊可以快速展開行銷活動，同時建立歷程。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/set-mobile-config.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>推出日期： 9月3日</p>
</br>
</td>
</tr>
</tbody>
</table>

**歷程**

（可用性日期： 9月10日） **重試功能** — 擷取匯出作業時，現在預設會針對對象觸發的歷程（從&#x200B;**讀取對象**&#x200B;或&#x200B;**商業事件**&#x200B;開始）套用重試。 如果在匯出作業建立期間發生錯誤，將每隔10mn進行重試，最長為1小時。 之後，我們會將其視為失敗。 因此，這些型別的歷程可在排程時間後最多1小時執行。 [了解更多](../building-journeys/read-audience.md#retries)

## 2024 年 8 月發行說明 {#8-2024}

**發行日期**：2024 年 8 月 20-21 日

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

### 新功能 {#8-features}

此發行版本提供下列詳細介紹的新功能。

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>改善的頻道設定</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>已增強目前的管道表面功能，以在所有管道中採取一致的方法。您現在可以為任何管道定義、管理和重複使用這些設定，包括網頁、應用程式內訊息或基於程式碼的體驗。</p>
<p><ul>
<li>管道表面現在已重新命名為<strong>管道設定</strong></li>
<li>您可以附加一或多個行銷動作，以強制執行同意和資料治理原則</li>
<li>物件層級存取控制 (OLAC) 現在可用於每個管道設定，可讓您決定允許哪些使用者建立或使用特定設定</li>
<li>對於某些管道，您可以建立以多個平台為目標的管道設定。以下為可鎖定網頁、iOS 應用程式和 Android 應用程式的應用程式內傳送訊息管道設定範例。</li>
</ul></p>
<p>如需詳細資訊，請參閱<a href="../configuration/channel-surfaces.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Marketo Engage 自訂動作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以將 Adobe Journey Optimizer 與Adobe Marketo Engage 整合，來建置您的 B2B 使用案例。 新的自訂動作可讓您從歷程將資料收錄到 Marketo。</p>
<p>如需詳細資訊，請參閱<a href="../action/marketo-engage.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>內容片段變數</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>片段全域變數可增強現有片段功能，以提高內容再使用性與指令碼使用案例的效率。 片段現在可以使用輸入變數，以及建立可用於行銷活動和歷程內容的輸出變數。在<a href="../personalization/use-expression-fragments.md">運算式片段</a>和<a href="../email/use-visual-fragments.md">視覺片段</a>這兩種片段中，皆可使用輸入變數。您可以使用這些變數，在行銷活動和歷程個人化您的訊息內容和參數。</p>
<p>如需詳細資訊，請參閱<a href="../personalization/use-expression-fragments.md">詳細文件</a>。</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP 暖身工作流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>推出日期：8 月 13 日</p>
<p>如果您使用全新的 IP 位址傳送電子郵件，現在可以直接從使用者介面輕鬆執行 IP 暖身工作流程。 Adobe Journey Optimizer 提供標準化和有效率的方式，讓您的 IP 位址按照最佳實務來暖身，以實現最佳傳遞能力。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/ip-warmup-gs.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改進項目 {#8-improvements}

此發行版本隨附下列改進項目。

**歷程**

* 在&#x200B;**條件**&#x200B;活動中，預設情況下，**[!UICONTROL 時間條件]**&#x200B;現在會從 00:00 到 12:00，依小時設定。 [閱讀全文](../building-journeys/condition-activity.md#time_condition)
* 當建立歷程時，現在會從&#x200B;**警示**&#x200B;按鈕顯示提醒，跟其他提醒保持同步，提供一致的使用者體驗。[閱讀全文](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* 已改善歷程工具列的縮放選項：您現在可以看到縮放百分比，可以更輕鬆將重設縮放值。

<!--**Audiences and Profiles**-->

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
<!--* When targeting a custom upload (CSV file) audience, you can now use attributes from the file in your campaigns and journeys. These attributes are available in the personalization editor, to personalize your messages, and the journey advanced expression editor.-->
<!--* The License usage dashboard now shows the count of Engageable Profiles. [Read more](../audience/license-usage.md)-->

**推播管道**

* 您現在可於 Adobe Journey Optimizer 管道設定的設定中新增行動應用程式推播認證。您不再需要在 Adobe Experience Platform 資料彙集中建立應用程式表面。

### 其他變更 {#changes}

**報告**

* 目前的報告體驗將於 10 月版本發行後淘汰。在此日期之後，新的報告體驗將成為標準體驗。建議您自行熟悉新功能，以確保順利轉換。

[開始使用 Journey Optimizer 新報告介面](../reports/report-gs-cja.md)

* 已將新的使用案例新增至全新報告體驗：

   * 可直接在報告中建立自訂計算量度。
   * 請從報告資料那邊建立對象。
   * 使用探索分析工具，可從已選取的&#x200B;**[!UICONTROL 維度]**&#x200B;和&#x200B;**[!UICONTROL 量度]**，輕鬆地建立表格和視覺效果。

  如需詳細資訊，請參閱[詳細文件](../reports/report-cja-manage.md)。
