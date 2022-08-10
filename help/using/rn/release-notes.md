---
title: 發行說明
description: Journey Optimizer 發行說明
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 8766f64c4ea7985c6c9d6e4ba022ef6b1fc0dbed
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 86%

---

# 發行說明 {#release-notes}

本頁面列出[!DNL Journey Optimizer]所有新功能和改進項目。您還可以參閱[最新文件更新](documentation-updates.md)頁面以了解更多變更。

[!DNL Adobe Experience Platform] 上內建的原生 [!DNL Adobe Journey Optimizer] 延續了最新版本的創新和改進內容。 欲深入瞭解這些變動，可參閱 [Adobe Experience Platform 發行說明](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=zh-Hant){target=&quot;_blank&quot;}。

![電子報](../assets/do-not-localize/nl-icon.png) 立即註冊 [Adobe Journey Optimizer 季度電子報](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} ，直接把每季最新產品更新、激勵人心的故事、使用案例、提示等內容傳送到您的收件匣。

## 2022 年 7 月發行版本 {#july-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>全新內嵌訊息流程</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 為歷程的訊息編寫提供全新流程。 線上傳送訊息消息將為使用者節省大量時間，並簡化在 Journey Optimizer 建立和傳遞電子郵件、推播通知或簡訊的工作流程。 透過將訊息作為單獨的步驟刪除，作為 Journey Canvas 動作的一部分都可內嵌編輯，使用者需要按更少的按鈕並導覽較少的畫面來設計和編輯其內容。</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>如需詳細資訊，請參閱<a href="../messages/get-started-content.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>以屬性為基礎的存取控制 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以使用定義組織或資料使用範圍的標籤標示身分綱要欄位。 管理員可以使用權限介面定義涵蓋 XDM 綱要欄位的存取原則，並更好地管理使用者或使用者群組 (內部、外部或協力廠商使用者) 的存取權限，以及管理對特定類型資料 (即敏感個人資料/SPD) 的存取權限。</p>
<p>以屬性為基礎的存取控制目前僅限於選定使用者，將在未來的版本中同步到所有環境。</p>
<p>如需詳細資訊，請參閱<a href="../administration/attribute-based-access.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>批次決策作業</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以從使用者介面執行批次決策作業，這樣我就不需要開發人員來執行批次 API 作業，而且我可以減少行銷所需的時間。 此新介面允許您建立作業及管理目前/過去的作業。</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>如需詳細資訊，請參閱<a href="../offers/batch-delivery.md">詳細文件。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>在您的決定中自動執行最佳優惠方案 (可用性限制)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以在決策管理中使用個人化最佳化模型系統。 這種新種類模型允許您根據區段及優惠方案市場對優惠進行最佳化及個人化。</p>
<p>個人化最佳化 AI 模型的使用目前僅限於選定使用者，將在未來的版本中同步到所有環境。</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>如需詳細資訊，請參閱<a href="../offers/ranking/personalized-optimization-model.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

### 改進項目

**歷程**

* **結束旅程**  — 在旅程畫布中， **結束** 活動已從調色板中刪除。 現在，每個路徑的末尾預設添加結束標籤，無法刪除。 這種改進能夠更好地報告客戶從行程中退出的位置，而無需從行程從業者處採取任何操作。 請參閱 [文檔](../building-journeys/journey-end.md) 和 [特徵視頻](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}。

**訊息**

* 訊息預設集現在是 **頻道介面**。 [進一步了解](../configuration/channel-surfaces.md)

**管理**

* **PTR 記錄版本** - 現在當更新 PTR 記錄時，處理時間最多只需 3 小時。 [了解更多](../configuration/ptr-records.md#processing)

* **允許清單 UI** — 您現在可以使用 Journey Optimizer 使用者介面將新電子郵件地址或網域新增到允許清單。 [了解更多](../configuration/allow-list.md)

* **允許清單邏輯更新** - 現在，即使清單為空，允許清單邏輯在功能啟用後立即適用。 [了解更多](../configuration/allow-list.md#logic)

* **URL跟蹤參數**  — 現在，您可以使用表達式編輯器在電子郵件曲面（即預設）中配置URL跟蹤參數。 [了解更多](../configuration/email-settings.md#url-tracking)

**Offer Decisioning**

* **對象規模** - 當建立決定規則、選擇區段或規則以設定優惠方案適用性或將區段或規則新增到決定範圍時，新的對象規模預估元件現在顯示在使用者介面中。