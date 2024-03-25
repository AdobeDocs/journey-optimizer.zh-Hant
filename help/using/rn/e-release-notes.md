---
solution: Journey Optimizer
product: journey optimizer
title: 發行說明
description: Journey Optimizer 搶先發行說明
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
hide: true
hidefromtoc: true
source-git-commit: f957737aa741cc8b854912414d15154489d1b0b0
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 100%

---

# 早期發行說明 {#e-release-notes}

[!DNL Adobe Journey Optimizer]持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

至發行日期之前，下方的搶先發行說明如有變更，恕不另行通知。 連結、畫面及更新的文件會在發行當日發佈於[發行說明](release-notes.md)。

## 2024 年 3 月搶先發行說明 {#e-2024}

**發行日期**： 2024 年 3 月 19 至 20 日

### 新功能 {#e-features}

此發行版本提供的新功能詳述如下。

<table>
<thead>
<tr>
<th><strong>程式碼型體驗</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>透過新的程式碼型體驗管道，Adobe Journey Optimizer 可讓您針對任何傳入屬性進行進階個人化及測試，跨不同接觸點 (例如網頁應用程式、行動應用程式、桌面應用程式、視訊主控台、電視連結的裝置、智慧型電視、資訊站、ATM、IoT 裝置等) 達成量身打造的無縫傳遞體驗。</p>
<P>主要功能包括：</p>
<ul><li> 通用個人化：擴充所有接觸點的個人化體驗，確保一致且量身打造的使用者歷程</li>
<li>精細的編輯精確度：在應用程式或網頁內的個別位置編輯特定內容</li>
<li>多樣化實施：支援伺服器端、API 或 SDK 型實施方法，以便順暢整合您的開發環境。</li></ul></p>
<p>如需詳細資訊，請參閱<a href="../code-based/get-started-code-based.md">詳細文件</a>。</p>
<img src="assets/do-not-localize/code-based.gif">
</tr>
</tbody>
</table>

### 改進項目 {#e-improvements}

此發行版本隨附下列改進項目。

**內容範本**

* **縮圖** - **網格檢視**&#x200B;模式現可用於內容範本，展示縮圖以便改善視覺化存取。目前僅支援電子郵件 HTML 範本。 [了解更多](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >此功能以有限可用性 (LA) 形式向一小部分客戶發布。

**歷程**

歷程編寫生命週期已新增新中介狀態：

* **正在發佈**&#x200B;狀態介於&#x200B;**草稿**&#x200B;狀態與&#x200B;**即時**&#x200B;狀態之間
* **正在停止**&#x200B;狀態介於&#x200B;**即時**&#x200B;狀態與&#x200B;**已停止**&#x200B;狀態之間
* **正在啟用測試模式**&#x200B;或&#x200B;**正在停用測試模式**&#x200B;狀態介於&#x200B;**草稿**&#x200B;狀態與&#x200B;**草稿 (測試)**&#x200B;狀態

當歷程處於中介狀態時，其是唯讀。