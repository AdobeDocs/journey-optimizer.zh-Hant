---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
hide: true
hidefromtoc: true
source-git-commit: c9be63086b63fb5f4d6094d8bc7690464cf6b768
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 21%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月最後一週整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2023年9月早期發行說明 {#sept-rn-2023}

**發行日期**： 2023年9月26日至27日

### 新功能{#sept-2023-features}

此發行版本提供下列新功能。


<table>
<thead>
<tr>
<th><strong>合併的管道報表</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>管道報表功能為分析師和行銷人員提供管道層級流量和參與量度的全面概觀。 若要存取「報表」功能表，您必須擁有「檢視管道報表」許可權。</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>資料集匯出目的地(GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在普遍提供匯出至雲端儲存空間目的地的Journey Optimizer資料集。 此功能可讓您與雲端儲存空間位置建立即時連線，以匯出資料集的內容。 </p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>每個沙箱行動應用程式憑證儲存</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>此新功能可讓您輕鬆管理推送認證，並將其與應用程式介面中的專用沙箱建立關聯。</p>
<p>如需詳細資訊，請參閱<a href="../in-app/inapp-configuration.md">詳細文件</a>。</p>
</tr>
</tbody>
</table>

### 改進項目 {#sept-2023-improvements}

此發行版本隨附下列改進項目。

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**個人化**

* 除了視覺化片段之外，現在還可以透過運算式編輯器從Journey Optimizer介面建立、儲存及重複使用運算式片段。 運算式片段會取代先前儲存的運算式。
* 您現在可以使用Adobe Experience Platform計算屬性在Journey Optimizer中進行個人化。 計算屬性是根據擷取到Adobe Experience Platform中的啟用設定檔體驗事件資料集計算的彙總值。

**警報**

* 已引進兩種新型別的系統警示。 您現在可以在自訂動作或讀取區段失敗時收到通知。

**網路頻道**

* 單頁應用程式(SPA)現在可以在網頁視覺編輯器中編寫。 您現在可以選取要套用網頁修改的特定檢視。 檢視可定義為整個網站或網站上一組視覺元素，例如首頁、整個產品網站或所有結帳頁面上的傳遞偏好設定框架。 需要一次性開發人員設定，才能定義Adobe Experience Platform Web SDK實作中的檢視，讓行銷人員能夠在SPA上建立並執行Adobe Journey Optimizer網路行銷活動。

* 使用Web設計工具編輯頁面時，您現在可以直接從「修改」窗格新增對內容的新變更，而無需從設計工具介面選取元件並進行編輯。
* 設定網頁子網域時，除了使用已委派給Adobe的子網域外，您現在可以選擇新增自己的子網域。

**歷程**

* 自訂動作回應功能現在為GA。 這可讓您在自訂動作中運用API呼叫回應，並根據這些回應協調您的歷程。 此外，已新增護欄，以將所有海關動作限製為每個端點5000次呼叫/秒。
* 複製歷程時，您現在可以定義歷程副本的名稱。
* 您可在等待活動中定義的持續時間上限現在是29天，而不是30天。

**電子郵件頻道**

電子郵件表面設定中的新選項可讓您選擇傳送交易式訊息給設定檔，即使其電子郵件地址在Adobe Journey Optimizer隱藏清單中亦然。

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->