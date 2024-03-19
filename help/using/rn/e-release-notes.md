---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 44170e04be45c5b3df6343767dc7e640a61940f8
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 29%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更會在每個月底的 [發行說明](release-notes.md).

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024年3月早期發行說明 {#e-2024}

**發行日期**： 2024年3月19至20日

### 新功能 {#e-features}

此版本提供下列詳細的新功能。

<table>
<thead>
<tr>
<th><strong>程式碼型體驗</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過新的程式碼型體驗頻道，Adobe Journey Optimizer可讓您針對任何傳入屬性進行進階個人化和測試，實現跨不同接觸點（例如網頁應用程式、行動應用程式、案頭應用程式、視訊主控台、電視連線裝置、智慧型電視、資訊站、ATM、物聯網裝置等）的量身打造體驗無縫交付。</p>
<P>主要功能包括：</p>
<ul><li> 通用個人化：擴充所有接觸點的個人化體驗，確保有凝聚力且量身打造的使用者歷程</li>
<li>精細的編輯精確度：在應用程式或網頁內的個別位置編輯特定內容</li>
<li>多樣化實作：支援伺服器端、API或SDK型實作方法，以便順暢地與您的開發環境整合。</li></ul></p>
<p>如需詳細資訊，請參閱<a href="../code-based/get-started-code-based.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/code-based.gif">
</tr>
</tbody>
</table>

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**內容範本**

* **縮圖** - A **格點檢視** 內容範本現在可使用此模式，顯示縮圖以改善視覺存取。 目前僅支援電子郵件HTML範本。 [了解更多](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >此功能以有限可用性 (LA) 形式向一小部分客戶發布。

**歷程**

歷程編寫生命週期已新增新的中繼狀態：

* **發佈** 介於兩者之間的狀態： **草稿** 狀態與 **即時** 狀態
* **正在停止** 介於兩者之間的狀態： **即時** 狀態與 **已停止** 狀態
* **啟用測試模式** 或 **停用測試模式** 介於兩者之間的狀態： **草稿** 狀態與 **草稿（測試）** 狀態

當歷程處於中繼狀態時，它是唯讀的。