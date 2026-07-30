---
solution: Journey Optimizer
product: journey optimizer
title: AI助理中的Content Credentials
description: 瞭解Adobe Journey Optimizer如何將Content Credentials自動套用至使用AI助理產生或編輯的影像，以及這對於您的內容有何意義。
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
hide: true
source-git-commit: 556502a5c45ad920827785a9950bc5f7bbc4ca8f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# AI助理中的Content Credentials {#generative-content-credentials}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解哪些AI助理動作會附加Content Credentials、這對於結合數個產生式AI來源的影像來說意味著什麼，以及當您的內容在應用程式之間移動時將會發生什麼情況。

>[!ENDSHADEBOX]

>[!INFO]
>
>圍繞創作AI透明度的新法律不斷湧現，Adobe正在努力滿足各個司法轄區的適用要求。 Content Credentials是Adobe用來符合這些法律要求的來源工具。

Content Credentials是長效的隱藏中繼資料，可記錄內容的建立或編輯方式。 當您在Adobe Journey Optimizer中使用AI助理產生或編輯具有產生式AI工具的影像時，Content Credentials會自動附加至該影像，您不需要採取任何動作。

## 附加Content Credentials的動作 {#cc-workflows}

下表總結了根據AI助理中執行的影像動作附加Content Credentials的時間。

| 動作 | 說明 | 已附加Content Credentials？ | 使用案例範例 |
| --- | --- | --- | --- |
| **產生影像** | 從文字提示、參照影像建立新影像，或產生類似影像 | 一律。 影像是由創作型AI所產生，因此一律會使用全新的Content Credential。 | 電子郵件促銷活動的橫幅影像是從描述所需視覺效果的文字提示中產生。 |
| **裁切影像** （中央或智慧型裁切） | 將影像調整至要求的尺寸 | 僅當來源影像已具有Content Credential時。 裁切會重新建立影像的畫素，這通常會擦除該Content Credential，因此AI Assistant會在裁切之前從來源影像讀取該畫素，然後重新建置並將其重新附加到裁切的結果。 裁切本身不會新增新產生的AI動作，而是保留現有的AI動作。 | 產生的橫幅影像會裁切成適合網頁：Content Credential會透過裁切保留。</br> 用作推播通知背景的已上傳庫存像片會裁切以符合熒幕：由於庫存像片不包含產生式AI動作，因此不會建立任何Content Credential。 |
| **新增文字覆蓋** | 在背景影像上演算產生的文字 | 只有在背景影像已具有Content Credential時。 演算覆蓋圖時，會從背景加上文字產生新影像，而文字通常會清除Content Credential，因此AI Assistant會預先從背景影像讀取該影像，然後重新建置影像，並將其重新附加至結果。 覆蓋步驟不會新增新產生的AI動作。 | 促銷標題會在登陸頁面產生的背景影像上呈現為文字重疊：背景影像中的Content Credential會保留。 |
| **覆蓋影像** | 將兩個或多個影像複合在一起 | 如果任何來源影像有Content Credential，則合併的影像會包含所有來源影像，並合併至單一Content Credential中。 合成作業會從來源產生新影像，這通常會清除這些Content Credentials，因此AI助理會在合成作業前讀取每個影像，然後建立單一合併Content Credential，列出有助於產生式AI動作的每個來源。 | 產生的產品影像與為電子郵件標題產生的背景合成：結果包含反映兩個產生AI來源的Content Credential。<br> 將兩張上傳的品牌像片合成一個拼貼：由於兩個來源都沒有產生式AI動作，因此不會建立任何Content Credential。 |

## 內容型別及其範圍 {#cc-content-types}

* **影像**：已涵蓋。 當影像使用產生式AI產生時，會附加Content Credentials，並透過由AI助理執行的裁切、文字覆蓋和影像覆蓋作業來保留。
* **文字**：不適用。 AI助理的純文字輸出（例如產生副本、翻譯和品牌對齊建議）不需要Content Credentials。

## 內容移動時發生什麼事 {#cc-content-moves}

Content Credentials會隨影像檔案移動。 從Adobe Journey Optimizer下載或匯出使用產生AI產生或編輯的影像時，會保留其Content Credentials。 [進一步瞭解Content Credentials](https://helpx.adobe.com/firefly/using/content-credentials.html){target="_blank"}。

將影像帶入內容的某些方法(例如從PDF或內嵌(base64)來源擷取影像)可能無法保留原始Content Credential。 在這些情況下，無法從來源讀取任何Content Credential，也不會針對結果建立任何專案。

## 其他資源

* [Adobe Content Credentials](https://helpx.adobe.com/firefly/using/content-credentials.html){target="_blank"}：進一步瞭解Content Credentials如何跨Adobe產品運作。
* [Adobe Experience Cloud Generative AI使用者指南](https://www.adobe.com/tw/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [護欄與限制](gs-generative.md#generative-guardrails)
