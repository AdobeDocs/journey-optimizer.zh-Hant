---
solution: Journey Optimizer
product: journey optimizer
title: 設定行動裝置和網頁
description: 瞭解如何設定和監控行動裝置和網路頻道
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 管道，表面，技術，引數，最佳化工具
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: 549efb9e12dccedb27335553194e09deab09a35f
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 17%

---

# 開始使用引導式管道設定 {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="行動裝置和網頁設定名稱"
>abstract="輸入您的行動或網頁設定名稱。此名稱將用於使用引導式管道設定自動建立的每個資源。"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="使用保證進行驗證"
>abstract="Adobe Experience Platform保證內嵌在此工作流程中，可協助您檢查SDK實作，以及模擬和驗證應用程式事件。"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home" text="Adobe Experience Platform Assurance 概觀"

此設定有助快速設定行銷頻道，確保隨時在都能在 Experience Platform、Journey Optimizer 資料收集取得所有必要資源。 這可讓您的行銷團隊從行銷活動和歷程建立開始。

「引導式頻道」設定支援下列平台和頻道。

* 平台和SDK：

   * Apple的Swift，iOS

   * Android州科特林

   * Javascript，網頁

* 頻道：

   * 行動應用程式內

   * 行動推送訊息

   * Web Basic

請注意，您想要設定的每個平台都需要建立個別的設定。 這是因為每個應用程式都需要獨特的管道設定，這樣就能靈活地決定您想要用於每個平台的管道。

## 先決條件 {#prereq}

* 為了有效實作，擁有修改網站或行動程式碼許可權和技術能力的組織成員必須監督設定。

  以下是執行「引導式管道設定」所需的許可權。

+++ 必要權限

  <table>
    <thead>
      <tr>
        <th><strong>解決方案</strong></th>
        <th><strong>權限</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <p>資料收集</p>
        </td>
        <td>
          <ul>
            <li>公司權利&gt;屬性</li>
            <li>屬性權利：開發、發佈、管理擴充功能和環境</li>
            <li>應用程式表面：管理應用程式設定</li>
         </ul>
        </td>
      </tr>
      <tr>
        <td>
          <p>Adobe Experience Platform</p>
        </td>
        <td>
        <ul>
            <li>資料收集：管理資料串流</li>
           <li>沙箱：授予沙箱的存取權</li>
            <li>管理區段：讀取、建立、編輯和刪除區段定義</li>
            <li>管理設定檔：讀取、建立、編輯和刪除設定檔</li>
            <li>讀取資料集：資料集的唯讀存取權</li>
            <li>讀取方案：對方案的唯讀存取權</li>
            <li>讀取身分名稱空間：身分名稱空間的唯讀存取權</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>
         <p>Adobe Journey Optimizer</p>
        </td>
        <td>
          <p>行銷活動：管理和發佈行銷活動</p>
        </td>
      </tr>
    </tbody>
  </table>

+++

* 如果您使用現有設定選項，請確定您使用下列Adobe Experience Platform Mobile SDK擴充功能版本。 如需SDK設定的詳細資訊，包括必要的相依性和初始化程式碼，請參閱[下列檔案](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks?lang=en)。

  適用於Android

   * 行動核心v3.1.0或更新版本
   * Adobe Journey Optimizer v3.1.0或更新版本

  適用於iOS

   * 行動核心v5.2.0或更新版本
   * Adobe Journey Optimizer v5.1.1或更新版本

## 自動建立的資源 {#auto-create-resources}

引導式管道設定簡化了行銷管道的快速設定，使所有基本資源都能隨時在Experience Platform、Journey Optimizer和資料收集應用程式中使用。 這可讓您的行銷團隊快速開始建立行銷活動和歷程。 以下是在引導式管道設定過程中自動產生和設定的資源清單。

瀏覽下列標籤，存取自動產生之所有資源的完整清單：

>[!BEGINTABS]

>[!TAB iOS]

對於&#x200B;**初始組態**，以下是在您按一下&#x200B;**自動建立資源**&#x200B;時，**組態詳細資料**&#x200B;畫面上建立的所有資源的完整清單。

<table>
  <thead>
  <tr>
  <th><strong>解決方案</strong></th>
  <th><strong>自動建立的資源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>標記</p>
  </td>
  <td>
  <ul>
  <li>行動標籤屬性</li>
  <li>規則</li>
  <li>資料元素</li>
  <li>資料庫</li>
  <li>環境（測試、生產、開發）</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>標籤擴充功能</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience PlatformEdge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP保證</li>
  <li>同意（已啟用預設同意政策）</li>
  <li>身分（使用預設ECID，使用預設拼接規則）</li>
  <li>行動核心</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>保證工作階段</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>資料流</p>
  </td>
  <td>
  <p>使用服務的資料流</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>資料集</li>
  <li>綱要</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

對於&#x200B;**頻道設定**，以下是在&#x200B;**新增頻道**&#x200B;畫面上建立的所有資源的完整清單。

<table>
  <thead>
  <tr>
  <th><strong>解決方案</strong></th>
  <th><strong>自動建立的資源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>頻道設定</li>
  <li>上傳推送認證（僅限行動推送訊息）</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

對於&#x200B;**初始組態**，以下是在您按一下&#x200B;**自動建立資源**&#x200B;時，**組態詳細資料**&#x200B;畫面上建立的所有資源的完整清單。

<table>
  <thead>
  <tr>
  <th><strong>解決方案</strong></th>
  <th><strong>自動建立的資源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>標記</p>
  </td>
  <td>
  <ul>
  <li>行動標籤屬性</li>
  <li>規則</li>
  <li>資料元素</li>
  <li>資料庫</li>
  <li>環境（測試、生產、開發）</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>標籤擴充功能</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience PlatformEdge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP保證</li>
  <li>同意（已啟用預設同意政策）</li>
  <li>身分（使用預設ECID，使用預設拼接規則）</li>
  <li>行動核心</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>保證工作階段</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>資料流</p>
  </td>
  <td>
  <p>使用服務的資料流</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>資料集</li>
  <li>綱要</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

對於&#x200B;**頻道設定**，以下是在&#x200B;**新增頻道**&#x200B;畫面上建立的所有資源的完整清單。

<table>
  <thead>
  <tr>
  <th><strong>解決方案</strong></th>
  <th><strong>自動建立的資源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>頻道設定</li>
  <li>上傳推送認證（僅限行動推送訊息）</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB 網路]

對於&#x200B;**初始組態**，以下是在您按一下&#x200B;**自動建立資源**&#x200B;時，**組態詳細資料**&#x200B;畫面上建立的所有資源的完整清單。

<table>
  <thead>
  <tr>
  <th><strong>解決方案</strong></th>
  <th><strong>自動建立的資源</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>標記</p>
  </td>
  <td>
  <ul>
  <li>行動標籤屬性</li>
  <li>規則</li>
  <li>資料元素</li>
  <li>資料庫</li>
  <li>環境（測試、生產、開發）</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>標籤擴充功能</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience PlatformEdge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP保證</li>
  <li>同意（已啟用預設同意政策）</li>
  <li>身分（使用預設ECID，使用預設拼接規則）</li>
  <li>行動核心</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>保證工作階段</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>資料流</p>
  </td>
  <td>
  <p>使用服務的資料流</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>資料集</li>
  <li>綱要</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]
