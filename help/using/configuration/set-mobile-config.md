---
solution: Journey Optimizer
product: journey optimizer
title: 設定行動裝置和網頁
description: 了解如何設定和監視行動和網路管道
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 管道, 表面, 技術, 參數, 最佳化工具
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
TQID: https://experienceleague.adobe.com/wZkMADPKflUPDtBaSa0eEdHESX-0X0MQCqmk98fZn9k
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2: id: d2e8a157-b3b0-4143-9ff3-809bf400be56id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 889
ht-degree: 96%

---

# 開始使用引導式管道設定 {#set-mobile-config}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解引導式管道設定工作流程如何自動建立在Adobe Journey Optimizer中設定行動裝置和網路管道所需的標籤屬性、資料串流和管道設定。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="行動裝置和網頁設定名稱"
>abstract="輸入您的行動裝置或網頁設定名稱。 此名稱將用於使用引導式管道設定自動建立的每個資源。"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="使用保證進行驗證"
>abstract="將 Adobe Experience Platform Assurance 嵌入此工作流程中，可協助您檢查 SDK 實作，以及模擬和驗證應用程式事件。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/experience-platform/assurance/home" text="Adobe Experience Platform Assurance 概觀"

**引導式管道設定**&#x200B;是 Adobe Journey Optimizer 中簡化的工作流程，可協助您快速設定行動裝置和網頁行銷管道。 它位於&#x200B;**管理** > **管道** > **管道設定**&#x200B;之下，並會在 Adobe Experience Platform、Journey Optimizer 和資料彙集中自動建立基本資源，例如標記屬性、資料串流和管道設定。 您不必手動設定每個元件，而是依照引導式流程為您設定所有內容，讓行銷團隊可以開始建立無延遲的應用程式內訊息、推播通知和網頁體驗。

引導式管道設定支援下列平台與管道。

>[!BEGINTABS]

>[!TAB iOS]

**SDK：** Apple 的 Swift

**管道：**&#x200B;行動應用程式內、行動推播訊息

>[!TAB Android]

**SDK：** Kotlin

**管道：**&#x200B;行動應用程式內、行動推播訊息

>[!TAB 網頁]

**SDK：** Javascript

**管道：** Web Basic

>[!ENDTABS]

請注意，您想要設定的每個平台都需要建立個別的設定。 這是因為每個應用程式都需要獨特的管道設定，這樣就能靈活地決定您想要用於每個平台的管道。

## 先決條件 {#prereq}

* 為了有效實作，擁有修改網站或行動裝置程式碼權限與技術能力的組織成員務必要監督設定。

  以下是執行「引導式管道設定」所需的權限。

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
            <li>公司權利 &gt; 屬性</li>
            <li>屬性權利：開發、發佈、管理擴充功能與環境</li>
            <li>應用程式介面：管理應用程式設定</li>
         </ul>
        </td>
      </tr>
      <tr>
        <td>
          <p>Adobe Experience Platform</p>
        </td>
        <td>
        <ul>
            <li>資料彙集：管理資料流</li>
           <li>沙箱：授予沙箱的存取權</li>
            <li>管理區段：讀取、建立、編輯和刪除區段定義</li>
            <li>管理輪廓：讀取、建立、編輯和刪除輪廓</li>
            <li>讀取資料集：資料集的唯讀存取權</li>
            <li>讀取結構描述：結構描述的唯讀存取權</li>
            <li>讀取身分識別命名空間：身分識別命名空間的唯讀存取權</li>
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

* 如果您使用現有設定選項，請確定您使用下列Adobe Experience Platform Mobile SDK 擴充功能版本。 如需 SDK 設定的詳細資訊，包括必要的相依性與初始化程式碼，請參閱[下列文件](https://experienceleague.adobe.com/zh-hant/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks)。

>[!BEGINTABS]

>[!TAB 對於 iOS]

* Mobile Core v5.2.0 或更新版本
* Adobe Journey Optimizer v5.1.1 或更新版本


>[!TAB 對於 Android]

* Mobile Core v3.1.0 或更新版本
* Adobe Journey Optimizer v3.1.0 或更新版本


>[!ENDTABS]


## 自動建立的資源 {#auto-create-resources}

此設定簡化行銷管道的快速設定，使所有基本資源都能隨時在 Experience Platform、Journey Optimizer 和資料彙集應用程式中使用。 這可讓行銷團隊快速開始建立行銷活動與歷程。 以下是進行引導式管道設定時自動產生和設定的資源清單。

瀏覽下列標籤，存取所有自動產生資源的完整清單：

>[!BEGINTABS]

>[!TAB iOS]

對於&#x200B;**初始設定**，以下是按一下&#x200B;**自動建立資源**&#x200B;時，**設定詳細資料**&#x200B;畫面上建立的所有資源完整清單。

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
  <li>行動標記屬性</li>
  <li>規則</li>
  <li>資料元素</li>
  <li>資料庫</li>
  <li>環境 (中繼、生產、開發)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>標記擴充功能</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>同意 (已啟用預設同意原則)</li>
  <li>身分識別 (使用預設 ECID 搭配預設拼接規則)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>保證</p>
  </td>
  <td>
  <p>Assurance 工作階段</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>資料串流</p>
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
  <li>結構描述</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

對於&#x200B;**管道設定**，以下是&#x200B;**新增管道**&#x200B;畫面上建立的所有資源完整清單。

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
  <li>管道設定</li>
  <li>上傳推播認證 (僅限行動裝置推播訊息)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

對於&#x200B;**初始設定**，以下是按一下&#x200B;**自動建立資源**&#x200B;時，**設定詳細資料**&#x200B;畫面上建立的所有資源完整清單。

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
  <li>行動標記屬性</li>
  <li>規則</li>
  <li>資料元素</li>
  <li>資料庫</li>
  <li>環境 (中繼、生產、開發)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>標記擴充功能</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>同意 (已啟用預設同意原則)</li>
  <li>身分識別 (使用預設 ECID 搭配預設拼接規則)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>保證</p>
  </td>
  <td>
  <p>Assurance 工作階段</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>資料串流</p>
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
  <li>結構描述</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

對於&#x200B;**管道設定**，以下是&#x200B;**新增管道**&#x200B;畫面上建立的所有資源完整清單。

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
  <li>管道設定</li>
  <li>上傳推播認證 (僅限行動裝置推播訊息)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB 網路]

對於&#x200B;**初始設定**，以下是按一下&#x200B;**自動建立資源**&#x200B;時，**設定詳細資料**&#x200B;畫面上建立的所有資源完整清單。

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
  <li>行動標記屬性</li>
  <li>規則</li>
  <li>資料元素</li>
  <li>資料庫</li>
  <li>環境 (中繼、生產、開發)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>標記擴充功能</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>同意 (已啟用預設同意原則)</li>
  <li>身分識別 (使用預設 ECID 搭配預設拼接規則)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>保證</p>
  </td>
  <td>
  <p>Assurance 工作階段</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>資料串流</p>
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
  <li>結構描述</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]

