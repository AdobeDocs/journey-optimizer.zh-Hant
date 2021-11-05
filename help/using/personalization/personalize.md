---
title: 在 Journey Optimizer 中個人化內容
description: 開始使用個人化
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 7be83409f7a594747963c5b125f3bf96c0b4f8b6
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 13%

---

# 開始使用個人化{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] 個人化功能，運用您擁有的相關資料和資訊，讓您的訊息與每個特定收件者相適應。 這可以是他們的名字，興趣，住的地方，他們買的東西，等等。

➡️ [了解如何個人化這些影片中的訊息](#video-perso)

[!DNL Journey Optimizer] 使用 **內嵌** 根據Handlebars的簡單個人化語法，可讓您建立包含雙大括弧內容的運算式 **{{}}**. 您可以在相同的內容或欄位中新增多個運算式，不受限制。 深入了解 [個人化語法](personalization-syntax.md).

根據由 Adobe Experience Platform 定義的 **XDM 個人設定檔**&#x200B;方案管理的設定檔資料進行個人化。 深入了解 [Adobe Experience Platform Data Model(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

>[!CAUTION]
>此 **XDM個別設定檔** 結構是您唯一可用來個人化 [!DNL Journey Optimizer].

**範例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

處理訊息（電子郵件和推播）時，Journey Optimizer會以Experience Cloud平台資料庫中包含的資料取代運算式：  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 變成了&quot;你好，無名氏&quot;


## 個人化內容{#personalization-areas}

傳遞的訊息的內容和顯示 [!DNL Journey Optimizer] 可以透過數種不同的方式進行個人化。

在具有編輯器圖示的每個欄位中，您可以開啟個人化編輯器（也稱為運算式編輯器）並定義個人化。

![](assets/perso_icon.png)

### 個人化您的電子郵件

當您建立電子郵件時，可以在 **[!UICONTROL Subject line]** 欄位。

![](assets/perso_subject.png)

在電子郵件設計工具中，您可以個人化內容：

* 在 **訊息**:按一下文字區塊內的，按一下 **個人化** 圖示並選取 **插入個人化** 欄位。 如需電子郵件設計工具介面的詳細資訊，請參閱 [節](../design-emails.md).

   ![](assets/perso_insert.png)

* 若 **連結**:選取文字區塊內的文字或影像，按一下 **插入連結** 圖示。 在視窗中，您可以按一下 **新增個人化** 表徵圖。

   ![](assets/perso_link.png)

在這兩種情況下，您都可存取個人化編輯器。

![](assets/perso_ee.png)

### 個人化您的推播通知

您也可以將 **推播通知** 在下列欄位中：

* **標題**
* **主體**
* **自訂音效**
* **徽章**
* **自訂資料**

![](assets/perso_push.png)

進一步了解推播通知設定，位於 [本節](../push-gs.md).

### 個人化您的優惠方案 {#personalize-offers}

將文字類型內容新增至選件的表示時，您也可以存取個人化編輯器。

進一步了解如何透過 [本節](../offers/offer-library/creating-personalized-offers.md#custom-text).

## 使用運算式編輯器 {#use-expression-editor}

運算式編輯器是 [!DNL Journey Optimizer].

它適用於您需要定義電子郵件、推送和選件之類個人化的每個內容。

在運算式編輯器介面中，您將選取、排列、自訂及驗證所有資料，以針對您的內容建立自訂個人化。

![](assets/perso_ee1.png)

畫面左側會顯示網域選取器，供您選取個人化來源。

![](assets/perso_ee3.png)

可用來源包括：

* **[!UICONTROL Profile attributes]** :列出與配置檔案架構相關的所有引用，如 [Adobe Experience Platform Data Model(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Segment memberships]** :會列出在Adobe Experience Platform區段服務中建立的所有區段。 可用區段的詳細資訊 [此處](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Offer decisions]** :列出與特定版位相關聯的所有優惠方案。 選取版位，然後在內容中插入優惠方案。 如需如何管理優惠方案的完整檔案，請參閱 [本節](../deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** :當 **訊息** 用於歷程中，您可透過此功能表取得內容歷程欄位。 深入了解 [本節](personalization-use-case.md).
* **[!UICONTROL Helper functions]** :列出所有可用於對資料執行操作的輔助功能，如計算、資料格式或轉換、條件，以及在個人化環境中處理這些功能。 深入了解 [本節](functions/functions.md).

選取時，參考會新增到編輯器中。

>[!NOTE]
>
>「+」圖示旁的資訊圖示會開啟工具提示，提供每個變數的詳細資訊。

在下列範例中，運算式編輯器可讓您選取生日為今天的設定檔，然後透過插入與當天相對應的特定選件來完成自訂。

![](assets/perso_ee2.png)

## 作法影片{#video-perso}

瞭解如何使用歷程中的內容事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

瞭解如何使用歷程中的內容事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
