---
title: 在 Journey Optimizer 中個人化內容
description: 開始使用個人化
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 244f05998098bf1770d5f33c955f09688f58ffe7
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 11%

---

# 開始個性化{#add-personalization}

發現 [!DNL Adobe Journey Optimizer] 個性化功能，通過利用您擁有的有關郵件的資料和資訊，將郵件調整為每個特定收件人。 它可以是他們的名字、興趣、居住地、購買的東西，等等。

➡️ [瞭解如何個性化這些視頻中的郵件](#video-perso)

[!DNL Journey Optimizer] 使用 **內** 基於Handlebar的簡單個性化語法，允許您建立包含雙大括弧的內容的表達式 **{{}}**。 您可以在相同的內容或欄位中新增多個運算式，不受限制。 瞭解詳情 [個性化語法](personalization-syntax.md)。

根據由 Adobe Experience Platform 定義的 **XDM 個人設定檔**&#x200B;方案管理的設定檔資料進行個人化。 瞭解詳情 [Adobe Experience Platform資料模型(XDM)文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

>[!CAUTION]
>的 **XDM個人配置檔案** 架構是唯一可用於個性化內容的架構 [!DNL Journey Optimizer]。

**範例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

在處理郵件（電子郵件和推送）時，Journey Optimizer用Experience Cloud平台資料庫中包含的資料替換表達式：  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 變成&quot;你好，無名氏&quot;


## 個性化上下文{#personalization-areas}

通過 [!DNL Journey Optimizer] 可以通過多種不同的方式實現個性化。

在每個帶有編輯器表徵圖的欄位中，都可以開啟個性化編輯器（也稱為表達式編輯器）並定義個性化。

![](assets/perso_icon.png)

### 個性化您的電子郵件

建立電子郵件時，可以在 **[!UICONTROL Subject line]** 的子菜單。

![](assets/perso_subject.png)

在電子郵件設計器中，您可以個性化內容：

* 在 **消息**:在文本塊內按一下，按一下 **個性化** 表徵圖，然後選擇 **插入個性化** 的子菜單。 有關電子郵件設計器介面的詳細資訊，請參閱 [節](../design-emails.md)。

   ![](assets/perso_insert.png)

* 對於 **連結**:在文本塊中選擇一些文本或影像，按一下 **插入連結** 表徵圖。 在窗口中，可以通過按一下 **添加個性化** 表徵圖

   ![](assets/perso_link.png)

在這兩種情況下，都可以訪問個性化編輯器。

![](assets/perso_ee.png)

### 個性化推送通知

您還可以個性化 **推送通知** 的子菜單。

* **標題**
* **身體**
* **自定義聲音**
* **徽章**
* **自訂資料**

![](assets/perso_push.png)

瞭解有關中推送通知配置的詳細資訊 [此部分](../push-gs.md)。

### 個性化您的產品 {#personalize-offers}

在將文本類型內容添加到優惠的表示形式時，您還可以訪問個性化編輯器。

瞭解有關使用決策管理管理內容的更多資訊 [此部分](../offers/offer-library/creating-personalized-offers.md#custom-text)。

## 使用表達式編輯器 {#use-expression-editor}

表達式編輯器是個性化的核心 [!DNL Journey Optimizer]。

它適用於您需要定義個性化的每個上下文，如電子郵件、推送和提供。

在表達式編輯器介面中，您將選擇、排列、自定義和驗證所有資料，以便為您的內容建立自定義個性化。

![](assets/perso_ee1.png)

螢幕的左側部分顯示一個域選擇器，用於選擇個性化的源。

![](assets/perso_ee3.png)

可用源包括：

* **[!UICONTROL Profile attributes]** :列出與中所述的配置檔案架構關聯的所有引用 [Adobe Experience Platform資料模型(XDM)文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Segment memberships]** :列出在Adobe Experience Platform分段服務中建立的所有段。 有關分段的詳細資訊 [這裡](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Offer decisions]** :列出與特定位置關聯的所有優惠。 選擇位置，然後在內容中插入聘用。 有關如何管理優惠的完整文檔，請參閱 [此部分](../deliver-personalized-offers.md)。
* **[!UICONTROL Contextual attributes]** :當 **消息** 在行程中使用，上下文行程欄位可通過此菜單使用。 瞭解詳情 [此部分](personalization-use-case.md)。
* **[!UICONTROL Helper functions]** :列出可用於對資料執行操作（如計算、資料格式化或轉換、條件）的所有幫助程式函式，並在個性化的上下文中對它們進行操作。 瞭解詳情 [此部分](functions/functions.md)。

在選擇時，將在編輯器中添加引用。

>[!NOTE]
>
>「+」表徵圖旁的「資訊」表徵圖開啟工具提示，提供每個變數的詳細資訊。

在以下示例中，表達式編輯器允許您選擇今天有生日的配置檔案，然後通過插入與當天對應的特定優惠來完成自定義。

![](assets/perso_ee2.png)

### 添加到收藏夾{#fav}

將不同的屬性添加到收藏夾菜單可快速訪問您使用頻率最高的項目。 要向收藏夾添加屬性，請按一下橢圓菜單並選擇 **[!UICONTROL Add to favorites]**。

![](assets/favorite-option.png)

要訪問已收藏的項目，請使用 **[!UICONTROL Favorites]** 的子菜單。

![](assets/favorite-menu.png)

從此清單中，您可以快速將個性化對象添加到當前表達式中。

![](assets/favorite-list.png)

如果不想再在收藏夾清單中看到項目，可從收藏夾中刪除。

![](assets/favorite-remove.png)

## 作法影片{#video-perso}

瞭解如何使用歷程中的內容事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

瞭解如何使用歷程中的內容事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
