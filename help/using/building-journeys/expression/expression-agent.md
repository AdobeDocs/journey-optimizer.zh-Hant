---
solution: Journey Optimizer
product: journey optimizer
title: 使用運算式助理來產生運算式
description: 瞭解如何使用Adobe Journey Optimizer中的運算式輔助程式，透過自然語言提示直接在Journey進階運算式編輯器中產生運算式。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="公開測試版" type="Informative"
mini-toc-levels: 2
feature_v2: []
subfeature_v2: []
source-git-commit: 9551133fab06cfa5e056ba98da73dcbf066916fc
workflow-type: tm+mt
source-wordcount: 1090
ht-degree: 2%

---


# 使用運算式助理來產生運算式 {#expression-agent}

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**公開測試版**&#x200B;中。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](../../rn/releases.md)。
>
>在使用Expression Assistant之前，請先閱讀適用於Journey Optimizer中產生AI功能的相關[護欄和限制](../../content-management/gs-generative.md#generative-guardrails)。

Expression Assistant是AI支援的功能，內建在Journey進階運算式編輯器中。 它可幫助您從純語言提示產生有效的運算式。

在歷程&#x200B;**[!UICONTROL 進階運算式編輯器]**&#x200B;開啟的任何位置，都可以使用它。 例如，當您在&#x200B;**[最佳化活動](../optimize.md)**&#x200B;中設定條件和路由，或當您設定使用自訂日期的[**[!UICONTROL 等待&#x200B;]**&#x200B;活動](../wait-activity.md)，而您需要`dateTimeOnly`運算式時。

## 產生運算式 {#generate}

若要使用「運算式輔助程式」產生運算式：

1. 在您的歷程中開啟&#x200B;**[!UICONTROL 進階運算式編輯器]**，例如從分支條件、**[!UICONTROL 最佳化]**&#x200B;活動或具有自訂日期的&#x200B;**[!UICONTROL 等待]**&#x200B;活動。

   ![](../assets/expression-assistant-pane.png)

1. 在文字欄位中，以純文字描述您要產生的運算式。 例如:

   * *&quot;來自美國的使用者年齡超過18歲&quot;*
   * *「過去30天內購買過的客戶」*

   請參閱此頁面結尾的[範例提示](#example-prompts)以取得想法。

1. 按一下&#x200B;**[!UICONTROL 產生]**&#x200B;提交您的提示。

   助理開始產生對應的運算式，並在產生過程中顯示進度狀態訊息。

   >[!NOTE]
   >
   >如果助理無法產生有效的運算式（例如，如果您的提示參考可用資料來源中不存在的欄位），便會出現錯誤訊息。 發生此情況時，請修訂您的提示，使用歷程設定中可用的欄位名稱和資料來源，然後再次產生。

1. 一旦運算式準備就緒，便可在面板中檢閱結果。

   ![](../assets/expression-assistant-result.png)

   * 在套用之前，請按一下![預覽圖示](../assets/do-not-localize/generation-preview.svg)圖示，以檢閱您要求的案例的助理輸出。

   * 按一下&#x200B;**[!UICONTROL 套用]**，將產生的運算式直接插入進階運算式編輯器中（與您手動貼入的位置相同）。
   * 使用複製控制項來抓取建議的運算式文字，並視需要將其貼到其他位置。

## 提示範例 {#example-prompts}

以下清單僅為提示性想法。 它們不會顯示產生的運算式語法，確切的輸出取決於歷程中定義的欄位和活動。

### 歷程事件和自訂動作 {#example-prompts-event-action}

* 訂單總價超過100的&#x200B;**
* *「過去7天內建立訂單的事件」*
* *&quot;事件型別為商務購買的事件&quot;*
* *&quot;在過去一小時內建立訂單的事件&quot;*
* 訂單總價超過200的&#x200B;*&quot;事件，且動作回應具有狀態代碼&quot;*

### 等待活動運算式 {#example-prompts-datetime}

當&#x200B;**[!UICONTROL 等待]**&#x200B;活動使用自訂日期時，您可以透過在&#x200B;**[!UICONTROL 進階運算式編輯器]**&#x200B;中建置`dateTimeOnly`運算式來定義設定檔何時繼續。 例如，來自設定檔屬性、事件時間戳記、區段資格資料，或計算的目前時間位移。 如需如何設定自訂等待和適用的限制，請參閱[自訂等待](../wait-activity.md#custom)。

* *「僅將客戶的上次訂購日期作為日期時間」*
* *「使用同意電子郵件時間作為僅日期時間」*
* *「將區段會籍上次資格取得時間轉換為僅日期時間」*
* *「等待節點：2024年聖誕節後一週，僅日期時間」*
* *「等待節點：從現在起的30天下午10點，僅日期時間」*
* *&quot;等到UTC時區的今天上午9點，僅傳回為日期時間&quot;*

## 相關資源 {#related}

* [使用進階運算式編輯器](expressionadvanced.md) — 運算式編輯器介面的概覽和支援的語法。
* [開始使用Journey Optimizer中的AI助理](../../content-management/gs-generative.md) — 一般護欄、存取及設定產生式AI功能。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面說明Expression Assistant，這是Journey進階運算式編輯器中AI支援的功能，可從純語言提示產生有效的歷程運算式。

**意圖：**

* 使用運算式助理從自然語言說明產生歷程運算式
* 使用套用按鈕，將產生的運算式直接套用至進階運算式編輯器
* 在最佳化活動、條件活動和自訂日期等待活動中使用運算式助理
* 提供事件型條件和`dateTimeOnly`等待運算式的範例提示
* 修改提示以參考有效欄位名稱和資料來源，以疑難排解失敗的產生

**字彙表：**

* **Expression Assistant**：內嵌於Journey Advanced運算式編輯器中的AI支援產生功能，可將純文字提示轉換為有效的歷程運算式&#x200B;*（產品專用）*
* **進階運算式編輯器**：在條件、等待活動及動作引數對應&#x200B;*（產品特定）*&#x200B;中寫入複雜運算式的Journey Optimizer介面
* **dateTimeOnly**：不含時區的日期 — 時間運算式型別，自訂日期等待活動&#x200B;*（產品特定）*&#x200B;所需
* **最佳化活動**：支援分支條件的歷程活動，可透過進階運算式編輯器&#x200B;*（產品特定）*&#x200B;設定

**護欄：**

* Expression Assistant目前在&#x200B;**公開測試版**&#x200B;中 — 可用性和行為可能會變更
* 主要AI Assistant檔案中的創作AI護欄和限制適用於此功能
* 如果助理參考的欄位未出現在您歷程的資料來源中，則會傳回錯誤 — 請修改提示以使用可用的欄位名稱
* 確切產生的運算式語法取決於特定歷程中設定的欄位和活動

**術語：**

* 正式名稱：運算式助理 — 縮寫：none — 變體：運算式AI、歷程運算式產生器
* 同義字： &quot;Expression Assistant&quot; = &quot;AI運算式產生器&quot;
* 請勿混淆： Expression Assistant （AI支援的產生器）≠進階運算式編輯器（手動程式碼編輯器本身）

**常見問題集：**

* **問：哪裡可以使用Expression Assistant？**  — 可在歷程進階運算式編輯器開啟的任何位置使用，包括條件活動、最佳化活動以及具有自訂日期的等待活動。
* **問：如果助理無法產生有效的運算式會發生什麼情況？**  — 出現錯誤訊息；您應該修訂提示，使用歷程設定中存在的欄位名稱和資料來源。
* **問：如何將產生的運算式插入編輯器？**  — 按一下助理面板中的&#x200B;**套用**&#x200B;按鈕，將它直接插入進階運算式編輯器中目前游標位置。
* **問：運算式助理可以產生`dateTimeOnly`等待活動的運算式嗎？**  — 是；例如，提示「從現在起的30天下午10點僅作為日期時間」會產生適當的`dateTimeOnly`運算式。
* **問：運算式助理一般可用嗎？**  — 否；目前為公開測試版。 請檢視Journey Optimizer發行週期頁面，瞭解可用性更新。

+++
