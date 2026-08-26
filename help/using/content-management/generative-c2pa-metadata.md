---
solution: Journey Optimizer
product: journey optimizer
title: AI助理中的C2PA中繼資料
description: 瞭解Adobe Journey Optimizer如何將C2PA中繼資料自動套用至使用AI Assistant產生或編輯的影像，以及這對於您的內容有何意義。
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
source-git-commit: cf5370872104972b3e49d544b09ab48858484da6
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# AI助理中的C2PA中繼資料 {#generative-content-credentials}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解哪些AI助理動作附加C2PA中繼資料、這對於結合數個產生式AI來源的影像來說意味著什麼，以及當您的內容在應用程式之間移動時將會有什麼影響。

>[!ENDSHADEBOX]

>[!INFO]
>
>圍繞創作AI透明度的新法律不斷湧現，Adobe正在努力滿足各個司法轄區的適用要求。 C2PA中繼資料是Adobe用來符合這些法律要求的來源工具。

C2PA中繼資料是持久且隱藏的中繼資料，會記錄內容的建立或編輯方式。 當您在Adobe Journey Optimizer中使用AI助理產生或編輯具有產生式AI工具的影像時，C2PA中繼資料會自動附加至該影像，您不需要採取任何動作。

## 附加C2PA中繼資料的動作 {#cc-workflows}

下表總結了根據AI助理中執行的影像動作，附加C2PA中繼資料的時間。

| 動作 | 說明 | 要附加C2PA中繼資料嗎？ | 使用案例範例 |
| --- | --- | --- | --- |
| **產生影像** | 從文字提示、參照影像建立新影像，或產生類似影像 | 一律。 影像是由產生式AI產生，因此一律會攜帶最新的C2PA中繼資料。 | 電子郵件促銷活動的橫幅影像是從描述所需視覺效果的文字提示中產生。 |
| **裁切影像** （中央或智慧型裁切） | 將影像調整至要求的尺寸 | 僅當來源影像已具有C2PA中繼資料時。 裁切會重新建立影像的畫素，通常會擦除C2PA中繼資料，因此AI Assistant會在裁切前從來源影像讀取該畫素，然後重新建置該畫素，並將其重新附加至裁切的結果。 裁切本身不會新增新產生的AI動作，而是保留現有的AI動作。 | 產生的橫幅影像會裁切成適合網頁：透過裁切會保留C2PA中繼資料。</br> 用作推播通知背景的上傳庫存像片會被裁切以適合熒幕：由於庫存像片不執行產生式AI動作，因此不會建立任何C2PA中繼資料。 |
| **新增文字覆蓋** | 在背景影像上演算產生的文字 | 只有在背景影像已有C2PA中繼資料時。 演算覆蓋圖時，會從背景加上文字產生新影像，這通常會清除該C2PA中繼資料，因此AI Assistant會預先從背景影像讀取，然後重新建置並重新附加至結果。 覆蓋步驟不會新增新產生的AI動作。 | 促銷標題會在登陸頁面產生的背景影像上呈現為文字重疊：背景影像的C2PA中繼資料會保留。 |
| **覆蓋影像** | 將兩個或多個影像複合在一起 | 如果任何來源影像有C2PA中繼資料，則合併的影像會攜帶所有這些，並合併到單一C2PA中繼資料中。 合成作業會從來源產生新影像，這通常會清除那些C2PA中繼資料，因此AI助理會在合成作業前讀取每個中繼資料，然後建立單一合併的C2PA中繼資料，列出貢獻產生AI動作的每個來源。 | 產生的產品影像與為電子郵件標題產生的背景合成：結果包含反映兩個產生AI來源的C2PA中繼資料。<br> 將兩張上傳的品牌像片合成一個拼貼：由於來源皆未執行創作AI動作，因此不會建立任何C2PA中繼資料。 |

## 內容型別及其範圍 {#cc-content-types}

* **影像**：已涵蓋。 使用產生AI產生影像時，會附加C2PA中繼資料，並透過由AI助理執行的裁切、文字覆蓋和影像覆蓋操作來保留。
* **文字**：不適用。 AI助理的純文字輸出，例如產生副本、翻譯和品牌對齊建議，不需要C2PA中繼資料。

## 內容移動時發生什麼事 {#cc-content-moves}

C2PA中繼資料會隨影像檔案移動。 從Adobe Journey Optimizer下載或匯出使用產生AI產生或編輯的影像時，會保留其C2PA中繼資料。 [進一步瞭解C2PA中繼資料](https://helpx.adobe.com/firefly/using/content-credentials.html){target="_blank"}。

將影像帶入內容的某些方法(例如從PDF或內嵌(base64)來源擷取影像)可能不會保留原始C2PA中繼資料。 在這些情況下，無法從來源讀取任何C2PA中繼資料，也無法針對結果建立任何資料。

## 其他資源

* [Adobe Experience Cloud Generative AI使用者指南](https://www.adobe.com/tw/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [護欄與限制](gs-generative.md#generative-guardrails)
* [Generative AI內容透明度](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency#related-links)