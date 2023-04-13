---
solution: Journey Optimizer
product: journey optimizer
title: 關於運算式編輯器
description: 了解如何使用運算式編輯器。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表達式，編輯器，關於，開始
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 93e3ed9e1a9a437353b800aee58952b86eab9370
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 12%

---

# 開始使用運算式編輯器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="關於運算式編輯器"
>abstract="運算式編輯器可讓您選取、排列、自訂和驗證所有資料，打造個人化的專屬內容。"

運算式編輯器是 [!DNL Journey Optimizer]. 它適用於您需要定義電子郵件、推送和選件之類個人化的每個內容。

在運算式編輯器介面中，您將選取、排列、自訂及驗證所有資料，以針對您的內容建立自訂個人化。

![](assets/perso_ee1.png)

## 可用的個人化來源 {#sources}

畫面左側會顯示網域選取器，供您選取個人化來源。 可用來源包括：

* **[!UICONTROL 設定檔屬性]** :列出與配置檔案架構相關的所有引用，如 [Adobe Experience Platform Data Model(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.
* **[!UICONTROL 區段成員資格]** :列出在Adobe Experience Platform區段服務中建立的所有區段。 可用區段的詳細資訊 [此處](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.
* **[!UICONTROL 優惠方案決策]** :列出與特定版位相關聯的所有優惠方案。 選取版位，然後在內容中插入優惠方案。 如需如何管理優惠方案的完整檔案，請參閱 [本節](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL 內容屬性]** :在歷程中使用管道動作活動（電子郵件、推播、簡訊）時，您可透過此功能表取得內容歷程欄位。 請參閱[此章節](personalization-use-case.md)深入瞭解。
* **[!UICONTROL 輔助函式]** :列出所有可用於對資料執行操作的輔助功能，如計算、資料格式或轉換、條件，以及在個人化環境中處理這些功能。 請參閱[此章節](functions/functions.md)深入瞭解。

## 新增個人化屬性 {#add}

按一下+按鈕，將屬性新增至您的個人化運算式。

「+」圖示旁的刪節號選單可讓您取得每個變數的詳細資訊，並將您最常使用的屬性新增至我的最愛。 [了解如何將屬性新增至我的最愛](personalization-favorites.md)

此外，您可以定義預設的後援文字，如果字串類型描述檔屬性為空，則會顯示此文字。 要執行此操作，請按一下屬性旁的刪節號按鈕，然後選取 **[!UICONTROL 插入後援文字]**. 如果設定檔的屬性值為空，則撰寫預設應顯示的文字，然後按一下 **[!UICONTROL 新增]**.

![](assets/attribute-details.png)

在下列範例中，運算式編輯器可讓您選取生日為今天的設定檔，然後透過插入與當天相對應的特定選件來完成自訂。

![](assets/perso_ee2.png)

當您的個人化運算式準備就緒後，您必須由運算式編輯器驗證。 請參閱[此章節](personalization-validation.md)深入瞭解。
