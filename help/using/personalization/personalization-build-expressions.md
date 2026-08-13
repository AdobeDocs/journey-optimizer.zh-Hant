---
solution: Journey Optimizer
product: journey optimizer
title: 新增個人化
description: 瞭解如何使用個人化編輯器新增個人化。
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
mini-toc-levels: 1
keywords: 運算式，編輯器，關於，開始
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: e51e8901-97d9-4f7d-a835-503025a90e32
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 2328
ht-degree: 7%

---

# 新增個人化 {#build-personalization-expressions}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用個人化編輯器，從設定檔屬性、對象、優惠決定和內容屬性等來源，新增、自訂及驗證個人化運算式。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="關於個人化編輯器"
>abstract="個人化編輯器可讓您選取、排列、自訂和驗證所有資料，打造個人化的專屬內容。"

個人化編輯器是[!DNL Journey Optimizer]中個人化的核心。 它可用於您需要定義個人化的每個內容，例如電子郵件、推播和選件。

在個人化編輯器介面中，您可以選取、排列、自訂及驗證所有資料，為您的內容建立自訂個人化。

![](assets/perso_ee1.png)

## 我可以在哪裡新增個人化 {#where}

您可以使用![新增個人化圖示](assets/do-not-localize/add-perso-icon.svg)圖示，在每一個欄位的&#x200B;**[!DNL Journey Optimizer]**&#x200B;中新增個人化。 請展開下列各節以取得詳細資訊。

+++訊息

在郵件中，可以在郵件的不同位置新增個人化，例如&#x200B;**[!UICONTROL 主旨列]**&#x200B;欄位。

![](assets/perso_subject.png)

您也可以在內容的其他區段中新增。 例如，對於[推播通知](../push/push-gs.md)，可以在&#x200B;**標題**、**內文**、**自訂聲音**、**徽章**&#x200B;和&#x200B;**自訂資料**&#x200B;欄位中新增個人化。

+++

+++電子郵件設計工具

在[電子郵件Designer](../email/get-started-email-design.md)中編輯電子郵件內容時，您可以使用內容工具列中的圖示，在大部分文字元素中新增個人化。

![](assets/perso_insert.png)

+++

+++URL

Journey Optimizer也可讓您個人化訊息中的&#x200B;**URL**。 個人化 URL 會根據輪廓屬性，將收件者帶往網站特定頁面或個人化微網站。 [了解更多](../email/url-personalization.md)

![](assets/perso-url.png){width="50%"}

>[!NOTE]
>
>URL個人化可用於這些型別的連結： **外部連結**、**取消訂閱連結**&#x200B;和&#x200B;**選擇退出**。

+++

+++電子郵件設定

建立電子郵件通道設定時，您可以定義子網域、標題和URL追蹤引數的個人化值。 [了解更多](../email/surface-personalization.md)

+++

+++產品建議

在您的&#x200B;**優惠方案代表**&#x200B;中使用文字型別內容時，您可以新增個人化。 [瞭解如何建立個人化優惠](../offers/offer-library/creating-personalized-offers.md)

+++

## Personalization來源 {#sources}

導覽窗格可讓您選取個人化的來源。 可用的來源包括：

* **[!UICONTROL 設定檔屬性]** ：列出與[Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}中說明的設定檔結構描述相關的所有參考。
* **[!UICONTROL Target屬性]** ：此資料夾專屬於「協調的行銷活動」。 它包含直接在行銷活動畫布中計算的屬性。 [瞭解如何在協調的行銷活動中新增個人化](../orchestrated/add-personalization.md)
* **[!UICONTROL 對象]** ：列出在Adobe Experience Platform細分服務中建立的所有對象。 在[Adobe Experience Platform Segmentation檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hant){target="_blank"}中進一步瞭解。
* **[!UICONTROL 優惠決定]** ：列出與特定位置相關聯的所有優惠。 選取版位，然後將優惠方案插入內容中。 如需有關如何管理優惠方案的完整檔案，請參閱[本節](../offers/get-started/starting-offer-decisioning.md)。
* **[!UICONTROL 內容屬性]** ：當歷程或行銷活動中使用管道動作活動（電子郵件、推播、簡訊）時，與事件和屬性相關的內容屬性可用於個人化。 在[本節](personalization-use-case.md)中顯示了運用內容屬性的個人化範例。 此外，自訂動作回應可用於個人化。 [瞭解如何在原生管道中使用自訂動作回應](../action/action-response.md#response-in-channels)。

>[!NOTE]
>
>如果您使用使用構成工作流程產生的擴充屬性來鎖定對象，您可以運用這些擴充屬性來個人化您的訊息。 [瞭解如何使用對象擴充屬性](../audience/about-audiences.md#enrichment)

## 新增個人化 {#add}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="自動完成"
>abstract="啟用此選項後，可允許系統在您輸入時自動建議並完成程式碼。 此功能僅適用於 HTML 和文字格式，並支援輪廓和內容屬性。 如果透過切換進行停用，編輯器將提供原生 HTML 程式碼自動完成。"

中央工作區是您建置個人化語法的位置。 若要使用屬性來個人化您的訊息，請在左側導覽窗格中找出該屬性，然後按一下`+`按鈕，將該屬性加入運算式中。

![](assets/personalization-add-attribute.png)

`+`圖示旁的省略符號功能表可讓您取得每個屬性的詳細資訊，並將您最常用的屬性新增至我的最愛。 可透過導覽窗格中的&#x200B;**[!UICONTROL 我的最愛]**&#x200B;功能表存取新增至我的最愛的屬性。

>[!NOTE]
>
>依預設，屬性窗格只會顯示填入的屬性。 若要顯示所有屬性，請選取搜尋欄位上方的![](assets/do-not-localize/settings-icon.svg)按鈕，並關閉&#x200B;**[!UICONTROL 只顯示填入的屬性]**&#x200B;選項。

此外，您可以定義預設後援文字，當字串型別的設定檔屬性為空白時將會顯示。 若要這麼做，請按一下屬性旁的省略符號按鈕，然後選取&#x200B;**[!UICONTROL 插入後援文字]**。 如果設定檔的屬性值是空的，則寫入預設應顯示的文字，然後按一下&#x200B;**[!UICONTROL 新增]**。

![](assets/attribute-details.png)

在下列範例中，個人化編輯器可讓您選取今天生日的設定檔，然後插入與今天對應的特定選件來完成自訂。

![](assets/perso_ee2.png)

## 運算式編輯選項 {#options}

中央工作區提供各種工具，協助您撰寫個人化運算式。

![](assets/perso-workspace.png)

可選擇下列選項：

1. **[!UICONTROL 尋找]** / **[!UICONTROL 尋找並取代]**：搜尋您的運算式並自動取代部分程式碼。
1. **[!UICONTROL 還原]** / **[!UICONTROL 重做]**：還原/重做上一個操作。
1. **[!UICONTROL 自動完成]**：在您輸入時自動建議並完成程式碼。 此功能僅適用於 HTML 和文字格式，並支援輪廓和內容屬性。 如果透過切換進行停用，編輯器將提供原生 HTML 程式碼自動完成。

   ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"}

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL 文字]**：識別您的程式碼格式。 這可讓系統根據選取的語言調整驗證及自動完成功能。
1. **[!UICONTROL 驗證]**：檢查運算式的語法。 請參閱[此章節](../personalization/personalization-build-expressions.md)深入瞭解。
1. **[!UICONTROL 另存為片段]**：將運算式另存為運算式片段。 請參閱[本節](../content-management/save-fragments.md#save-as-expression-fragment)以進一步瞭解
1. **[!UICONTROL 字型大小]**：調整編輯器內內容的字型大小，以提高可讀性。
1. **[!UICONTROL 自動換行]**：啟用或停用自動換行，允許長運算式顯示在單行或包含在編輯器中。 選項包括:
   * **關閉** （預設） — 無自動換行。 長線超出編輯器檢視範圍，需要水準捲動。
   * **On** — 以編輯器的寬度換行。
   * **自動換行** — 當行字元達到80個字元時換行。
   * **已繫結** — 以編輯器寬度或80個字元（以較小者為準）來換行。
1. **[!UICONTROL Picks]**：將屬性顯示為精簡的「Picks」，藉由隱藏長屬性路徑來改善可讀性。 按一下屬性以顯示其完整路徑。

   >[!NOTE]
   >
   >此選項僅適用於設定檔屬性、內容屬性和動態媒體。

在導覽窗格中，有其他功能可協助您建置個人化運算式。

![](assets/perso-features.png)

* **[!UICONTROL 輔助函式]** — 輔助函式可讓您對資料執行操作，例如計算、資料格式或轉換、條件，並在個人化的內容中操作它們。 [進一步瞭解可用的協助程式功能](functions/functions.md)

* **[!UICONTROL 我的最愛]** — 您新增至我的最愛屬性會顯示在此清單中。 這可讓您快速存取您使用頻率最高的專案。 若要新增屬性至您的最愛，請按一下省略符號選單，然後選擇&#x200B;**[!UICONTROL 新增至我的最愛]**。

* **[!UICONTROL 條件]** — 運用在程式庫中建立的條件式規則，將動態內容新增至您的訊息。 這可讓您根據條件建立訊息的多個變體。 [瞭解如何建立動態內容](../personalization/get-started-dynamic-content.md)

* **[!UICONTROL 片段]** — 運用已建立或儲存至目前沙箱的運算式片段。 片段是可重複使用的元件，可跨[!DNL Journey Optimizer]個行銷活動和歷程參照。 此功能允許預先建置多個自訂內容區塊，可供行銷使用者在改良的設計流程中快速組合內容。 [瞭解如何使用運算式片段進行個人化](../personalization/use-expression-fragments.md)

>[!TIP]
>
>在尋找現成的運算式嗎？ **[Personalization訣竅](personalization-recipes.md)**&#x200B;頁面針對最常見的使用案例提供複製貼上模式：日期格式、倒數計時器、條件式遞補、僅限時間顯示等。

一旦您的個人化運算式準備就緒，就需要由個人化編輯器驗證。 請參閱[此章節](../personalization/personalization-build-expressions.md)深入瞭解。

## 驗證機制 {#validation-mechanisms}

當您按一下&#x200B;**新增**&#x200B;按鈕以關閉編輯器視窗時，會自動執行運算式的驗證。 您也可以使用&#x200B;**驗證**&#x200B;按鈕來檢查您的個人化語法。

![](assets/perso_validation1.png)

展開以下區段以檢視驗證個人化時可能發生的常見錯誤。

+++常見錯誤

* **找不到「XYZ」路徑**

嘗試參照結構描述中未定義的欄位時。

在此情況下，**firstName1**&#x200B;未定義為設定檔結構描述中的屬性：

```
{{profile.person.name.firstName1}}
```

* **變數&quot;XYZ&quot;的型別不相符。 必須是陣列。 找到字串。**

嘗試對字串而非陣列重複時。

在此情況下，**product**&#x200B;不是陣列：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **無效的Handlebars語法。 找到`'[XYZ}}'`**

使用無效的Handlebars語法時。

Handlebars運算式周圍有&#x200B;**{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **無效的區段定義**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

+++

若是選件，可能會發生特定錯誤。 展開下列區段以取得詳細資訊：

+++ 與優惠方案相關的特定錯誤

與電子郵件或推播訊息中的優惠方案整合相關的錯誤具有以下模式：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

驗證會在個人化編輯器中的個人化內容驗證期間執行。

<table> 
 <thead> 
  <tr> 
   <th> 錯誤標題<br /> </th> 
   <th> 驗證/解析度<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>找不到id placementID和型別OfferPlacement的資源 <br/>
找不到id activityID和型別OfferActivity的資源<br/></td> 
   <td>檢查ActivityID和/或PlacementID是否可用</td> 
  </tr> 
   <tr> 
   <td>無法驗證資源。</td> 
   <td>位置中的componentType應符合offerType選件</td> 
  </tr> 
   <tr> 
   <td>offerId中未出現公用URL。</td> 
   <td>影像選件（與決定和位置配對相關的所有個人化和遞補）應填入公用URL （deliveryURL不應空白）。</td> 
  </tr> 
  <tr> 
   <td>決定包含非設定檔屬性。</td> 
   <td>選件模型使用方式應僅包含設定檔屬性。</td> 
  </tr> 
  <tr> 
   <td>擷取決策使用方式時發生錯誤。</td> 
   <td>當API嘗試擷取選件模型時，可能會發生此錯誤。</td> 
  </tr>
  <tr> 
   <td>優惠屬性offer-attribute無效。</td> 
   <td>檢查優惠方案drp中參照的優惠方案屬性是否有效。 以下是有效的屬性： <br/>
影像：deliveryURL、linkURL<br/>
文字：內容<br/>
HTML：內容<br/></td> 
  </tr> 
 </tbody> 
</table>

+++

## 快速參考 {#quick-reference}

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

>[!BEGINTABS]

>[!TAB 概觀]

**TL；DR**

此頁面說明如何使用Journey Optimizer個人化編輯器，從來源（包括設定檔屬性、對象、優惠決定和內容屬性）選取、建立、自訂及驗證個人化運算式。

**個意圖**

* 瞭解可在Journey Optimizer中新增個人化的位置（訊息、電子郵件Designer、URL、電子郵件設定、選件）
* 為運算式選取適當的個人化來源
* 在編輯器工作區中新增屬性和建置運算式
* 使用編輯器工具：尋找/取代、自動完成、驗證、Pills、儲存為片段
* 使用導覽窗格功能：協助程式功能、我的最愛、條件、片段
* 驗證運算式並解決常見錯誤

>[!TAB 字彙]

* **Personalization編輯器**： Journey Optimizer中用於建立、自訂及驗證個人化運算式的中央UI工具；可在可定義個人化的任何地方使用。 *（產品特定）*
* **Personalization來源**：可用於建立運算式的資料類別 — 設定檔屬性、目標屬性、對象、優惠決定和內容屬性。
* **內容屬性**：歷程或行銷活動的特定資料（事件、屬性、自訂動作回應），只有在歷程或行銷活動中使用管道動作時才能用於個人化。 *（產品特定）*
* **Pills**：個人化編輯器顯示模式，會將長屬性路徑呈現為精簡的可點按權杖，以改善可讀性。 僅適用於設定檔屬性、內容屬性和動態媒體。 *（產品特定）*
* **自動完成**：一種編輯器功能，可在您輸入時自動建議並完成程式碼；僅適用於HTML和文字格式，僅支援「設定檔」和「內容」屬性。 *（產品特定）*
* **運算式片段**：可在行銷活動和歷程間參考的可重複使用的個人化運算式元件。 *（產品特定）*
* **遞補文字**：當指定設定檔的字串型別設定檔屬性為空白時顯示的預設字串；透過「插入遞補文字」為每個屬性設定。

>[!TAB 術語]

* **正式名稱：**&#x200B;個人化編輯器
* **請勿混淆：** Personalization編輯器（用來建置訊息、電子郵件、推播通知和選件中的內容運算式 — 支援Handlebars和PQL語法）≠進階運算式編輯器（用於歷程中的資料來源和事件資訊、自訂等待活動及動作引數對應條件 — 提供不同於個人化編輯器的內建函式和運運算元）
* **請勿混淆：**&#x200B;設定檔屬性（以XDM結構描述為基礎，可用於所有內容）≠內容屬性（歷程/行銷活動專用，僅可用於該內容）≠Target屬性（僅限協調的行銷活動）
* **請勿混淆：**&#x200B;自動完成HTML/文字（建議個人化屬性完成）≠原生HTML程式碼自動完成（停用切換時的編輯器預設值）

>[!TAB 護欄與限制]

* 自動完成僅適用於HTML和文字格式；它僅支援「設定檔」和「內容」屬性。
* 「藥丸」顯示模式僅適用於設定檔屬性、內容屬性和動態媒體。
* URL個人化僅適用於外部連結、取消訂閱連結和選擇退出連結型別。
* 依預設，屬性窗格只會顯示填入的屬性；將「只顯示填入的屬性」切換為顯示所有的結構描述屬性。
* 優惠模型使用方式必須僅包含設定檔屬性；決定中的非設定檔屬性會導致驗證錯誤。

>[!TAB 常見問題集]

**問：可以在Journey Optimizer的哪裡新增個人化？**

在任何具有新增個人化圖示的欄位中 — 包括電子郵件主旨列、推播通知欄位（標題、內文、自訂音效、徽章、自訂資料）、電子郵件Designer文字元素、URL （外部連結、取消訂閱連結、選擇退出）、電子郵件設定子網域/標題/URL追蹤引數，以及選件文字型別的表示方式。

**問：可用的個人化來源有哪些？**

設定檔屬性、目標屬性（僅限協調的行銷活動）、對象、優惠決定和內容屬性（歷程/行銷活動事件和自訂動作回應）。

**問：如何驗證運算式？**

當您按一下「新增」以關閉編輯器時，驗證會自動執行。 您也可以使用「驗證」按鈕手動觸發。 常見錯誤包括：找不到路徑（不在結構描述中的欄位）、型別不相符（將字串迭代為陣列）、無效的Handlebars語法以及無效的區段定義。

**問：丸子選項有什麼作用？**

它會將長屬性路徑呈現為精簡的可點按權杖，以便在編輯器中更容易閱讀。 僅適用於設定檔屬性、內容屬性和動態媒體。

**問：為什麼我只在屬性窗格中看到某些屬性？**

依預設，窗格只會顯示填入的屬性。 選取搜尋欄位上方的設定圖示，然後關閉「僅顯示填入的屬性」以顯示所有結構描述屬性。

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 54973b31 -->
