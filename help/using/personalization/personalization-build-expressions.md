---
solution: Journey Optimizer
product: journey optimizer
title: 關於運算式編輯器
description: 瞭解如何使用表達式編輯器。
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

# 開始使用表達式編輯器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="關於運算式編輯器"
>abstract="運算式編輯器可讓您選取、排列、自訂和驗證所有資料，打造個人化的專屬內容。"

表達式編輯器是中個性化的核心 [!DNL Journey Optimizer]。 它適用於您需要定義個性化的每個上下文，如電子郵件、推送和提供。

在表達式編輯器介面中，您將選擇、排列、自定義和驗證所有資料，以便為您的內容建立自定義個性化。

![](assets/perso_ee1.png)

## 可用的個性化源 {#sources}

螢幕的左側部分顯示一個域選擇器，用於選擇個性化的源。 可用源包括：

* **[!UICONTROL 配置檔案屬性]** :列出與中所述的配置檔案架構關聯的所有引用 [Adobe Experience Platform資料模型(XDM)文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}。
* **[!UICONTROL 段成員資格]** :列出了在Adobe Experience Platform分割服務中建立的所有段。 有關分段的詳細資訊 [這裡](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}。
* **[!UICONTROL 提供決策]** :列出與特定位置關聯的所有優惠。 選擇位置，然後在內容中插入聘用。 有關如何管理優惠的完整文檔，請參閱 [此部分](../offers/get-started/starting-offer-decisioning.md)。
* **[!UICONTROL 上下文屬性]** :在行程中使用渠道活動（電子郵件、推送、SMS）時，上下文行程欄位可通過此菜單使用。 請參閱[此章節](personalization-use-case.md)深入瞭解。
* **[!UICONTROL 幫助程式函式]** :列出可用於對資料執行操作（如計算、資料格式化或轉換、條件）的所有幫助程式函式，並在個性化的上下文中對它們進行操作。 請參閱[此章節](functions/functions.md)深入瞭解。

## 添加個性化屬性 {#add}

按一下+按鈕，將屬性添加到個性化表達式中。

「+」表徵圖旁邊的省略號菜單允許您獲取每個變數的詳細資訊，並將最常用的屬性添加到收藏夾。 [瞭解如何將屬性添加到收藏夾](personalization-favorites.md)

此外，您還可以定義預設回退文本，如果字串類型配置檔案屬性為空，則該文本將顯示。 要執行此操作，請按一下屬性旁邊的省略號按鈕並選擇 **[!UICONTROL 插入時帶回退文本]**。 如果配置檔案的屬性值為空，則寫入預設情況下應顯示的文本，然後按一下 **[!UICONTROL 添加]**。

![](assets/attribute-details.png)

在以下示例中，表達式編輯器允許您選擇今天有生日的配置檔案，然後通過插入與當天對應的特定優惠來完成自定義。

![](assets/perso_ee2.png)

個性化表達式準備好後，您需要通過表達式編輯器驗證它。 請參閱[此章節](personalization-validation.md)深入瞭解。
