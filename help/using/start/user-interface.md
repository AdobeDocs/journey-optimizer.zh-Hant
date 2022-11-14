---
solution: Journey Optimizer
product: journey optimizer
title: 使用者介面
description: 瞭解有關 Journey Optimizer 使用者介面的詳細資訊
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 681532f8-1149-465e-92c8-2b5366abc3aa
source-git-commit: a2d05c7f2c00172a6f4e7b9d9f60d1732c91af8a
workflow-type: tm+mt
source-wordcount: '1572'
ht-degree: 100%

---

# 使用者介面 {#cjm-user-interface}

連線至 [Adobe Experience Cloud](http://experience.adobe.com) 並瀏覽至 [!DNL Journey Optimizer]。

瀏覽使用者介面時的重要概念與 Adobe Experience Platform 相同。如需詳細資訊，請參閱 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-ui/ui-guide.html?lang=zh-Hant#adobe-experience-platform-ui-guide){target=&quot;_blank&quot;}。

可用的 UI 元件及功能取決於您的[權限](../administration/permissions.md)和[授權套件](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}。如有任何問題，請聯絡您的 Adobe 客戶成功經理。

>[!NOTE]
>
>本文件將經常更新，以反應此產品使用者介面的最新變更。不過，有些螢幕擷取畫面可能會與使用者介面稍有不同。


## 左側導覽 {#left-nav}

瀏覽左側連結來存取[!DNL Journey Optimizer]功能。

![](assets/ajo-home.png)

>[!NOTE]
>
>可用功能可能會視您的權限與授權合約而有所不同。

您可以在下方左側導覽找到完整的服務與功能清單，以及相關協助頁面的連結。

**首頁**

[!DNL Journey Optimizer] 首頁包含要啟動的主要連結和資源。**[!UICONTROL 最近]**&#x200B;清單提供最近建立事件與歷程的捷徑。 此清單顯示其建立和修改日期和狀態。

**[!UICONTROL 歷程管理]**

* **[!UICONTROL 歷程]** - 建立、設定和協調客戶歷程。[了解更多](../building-journeys/journey-gs.md#jo-build)

* **[!UICONTROL 登陸頁面]** - 建立、設計、測試及發佈登陸頁面。 [了解更多](../landing-pages/get-started-lp.md)

**[!UICONTROL 決策管理]**

* **[!UICONTROL 訂閱詳情]** - 從此功能表存取您最近的資源和資料集。使用此區段建立新優惠。 [了解更多](../offers/offer-library/creating-personalized-offers.md)

* **[!UICONTROL 元件]** - 建立位置、規則和標記。[了解更多](../offers/offer-library/key-steps.md)

**[!UICONTROL 內容管理]**

* **[!UICONTROL 資產]** - [!DNL Adobe Experience Manager Assets Essentials]為資產集中存放庫，可用來填入訊息。[了解更多](../design/assets-essentials.md)

**[!UICONTROL 資料管理]**

* **[!UICONTROL 結構描述]** - 使用 Adobe Experience Platform 在「方案編輯器」這個互動式視覺畫布中建立和管理體驗資料模型 (XDM) 方案。[了解更多](../data/get-started-schemas.md)

* **[!UICONTROL 資料集]** - 所有內嵌至 Adobe Experience Platform 的資料都會以資料集的形式保留在資料湖中。資料集是資料集合的儲存和管理結構，通常是包含方案 (欄) 和欄 (列) 的表格。 [進一步了解](../data/get-started-datasets.md)

* **[!UICONTROL 查詢]** - 使用 Adobe Experience Platform 查詢服務來寫入和執行查詢、檢視以前執行的查詢，以及存取由您組織內的使用者儲存的查詢。[了解更多](../data/get-started-queries.md)

* **[!UICONTROL 監視]** - 使用此功能表在 Adobe Experience Platform 使用者介面中監視資料擷取。[了解更多](https://experienceleague.adobe.com/docs/experience-platform/ingestion/quality/monitor-data-ingestion.html?lang=zh-Hant){target=&quot;_blank&quot;}

**[!UICONTROL 連線]**

* **[!UICONTROL 來源]** - 使用此功能表從多種來源 (例如 Adobe 應用程式、雲端儲存、資料庫等) 擷取資料，並建構、標示和增強傳入資料。[了解更多](get-started-sources.md)

**[!UICONTROL 客戶]**

* **[!UICONTROL 區段]** - 建立和管理 Experience Platform 區段定義，並將它們運用在您的歷程中。[了解更多](../segment/about-segments.md)

* **[!UICONTROL 設定檔]** - 即時客戶設定檔可為個別客戶建立整體檢視，並結合來自多個頻道的資料，包括線上、離線、CRM 和第三方資料。[了解更多](../segment/get-started-profiles.md)

* **[!UICONTROL 識別]** - Adobe Experience Platform 身分服務透過 Adobe Experience Platform 的身分圖表，管理跨裝置、跨頻道及幾乎即時的客戶身分識別。[了解更多](../segment/get-started-identity.md)

**[!UICONTROL 管理]**

* **[!UICONTROL 歷程管理]** - 使用此選單來設定 [事件](../event/about-events.md)、[資料來源](../datasource/about-data-sources.md)和[動作](../action/action.md) ，以用於您的歷程。

* **[!UICONTROL 沙箱]** - Adobe Experience 平台提供的沙箱可將單一執行個體分割成個別的虛擬環境，以利開發及改進數位體驗應用程式。[了解更多](../administration/sandboxes.md)

* **[!UICONTROL 警報]** - 使用者介面可讓您根據 Adobe Experience Platform 可檢視性深入解析顯示的指標查看收到警報的歷史記錄。UI 也可讓您檢視、啟用和停用可用的警報規則。 [了解跟多](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=zh-Hant){target=&quot;_blank&quot;}


## 產品內使用案例 {#in-product-uc}

善用首頁的[!DNL Adobe Journey Optimizer]使用案例，並提供一些快速輸入項目以建立客戶歷程。

![](assets/use-cases-home.png)

可用的使用案例包括：

* **建立測試設定檔**，以使用我們的 CSV 範本建立測試設定檔，以測試個人化訊息和歷程。在[本頁面](../segment/creating-test-profiles.md#use-case-1)瞭解如何實施此使用案例。
* **傳送生日訊息給客戶**，以自動傳送電子郵件祝賀客戶生日。(即將推出)
* **傳送電子郵件以吸引新客戶**，輕鬆傳送最多兩封電子郵件來歡迎新註冊的客戶。(即將推出)
* **傳送推播訊息至匯入的客戶清單**，以快速將推播通知傳送至從 CSV 檔案匯入的客戶清單。(即將推出)

按一下&#x200B;**[!UICONTROL 檢視詳細資料]**&#x200B;以進一步瞭解每個使用案例。

按一下&#x200B;**[!UICONTROL 開始]**&#x200B;按鈕以開始使用案例。

您可以從&#x200B;**[!UICONTROL 檢視使用案例庫]**&#x200B;按鈕存取已執行的案例。

## 協助工具{#accessibility}

[!DNL Adobe Journey Optimizer] 中的協助工具功能繼承自 Adobe Experience Platform：

* 鍵盤協助工具
* 顏色對比
* 驗證必填欄位

在 Adobe Experience Platform 文件中[進一步了解](https://experienceleague.adobe.com/docs/experience-platform/accessibility/features.html?lang=zh-Hant){target=&quot;_blank&quot;}。

您可以在 [!DNL Journey Optimizer] 使用這些常見的鍵盤快速鍵：

| 動作 | 快速鍵 |
| --- | --- |
| 在使用者介面元素、區段和功能表群組之間移動 | Tab 鍵 |
| 在使用者介面元素、區段和功能表群組之間向後移動 | Shift + Tab 鍵 |
| 在區段內移動並將焦點設定為個別元素 | 箭頭 |
| 選取或清除焦點中的元素 | 輸入或空格鍵 |
| 取消選取、摺疊窗格或關閉對話方塊 | Esc 鍵 |

在 Adobe Experience Platform 文件中[進一步了解](https://experienceleague.adobe.com/docs/experience-platform/accessibility/custom.html?lang=zh-Hant){target=&quot;_blank&quot;}。

您可以在 Journey Optimizer 的特定部分使用下列快速鍵：

<table>
  <thead>
    <tr>
      <th>介面元素</th>
      <th>動作</th>
      <th>快速鍵</th>
    </tr>
  </thead>
  <tr>
    <td>歷程、動作、資料來源或事件清單</td>
    <td>建立歷程、動作、資料來源或事件</td>
    <td>C</td>
  </tr>
  <tr>
    <td rowspan="3">草稿狀態的歷程畫布</td>
    <td>從左側色盤的第一個可用位置 (從上到下) 新增活動</td>
    <td>在活動上按兩下</td>
  </tr>
  <tr>
    <td>選取所有活動</td>
    <td>Ctrl + A (Windows)<br/> Command + A (Mac)</td>
  </tr>
  <tr>
    <td>刪除選取的活動</td>
    <td>刪除或退格，然後輸入以確認刪除</td>
  </tr>
  <tr>
  <td rowspan="3">

這些元素的設定窗格：

<ul>
  <li>歷程中的活動</li>
  <li>事件</li>
  <li>資料來源</li>
  <li>動作</li>
</ul>

</td>
    <td>移至下一個要設定的欄位</td>
    <td>Tab 鍵</td>
  </tr>
  <tr>
    <td>儲存變更並關閉設定窗格</td>
    <td>Enter 鍵</td>
  </tr>
  <tr>
    <td>放棄變更並關閉設定窗格</td>
    <td>Esc 鍵</td>
  </tr>
  <tr>
    <td rowspan="4">測試模式中的歷程</td>
    <td>啟用或停用測試模式</td>
    <td>T</td>
  </tr>
  <tr>
    <td>觸發事件歷程中的事件</td>
    <td>E</td>
  </tr>
  <tr>
    <td>

在以區段為基礎的歷程中觸發事件，並為其啟用了&#x200B;**[!UICONTROL 一次單一設定檔]**&#x200B;選項

</td>
    <td>P</td>
  </tr>
  <tr>
    <td>顯示測試記錄</td>
    <td>L</td>
  </tr>
<!-- //Ajouter ce raccourci quand il marchera (actuellement, le raccourci Ctrl/Cmd+F du navigateur a priorité sur celui de AJO).//
  <tr>
    <td>Page with a search bar</td>
    <td>Select the search bar</td>
    <td>Ctrl/Command + F</td>
  </tr>
-->
  <tr>
    <td>文字欄位</td>
    <td>選取所選欄位中的所有文字</td>
    <td>Ctrl + A (Windows)<br/> Command + A (Mac)</td>
  </tr>
  <tr>
    <td rowspan="2">快顯視窗</td>
    <td>儲存變更或確認動作</td>
    <td>Enter 鍵</td>
  </tr>
  <tr>
    <td>關閉視窗</td>
    <td>Esc 鍵</td>
  </tr>
  <tr>
    <td>簡易運算式編輯器</td>
    <td>選取並新增欄位</td>
    <td>在欄位上按兩下</td>
  </tr>
  <tr>
    <td>瀏覽 XDM 欄位</td>
    <td>選取節點的所有欄位</td>
    <td>選擇上層節點</td>
  </tr>
  <tr>
    <td>內容預覽</td>
    <td>選取內容</td>
    <td>Ctrl + A (Windows)<br/> Command + A (Mac)</td>
  </tr>
</table>

## 尋找說明與支援 {#find-help}

從首頁的下半頁面存取 Adobe Journey Optimizer 重要說明頁面。

使用&#x200B;**說明**&#x200B;圖示來存取說明頁面、聯絡支援並分享意見。 您可以從搜尋欄位搜尋說明文章和影片。

![](assets/ajo-help.png)

## 支援的瀏覽器 {#browsers}

Adobe [!DNL Journey Optimizer] 介面的設計可在最新版 Google Chrome 中以最佳方式運作。 您在舊版或其他瀏覽器上使用某些功能時可能會遇到問題。

## 語言偏好設定 {#language-pref}

使用者介面目前提供下列語言版本：

* 英文
* 法文
* 德文

您的預設介面語言是由使用者設定檔中指定的偏好語言所決定。

若要變更您的語言：

* 按一下右上角頭像處的&#x200B;**「偏好設定」**。
   ![](assets/preferences.png)
* 然後按一下您電子郵件地址下方顯示的語言
* 選擇您偏好的語言，然後按一下 **「儲存」**。您可以選取第二種語言，以在您使用的元件未以您的預設語言在地化時使用。
   ![](assets/select-language.png)

## 搜尋{#unified-search}

在 Adobe Journey Optimizer 介面的任意處，利用頂端列中央的 Unified Adobe Experience Cloud 搜尋功能，在您的沙盒尋找資產、歷程、資料集等等。 

開始輸入內容以顯示排名最前的結果。有關輸入關鍵字的說明文章也會顯示在結果中。

![](assets/unified-search.png)

請按下 **Enter** 以存取所有結果，並按業務對象進行篩選。

![](assets/search-and-filter.png)

## 篩選清單{#filter-lists}

在大多數清單中，搜尋列可讓您搜尋特定項目並選取篩選條件。

按一下清單左上方的篩選圖示，即可存取篩選器 。篩選功能表可讓您根據不同的條件篩選顯示的元素。您可以選擇僅顯示某一類型或狀態的元素、您建立的元素，或者在過去 30 天內修改的元素。選項會因內容而異。

在歷程清單中，您可以從&#x200B;**[!UICONTROL 狀態及版本篩選器]**&#x200B;中根據歷程的狀態、類型與版本來篩選歷程。 類型可以是： **[!UICONTROL 單一事件]**、**[!UICONTROL 區段資格]**、**[!UICONTROL 讀取區段]**、**[!UICONTROL 企業活動]**&#x200B;或 **[!UICONTROL 突發事件]**。您可以選擇僅顯示使用&#x200B;**[!UICONTROL 事件篩選器]**&#x200B;與&#x200B;**[!UICONTROL 資料篩選器]**&#x200B;中的特定事件、欄位群組或動作的歷程。**[!UICONTROL 出版物篩選器]**&#x200B;可讓您選擇出版物日期或使用者。 舉例來說，您可以選擇只顯示昨天發佈之即時歷程的最新版本。[了解更多](../building-journeys/using-the-journey-designer.md)。

>[!NOTE]
>
>請注意，顯示的欄可使用清單右上角的設定按鈕進行個人化。系統會為每位使用者儲存個人化設定。

使用&#x200B;**[!UICONTROL 上次更新]**&#x200B;及&#x200B;**[!UICONTROL 最後更新者]**&#x200B;欄來檢查您的歷程上次更新發生的時間以及儲存者。

![](assets/filter-journeys.png)

在事件、資料來源和動作設定窗格中，**[!UICONTROL 使用位置]**&#x200B;欄位會顯示使用該特定事件、欄位群組或操作的歷程次數。您可以按一下&#x200B;**[!UICONTROL 檢視歷程]**&#x200B;按鈕以顯示對應歷程的清單。

![](assets/journey3bis.png)

您可以對清單的每一元素執行基本動作。例如，您可以複製或刪除項目。

![](assets/journey4.png)
