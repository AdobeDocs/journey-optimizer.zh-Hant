---
solution: Journey Optimizer
product: journey optimizer
title: 關於個人化編輯器
description: 瞭解如何使用個人化編輯器。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，關於，開始
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: ff6619925a36d2687922d1b631d1cabbcb98167e
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 6%

---

# 開始使用個人化編輯器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="關於個人化編輯器"
>abstract="個人化編輯器可讓您選取、排列、自訂和驗證所有資料，打造個人化的專屬內容。"

個人化編輯器是[!DNL Journey Optimizer]中個人化的核心。 它可用於您需要定義個人化的每個內容，例如電子郵件、推播和選件。

在個人化編輯器介面中，您將選取、排列、自訂及驗證所有資料，為您的內容建立自訂個人化。

![](assets/perso_ee1.png)

## Personalization來源 {#sources}

畫面左側會顯示網域選擇器，讓您選取個人化的來源。 可用的來源包括：

* **[!UICONTROL 設定檔屬性]** ：列出與[Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}中說明的設定檔結構描述相關的所有參考。
* **[!UICONTROL 對象]** ：列出在Adobe Experience Platform細分服務中建立的所有對象。 [此處](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hant){target="_blank"}提供分段的相關詳細資訊。
* **[!UICONTROL 優惠決定]** ：列出與特定位置相關聯的所有優惠。 選取版位，然後將優惠方案插入內容中。 如需有關如何管理優惠方案的完整檔案，請參閱[本節](../offers/get-started/starting-offer-decisioning.md)。
* **[!UICONTROL 內容屬性]** ：當歷程或行銷活動中使用管道動作活動（電子郵件、推播、簡訊）時，與事件和屬性相關的內容屬性可用於個人化。 在[此區段](personalization-use-case.md)中呈現了運用內容屬性的個人化範例。

>[!NOTE]
>
>如果您使用使用構成工作流程產生的擴充屬性來鎖定對象，您可以運用這些擴充屬性來個人化您的訊息。 [瞭解如何使用對象擴充屬性](../audience/about-audiences.md#enrichment)

## 新增個人化 {#add}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="自動完成"
>abstract="切換此選項可讓系統在您輸入時自動建議並完成程式碼。 此功能僅適用於HTML和文字格式，並支援「設定檔」和「內容」屬性。 如果透過切換功能停用，編輯器將提供原生HTML程式碼自動完成。"

中央工作區是您建置個人化語法的位置。 若要使用屬性來個人化您的訊息，請在左側導覽窗格中找出該屬性，然後按一下`+`按鈕，將該屬性加入運算式中。

`+`圖示旁的省略符號功能表可讓您取得每個屬性的詳細資訊，並將您最常用的屬性新增至我的最愛。 新增至我的最愛屬性可從左側導覽窗格中的&#x200B;**[!UICONTROL 我的最愛]**&#x200B;功能表存取。

此外，您可以定義預設後援文字，當字串型別的設定檔屬性為空白時將會顯示。 若要這麼做，請按一下屬性旁的省略符號按鈕，然後選取&#x200B;**[!UICONTROL 插入後援文字]**。 如果設定檔的屬性值是空的，則寫入預設應顯示的文字，然後按一下&#x200B;**[!UICONTROL 新增]**。

![](assets/attribute-details.png)

在下列範例中，個人化編輯器可讓您選取今天生日的設定檔，然後插入與今天對應的特定選件來完成自訂。

![](assets/perso_ee2.png)

## 運算式編輯工具

中央工作區提供各種工具，協助您撰寫個人化運算式。

![](assets/perso-workspace.png)

可選擇下列選項：

1. **[!UICONTROL 尋找]** / **[!UICONTROL 尋找並取代]**：搜尋您的運算式並自動取代部分程式碼。
1. **[!UICONTROL 還原]** / **[!UICONTROL 重做]**：還原/重做上一個操作。
1. **[!UICONTROL 自動完成]**：在您輸入時自動建議並完成程式碼。 此功能僅適用於HTML和文字格式，並支援「設定檔」和「內容」屬性。 如果透過切換功能停用，編輯器將提供原生HTML程式碼自動完成。

   ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"}

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL 文字]**：識別您的程式碼格式。 這可讓系統根據選取的語言調整驗證及自動完成功能。
1. **[!UICONTROL 驗證]**：檢查運算式的語法。 請參閱[此章節](personalization-validation.md)深入瞭解。
1. **[!UICONTROL 另存為片段]**：將運算式另存為運算式片段。 請參閱[本節](../content-management/save-fragments.md#save-as-expression-fragment)以進一步瞭解
1. **[!UICONTROL 字型大小]**：調整編輯器內內容的字型大小，以提高可讀性。
1. **[!UICONTROL 自動換行]**：啟用或停用自動換行，允許長運算式顯示在單行或包含在編輯器中。 選項包括：
   * **關閉** （預設） — 無自動換行。 長線超出編輯器檢視範圍，需要水準捲動。
   * **On** — 以編輯器的寬度換行。
   * **自動換行** — 當行字元達到80個字元時換行。
   * **已繫結** — 以編輯器寬度或80個字元（以較小者為準）來換行。

在導覽窗格中，有其他功能可協助您建置個人化運算式。

![](assets/perso-features.png)

* **[!UICONTROL 輔助函式]** — 輔助函式可讓您對資料執行操作，例如計算、資料格式或轉換、條件，並在個人化的內容中操作它們。 [進一步瞭解可用的協助程式功能](functions/functions.md)

* **[!UICONTROL 我的最愛]** — 您新增至我的最愛屬性會顯示在此清單中。 這可讓您快速存取您使用頻率最高的專案。 若要新增屬性至您的最愛，請按一下省略符號選單，然後選擇&#x200B;**[!UICONTROL 新增至我的最愛]**。

* **[!UICONTROL 條件]** — 運用在程式庫中建立的條件式規則，將動態內容新增至您的訊息。 這可讓您根據條件建立訊息的多個變體。 [瞭解如何建立動態內容](../personalization/get-started-dynamic-content.md)

* **[!UICONTROL 片段]** — 運用已建立或儲存至目前沙箱的運算式片段。 片段是可重複使用的元件，可跨[!DNL Journey Optimizer]個行銷活動和歷程參照。 此功能允許預先建置多個自訂內容區塊，可供行銷使用者在改良的設計流程中快速組合內容。 [瞭解如何使用運算式片段進行個人化](../personalization/use-expression-fragments.md)

一旦您的個人化運算式準備就緒，就需要由個人化編輯器驗證。 請參閱[此章節](personalization-validation.md)深入瞭解。
