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
source-git-commit: 962dbbb070bbfe944e174bc330659599a1101ebe
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 10%

---

# 開始使用個人化編輯器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="關於個人化編輯器"
>abstract="個人化編輯器可讓您選取、排列、自訂和驗證所有資料，打造個人化的專屬內容。"

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="自動完成"
>abstract="切換此選項可讓系統在您輸入運算式時自動完成程式碼並提出建議。 此選項僅適用於HTML和文字格式。"

個人化編輯器是[!DNL Journey Optimizer]中個人化的核心。 它可用於您需要定義個人化的每個內容，例如電子郵件、推播和選件。

在個人化編輯器介面中，您將選取、排列、自訂及驗證所有資料，為您的內容建立自訂個人化。

![](assets/perso_ee1.png)

## 可用的個人化來源 {#sources}

畫面左側會顯示網域選擇器，讓您選取個人化的來源。 可用的來源包括：

* **[!UICONTROL 設定檔屬性]** ：列出與[Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}中說明的設定檔結構描述相關的所有參考。
* **[!UICONTROL 對象]** ：列出在Adobe Experience Platform細分服務中建立的所有對象。 [此處](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hant){target="_blank"}提供分段的相關詳細資訊。
* **[!UICONTROL 優惠決定]** ：列出與特定位置相關聯的所有優惠。 選取版位，然後將優惠方案插入內容中。 如需有關如何管理優惠方案的完整檔案，請參閱[本節](../offers/get-started/starting-offer-decisioning.md)。
* **[!UICONTROL 內容屬性]** ：當歷程或行銷活動中使用管道動作活動（電子郵件、推播、簡訊）時，與事件和屬性相關的內容屬性可用於個人化。 在[此區段](personalization-use-case.md)中呈現了運用內容屬性的個人化範例。
* **[!UICONTROL 輔助函式]** ：列出所有輔助函式，可用於對資料執行操作，例如計算、資料格式或轉換、條件，以及在個人化內容中操作這些函式。 請參閱[此章節](functions/functions.md)深入瞭解。

## 新增個人化屬性 {#add}

按一下+按鈕，將屬性新增至個人化運算式。

「+」圖示旁的省略符號選單可讓您取得每個變數的詳細資訊，並將您最常使用的屬性新增至我的最愛。 [瞭解如何新增屬性至我的最愛](personalization-favorites.md)

>[!NOTE]
>
>如果您使用使用構成工作流程產生的擴充屬性來鎖定對象，您可以運用這些擴充屬性來個人化您的訊息。 [瞭解如何使用對象擴充屬性](../audience/about-audiences.md#enrichment)

此外，您可以定義預設後援文字，當字串型別的設定檔屬性為空白時將會顯示。 若要這麼做，請按一下屬性旁的省略符號按鈕，然後選取&#x200B;**[!UICONTROL 插入後援文字]**。 如果設定檔的屬性值是空的，則寫入預設應顯示的文字，然後按一下&#x200B;**[!UICONTROL 新增]**。

![](assets/attribute-details.png)

在下列範例中，個人化編輯器可讓您選取今天生日的設定檔，然後插入與今天對應的特定選件來完成自訂。

![](assets/perso_ee2.png)

一旦您的個人化運算式準備就緒，就需要由個人化編輯器驗證。 請參閱[此章節](personalization-validation.md)深入瞭解。
